## Chapter 11: Conventions and Development Standards—Let AI Dance in Chains

> "The importance of Convention and development standards for AI-Native teams will only be higher, because they are the best tools to slow entropy increase. At the start of a project, we should design as many constraints and conventions as possible. Let AI 'dance in chains.'"

> Extended reading: Why conventions are especially critical for small teams, see [*The Structural Advantages of AI-Native Small Teams*](./10-small-team-advantage.md). For how conventions integrate with AI-native workflows, see [*AI-Native Workflows: Plan–Act, Test–Code, Doc–Code–Doc*](./05-ai-native-workflows.md).

### 1. Why Conventions Are More Important in the AI-Native Era

In traditional software engineering, conventions and development standards are already important, but in the AI-Native context, their importance will further increase.

The reasons are:

- **AI writes code too fast**  
  If there are no constraints, AI will produce a lot of inconsistent style, non-unified structure code in a very short time.  
  Human brains can't review it all, let alone maintain it long-term.

- **AI itself is 'stateless'**  
  Every new AI session is a "new team member," it won't automatically remember the conventions you set last time.  
  Only by explicitly writing these conventions **into the codebase, into prompts, into test frameworks** can AI continuously follow them.

- **Entropy increase speed is amplified**  
  The faster code volume grows, if there are no strong constraints, the speed of system chaos increase will also be faster.  
  Conventions are the most direct and effective means to slow entropy increase.

### 2. Design as Many Constraints as Possible at Project Start

A common misconception is:

> "Let's develop quickly first, set standards when there's more code."

In AI-Native teams, this thinking doesn't work. The reasons are:

- AI's productivity is too high. By the time you "think it's time to set standards," the codebase might already be so large that "the cost of setting standards is higher than starting over"
- AI will reference existing code style. If early code is chaotic, subsequent AI-generated code will continue this chaos

The correct approach is:

> **At project start, design as many constraints as possible.**

These constraints include:

1. **Code Style and Naming Conventions**  
   - Function naming, variable naming, file organization methods
   - Have AI reference existing, convention-compliant code when writing code

2. **Testing Framework and Testing Conventions**  
   - Test file organization methods, test case writing style
   - This way, when AI generates new tests, it will automatically reference existing test patterns

3. **Architectural Boundaries and Module Responsibilities**  
   - Which code should go where, which modules cannot directly call each other
   - Through documentation and code structure, let AI understand these boundaries

4. **Documentation and Code Synchronization Rules**  
   - When to write documentation, what documentation should contain, when to delete documentation
   - Avoid AI generating a lot of procedural, historical documentation garbage

### 3. How Conventions "Slow Entropy Increase"

The essence of entropy increase is: **systems spontaneously become more chaotic and disordered.**

In codebases, entropy increase manifests as:

- Code style becomes increasingly inconsistent
- Module boundaries become increasingly blurred
- Test coverage becomes increasingly low
- Documentation and code become increasingly out of sync

Conventions slow entropy increase through the following ways:

1. **Give AI a 'Standard Answer'**  
   When AI doesn't know how to write, it will reference existing, convention-compliant code.  
   If these "reference codes" themselves are standardized, AI-generated code will also be more standardized.

2. **Reduce 'Free Play' Space**  
   The more constraints, the fewer places AI can "write randomly."  
   Although it sounds a bit "limiting creativity," in the AI-Native era, **controllability is more important than flexibility.**

3. **Make Review Simpler**  
   If all code follows the same set of conventions, human reviewers only need to focus on "whether the logic is correct," without spending a lot of time correcting style issues.

### 4. Practical Implementation Recommendations

In a two-person small team, strongly dependent on AI, you can implement conventions like this:

1. **At the very start of the project, spend 1–5 days setting basic conventions**  
   - Code style (ESLint/Prettier configuration)
   - Testing framework and test organization methods
   - Documentation scope and format

2. **Write these conventions into prompts and cursor rules**  
   - Let AI "see" these conventions every time it writes code
   - Regularly review these rules to ensure they're consistent with the actual codebase

3. **Enforce with testing and lint tools**  
   - Code that doesn't meet conventions directly fails CI
   - Don't expect "manual review to correct"—human brains can't review it all

4. **Regularly Review and Update Conventions**  
   - If you find a convention is "always violated" in actual use, the convention itself might be problematic and needs adjustment
   - But adjustments must be very cautious, because every adjustment might make AI produce a batch of code that doesn't meet the new conventions

### 5. Summary

In the AI-Native era, conventions and development standards are no longer "nice to have," but "must have."

> **Let AI dance in chains—these chains are your conventions.**  
> Without chains, AI will dance very fast, but also very chaotically, and eventually the entire system will be out of control.  
> With chains, AI, although it can't "freely play," can continuously produce controllable, maintainable code.

Spending time designing these "chains" at project start is one of the most important investments for AI-Native teams.

