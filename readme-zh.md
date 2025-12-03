# AI-Native 软件工程宣言（中文）

> English version: [AI-Native Engineering Manifesto (English)](./readme.md)  
> 本仓库还包含一组中文长文扩展章节，位于 `chapters-zh/` 目录，对 11 条真相中的部分主题做了系统展开。

[![Revision March 2025](https://img.shields.io/badge/Revision-March_2025-0a84ff)](#march-2025-cn)
[![Revision May 2025](https://img.shields.io/badge/Revision-May_2025-34c759)](#may-2025-cn)
[![Revision Dec 2025](https://img.shields.io/badge/Revision-Dec_2025-ff9f0a)](#dec-2025-cn)

---

## Table of Contents
- [AI-Native的软件工程理念](#ai-native的软件工程理念)
- [AI-Native的软件工程：2025 年的 11 条真相](#ai-native的软件工程2025-年的-11-条真相)
- [扩展章节：AI-Native 工程实践](#扩展章节ai-native-工程实践)
- [March 2025](#march-2025-cn)
- [May 2025 修订](#may-2025-cn)
- [Dec 2025 修订](#dec-2025-cn)

## AI-Native的软件工程理念

| **Author** | [Limin Ge](https://www.linkedin.com/in/limin-ge-573b4b28a/) |
| --- | --- |
| **First Draft** | March 2025 |
| **Revisions** | May 2025, December 2025 |

---

<a id="ai-native的软件工程2025-年的-11-条真相"></a>
## AI-Native的软件工程：2025 年的 11 条真相

1. 一切诞生了超过3年的知识体系、方法论、技术栈，都应该被淘汰。

2. 你的代码库、文档库、会议纪要、会议录音、团队的记忆、直觉都不是项目真正可依赖的核心资产，唯一可依赖的核心资产有且只有你的测试案例库。（详见《Test–Code 循环：为什么测试代码比功能代码更重要》）

3. 理解AI的关键在于理解**无状态性**。（详见《AI 的无状态性与 Context Window》）

4. 我们可以容忍AI犯错错误，只要它不会在下一次模型迭代前杀死我们。（与调试深水区和 Human-in-the-loop 相关，详见《Debugging：在深水区和 AI 一起查 bug》）

5. 软件的复杂度需要从垂直转为水平

6. AI的context window 的上限，将是新时代程序员最需要关心的资源。（详见《AI 的无状态性与 Context Window》）

7. Plan–Act、Test–Code、Doc–Code–Doc 是新工程时代的工程循环。（详见《AI-Native 工作流：Plan–Act、Test–Code、Doc–Code–Doc》）

8. 代码的未来不是复用和抽象，而是海量彼此独立、足够小、AI 可直接理解的单元。

9. AI不能解决所有问题，AI不能解决第一公里和最后一公里的问题，这本质上是人的问题，

10. AI 生成的 Artifact 是一种新的模态。

11. AI IDE或AI Agent 卖的是Context选择的能力。（详见《工具与 Context 选择：为什么 AI IDE 卖的是“上下文选择能力”》）

---

<a id="扩展章节ai-native-工程实践"></a>
## 扩展章节：AI-Native 工程实践

以下章节对上文中的若干“真相”做了更系统、更工程化的展开，采用了访谈与实战记录中的原始表述，尽量保留了第一手语感：

- 《AI 的无状态性与 Context Window》（对应真相 3、6）  
  - 文件：`chapters-zh/01-ai-statelessness-and-context-window-zh.md`
- 《Test–Code 循环：为什么测试代码比功能代码更重要》（对应真相 2、7）  
  - 文件：`chapters-zh/02-test-code-loop-zh.md`
- 《Debugging：在深水区和 AI 一起查 bug》（对应真相 4、9）  
  - 文件：`chapters-zh/03-debugging-with-ai-zh.md`
- 《工具与 Context 选择：为什么 AI IDE 卖的是“上下文选择能力”》（对应真相 6、11）  
  - 文件：`chapters-zh/04-tools-and-context-selection-zh.md`
- 《AI-Native 工作流：Plan–Act、Test–Code、Doc–Code–Doc》（对应真相 2、3、7、9）  
  - 文件：`chapters-zh/05-ai-native-workflows-zh.md`
- 《从垂直复杂度到水平复杂度》（对应真相 5、8）  
  - 文件：`chapters-zh/06-horizontal-complexity-zh.md`
- 《Human-in-the-loop 与新人培养》（对应真相 4、9）  
  - 文件：`chapters-zh/07-human-in-the-loop-and-onboarding-zh.md`
- 《为 AI 选择兼容的技术栈》（对应真相 1、12）  
  - 文件：`chapters-zh/08-ai-compatible-tech-stack-zh.md`
- 《AI Coding 的五个等级与 User Story Driven 终局》（对应真相 7）  
  - 文件：`chapters-zh/09-ai-coding-levels-and-user-story-driven-zh.md`
- 《AI-Native 小团队的结构性优势》（对应真相 8）  
  - 文件：`chapters-zh/10-small-team-advantage-zh.md`
- 《Convention 与开发规范——让 AI 带着镣铐跳舞》（对应 Dec 2025 修订第 5 条）  
  - 文件：`chapters-zh/11-conventions-and-standards-zh.md`
- 《Token 作为项目规模的量化指标》（对应 May 2025 修订第 5 条）  
  - 文件：`chapters-zh/12-token-as-project-scale-zh.md`
- 《会议录音→PRD→TDD→代码——AI-Native 团队的知识工作流》（对应 May 2025 修订第 2、3 条）  
  - 文件：`chapters-zh/13-knowledge-workflow-pipeline-zh.md`
- 《从垂直复杂度到水平复杂度》（对应真相 5、8）  
  - 文件：`chapters-zh/06-horizontal-complexity-zh.md`
- 《Human-in-the-loop 与新人培养》（对应真相 4、9）  
  - 文件：`chapters-zh/07-human-in-the-loop-and-onboarding-zh.md`
- 《为 AI 选择兼容的技术栈》（对应真相 1、5）  
  - 文件：`chapters-zh/08-ai-compatible-tech-stack-zh.md`
- 《AI Coding 的五个等级与 User Story Driven 终局》（对应真相 7、9、10）  
  - 文件：`chapters-zh/09-ai-coding-levels-and-user-story-driven-zh.md`
- 《AI-Native 小团队的结构性优势》（与整篇宣言的整体取向相关）  
  - 文件：`chapters-zh/10-small-team-advantage-zh.md`

---

<a id="march-2025-cn"></a>
## March 2025

1. 一切诞生了超过3年的知识体系、方法论、技术栈，都应该被淘汰。
2. Plan-Act循环
3. Test-code循环
    1. AI Coding的时代下，测试会变得特别重要，后端的测试相对简单，网页端甚至移动端会难许多，很难端到端测试，尤其是移动端。
4. Doc-Code-Doc循环
5. AI的context window 的上限，将是新时代程序员最需要关心的资源。
6. 文档化，帮助大模型做记忆的cache。
    1. 全量/快照式的文档优于增量式的文档
    2. AI IDE的能力上限就是它的context window的上限，其实人类也是，人类的context window也是有上限的。那么人类是如何handle复杂系统的呢？回想一下大厂是如何协作的就能明白。我们与AI的协作，应该模拟大厂间不同职能、不同团队的协作。
7. Vibe Coding只描绘了一个非常初级的coding阶段，终局应该是user story驱动的开发。现在许多用户将Cursor作为一个简单地辅助完成需求的工具，其实这之后还有好几个等级。反应到思维上，初级阶段程序员还是人的思维，中级阶段里程序员是机器的思维，高级阶段里要更进一步地升级为机器的管理者的思维。等级如下：
    1. 不熟练的AI Coding使用者，使用中文，漫无目的，想到什么做什么，Vibe Coding
    2. 熟练的AI Coding使用者，意识到要用英文，意识到context window有限，意识到cursor并不会读你的文件的全文
    3. 将自己的流程固化下来的使用者，快速应用cursor rules，
    4. Issue Tracker，应用MCP，以一个issue或一个需求为中心，模拟一个团队的完整的协作流程
    5. User Story Driven，整个系统彻底转型为AI-Native的级别，AI能够异步、多线程地工作，同时有100个user story同步开发
8. 人类能够将基建搭得有多好多适配AI的需要，那么AI就能把自己的能力释放得有多好。对于existing system来说，这是一个挑战。
9. 除了AI IDE之外，AI带来的生产力的革新还涉及方方面面，比如说绘制流程图、撰写PRD、PRD转TDD、堆栈分析，端到端测试、等等等等。软件工程的任何侧面都应该有一个新时代下的AI替代品，我从YC上就爬过一个列表（这个列表本身也是一个AI Agent帮助我爬的）。
10. 以往我们会讲究复用抽象等，但是AI没有能力理解那么长的上下文，以往我们可能有精心创作的500个函数，相互复用抽象隔离，新时代我们可能会写5000个scope非常小的相互无关的函数，每一个的scope都在AI的context window之内。(待验证）
11. AI不能解决所有问题，AI不能解决第一公里和最后一公里的问题，即设计方案和最终写对每一行代码，但这本质上不是AI的问题，这本质上是人的问题，人类和AI的关系是审阅者和执行者的关系，但人无法评估自己都不了解的事物。对于一个existing的系统，人自己首先要理解里面的方方面面，之后才能评估AI出的方案的好坏。human in the loop是绝对不可避免的。
12. 过于新的技术堆栈，AI没有能力掌握，因为训练数据过少，例如deno，但如果是成熟的如nextjs，AI可以很快地吐出正确的代码。兼容性这个词有了新的涵义。
13. Prompt一定要写得详细，能够引用的对象就要提供引用，因为不然cursor使用的是RAG的形式去查找的，准确率特别差。未来cursor应该能够要能对符号建立索引才行。现在的大部分AI是非常neutral，非常中立的，我们需要让它变得足够opinionated，并且这个opinion是完全个性化的，完全服务于某个开发者/团队本身的。
14. 四十年前的编程范式，目标是让机器读懂，二十年前是让人读懂，今天我们应该让AI读懂。AI能读懂什么文本是有规律的，但我们也不应该过分地finetune我们的prompt以至于overfitting，因为AI本身能力也在演进，例如COT的诞生、DeepSeek的opinionated的属性，这使得许多prompt engineering的技巧迅速落伍，所以这是一个永恒的话题。

---

<a id="may-2025-cn"></a>
## May 2025 修订
1. 从商业模式的角度，ai ide就不可能提供llm web端能提供的服务水平，站在使用者的角度，最好的服务来自于API调用或者Web端
2. 一些曾经更激进的想象，我们有钱有人力后，可以开始试验：将所有的会议录制->生成字幕->生成prd->生成tdd->生成code draft。可以使用browser use做中介，转发内部的所有知识（包括代码库）到Gemini Web。以此提升团队内部所有工作的生产力。结合新的flowith、Manus等工具。这个内部的工作平台将成为每一个岗位，每一个成员的主要工作平台。作为新团队，我们没有那么多的历史债务，可以快速地收集所有的知识到这里。
3. 另一个用例：使用通用MCP，集成manus、flowith等工具，如运营需要生产100个场景内容，Agent自动完成这个任务，人肉确认通过后，就可以导入我们平台。这个Agent将成为全团队浏览器的首页，是所有工作的入口和起始点
4. 对于有一定历史积淀的团队来说，Context的窗口是无论如何都不够用的，此时的关键就来到了Context的择优，也就是所有的AI IDE团队，所有的AI Agent团队最核心的工作内容。
5. token是一个可以对一个项目所含信息量进行量化的一个指标，一个项目沉淀的所有资产转换为token的数量就是对这个项目规模的衡量。目前我们正好在1M Token左右，在10M Token之内，这个方案都会一直带来至少3倍的生产力提升
6. AI IDE或AI Agent卖的是两个：一个是Context选择的能力，一个是最佳实践通用化的能力
7. 由AI IDE创造的artifact是一种新的模态，它的意义就像人们第一次可以在网上发帖，传图片，传音频视频一样，面向普通人群的AI IDE应该打通到部署的最后一英里。
8. AI IDE的codebase index应该是AST，符号级别的

---

<a id="dec-2025-cn"></a>
## Dec 2025 修订
1. 如何解决llm引入的bug：
    1. 将我们工作的重心从管理功能代码，转移成管理测试代码，只要我有足够海量的测试案例，我能够确保这些情况下最终的结果是正确的，我们就能够减少管理功能代码过程中的负担
    2. 我们可以容忍AI犯错，只要这个错误不会在3个月内杀死我们即可，因为3个月后模型能力将会进一步迭代，将会解决曾经我们无法解决的问题。
    3. 但是，一个先进的AI团队，一定会始终顶着AI模型能力的上限去使用AI，并且会非常快地达到每一个AI的能力上限，这个团队的大多数时候仍会处在AI无法解决我们问题的煎熬中。
2. 我们应该将软件的复杂度从垂直转为水平——仍然是过去的2025.3时提出的思路10的延伸，即通过增加链路的多样性，来实现链路的深度降低。一个非常深入的链路AI很难debug，但AI可以处理两条非常相近的链路，只要这两条链路相互独立即可。
3. https://github.com/ge-limin/shad-expo-studio 是一个降低垂直复杂度的尝试，即将前端展示层和功能层的功能彻底隔离，并且通过storybook强制的回归测试来确保展示层不漂变
4. 你的代码库、文档库、会议纪要、会议录音、团队的记忆、直觉都不是项目真正可依赖的核心资产，唯一可依赖的核心资产有且只有你的测试案例库， https://github.com/ge-limin/story-ops 是一个更深入的探索，其愿景是user story = prd = e2e test cases。
5. Convention、开发规范的重要性，对于AI-Native团队的重要性，只会更高，因为它们是延缓熵增最好的手段。项目起步时一定要尽可能地设计好尽可能多地束缚。让AI带着镣铐跳舞。
6. 如果AI一次工作的context和能力有上限，就需要让AI接力在某件事情上工作。最好的benchmark方式就是检验一个非常难以处理的bug，究竟是否可以通过这种方式解决。接力的方式就是在一个AI能力即将下滑的阶段，让它把本次尽可能多的context持久化，后续的AI在此基础上进一步工作，就像人类一样，总是站在巨人的肩膀上学习，而不会重新发明轮子，否则人类的科技只会锁死。
7. 理解AI的关键在于理解**无状态性**，代码库应该抛弃所有的过程性、历史性信息，让任何一个读者（你的每一个AI session）都不用去理解任何历史上下文。
