# Awesome Agent Memory

Agent 记忆论文中文解析：用通俗语言讲清问题、方法与证据，再讨论如何落实到记忆系统。

首批收录五条阅读路线涉及的 **19 篇不同论文／工作**，每篇均有独立的首版通俗解析。编号按清单首次出现顺序排列，不代表质量或权威性排名。核对日期：**2026-10-23**。

## 怎么读

先用“一句话理解”建立直觉，再读方法和教学例子，最后看实验的适用范围与工程启示。

- 论文中的设计和结果附来源编号；教学例子用于解释，不是作者实验。
- “本文推论”属于工程分析，不表述成作者已经实现或验证的能力。
- 本仓库没有独立复现实验，也不把不同模型、数据或裁判协议下的分数混排。
- 中文题名为参考译名，检索与引用使用完整英文题名。

## 五条阅读路线

| 目标 | 阅读顺序 |
| --- | --- |
| 建立完整的学术认识 | [TOIS 记忆机制综述](papers/01-memory-survey.md) → [CoALA](papers/02-coala.md) → [Generative Agents](papers/03-generative-agents.md) → [Reflexion](papers/04-reflexion.md) → [Voyager](papers/05-voyager.md) |
| 研究长期用户记忆 | [MemoryBank](papers/06-memorybank.md) → [LongMemEval](papers/07-longmemeval.md) → [MemoryOS](papers/08-memoryos.md) → [Mem0](papers/09-mem0.md) |
| 设计记忆基础设施 | [CoALA](papers/02-coala.md) → [MemGPT](papers/10-memgpt.md) → [HippoRAG 2](papers/11-hipporag2.md) → [A-Mem](papers/12-amem.md) → [LightMem](papers/13-lightmem.md) → [Hindsight](papers/14-hindsight.md) |
| 研究从经验中持续改进的 Agent | [Reflexion](papers/04-reflexion.md) → [Voyager](papers/05-voyager.md) → [ReasoningBank](papers/15-reasoningbank.md) → [Memory-R1](papers/16-memory-r1.md) → [MemoryArena](papers/17-memoryarena.md) |
| 建立评测体系 | [LongMemEval](papers/07-longmemeval.md) → [LoCoMo](papers/18-locomo.md) → [MemoryAgentBench](papers/19-memoryagentbench.md) → [MemoryArena](papers/17-memoryarena.md) |

## 论文与解析索引

