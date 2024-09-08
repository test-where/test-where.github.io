---
title: "The one with Marty, Rabbit and Trivia"
date: "2024-01-29"
categories: 
  - "posts"
---

- The week before [I wrote about TMMi](/posts/2024/01/21/the-one-where-i-never-knew-tmmi.html) and the last week I was already exploring how to combine maturity models/levels together with 4 qualities from [Google's "theory of quality"](/posts/2024/01/07/the-one-with-googles-theory-of-quality.html) or the famous [effort/output/outcome/impact model](/effort-impact-and-experimentation-in-testing/). Actually, I have started working on some draft ideas about it already. But then, I noticed a canyon-wide knowledge gap in the world of 4 qualities and their tensions between traditional (command and control) and emerging modern practices - I recognized, that I don't know much about "empowered product teams" (in contrast to traditional command-and-control product management). Luckily, not so long ago my nine-to-five colleague shared [a nice speech given by Marty Cagan on "10 Major Misconceptions About Product"](https://www.youtube.com/watch?v=Do11ib8bBUM&ab_channel=DanOlsen). As I never remember authors by name until I dig into some of their masterpieces, I did not initially recognize Marty Cagan. So I googled. And apparently, he is actually the author behind the books called "Inspired", "Empowered", "Loved" and "Transformed". It rang a bell, as the first two books were already in my Kindle (waiting for better times, a.k.a. reading motivation). So, that time has come - I started the "Empowered" the same evening.

- Maaret Pyhäjärvi shared [her story about 5000 test cases](https://www.linkedin.com/posts/maaret_two-years-ago-i-inherited-a-legacy-project-activity-7154570299143860224-lZ0-/) and their decision to "leave those tests behind and do exploratory testing". Who am I to question the Maaret team's decisions, leaving out 5000 test cases sounds wrong to me. I cannot imagine a document or other storage unit containing 5000 test cases (and all their respective steps) that would not be somehow grouped into epics, features, sub-features, or other taxonomy/hierarchy. I don't know the full context, but I believe we can learn from that story. If you have 5000 test cases (or another big piece of valuable information), make it user-friendly. Make it beginner-friendly, easily explorable, and navigatable. So, 5000 test cases can fall under 200 features under 10-15 epics. If you see the list of 10-15 epics and can understand their intent in the product context, that is a rather good starting point, and you can go deeper from here into features, and then into test cases. Talking about test cases - their naming is another problem and my experience says that it is a good idea to think about A --> Z sorting when coming up with a naming convention. Good naming like  
    "LoginComponent\_ReturnsSuccessAndRedirects\_AfterSubmittingValidCredentials"  
    falls nicely into groups of similar expected behavior even within the same folder (test suite/feature) allowing the test engineer to spot missing test cases more easily. Also, in most cases, such a name is just enough to get the full picture of what such a test case should do, so describing all the exact steps (which is maintenance hell) is not really needed.

- Some time ago in [Testing and gen-AI, LLMs – why will testing not go away?](/testing-and-gen-ai-llms-why-will-testing-not-go-away/) I wrote about how we cannot really trust in gen-AI, and therefore in their testing abilities. But who said we can trust in human specialists? This week I had a chance to discuss some post-mortem findings with another test engineer, and as we speculated on how the development process could be improved we counted 3 or 4 places where the team may have caught the issue, but somehow the decisions in those 3-4 situations were insufficient. What I am trying to say is that in a modern software development team the QA/QE processes (decisions) are layered and overlapping, so it usually takes multiple errors to bypass an issue to production - and one error is not enough. And that is good as it takes some of the responsibility of the engineering shoulders. It is a game of probabilities, and humans should not be perfect to contribute, so maybe we should not expect gen-AI to be perfect either. That was my point in another discussion about a team of gen-AI agents working together in the roles of a software developer team. But without a demo, all we can do is speculate. Therefore, it would be interesting to see a demo of such a setup of multiple agents working together as a group, refining each other's work towards the best results. No demo yet?

- Talking about AI - have you heard of [Rabbit R1](https://www.rabbit.tech/) yet? If not, you should see the keynote demo of the 200-dollar device itself, and even more interestingly (for me as a test engineer) - [their concept of LAM (large actions model)](https://www.youtube.com/watch?v=o2lKl7RMb3Y&ab_channel=MisterZeitgeist) - which at first looks familiar to some record-playback tool, but knowing its AI nature, it's getting really exciting thinking about its possibilities (and capabilities for (test) automation on various interfaces - web, mobile, desktop). Interesting times, huh?

- Finally, last week [the first episode of PAK'torina](https://www.youtube.com/watch?v=JA9O1iGAbDc&ab_channel=PokalbiaiApieKokyb%C4%99) (trivia about testing) aired on YouTube. I will not spoil how it went (but hopefully, if all goes well, I will get back for one more game there sometime later, fingers crossed). Honestly, I am a fan of such trivia games. I was involved much more in my university days - both as a player and as an organizer - so it was really nice to feel that competitive tension and excitement again (as I do not have so many chances currently). Lastly, PAK'torina reminded me of [another trivia on national TV (back in 2011)](https://www.youtube.com/watch?v=hoxVQP3Uju0&t=192s&ab_channel=1000Vaikai) where they got me. Oh boy, that aged... hm... well, I guess?