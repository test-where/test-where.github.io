---
title: "The one with AI agents and AnythingLLM"
date: "2025-02-23"
---

- A year ago, I was writing [the one about Demos and Persuasion](/2024/02/26/the-one-with-demos-and-persuasion.html) inspired mostly by then recent OpenAI DevDay keynote presentation. That time they demonstrated custom GPTs and it felt amazing to have an assistant tailored to your individual needs, to specific use-cases or acting as a predesigned persona. A lot has changed since then as multiple players entered the race and branched the topics into various directions. However, the directions being discussed the most currently are AI agents, agentic flows, and RAG (retrieval-augmented generation) capabilities. I guess you have heard someone saying that "2025 will be all about AI agents", so what is that all about?

- Recently, I had a chance to attend some training to get to know Google tooling for building AI agents and flows - Agentspace. After a short research on how to try something like that out (without leaving my credit card data for a trial version), I landed with an idea to give a try to another app - [AnythingLLM](https://anythingllm.com/) - as it promised a lot of functionalities with a simple low-code setup. I started by downloading and playing through the desktop app (connected to a local LLM - llama 3.2 3B, 2.0 GB), but soon I noticed that there is a cloud solution that one can run on Docker, so I switched to have more control over the setup, transparency, and more functionality. To tickle your imagination - my setup's client interface looked something like this:
![/images/anythingllm_setup_browser.png](/images/anythingllm_setup_browser.png)

- I will not cover all the AnythingLLM functionality here as they have pretty comprehensive [AnythingLLM documentation](https://docs.anythingllm.com/), but let's say I liked how quickly I am able to setup and tune various things. Some of my findings:
    - AnythingLLM workspaces are extremely easy to adjust (chat prompt (to adjust the persona), temperature, suggested messages, etc.)
    - You can upload documents to get more context to your workspace. However, I had a chance to test it against ChatGPT Projects, so AnythingLLM does not give priority to uploaded content by default while ChatGPT does. Later, I was able to achieve something similar to that expected behavior by adjusting the workspace settings (chat prompt).
    - AnythingLLM agent is far slower than a single prompt (which is logical), lacks accuracy, and does not feel that smart under the hood. But I assume, that is me, learning curve, not the tool - as I was not able to enable all the available agent tools.
    - Roles (yes, cloud solution can have multiple users!) are easy to setup and manage. One thing I missed - more tooling for product discovery. Is my workspace helping the users? Users can press "like" on chat responses, but admin does not get that data.


- Something to explore further:
    - Agents. All their tools. And how to debug them.
    - Building custom agent flows and executing them from the chat.
    - Adding custom agent tools via JavaScript.
    - (Workspace) infrastructure as a code? (and proper CI/CD for solution development)
    - ...


- I feel like AnythingLLM is a nice tool to get some hands-on experience with the topic with a huge ROI. Desktop app setup is easy-peasy, and if you want to get your hands dirty with Docker setup - I have a [ready-to-go setup in this GitHub repo](https://github.com/test-where/anythingllm-setup). Have fun! (I will sure do.)