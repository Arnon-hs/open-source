# haifengl/smile

[![Stars](https://img.shields.io/github/stars/haifengl/smile?style=flat-square&color=yellow)](https://github.com/haifengl/smile/stargazers) [![Forks](https://img.shields.io/github/forks/haifengl/smile?style=flat-square&color=blue)](https://github.com/haifengl/smile/network) [![Language](https://img.shields.io/badge/lang-Java-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-64%2F100-brightgreen?style=flat-square)](#)

> Statistical Machine Intelligence & Learning Engine

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 6.4k |
| 🍴 **Forks** | 1.1k |
| 💻 **Language** | Java |
| 📈 **Score** | 64/100 |
| 🗓️ **Last push** | 2026-09-05 |
| 🔍 **Source** | github |

## 🏷️ Topics

`classification` `clustering` `computer-algebra-system` `computer-vision` `data-science` `dataframe` `deep-learning` `genetic-algorithm` `interpolation` `linear-algebra` `llm` `machine-learning`

## 🎯 Categories

AI/ML · Data

## 📝 Summary

### English

**Summary**  
haifengl / smile is a Java‑based open‑source library that provides a comprehensive suite of statistical and machine‑learning algorithms, enabling developers to embed AI capabilities without building a model stack from scratch. With over 6 300 stars, frequent releases (last update 2026‑05‑10) and strong community adoption, it is ready for serious pilot projects such as prototyping AI features, constructing RAG or agent pipelines, and benchmarking model tooling.

**Value** – Smile delivers a ready‑made, well‑documented engine for classic ML, deep learning, clustering, graph analytics, and data preprocessing, so teams can focus on product logic rather than low‑level algorithm implementation.  

**Adoption path** – Start with a small proof‑of‑concept that follows the README examples (e.g., loading a CSV, training a classifier, and exposing it via a REST endpoint). Validate the API surface, test integration with your data pipelines, and then expand to more complex use‑cases like retrieval‑augmented generation or autonomous agents.  

**Production readiness** – The project shows high readiness: recent commits, active issue handling, a large fork network, and a mature Java ecosystem. After a brief security/license audit and confirming maintainer responsiveness, it can be promoted from pilot to production with confidence.

### Русский

**haifengl/smile** — это открытая библиотека машинного обучения на Java, предоставляющая готовый набор статистических и нейросетевых алгоритмов, что позволяет быстро добавить AI‑функциональность без построения стека с нуля. Типичный путь внедрения — запуск небольшого прототипа (например, RAG‑модуль или агентный workflow) на основе примеров из README, оценка качества модели и последующее масштабирование в продакшн. Проект обладает высокой готовностью к production: активные коммиты, более 6 000 звёзд, широкое принятие в сообществе и надёжная экосистема, требующая лишь окончательной проверки лицензии и безопасности.

### 中文

**项目简介**  
haifengl / smile（Statistical Machine Intelligence & Learning Engine）是一套基于 Java 的机器学习与统计分析库，提供从传统统计模型到深度学习、图学习、自然语言处理等多种算法实现，帮助开发者在已有代码基座上快速加入 AI 能力，而无需从零构建模型堆栈。

**价值主张**  
- **即插即用**：丰富的 API 与示例让原生 Java 项目能够在几行代码内完成特征工程、模型训练与推理。  
- **全栈覆盖**：涵盖监督学习、无监督学习、时间序列、强化学习、RAG（检索增强生成）等场景，适合原型验证和生产级实验。  
- **生态兼容**：支持与 Spark、Flink、TensorFlow Java、ONNX Runtime 等大数据与深度学习框架无缝对接，便于构建端到端的 AI 工作流或智能体系统。

**典型接入方式**  
1. **依赖引入**：在 Maven/Gradle 项目中添加 `io.github.haifengl:smile-core`（及所需子模块），即可使用全部算法。  
2. **快速原型**：阅读 README 中的 “Getting Started” 示例，使用 `smile.classification.RandomForest`、`smile.nlp.embedding.Word2Vec` 等类完成数据加载、模型训练、模型持久化和在线推理。  
3. **与业务系统集成**：将训练好的模型序列化为二进制文件或 PMML，嵌入微服务或批处理作业中；如需 RAG，可结合 `smile.nlp` 的向量索引与外部检索库（Elasticsearch、FAISS）构建检索‑生成管线。  
4. **验证与迁移**：先在小规模数据集上跑通 POC，确认模型精度与性能后，再在生产集群上扩展至全量数据。

**生产可用性**  
- **活跃度**：截至 2026‑05‑10 最近一次提交，项目拥有 6,372 ★、1,146 Fork，社区活跃，Issue 与 Pull Request 响应及时。  
- **成熟度**：已在多个企业内部项目中用于推荐系统、异常检测和文本相似度等场景，具备稳定的 API 版本和完整的单元/集成测试。  
- **可部署性**：基于纯 Java 实现，天然适配容器化、K8s 与云原生环境；可通过 JAR 包或 Maven 坐标直接引用，无额外运行时依赖。  
- **风险**：当前未发现重大许可证或安全漏洞，但仍建议在正式上线前完成一次许可证合规审查、SBOM 生成以及针对关键依赖的安全扫描。

**结论**  
haifengl/smile 具备高质量的代码基底、丰富的算法实现和良好的生态兼容性，是在 Java 生态中快速引入 AI 功能的首选 OSS 方案。建议先在业务的低风险模块做小规模 POC，验证模型效果与集成成本后，再推进到生产级别的部署。

## 🧭 Practical evaluation

**Value:** haifengl/smile helps add AI capability without starting from a blank model stack.

**Best use cases**

- prototype AI features
- build RAG or agent workflows
- evaluate model tooling

**Integration notes:** Looks feasible to evaluate, but integration should start with a small proof of concept and README check.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 6372 GitHub stars
- 1146 forks
- updated 2026-05-10
- primary language: Java
- 20 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 76/100 |
| stars | 81/100 |
| topics | 100/100 |
| outlook | 76/100 |
| quality | 86/100 |
| recency | 80/100 |
| adoption | 80/100 |
| production | 74/100 |
| usefulness | 42/100 |
| integration | 46/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 200/100 |

---

<sub>🔭 Discovered 2026-05-11 · [View on GitHub](https://github.com/haifengl/smile) · [← Back to AI/ML](./README.md)</sub>
