---
title: Agentic RL 调研报告
description: 多轮交互、工具使用、长程规划场景下的强化学习算法与系统调研报告
tags:
  - Agentic RL
  - 多轮交互
  - 工具使用
---

# Agentic RL 调研报告

<p class="byline">基于 47 篇代表性论文（2024–2026 Q1）与工业级 Agent 系统的结构化分析</p>

---

<div class="grid cards" markdown>

-   :material-flask:{ .lg .middle } **1. 算法与核心挑战**

    ---

    从单轮推理 RL 到多轮 Agentic RL 的本质范式跨越，围绕**奖励信号、训练稳定性、探索效率、信用分配**四大挑战剖析 IGPO、SeeUPO、ARLArena、VCPO、EMPO²、GiGPO、ELPO、ProxMO 等代表算法与工程系统。

    [:octicons-arrow-right-24: 开始阅读](./ch1/1.1-overview.md)

-   :material-crystal-ball:{ .lg .middle } **2. 全景分析与展望**

    ---

    2024–2026 领域演进时间线、全球核心研究机构分布、三条主干技术路线（修复基础算法 / 重新建模问题 / 增强环境与记忆基础设施）对比，以及六条核心判断与未来预测。

    [:octicons-arrow-right-24: 开始阅读](./ch2/2.1-landscape.md)

</div>

---

## 与《Post-Training 技术报告》的分工衔接

| 内容维度 | Post-Training 技术报告 | Agentic RL 调研报告（本篇） |
|----------|------------------------|----------------------------|
| **PPO / GRPO / DAPO / VAPO / CISPO / GSPO / SAPO** | **完整公式推导与梯度分析** | 作为单轮基线简要引用 |
| **单轮长思维链推理（数学 / 竞赛代码）** | **核心焦点** | 前置背景与成功边界对照 |
| **多轮环境交互、工具调用与跨步归因** | 从旗舰模型流水线视角切入 | **核心焦点（按四大算法挑战拆解）** |
| **47 篇专项 Agentic RL 前沿论文横向测绘** | 未单独展开 | **系统分类、机制对比与局限剖析** |

---

??? abstract "核心代表论文速查索引"
    | 算法 / 系统 | arXiv 编号 | 核心技术贡献 | 影响层级 |
    |------------|-----------|-------------|----------|
    | **GLM-5** | [2602.15763](https://arxiv.org/abs/2602.15763) | Slime 异步 Agentic RL 框架、TITO 与确定性算子排障、跨阶段蒸馏 | Tier 1 工业标杆 |
    | **Kimi K2 / K2.5** | [2507.20534](https://arxiv.org/abs/2507.20534) / [2602.02276](https://arxiv.org/abs/2602.02276) | 3K→20K MCP 世界模拟器合成、闭环 Rubric 与 PARL 并行蜂群 | Tier 1 工业标杆 |
    | **SeeUPO** | [2602.06554](https://arxiv.org/abs/2602.06554) | 多智能体顺序决策重建模 + 逆向归纳首个多轮全局收敛保证 | Tier 2 理论突破 |
    | **EMPO²** | [2602.23008](https://arxiv.org/abs/2602.23008) | 跨回合自生成记忆探索 + On/Off-policy 记忆参数化内化 | Tier 2 范式创新 |
    | **GiGPO** | [2505.10978](https://arxiv.org/abs/2505.10978) | Episode + Anchor State（锚点状态）双层分组步级优势估计 | Tier 3 归因代表 |
    | **ARLArena / SAMPO** | [2602.21534](https://arxiv.org/abs/2602.21534) | 四维正交稳定性消融框架，定位异策略负优势崩溃根因 | Tier 3 系统分析 |
    | **ELPO** | [2602.09598](https://arxiv.org/abs/2602.09598) | 二分树搜索精确定位“首个不可挽回错误步”并分层自适应裁剪 | Tier 3 归因创新 |
    | **ProxMO** | [2602.19225](https://arxiv.org/abs/2602.19225) | 连续语义邻近性软聚合基线，突破离散锚点匹配限制 | Tier 3 归因创新 |
    | **VCPO** | [2602.17616](https://arxiv.org/abs/2602.17616) | 基于有效样本量（ESS）的异策略动态学习率与闭式最小方差基线 | Tier 3 稳定优化 |
    | **IGPO** | [2510.14967](https://arxiv.org/abs/2510.14967) | 基于真值后验概率边际提升（信息增益）的轮级内在密集奖励 | Tier 4 奖励设计 |
    | **LUFFY** | [2504.14945](https://arxiv.org/abs/2504.14945) | 融合外部强示范轨迹与策略塑形的 Mixed-Policy GRPO | Tier 4 探索增强 |
    | **CM2** | [2602.12268](https://arxiv.org/abs/2602.12268) | 面向多轮工具调用的细粒度多维 Checklist 结构化奖励 | Tier 4 奖励设计 |

---

!!! tip "阅读路径建议"
    - **15 分钟把握全局** — [1.1 核心矛盾与四大挑战](./ch1/1.1-overview.md) + [1.5 算法速查与路线图](./ch1/1.5-algorithm-summary.md) + [2.2 核心判断与预测](./ch2/2.2-outlook.md)
    - **深入四大技术难点** — [1.2 奖励信号与训练稳定性](./ch1/1.2-reward-stability.md) + [1.3 探索效率与信用分配](./ch1/1.3-exploration-credit.md)
    - **工业落地与生态视角** — [1.4 工业工程与环境构建](./ch1/1.4-engineering.md) + [2.1 领域全景与三条路线](./ch2/2.1-landscape.md)
