# 来源、题名与版本

本库收录原始五条路线去重后的 19 篇论文／工作，编号按首次出现顺序。更新日期：2026-10-23。

## 实际阅读版本

每篇详细解析都注明正文来源。正式发表页用于确定题名和主文入口，具体章节与表格按实际采用的正文版本引用。

| 编号 | 论文 | 详细解析使用的正文 | 主文入口 |
| --- | --- | --- | --- |
| 1 | [TOIS 记忆机制综述](../papers/01-memory-survey.md) | [正文](https://arxiv.org/html/2404.13501v1) | [主文](https://dl.acm.org/doi/10.1145/3748302) |
| 2 | [CoALA](../papers/02-coala.md) | [正文](https://arxiv.org/pdf/2309.02427) | [主文](https://openreview.net/forum?id=1i6ZCvflQJ) |
| 3 | [Generative Agents](../papers/03-generative-agents.md) | [正文](https://arxiv.org/html/2304.03442) | [主文](https://arxiv.org/abs/2304.03442) |
| 4 | [Reflexion](../papers/04-reflexion.md) | [正文](https://arxiv.org/html/2303.11366) | [主文](https://papers.nips.cc/paper_files/paper/2023/hash/1b44b878bb782e6954cd888628510e90-Abstract-Conference.html) |
| 5 | [Voyager](../papers/05-voyager.md) | [正文](https://arxiv.org/html/2305.16291) | [主文](https://arxiv.org/abs/2305.16291) |
| 6 | [MemoryBank](../papers/06-memorybank.md) | [正文](https://arxiv.org/pdf/2305.10250) | [主文](https://ojs.aaai.org/index.php/AAAI/article/view/29946) |
| 7 | [LongMemEval](../papers/07-longmemeval.md) | [正文](https://arxiv.org/html/2410.10813v1) | [主文](https://arxiv.org/abs/2410.10813) |
| 8 | [MemoryOS](../papers/08-memoryos.md) | [正文](https://arxiv.org/html/2506.06326v1) | [主文](https://aclanthology.org/2025.emnlp-main.1318/) |
| 9 | [Mem0](../papers/09-mem0.md) | [正文](https://arxiv.org/html/2504.19413v1) | [主文](https://arxiv.org/abs/2504.19413) |
| 10 | [MemGPT](../papers/10-memgpt.md) | [正文](https://arxiv.org/pdf/2310.08560) | [主文](https://arxiv.org/abs/2310.08560) |
| 11 | [HippoRAG 2](../papers/11-hipporag2.md) | [正文](https://arxiv.org/html/2502.14802v2) | [主文](https://proceedings.mlr.press/v267/gutierrez25a.html) |
| 12 | [A-Mem](../papers/12-amem.md) | [正文](https://arxiv.org/html/2502.12110v11) | [主文](https://proceedings.neurips.cc/paper_files/paper/2025/hash/19909c36f51abc4856b4560aff3d36d6-Abstract-Conference.html) |
| 13 | [LightMem](../papers/13-lightmem.md) | [正文](https://arxiv.org/html/2510.18866v1) | [主文](https://proceedings.iclr.cc/paper_files/paper/2026/hash/a05b72653ec5b473732129829ae04195-Abstract-Conference.html) |
| 14 | [Hindsight](../papers/14-hindsight.md) | [正文](https://aclanthology.org/2026.acl-demo.27.pdf) | [主文](https://aclanthology.org/2026.acl-demo.27/) |
| 15 | [ReasoningBank](../papers/15-reasoningbank.md) | [正文](https://arxiv.org/html/2509.25140v1) | [主文](https://arxiv.org/abs/2509.25140) |
| 16 | [Memory-R1](../papers/16-memory-r1.md) | [正文](https://aclanthology.org/2026.acl-long.583.pdf) | [主文](https://aclanthology.org/2026.acl-long.583/) |
| 17 | [MemoryArena](../papers/17-memoryarena.md) | [正文](https://arxiv.org/html/2602.16313v1) | [主文](https://proceedings.mlr.press/v306/he26am.html) |
| 18 | [LoCoMo](../papers/18-locomo.md) | [正文](https://aclanthology.org/2024.acl-long.747.pdf) | [主文](https://aclanthology.org/2024.acl-long.747/) |
| 19 | [MemoryAgentBench](../papers/19-memoryagentbench.md) | [正文](https://proceedings.iclr.cc/paper_files/paper/2026/file/fd1eff9dd295df50a41f2521942fa31d-Paper-Conference.pdf) | [主文](https://proceedings.iclr.cc/paper_files/paper/2026/hash/fd1eff9dd295df50a41f2521942fa31d-Abstract-Conference.html) |

## 逐篇需要注意的差异

### TOIS 记忆机制综述

正文为 arXiv v1；TOIS 正式题名带 Model-based，早期稿写作 Model based。ACM 页面曾直接读取返回 403，因此不声称逐项核对期刊版全部修订。

### CoALA

OpenReview 页面曾要求验证，正文使用 arXiv PDF；首页给出 TMLR 2024 与相同 OpenReview ID。

### Generative Agents

使用 arXiv 正文；TrueSkill 是行为可信度比较分数，不是问答准确率。

### Reflexion

编程 pass@1 包含内部自测与修正流程；不等同于无额外计算的一次生成。

### Voyager

技术稿中的效率主要以提示迭代衡量；技能库学习不要求微调 GPT-4。

### MemoryBank

使用可读取的 arXiv PDF；AAAI 原始入口另列。SiliconFriend 的模型训练与 MemoryBank 记忆效果分开讨论。

### LongMemEval

方法与具体结果依据 v1；S、M 与 Oracle 设置不能混排。

### MemoryOS

方法与效率表依据 arXiv v1；正式 EMNLP 版部分汇总数字变化，不混用。

### Mem0

依据 arXiv v1；基础版和图版分别评价，四种问题类别的结果不被汇总表述掩盖。

### MemGPT

正文为 arXiv PDF；虚拟上下文是外部访问与调度，不是单次窗口无限扩展。

### HippoRAG 2

依据 arXiv v2；用明确数据集 F1 对照说明收益，不混用相对百分比与百分点。

### A-Mem

依据 arXiv v11；说明笔记演进与查询 top-k，避免把全部收益归为固定的图遍历算法。

### LightMem

依据 arXiv v1；成本合看在线与离线，明确整理后问答也可能退步。

### Hindsight

主文为 ACL 2026 演示稿，长稿 Hindsight is 20/20 为补充；不作为第 20 篇，也不把 PostgreSQL 论文实现当作后来的 Memlake 设计。

### ReasoningBank

依据 arXiv v1；consolidation 在该稿中是简单加入，不虚构复杂冲突治理。

### Memory-R1

使用 ACL 2026 正式长论文，按该版比较 MemoryOS，并说明 QA 标准答案参与训练奖励。

### MemoryArena

使用指定 arXiv v1，保留正式 ICML 入口；不同环境成功判定与进度分分别说明。

### LoCoMo

使用 ACL 2024 正式稿：10 段对话，平均约 600 轮／16k token；不混用早期稿的 50 段等统计。

### MemoryAgentBench

改用 ICLR 2026 正式 PDF；第四类为 Selective Forgetting，主实验多跳结果不沿用早期稿的 6% 数字。

## 如何理解正文中的材料

**论文内容**包括背景、结构、算法、流程、实验设置与作者结论，指向对应正文与章节。

**教学示例**由本库原创，用于把机制串起来；涉及数据库、分页或运维的例子不表示原论文做过相应实验。

**总结**概括方法实际完成的事；**我的看法**给出独立判断，包括值得借鉴之处、局限和适用条件。

本次重写以详细内容为目标，补充机制、实验对照和评论；没有进行实验复现或对产品最新源码作完整审计。不把不同模型、题集、预算和评分协议下的数字组成统一排行榜。

[返回研究索引](../README.md)
