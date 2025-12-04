## Chapter 9: Five Levels of AI Coding and the User Story Driven Endgame

> "Vibe Coding only describes a very primitive stage. The endgame should be user-story-driven development."

### 1. From Vibe Coding to Machine Manager

Today, many people using AI IDEs (like Cursor) stay at a very primitive stage:

- Think of something and type a paragraph in Chinese
- Have AI help "do this requirement"
- Look at the effect, roughly works is fine

This is so-called **Vibe Coding**:  
More of a feeling-based, unclear-boundary, unstructured way of using it.

But if you extend the timeline, you'll find AI coding users actually have a very clear "rank evolution path":

> "At the beginner level, the programmer is still thinking like a human.  
>  At the intermediate level, the programmer starts thinking like a machine.  
>  At the advanced level, the programmer becomes a *manager of machines*."

### 2. Five Levels of AI Coding Users

A relatively clear classification can be:

1. **Inexperienced AI Coding Users**
   - Use Chinese, aimless, think of something and do it
   - Don't realize context window is limited
   - Don't realize AI IDE hasn't read your entire codebase

2. **Proficient AI Coding Users**
   - Realize they should use English
   - Realize context window is limited
   - Realize Cursor doesn't read your file's full text, but does fragment retrieval

3. **Users Who Have Solidified Their Own Workflows**
   - Have a stable prompt pattern and workflow
   - Can quickly apply their own Cursor rules, command-line tools, templates

4. **Issue Tracker Level Users**
   - Use MCP, Issue Tracker, and other tools, treating "one issue / one requirement" as the core unit of collaboration
   - Can simulate a complete team collaboration flow around one issue (requirement → design → development → testing)

5. **User Story Driven AI-Native Teams**
   - The entire system is completely transformed to AI-Native:
     - User story is a first-class citizen
     - AI can work asynchronously and in parallel
     - Can have 100 user stories in different stages progressing in parallel simultaneously

### 3. Why the Endgame Must Be User Story Driven

From an engineering perspective, User Story Driven has several natural advantages:

- **Natural Segmentation Unit**:  
  A user story comes with context, expected behavior, and acceptance criteria, making it very suitable as an AI work unit.

- **Natural Test Carrier**:  
  In ideal state, one user story = one set of end-to-end tests, which has been explicitly proposed in the `story-ops` exploration.

- **Naturally Suited for Horizontal Complexity**:  
  Each story is a relatively independent shallow chain, which fits well with the idea of "complexity from vertical to horizontal" (see *From Vertical to Horizontal Complexity* for details).

When teams truly reach the User Story Driven stage:

- The subject between product, design, engineering, and testing all becomes "story"
- AI doesn't directly operate on "code," but operates on "the complete lifecycle of a story"
- Code, documentation, and tests all become derivatives of stories

### 4. How to Level Up from Where You Are Today

In reality, you don't need to rush to level 5 from the start. You can first ask yourself a question:

> "What level of AI coding am I at today?  
>  What can I do next to level up?"

Some practical upgrade paths:

- From 1 → 2:  
  - Switch to English
  - Explicitly consider context window size and content selection

- From 2 → 3:  
  - Solidify frequent operations into documents, templates, commands
  - Have AI read these rules first, then start working

- From 3 → 4:  
  - Organize work by issue
  - For each issue, be clear: what's the input, what's the output, what's the verification method

- From 4 → 5:  
  - Further abstract issues into user stories
  - Try to achieve: one story comes with PRD + TDD + test cases
  - Use tools (like future story-ops) to make story the main entry point for all roles

The AI-Native endgame isn't some cool tool, but a new collaboration method "with user story as the atomic unit."  
From Vibe Coding to User Story Driven is a growth curve about "how to collaborate with AI."

