# 项目实现与数据导航

[Agent Memory](#memory) · [RAG 项目与数据](rag-implementations-and-data.md)

<a id="memory"></a>

这份索引帮助你从论文走到代码和数据。每篇文章的“项目实现与数据”一节解释了该从哪里读、输入输出是什么，以及怎样观察方法是否真的起作用。

**核查日期：2026-10-24。** 已检查作者仓库、相关源码入口及数据说明；未安装运行全部项目，也未重新复现实验分数。下表的“公开”指找到对应资源，不代表能在当前环境下一键复现。各项目的代码、数据与模型权重应分别遵守其许可。

| 论文 | 作者项目／资源 | 数据或运行产物 | 阅读重点 |
| :--- | :--- | :--- | :--- |
| [01 TOIS 综述](../papers/01-memory-survey.md#implementation) | [综述资源](https://github.com/nuster1128/LLM_Agent_Memory_Survey) | 分类图与文献，没有独立运行时或新基准 | 将业务中的记忆问题对应到分类 |
| [02 CoALA](../papers/02-coala.md#implementation) | [作者资料集](https://github.com/ysymyth/awesome-language-agents) | 架构说明与文献索引 | 把概念对应到具体 Agent 的读写与决策 |
| [03 Generative Agents](../papers/03-generative-agents.md#implementation) | [小镇模拟](https://github.com/joonspk-research/generative_agents) | 初始角色历史、场景、模拟记录 | 从记忆变化追踪角色行为 |
| [04 Reflexion](../papers/04-reflexion.md#implementation) | [任务代码与日志](https://github.com/noahshinn/reflexion) | 问答、环境任务、编程题与历史轨迹 | 反馈怎样进入下一次尝试 |
| [05 Voyager](../papers/05-voyager.md#implementation) | [游戏 Agent](https://github.com/MineDojo/Voyager) | 技能代码、描述、向量索引和检查点 | 描述用于找技能，程序用于做事情 |
| [06 MemoryBank](../papers/06-memorybank.md#implementation) | [SiliconFriend](https://github.com/zhongwanjun/MemoryBank-SiliconFriend) | 中英文模拟历史、探测问题、LoRA 权重入口 | 分清用户记忆与模型训练材料 |
| [07 LongMemEval](../papers/07-longmemeval.md#implementation) | [评测代码](https://github.com/xiaowu0162/LongMemEval) | [cleaned 数据](https://huggingface.co/datasets/xiaowu0162/longmemeval-cleaned) | 历史、问题、答案与证据标签各有用途 |
| [08 MemoryOS](../papers/08-memoryos.md#implementation) | [分层记忆实现](https://github.com/BAI-LAB/MemoryOS) | LoCoMo 副本、逐层状态与回答结果 | 论文实验目录与应用封装配置不同 |
| [09 Mem0](../papers/09-mem0.md#implementation) | [项目](https://github.com/mem0ai/mem0) · [后续评测](https://github.com/mem0ai/memory-benchmarks) | LoCoMo、LongMemEval 等外部基准 | 2025 论文、当前 OSS 与托管平台分别看 |
| [10 MemGPT](../papers/10-memgpt.md#implementation) | [研究主页](https://research.memgpt.ai/) · [Letta 项目入口](https://github.com/letta-ai/letta) | [MSC-Self-Instruct](https://huggingface.co/datasets/MemGPT/MSC-Self-Instruct) · [qa_data](https://huggingface.co/datasets/MemGPT/qa_data) | 当前 Letta 与原始论文实现有代际差异 |
| [11 HippoRAG 2](../papers/11-hipporag2.md#implementation) | [索引与问答代码](https://github.com/OSU-NLP-Group/HippoRAG) | [语料与 QA 文件](https://huggingface.co/datasets/osunlp/HippoRAG_2)、部分抽取缓存 | 分别核对结构抽取、证据召回和回答 |
| [12 A-Mem](../papers/12-amem.md#implementation) | [实验代码](https://github.com/WujiangXu/A-mem) · [应用库](https://github.com/WujiangXu/A-mem-sys) | LoCoMo、生成笔记与记忆缓存 | 两个仓库的用途、参数与缓存来源 |
| [13 LightMem](../papers/13-lightmem.md#implementation) | [核心库与实验脚本](https://github.com/zjunlp/LightMem) | LongMemEval、LoCoMo、压缩与更新产物 | 消息选择、压缩损失、离线整理成本 |
| [14 Hindsight](../papers/14-hindsight.md#implementation) | [服务端与客户端](https://github.com/vectorize-io/hindsight) | 外部基准；当前质量评测指向 [AMB](https://github.com/vectorize-io/agent-memory-benchmark) | 写入事实、检索证据与推理回答分开观察 |
| [15 ReasoningBank](../papers/15-reasoningbank.md#implementation) | [官方实现](https://github.com/google-research/reasoning-bank) | WebArena、SWE-Bench 任务及运行生成的经验 | 环境、任务顺序、自评与策略提炼 |
| [16 Memory-R1](../papers/16-memory-r1.md#implementation) | [作者项目页](https://github.com/yansikuan/memory-r1) | 尚未看到训练代码、划分文件或 checkpoint | 仓库仍写 Code coming soon，不能声称可直接复现 |
| [17 MemoryArena](../papers/17-memoryarena.md#implementation) | [Agent／环境／记忆框架](https://github.com/ZexueHe/MemoryArena) | [依赖任务组](https://huggingface.co/datasets/ZexueHe/memoryarena)与各环境数据 | 一组任务如何连续执行、如何重置和保留状态 |
| [18 LoCoMo](../papers/18-locomo.md#implementation) | [数据与任务代码](https://github.com/snap-research/locomo) | `locomo10.json`、生成摘要与证据标注 | 生成材料与人工参考答案不能混用 |
| [19 MemoryAgentBench](../papers/19-memoryagentbench.md#implementation) | [评测框架](https://github.com/HUST-AI-HYZ/MemoryAgentBench) | [增量输入与多问题数据](https://huggingface.co/datasets/ai-hyz/MemoryAgentBench) | 数据行、问题数、切块与任务指标分别记录 |

## 怎样读懂一份记忆实验的数据

以“用户先住北京，后来搬到上海”为例，系统应先按时间接收两段历史，再回答当前住址。历史是输入，最终问题是查询，标准答案是评价依据，证据 ID 帮助定位错误。将这四类内容拼在一起写入记忆，会把答案提前透露给系统。

| 数据层次 | 典型内容 | 应检查什么 |
| :--- | :--- | :--- |
| 原始输入 | 消息、文档、行动与环境反馈 | 主体、顺序、时间和来源是否保留 |
| 派生记忆 | 摘要、事实、笔记、实体、技能 | 哪个模型和配置生成，是否遗漏或添加信息 |
| 查询与预测 | 问题、检索候选、模型回答 | 当时到底看到了什么证据 |
| 评价材料 | 标准答案、证据标记、任务奖励 | 是否隔离于正常写入和推理输入 |

最有用的第一步通常是跟踪一个样本，而不是立即跑完所有数据。保存它的原文、写入结果、检索结果和最终回答，就能看清错误在哪个阶段发生。确认流程正确后，再扩大到完整基准。

## 怎样解释“复现成功”

**代码跑通**说明依赖、接口和数据格式能够配合。**方法复现**还需要使用对应算法、数据划分和预算。**数值复现**则进一步要求模型、提示、裁判、随机性等条件足够接近。三者应分别报告。

一次可比较的运行至少要留下代码提交、数据版本、任务顺序、模型配置、检索与尝试预算，以及逐题结果。对有离线写入或巩固的系统，另记建库耗时和查询耗时；对学习型方法，另记训练数据与参数更新；对行动型方法，另记环境版本及重置方式。

[返回研究索引](../README.md) · [论文版本说明](source-verification.md)
