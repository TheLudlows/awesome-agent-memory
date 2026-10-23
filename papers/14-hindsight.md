# Hindsight：支持保留、回忆与反思的结构化智能体记忆

**英文题名：** Hindsight: Structured Agent Memory that Retains, Recalls, and Reflects

**版本与时间：** 2026 ACL System Demonstrations  
**主题：** 结构化记忆与混合检索  
**原文入口：** [主文](https://aclanthology.org/2026.acl-demo.27/) · [arXiv](https://arxiv.org/abs/2512.12818)  
**核对日期：** 2026-10-23  
**阅读依据：** [正文或技术版本](https://aclanthology.org/2026.acl-demo.27.pdf)；涉及补充稿的内容单独说明。本文为首版通俗解析，不包含独立实验复现。文中的教学例子与“本文推论”不是论文原始实验。

## 一句话理解

不只记住“说过什么”，还区分“世界发生了什么、我做过什么、多个事实说明什么、我目前相信什么”。找资料和基于资料思考，也提供不同入口。[1]

## 四类逻辑记忆

| 类型 | 含义 | 教学例子 |
| --- | --- | --- |
| World | 外部世界的事实 | 某实例在某时出现连接数峰值 |
| Experience | Agent 自身经历 | 我查询过该实例的连接指标 |
| Observation | 多条事实的中性综合 | 最近几次峰值均在批处理窗口 |
| Opinion | 带置信度的主观观点 | 我倾向认为批处理并发过高 |

这是论文中的逻辑分类，不表示四套独立物理数据库；Observation 与 Opinion 都应注意其推导性质。[1–2]

## 三个操作怎么分工

**Retain** 把输入提取为带时间、实体和联系的记忆。**Recall** 检索已有证据，结合向量、关键词、图和时间等路径。**Reflect** 在记忆基础上进行综合推理；较长技术稿进一步展开观点形成与更新机制。[1–2]

直观地说：“找出上周的故障记录”侧重 recall；“综合这些故障，我们应优先改进什么”侧重 reflect。后者的结论仍需证据支持。

## 证据与版本边界

本清单以 ACL 2026 演示论文为主文。[1] 较长 arXiv 稿的题名是 **Hindsight is 20/20: Building Agent Memory that Retains, Recalls, and Reflects**，作为技术补充列出。[2]

论文使用 LongMemEval、LoCoMo 验证该体系；这些结果依赖回答模型和协议，不能直接外推为执行任务能力或独立复现实验结果。

## 对基础设施的启示（本文推论）

事实、推导与观点要分清，便于修正与解释；混合召回需要统一证据标识、融合和预算。这里的论文解析也不代表对当前产品代码逐行审计：论文描述的 PostgreSQL 实现，不应直接当成后来 Memlake 等存储设计的证明。

## 建议阅读位置

先看系统概览、四类记忆与三种操作，再查补充技术稿中的 TEMPR 检索与 CARA 观点机制。

## 来源

[1] [ACL 演示论文](https://aclanthology.org/2026.acl-demo.27/)。

[2] [补充技术稿，题名 Hindsight is 20/20，与主文区分](https://arxiv.org/html/2512.12818v1)。

[返回论文索引](../README.md) · [查看横向对比](../guides/comparison.md)
