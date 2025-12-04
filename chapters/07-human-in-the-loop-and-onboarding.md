## Chapter 7: Human-in-the-Loop and Onboarding

> "AI cannot solve all problems. AI cannot solve the first mile and the last mile. This is essentially a human problem."

> Extended reading: How debugging workflows demonstrate human-AI collaboration boundaries, see [*Debugging: Finding Bugs with AI in Deep Waters*](./03-debugging-with-ai.md). For how test systems provide safety nets that enable human delegation, see [*Test–Code Loop: Why Test Code Is More Important Than Functional Code*](./02-test-code-loop.md).

### 1. First Mile and Last Mile: The Two Ends AI Cannot Do

In the AI-native world, there are two things AI cannot do, or cannot do well, or shouldn't do:

- **First Mile**: Designing a truly reasonable solution
- **Last Mile**: Getting every line of code correct in a real environment

> "The relationship between humans and AI is that of reviewer and executor, but humans cannot evaluate things they themselves don't understand."

The subtext of this statement is:

- You cannot hand a system you don't even understand to AI for "automatic maintenance"
- You must first have sufficient understanding of the system before you're qualified to evaluate whether AI is doing well

### 2. Human-in-the-Loop Is an Unavoidable Engineering Cost

Many people hope that one day they can achieve "full automation":  
PRD → AI automatically breaks down tasks → automatically writes code → automatically deploys → automatically maintains.

The conclusion from practice is:

- Once this fantasy is introduced into real, complex, long-lived systems, it quickly collapses
- The more you rely on AI automation, the fewer people seriously review, the faster debt accumulates

The truly feasible and must-accept model is:

- **Human-in-the-loop is present throughout**:  
  - In requirement clarification phase
  - When making key architectural decisions
  - After each round of major changes and critical path changes
- AI can help you complete a lot of repetitive, physical, local work
- But for "overall direction" and "key decisions," humans must explicitly sign off

### 3. Onboarding: AI Cannot Train a Real Engineer

In an AI-native team, newcomers easily fall into two extremes:

1. **Fed by AI**:  
   - Ask AI everything, have AI write whatever is needed
   - Don't build their own mental model of the system's real structure and boundaries
   - When encountering deep waters that AI can't handle, completely lose direction

2. **Completely Bypass AI**:  
   - Worry AI will make mistakes, don't trust AI
   - Write everything by hand alone
   - At today's pace, quickly get left behind by the overall rhythm

A relatively healthy onboarding approach is:

- Treat AI as a "very skilled but not very reliable assistant"
- Require newcomers to, for every AI change:
  - Know which part it changed
  - Know this part's position in the entire system
  - Know this part's test coverage and verification method

> "Although humans don't need to write code, you must know which part it's changing... cannot accept results of 'accidentally fixing it correctly.'"

### 4. Using Debug and Tests to Train Newcomers' Judgment

For training newcomers, the best training scenarios aren't "have them write features," but:

- Take them through debugging a real deep bug together (see [*Debugging: Finding Bugs with AI in Deep Waters*](./03-debugging-with-ai.md))
- Take them through adding a test for a critical path together (see [*Test–Code Loop: Why Test Code Is More Important Than Functional Code*](./02-test-code-loop.md))

In these scenarios, newcomers must learn:

- How to clearly describe problem phenomena to AI
- How to use logs and tests to correct AI's misjudgments
- How to take over the relay baton and read code themselves when AI fails to solve it after two consecutive rounds
- How to precipitate final "conclusive information" into documentation, rather than pasting the entire process

This entire process essentially trains newcomers to:

- Build their own mental model of the system
- Build intuition about AI's limitations
- Have judgment about the boundary of "when to trust AI, when to definitely look yourself"

### 5. Team-Level Human-in-the-Loop Design

From a team perspective, Human-in-the-loop isn't just a "philosophical attitude," but should be designed as an explicit mechanism:

- Which modules, which paths, any changes must have human review
- Which types of changes can be "AI + tests pass is enough"
- Which decisions must have "written record + signature"
- Which documentation and tests must be read before newcomers join the group

As long as the team is still writing externally visible code, as long as the product is still responsible to real users,  
**Human-in-the-loop cannot disappear; it can only be designed more clearly or more chaotically.**

