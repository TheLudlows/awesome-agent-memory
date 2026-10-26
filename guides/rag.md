# RAG：从找对资料，到用好证据

RAG 系统答错，可能是没有找到资料，也可能是找到了却读错了；资料不断增加之后，还会出现跨文档关联、全局归纳和版本冲突。下面这 16 篇论文，从不同环节解释这些问题。

其中 15 篇是本次新增，HippoRAG 2 与记忆路线共用一篇解析。先读 RAG、DPR 和 FiD 理解基本结构，再按自己的任务选择方向。

[返回首页](../README.md) · [代码与数据](rag-implementations-and-data.md) · [Agent Memory 横向对比](comparison.md)

## 按目标选择

| 目标 | 阅读顺序 |
| :--- | :--- |
| **建立完整认识，先读 8 篇** | [RAG](../papers/20-rag.md) → [DPR](../papers/21-dpr.md) → [FiD](../papers/22-fid.md) → [HyDE](../papers/25-hyde.md) → [IRCoT](../papers/26-ircot.md) → [Self-RAG](../papers/27-self-rag.md) → [Lost in the Middle](../papers/31-lost-in-the-middle.md) → [RAGChecker](../papers/34-ragchecker.md) |
| **检索与索引设计** | [DPR](../papers/21-dpr.md) → [SPLADE](../papers/24-splade.md) → [ColBERTv2](../papers/23-colbertv2.md) → [BEIR](../papers/32-beir.md) |
| **长文档与企业知识库** | [RAG](../papers/20-rag.md) → [HyDE](../papers/25-hyde.md) → [RAPTOR](../papers/29-raptor.md) → [GraphRAG](../papers/30-graphrag.md) → [Lost in the Middle](../papers/31-lost-in-the-middle.md) → [RAGChecker](../papers/34-ragchecker.md) |
| **Agent 与多步检索** | [IRCoT](../papers/26-ircot.md) → [Self-RAG](../papers/27-self-rag.md) → [CRAG](../papers/28-crag.md) → [HippoRAG 2](../papers/11-hipporag2.md) |
| **评测与调优** | [BEIR](../papers/32-beir.md) → [Lost in the Middle](../papers/31-lost-in-the-middle.md) → [RAGAs](../papers/33-ragas.md) → [RAGChecker](../papers/34-ragchecker.md) |

## 基础架构

