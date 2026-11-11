# 大模型后训练笔记

<p class="byline">重写自 <a href="https://github.com/XavierZhang2002/agentic-rl-analysis">zhenliang / agentic-rl-analysis</a> 的后训练报告，并按公开论文核对了公式与数字。</p>

这份笔记回答三件事：后训练在整条训练流程里做什么，PPO 之后的算法各自改了目标函数的哪一项，以及 DeepSeek、Kimi、Qwen、MiniMax、GLM、Seed 实际怎么把这些算法跑起来。

阅读顺序：

- 先建立对象：[1.1 训练全景](post-training/ch1/1.1-training-landscape.md) 和 [1.2 两大范式](post-training/ch1/1.2-rlhf-rlvr.md)。1.2 固定了后文所有符号。
- 算法按依赖往下读：DPO 和 PPO 可以并列看，GRPO 依赖 PPO 的裁剪，DAPO、CISPO、GSPO、SAPO 都在改 GRPO 的比率，VAPO 把价值网络加回来。
- 工业章节只讲流水线、数据和工程，不再改写算法定义。算法以第 1 章为准。
- 第 3 章的个人判断沿用原综述的问题意识。前提已被论文改写的地方，正文会直接写成核对后的版本。

本地常用的两个指标先记在这里。**AIME** 是美国数学邀请赛，后训练论文多用它看竞赛数学。**avg@k** 是同一题采样 k 次的平均准确率；**pass@k** 是 k 次里至少对一次的比例。pass@k 通常高于 avg@k，不能把它当成平均分。
