---
title: "The messiest codebase in the universe (until now)"
date: 2026-02-25
draft: false
description: "The tension between readability and evolvability."
---

{{< newthought >}}There is a firmware{{< /newthought >}} that is massively adopted basically everywhere in the world, and yet the codebase is an incredible collection of anti-patterns. Most of the code is completely ineffective, and it can be changed, deleted, and moved around at runtime. The whole thing has been repeatedly duplicated over the years{{< sidenote >}}*«[Susumu Ohno, "Evolution by Gene Duplication" (Springer, 1970)](https://link.springer.com/book/10.1007/978-3-642-86659-3) — the foundational argument that gene duplication creates redundant copies freed from selection pressure, allowing them to accumulate mutations and acquire new functions.»*{{< /sidenote >}}, and whole segments consist basically of a few lines repeated over and over hundred of times. Sometimes, the duplicated code has been tinkered to develop new features; some others, the duplication of identical code just ensures that it is executed the correct number of times. There are portions of code that run only to copy-paste themselves around.{{< sidenote >}}[Transposable elements](https://www.nature.com/scitable/topicpage/barbara-mcclintock-and-the-discovery-of-jumping-34083/), or "jumping genes".{{< /sidenote >}} Goes without saying, not a single docstring, or truly descriptive variable names.{{< sidenote >}}even worse: analysts have been piling up crazy nicknames to talk about this codebase{{< /sidenote >}}And yet, its success is undeniable: it powers the most succesful ecosystem . It constitues the core of the only entities whose *agency* nobody would deny.

This is obviously the genetic code, where _code_ is to some degree a misnomer that would, if taken literally, encounter a frowned look from more than one biologist. Still, it is fair to recognise some very loose analogy with computer code. They both are durable registries  whose changes, once enacted through the intermediation of an interpreter, translate into changes of a system and its ability to interact with the environment. {{< sidenote >}}This is pretty much as far as I will go in terms of analogy. The original meaning of "code" has a whole story...{{< /sidenote >}}

The way genomes evolution has produced the mind-boggling variety of life forms we know sounds so miracolous that a significan fraction of humanity still struggle to believe it. DNA has just accumulated  random mutations over millions, billions of years and the differential reproductive success produced by the interactions between the organism "system" and the environment has led to the adaptations and diversity we see today.

## The secret sauce of blind evolution: evolvability

I remember an image from my high school biology textbook: the probability that a random mutation produces an adaptive change was compared to the chance that shooting to a car engine would produce an improvement in the motor. Taken at face value, such an image would destroy the conviction of even the strongest evolutionists. But it is actually incredibly misleading: the car engine is a delicate engineered system where each component was designed, and it interactions with the rest of the system optimized studied under the assumption people would not actually shoot at the hood to make the car go faster.

Genomes and organisms are a very different story. Since life exists and it has been self-replicating, adaptations to the environment could be driven only through DNA mutations. So even though each single mutation was just adaptive in itself, the system over time acquires features that make it more likely that further mutations are actually adaptive. Let's get more concrete. A mayor challenge of producing useful changes that make a protein acquire a new function, for example metabolizing a new nutrient, is the fact that by changing it we would risk loosing the function it had before. Here, genomic duplications are crucial. The _duplication_ of a whole segment of genome is not in itself adaptive. Even worse, it could actually produce imbalances that prove harmful for a cell. But it actually increases a lot the _surface_ for further adaptive mutations to happen: a second mutational event could introduce new features without breaking the old ones. Guess what, duplications are everywhere in genomes, and mayor innovation periods in evolutionary history have corresponded to duplication events that made available a lot of "tinkering material".

There is a long list of similar traits, that increase evolvability by making the system more prone to benefit from further random mutations. Other examples include _modularity_: the fact that while genes work together in the determination of phenotypic traits, their competence is to some degree limited, and they do not interact with every other part of the genome. In this way, if they change or get lost, the impact of the event reflects on a specific set of functions of the organism, or the development of a specific body part. The fact that organisms are stacks of semi-autonomous hierarchical levels also make them more evolvable: genetic programs produce cells that are able to mind their own business without micromanagement from the organ they belong to, while still cooperating as a whole. In this way, the occasional reconfiguration of the high level system - eg, [insert here cool macro change of an organism] - can happen without specifying a whole different routine for each cell that compose it. But also the fact that they are _semi_ autonomous help: the occasional message can travel up and down the herarchy very easily, letting every cell in the [fact check] body know our conscious mind is cogitating about food. _Robustness_ to mutation, the ability of not changing readily the phenotype after a mutation is, maybe paradoxycally, also very useful. Once a mutation _does_ have an effect, that effect can be amplified by the previously accumulated neutral mutations{{< sidenote >}}Mutations that do not have a measurable phenotypic effect.{{< /sidenote >}}


## What about code?

I promised you code in the title, so, what about it? Well, turns out software engineers also talk about the evolution of their codebases {{< sidenote >}}Mainteinability is a more common term, but it is recognized that maintaining and evolving a codebase are two separate things.{{< /sidenote >}}. People have observed evolutionary phenomena emerging in long term code projects [refs on laws of code evolution]. {{< sidenote >}}There are even papers that compare the statistics and the organization of genomes and Linux packages installation{{< /sidenote >}}. So, what make code evolvable?

Very interestingly, some of the evolvable features we saw above appear also as good coding practices. Code _coupling_, tangles of interdependencies that make the implementation of a single feature require a ripple of changes troughout the codebase

{{< sidenote >}}*«The concept of evolvability — the idea that biological systems are structured so that random genetic changes are biased toward producing viable variation — is developed in [Kirschner & Gerhart, "The Plausibility of Life" (Yale UP, 2005)](https://yalebooks.yale.edu/book/9780300119770/the-plausibility-of-life/) and [Wagner, "Robustness and Evolvability in Living Systems" (Princeton UP, 2005)](https://press.princeton.edu/books/paperback/9780691134048/robustness-and-evolvability-in-living-systems).»*{{< /sidenote >}}

A software codebase, on the other end is (most of the times) the result of slow careful planning, skilled implementation, and thorough testing. It comes from deliberate thinking and, most importantly

---
**[TODO: sentence is unfinished — complete the thought about what most importantly distinguishes deliberate software engineering]**

---

I think that those intuitions might be challenged by what is now becoming widely known as "vibe coding"{{< sidenote >}}*«The term was [coined by Andrej Karpathy on February 6, 2025](https://x.com/karpathy/status/1886192184808149383), describing a mode of programming where you "fully give in to the vibes", accept all LLM suggestions without reading diffs, and barely touch the keyboard. It was subsequently named Collins English Dictionary's Word of the Year for 2025.»*{{< /sidenote >}} or, by some attempts to make it sound a bit less improv theatre and a bit more LinkedIn skills, "agentic coding". In the most literal definition, this  means delegating to a LLM model (with some tools to interact with your codebase and your computer) the whole code writing for your project, while

---
**[TODO: complete — "while" what? While you do what? Describe the human's role during vibe coding]**

---

If you have tried it yourself or you have been reading even the slightest about it, you know the usual takeaways: universally accepted as incredible for super short-horizon tasks; a maturing technology for working autonomously on implementing new features within some strict guardrails; people splitting between "utterly useless" or "revolutionary" when working entirely by itself putting up whole piece of production-ready software by itself.

As of now I have been working for 3 months on an extensive project that has been entirely vibecoded, almost* from scratch. I was in the purest sense vibecoding: I could not read any of the codebase myself (the tech stack was;

---
**[TODO: complete — what was the tech stack?]**

---

I only know Python…). First of all, it was fascinating to observe in such a cristal clear way how much work is still there to be done when one does not have to write a single line of code. With no training or experience in client-facing applications, I used to think a software is primarily defined by its codebase, and its environment is the machine it runs on. This is actually very wrong: it is just as much interaction within the physical world it is a part of

---
**[TODO: add citation on software types]**

---

When working on this codebase, we have been using all the known drills. We have set up our cursor rules, our AGENTS.md (in 2026, a markdown filename constitute a standard…), declared all our nice codebase principles, employed state of the art models. The codebase, once the project reached maturity (500 LOC, stably deployed since some months now), has become reasonably stable. And yet…

Yet the codebase keeps accumulating what an engineer would immediately recognise as code smell.{{< sidenote >}}*«The term was [coined by Kent Beck](https://martinfowler.com/bliki/CodeSmell.html) and systematized in chapter 3 of [Fowler & Beck, "Refactoring: Improving the Design of Existing Code" (Addison-Wesley, 1999)](https://www.oreilly.com/library/view/refactoring-improving-the/0201485672/ch03.html).»*{{< /sidenote >}} Duplications are ubiquitous, and keep appearing. Code is basically never refactored, and carries around vestigial modules whose function is getting forgotten. And yet, the more we progress, the less interference new implementation have on the old ones. (please, do not take this for science. This is a very superficial gut feeling, and not the empirical validation of what follows. Feel free to be skeptical about this observation but do not take the rest as dependent on it).

In light of all this, I actually started wondering whether is is possible that continuous rounds of vibecoding could actually put a "evolutionary pressure" that, via the constant evolution of new adaptive traits, promote the appearance of adaptive traits such as duplications and uncoupling, despite all the prompt cueing of keeping code tidy that would come from the upfront .rules.mdc files configurations. It actually made me start wondering: is it possible that there is an inescapable tension between *readable* and *evolvable*? While some of the attributes that make a codebase maintainable are similar to what makes genomes evolvable, readability is a major difference (and also

---
**[TODO: complete the parenthetical — "and also" what?]**

---

). Readability is a requirement that inevitably increases coupling: we want to reuse the same functions, adhere to our tidy abstractions, preserve layer segregations…And coupling is bad for evolvability: new features become inevitably harder to implement, bug fixes that were supposed to be small need propagating changes thoughout the codebase, etc etc.

Traditionally, the costs of loosing readability were very clear in terms of increasing cognitive load, and reduced productivity for developers; and obviously, duplications and reimplementations linearly scale the amount of labour required to fix bugs around. But do the same constraints really apply when we can have free variance, and just keep throwing spaghetti at the wall and see what sticks? If the complications of delivering code that passes all "at the surface" tests cannot be fully inferred from the codebase and the docs alone, could it be better to maximise tinkerability at the expense of global analysability?

I believe that the future of coding is inevitably a story of software engineers being increasingly pushed away (and upward) the chain of feedback loops that need to be closed for software to be maintained and evolved. As this happens, their understanding of the nitty-gritty will progressively loose relevance, and the definition of what "nitty-gritty" stands for in the previous sentence will get up the abstraction chain. Issues will be automatically addressed. Sentry logs will directly feed agent pipelines. User requests could be automatically screened and lead to new features implementations. Even further, users or group of users could directly or indirectly (through their measured interactions with the software) steer the improvement of a tailored version of the application. In the backend, microservices offering the same interface with different flavours of internal logic could compete with each other and be selected on speed or robustness. Once free code variance is unleashed, …

---
**[TODO: complete — what happens once free code variance is unleashed?]**

---

Are we sure that in this reconfiguration we want to stick to the principles that until now have defined code quality in the eyes of the human developer? It does not matter how many trillions of human-typed tokens an LLM has ingested, it is a very different object from a human mind. "Jaggedness"{{< sidenote >}}*«The "jagged technological frontier" concept comes from [Dell'Acqua, Mollick et al., "Navigating the Jagged Technological Frontier", Harvard Business School, 2023](https://papers.ssrn.com/sol3/papers.cfm?abstract_id=4573321) — a randomized experiment with 758 BCG consultants showing AI is superhuman inside the frontier and subhuman outside it.»*{{< /sidenote >}}, the idea that models are already super-human at many subtasks and sub-human for many others, is probably there for staying. And no matter how good they will get with code, it is unlikely that any granularity of upfront specifications will predict every possible interaction between software and the big world it faces in production. So why not loose constraints, harvest variance? Why not, start deploying whole pools of code forks, implementing new features on all of them, and screen the variants that have the best fitness in production - whatever measure of fitness we use? What people have been studying for genetic algorithms since a very long time{{< sidenote >}}*«[Genetic algorithms](https://en.wikipedia.org/wiki/Genetic_algorithm), first formalized by John Holland in 1975, apply evolutionary principles — selection, crossover, mutation — to search and optimization problems. The idea of evolving programs directly is the subject of [genetic programming (Koza, 1992)](https://en.wikipedia.org/wiki/Genetic_programming).»*{{< /sidenote >}},

---
**[TODO: complete — "(note: in the classification above, always in the context of X type software), bring it to the world of Y-software?" — clarify what X and Y software types refer to]**

---

bring it to the world of Y-software?

Loosing control is never nice, and it is a big leap of faith when we are convinced that we are giving it up for a solution that - in the short term - looks worse than what our sweat and elbow grease could produce. But it maybe resemble what artificial intelligence underwent in the long transition from Good Old Fashoned AI{{< sidenote >}}*«The term "GOFAI" (Good Old-Fashioned AI) was [coined by philosopher John Haugeland](https://en.wikipedia.org/wiki/GOFAI) in his 1985 book "Artificial Intelligence: The Very Idea" to label the classical, symbol-manipulation-based paradigm (logic, search, expert systems), distinguishing it from connectionist approaches.»*{{< /sidenote >}} to modern neural networks. Focusing on learning rules and hyperparameterer tweaking, studying learning dynamics, optimising boundary conditions that make optima discoverable, instead of micromanaging heuristics. And remember

---
**[TODO: article ends mid-sentence — "And remember" what? Complete the closing thought]**

---