| 解析 | 完整英文题名与原文 | 中文参考译名 | 主要问题 |
| :--- | :--- | :--- | :--- |
| [20 · RAG](../papers/20-rag.md) | [Retrieval-Augmented Generation for Knowledge-Intensive NLP Tasks](https://arxiv.org/abs/2005.11401) | 面向知识密集型自然语言处理任务的检索增强生成 | 外部知识如何参与生成与训练？ |
| [21 · DPR](../papers/21-dpr.md) | [Dense Passage Retrieval for Open-Domain Question Answering](https://aclanthology.org/2020.emnlp-main.550/) | 面向开放域问答的稠密段落检索 | 如何学习问题与答案段落的匹配？ |
| [22 · FiD](../papers/22-fid.md) | [Leveraging Passage Retrieval with Generative Models for Open Domain Question Answering](https://aclanthology.org/2021.eacl-main.74/) | 利用段落检索与生成模型进行开放域问答 | 多段资料如何在解码器中融合？ |

## 检索表示与查询改写

| 解析 | 完整英文题名与原文 | 中文参考译名 | 主要问题 |
| :--- | :--- | :--- | :--- |
| [23 · ColBERTv2](../papers/23-colbertv2.md) | [ColBERTv2: Effective and Efficient Retrieval via Lightweight Late Interaction](https://aclanthology.org/2022.naacl-main.272/) | ColBERTv2：通过轻量级后期交互实现高质量、高效率检索 | 多向量怎样保留细节并降低存储成本？ |
| [24 · SPLADE](../papers/24-splade.md) | [SPLADE: Sparse Lexical and Expansion Model for First Stage Ranking](https://arxiv.org/abs/2107.05720) | SPLADE：用于第一阶段排序的稀疏词项与扩展模型 | 神经语义能力怎样进入倒排索引？ |
| [25 · HyDE](../papers/25-hyde.md) | [Precise Zero-Shot Dense Retrieval without Relevance Labels](https://aclanthology.org/2023.acl-long.99/) | 无需相关性标注的精确零样本稠密检索 | 假想文档为什么能帮助寻找真实资料？ |

## 多步检索与证据控制

| 解析 | 完整英文题名与原文 | 中文参考译名 | 主要问题 |
| :--- | :--- | :--- | :--- |
| [26 · IRCoT](../papers/26-ircot.md) | [Interleaving Retrieval with Chain-of-Thought Reasoning for Knowledge-Intensive Multi-Step Questions](https://aclanthology.org/2023.acl-long.557/) | 面向知识密集型多步问题的检索与思维链交替推理 | 新事实怎样决定下一次搜索？ |
| [27 · Self-RAG](../papers/27-self-rag.md) | [Self-RAG: Learning to Retrieve, Generate, and Critique through Self-Reflection](https://arxiv.org/abs/2310.11511) | Self-RAG：通过自我反思学习检索、生成与评价 | 如何训练模型决定检索并检查支持度？ |
| [28 · CRAG](../papers/28-crag.md) | [Corrective Retrieval Augmented Generation](https://arxiv.org/abs/2401.15884) | 纠正式检索增强生成 | 检索失败或不确定时怎样补救？ |

## 文档组织与记忆

| 解析 | 完整英文题名与原文 | 中文参考译名 | 主要问题 |
| :--- | :--- | :--- | :--- |
| [29 · RAPTOR](../papers/29-raptor.md) | [RAPTOR: Recursive Abstractive Processing for Tree-Organized Retrieval](https://arxiv.org/abs/2401.18059) | RAPTOR：用于树状组织检索的递归抽象处理 | 如何同时检索原文细节与高层摘要？ |
| [30 · GraphRAG](../papers/30-graphrag.md) | [From Local to Global: A Graph RAG Approach to Query-Focused Summarization](https://arxiv.org/abs/2404.16130) | 从局部到全局：面向查询导向总结的图 RAG 方法 | 如何覆盖整批资料并回答全局问题？ |
| [11 · HippoRAG 2](../papers/11-hipporag2.md) | [From RAG to Memory: Non-Parametric Continual Learning for Large Language Models](https://proceedings.mlr.press/v267/gutierrez25a.html) | 从 RAG 到记忆：大语言模型的非参数持续学习 | 怎样通过关联结构找回间接证据？ |

## 评测与诊断

| 解析 | 完整英文题名与原文 | 中文参考译名 | 主要问题 |
| :--- | :--- | :--- | :--- |
| [31 · Lost in the Middle](../papers/31-lost-in-the-middle.md) | [Lost in the Middle: How Language Models Use Long Contexts](https://aclanthology.org/2024.tacl-1.9/) | 迷失在中间：语言模型如何使用长上下文 | 证据已经在场，为什么仍然答错？ |
| [32 · BEIR](../papers/32-beir.md) | [BEIR: A Heterogeneous Benchmark for Zero-shot Evaluation of Information Retrieval Models](https://arxiv.org/abs/2104.08663) | BEIR：用于信息检索模型零样本评估的异构基准 | 换领域后，检索能力是否仍然成立？ |
| [33 · RAGAs](../papers/33-ragas.md) | [RAGAs: Automated Evaluation of Retrieval Augmented Generation](https://aclanthology.org/2024.eacl-demo.16/) | RAGAs：检索增强生成的自动评估 | 缺少参考答案时怎样检查回答？ |
| [34 · RAGChecker](../papers/34-ragchecker.md) | [RAGChecker: A Fine-grained Framework for Diagnosing Retrieval-Augmented Generation](https://arxiv.org/abs/2408.08067) | RAGChecker：诊断检索增强生成的细粒度框架 | 怎样把错误归因到检索和生成？ |

## 放在一起读，区别更清楚

**DPR、SPLADE 与 ColBERTv2**改变的是文本表示和匹配方式：单个稠密向量、稀疏词项、多词元向量。比较时要同时看召回、排序、索引大小和计算成本。

**HyDE 与 IRCoT**都改变查询，但前者在检索前生成假想文档，后者根据已经取得的资料继续搜索。一个主要弥合表达差异，一个处理信息依赖。

**Self-RAG 与 CRAG**都对检索过程增加判断，但 Self-RAG 把反思标记学进生成模型，CRAG 则通过评价器组织纠正路径。它们的训练与部署要求不同。

**RAPTOR、GraphRAG 与 HippoRAG 2**都利用结构。RAPTOR 建立不同抽象层次，GraphRAG 借社区摘要回答全局问题，HippoRAG 2 借关联图改善证据访问。不能只因为都画成树或图，就认为它们解决同一种问题。

**BEIR、Lost in the Middle、RAGAs 与 RAGChecker**分别观察检索泛化、上下文利用、参考自由评价以及有参考答案的细粒度诊断。它们适合组合使用，不能相互代替。

## 如果要动手验证

先保留一个能解释清楚的基线：固定资料、固定模型、保存每次检索和回答。准备一批真实问题，区分精确查找、概念解释、跨文档关联与全局总结。然后每次只改变一个主要环节。

比较新的检索模型时，先固定生成器；比较新的上下文组织方式时，尽量控制证据和 token 预算。对每个方案同时记录质量、延迟、模型调用次数和索引维护成本。这样读到的方法才能转化为可验证的改进，而不只是更复杂的流程。
