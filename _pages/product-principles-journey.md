---
layout: page
title: Journey to Product Principles
permalink: /product-principles-journey/
image: /_pages/product-principles/product-pyramid.drawio.svg
---

While I was always interested in topics related to testing, quality, critical thinking, the search for proper answers intensified once I gained some experience (and noticed by own experience that some products fail even with good testing in place) and stepped into (then, highly uncertain) role of Testing Practice Lead (a.k.a. Head of Testing). Role uncertainty lead to the following questions:

* How do I know I am successful in the role responsible for testing (or quality?) practices across 40+ projects?
* How do I know testing/quality practices are successful and improving in those 40+ projects?
* How do I know testing/quality practices are successful and improving in a single project?
* How do I make a single team aware of testing/quality practices in their project to spot the gaps on their own and improve proactively?
* ...

Finally, I narrowed all the uncertainty down into two questions - one for software development teams, and one for any product or service (considering my role as a service within the company context):

* How to define and assess quality in the context of software product (and its development team)?
* How to define and assess quality in the context of any product or service?

### Thinking about Metrics (outer, inner, process, etc.)

Getting to understand some metrics felt like a good start. However, one can easily notice that metrics are not equal - North Star metrics like total watch minutes in the context of YouTube, and their trends say a lot more than "vanity metrics" like number of executed test cases. However, not all the metrics are good or bad, black or white. It felt like different metrics are meant for different purposes, so I wanted to find a way how to distribute them across different places where they should be, and check if there are no gaps - if we have all the metrics in all the places.

[Finding Adequate Metrics for Outer, Inner, and Process Quality in Software Development](https://www.infoq.com/articles/metrics-quality-software/) by Michael Kutz was the article that (together with nicely clarifying a lot of things about metrics) introduced that model of Outer, Inner, and Process Quality.

And for quite some time I referenced to that model advocating the importance of thinking about Outer quality, Outer metrics to not build the wrong thing.

![Outer, Inner, Process quality](https://imgopt.infoq.com/fit-in/3000x4000/filters:quality(85)/filters:no_upscale()/articles/metrics-quality-software/en/resources/4figure-5-1673961550238.jpg)

### Effort-Output-Outcome-Impact

![Effort-output-outcome-impact](/images/effort-output-outcome-impact.drawio.svg)

[Measuring developer productivity? A response to McKinsey](https://newsletter.pragmaticengineer.com/p/measuring-developer-productivity) by The Pragmatic Engineer was the article that introduced Effort-Output-Outcome-Impact model to me and summed up the productivity topic in general. It provides some nice examples as well as some great advice, like:

> When you measure in the open, aim for team outcomes and impact, not effort and output. People will figure out how to “game” what you measure, and optimize for this. Here’s what happens when you measure each of the areas:
>
> * Measure effort: create high-effort busywork of dubious value
>
> * Measure output: increase the quantity of the output by what’s easiest to do. This might not help with outcomes or impact.
>
> * Measure outcomes: aim to beat targets, even if this means taking shortcuts
>
> * Measure impact: get creative in reaching this with less effort and output
>
> Don’t ignore the effort and output people and teams produce, though! Instead of measuring them, use this to debug issues with outcomes or impact.

So, it was clear to focus on the right, and research to the left - how one's efforts ripple towards some measurable impact. More precisely, how efforts ripple to outputs that ripple to outcomes that ripple to impact.

Exploring my role responsibilities and its relationships to other functions within the organization and guided by the structure of Effort-Output-Outcome-Impact, I was able to sketch some helpful [impact maps](https://www.impactmapping.org/).

Later, I noticed similar 4 categories apply in the context of software development as well, and inspired by this model I wrote ["Effort, Impact, and Experimentation in Testing"](/effort-impact-and-experimentation-in-testing/).

### Process-Code-System-Product

Later, Google published its research on [Developer Productivity for Humans, Part 7: Software Quality](https://ieeexplore.ieee.org/document/10372494), which aligned nicely with my ongoing journey.

Process-Code-System-Product felt like a perfect mapping of Effort-Output-Outcome-Impact to the context of software engineering.

![Process-Code-System-Product](/images/process-code-system-product.png)

### Maturing

The earlier advice to focus on the right and research to the left in the context of Process-Code-System-Product looked like that:

![Process-Code-System-Product maturity](/images/process-code-system-product-maturity.drawio.svg)

[TMMi](https://www.tmmi.org/tmmi-model/) model

[Assessing Agile Quality Practices with QPAM](https://leanpub.com/qualityassessmentpracticesmodelqpam) by Janet Gregory and Selena Delesie

[Quality Culture Transition Guide](https://docs.google.com/spreadsheets/d/1kan20hYsdbvk7HW4si-X6Ve1fLtCeTI2H_PjiniKsxY/edit?gid=1897633328#gid=1897633328) by Alan Page

### Studying Product

[Transformed: Moving to the Product Operating Model](https://www.goodreads.com/book/show/56465356-transformed) by Marty Cagan

### Merging Assessments

[![Merging Models into Product Principles](/_pages/product-principles/product-principles-merging-models.drawio.svg)](/_pages/product-principles/product-principles-merging-models.drawio.svg)

### Product Principles

Final result - **Product Principles**, where ultimate goal is the Product Quality:

![Product Principles](/_pages/product-principles/product-principles.drawio.svg)

Or, if you wish - **Product Pyramid**:

![Product Pyramid](/_pages/product-principles/product-pyramid.drawio.svg)

End of journey. Please find more details behind each principle in [Product Principles](/product-principles/) page.