## Chapter 13: Meeting Recording→PRD→TDD→Code: AI-Native Team's Knowledge Workflow

> "A more radical vision to try when we have enough funding and people: Record all meetings → generate subtitles/transcripts → generate PRDs → generate TDDs → generate code drafts."

> Extended reading: How this pipeline fits into the broader AI-native workflow loops, see [*AI-Native Workflows: Plan/Act, Test/Code, Doc/Code/Doc*](./05-ai-native-workflows.md). For why small teams are particularly well-suited for this approach, see [*The Structural Advantages of AI-Native Small Teams*](./10-small-team-advantage.md). For how user stories connect to this pipeline, see [*Five Levels of AI Coding and the User Story Driven Endgame*](./09-ai-coding-levels-and-user-story-driven.md).

### 1. A "radical" but feasible vision

In the May 2025 revision, a complete knowledge workflow pipeline was mentioned:

1. **Meeting Recording** → Generate subtitles/transcription
2. **Subtitles/Transcription** → Generate PRD
3. **PRD** → Generate TDD (Technical Design Document)
4. **TDD** → Generate code draft
5. **Code Draft** → Human review and refine

The complete form of this pipeline is:

> "Use browser-use as an intermediary to forward all internal knowledge (including codebases) to Gemini Web. This improves productivity for all internal work. Combine with new tools like Flowith and Manus. This internal work platform will become the primary interface for every role and every team member."

### 2. Why this pipeline is particularly valuable for small teams

For new teams and small teams, there is less historical debt: not so many "legacy systems" or "historical baggage," so all knowledge can be collected into this platform quickly. They can also AI-ize all links. Large companies might only innovate in 10 links, but small teams can AI-ize 100 links, and the final overall efficiency will far exceed large companies. Knowledge density is high too: small teams' knowledge is more concentrated, easier for AI to fully understand and process.

The core value of this pipeline is to transform unstructured knowledge into structured assets. Meeting recordings, discussions, design drafts, knowledge that used to be "scattered everywhere," can now be automatically converted into part of the codebase. It reduces information loss. In the past, decisions, discussions, and design ideas from meetings might only be remembered by attendees. Now they can all be recorded, letting AI help with subsequent development and maintenance. It also makes knowledge work automate-able. Not just writing code, but even "understanding requirements," "designing systems," "writing documentation": these tasks can also have AI participate.

### 3. Technical implementation path

**Core Toolchain:**

1. **Meeting Recording and Transcription**  
   - Use existing meeting tools' (Zoom, Tencent Meeting, etc.) automatic transcription features
   - Or use specialized transcription services

2. **Browser Use as Intermediary**  
   - Browser Use can let AI access internal systems, codebases, documentation libraries
   - Forward transcribed text, codebase, and related documentation together to Gemini Web

3. **Gemini Web as 'Knowledge Processing Center'**  
   - 1 million token context, can load the entire project's knowledge at once
   - Let AI understand the relationship between "meeting discussion content" and "existing codebase/documentation"

4. **Flowith, Manus, and Other Tools as 'Workflow Orchestrators'**  
   - Automated pipeline: Transcription → PRD → TDD → Code
   - Each link can have human review and confirmation checkpoints

### 4. Another use case: batch generation of operations content

Besides the "meeting → code" pipeline, there's another practical use case:

> "Use generic MCP, integrate tools like Manus and Flowith. For example, operations needs to produce 100 scenario contents. Agent automatically completes this task. After human confirmation passes, it can be imported into our platform. This Agent will become the homepage of everyone's browser: the starting point of all work."

This use case demonstrates that AI can handle repetitive, batch work. Operations needs 100 scenario contents. Humans writing would be exhausting, but AI can batch generate. Humans only need to confirm and gatekeep: generated content, after human review passes, can be directly used. This Agent can also become a work entry point. Not just writing code, all work that needs "batch content generation" can be completed through this Agent.

### 5. Challenges and limitations of this pipeline

**Main Challenges:**

1. **Quality Control**  
   - AI-generated PRDs, TDDs, and code might have unstable quality
   - Need humans to carefully review at each link, cannot be "fully automatic"

2. **Information Accuracy**  
   - Meeting recording transcriptions might have errors
   - Transcription → PRD conversion might lose critical information
   - Need humans to confirm accuracy at each link

3. **Context Management**  
   - If project scale exceeds 10M token, Gemini Web also cannot load it all at once
   - Need more complex context selection strategies

For practical implementation, start with small-scale experiments: first experiment with this pipeline in a small project, small team, and accumulate experience. Each link must have human checkpoints. It cannot be "fully automatic," and content generated at each link must be confirmed by humans. Review and optimize regularly: if you find a certain link always has problems, adjust the pipeline design.

### 6. The future of this pipeline

Although this pipeline is still in the "radical imagination" stage, as AI capabilities improve, it might become the "standard configuration" for AI-Native teams:

Meeting recordings automatically convert to PRD: after meetings end, the PRD is automatically generated, and humans only need to review and refine. PRD automatically converts to TDD. Technical design documents can also be automatically generated, and humans only need to confirm technical solution reasonableness. TDD automatically converts to code: code drafts are automatically generated, and humans only need to review and test. All knowledge becomes searchable, understandable, and reusable. Knowledge that used to be scattered everywhere now becomes part of the codebase, and AI can call it anytime.

### 7. Summary

Meeting recording → PRD → TDD → code: this complete knowledge workflow pipeline, although still in the "radical imagination" stage, demonstrates a possible future for AI-Native teams:

> **All knowledge work can be participated in and accelerated by AI.**  
> Humans no longer need to "manually organize requirements," "manually write documentation," "manually write code." Instead, let AI do it first, and humans only need to review and refine.

For small teams and new teams, this pipeline is particularly valuable because:

- Less historical debt, can quickly implement
- Can "AI-ize all links," efficiency improvement will be very obvious
- High knowledge density, AI can fully understand and process

Although it's still in the stage of "can start experimenting when we have enough funding and people," as AI capabilities improve and toolchains mature, this pipeline might become the "standard configuration" for AI-Native teams.

