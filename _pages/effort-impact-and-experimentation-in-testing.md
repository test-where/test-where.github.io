---
title: Effort, Impact and Experimentation in Testing
permalink: /effort-impact-and-experimentation-in-testing/
---

This article aims to explain how effort-output-outcome-impact model and experimentation can be used together to build a better understanding about value and impact in software engineering.

### Effort-Output-Outcome-Impact model

![Effort-Output-Outcome-Impact](/images/effort-output-outcome-impact.drawio.svg)

The following material is based on effort-output-outcome-impact model from  
["Measuring developer productivity? A response to McKinsey"](https://newsletter.pragmaticengineer.com/p/measuring-developer-productivity) and  
["Measuring developer productivity? A response to McKinsey, Part 2"](https://newsletter.pragmaticengineer.com/p/measuring-developer-productivity-part-2),  
therefore, please read those articles first as they clarify a lot of engineering productivity (and its measurement) related topics already.

### Adaptation for quality engineering and testing

Not sure if that is really an adaptation as very similar principles apply:

> **When you measure in the open, aim for** _**team**_ **outcomes and impact, not effort and output.** People will figure out how to “game” what you measure, and optimize for this. Here’s what happens when you measure each of the areas:
> 
> - Measure effort: create high-effort busywork of dubious value
> 
> - Measure output: increase the quantity of the output by what’s easiest to do. This might not help with outcomes or impact.
> 
> - Measure outcomes: aim to beat targets, even if this means taking shortcuts
> 
> - Measure impact: get creative in reaching this with less effort and output
> 
> Don’t ignore the effort and output people and teams produce, though! Instead of measuring them, use this to debug issues with outcomes or impact.
> 
> \- ["Measuring developer productivity? A response to McKinsey, Part 2"](https://newsletter.pragmaticengineer.com/p/measuring-developer-productivity-part-2)

Therefore, when considering various typical quality metrics it is worth understanding whether such metrics will be measuring more of our efforts and outputs, or outcomes and impact.

<table><tbody><tr><td><strong>Effort</strong><br>(tasks and time spent on them, process)</td><td><strong>Output</strong><br>(software code and related deliverables)</td><td><strong>Outcome</strong><br>(product in use/live)</td><td><strong>Impact</strong><br>(impact on business and users)</td></tr><tr><td>Story points?<br><br>"Vanity metrics":<br><br>- number of test cases (or test coverage)<br><br>- number of defects reported (defect removal efficiency, etc.)</td><td>Static code analysis (code smells, complexity metrics, etc.)<br><br>Technical debt<br><br>Code coverage? Requirements coverage?<br><br>Documentation and other deliverables' quality</td><td>SLA/SLO agreements (SRE)<br><br>Non-functional requirements<br><br>Lead Time for Changes (DORA)<br><br>Deployment Frequency (DORA)<br><br>Time to Restore Service (DORA)</td><td><a href="/business-success-metrics/">Business Success metrics</a> (Product Charter, North Star?)<br><br>End-users satisfaction (<a href="https://uxdesign.cc/tars-a-product-metric-game-changer-c523f260306a">TARS</a>, <a href="https://uxdesign.cc/googles-heart-framework-choosing-the-right-metrics-for-your-product-112bd7300d55">HEART</a>, user reviews, etc.)<br><br>Success Failure Rate (DORA)</td></tr></tbody></table>

When a team designs strategies for a project, it should start from the right-side (impact) and make decisions to the left based on what is already known in the right.

You can do an exercise and map down the measurements you are using in your project. If most of them appear in the left (effort, outputs), then that may be a sign you lack understanding and/or alignment on the impact to business.

### Experimentation

"Good tester thinks like a scientist."

Good testing treats information carefully - it tends to spot assumptions (and risks behind them), treat them as hypotheses, and design and perform experiments (a.k.a. tests) to confirm or bust them.

Good example of experimentation in practice is DORA research. First, they build huge models based on their assumptions (hypotheses) about individual, team and organizational aspects. Then, they design and run a survey to collect as much data as possible. Finally, they analyze the collected data and see whether they can confirm or bust their hypotheses (and compose an amazing "State of DevOps Report" for the community).

![](https://testwhere.wordpress.com/wp-content/uploads/2023/11/image-1.png?w=779)
An example of how a diagram can be used to visualize hypotheses (from ["Accelerate State of DevOps Report 2023"](https://services.google.com/fh/files/misc/2023_final_report_sodr.pdf)), where "+" means positive effect

Another model to think about experimentation is Measure, Design, Try:

![](https://testwhere.wordpress.com/wp-content/uploads/2023/11/image-8.png?w=593)
Measure, Design, Try model is widely applied in Academic and User Researches (from ["Measure, Design, Try: On Building New Things"](https://danyelfisher.info/blog/2023/10/5/measure-design-try-on-building-new-things))

Experimentation principles can and should be applied to software engineering as well. Similarly to an example model from DORA research, effort/output/outcome/impact model can be translated into a series of hypotheses (and experiments):

![](https://testwhere.wordpress.com/wp-content/uploads/2023/11/image-2.png?w=856)

1. **Effort -> Output.** Developers' effort (tasks and time spent on them) translates into their outputs (software code and related deliverables), and to find out their quality team runs a number of experiments like unit tests, integration tests, static code analysis, E2E tests and so on.  
    (Note, effort is spent not only on coding, but also on building a better understanding about requirements, tech-debt, big-picture, business problem, impact, etc. as such understanding helps to avoid rework and move faster -> higher productivity.)  
    

3. **Output -> Outcome.** At some point, outputs (respective software code) are deployed to production environment (or get enabled via feature toggle) to be accessible for end-users. Team runs a number of experiments (immediately and continuously) via telemetry and monitoring to make sure the services are running smoothly as intended. Sometimes, such experiments can be described simply as "dashboards look like expected."  
    

5. **Outcome -> Impact.** After a reasonable amount of time since that new feature or change became accessible, team checks whether their hypotheses about causing an impact have proven to be right - team reviews respective business success metrics or user-satisfaction metrics to identify the impact. A/B testing can be used to isolate the impact.

### The most important test

> "The product is a solution. If the problem isn’t solved, the product doesn’t work."
> 
> \- Principle #5 from [Context Driven Testing Principles](https://context-driven-testing.com/).

The most important problem in the project is the business problem the product is solving. The product aims to provide a solution to that problem, but be careful - that is an assumption (or hypothesis). Therefore, we arrive to the most important test (or experiment) - to examine the solution (outcome) to see whether it is actually solving the business problem (whether it makes an impact).

> "One of the biggest hurdles to delivering something valuable is assuming the idea is valuable. Instead, we should treat the idea as a value hypothesis."
> 
> \- ["5-Minute DevOps: The Three Wrongs" by Bryan Finster](https://medium.com/defense-unicorns/5-minute-devops-the-three-wrongs-6c660f1287e7)

In other words, **the most important tests are in the part #3 (Outcome -> Impact)**. That does not mean that parts #1 and #2 are somehow less important - they cannot be skipped, their quality may transform into higher or lower impact to business or end-users, so typically, they will be done first and with more investment than #3. But still, experiments for part #3 should be carried out and cannot be forgotten or worse - assumed.

Measurable impact to business not only justifies developer productivity, but also works as a feedback loop to the engineering team - informing whether and how team efforts actually translates into business value. Testing the impact (similarly as testing the outcomes and outputs) leads to better understanding and directs team effort towards less rework and faster delivery, therefore, higher productivity.

![](https://testwhere.wordpress.com/wp-content/uploads/2023/11/image-5.png?w=856)