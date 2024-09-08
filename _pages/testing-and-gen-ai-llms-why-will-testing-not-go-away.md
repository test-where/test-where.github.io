---
title: Testing and gen-AI, LLMs - why will testing not go away?
permalink: /testing-and-gen-ai-llms-why-will-testing-not-go-away/
---

This article aims to explain how the essence of testing is to build trust and confidence, how humans achieve that, and why gen-AI models are unable to create that trust in them. Finally, it aims not to discredit gen-AI in testing, but seeks to understand it better and to provide clarity about their constraints and advantages.

### What is testing?

Let's think about testing - not about what testers do, but about testing as an activity everyone can perform. And I think that everyone performs testing already to some extent.

- When one writes a paragraph to publish for wider audience, they think about its impact, about how it may be read by others, they may ask for some friend to review it, or even use tools like ChatGPT, Grammarly or others to refine that paragraph. This will be less time consuming for a friendly conversation in chat, and likely more time consuming if that message goes for their company engineers.

- When one plans a trip, they think about what's important, what are associated risks, what are main goals for that trip. Preparation for 15-minute Uber ride will likely be a lot simpler than planning a trip to Everest.

- When one develops a device for others to use, they think about a lot of things, and that really depends on the specifics of that device, its context, potential user-base, and a lot of other factors. However, based on potential impact and risks, such examination can be very different - Apollo space shuttles have been examined a lot more thoroughly than you would examine a paper plane you have folded for your kid to play.

- ...

When we build things for ourselves or others, when we are planning some events, when we are about to make some decision, we test, we all do. We think, we research, we simulate various situations, and examine possible options physically or in our minds. This is testing, and I assume we all do that to some extent. We proceed with some decisions only after thinking about them, after applying some testing, some examination, some experimentation, and based on potential impact and risks, we apply more or less effort for testing. Otherwise, not testing a complex, highly risky, and yet very impactful idea (or testing it poorly) could end up in blindly stupid decision-making.

And, poor testing is often a result of missing some context, not understanding the complexity, related risks or possible impacts, impacted parties (or simply not caring). Typically, higher risks and higher impacts transform into more testing to collect enough information, enough understanding, to build enough confidence and trust in the upcoming decision.

So, let's generalize:

**Testing aims to examine an idea and to provide information to build trust and confidence for decision making.**

### How do people build trust in other people and their decisions?

Building trust in other people is a complex and gradual process that involves a combination of factors and behaviors. Here are some key elements that contribute to building trust:

1. **Consistency:** Consistent behavior over time helps establish trust. When people can predict how you will act or respond in different situations, it creates a sense of reliability.

3. **Reliability:** Being reliable and fulfilling your commitments fosters trust. If you consistently follow through on your promises and responsibilities, others are more likely to trust you.

5. **Open Communication:** Transparent and open communication is crucial for trust. Sharing information, thoughts, and feelings honestly helps build a foundation of trust. Avoiding deception and being straightforward contributes to trustworthiness.

7. **Integrity:** Acting with integrity, adhering to a strong set of principles and values, and being honest even when it's difficult are essential components of building trust. People are more likely to trust those who demonstrate high moral character.

9. **Empathy:** Demonstrating empathy and understanding others' perspectives fosters trust. When people feel that you genuinely care about their feelings and concerns, they are more likely to trust you.

11. **Competence:** Demonstrating competence in your abilities and skills builds trust. People are more likely to trust those who are knowledgeable and capable in their respective fields.

13. **Accountability:** Taking responsibility for your actions, admitting mistakes, and making amends when necessary contribute to trust. Accountability shows that you are reliable and committed to rectifying any issues that may arise.

15. **Respect:** Treating others with respect and showing that you value their opinions and contributions is fundamental to trust. Mutual respect forms the basis for healthy relationships.

17. **Dependability:** Being there for others when they need support helps build trust. Dependability involves being a reliable and consistent presence in others' lives.

19. **Shared Experiences:** Going through challenging or positive experiences together can strengthen trust. Shared experiences create a sense of connection and solidarity.

It is important to note that building trust takes time, and it can be easily damaged if there are breaches in any of these elements. Trust is a two-way street, and both parties in a relationship must actively contribute to its development and maintenance.

### How do people build trust in gen-AI models and their outputs?

Knock knock! Who is there? Generative AI model to replace you in testing.

If so, let's examine the generative AI model (having ChatGPT as an example in mind) against the same criteria:

