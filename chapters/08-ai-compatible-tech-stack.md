## Chapter 8: Choosing AI-Compatible Technology Stacks

> "Very new technology stacks are hard for AI to master, because training data is too limited... The word 'compatibility' gains a new meaning in this context."

> Extended reading: How small teams can leverage AI-compatible stacks more effectively, see [*The Structural Advantages of AI-Native Small Teams*](./10-small-team-advantage.md). For how conventions work with tech stack choices, see [*Conventions and Development Standards—Let AI Dance in Chains*](./11-conventions-and-standards.md).

### 1. "AI Compatibility" Is a New Kind of Compatibility

Traditionally, when we talk about "compatibility," we mean:

- Browser compatibility
- Platform compatibility
- Third-party library API compatibility

In the AI-native era, there's another layer:

- **Is the technology stack friendly to AI?**
- **Does AI have enough training data and practical samples on this stack?**

> "Very new technology stacks are hard for AI to master, because training data is too limited, for example Deno;  
>  But if it's mature like Next.js, AI can quickly produce correct code."

This means:

- Technology selection is no longer just a game of "performance, ecosystem, stability"
- You also need to consider: "How much work can AI help with on this stack?"

### 2. Choosing Mature Stacks Is to Let AI Do More

If you choose a very new stack with a still-thin ecosystem:

- Documentation is incomplete, community practice samples are few
- Code samples in training data are also few
- AI's "proficiency" on this stack will be noticeably low

Conversely, if you choose a stack that's been validated by massive projects:

- Various typical usages, best practices, anti-patterns—AI has "seen many times"
- When you ask it to write code, write tests, refactor, success rate will be much higher
- You can put more energy into business and workflow design, rather than struggling with the stack itself

This is the practical meaning of "AI compatibility":

- Not that new stacks aren't worth attention
- But when your team has limited people and strongly depends on AI productivity,  
  **choosing a stack AI is very familiar with is often more cost-effective.**

### 3. Practical Decision Recommendations

In a two-person small team, strongly dependent on AI, you can use a relatively simple set of decision principles:

1. **Prioritize stacks AI is very familiar with**  
   - Web frontend: Next.js / React / Tailwind / common UI libraries
   - Backend: Node/TypeScript + Postgres, or mature serverless combinations

2. **Prioritize AST / symbol-friendly languages and toolchains**  
   - Convenient for AI IDEs and CLI tools to do intelligent refactoring, navigation, and test generation

3. **Consciously avoid overly 'pioneering' technology combinations**  
   - If a stack is still in the "trial period" in the community, AI probably can't help much

Technology selection is always a trade-off, but in the AI-native world,  
**if you want AI to truly become a team member, the technology stack must be friendly to AI.**

