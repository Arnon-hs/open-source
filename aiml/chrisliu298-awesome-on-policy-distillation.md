# chrisliu298/awesome-on-policy-distillation

[![Stars](https://img.shields.io/github/stars/chrisliu298/awesome-on-policy-distillation?style=flat-square&color=yellow)](https://github.com/chrisliu298/awesome-on-policy-distillation/stargazers) [![Forks](https://img.shields.io/github/forks/chrisliu298/awesome-on-policy-distillation?style=flat-square&color=blue)](https://github.com/chrisliu298/awesome-on-policy-distillation/network) [![Language](https://img.shields.io/badge/lang-Unknown-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-62%2F100-brightgreen?style=flat-square)](#)

> A curated collection of papers, technical reports, frameworks, and tools for on-policy distillation (OPD) of large language models

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 417 |
| 🍴 **Forks** | 12 |
| 💻 **Language** | Unknown |
| 📈 **Score** | 62/100 |
| 🗓️ **Last push** | 2026-09-05 |
| 🔍 **Source** | github |

## 🏷️ Topics

`awesome` `awesome-list` `distillation` `gkd` `knowledge-distillation` `llm` `llm-distillation` `llm-training` `minillm` `on-policy-distillation` `opd` `post-training`

## 🎯 Categories

AI/ML

## 📝 Summary

### English

**Project Summary:**

The "awesome-on-policy-distillation" project is an open-source collection of resources for on-policy distillation (OPD) of large language models. It provides a curated list of papers, technical reports, frameworks, and tools to help developers add AI capabilities without starting from scratch. This project is ideal for prototyping AI features and building workflows for RAG (Retrieval-Augmented Generation) or agent models.

**Value Proposition:**

The project offers significant value to developers who want to leverage on-policy distillation for their AI projects. By providing a comprehensive collection of resources, it saves developers time and effort in researching and gathering relevant information. This enables them to focus on building and integrating AI capabilities into their projects, rather than starting from a blank slate.

**Practical Adoption Path:**

To adopt this project, developers need to manually inspect the resources and tools provided before integrating them into their workflows. This requires some effort and expertise in AI and machine learning. However, the project's curator has done the heavy lifting in gathering and categorizing the resources, making it easier for developers to find what they need. Before committing to production, developers should validate the setup costs and ensure that the integration path is clear and feasible.

**Production Readiness:**

The project is considered

### Русский

**awesome-on-policy-distillation** — это открытая подборка статей, технических отчётов, фреймворков и инструментов, посвящённых on‑policy distillation больших языковых моделей. Она позволяет быстро добавить AI‑функциональность в прототипы (например, RAG‑системы или агентные пайплайны), не начиная с нуля, однако требует ручного анализа и проверки совместимости перед внедрением, поскольку метаданные дают ограниченную информацию о процессе интеграции. Проект находится на уровне «medium» готовности: подходит для внутренних экспериментов и прототипов, но перед переходом в продакшн необходимо оценить зависимости и затраты на настройку.

### 中文

**项目简介（2‑3 句话）**  
chrisliu298/awesome-on-policy-distillation 是一个精选的资源库，收录了关于大语言模型 **On‑Policy Distillation（OPD）** 的论文、技术报告、框架和工具。它帮助开发者在已有模型基础上快速添加或迁移 AI 能力，而无需从零构建模型堆栈。

---

## 价值说明  
- **加速原型开发**：提供完整的 OPD 研究与实现材料，研发人员可以直接挑选适配的方案进行实验，显著缩短从概念到可用功能的时间。  
- **降低成本**：通过蒸馏已有大模型，获取轻量化、推理更快的模型，节省算力和部署费用。  
- **支撑 RAG / Agent 工作流**：资源库中包含多种面向检索增强生成（RAG）和智能体（Agent）场景的蒸馏方法，便于在这些业务中快速集成高质量语言能力。  

---

## 典型接入方式  
1. **资源筛选**：在 `README` 或 `topics` 中定位与业务场景最匹配的论文/实现（如针对对话蒸馏、检索蒸馏等）。  
2. **代码克隆**：将对应的开源框架（如 `torchdistill`、`distilbert` 的 OPD 分支）克隆到本地或内部代码库。  
3. **数据准备**：按照文档准备 on‑policy 训练数据（通常是模型自身生成的样本或交互日志）。  
4. **微调/蒸馏**：使用提供的训练脚本或自行改写，运行 on‑policy 蒸馏流程，生成轻量模型。  
5. **评估与集成**：利用库中列出的评估基准（BLEU、ROUGE、Recall@k 等）验证蒸馏效果，再将模型部署到现有的推理服务或 RAG/Agent 流程中。  

> **注意**：项目元数据的集成提示较少，建议在正式接入前手动审查每个子项目的依赖、许可证和维护状态。

---

## 生产可用性评估  
- **成熟度**：Medium。资源库本身更新活跃（截至 2026‑06‑27），拥有 417 ⭐、12 🍴，但各子项目的维护频率不一，需自行评估每个实现的稳定性。  
- **适用场景**：非常适合作为 **原型** 或 **内部实验平台**，快速验证 OPD 对业务的价值。对外部客户或高并发生产环境使用时，需要完成以下检查：  
  1. **依赖审计**：确认所有第三方库的安全性和兼容性。  
  2. **性能基准**：在目标硬件上跑完整的蒸馏+推理基准，确保满足 latency/throughput 要求。  
  3. **监控与回滚**：为蒸馏模型加入监控（如推理错误率、漂移检测），并准备回滚到原始大模型的方案。  
- **上线建议**：先在 **内部测试环境** 完成端到端验证，随后在 **灰度流量** 中逐步替换部分请求，观察实际业务指标后再全面推广。  

综上，chrisliu298/awesome-on-policy-distillation 为想要在现有大模型上实现轻量化、快速迭代的团队提供了宝贵的资料入口；但在生产化之前，需要对具体实现进行充分的依赖、性能和安全审查。

## 🧭 Practical evaluation

**Value:** chrisliu298/awesome-on-policy-distillation helps add AI capability without starting from a blank model stack.

**Best use cases**

- prototype AI features
- build RAG or agent workflows
- evaluate model tooling

**Integration notes:** Needs manual inspection before adoption because integration signals are sparse in the discovered metadata.

**Production readiness:** Medium: useful for prototypes or internal workflows, with dependency and maintenance checks before production.

**Quality signals**

- 417 GitHub stars
- 12 forks
- updated 2026-06-27
- 17 topics

**Risks:** Integration path is not obvious from metadata; validate setup cost before committing.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 28/100 |
| stars | 56/100 |
| topics | 100/100 |
| outlook | 75/100 |
| quality | 72/100 |
| recency | 80/100 |
| adoption | 48/100 |
| production | 66/100 |
| usefulness | 74/100 |
| integration | 30/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 100/100 |

---

<sub>🔭 Discovered 2026-06-27 · [View on GitHub](https://github.com/chrisliu298/awesome-on-policy-distillation) · [← Back to AI/ML](./README.md)</sub>
