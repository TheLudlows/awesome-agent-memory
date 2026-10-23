<div align="center">

<img src="assets/cover.svg" alt="Awesome Agent Memory — A research reading room" width="100%" />

<h3>Agent 记忆研究的中文精读库</h3>
<p>从原论文的背景与方法出发，读懂记忆如何形成、如何被使用，以及何时能够改善行动。</p>
<p><sub>19 篇详细解析 · 5 条阅读路径 · 方法拆解 · 实验证据 · 独立评论</sub></p>
<p><a href="guides/comparison.md">研究对照</a> · <a href="guides/source-verification.md">术语与版本</a> · <a href="templates/paper-analysis.md">解析规范</a></p>

</div>

## 阅读这份知识库

这里的每篇文章都围绕一篇论文展开：先说明作者为什么提出问题，再逐步解释数据结构、算法与处理流程，用具体例子建立直觉，最后讨论实验真正支持的结论，并给出**总结与我的看法**。

对系统论文，重点是信息怎样写入、更新、读取和影响决策；对评测论文，重点是题目怎样构造、指标怎样定义、结果揭示了什么。复杂概念会保留必要技术细节，同时使用通俗语言说明其含义。

<table>
<tr>
<td width="33%" valign="top">

**理解方法**

从问题到机制，解释模块之间怎样配合；需要时用公式、流程图与完整案例展开。

</td>
<td width="33%" valign="top">

**审视证据**

说明实验模型、比较对象与指标，关注收益、退步和成本之间的关系。

</td>
<td width="33%" valign="top">

**形成判断**

每篇以总结和独立评论收尾，讨论值得借鉴的设计、尚未解决的问题与适用条件。

</td>
</tr>
</table>

## 五条阅读路径

根据目标选择路线。重复出现的论文链接到同一篇解析，编号按原始清单首次出现顺序保留。

| 你的目标 | 建议阅读顺序 |
| :--- | :--- |
| **建立完整的学术认识** | [TOIS 记忆机制综述](papers/01-memory-survey.md) → [CoALA](papers/02-coala.md) → [Generative Agents](papers/03-generative-agents.md) → [Reflexion](papers/04-reflexion.md) → [Voyager](papers/05-voyager.md) |
| **研究长期用户记忆** | [MemoryBank](papers/06-memorybank.md) → [LongMemEval](papers/07-longmemeval.md) → [MemoryOS](papers/08-memoryos.md) → [Mem0](papers/09-mem0.md) |
| **设计记忆基础设施** | [CoALA](papers/02-coala.md) → [MemGPT](papers/10-memgpt.md) → [HippoRAG 2](papers/11-hipporag2.md) → [A-Mem](papers/12-amem.md) → [LightMem](papers/13-lightmem.md) → [Hindsight](papers/14-hindsight.md) |
| **研究持续改进的 Agent** | [Reflexion](papers/04-reflexion.md) → [Voyager](papers/05-voyager.md) → [ReasoningBank](papers/15-reasoningbank.md) → [Memory-R1](papers/16-memory-r1.md) → [MemoryArena](papers/17-memoryarena.md) |
| **建立评测体系** | [LongMemEval](papers/07-longmemeval.md) → [LoCoMo](papers/18-locomo.md) → [MemoryAgentBench](papers/19-memoryagentbench.md) → [MemoryArena](papers/17-memoryarena.md) |

## 论文精读索引

### 01 · Foundations

建立记忆与认知架构的共同语言。

