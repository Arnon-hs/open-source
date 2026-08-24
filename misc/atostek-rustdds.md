# Atostek/RustDDS

[![Stars](https://img.shields.io/github/stars/Atostek/RustDDS?style=flat-square&color=yellow)](https://github.com/Atostek/RustDDS/stargazers) [![Forks](https://img.shields.io/github/forks/Atostek/RustDDS?style=flat-square&color=blue)](https://github.com/Atostek/RustDDS/network) [![Language](https://img.shields.io/badge/lang-Rust-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-44%2F100-brightgreen?style=flat-square)](#)

> Rust implementation of Data Distribution Service

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 457 |
| 🍴 **Forks** | 83 |
| 💻 **Language** | Rust |
| 📈 **Score** | 44/100 |
| 🗓️ **Last push** | 2026-08-24 |
| 🔍 **Source** | github |

## 🏷️ Topics

_no topics_

## 🎯 Categories

Misc

## 📝 Summary

### English

**Project Summary:**
Atostek/RustDDS is an open-source project that provides a Rust implementation of the Data Distribution Service, enabling the conversion of raw data into searchable, analyzable, or automated pipelines. Its value proposition lies in streamlining analytics pipelines, processing datasets, and improving reporting workflows. However, its integration path requires manual inspection, and production readiness is medium due to potential dependency and maintenance challenges.

**Value:**
Atostek/RustDDS offers significant value by helping organizations transform raw data into actionable insights, facilitating data-driven decision-making. It enables the creation of efficient analytics pipelines, making it an attractive solution for data-intensive workflows.

**Practical Adoption Path:**
To adopt Atostek/RustDDS, developers should start by manually inspecting the integration signals to understand the project's requirements and limitations. This will help identify potential setup costs and validate the project's feasibility for their specific use case. Once the integration path is clear, developers can proceed with implementing the project, ensuring they perform dependency and maintenance checks to ensure production readiness.

**Production Readiness:**
Atostek/RustDDS has a medium production readiness score, indicating that it is suitable for prototype development, internal workflows, or proof-of-concept projects. While it has a decent GitHub presence (457

### Русский

Atostek/RustDDS — это открытая реализация протокола Data Distribution Service на Rust, позволяющая быстро построить аналитические и автоматизированные конвейеры обработки сырых данных. Проект удобно использовать для организации пайплайнов аналитики, обработки наборов данных и улучшения отчётных процессов, однако перед внедрением требуется ручная проверка и оценка стоимости интеграции из‑за скудной метаданных. Готовность к production — средняя: подходит для прототипов и внутренних сервисов, но требует дополнительного контроля зависимостей и поддержки перед запуском в продакшн.

### 中文

**项目简介**  
Atostek/RustDDS 是用 Rust 实现的 DDS（Data Distribution Service）协议栈，提供高性能、零拷贝的发布/订阅通信，适合在对实时性和安全性有严格要求的系统中使用。

**价值**  
- **实时数据分发**：基于 DDS 的 QoS 机制，能够在分布式环境中实现毫秒级甚至微秒级的数据传输。  
- **安全可靠**：Rust 的内存安全特性配合 DDS 的可靠传输、持久化和历史数据查询，帮助构建稳健的数据管道。  
- **跨语言互操作**：遵循 DDS 标准，可与其他语言（C/C++、Java、Python 等）实现的 DDS 实例无缝对接，便于在混合技术栈中统一数据流。

**典型接入方式**  
1. **在 Cargo.toml 中添加依赖**  
   ```toml
   [dependencies]
   rustdds = { git = "https://github.com/Atostek/RustDDS.git", tag = "v0.6.0" }
   ```  
2. **创建 DomainParticipant、Publisher/Subscriber**  
   ```rust
   use rustdds::dds::*;
   let domain = DomainParticipant::new(0).unwrap();
   let publisher = domain.create_publisher().unwrap();
   let subscriber = domain.create_subscriber().unwrap();

   // 定义 Topic
   let topic = domain.create_topic::<MyData>("MyTopic", None).unwrap();

   // 创建 DataWriter / DataReader
   let writer = publisher.create_datawriter(&topic, None).unwrap();
   let reader = subscriber.create_datareader(&topic, None).unwrap();
   ```
3. **配置 QoS（可选）**  
   通过 `QosPolicy` 调整可靠性、历史深度、传输优先级等，以满足具体的实时或带宽需求。  
4. **在业务代码中发布/订阅**  
   ```rust
   writer.write(&my_data, None).unwrap();   // 发布
   let samples = reader.take().unwrap();    // 拉取
   ```

**生产可用性**  
- **成熟度**：GitHub 457 ⭐、83 🍴，最近一次提交在 2026‑07‑02，活跃度尚可。  
- **适用场景**：原型、内部数据分析管线或对实时性有要求的内部服务，可直接投入使用。  
- **风险**：项目文档和集成示例相对有限，元数据中缺少完整的部署指南；在生产环境部署前需要自行验证网络拓扑、QoS 配置以及与现有 DDS 实例的兼容性。  
- **建议**：在正式上线前进行一次端到端的功能验证（包括安全、可靠性和性能基准），并制定依赖升级与维护策略。若项目需求长期稳定，考虑在内部维护一个 fork，以便及时修复潜在的安全或兼容性问题。

## 🧭 Practical evaluation

**Value:** Atostek/RustDDS helps convert raw data into searchable, analyzable, or automated pipelines.

**Best use cases**

- organize analytics pipelines
- process datasets
- improve reporting workflows

**Integration notes:** Needs manual inspection before adoption because integration signals are sparse in the discovered metadata.

**Production readiness:** Medium: useful for prototypes or internal workflows, with dependency and maintenance checks before production.

**Quality signals**

- 457 GitHub stars
- 83 forks
- updated 2026-07-02
- primary language: Rust

**Risks:** Integration path is not obvious from metadata; validate setup cost before committing.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 48/100 |
| stars | 57/100 |
| topics | 0/100 |
| outlook | 46/100 |
| quality | 49/100 |
| recency | 40/100 |
| adoption | 54/100 |
| production | 49/100 |
| usefulness | 42/100 |
| integration | 30/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 0/100 |

---

<sub>🔭 Discovered 2026-07-02 · [View on GitHub](https://github.com/Atostek/RustDDS) · [← Back to Misc](./README.md)</sub>
