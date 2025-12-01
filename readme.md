# AI-Native Engineering Manifesto (English)

[![Revision March 2025](https://img.shields.io/badge/Revision-March_2025-0a84ff)](#march-2025)
[![Revision May 2025](https://img.shields.io/badge/Revision-May_2025-34c759)](#may-2025-revision)
[![Revision Dec 2025](https://img.shields.io/badge/Revision-Dec_2025-ff9f0a)](#december-2025-revision)

---

## Table of Contents
- [AI-Native Software Engineering](#ai-native-software-engineering)
- [AI-Native Engineering: 11 Hard Truths for 2025](#ai-native-engineering-11-hard-truths-for-2025)
- [March 2025](#march-2025)
- [May 2025 Revision](#may-2025-revision)
- [December 2025 Revision](#december-2025-revision)

# AI-Native Software Engineering

| **Author** | [Limin Ge](https://www.linkedin.com/in/limin-ge-573b4b28a/) |
| --- | --- |
| **First Draft** | March 2025 |
| **Revisions** | May 2025, December 2025 |

---

<a id="ai-native-engineering-11-hard-truths-for-2025"></a>
## AI-Native Engineering: 11 Hard Truths for 2025

1. If a knowledge, methodology, or tech stack is older than 3 years, it’s obsolete until proven otherwise.

2. Your codebase, your docs, your meeting notes — none of these are your backbone. Your only reliable, compounding asset is your test case library.

3. To truly understand AI, you must understand its nature: AI is completely, fundamentally stateless.

4. We can accept AI making mistakes — as long as those mistakes don’t kill the team before the next model upgrade.

5. Software complexity must flatten.   We’re moving from deep, vertical stacks to wide, horizontal systems.

6. The context window is the most critical computational resource every engineer must master.

7. Plan–Act, Test–Code, and Doc–Code–Doc are the new operating system of engineering.

8. The future of code isn’t abstraction — it’s tiny, isolated, AI-readable units that stand on their own.

9. AI will never solve the first mile or the last mile. Those remain stubbornly, unavoidably human.

10. AI-generated Artifacts are not side effects. They are a new software modality — and they become part of your engineering assets.

11. The real power of AI IDEs and Agents is not generation —   it’s ruthless, intelligent context selection.

---

<a id="march-2025"></a>
## March 2025

1. **Any knowledge system, methodology, or technology stack that is more than three years old should be considered obsolete.**
   In an AI-native era, most “best practices” and “mature stacks” decay much faster. The advantage lies not in accumulating old techniques, but in continuously rebuilding on new capabilities.

2. **The Plan–Act loop.**
   We still plan and execute, but planning itself becomes a collaboration between humans and AI. “Planning” is no longer just writing tickets; it includes prompting, structuring context, and orchestrating agents.

3. **The Test–Code loop.**

   1. In the age of AI coding, tests become critically important.
   2. Backend tests are relatively straightforward; web frontends and especially mobile clients are much harder to test end-to-end. Truly reliable E2E automation on mobile is extremely challenging.

4. **The Doc–Code–Doc loop.**
   Documentation and code should form a continuous loop:

   * Docs guide AI to write code.
   * Code changes regenerate or update docs.
   * Docs become the long-lived memory of the system—for both humans and AI.

5. **The upper bound of an AI’s context window will be the most important “resource” for programmers in this new era.**
   Whoever can manage context—select, compress, and feed it effectively—wins.

6. **Documentation is the cache for AI memory.**

   1. Snapshot-style, full-volume documentation is superior to incremental, diffs-only documentation from an AI’s perspective.
   2. The upper bound of an AI IDE’s capability is the upper bound of its usable context window. Humans are similar: our mental context window is also limited.
      How do humans handle complex systems? Look at how big companies organize collaboration across functions and teams.
      Our collaboration with AI should mimic this: multiple roles, multiple teams, each with a bounded view, but coordinated through shared artifacts.

7. **“Vibe Coding” only describes a very primitive stage. The endgame is user-story-driven development.**

   Today, many people use Cursor as a simple tool to help “finish a requirement.” But there are several levels beyond that. From a mindset perspective:

   * At the beginner level, the programmer is still thinking like a human.
   * At the intermediate level, the programmer starts thinking like a machine.
   * At the advanced level, the programmer becomes a *manager of machines*.

   Rough levels:

   1. **Inexperienced AI coding users**

      * Use their native language (e.g., Chinese)
      * Vague, wandering prompts
      * “Do whatever comes to mind,” pure vibe coding

   2. **Proficient AI coding users**

      * Realize they should use English
      * Understand the context window is limited
      * Understand Cursor does *not* read their entire codebase

   3. **Process-structured users**

      * Have solidified their own workflows
      * Apply Cursor rules and patterns quickly and consistently

   4. **Issue-Tracker-level users**

      * Use MCP and other tools
      * Treat each issue or requirement as the center
      * Simulate a full team’s collaboration flow around one issue

   5. **User-Story-Driven organizations (AI-Native level)**

      * The entire system is restructured to be AI-native
      * AI can work asynchronously and in parallel
      * 100 user stories can be developed simultaneously like a multi-threaded team

8. **The better humans build infrastructure that fits AI’s needs, the more AI can release its power.**
   For existing systems, this is a huge challenge, because they were not born AI-native.

9. **Beyond AI IDEs, AI-driven productivity reform touches every corner of software engineering.**
   For example:

   * Drawing flowcharts
   * Writing PRDs
   * Converting PRDs to TDD
   * Stack trace and log analysis
   * End-to-end testing
   * …and many more

   Every aspect of software engineering should have a “new era, AI-native alternative.”
   I once crawled a list of such tools from YC—using an AI agent to crawl it for me.

10. **In the past, we emphasized reuse and abstraction. Now, AI cannot understand very long contexts.**

    Previously, we might carefully craft 500 functions that heavily reuse each other and form deep abstractions.
    In the AI-native era, we might instead write 5,000 small-scope, mutually independent functions, each fully understandable within a single context window.

    (This is a hypothesis that still needs to be validated.)

11. **AI cannot solve everything. Specifically, it cannot fully solve the first mile and the last mile.**

    * The *first mile* is designing a good solution.
    * The *last mile* is making every single line of code correct in a real-world environment.

    This is not a limitation of AI per se, but of humans.

    The human–AI relationship is that of **reviewer and executor**. But a human cannot review what they themselves do not understand.

    For any existing system, humans must first understand its modules, flows, and constraints, before they can evaluate whether AI’s solutions are good or bad.
    Human-in-the-loop is absolutely unavoidable.

12. **Very new technology stacks are hard for AI to master.**

    Stack like Deno have limited training data, so AI’s capabilities are weak there.
    Mature stacks like Next.js, on the other hand, can be handled very well by AI, which can quickly produce correct code.

    The word *compatibility* gains a new meaning in this context.

13. **“Postgres for everything” plus cloud functions.**

    Recently, I’ve been exploring Supabase + Vercel. This combination appears capable of handling almost everything.

    Traditionally, collaboration between frontend and backend uses API contracts as the main interface:

    * If the backend “handles everything” for the frontend, then the API contract must be extremely comprehensive and detailed.
    * If the frontend also performs part of the business logic, then in addition to syncing over API contracts, you also need to sync database schema and other system components.

    If we use Postgres webhooks, frontend–backend collaboration becomes much simpler.
    Both sides only need to align on the **DB schema**, and a huge amount of communication overhead disappears.

14. **Prompts must be detailed, and references must be explicit.**

    If you can reference something, you should provide that reference (files, symbols, etc.).
    Otherwise tools like Cursor will resort to RAG-style search over your codebase, which is often very inaccurate.

    In the future, Cursor and similar tools should be able to build indexes over symbols.

    Most current AIs are extremely neutral. We need them to become **opinionated**, and those opinions should be **personalized**, fully aligned to a specific developer or team.

15. **Programming paradigms over the last 40 years:**

    * 40 years ago, we wrote code mainly for **machines to understand**.
    * 20 years ago, we started writing code mainly for **humans to understand**.
    * Today, we should write code so that **AI can understand it**.

    There are patterns and regularities in what AI can understand, and we should learn them.

    But we should not over-finetune our prompts to the point of overfitting, because AI itself is evolving—e.g.:

    * The emergence of chain-of-thought (CoT)
    * Models like DeepSeek that are intentionally opinionated

    These shifts can quickly invalidate many “prompt engineering tricks.”
    This tension between *prompt patterns* and *model evolution* will be a permanent topic.

---

<a id="may-2025-revision"></a>
## May 2025 Revision

1. **From a business model perspective, AI IDEs will never be able to provide the same level of service as LLM web interfaces.**

   From a user’s point of view, the best service will come from:

   * Direct API calls, or
   * A powerful web-based interface (like ChatGPT / Gemini / Claude in the browser)

2. **A more radical vision to try when we have enough funding and people:**

   * Record **all meetings** → generate **subtitles/transcripts** → generate **PRDs** → generate **TDDs** → generate **code drafts**.
   * Use browser-based agents (browser-use) as an intermediary to forward all internal knowledge (including codebases) to something like Gemini Web.
   * Combine this with tools like Flowith and Manus.

   This internal work platform becomes the **primary interface** for every role and every team member.

   As a new team, we have very little historical baggage, so we can quickly pipe *all* our knowledge into such a platform.

3. **Another use case: a generic MCP-based agent hub.**

   * Integrate Manus, Flowith, and other tools via MCP.
   * Example: operations needs to generate 100 content scenarios.

     * The agent automatically completes the tasks.
     * Humans review and approve.
     * Approved content is imported into our internal platform.

   This agent becomes the homepage of everyone’s browser—the starting point of all work.

4. **For teams with historical accumulation, context windows will *never* be enough.**

   In such cases, the key becomes **context selection**.
   This is the *core work* of all AI IDE teams and AI Agent teams.

5. **Tokens as a way to quantify the information volume of a project.**

   * The total number of tokens needed to encode all assets of a project is a measure of its scale.
   * Right now, we are around **1M tokens**.
   * As long as we remain under **10M tokens**, this architecture can continue to deliver at least a **3× productivity boost**.

6. **AI IDEs and AI agents sell two things:**

   1. **The ability to select context well**
   2. **The ability to generalize best practices**

7. **Artifacts created by AI IDEs are a new modality.**

   Their significance is comparable to when humans first gained the ability to:

   * Post online
   * Upload images
   * Share audio and video

   For ordinary users, an AI IDE should be able to reach all the way to the **final mile of deployment**.

8. **The codebase index of an AI IDE should be an AST and symbol-level index.**

   Indexing at line or file level is no longer enough.
   We need symbol-level, AST-level understanding for reliable AI refactoring and navigation.

---

<a id="december-2025-revision"></a>
## December 2025 Revision

1. **How do we deal with bugs introduced by LLMs?**

   1. **Shift our focus from managing functional code to managing test code.**
      As long as we have enough test cases to guarantee correctness across a wide variety of scenarios, we can reduce the burden of manually managing functional code.

   2. **We can tolerate AI making errors as long as they don’t kill us within three months.**
      Because three months later, model capabilities will improve again and may solve problems that we currently cannot.

   3. **But an advanced AI team will always be pushing the limits of the latest model.**
      They will quickly reach those limits, and thus spend much of their time in the painful zone where AI cannot yet solve their problems.

2. **We should transform software complexity from vertical to horizontal.**

   This extends the idea from March 2025, point 10:

   * Instead of one or two very deep chains of logic, we create **many shallower, diverse paths**.
   * Deep chains are very hard for AI to debug, but AI can handle two or more very similar yet independent shallow chains.

   By increasing the diversity of paths, we can reduce the depth of any single path.

3. **[Repo] `https://github.com/ge-limin/shad-expo-studio`**

   This is an attempt to reduce **vertical complexity** by:

   * Completely separating the frontend presentation layer from the functional layer
   * Using Storybook-enforced regression tests to ensure the presentation layer does not drift over time

4. **[Repo] `https://github.com/ge-limin/story-ops`**

   Your codebase, docs, meeting notes, recordings, team memory, and intuition are *not* the truly reliable assets of a project; the only reliable core asset is your test corpus. This repo is a deeper exploration whose vision is:

   > **user story = PRD = E2E test cases**

5. **Conventions and coding standards become even more important for AI-native teams.**

   They are the best tools to **slow entropy increase**.

   * At the start of a project, we should design as many constraints and conventions as possible.
   * Let AI “dance in chains.”
   * The chains are what keep the system coherent over time.

6. **If the context and capability of a single AI session are bounded, we must let AIs work in relay on the same problem.**

   A good benchmark for this approach is:

   > Can we solve a very hard bug by using AI in multiple rounds of relay?

   The relay pattern:

   * When an AI is approaching its capability limit on a task, we ask it to persist as much **context** as possible:

     * Rationale, intermediate artifacts, decision logs, simplified diagrams…
   * The next AI (or next session) continues from there, instead of starting from scratch.

   This is exactly how humans stand on the shoulders of giants instead of reinventing the wheel every time.
   Without such relay, human technology would be frozen in place; with relay, both human and AI knowledge can compound.

7. Understanding AI hinges on understanding **statelessness**. A codebase should shed all procedural and historical baggage so that any reader—every AI session—needs zero historical context to operate.
