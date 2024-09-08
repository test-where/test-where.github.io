---
title: Waiting in Test Automation
permalink: /waiting-in-test-automation/
---

Waiting is a very common practice in test automation and automation in general as a lot of times automation is faster than its object (i.e. web application), therefore, automation needs to know how to wait for the object to be ready for some next step.

A very common problem in modern web application test automation is flaky tests (inconsistent results under the same circumstances, false positives). Most (if not all) of the time flaky test means that its author does not have a full understanding of what is happening in some particular situations (or how to resolve it).

Understanding is critical in some other situations as well.

Another problem in test automation is when failures occur due to a slight change in circumstances or environments (i.e. test works fine on the local computer, but fails constantly in the CI/CD pipeline). That also indicates that the author lacks understanding of what is the difference exactly. (Sometimes it may be a valid bug in the system, but) A lot of times (after finding out how to reproduce and debugging) it appears that automation needs to wait for some resource to load, some status to change in case of a worse network, its constraints, or something else.

To fight flaky tests, creators of some commercial tools suggest using a retry mechanism as most of the time retrying the same test will succeed on a second or later attempt. Yes, it is easier to go that way, and it may stabilize your test suite, but it will not provide you further understanding and confidence in whatever you are doing. It is not progress, it is a workaround with the same known unknown remaining, pure ignorance, and poor care. Therefore, instead of such a "global retry" approach (retrying a whole test), a better alternative is to gain an understanding of what is actually causing the issue and fix it with a "local retry" approach - identify, isolate, and suppress only this situation, and maybe it will not appear on the next iteration.

### Local retry approach for waiting

Instead of retrying the whole test, the local retry approach suggests retrying only within the scope that does not meet some particular condition yet. The most popular example probably is waiting for a web element to appear, and various browser drivers already have their proposed wait mechanisms built-in (and that is fine). But sometimes test script may need to wait for some specific file to appear in some folder, some specific status to be set in respective database entry, or even a specific combo of multiple conditions.

To have the flexibility to use the following waiting mechanism for various purposes across multiple drivers, clients, and integrations and to provide custom debugging and logging capabilities for some complex cases (see nested waiting example below), a better approach would be to have a simple custom method for waiting.

This is a sample method you can store in some static class or extension to handle waiting in test automation:

```csharp
public static void WaitFor(Func<(bool result, Exception exception)> action, double timeoutInSecs = DefaultTimeoutInSeconds)
{
	var start = DateTime.Now;
	var actionResult = false;
	Exception actionException = null;
	var iteration = 0;
	while ((DateTime.Now - start).TotalSeconds < timeoutInSecs || iteration < 1)
	{
		var outcome = action();
		actionResult = outcome.result;
		actionException = outcome.exception;
		if (actionResult)
		{
			break;
		}
		Thread.Sleep(500);
		iteration++;
	}
	if (!actionResult)
	{
		var outputMessage = $"Action returned false after timeout (in {iteration} tries)";
		Exception outputException = actionException == null
			? new TimeoutException(outputMessage)
			: new TimeoutException(outputMessage, actionException);
		throw outputException;
	}
}
```

Code snippet taken from: [DotNetVisualTesting.Core/WaitHelpers.cs](https://github.com/justlauzadis/dotnet-visual-testing/blob/main/DotNetVisualTesting.Core/WaitHelpers.cs)

Then, such helper method can be used in automation logic like this:

```csharp
WaitHelpers.WaitFor(() =>
{
	try
	{
		// here should go some actions to perform
		
		// and if everything goes well, then...
		return (true, null);
	}
	catch (SomeSpecificKnownException ex)
	{
		// but if your action throws
		// some known specific exception
		// for specific and known reason
		// 
		return (false, ex);
	}
}, timeoutInSeconds);
```

The important part in such a construct is that the catch clause will be handling only a well-known and narrowly defined situation that throws SomeSpecificKnownException (if there is a need to be more specific, more details may be added to condition), and all the other failures will be still thrown as a new information for further investigation.

### Dangers of too global retry

It is very important to be very specific and not to suppress unknown unknowns that may exist now or may be introduced in the future. If retry is suppressing too much (i.e. "global retry" approach or not enough specific catch block) some new findings (i.e. valid low probability race condition bug) can be not reported at all.

### Dangers of nested waiting

Another danger when stabilizing test automation with such waiting mechanisms is when such methods start to conflict due to being nested, especially, when similar timeout lengths are applied (and that is very common and easy to get into). In such case, the inner wait can timeout and that will not give a second chance (second iteration) for the outer wait because the outer wait will be hitting its timeout already as well. And that can easily happen if the success of the inner wait depends on some prerequisites from the outer wait scope (i.e. SomeAction() method):

```csharp
WaitHelpers.WaitFor(() =>
{
	SomeAction();
	WaitHelpers.WaitFor(() =>
	{
		
	}, timeoutInSeconds);
	SomeAnotherAction();
	return (true, null);
	
}, timeoutInSeconds);
```

In POM or other object-oriented patterns, such wait mechanisms become a part of many larger methods. Therefore, nested waiting becomes not so easy to spot:

```csharp
WaitHelpers.WaitFor(() =>
{
	SomeActionContainingSimilarWaitInside();
	return (true, null);
	
}, timeoutInSeconds);
```

That is why in case of timeouts it is important to log a number of iterations - in case of timeouts in nested waiting, the stack trace will log multiple chained TimeoutExceptions (always add _innerExceptions_ for debugging!), and if any of them indicates only single iteration was performed, that might be a signal to investigate a possible issue due to nested waiting there.

A solution for such situations is simple - inner waits should have shorter timeouts, so the outer wait will be able to have another iteration, another try. And regarding the timeout proportions, there is no silver bullet as they may highly depend on the nature of processes being automated.

### Conclusion

This article provides practical advise how to handle waiting in test automation, and some common pitfalls. Thinking about how to deal with known unknowns and yet unknown unknowns in long-term drives to a conclusion that waiting mechanisms need to be applied carefully, narrowly and specifically to the situation it is solving. Finally, it is worth remembering that "green tests" are only a part of the goal, but continuously improving your understanding and confidence that those "green tests" are not missing out on something important is a lot more critical.
