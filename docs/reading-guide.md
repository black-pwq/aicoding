# Reading Guide

针对 AI Coding / Coding Agent 方向的入门阅读指南。以下 10 篇论文从 [papers.md](papers.md) 中筛选，按推荐阅读顺序排列，由基础概念逐步过渡到系统设计与前沿方向。

## 优先必读论文（Top 10）

### 1. Chain-of-Thought Prompting Elicits Reasoning in Large Language Models

- 链接：https://arxiv.org/abs/2201.11903
- 会议：NeurIPS2022
- 为什么先读：CoT 是所有 agent 推理能力的思想源头。理解"让模型一步步想"，才能理解后续的"边想边做"。

### 2. ReAct: Synergizing Reasoning and Acting in Language Models

- 链接：https://arxiv.org/abs/2210.03629
- 会议：ICLR2023
- 为什么先读：Agent 方向的奠基论文。"推理→行动→观察"的交替循环是几乎所有 Coding Agent 的底层运行逻辑。建立在 CoT 之上，是进入 agent 领域的必经之路。

### 3. Reflexion: Language Agents with Verbal Reinforcement Learning

- 链接：https://arxiv.org/abs/2303.11366
- 会议：NeurIPS2023
- 为什么先读：Agent 自我反思机制的代表作。理解 agent 如何从失败中学习、迭代改进，是理解后续调试型 agent 和自动修复系统的前提。

### 4. CodeAct: Executable Code Actions Elicit Better LLM Agents

- 链接：https://arxiv.org/abs/2402.01030
- 会议：ICML2024
- 为什么先读：证明"用可执行代码作为 agent 行动"优于 JSON 或文本格式，直接影响 Coding Agent 的行动空间设计。读完 ReAct 和 Reflexion 后，这篇帮你理解 agent 该"怎么动手"。

### 5. SWE-bench: Can Language Models Resolve Real-World GitHub Issues?

- 链接：https://arxiv.org/abs/2310.06770
- 会议：ICLR2024
- 为什么先读：Coding Agent 评测的事实标准。定义了"从真实 GitHub issue 出发"的仓库级评测范式，后续几乎所有系统都在此基准上比较。不理解 SWE-bench，就无法正确解读该方向的实验结果。

### 6. SWE-agent: Agent-Computer Interfaces Enable Automated Software Engineering

- 链接：https://arxiv.org/abs/2405.15793
- 会议：NeurIPS2024
- 为什么先读：ACI（Agent-Computer Interface）的提出是本方向最有影响力的思想贡献之一。Agent 的能力上限不只取决于模型，更取决于它如何与环境交互。读完 SWE-bench 后读这篇，理解如何在该评测框架上设计高效系统。

### 7. Agentless: Demystifying LLM-based Software Engineering Agents

- 链接：https://arxiv.org/abs/2407.01489
- 会议：FSE2025
- 为什么先读：最具批判性价值的论文。用两阶段简单方法挑战了"必须用 agent 循环"的默认假设。紧接 SWE-agent 读，形成正反对照，避免陷入过度工程。

### 8. A Survey of Context Engineering for Large Language Models

- 链接：https://arxiv.org/abs/2507.13334
- 会议：CoRR2025
- 为什么先读：上下文工程是决定 agent 系统上限的核心工程能力。在理解了基础方法、评测基准和代表系统之后，再读这篇综述，更容易抓住"上下文构造、检索、压缩、管理"为何正在成为关键差异变量。

### 9. OpenHands: An Open Platform for AI Software Developers as Generalist Agents

- 链接：https://arxiv.org/abs/2407.16741
- 会议：ICLR2025
- 为什么先读：目前最成熟的开源 Coding Agent 平台。放在 context engineering 综述之后阅读，更容易从工程实现角度理解系统如何把上下文管理、工具调用与 agent loop 结合起来。

### 10. Context Before Code: An Experience Report on Vibe Coding in Practice

- 链接：https://arxiv.org/abs/2603.11073
- 会议：CoRR2026
- 为什么先读：这篇把 Vibe Coding 从概念讨论拉回真实工程现场，强调在生产约束下，决定效果的往往不是“先写代码”，而是先明确上下文、边界和不可委托区域。放在最后读，适合用来反看前面方法与系统在真实协作中的落地边界。

## 阅读路线说明

```text
基础理论          系统与评测              前沿方向
─────────       ──────────────        ──────────
CoT ──→ ReAct    SWE-bench ──→ SWE-agent   Context Engineering Survey
   │               │              │
   ↓               ↓              ↓
Reflexion       Agentless        OpenHands
   │
   ↓
CodeAct

实践反思：Context Before Code
```

- **第 1-4 篇**：建立 agent 基础认知（推理、行动、反思、代码行动）
- **第 5-7 篇**：理解评测标准和代表系统（评测→系统→批判）
- **第 8-9 篇**：进入当前核心工程主线（上下文工程→平台实现）
- **第 10 篇**：从真实实践回看人机分工、上下文准备与落地边界

> 完整论文列表与详细评语见 [papers.md](papers.md)。