1. **Consistency:** It is a fair thing to expect consistency from the gen-AI model performing testing. However, researchers still report that both ChatGPT 3 and ChatGPT 4 ["frequently fall short of generating logically consistent predictions"](https://arxiv.org/abs/2303.06273). Note - "predictions" is a very precise word to describe the output of LLMs due to their predictive nature.

3. **Reliability:** Several elements that harms LLM reliability:
    - LLM structure (neural network) is very complex, so it is treated as a black-box. Therefore, given its interface of free-form input and free-form output, it is close to impossible to understand its reliability using conventional black-box testing techniques.
    
    - LLM specific reliability issues like [cognitive biases in evaluations](https://arxiv.org/abs/2309.17012), hallucinations, extrapolating the context (incorrect assumptions taken as a fact), etc. See a comprehensive list of [LLM syndromes](https://developsense.com/large-language-model-syndromes).

5. **Open Communication:** Gen-AI outputs depend a lot on their inputs (and there is a big buzz around ["prompt engineering"](https://platform.openai.com/docs/guides/prompt-engineering) because of that). So, input can be adjusted to generate an openly sounding output, but that is more the result of fine-tuning the model and inputs than the real intent to explain the structure of the thinking process. I am not sure if we can discuss about model's intent at all.

7. **Integrity:** Moral principles and values of a machine? Or its creators? If so, it is a lot easier to trust a single person than a huge corporation that built a piece of machinery.

9. **Empathy:** Initially, it feels like machines cannot be empathetic, but the more I think about that, the more I doubt that this is only a human trait. When you try to translate empathy into algorithms, it is all about reading and interpreting human signals - physical, social, psychological, body language, etc. - putting yourself into other's shoes, thinking from different perspectives, and impersonating mentally. Not only ChatGPT, but Grammarly as well can capture and score the tone of your sentence leading to interpreting your mood as part of the input context. Furthermore, considering how many people struggle to be empathetic, and all those countless methods to collect human-centric information in the era of IoT, I feel like machines may have an advantage in this field soon.

11. **Competence:** Knowing the predictive nature of LLMs and how they predict their outputs at both high level (how the output structure should look like?) and low level (what is the most likely next word?), initially, we tend to believe that humans are smarter than this. But are they? When humans are composing their decisions (output), they think about all their previous experiences that they lived, read, heard, or consumed in some other way (training data). They try to find something similar to the current context (input) to justify their decision (output). And if they do not feel confident with composed decisions, they test some more (by default, we do not see confidence scores in ChatGPT outputs).  
    Therefore, for me, it seems that the mechanics of neural networks and human thinking are pretty similar. However, humans apply not only language, but a lot of other models as well, and LLM alone has trouble dealing with other models (i.e. there are a lot of examples of how ChatGPT struggles with rather simple math problems). From my personal experience, LLMs perform a lot better on high-level problems (summarizing and listing options) compared to lower-level problems (identifying an exact option in detail). We should not expect LLMs to capture all those other models, all their inner relationships and dependencies right. Due to a high volume of training data, some of them seem to be captured right even at low-level (creating that "LLM magic"), but we should be careful about projecting that to every topic and every model that comes to mind. Training data was not scored on every possible model.

13. **Accountability:** I am not sure a machine can take responsibility for its actions. Any opposite claim from their creators would raise a lot of eyebrows.

15. **Respect:** At first glance, LLMs' outputs are very respectful and polite - they use polite language and try not to include information that may be of sensitive and/or controversial nature. However, and more importantly - it does not always respect given inputs, opinions, and context (see reliability issues).

17. **Dependability:** What we call "being there for others" for human specialists, for systems we specify as availability. In this area, high-availability systems outperform humans largely.

19. **Shared Experiences:** We often build trust in tools once we spend some more time working with them and applying them in some challenging situations. Or when something unexpected surfaces and the tool surprises us by taking care of such unpleasant circumstances. We use that "track record" that we collected over time and extend that to the future. But to project that "track record" for the future, consistency is required (which is not a strength of gen-AI models).

To sum up, the main reasons not to trust gen-AI models completely lie in their respective gaps in consistency, reliability, integrity, and competence. Given their complex non-deterministic nature, there will always be some associated risks in using gen-AI **alone** for decision making.

### Testing in pair with gen-AI

It is a popular opinion that a human specialist working together with gen-AI may achieve better results than both of them working alone, and I completely agree. LLMs can be very useful in speeding up the generation of various content. However, I would like to mention some fallacies that may occur when testing in a pair with gen-AI:

- **Building trust based on gen-AI "human factors".** Our trust in gen-AI output should not depend on "human factors" that can be found in LLM outputs. It can say "I am sorry for my mistake", "I feel you" or "I hear you", but that would be only a figure of speech to make it sound more lively. The reader should not forget that such things are only decorations and double-check. If LLM says that it is sorry for its mistake, has it really fixed that mistake now?

- **Starting with gen-AI output.** LLM is a good tool for thinking, but do not let yourself run into confirmation biases by starting with LLM's output. Instead, it is better to start by capturing your own ideas first, and only then double-checking with gen-AI to validate your own thinking.

All in all, LLMs can be very helpful in speeding up content creation in various situations. However, the important part is to keep ourselves aware of our required level of quality, LLM constraints, and do not fall into the traps of overconfidence in LLM's outputs.
