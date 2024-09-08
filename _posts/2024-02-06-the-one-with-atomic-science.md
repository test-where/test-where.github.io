---
title: "The one with Atomic Science"
date: "2024-02-06"
categories: 
  - "posts"
---

- Research is often fascinating. Therefore, I was excited to find yet another insightful research paper - Microsoft's [The New Future of Work report](https://www.microsoft.com/en-us/research/project/the-new-future-of-work/overview/). It reviews the year 2023 focusing mostly on AI and LLM advancements. It concludes some interesting points (and provides more resources and references for a deeper study):
    - "Analyzing and integrating may become more important skills than searching and creating." Not gonna say it is surprising as I hear more and more speculations that testing (as a general term for any kind of analysis to support decision-making) is not going away because of gen-AI advancements (while coding as we know it might be in danger).
    - "Appropriate reliance on AI is a key challenge in human-AI interaction." Very similar conclusion to the one from [Testing and gen-AI, LLMs – why will testing not go away?](/testing-and-gen-ai-llms-why-will-testing-not-go-away/) article. It looks like I am not the only one with trust issues.
    - "Instant AI feedback may improve real-time interactions in meetings." It would be interesting to see how AI may assist in meetings, for example, to achieve more equal participation.
    - "Critical thinking: LLM-based tools can be useful provocateurs." The risk I see here is to fall into the traps of availability/confirmation biases. To mitigate it, do not start with LLM output - come up with your ideas first, and validate them later by asking LLM to deal with a similar challenge. Only then compare the results and see if you have not missed something the LLM pointed out.
    - "Call to action: Lead like a scientist." Embracing the experimentation, and research. More and more fields (product management, developer experience, developer productivity, DORA research, A/B testing, UX/design, etc.) are talking the same already. Small and frequent experiments are critical to identify, quantify, and understand the value and impact behind our efforts (you can read more in detail here - [Effort, Impact and Experimentation in Testing](/effort-impact-and-experimentation-in-testing/)).

<figure>

![](https://testwhere.wordpress.com/wp-content/uploads/2024/02/image.png?w=1024)

<figcaption>

The last slide from [Microsoft New Future of Work Report](https://www.microsoft.com/en-us/research/uploads/prod/2023/12/NewFutureOfWork_Report2023.pdf)

</figcaption>

</figure>

- Another interesting find was an [ATOM model for automation](https://www.automatetheplanet.com/atom-model-optimization/) from the [Automate The Planet newsletter](https://www.linkedin.com/newsletters/automate-the-planet-weekly-7054059427556929536/). The more models I study, the more I like the ones that provide a few relatively simple rules and/or visuals to stimulate thinking instead of a lot of low-level details involving calculations. I know the devil can be and is in the details, but the purpose of such models should be to simplify and help explain, and not to complicate things. Therefore, getting back to the ATOM model, it looks like lacking a high-level rationale and structure. When it starts from the low level, I start wondering whether we are not missing something from the big picture.

- Talking about atomic things - probably you know the book called ["Atomic Habits"](https://www.amazon.com/Atomic-Habits-Proven-Build-Break/dp/0735211299). Over the years I recognized I developed a lot of small habits in my workflows. Some (or most?) of them were related to reminders in one or the other form as I really like to free my physical memory and store notes as reminders in some digital format to pop up tomorrow at 9AM or on Monday. And sometimes when you have such atomic comfortable things boosting your productivity, you do not even recognize how much power they hold. But when you lose them (and need to find an alternative that is simply not the same), then you really start recognizing the power of such atomic habits, and how much productivity they brought. That is not how I imagine getting out of my comfort zone.

- Another thing that comes to my mind when I think about the word "atomic" is tests. Atomic, independent, and descriptive are [3 characteristics of a sustainable test automation garden](https://medium.com/detesters/characteristics-of-a-sustainable-test-automation-garden-f4132bf12e68). However, my experience tells me that at higher levels (API, E2E) atomic tests should go hand in hand with wider scope full flow/scenario tests. While "atomic" suggests deriving your test design from system structure (units, components), and that can play well in identifying what is failing exactly, on the other hand, too much focus on separate units can break some integrations without noticing. Furthermore, atomic tests may not notice that full flow got extended with a new step or a new branch/path.

- Lastly, let's end this issue with an artistic note - an inspiring song (and its [video](https://www.youtube.com/watch?v=r9O2RNqAYao&ab_channel=THEROOP) starting with an explosion of the atomic bomb) - as The Roop dropped yet another bomb. However, its melody, vocals, and lyrics resonated highly with current emotional background, uncertainty, stoic thoughts, and need to focus on something small that is in our control. Something we can do on our own with quality and the level of detail we own. And accepting that it is enough.  
      
    "All my life  
    I've been thinking I need something more  
    Now I'm fine  
    I'm enough with my own simple joy"