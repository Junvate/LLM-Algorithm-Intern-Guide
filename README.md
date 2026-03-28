# 🚀 大模型算法岗实习面经 | 包含 DeepSeek/Qwen 技术报告解析、手撕 PPO/RoPE/Transformer、RLHF 核心与八股文 | 持续更新中... [笔记链接](https://my.feishu.cn/wiki/Ipm5woCF1i28pPkFqtMcAhQyndh?from=from_copylink)

## 📈 Star History

[![Star History Chart](https://api.star-history.com/svg?repos=Junvate/LLM-Algorithm-Intern-Guide&type=Date)](https://star-history.com/#Junvate/LLM-Algorithm-Intern-Guide&Date)



[![License](https://img.shields.io/badge/license-MIT-blue.svg)](LICENSE)
[![PRs Welcome](https://img.shields.io/badge/PRs-welcome-brightgreen.svg)](CONTRIBUTING.md)
[![DeepSeek](https://img.shields.io/badge/Focus-DeepSeek%2FRLHF-red)](README.md)

> **写在前面**：
> 本仓库记录了我在准备大模型算法岗实习过程中的核心笔记。
> 这里的每一个知识点都是我在面试时被实际问到或者在小红书收集到的八股面经
> 内容全部托管在飞书文档

## 📚 核心文档导航 (Document Navigation)

所有内容已整理为飞书文档，**点击下方链接即可查看**：[笔记链接](https://my.feishu.cn/wiki/Ipm5woCF1i28pPkFqtMcAhQyndh?from=from_copylink)


<table align="center">
  <tr>
    <td align="center">
      <img src="https://github.com/user-attachments/assets/4ca9cebc-49d6-4068-8f9d-6c21e4be8e74" width="260" />
      <br />
      <sub>目录</sub>
    </td>
    <td align="center">
      <img src="https://github.com/user-attachments/assets/b8e6b2a8-a944-4828-a800-9196ad0a77b1" width="260" />
      <br />
      <sub>目录</sub>
    </td>
    <td align="center">
      <img src="https://github.com/user-attachments/assets/c785c30d-b7e6-44d3-8900-891da8ef8fb9" width="260" />
      <br />
      <sub>目录</sub>
    </td>
  </tr>
</table>


### 🏗️ 第一章：大模型基础与架构 (Architecture & Math)
*面试造火箭的基础，包含 Transformer 变体与底层数学原理。*
- [x] **[Transformer 核心架构与 Attention 变体 (MHA/MQA/GQA/MLA)]** `High Frequency`
  - *解析 DeepSeek 为什么使用 MLA (多头潜在注意力) 进行 KV Cache 压缩*
- [x] **[位置编码进化史：从绝对位置到 RoPE (旋转位置编码) 代码推导]**
- [x] **[显存优化必考：KV Cache 计算公式与 PagedAttention (vLLM) 原理]**
- [x] **[机器学习基石：优化器 (SGD/Adam) 与 损失函数 (Cross-Entropy/MSE)]**
- [x] **[精度与量化：FP32 vs FP16 vs BF16 及显存估算指南]**

### 🤖 第二章：Agent 应用与 RAG 系统 (RAG & Agent)
*从“鹦鹉学舌”到“自主智能”，涵盖最新的 MCP 协议与检索增强。*
- [x] **[RAG 全链路：Chunking 切片、向量检索与 Query 改写策略]**
- [x] **[Rerank (重排序) 详解：Bi-Encoder vs Cross-Encoder 的本质区别]** `Project Essential`
- [x] **[Agent 新范式：MCP (模型上下文协议) 是什么？(含 Python 示例)]** `New`
- [x] **[Agent Skill：如何定义大模型的“手脚”与工具调用]**

### 🔧 第三章：高效微调与训练 (PEFT & Training)
*如何低成本训练大模型？SFT 细节与灾难性遗忘解决方案。*
- [x] **[LoRA 矩阵初始化原理：为什么要 A 高斯 B 全 0？]**
- [x] **[QLoRA 核心技术：NF4 量化与双重量化解析]**
- [x] **[微调进阶：AdaLoRA、DoRA 与 P-Tuning 选型指南]**
- [x] **[灾难性遗忘 (Catastrophic Forgetting)：原因与 Replay/Freeze 解决方案]**

### ⚔️ 第四章：RLHF 与对齐算法 (Alignment & RL)
*DeepSeek-R1 引爆的核心板块，从 PPO 到 GRPO 的演进。*
- [x] **[PPO vs DPO vs GRPO：On-Policy 与 Off-Policy 的本质差异]** `Hot`
  - *重点解析 DeepSeek-R1 使用的 GRPO (Group Relative Policy Optimization)*
- [x] **[RLHF 核心概念：Reward Hacking (奖励黑客) 与 熵坍塌 (Entropy Collapse)]**
- [x] **[Critic vs Reward Model：为什么 GRPO 不需要 Critic 网络？]**
- [x] **[KL 散度：在 RLHF 中如何防止模型“玩坏”？]**

### 🐳 第五章：前沿模型技术报告精读 (DeepSeek & Qwen)
*不读 Paper 怎么过面试？DeepSeek-V3/R1 与 Qwen 系列深度拆解。*
- [x] **[DeepSeek-V3 核心：MoE (混合专家) 架构与无辅助损失负载均衡]**
- [x] **[DeepSeek-R1 揭秘：冷启动 (Cold Start) SFT 的必要性与纯 RL 训练流程]**
- [x] **[Qwen3 vs DeepSeek-R1：思考模式 (Thinking Budget) 与通用能力的权衡]**
- [x] **[Scaling Law：大模型扩展定律与训练计算量估算]**

### 💻 第六章：工程框架与手撕代码 (Engineering & Coding)
*Talk is cheap, show me the code.*
- [x] **[训练框架对比：LLaMA-Factory (全栈) vs Deepspeed vs VerL (RL 专用)]**
- [x] **[LeetCode Hot 100：算法岗面试最最高频题目硬刷笔记]**
- [x] **[Python 手撕：Multi-Head Attention 与 RoPE 核心实现]**

---

## 🌟 为什么要做这个仓库？
现在的面经太杂，很多只是简单的问答。我希望从**原理推导**和**工程实践**两个角度，把知识点揉碎。
文档中包含了：
1.  **小白友好的白话解释**
2.  **面试官视角的追问预测**
3.  **详细耐心的反复讲解问题**。


---

## 🤝 交流与贡献
如果你觉得这些笔记对你有帮助，请点亮右上角的 ⭐️ **Star**！
如有错误，欢迎在 Issue 中指出。
