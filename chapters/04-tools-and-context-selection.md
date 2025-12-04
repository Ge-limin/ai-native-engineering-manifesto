## Chapter 4: Tools and Context Selection—Why AI IDEs Sell "Context Selection Capability"

> "AI IDEs or AI Agents sell two things: Context selection capability, and best practice generalization capability."

> Extended reading: The physical boundaries of context windows and their impact on engineering practice, see [*AI Statelessness and Context Window*](./01-ai-statelessness-and-context-window.md).

This chapter focuses on: characteristics of different AI coding tools, hidden constraints from business models, and why RAG, task managers, and multi-agent systems—things that "look smart"—are often anti-patterns in AI-native engineering practice.

### 1. Cursor's Business Model Problem: Wholesale to Retail

From a business perspective, Cursor's business model is "wholesale to retail":

- It buys tokens wholesale from large model vendors
- Then retails them to individual developers
- To maximize profits, it must "reduce costs and increase efficiency," and the most direct means is: **compress your context**

Once context is compressed:

- The compression might not be correct, potentially losing very critical information
- After compression, the large model lacks necessary details, and its judgments will be wrong
- The larger Cursor's user base, the greater its profit pressure, and the more incentive it has to secretly compress context where you can't see it

The result is: **You think it read the entire file, but it actually only looked at a few paragraphs in the middle.**

### 2. The Best Tools Often Come from Model Vendors

> Extended reading: How token scale affects tool selection decisions, see [*Token as a Quantitative Measure of Project Scale*](./12-token-as-project-scale.md).

Therefore, the best tools are actually those made by large model vendors themselves:

- They have no incentive to compress context
- What they really care about is "getting more data to train their models"
- So they won't secretly drop information where you can't see it

The cost is:  
— Not all ordinary people can afford the bill. Randomly chatting can cost dozens or hundreds of dollars, and $20–200 has become the "average price."

### 3. Web Interface + Large Context: How to Use Gemini

Another approach is: directly use the model vendor's web interface.

For example, Gemini:

- Has one million token context
- Can use some tools to package the entire codebase into a document with one click
- Paste the document into the web interface, then discuss your problem with it

But the biggest problem here isn't the tool, but:

- You need the ability to understand the answers it gives you
- You need the ability to confirm the scope and reasonableness of its changes
- Otherwise, you're just changing the channel through which "hard-to-review code" floods in

> When you're handling ultra-large context in the web interface, you still need to use the test system emphasized in [*Test–Code Loop: Why Test Code Is More Important Than Functional Code*](./02-test-code-loop.md) as a safety net.

### 4. RAG vs. AST: Why Symbol Indexing Is More Reliable Than "Smart Retrieval"

Cursor uses RAG to find things.  
From an engineering perspective, RAG technology has one major drawback: **accuracy is particularly low.**

> "Cursor often finds things that are similar but not quite right. The only reliable approach is to build an index on symbols, which is what's called AST."

Later we learned that tools like Codex or Cloud Code are essentially AST/symbol indexing approaches:

- Let AI master some underlying, 100% deterministic tools, like grep
- Don't let AI directly rely on "fuzzy matching" retrieval
- If AI doesn't find it the first time, it can adjust keywords and search a second, third time, and will eventually find 100% correct information sources

In contrast:

- RAG's "intelligence" definitely can't match the large model itself
- But it makes the smart large model depend on an index built by a "relatively dumb RAG"
- This combination is unreliable from the start

The correct approach should be:

> "Let the large model build the index itself, then let the large model call its own index."

### 5. Multi-Task, Multi-Agent, Task Manager: Intuitive but Wrong Ideas

There are many AI-based "task manager" products on the market:

- Let you write PRDs and rough requirements inside
- Use a Plan tool to first produce very detailed task lists, dependencies, and acceptance criteria
- Then use an Execute tool to let Agents execute these tasks concurrently
- Finally automatically test results

The starting point of this path is good. I myself walked this path for over half a year, even hand-crafted similar pipelines.

But I eventually eliminated all such processes, because:

1. They create huge mental burden for humans: PRDs, Tech Docs, execution records—a pile of documents all need to stay in sync
2. Once there's inconsistency, it means you're misleading AI, and it's easy for it to do wrong things
3. AI itself has a small error on each task, like 1%. After multi-task parallelization, errors will amplify geometrically

> "Even AI as strong as Codex can't safely develop complex projects in parallel. Errors accumulate too easily."

Therefore, **rather than pursuing the 'coolness' of multi-agent, multi-pipeline systems, it's better to work serially and honestly.**

### 6. Documentation and Code Consistency: Don't Let AI Eat Contradictory Information

Around tools and context selection, there's another very critical point: **consistency between documentation and code.**

Many people have a natural habit:  
Want to have AI first write a plan document with a checklist, then have AI check items one by one;  
After finishing, produce another execution record document.

This approach itself isn't wrong, but the problem is:

1. These "procedural" plans and execution records, if left in the codebase long-term, will form a lot of contradictory information with the code itself
2. AI reading descriptions like "it was A before, now it's B" will be confused about whether you want A or B
3. Combined with IDE/tool's own automatic summarization and compression logic, this contradiction will be further amplified

The correct approach is:

- Plan documents can be written, but delete them after tasks are complete
- Extract truly valuable "conclusive information" and merge it into main documentation
- Don't have sentences like "we originally designed A, later changed to B"

> This is completely consistent with the principle of "delete all A, only keep B" in [*AI Statelessness and Context Window*](./01-ai-statelessness-and-context-window.md).

### 7. Tool Selection Strategy: Who Does What

Combining all the above experience, a relatively simple tool selection strategy is:

- **Codex / Cloud Code**: Backend and all functional logic code
- **Cursor**: Component development, UI development, design restoration (utilizing IDE advantages)
- **Gemini Web and other large-context tools**: Scenarios requiring 10^6 level token context

Accompanying usage principles:

1. Within capability range, try to directly use model vendors' own tools
2. If using IDE-type tools, be very clear in your mind: it might be "secretly saving tokens" behind your back
3. All tools are just "entry points." What's really important is:
   - Your context organization method
   - Your test system (see [*Test–Code Loop: Why Test Code Is More Important Than Functional Code*](./02-test-code-loop.md))
   - Whether your documentation and code are consistent (see [*AI-Native Workflows: Plan–Act, Test–Code, Doc–Code–Doc*](./05-ai-native-workflows.md))

### 8. Context Selection Is the Core Capability of AI IDEs

Returning to the opening statement:

> "AI IDEs or AI Agents sell two things: Context selection capability, and best practice generalization capability."

This means:

- You shouldn't just look at "whether the prompts look good" or "whether the UI is pretty"
- What you really need to ask is:
  - How does it select context?
  - Will it randomly compress behind your back?
  - Does it use RAG or symbol indexing?
  - Will it mix procedural garbage with conclusive information and feed it to the model?

For an AI-native team, **the essence of tool selection isn't how comprehensive the features are, but: can it stably and predictably help you manage context well?**

