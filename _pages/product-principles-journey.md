---
layout: page
title: Journey to Product Principles
permalink: /product-principles-journey/
image: /_pages/product-principles/product-pyramid.drawio.svg
---

Note, this journey was covered in a talk - ["Striving in the Gap. Impact Engineering"](https://www.youtube.com/watch?v=-sVasQ1RcbU&ab_channel=QLTYPULSE) (or find the video embed at the bottom of this page).

## Intro

While I was always interested in topics related to testing, quality, critical thinking, the search for proper answers intensified once I gained some experience (and noticed by own experience that some products fail even with good testing in place) and stepped into (then, highly uncertain) role of Testing Practice Lead (a.k.a. Head of Testing). Role uncertainty lead to the following questions:

* How do I know I am successful in the role responsible for testing (or quality?) practices across 40+ projects?
* How do I know testing/quality practices are successful and improving in those 40+ projects?
* How do I know testing/quality practices are successful and improving in a single project?
* How do I make a single team aware of testing/quality practices in their project to spot the gaps on their own and improve proactively?
* ...

Finally, I narrowed all the uncertainty down into two questions - one for software development teams, and one for any product or service (considering my role as a service within the company context):

* How to define and assess quality in the context of software product (and its development team)?
* How to define and assess quality in the context of any product or service?

## Thinking about Metrics (outer, inner, process, etc.)

Getting to understand some metrics felt like a good start. However, one can easily notice that metrics are not equal - North Star metrics like total watch minutes in the context of YouTube, and their trends say a lot more than "vanity metrics" like number of executed test cases. However, not all the metrics are good or bad, black or white. It felt like different metrics are meant for different purposes, so I wanted to find a way how to distribute them across different places where they should be, and check if there are no gaps - if we have all the metrics in all the places.

[Finding Adequate Metrics for Outer, Inner, and Process Quality in Software Development](https://www.infoq.com/articles/metrics-quality-software/) by Michael Kutz was the article that (together with nicely clarifying a lot of things about metrics) introduced that model of Outer, Inner, and Process Quality.

And for quite some time I referenced to that model advocating the importance of thinking about Outer quality, Outer metrics to not build the wrong thing.

![Outer, Inner, Process quality](https://imgopt.infoq.com/fit-in/3000x4000/filters:quality(85)/filters:no_upscale()/articles/metrics-quality-software/en/resources/4figure-5-1673961550238.jpg)

## Effort-Output-Outcome-Impact

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

## Process-Code-System-Product

Later, Google published its research on [Developer Productivity for Humans, Part 7: Software Quality](https://ieeexplore.ieee.org/document/10372494), which aligned nicely with my ongoing journey.

Process-Code-System-Product felt like a perfect mapping of Effort-Output-Outcome-Impact to the context of software engineering.

![Process-Code-System-Product](/images/process-code-system-product.png)

## Maturing

The earlier advice to focus on the right and research to the left in the context of Process-Code-System-Product looked like that:

![Process-Code-System-Product maturity](/images/process-code-system-product-maturity.drawio.svg)

Inspired by [TMMi model](https://www.tmmi.org/tmmi-model/), and understanding that it focuses on processes part mostly (all the critique to the maturity models and process frameworks for disregarding the context and product problems), I was looking into some more modern models with a hope to understand and cover maturity of all 4 parts - process, code, system and product.

Firstly, to [Quality Culture Transition Guide](https://docs.google.com/spreadsheets/d/1kan20hYsdbvk7HW4si-X6Ve1fLtCeTI2H_PjiniKsxY/edit?gid=1897633328#gid=1897633328) by Alan Page...

And later, to [Assessing Agile Quality Practices with QPAM](https://leanpub.com/qualityassessmentpracticesmodelqpam) by Janet Gregory and Selena Delesie, which was built on top of Alan Page's model, refined and described in more detail - as a complete book.

However, QPAM did not cover much of Product part either. The best I found was "quality understanding" which sounded to me like something that shapes over time working in collaboration with other team members, customers and end-users.

But that felt too vague. Based on Modern Testing Principle #5 ("<...> the customer is the only one capable to judge and evaluate the quality of our product") it was clear that "quality understanding" lives in the very right side - at the Product. Therefore, one needed to study Product Strategies, Product Discovery, and other things the Product specialists do.

## Studying Product

Until then, I was familiar with the concept of "Empowered Product teams", I knew some success stories based on such working model. Also, I knew some strong Product specialists who were evangelising the book called "Inspired", however, I have not recalled the name of the author back then.

So, when I decided to study Product in more depth, it took me a few minutes to arrive into Marty Cagan and find a lot of great supporting resources ([SVPG website](https://www.svpg.com/), YouTube videos, books...)

Luckily for me, by the time I arrived to that problem Marty Cagan was releasing his newest book (at that time) - [Transformed: Moving to the Product Operating Model](https://www.goodreads.com/book/show/56465356-transformed), which provided exactly what I needed - a model. Product Operating Model based on 20 priciples across Product Strategy, Product Discovery, Product Delivery, Teamwork, and Culture.

The book is great. Actually, I was listening to the audio book narrated by Marty Cagan himself, and that put some extra flavor on that experience. Typically, I do not listen to audio books, I tend to read written symbols, so listening to an audio book narrated by the author about an unexplored subject was interesting in many levels (I am smiling now only recalling that memory).

Marty Cagan covered a lot of engineering practices, I noticed a lot of overlap with my past experiences in software development, a lot of overlap with the models I already know, with the principles I already live.

It did not took long until I decided to merge 20 Product Operating Model principles together with 10 categories from Agile Quality Practices Assessment.

## Merging Two Worlds

The excercise was simple - draw the respective principles as boxes, and drag-and-drop them across the structure of Teamwork/Process - Code - System - Product, find the overlaps, remove the overhead, crystalize the essence.

[![Merging Models into Product Principles](/_pages/product-principles/product-principles-merging-models.drawio.svg)](/_pages/product-principles/product-principles-merging-models.drawio.svg)

The unexpected thing that crystalized pretty quickly - the fifth group that cannot be put under the initial four ones - Culture.

Another insight that should be made before the final merge - those five categories are not that equal in nature, and it was odd to see them in a linear chain. It is not like that. It is more like the following:

* Code creates systems, and systems creates products.

* Processes are everywhere - around code, systems, and product.

* Culture shapes processes. Therefore, culture surrounds everything.

![](/_pages/product-principles/product-system-code-process-culture.drawio.svg){:width="400px"}

## Product Principles

Final result after merging - **Product Principles**, where ultimate goal is the Product Quality:

![Product Principles](/_pages/product-principles/product-principles.drawio.svg)

Or, if you wish - **Product Pyramid**:

![Product Pyramid](/_pages/product-principles/product-pyramid.drawio.svg)

* **Product should define "Quality Understanding".** Product (and especially - Focus) is at the top and sets the direction for everything. Product is window to the outside, the real world, the truth.

* **Culture is foundation.** Culture is like opinions. And, "opinions are like a\*\*holes - everyone has one (but they think each others stink)." So, everyone coming to the table brings their culture with them, and that is something to deal with.

    Even though culture is at the bottom, it diffuses everywhere. Solving any other problem can be temporary, if the root cause is in culture.

* **Engineering lives in between.** Systems, Code, Processes and Teamwork are in the middle between Product and Culture. Understanding the influence from Product and Culture, and associated risks should give motivation to influence back - study those topics, discuss them with leaders (culture) and product specialists, clarify the risks, drive/support risk mitigation.

End of journey. Just joking - journey never ends.

Please find more details behind each principle in [Product Principles](/product-principles/) page.

## Video

Talk that covers the journey.

<center><iframe width="560" height="315" src="https://www.youtube.com/embed/-sVasQ1RcbU?si=LqXhW1DbynkgQdW-&amp;controls=0" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe></center>