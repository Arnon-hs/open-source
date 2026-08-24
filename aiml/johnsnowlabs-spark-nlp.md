# JohnSnowLabs/spark-nlp

[![Stars](https://img.shields.io/github/stars/JohnSnowLabs/spark-nlp?style=flat-square&color=yellow)](https://github.com/JohnSnowLabs/spark-nlp/stargazers) [![Forks](https://img.shields.io/github/forks/JohnSnowLabs/spark-nlp?style=flat-square&color=blue)](https://github.com/JohnSnowLabs/spark-nlp/network) [![Language](https://img.shields.io/badge/lang-Scala-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-54%2F100-brightgreen?style=flat-square)](#)

> State of the Art Natural Language Processing

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 4.1k |
| 🍴 **Forks** | 742 |
| 💻 **Language** | Scala |
| 📈 **Score** | 54/100 |
| 🗓️ **Last push** | 2026-08-24 |
| 🔍 **Source** | github |

## 🏷️ Topics

`bert` `entity-extraction` `language-detection` `lemmatizer` `llamacpp` `llm` `machine-translation` `named-entity-recognition` `natural-language-processing` `nlp` `onnx` `part-of-speech-tagger`

## 🎯 Categories

AI/ML

## 📝 Summary

### English

**Brief Summary (2‑3 sentences)**  
spark‑nlp (JohnSnowLabs) is a high‑performance, open‑source library that brings state‑of‑the‑art natural‑language‑processing to Apache Spark, letting you add sophisticated AI capabilities without building a model stack from scratch. With over 4 000 stars, active maintenance, and strong community adoption, it is ready for serious pilot projects and can be evaluated quickly via the provided README and example notebooks.  

**Value**  
- **Accelerated AI development** – Pre‑trained pipelines (tokenizers, embeddings, NER, sentiment, etc.) run natively on Spark, so you can prototype and scale NLP features with minimal code.  
- **Seamless integration with existing data stacks** – Because it lives in the Spark ecosystem, you can reuse your current Spark jobs, data lakes, and streaming pipelines, avoiding data movement overhead.  
- **Extensible for advanced use‑cases** – Supports custom models, TensorFlow/PyTorch embeddings, and can be combined with Retrieval‑Augmented Generation (RAG) or agent workflows for downstream AI products.  

**Practical Adoption Path**  
1. **Proof‑of‑Concept** – Clone the repo, run the “quick‑start” notebook from the README, and process a small sample of your data to verify that the Spark‑NLP pipelines work in your environment.  
2. **Pilot Integration** – Wrap the desired pipeline (e.g., NER or text classification) in a reusable Spark UDF or ML‑pipeline stage, and embed it into an existing Spark job or Databricks notebook.  
3. **Scale & Extend** – Move the pilot to larger datasets, tune hyper‑parameters, or plug in custom embeddings/models; optionally integrate with RAG/agent frameworks via the provided Spark‑ML API.  

**Production Readiness**  
- **Active maintenance** – Last commit on 2026‑06‑24, frequent releases, and a large contributor base.  
- **Ecosystem maturity** – Over 4 k stars, 742 forks, and proven use in enterprise Spark deployments; the Scala core plus Python wrappers (spark‑nlp) cover most language needs.  
- **Stability & Performance** – Designed for distributed execution, with benchmarked speedups on large Spark clusters; documented best‑practice configurations for memory and executor tuning.  

**Risks & Mitigations**  
- The integration steps are not fully described in the metadata, so a small PoC is essential to surface any environment‑specific setup costs (e.g., Spark version compatibility, JVM/Scala dependencies).  
- Validate that your cluster meets the recommended Spark/Scala versions before committing to a full rollout.  

Overall, spark‑nlp is a production‑ready OSS component that can quickly bring advanced NLP to existing Spark workloads, with a clear, incremental adoption path from proof‑of‑concept to scalable deployment.

### Русский

**JohnSnowLabs/spark‑nlp** — это открытая библиотека, предоставляющая готовые модели и пайплайны для современного NLP на базе Apache Spark, что позволяет быстро добавить AI‑функциональность в проекты без необходимости строить стек с нуля. Типичный сценарий внедрения — запуск небольшого proof‑of‑concept (по примеру README), интеграция в прототипы RAG/агентных workflow или оценка инструментов моделирования, после чего масштабирование до продакшн‑окружения. Библиотека обладает высокой готовностью к production: активная поддержка, частые обновления, более 4 тыс. звёзд на GitHub и широкое принятие в сообществе, однако перед полным развертыванием следует уточнить детали установки и оценить затраты на интеграцию.

### 中文

**项目简介（2‑3 句话）**  
JohnSnowLabs 的 **spark‑nlp** 是基于 Apache Spark 的开源自然语言处理库，提供业界领先的分词、实体识别、情感分析等模型，能够在大规模分布式环境下快速完成文本理解。它通过预训练模型和可扩展的管道 API，让开发者无需从零搭建模型堆栈，即可直接在 Spark 作业中加入 AI 能力。

**价值**  
- **快速原型**：即插即用的预训练模型让团队在几行代码内实现 NLP 功能，极大缩短研发周期。  
- **可扩展性**：基于 Spark 的分布式计算框架，天然支持大数据量处理，适用于企业级批处理和流式场景。  
- **生态兼容**：与 Spark SQL、DataFrames、MLlib 等生态无缝衔接，便于在已有数据管道中加入 RAG、智能客服或自动化 Agent 等高级功能。

**典型接入方式**  
1. **环境准备**：在已有 Spark 集群或本地 Spark 环境中加入 Maven/ivy 依赖 `com.johnsnowlabs.nlp:spark-nlp_2.12:<version>`（或使用 `spark-packages`）。  
2. **代码示例**（Scala）  
   ```scala
   import com.johnsnowlabs.nlp.pretrained.PretrainedPipeline
   val pipeline = PretrainedPipeline("explain_document_ml")
   val data = spark.createDataFrame(Seq(
     ("I love Spark NLP!", 0)
   )).toDF("text", "label")
   val result = pipeline.annotate(data.select("text"))
   result.show(false)
   ```  
   Python 用户同样可以通过 `spark-nlp` 包直接 `import sparknlp` 使用。  
3. **小规模 PoC**：先在本地单机模式跑通一个简单的文本分类或实体抽取任务，确认依赖、模型下载和 Spark 配置无误后，再迁移到集群进行规模化测试。  

**生产可用性**  
- **活跃度**：截至 2026‑06‑24，项目拥有 4 138+ Stars、742+ Forks，最近一次提交在当日，说明社区活跃且维护及时。  
- **成熟度**：已在多个行业（金融、医疗、客服）中实际部署，具备完善的文档、示例 notebook 与 CI 测试，属于 OSS 候选中 **生产级**。  
- **风险与建议**：集成路径虽不完全透明（尤其是模型下载与 Spark 配置），建议在正式投入前完成一次完整的 PoC，评估网络带宽、模型缓存及集群资源占用情况。  

综上，spark‑nlp 提供了即插即用的高质量 NLP 能力，适合在已有 Spark 基础设施上快速构建和扩展 AI 功能，具备足够的成熟度和社区支持，可直接用于生产环境。

## 🧭 Practical evaluation

**Value:** JohnSnowLabs/spark-nlp helps add AI capability without starting from a blank model stack.

**Best use cases**

- prototype AI features
- build RAG or agent workflows
- evaluate model tooling

**Integration notes:** Looks feasible to evaluate, but integration should start with a small proof of concept and README check.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 4138 GitHub stars
- 742 forks
- updated 2026-06-24
- primary language: Scala
- 20 topics

**Risks:** Integration path is not obvious from metadata; validate setup cost before committing.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 72/100 |
| stars | 77/100 |
| topics | 100/100 |
| outlook | 61/100 |
| quality | 74/100 |
| recency | 40/100 |
| adoption | 76/100 |
| production | 58/100 |
| usefulness | 42/100 |
| integration | 30/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 100/100 |

---

<sub>🔭 Discovered 2026-06-24 · [View on GitHub](https://github.com/JohnSnowLabs/spark-nlp) · [← Back to AI/ML](./README.md)</sub>
