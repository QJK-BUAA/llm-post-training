---
title: Post-Training 技术报告
description: 系统梳理大语言模型后训练的算法原理、工业实践与趋势展望
tags:
  - Post-Training
  - RLHF
  - RLVR
---

# Post-Training 技术报告

<p class="byline">系统梳理大语言模型后训练的算法原理、工业实践与趋势展望</p>

---

<div class="grid cards" markdown>

-   :material-flask:{ .lg .middle } **1. 算法基础**

    ---

    RLHF 与 RLVR 两大范式、统一符号表与核心前置概念，DPO 以及 PPO → GRPO → DAPO → VAPO → CISPO → GSPO → SAPO 的完整演进推导与数值算例。

    [:octicons-arrow-right-24: 开始阅读](./ch1/1.1-training-landscape.md)

-   :material-office-building:{ .lg .middle } **2. 技术报告深度解读**

    ---

    DeepSeek R1/V3/V3.2、Kimi K1.5/K2/K2.5、Qwen2.5/3/3.5、MiniMax 01/M1/M2.5、GLM-5、Seed1.5 等 6 大系列的训练策略与工程经验，附 10 条跨模型共性总结与数据工程全景专题。

    [:octicons-arrow-right-24: 开始阅读](./ch2/2.1-deepseek.md)

-   :material-crystal-ball:{ .lg .middle } **3. 演进路线与趋势展望**

    ---

    从 InstructGPT 到 Agentic RL 的四代范式变迁，6 大行业共识与 5 大核心技术挑战，以及 9 条深度分析与思考。

    [:octicons-arrow-right-24: 开始阅读](./ch3/3.1-timeline-paradigms.md)

</div>

---

!!! tip "阅读建议"
    - **30 分钟把握主脉络** — [1.1 训练全景](./ch1/1.1-training-landscape.md) + [1.2 两大范式与符号体系](./ch1/1.2-rlhf-rlvr.md) + [1.11 公式速查表](./ch1/1.11-cheatsheet.md) + [3.1 演进时间线](./ch3/3.1-timeline-paradigms.md)
    - **吃透算法细节** — 从 [1.3 DPO](./ch1/1.3-dpo.md)、[1.4 PPO](./ch1/1.4-ppo.md) 顺读至 [1.10 SAPO](./ch1/1.10-sapo.md)，每节均配有前置概念铺垫与逐步求导
    - **对齐工业一线实践** — [2.8 跨模型训练经验](./ch2/2.8-cross-model.md) + [2.9 数据工程专题](./ch2/2.9-data-engineering.md) + [3.2 行业共识与挑战](./ch3/3.2-challenges-future.md)