| 序号 | 中文解析 | 完整英文题名与主文 | 主题 |
| --- | --- | --- | --- |
| 1 | [TOIS 记忆机制综述：基于大语言模型的智能体记忆机制综述](papers/01-memory-survey.md) | [A Survey on the Memory Mechanism of Large Language Model-based Agents](https://dl.acm.org/doi/10.1145/3748302) | 综述 |
| 2 | [CoALA：语言智能体的认知架构](papers/02-coala.md) | [Cognitive Architectures for Language Agents](https://openreview.net/forum?id=1i6ZCvflQJ) | 认知架构 |
| 3 | [Generative Agents：生成式智能体：人类行为的交互式模拟](papers/03-generative-agents.md) | [Generative Agents: Interactive Simulacra of Human Behavior](https://arxiv.org/abs/2304.03442) | 记忆与行为 |
| 4 | [Reflexion：Reflexion：通过语言反馈改进的语言智能体](papers/04-reflexion.md) | [Reflexion: Language Agents with Verbal Reinforcement Learning](https://papers.nips.cc/paper_files/paper/2023/hash/1b44b878bb782e6954cd888628510e90-Abstract-Conference.html) | 经验改进 |
| 5 | [Voyager：Voyager：基于大语言模型的开放式具身智能体](papers/05-voyager.md) | [Voyager: An Open-Ended Embodied Agent with Large Language Models](https://arxiv.org/abs/2305.16291) | 技能记忆 |
| 6 | [MemoryBank：MemoryBank：通过长期记忆增强大语言模型](papers/06-memorybank.md) | [MemoryBank: Enhancing Large Language Models with Long-Term Memory](https://ojs.aaai.org/index.php/AAAI/article/view/29946) | 用户长期记忆 |
| 7 | [LongMemEval：LongMemEval：聊天助手长期交互记忆的基准评测](papers/07-longmemeval.md) | [LongMemEval: Benchmarking Chat Assistants on Long-Term Interactive Memory](https://arxiv.org/abs/2410.10813) | 评测 |
| 8 | [MemoryOS：AI 智能体的记忆操作系统](papers/08-memoryos.md) | [Memory OS of AI Agent](https://aclanthology.org/2025.emnlp-main.1318/) | 分层记忆 |
| 9 | [Mem0：Mem0：构建具备可扩展长期记忆、面向生产环境的 AI 智能体](papers/09-mem0.md) | [Mem0: Building Production-Ready AI Agents with Scalable Long-Term Memory](https://arxiv.org/abs/2504.19413) | 事实记忆管理 |
| 10 | [MemGPT：MemGPT：迈向作为操作系统的大语言模型](papers/10-memgpt.md) | [MemGPT: Towards LLMs as Operating Systems](https://arxiv.org/abs/2310.08560) | 上下文管理 |
| 11 | [HippoRAG 2：从 RAG 到记忆：大语言模型的非参数持续学习](papers/11-hipporag2.md) | [From RAG to Memory: Non-Parametric Continual Learning for Large Language Models](https://proceedings.mlr.press/v267/gutierrez25a.html) | 关联检索 |
| 12 | [A-Mem：A-Mem：面向大语言模型智能体的自主记忆](papers/12-amem.md) | [A-Mem: Agentic Memory for LLM Agents](https://proceedings.neurips.cc/paper_files/paper/2025/hash/19909c36f51abc4856b4560aff3d36d6-Abstract-Conference.html) | 自组织记忆 |
| 13 | [LightMem：LightMem：轻量、高效的记忆增强生成](papers/13-lightmem.md) | [LightMem: Lightweight and Efficient Memory-Augmented Generation](https://proceedings.iclr.cc/paper_files/paper/2026/hash/a05b72653ec5b473732129829ae04195-Abstract-Conference.html) | 效率与离线整理 |
| 14 | [Hindsight：Hindsight：支持保留、回忆与反思的结构化智能体记忆](papers/14-hindsight.md) | [Hindsight: Structured Agent Memory that Retains, Recalls, and Reflects](https://aclanthology.org/2026.acl-demo.27/) | 结构化记忆与混合检索 |
| 15 | [ReasoningBank：ReasoningBank：通过推理记忆扩展智能体的自我进化能力](papers/15-reasoningbank.md) | [ReasoningBank: Scaling Agent Self-Evolving with Reasoning Memory](https://arxiv.org/abs/2509.25140) | 经验提炼 |
| 16 | [Memory-R1：Memory-R1：通过强化学习提升大语言模型智能体管理和利用记忆的能力](papers/16-memory-r1.md) | [Memory-R1: Enhancing Large Language Model Agents to Manage and Utilize Memories via Reinforcement Learning](https://aclanthology.org/2026.acl-long.583/) | 学习记忆策略 |
| 17 | [MemoryArena：在相互依赖的多会话智能体任务中评测智能体记忆](papers/17-memoryarena.md) | [Benchmarking Agent Memory in Interdependent Multi-Session Agentic Tasks](https://proceedings.mlr.press/v306/he26am.html) | 记忆驱动行动评测 |
| 18 | [LoCoMo：评估大语言模型智能体的超长期对话记忆](papers/18-locomo.md) | [Evaluating Very Long-Term Conversational Memory of LLM Agents](https://aclanthology.org/2024.acl-long.747/) | 长期对话评测 |
| 19 | [MemoryAgentBench：通过增量式多轮交互评估大语言模型智能体的记忆](papers/19-memoryagentbench.md) | [Evaluating Memory in LLM Agents via Incremental Multi-Turn Interactions](https://proceedings.iclr.cc/paper_files/paper/2026/hash/fd1eff9dd295df50a41f2521942fa31d-Abstract-Conference.html) | 增量记忆评测 |

## 配套材料

- [横向对比与术语解释](guides/comparison.md)：分别记什么、怎样使用，以及不同评测测什么。
- [题名与版本核对说明](guides/source-verification.md)：正式发表版、预印本和易混名称。
- [论文解析模板](templates/paper-analysis.md)：后续增加论文时保持一致结构。

## 版本说明

TOIS 综述的期刊题名带 Model-based，早期 arXiv 稿的标点略有区别。Hindsight 主文是 ACL 2026 演示论文，长技术稿另有题名；MemoryArena 的正式标题不含 “MemoryArena:” 前缀。LightMem 使用 arXiv 2510.18866 对应的 ICLR 工作。细节见核对说明。

## 后续维护

新增或修订解析时，先确定唯一论文标识与阅读版本，再核对方法、实验设置和结论。数值补充应注明指标、模型、数据版本、基线与计算预算；若进行了复现，另附代码、配置和日志。原文版权归原作者和出版方，本仓库提供原创解读及原文链接。
