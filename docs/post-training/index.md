# 后训练笔记

<p class="byline">材料来自 2024–2026 年的技术报告与算法论文。原文综述：<a href="https://xavierzhang2002.github.io/agentic-rl-analysis/">LLM Post-Training 与 Agentic RL 研究</a>。</p>

<div class="grid cards" markdown>

-   **1. 算法基础**

    ---

    先分清旧策略、参考模型和奖励。然后顺着 PPO、GRPO、DAPO、VAPO、CISPO、GSPO、SAPO 看每一项改动。

    [从训练全景开始](ch1/1.1-training-landscape.md)

-   **2. 技术报告**

    ---

    DeepSeek、Kimi、Qwen、MiniMax、GLM-5、Seed 的流水线，加上闭源模型里能核对的部分、跨模型经验和数据工程。

    [从 DeepSeek 开始](ch2/2.1-deepseek.md)

-   **3. 趋势与判断**

    ---

    从 InstructGPT 到 Agentic RL 的范式变化、目前能并列站住的共识，以及原综述作者的判断。

    [从时间线开始](ch3/3.1-timeline-paradigms.md)

</div>

!!! tip "三十分钟路径"
    [1.1](ch1/1.1-training-landscape.md)、[1.2](ch1/1.2-rlhf-rlvr.md)、[1.11 速查](ch1/1.11-cheatsheet.md)、[3.1](ch3/3.1-timeline-paradigms.md)。

!!! note "这一版改了什么"
    主体仍是原综述的章节和结论。改动集中在四类：概念在第一次使用前定义；旧策略 \(\pi_{\theta_{\mathrm{old}}}\) 和参考模型 \(\pi_{\mathrm{ref}}\) 分开；CISPO、DAPO 消融、K3 散度、GLM-5 的熵变化与原论文对齐；工业章不再把算法重写成另一种公式。
