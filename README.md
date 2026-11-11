<div align="center">

# LLM Post-Training & Agentic RL

**系统性梳理大语言模型后训练与 Agentic RL 的算法原理、工业实践与前沿方向**

[![在线阅读](https://img.shields.io/badge/在线阅读-blue?style=for-the-badge&logo=materialformkdocs&logoColor=white)](https://QJK-BUAA.github.io/llm-post-training/)
[![论文](https://img.shields.io/badge/50%2B_Papers-purple?style=for-the-badge&logo=arxiv&logoColor=white)](#)
[![模型](https://img.shields.io/badge/12%2B_Models-teal?style=for-the-badge&logo=huggingface&logoColor=white)](#)
[![License: MIT](https://img.shields.io/badge/License-MIT-green?style=for-the-badge)](LICENSE)

</div>

---

## 概述

本仓库包含两份互补的技术调研报告，覆盖 50+ 篇论文与 12+ 主流模型技术报告（DeepSeek / Qwen / Kimi / MiniMax / GLM-5 / Seed 等），系统解构 2024–2026 年大语言模型后训练与 Agentic RL 领域的核心进展。全书在保留原始调研脉络的基础上，补齐了前置数学与概念铺垫，并逐项对齐了原始论文中的公式、消融数据与系统机制。

### Post-Training 技术报告

> PPO → GRPO → DAPO → VAPO → CISPO → GSPO → SAPO 的算法演进全景

| 章节 | 内容 |
|:-----|:-----|
| **1. 算法基础** | RLHF 与 RLVR 两大范式、全局符号与前置概念，DPO 与 7 种策略优化算法的完整推导与对比 |
| **2. 技术报告深度解读** | DeepSeek、Kimi、Qwen、MiniMax、GLM-5、Seed 六大模型系列的训练流水线、跨模型经验与数据工程专题 |
| **3. 演进路线与趋势展望** | 四代范式变迁时间线 · 6 大行业共识 · 5 大核心技术挑战 · 9 条深度分析与思考 |

### Agentic RL 调研报告

> 多轮交互 · 工具使用 · 长程规划场景下的 RL 算法，47 篇论文系统分析

| 章节 | 内容 |
|:-----|:-----|
| **1. 算法与核心挑战** | 奖励信号、训练稳定性、探索效率、信用分配四大挑战及代表性方案（IGPO / SeeUPO / EMPO² / GiGPO / ELPO / ProxMO 等） |
| **2. 全景分析与展望** | 领域时间线 · 三条技术路线对比 · 产业落地观察 · 未来方向预测 |

## 本地运行与构建

```bash
pip install -r requirements.txt
mkdocs serve            # 本地预览 http://127.0.0.1:8000
mkdocs build --strict   # 严格检查构建
```

## 致谢与许可

MIT License · 内容框架源自 [XavierZhang2002/agentic-rl-analysis](https://github.com/XavierZhang2002/agentic-rl-analysis)，经原论文核验与教学重构后发布。