| 编号 | 论文解析 | 核心内容 | 原文 |
| :---: | :--- | :--- | :---: |
| 01 | [TOIS 记忆机制综述](papers/01-memory-survey.md) | 用“来源、形式、操作、评测”给 Agent 记忆建立分类地图 | [↗](https://dl.acm.org/doi/10.1145/3748302) |
| 02 | [CoALA](papers/02-coala.md) | 把工作记忆、经历、知识和技能放到统一的决策框架中 | [↗](https://openreview.net/forum?id=1i6ZCvflQJ) |
| 03 | [Generative Agents](papers/03-generative-agents.md) | 记录经历、总结高层认识，再用相关记忆指导计划与行为 | [↗](https://arxiv.org/abs/2304.03442) |
| 04 | [Reflexion](papers/04-reflexion.md) | 把失败反馈变成可执行的文字教训，供下一次尝试使用 | [↗](https://papers.nips.cc/paper_files/paper/2023/hash/1b44b878bb782e6954cd888628510e90-Abstract-Conference.html) |
| 05 | [Voyager](papers/05-voyager.md) | 把做成功的操作保存为代码技能，后续检索、组合并复用 | [↗](https://arxiv.org/abs/2305.16291) |

### 02 · Personal Memory

从长期对话中维护事实与用户理解。

| 编号 | 论文解析 | 核心内容 | 原文 |
| :---: | :--- | :--- | :---: |
| 06 | [MemoryBank](papers/06-memorybank.md) | 保存长期对话与用户认识，并借助遗忘和强化机制管理记忆 | [↗](https://ojs.aaai.org/index.php/AAAI/article/view/29946) |
| 08 | [MemoryOS](papers/08-memoryos.md) | 用短期、中期和长期个人记忆管理近期上下文、主题内容与稳定画像 | [↗](https://aclanthology.org/2025.emnlp-main.1318/) |
| 09 | [Mem0](papers/09-mem0.md) | 把新对话提取为候选事实，再与旧记忆比较后增删改或忽略 | [↗](https://arxiv.org/abs/2504.19413) |

### 03 · Memory Systems

组织、访问与维护不断增长的记忆。

| 编号 | 论文解析 | 核心内容 | 原文 |
| :---: | :--- | :--- | :---: |
| 10 | [MemGPT](papers/10-memgpt.md) | 让模型借助工具在有限上下文与外部存储之间调入、调出信息 | [↗](https://arxiv.org/abs/2310.08560) |
| 11 | [HippoRAG 2](papers/11-hipporag2.md) | 借助图结构和 Personalized PageRank 找到不能只靠相似度定位的关联证据 | [↗](https://proceedings.mlr.press/v267/gutierrez25a.html) |
| 12 | [A-Mem](papers/12-amem.md) | 把记忆写成互相关联的笔记，并让新信息推动旧笔记的理解更新 | [↗](https://proceedings.neurips.cc/paper_files/paper/2025/hash/19909c36f51abc4856b4560aff3d36d6-Abstract-Conference.html) |
| 13 | [LightMem](papers/13-lightmem.md) | 先压缩和按主题整理，再把昂贵的长期维护移到离线阶段 | [↗](https://proceedings.iclr.cc/paper_files/paper/2026/hash/a05b72653ec5b473732129829ae04195-Abstract-Conference.html) |
| 14 | [Hindsight](papers/14-hindsight.md) | 分清事实、经历、综合观察和观点，再用保留、回忆、反思三个操作访问 | [↗](https://aclanthology.org/2026.acl-demo.27/) |

### 04 · Learning from Experience

让过去的经验改变未来的策略。

| 编号 | 论文解析 | 核心内容 | 原文 |
| :---: | :--- | :--- | :---: |
| 15 | [ReasoningBank](papers/15-reasoningbank.md) | 从成功与失败轨迹中提炼可迁移的策略，再指导后续任务 | [↗](https://arxiv.org/abs/2509.25140) |
| 16 | [Memory-R1](papers/16-memory-r1.md) | 通过强化学习训练模型，让它更会管理记忆，也更会筛选和使用记忆 | [↗](https://aclanthology.org/2026.acl-long.583/) |

### 05 · Evaluation

分清记住、理解、更新与行动。

| 编号 | 论文解析 | 核心内容 | 原文 |
| :---: | :--- | :--- | :---: |
| 07 | [LongMemEval](papers/07-longmemeval.md) | 检查长时间交互中的事实提取、跨会话推理、更新、时间判断与拒答 | [↗](https://arxiv.org/abs/2410.10813) |
| 17 | [MemoryArena](papers/17-memoryarena.md) | 检查 Agent 能否把前面任务的经验用于后续相互依赖的任务 | [↗](https://proceedings.mlr.press/v306/he26am.html) |
| 18 | [LoCoMo](papers/18-locomo.md) | 通过长期对话检查事实回忆、跨事件理解、时间关系和回答一致性 | [↗](https://aclanthology.org/2024.acl-long.747/) |
| 19 | [MemoryAgentBench](papers/19-memoryagentbench.md) | 逐步输入信息，分别测试检索、测试时学习、长程理解和选择性遗忘 | [↗](https://proceedings.iclr.cc/paper_files/paper/2026/hash/fd1eff9dd295df50a41f2521942fa31d-Abstract-Conference.html) |

## 读完以后，应该能回答什么

- **记忆的内容**：历史、事实、反思、观点和代码技能分别承担什么角色？
- **记忆的组织**：平铺条目、分层主题、笔记网络与实体图，各自解决什么问题？
- **记忆的使用**：检索正确以后，为什么模型仍然可能读错或执行失败？
- **记忆的演进**：新事实怎样改变旧状态，经验怎样影响后续任务？
- **记忆的证据**：一个分数说明了什么，它背后的模型、预算和协议是什么？

[横向对比与术语解释 →](guides/comparison.md)

## 精读中的几个关键判断

**保存原文与提炼经验承担不同职责。** 摘要和结构可以改善访问，但有损提取也可能删掉以后需要的条件。LongMemEval、A-Mem 与 LightMem 提供了不同角度。

**更复杂的记忆不一定更好。** 图结构、反思与离线更新都有维护成本，也可能带来错误。Mem0、Reflexion 与 LightMem 的结果包含有价值的反例。

**回忆与行动需要分开验证。** 能说出规则，不等于执行中始终遵守；能找回一个事实，不等于能完成连续任务。MemoryAgentBench 与 MemoryArena 让这一差别更清楚。

以上是本库基于各篇解析形成的阅读判断，具体证据与适用条件见文章。

## 引用与版本

完整英文题名、主文链接、实际阅读版本与章节引用，均列于每篇文章。Hindsight 的演示论文与长技术稿、LoCoMo 的不同数据版本、Memory-R1 与 MemoryAgentBench 的正式版实验，均做单独说明。

实验数字属于原作者报告；教学案例用于解释机制；文章末尾的看法属于独立分析。本库没有独立复现实验，也不以不同协议下的分数制作统一排行榜。

[查看题名、来源与版本说明 →](guides/source-verification.md)

## 延续这份精读

修订应补充真实方法细节、明确实验条件，或纠正解释与引用。新增文章可使用 [解析规范](templates/paper-analysis.md)，完整覆盖背景、方法、案例、实验、总结与评论。

---

<div align="center">
<sub>Memory · Retrieval · Learning · Evaluation</sub><br />
<sub>论文版权归原作者与出版方。本库提供中文解读、原创示例与评论。</sub>
</div>
