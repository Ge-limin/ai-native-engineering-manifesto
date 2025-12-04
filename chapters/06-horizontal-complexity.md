## Chapter 6: From Vertical to Horizontal Complexity

> "We should transform software complexity from vertical to horizontal... by increasing the diversity of paths, we can reduce the depth of any single path."

### 1. What Are "Vertical Complexity" and "Horizontal Complexity"

Traditional software systems like to grow "vertically":  
- One main line is very deep, going through many layers of abstraction, many layers of calls, many implicit states
- Once problems occur, when debugging, you must follow from the top layer all the way to the bottom layer, and any layer in between might hide pitfalls

In the AI-native world, such deep chains have a fatal problem:  
> A very deep chain is very hard for AI to debug.

Conversely, if we "flatten" complexity and make the system:

- Have more chains, each shorter, shallower, and more independent
- Each chain's logic can be fully understood by AI within a single context window

This is the so-called complexity transformation "from vertical to horizontal."

### 2. Why Horizontal Complexity Is More Suitable for AI-Native Systems

AI's context window is limited, which is already covered in *AI Statelessness and Context Window*. Looking at complexity in combination with this:

- **Single chain with very deep depth**:  
  - Context spans too many modules, files, historical decisions
  - AI has difficulty "fitting in" all the causes and effects in one session
  - When debugging, it's easy to have situations where "I see the local part but can't understand the whole"

- **Multiple similar but independent shallow chains**:  
  - Each chain requires shorter context
  - AI can more easily complete understanding, modification, and verification within one session
  - Comparing two similar but mutually independent chains is something AI is particularly good at

> "A very deep chain is very hard for AI to debug, but AI can handle two very similar chains, as long as these two chains are mutually independent."

### 3. shad-expo-studio: An Attempt to Reduce Vertical Complexity

`https://github.com/ge-limin/shad-expo-studio` is a concrete attempt to reduce vertical complexity:

- Completely isolate frontend presentation layer functionality from functional layer functionality
- Use Storybook for mandatory regression tests to ensure the presentation layer doesn't "quietly drift" as business iterates

The essence of this is splitting "one vertically integrated frontend page" into several more horizontal chains:

- Presentation layer: Styles, component structure, interaction details
- Functional layer: Data flow, business rules, API calls

For AI:

- Presentation layer changes can be locally understood and tested in Storybook scenarios
- Functional layer changes can be locally understood and tested in test code
- Avoids having to "understand the entire page from UI to business to backend" in one session—a deep chain

### 4. story-ops: Compressing Complexity to "User Stories"

`https://github.com/ge-limin/story-ops` is another further exploration, with the goal:

> "user story = PRD = E2E test cases"

That is:

- The unit of complexity is no longer "modules" or "subsystems," but independent user stories one by one
- Each story itself contains: requirement description, expected behavior, end-to-end tests

From a complexity perspective, this is equivalent to:

- Splitting past "large and comprehensive" vertical systems into many "parallel user stories"
- Each story has its own input, output, and verification method
- AI can complete understanding and modification within the scope of one story, without having to swallow the entire system at once

### 5. What to Do Next

If you want your system to evolve from vertical to horizontal, consider several practical paths:

1. **Identify Deep Chains**:  
   Find those key chains that "go from frontend all the way to the bottom layer," and see if they've already exceeded an AI session's comprehensible range.

2. **Split Presentation and Function**:  
   Like shad-expo-studio, physically separate UI and business logic, and establish regression scenarios (like Storybook) for the UI layer.

3. **Use User Stories as Segmentation Units**:  
   Try to make one user story carry its own "complete manual" and "complete tests," rather than relying on a lot of shared implicit state.

4. **Tolerate Moderate Code Duplication**:  
   To make each chain independent and short enough, you must accept some implementations that "look repetitive." This is already mentioned in the "500 functions vs. 5,000 small functions" discussion.

Complexity won't disappear; it will only exist in a different form.  
In the AI-native era, what we need to do is transform complexity from "vertical deep chains that are hard for both AI and humans to control" into "horizontal shallow chains that AI can eat one by one."

