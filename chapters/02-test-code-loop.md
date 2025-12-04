## Chapter 2: Test–Code Loop—Why Test Code Is More Important Than Functional Code

> "You must spend a lot of time—more than 50%—writing testing code."

> Extended reading: Why the test case library is the only reliable asset in a stateless world, see *AI Statelessness and Context Window*.

### 1. The Productivity Paradox: Why Nobody Wrote Tests in the Past

Before AI, everyone knew test code was important, but in reality, 99% of teams didn't write test code. The reasons were:

- Human resources were both sufficient and insufficient
- "Sufficient" meant: there were test engineers to help us test
- Insufficient meant: there were too many requirements. You couldn't even finish writing functional code, let alone test code
- If someone could help you test manually, why write test code?

This logic made sense in the past, but it doesn't work today.

### 2. AI "Flattens" Teams: Brain Capacity vs. Code Volume

With AI assistance today, everyone's productivity is too high, directly leading to reduced team size.

> "No matter how strong AI is, human brains still need to have control over the project. Once you relax control, it will collapse immediately."

In the past, a project had a team of ten people. Everyone could share part of the work, and everyone worked slowly with long cycles, so everyone had plenty of time to understand and master every detail in the code.

But today, what ten people did in the past might be done by one person, and in one-third of the time.  
This means: **You need to remember and understand in one brain, in one-third of the time, the information that used to require "one team × three times the time" to master.**

For AI-native teams, this is a huge challenge.

### 3. Using Massive Tests to Cover What Brains Can't Cover

In this situation, how do we ensure software quality? A very natural idea is:

> "Use massive test code to cover the parts your brain can't cover."

- AI is very good at writing test code, because test code isn't difficult—it's pure grunt work
- Humans don't like doing grunt work, but AI has no problem with it
- We already know very clearly that AI-generated code is unreliable, and human brains can't fully review it

Under this premise, the only effective way to protect yourself is to use massive test cases to cover:

1. When writing new features, you already ensure the new feature is likely correct
2. In the future, when you modify other code, if you accidentally touch this part, you'll know immediately—use test cases to discover when AI oversteps and touches things it shouldn't

### 4. Programming in Chaos: The Essence of Test–Code

> "Today's AI programming can be understood as programming in uncertainty, in chaos, in confusion. We already know very clearly that AI-generated code is unreliable."

But we have to let AI write code because its productivity is too high. We have to accept this chaos, accept this uncertainty.

In this situation, the only effective thing to protect yourself is your test cases:

- As long as you ensure you respect test cases enough
- When reviewing test cases, be careful enough
- Don't casually modify test cases

Test cases can always protect you at all levels, all scopes, and all links.

### 5. Managing AI-Generated Tests: Frameworks and Constraints

First, test code must of course meet your requirements. At the beginning, you still need to set up the testing framework and testing conventions.

Because when AI writes code, it will reference nearby or related code:  
You already have some test cases there, and it will use similar patterns to write, which is likely fine.

Second, when modifying code and reviewing code, you must spend a lot of time and attention to see: **Has AI touched the test cases?**

- If test code has really been touched, you must think clearly:
  - Why was it touched?
  - Can it be touched?
  - Should it be touched?
- If you can't explain why test cases were touched, it means this work might need to be redone

### 6. Defect Explosion: Why "Just Writing a Bit More Code" Becomes a Disaster

In Silicon Valley, many teams work on AI testing. They have a curve chart:

- One curve is "all human code volume/engineer productivity," gradually rising over time with a relatively low and stable slope
- Rising code productivity means the number of engineers is rising, and the number of test engineers is also rising synchronously
- So as code production increases, the number of bugs you can solve also increases. These three lines remain relatively consistent

But after AI appeared, this situation changed:

- AI directly pulled up the line of human code production, and the slope became very large
- As code production rises, the number of defects will also be pulled up in a straight line
- Because it's written by AI, written too fast, and team size has decreased, **the speed of defect increase may be faster than the speed of code increase**

So it becomes:

> The slope of defect quantity is the highest, followed by code quantity, and finally test engineer quantity.

The number of test engineers cannot expand 3–4 times overnight.  
This means: several times more defects appearing overnight cannot be covered by humans.

This is a very dangerous but inevitable trend. We've already seen many cloud vendors and internet infrastructure vendors have many accidents this year, and this is the reason.

### 7. Test–Code Loop: From "Code-First" to "Test-First"

> "The test-to-code loop is essentially because code productivity has risen too fast."

In this situation, you need to both cover the faster-rising defect count and accept the reality of "fewer brains, fewer people."  
There's only one solution: **Use massive test cases to fill the gap.**

This also explains why, in this context, test code is more important than functional code:

- Before: Functional code was most important, test code was said to be important but no one actually wrote a single line
- Now: Test code is much more important than functional code

Because often, AI-modified functional code has far exceeded your cognitive burden and cognitive limits—you simply can't grasp it.  
At this point, the only thing you can trust is your entire set of massive test code:

- **Test code passes**: It means the changes are likely still controllable
- **Test code fails**: It's recommended to carefully review, or even try to redo this work

> In deep-water debugging scenarios, how tests work with logs and documentation, see *Debugging: Finding Bugs with AI in Deep Waters* and *AI-Native Workflows: Plan–Act, Test–Code, Doc–Code–Doc*.

