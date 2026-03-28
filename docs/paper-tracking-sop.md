# Paper Tracking SOP

本页用于规范 AI coding、vibe coding、智能体（Agents）相关论文的持续追踪流程，帮助稳定发现新论文、筛选重点文献，并沉淀进入资源库。

## 适用目标

- 跟踪与实验室主线研究方向高度相关的新论文
- 提高论文发现、筛选、阅读与收录的效率
- 建立相对稳定、可复用的论文雷达机制

## 重点追踪方向

建议优先围绕以下几类主题持续追踪：

- Coding Agent 系统与工作流
- 上下文工程（context engineering）
- vibe coding 与人机分工边界
- 多 agent 协作
- 工具调用、MCP 与权限治理
- benchmark、评测与生产环境度量
- 安全、可靠性与企业落地风险

## 核心渠道

### 1. Hugging Face Papers

- [Hugging Face Papers](https://huggingface.co/papers)

适合快速发现“最近有哪些论文开始被社区关注”。对 agents、tool use、context engineering、code generation、benchmark 这类热点方向较敏感，适合作为日常入口。

### 2. arXiv 最新提交

建议重点关注以下分类：

- [cs.AI](https://arxiv.org/list/cs.AI/recent)
- [cs.SE](https://arxiv.org/list/cs.SE/recent)
- [cs.CL](https://arxiv.org/list/cs.CL/recent)
- [cs.LG](https://arxiv.org/list/cs.LG/recent)
- [cs.CR](https://arxiv.org/list/cs.CR/recent)

其中：

- `cs.AI` 适合看 agents、planning、tool use、autonomy
- `cs.SE` 适合看 software engineering agents、code generation、benchmark
- `cs.CL` 适合看 context engineering、prompting、retrieval、reasoning
- `cs.LG` 适合看 agent learning、self-improvement、training-related work
- `cs.CR` 适合看 MCP、权限治理、安全和风险分析

### 3. OpenReview

- [OpenReview Venues](https://openreview.net/venues)

适合追踪 ICLR、NeurIPS、ICML 等顶会的在审与已收录论文。对 agents、reasoning、tool use、benchmark 方向尤其重要。

### 4. alphaXiv

- [alphaXiv](https://www.alphaxiv.org/)

适合在发现候选论文后查看社区讨论、阅读批注和快速判断“标题是否大于内容”。

### 5. Semantic Scholar

- [Semantic Scholar](https://www.semanticscholar.org/)

适合建立关键词级别的长期 alert，建议关注：

- `coding agent`
- `software engineering agent`
- `context engineering`
- `tool use`
- `vibe coding`
- `MCP security`
- `agent benchmark`

## 推荐执行节奏

### 每日

建议用 10 到 15 分钟完成快速扫面：

1. 浏览 `Hugging Face Papers`
2. 记录标题明显相关的候选论文
3. 对特别相关的论文立刻加入待筛选列表

### 每周

建议做一次系统性整理：

1. 扫一遍 `arXiv cs.AI / cs.SE / cs.CL / cs.LG / cs.CR`
2. 合并本周从 Hugging Face Papers 记录的候选论文
3. 删除明显无关或重复论文
4. 选出值得精读的候选

### 每月

建议做一次集中更新：

1. 查看 `OpenReview` 和主要顶会的新论文
2. 回顾 `Semantic Scholar` 的 alert 结果
3. 从候选论文中挑选值得进入 `papers.md` 的条目
4. 对重点论文补简介、推荐语与分类

## 初筛标准

优先保留以下论文：

- 与当前研究主线高度相关
- 提出明确方法、系统或 benchmark
- 对后续实验设计或工程实现有实际参考价值
- 在社区已有一定讨论度，或问题切得非常准

优先降低以下论文的处理优先级：

- 标题相关但实质偏离主线
- 仅做非常局部的小改动，方法增量有限
- 与编程 agent 关系很弱、只属于泛 LLM 话题
- 很难转化为研究问题、实验变量或工程实践

## 推荐筛选流程

1. 发现论文
来源可以是 Hugging Face Papers、arXiv、OpenReview、alphaXiv 或 Semantic Scholar。

2. 判断是否与主线相关
先判断它更偏哪一类：

- Coding Agent
- 上下文工程
- vibe coding
- 多 agent
- MCP / 工具治理
- benchmark / 评测
- 安全 / 风险

3. 判断论文性质
区分它属于：

- 综述
- 概念文
- 方法论文
- 系统论文
- benchmark / 测量论文
- 经验报告

4. 判断是否值得进入 `papers.md`
如果满足“方向相关 + 有代表性 + 对后续工作有帮助”，则进入 `papers.md` 候选列表。

5. 补全文档信息
加入 `papers.md` 时，按现有页面风格补全：

- 论文题目
- 论文链接
- venue / year
- 1 到 2 句简介
- 推荐语与评分

## 与 `papers.md` 的衔接规则

- 综述、概念界定、经验入口型论文优先进入“综述与概念入口”
- 通用 agent 方法进入“Agent 基础方法”
- 面向软件工程任务的 agent 框架与多 agent 编程系统进入“Coding Agent 系统”
- 上下文管理、压缩、演化类论文进入“上下文工程”
- 安全、权限治理、风险分析进入“安全与风险分析”
- benchmark、生产测量与评测类论文进入“评测与基准”

## 建议的最小工作流

如果时间有限，建议至少执行这个精简版流程：

1. 每天看 Hugging Face Papers
2. 每周看一次 arXiv `cs.AI / cs.SE / cs.CL`
3. 每月集中更新一次 `papers.md`

## 后续可补充内容

- 关键词订阅模板
- 候选论文记录表模板
- 每周追踪例会模板
- 从论文发现到收录的 checklist
