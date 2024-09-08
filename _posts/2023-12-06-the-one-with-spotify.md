---
title: "The one with Spotify"
date: "2023-12-06"
categories: 
  - "posts"
---

- As the previous week I wrote about the [Advent Calendar of White-box Testing](/advent-calendar-of-white-box-testing/) and other Advent traditions, the beginning of December has countless virtual traditions that suggest reflecting on the year passing in one way or the other. One of such is [Spotify Wrapped](https://newsroom.spotify.com/2023-wrapped/) which sums up your listening habits into several colorful infographics. Such campaigns that appear at a very specific time require thorough load testing, so here's the article on [how Spotify load tested for 2022 Wrapped](https://engineering.atspotify.com/2023/03/load-testing-for-2022-wrapped/).

- Spotify is famous for its modern software engineering practices, innovation, experimentation, work culture... (just read ["The Product Model by Spotify"](https://joakimsunden.com/the-product-model-at-spotify/) by Joakim Sunden and you will get it) Therefore, it's worth exploring [Spotify's engineering blog](https://engineering.atspotify.com/). Or if you want to focus more on quality engineering, there is a nice article focused on quality and productivity topics by [Antoine Craske](https://www.linkedin.com/in/acraske/) about ["Quality Engineering Productivity at Spotify"](https://qeunit.com/blog/quality-engineering-productivity-at-spotify/).  
      
    _“Quickly turn ideas into products and experiment to improve the user experience, growing into new markets, and remaining competitive as a content streaming provider.”_ - somehow reminds me of [Effort, Impact and Experimentation in Testing](/effort-impact-and-experimentation-in-testing/).

- Another interesting piece from Spotify I found some time ago when I was exploring ways how to perform quality assessments in the project space - ["Squad Health Check model"](https://engineering.atspotify.com/2014/09/squad-health-check-model/). (You can easily see the date it was published - so you can see Spotify was experimenting with gamification long before I started my career as a tester...) Some time later I found better and more tailored models for that same purpose, which I actively refer to this day:
    - ["Quality Culture Transition Guide"](https://docs.google.com/spreadsheets/d/1kan20hYsdbvk7HW4si-X6Ve1fLtCeTI2H_PjiniKsxY/edit#gid=1639699416) from [Modern Testing](https://github.com/moderntesting/resources).
    - [Quality Practices Assessment Model (QPAM)](https://leanpub.com/qualityassessmentpracticesmodelqpam) from [Janet Gregory](https://www.linkedin.com/in/janetgregory/) and [Selena Delesie](https://www.linkedin.com/in/selenadelesie/) (which was actually derived from the same "Quality Culture Transition Guide", and described in more detail).

- And at the same time one idealizes their software development practices, work culture, speed, and other fancy things, [they announced layoffs of 17% of their staff](https://edition.cnn.com/2023/12/04/tech/spotify-layoffs-third-round) (~1500 out of 9000+ people). Many people on social media are blaming Spotify for layoffs with a 5-month severance package, but I am not sure what is worse - layoffs here and now or quiet firing. Oh, Bittersweet Symphony...

- But let's not end with a sad note. Let's end _forte_! Something to try out! Let it be about music and AI, and a mix of both - let's try [Facebook's MusicGen model demo available in HuggingFace](https://huggingface.co/spaces/facebook/MusicGen) which generates a 15-second melody out of your text query and (optional) music sample. It takes some time to generate that short melody, but it is surprisingly good. For advanced users, I suggest using [MusicGen Colab space](https://ai.honu.io/red/musicgen-colab) which is faster and has more options. Try it out!
