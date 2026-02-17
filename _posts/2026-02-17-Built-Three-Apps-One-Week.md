---
title: "I built 3 apps in a week"
categories: [AI,coding,building]
---
Last week, I watched a [TED talk](https://www.youtube.com/watch?v=3lPnN8omdPA) about an AI tool that challenges readers to think critically. The researcher never released it. So I built it myself (and then, two other apps) without writing a single line of code. I'm a Java backend developer who's never built a native Mac app before.

# Phase 1: Let’s build an app blind
In the talk, Advait Sarkar discussed developing a research prototype that encouraged readers to think critically through AI prompts. Immediately, this idea stood out to me as a fascinating tool. Except, they didn’t release it. A few weeks later, I stumbled upon the video again. This time, I realized I didn’t need them to release it. I could build it myself - despite having never built an app before.
I discussed the idea with Perplexity. There didn’t seem to be any products like this yet. Perplexity estimated it may take a few weeks. I used Codex and asked it to create the specs, requirements and mockups. 
￼
![Image of initial version of Tool for Thought](/assets/images/toolforthought.PNG)

The agent broke the problem down into tasks then proceeded to do each one, step by step. The end result wasn’t very visually pleasing, but the core functionality was there. After tinkering around, I decided to go all in on a Mac native experience. 

# Phase 2: Blind Spec Driven Development
I had been hearing about [spec-driven development](https://github.blog/ai-and-ml/generative-ai/spec-driven-development-with-ai-get-started-with-a-new-open-source-toolkit/), and this was the perfect opportunity to try it out. I found [Spec Kitty](https://priivacy-ai.github.io/spec-kitty/), a fork of Github’s [Spec Kit](https://github.github.com/spec-kit/). Its packed feature set sold me immediately. Not only does it use AI to generate requirements, specs, plans, and tasks, it can implement tasks in parallel and uses review agents. After a short interview with Codex about my idea, it drafted up a full set of requirements, spec, plans, and tasks. It broke down the task into 8 work packages. So, I let it implement them all on its own. Let me introduce FreeThoughts:

![Image of initial version of FreeThoughts](/assets/images/freethoughts.PNG)
￼

The results were surprisingly good. A few bugs and some polishing were needed, but it got me 70% of the way there. The results were buggy and imperfect - but working versions that let me play with the idea and iterate. The cost of making a prototype or POC is now almost free. 

# Phase 3: Embrace the Pivot
My next idea took the same concept for AI prompts and extended it beyond documents. Users should be able to view prompts everywhere on their screen, no PDFs needed.
￼
![Image of initial version of Tool for Thought](/assets/images/freethinker.PNG)

Meet FreeThinker. This project is the result of my rapid experimentation. To build it, I used the Spec Kitty process again. This time, I had another agent review the plan, specification and tasks. Now once the agents began implementing, they had a better starting point. I also used the orchestrator for the first time, allowing agents to work in parallel. It was a bit buggy, but within hours I had a working product. 

The fun part about building with agents is how fast a vision can be turned into reality. I don’t have experience in Swift or app development. Without AI, I wouldn’t have attempted to build these apps. In fact, I was building more software in my free time than I had in years. AI extends my abilities and enables me to build more.

Final versions of these projects were only 70% of the way to being "finished", which points to two areas of improvement for these models. The most important is verification: the agents need a way to verify their work. Writing tests isn’t effective as verification (it’s ok for regression). While I was testing the app and reporting to the agents what needed fixing, I realized I had become the QA. Instead, we need a way for these models to interact with the app to verify its work on its own - without cheating.

Second is the spec. Details matter. Any gaps in the specification leaves room for the agents to fill in on their own. If they make a different decision than what you want, that’s something you’ll need to correct. More often than not, I found myself needing to correct some of the decisions the agents made. For example, in the FreeThinker app, the agent made its own GlobalHotkeyService, instead of using a standard library like KeyboardShortcuts. There were also several UI tweaks I made to make the project look more polished. Your taste still matters; you know your vision, and agents aren’t going to replicate your taste for you.

AI can now do 70% of the coding on a project. With better specs and a way to verify, will it get to 80%? 90%? Dario (CEO of Anthropic) [expects](https://www.youtube.com/watch?v=n1E9IZfvGMA&t=804s) AI to do SWE jobs 100% end to end by the end of the year. There’s still a ways to go, but the real bottleneck isn't coding. It's a clear vision and purpose.