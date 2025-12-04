## Chapter 12: Token as a Quantitative Measure of Project Scale

> "Token is a metric that can quantify the information volume contained in a project. The total number of tokens needed to encode all assets of a project is a measure of its scale."

### 1. Why Use Token to Measure Project Scale

In traditional software engineering, we usually measure project scale by:

- Lines of code (LoC)
- Number of files
- Number of functional modules
- Team size

But in the AI-Native era, these metrics all have limitations:

- **Lines of code**: AI-generated code might be very "verbose"—more lines don't mean higher complexity
- **Number of files**: AI tends to generate many small files—file count doesn't reflect real information density
- **Number of functional modules**: Module boundaries become more blurred in the AI era—count doesn't mean much
- **Team size**: AI dramatically increases individual productivity—the relationship between people and project scale is broken

**Token, as a new quantitative metric, has unique advantages:**

1. **Directly Reflects AI's 'Understanding Cost'**  
   How many tokens a project needs for AI to fully understand directly determines:
   - Whether AI can process the entire project in one session
   - How many rounds of AI relay are needed to complete a requirement
   - The complexity of context selection strategies

2. **Unified Measurement of All Assets**  
   Token can uniformly measure:
   - Code
   - Documentation
   - Test cases
   - Configuration files
   - Even meeting recordings, design drafts (if converted to text)

3. **Directly Tied to AI Costs**  
   Token consumption = AI usage cost. This metric directly relates to:
   - Whether the team can continuously use AI
   - Which tools/models are suitable for the current project scale

### 2. The 1M Token and 10M Token Boundaries

Based on practical experience, there are two key numerical boundaries:

- **1M Token**: All content produced by a very small AI-Native team in 15–30 days is roughly at this scale
- **10M Token**: Within this scale, AI-Native solutions can bring at least **3× productivity improvement**

**What 1M Token Means:**

- A medium-sized codebase (tens of thousands to over a hundred thousand lines of code)
- Plus necessary documentation and tests
- Can be fully loaded in a "large context model" (like Gemini's 1 million token)
- AI can understand the entire project's full picture in one session

**What 10M Token Means:**

- A large project, or a collection of multiple related projects
- Already cannot be fully loaded in one session
- Must rely on context selection strategies, letting AI only focus on "relevant parts"
- But within this scale, as long as context selection is done well, AI can still bring significant productivity improvements

**After Exceeding 10M Token:**

- Context selection complexity will rise sharply
- AI accuracy will noticeably decline (because it can always only see "partial context")
- May need to consider "project splitting" or "architecture refactoring," splitting large projects into multiple 1–10M token sub-projects

### 3. How to Measure a Project's Token Scale

A rough estimation method is:

1. **Code Part**  
   - Add up all text from the entire codebase
   - Estimate by "1 token ≈ 4 English characters" or "1 token ≈ 1.5 Chinese characters"
   - Or directly use tools (like tiktoken) for precise calculation

2. **Documentation Part**  
   - Add up all markdown, text documents
   - Similarly estimate by token ratio

3. **Test Part**  
   - Test code and test data
   - If there are many test cases, this part might account for a large proportion

4. **Other Assets**  
   - Configuration files, SQL schemas, API documentation, etc.
   - If the project has "meeting recordings converted to text" or "design drafts converted to text," these should also be included

**Practical Measurement Recommendations:**

- Can use scripts to regularly scan the entire codebase and calculate total token count
- Focus on token count's **growth trend**, not absolute numbers
- If you find token count growing too fast, think: Are documents/tests written too much? Is code duplication too high?

### 4. Impact of Token Scale on Engineering Practice

**Within 1M Token:**

- Can relatively "luxuriously" use AI
- Can have AI read the entire codebase, do global refactoring and optimization
- Documentation can be slightly "redundant," because context space is still sufficient

**Between 1–10M Token:**

- Must start paying attention to context selection
- Documentation must be more concise, only keep "snapshot-style" high-level documentation
- Code must be more modular, so AI can work by "only looking at relevant modules"

**Exceeding 10M Token:**

- Context selection becomes the core bottleneck
- May need to introduce "project indexing," "symbol indexing," and other more complex mechanisms
- Or consider "splitting projects," splitting large projects into multiple independent small projects

### 5. Practical Decision Recommendations

In a two-person small team, strongly dependent on AI, you can use the token metric like this:

1. **Regularly Measure Project Token Scale**  
   - Measure once per month or quarter
   - Focus on growth trends. If growth is too fast, analyze the reasons

2. **Adjust Strategy Based on Token Scale**  
   - Within 1M: Can be "extensive," let AI read more context
   - 1–10M: Start paying attention to context selection, simplify documentation
   - Exceeding 10M: Consider project splitting or architecture refactoring

3. **Use Token Scale to Evaluate Tool/Model Selection**  
   - If the project is within 1M token, can directly use Gemini Web (1 million token context)
   - If exceeding 1M, may need tools like Codex/Cloud Code that use "symbol indexing + intelligent selection"

### 6. Summary

Token, as a quantitative measure of project scale, has unique value in the AI-Native era:

- It directly reflects AI's "understanding cost"
- It uniformly measures all types of project assets
- It's directly tied to AI usage costs

> **1M Token is a 'comfort zone,' 10M Token is a 'critical point.'**  
> Within this range, AI-Native solutions can continuously bring at least 3× productivity improvement.  
> Beyond this range, more complex context selection strategies are needed, or consider project splitting.

Regularly measuring and paying attention to token scale is an important means for AI-Native teams to manage project complexity.

