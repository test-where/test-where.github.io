---
title: "The one with Data-driven decisions"
date: "2023-12-20"
categories: 
  - "posts"
---

- Principle #5 from [Modern Testing principles](https://www.moderntesting.org/) states "We believe that the customer is the only one capable to judge and evaluate the quality of our product." In my opinion, it is closely coupled with principle #6 - "We use data extensively to deeply understand customer usage and then close the gaps between product hypotheses and business impact." As this year I landed in a highly abstract role, I was actively exploring more data-driven decision-making techniques, metrics, developer productivity, developer experience, and other topics that would help me justify my or/and team's efforts and hypotheses, and reduce waste.

- Last week I had some spare time to catch up on the AB testing podcast and episode 189 (more specifically - 8:00-12:15) provided some nice insights into how those principles look like in real-life projects - and what are the potential good signs to look for:
    - "If the PM in charge of the feature <...> has produced their own Power BI that is tracking the performance of the feature, and it is not vanity metrics." - and if not, there is something you can suggest. There are some frameworks (like [TARS](https://uxdesign.cc/tars-a-product-metric-game-changer-c523f260306a) or [HEART](https://uxdesign.cc/googles-heart-framework-choosing-the-right-metrics-for-your-product-112bd7300d55)) that give some ideas of how such telemetry can be implemented in feature level.
    
    - "If I can have a conversation with the PM <...> or anyone and correctly define the difference between a vanity metric and an actionable metric - that is a great sign."
    
    - "If they come to me and say hey we have this **hypothesis**, and this is what we did to validate it, and this is what we think is the result, can you look over and make sure we are OK?" - remember, I wrote about assumptions, hypotheses, and experimentation some time ago? Here is that article again: [Effort, Impact and Experimentation in Testing](https://testwhere.blog/effort-impact-and-experimentation-in-testing/).
    
    - "Seeing visibility of a more formal A/B testing or hypothesis testing type of structure is another great sign."
    
    - ...

- Switching from features (business) to system (technical) level - have you ever heard of [The Four Golden Signals](https://sre.google/sre-book/monitoring-distributed-systems/) (of user-facing systems)? They are latency, traffic, errors, and saturation. "If you can only measure four metrics of your user-facing system, focus on these four." But it is not as simple as it sounds - it is only the beginning of a complex Site Reliability Engineering (SRE) topic. Wanna explore SRE further? Google provides several fine [SRE books for online reading](https://sre.google/books/).

- Continuing with the data-driven topic in the world of DDD, BDD, TDD, and other DDs, Ingo Steinke suggests looking into ["Emotion-driven development"](https://dev.to/ingosteinke/emotion-driven-development-4ai1) treating emotions as signals, as a source of information that can be interpreted in an actionable way. For that, he talks about an interesting technique called "emotion poker".

- Lastly, when I connect the dots between data-driven topic and test automation, the first thing that comes to my mind is an advice from Bas Dijkstra stating that [parametrized E2E tests are an anti-pattern](https://www.linkedin.com/posts/basdijkstra_i-think-parameterized-data-driven-end-to-end-activity-7016663446221934592-KRWk), and I should say I agree to this brave statement.
