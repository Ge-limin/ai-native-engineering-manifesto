## 第 9 章：AI Coding 的五个等级与 User Story Driven 终局

> "Vibe Coding 只描绘了一个非常初级的 coding 阶段，终局应该是 user story 驱动的开发。"

> 延伸阅读：用户故事如何实现水平复杂度转型，参见[*从垂直复杂度到水平复杂度*](./06-horizontal-complexity-zh.md)。连接用户故事到代码的完整知识工作流，参见[*会议录音→PRD→TDD→代码——AI-Native 团队的知识工作流*](./13-knowledge-workflow-pipeline-zh.md)。

### 1. 从 Vibe Coding 到机器管理者

今天很多人使用 AI IDE（比如 Cursor），停留在一个很初级的阶段：

- 想到什么就打一段中文  
- 让 AI 帮忙“把这个需求做一下”  
- 看看效果，大概能跑就行

这就是所谓的 **Vibe Coding**：  
更多是一种凭感觉的、没有清晰边界和结构的使用方式。

但如果你把时间拉长，会发现 AI Coding 的使用者，其实有一条非常清晰的“段位进化路径”：

> “初级阶段程序员还是人的思维，中级阶段程序员是机器的思维，  
>  高级阶段要进一步升级为机器的管理者的思维。”

### 2. 五个等级的 AI Coding 使用者

一个比较清晰的分级可以是：

1. **不熟练的 AI Coding 使用者**
   - 使用中文，漫无目的，想到什么做什么  
   - 不意识到 context window 有限  
   - 不意识到 AI IDE 并没有读完你整个代码库

2. **熟练的 AI Coding 使用者**
   - 意识到要用英文  
   - 意识到 context window 有限  
   - 意识到 Cursor 并不会读你的文件全文，而是做片段检索  

3. **将自己的流程固化下来的使用者**
   - 有一套稳定的 prompt pattern 和工作流  
   - 能够快速应用自己的 Cursor 规则、命令行工具、模板  

4. **Issue Tracker 级别的使用者**
   - 会用 MCP、Issue Tracker 等工具，将“一个 issue / 一个需求”当成协作的核心单元  
   - 能够围绕一个 issue，模拟一个完整团队的协作流程（需求 → 设计 → 开发 → 测试）  

5. **User Story Driven 的 AI-Native 团队**
   - 整个系统彻底转为 AI-Native：  
     - user story 是第一等公民  
     - AI 可以异步、多线程地工作  
     - 可以同时有 100 个 user story 在不同的阶段并行推进

### 3. 为什么终局一定是 User Story Driven

从工程角度看，User Story Driven 有几个天然优势：

- **天然的切分单位**：  
  一个 user story 自带上下文、期望行为、验收标准，很适合作为 AI 的工作单元。

- **天然的测试载体**：  
  在理想状态下，一个 user story = 一组端到端测试，这在 `story-ops` 的探索里已经被明确提出。

- **天然适合水平复杂度**：  
  每个 story 都是一条相对独立的浅链路，可以很好地贴合"复杂度从垂直到水平"的思路（详见[*从垂直复杂度到水平复杂度*](./06-horizontal-complexity-zh.md)）。

当团队真正到达 User Story Driven 的阶段时：

- 产品、设计、工程、测试之间的主语，全部变成了 “story”  
- AI 不是直接对“代码”做操作，而是对 “一个 story 的完整生命周期” 做操作  
- 代码、文档、测试都变成 story 的衍生物

### 4. 如何从今天的自己，往上升一级

现实情况下，你不需要一开始就冲到第 5 级，可以先问自己一个问题：

> “我今天所处的 AI Coding 等级是几级？  
>  我下一步可以做什么，让自己往上升一级？”

一些实际可行的升级路径：

- 从 1 → 2：  
  - 改用英文  
  - 显式考虑 context window 的大小和内容选择  

- 从 2 → 3：  
  - 把高频操作固化成文档、模板、命令  
  - 让 AI 先读这些规则，再开始工作  

- 从 3 → 4：  
  - 以 issue 为单位组织工作  
  - 对每个 issue 明确：输入是什么、产出是什么、验证方式是什么  

- 从 4 → 5：  
  - 把 issue 再抽象成 user story  
  - 尝试做到：一条 story 自带 PRD + TDD + 测试案例  
  - 用工具（比如 future 的 story-ops）把 story 变成所有工种的主入口

AI-Native 的终局，不是某一个炫酷的工具，而是一种新的“以 user story 为原子单元”的协作方式。  
从 Vibe Coding 到 User Story Driven，是一条关于“如何与 AI 合作”的成长曲线。 


