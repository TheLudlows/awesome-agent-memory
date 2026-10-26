# RAG 项目与数据

从一条问题开始，沿着输入、候选资料、生成结果和评价记录读代码，通常比直接跑完整 benchmark 更容易理解方法。下面按论文列出入口；各篇解析说明了其中的实现细节与适用边界。

[阅读路线](rag.md) · [返回首页](../README.md) · [Agent Memory 项目与数据](implementations-and-data.md)

## 从哪里读代码

| 论文 | 官方实现或资源 | 先看哪里 | 数据与产物 |
| :--- | :--- | :--- | :--- |
| [RAG](../papers/20-rag.md) | [Transformers RAG](https://huggingface.co/docs/transformers/model_doc/rag) | Retriever 与 Sequence/Token 两种概率组合 | Wikipedia 段落与索引、NQ 等问答集、模型检查点 |
| [DPR](../papers/21-dpr.md) | [facebookresearch/DPR](https://github.com/facebookresearch/DPR) | `train_dense_encoder.py` → `generate_dense_embeddings.py` → `dense_retriever.py` | 问题、正负段落、语料 ID、预计算向量和检索结果 |
| [FiD](../papers/22-fid.md) | [facebookresearch/FiD](https://github.com/facebookresearch/FiD) | `train_reader.py`、`test_reader.py` 与多 passage 输入 | NQ、TriviaQA，问题、答案和 `ctxs` |
| [ColBERTv2](../papers/23-colbertv2.md) | [ColBERT](https://github.com/stanford-futuredata/ColBERT) | `Indexer`、`Searcher`、残差位数与候选生成 | MS MARCO、LoTTE、ColBERTv2 检查点、多向量索引 |
| [SPLADE](../papers/24-splade.md) | [naver/splade](https://github.com/naver/splade) | `train.py`、`index.py`、`retrieve.py` 与模型配置 | MS MARCO、BEIR，稀疏词项和权重 |
| [HyDE](../papers/25-hyde.md) | [texttron/hyde](https://github.com/texttron/hyde) | `hyde-demo.ipynb`、`hyde-dl19.ipynb` | 假想文档、编码向量、TREC DL 等真实检索集合 |
| [IRCoT](../papers/26-ircot.md) | [StonyBrookNLP/ircot](https://github.com/StonyBrookNLP/ircot) | 索引脚本、`base_configs`、`runner.py` | HotpotQA、2WikiMultihopQA、MuSiQue、IIRC，逐轮查询与证据 |
| [Self-RAG](../papers/27-self-rag.md) | [AkariAsai/self-rag](https://github.com/AkariAsai/self-rag) | 带反思 token 的样本、推理脚本中的概率评分 | [训练数据](https://huggingface.co/datasets/selfrag/selfrag_train_data)、7B/13B 权重与多任务评测输入 |
| [CRAG](../papers/28-crag.md) | [HuskyInSalt/CRAG](https://github.com/HuskyInSalt/CRAG) | 评价器、三条纠正路径与精炼结果 | PopQA、PubHealth、ARC、传记任务，初始资料与 Web 补充资料 |
| [RAPTOR](../papers/29-raptor.md) | [parthsarthi03/raptor](https://github.com/parthsarthi03/raptor) | `RetrievalAugmentation` 与树的构建、保存和检索 | NarrativeQA、QASPER、QuALITY，原文节点与摘要节点 |
| [GraphRAG](../papers/30-graphrag.md) | [microsoft/graphrag](https://github.com/microsoft/graphrag) | text units、entities、relationships、communities、reports | 自备文档及图、社区报告；论文实验语料另行核对 |
| [HippoRAG 2](../papers/11-hipporag2.md#implementation) | [OSU-NLP-Group/HippoRAG](https://github.com/OSU-NLP-Group/HippoRAG) | 关系抽取、检索起点、图传播、最终段落 | [HippoRAG_2 数据](https://huggingface.co/datasets/osunlp/HippoRAG_2)与抽取缓存 |
| [Lost in the Middle](../papers/31-lost-in-the-middle.md) | [nelson-liu/lost-in-the-middle](https://github.com/nelson-liu/lost-in-the-middle) | `qa_data`、`kv_retrieval_data` 与位置变化实验 | NQ 问答、干扰材料、合成键值对 |
| [BEIR](../papers/32-beir.md) | [beir-cellar/beir](https://github.com/beir-cellar/beir) | `GenericDataLoader`、检索适配与评价 | [BeIR 数据入口](https://huggingface.co/BeIR)，corpus、queries、qrels |
| [RAGAs](../papers/33-ragas.md) | [官方文档](https://docs.ragas.io/) · [项目](https://github.com/vibrantlabsai/ragas) | 具体指标的输入要求和模型裁判配置 | 原文介绍 WikiEval；业务评价需问题、上下文、回答等字段 |
| [RAGChecker](../papers/34-ragchecker.md) | [amazon-science/RAGChecker](https://github.com/amazon-science/RAGChecker) | claims 提取、支持关系与分模块指标 | [benchmark 获取说明](https://github.com/amazon-science/RAGChecker/tree/main/data/benchmark) · [人工偏好数据](https://github.com/amazon-science/RAGChecker/tree/main/data/meta_evaluation) |

以上新增资源入口核对于 2026-10-26；HippoRAG 2 沿用既有文章的核对记录。本次没有运行模型训练或数据集评测。代码、数据和模型分别发布，不代表每个项目都能只凭克隆仓库完成复现。

## 几个实际容易踩到的问题

**代码主干已经包含后续论文。** ColBERT 主干包含 PLAID，FiD 仓库包含 retriever 训练相关工作，SPLADE 也有多代模型。先确认自己在读哪个版本，再把代码对应到论文。

**评测文件不等于完整语料。** DPR、IRCoT 和 BEIR 都需要相应 corpus；RAGChecker 的数据构建还涉及 BioASQ、LoTTE、NovelQA 等原始资源及访问要求。缺少语料快照，只有问题和答案不能重建同一实验。

**动态外部来源会改变结果。** CRAG 使用 Web 搜索，历史模型接口也可能变化。保存当次获取的材料、模型版本与配置，才有机会解释后续分数变化。

**不能提前把评价答案放进检索库。** 标准答案、qrels 和支持文档标签用于评价与允许的训练环节，测试时不能把它们混入正常输入。否则结果再高，也不能证明系统具备相应检索能力。

## 一条样本值得保留哪些信息

| 阶段 | 建议记录 | 能定位的问题 |
| :--- | :--- | :--- |
| 输入 | 原始问题、允许访问的资料范围、版本过滤 | 是问题不明确，还是过滤条件错了？ |
| 检索 | 实际查询、候选 ID、分数、截断与重排结果 | 正确证据在哪一步被漏掉？ |
| 组织 | 摘要、图关系、原文引用及生成配置 | 派生材料是否丢掉条件或增加推断？ |
| 生成 | 实际上下文、回答、引用、token 与耗时 | 找到了却没用，还是受到噪声影响？ |
| 评价 | 参考答案、claims、支持判定、裁判配置 | 是系统错误，还是评分口径变化？ |

这些记录是为了帮助理解故障，不必全部展示给最终用户。数据已经准备齐全时，再扩大样本与语料规模，测量质量和性能的变化。
