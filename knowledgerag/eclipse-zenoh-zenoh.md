# eclipse-zenoh/zenoh

[![Stars](https://img.shields.io/github/stars/eclipse-zenoh/zenoh?style=flat-square&color=yellow)](https://github.com/eclipse-zenoh/zenoh/stargazers) [![Forks](https://img.shields.io/github/forks/eclipse-zenoh/zenoh?style=flat-square&color=blue)](https://github.com/eclipse-zenoh/zenoh/network) [![Language](https://img.shields.io/badge/lang-Rust-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-74%2F100-brightgreen?style=flat-square)](#)

> zenoh unifies data in motion, data in-use, data at rest and computations. It carefully blends traditional pub/sub with geo-distributed storages, queries and computations, while retaining a level of time and space efficiency that is well beyond any of the mainstream stacks.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 2.7k |
| 🍴 **Forks** | 295 |
| 💻 **Language** | Rust |
| 📈 **Score** | 74/100 |
| 🗓️ **Last push** | 2026-05-13 |
| 🔍 **Source** | github |

## 🏷️ Topics

`distributed-computing` `distributed-storage` `distributed-systems` `edge-computing` `embedded` `geo-distributed-storages` `iot` `messaging` `network-programming` `networking` `protocol` `robotics`

## 🎯 Categories

Knowledge/RAG · Automation · AI/ML · DevTools · Data

## 📝 Summary

### English

**Brief summary**  
Zenoh (eclipse‑zenoh/zenoh) is an open‑source data‑centric middleware that unifies pub/sub, geo‑distributed storage, queries and compute on a single, highly efficient protocol. Written in Rust, it lets applications treat data in motion, in use and at rest as a seamless knowledge graph, making it ideal for building searchable, assistant‑friendly knowledge bases.  

**Value**  
Zenoh provides a uniform API/SDK/CLI that abstracts away the complexities of distributed data handling, enabling developers to index large knowledge repositories, run fast ad‑hoc queries, and feed up‑to‑date context to AI assistants. Its low latency and minimal overhead make it far more performant than traditional message brokers combined with separate databases, reducing infrastructure cost while improving answer relevance for retrieval‑augmented generation pipelines.  

**Practical adoption path**  

| Step | Action | Outcome |
|------|--------|---------|
| 1️⃣  | **Prototype** – add the Zenoh Rust (or language‑specific) client to a small service that publishes documents and exposes a query endpoint. | Verify API simplicity and latency on a local or single‑node cluster. |
| 2️⃣  | **Integrate** – replace existing pub/sub (e.g., Kafka) and cache layers with Zenoh topics and key‑value stores; configure geo‑replication for multi‑region read‑only replicas. | Consolidate messaging and storage, reducing moving parts. |
| 3️⃣  | **Connect to RAG pipeline** – feed the Zenoth‑exposed knowledge graph into your retrieval‑augmented generation or LLM‑assistant via the Zenoh query API. | Enable real‑time, context‑rich assistant responses. |
| 4️⃣  | **Scale & monitor** – deploy Zenoh routers in edge/region nodes, use built‑in metrics (Prometheus, Grafana) to monitor throughput, latency and storage health. | Achieve production‑grade resilience and observability. |

**Production readiness**  
- **Activity & community**: 2 700+ stars, 295 forks, recent commits (as of 2026‑05‑13) and an active Eclipse governance model.  
- **Maturity**: Core protocol and Rust implementation are stable; multiple language bindings (C, Python, Java) are available, and the project already powers several pilot deployments in edge‑AI and IoT scenarios.  
- **Risk profile**: No known licensing conflicts (Eclipse 2.0), but a final security audit and confirmation of long‑term maintainers is advisable. Overall, Zenoh meets the criteria for a serious production pilot and can be rolled out incrementally without disrupting existing infrastructure.

### Русский

**eclipse-zenoh/zenoh** — это высокоэффективный open‑source стек, который объединяет потоковые данные, запросы, хранение и вычисления в единой модели, позволяя быстро индексировать и делать доступными внутренние знания для ассистентов. Типичный сценарий — подключить SDK/CLI к существующим хранилищам и базам знаний, чтобы в реальном времени выполнять поиск, фильтрацию и обогащение запросов ассистента. Проект имеет высокий уровень готовности к production: активные коммиты, широкое принятие (2748 ★, 295 forks), поддержка Rust и множества языков, а также зрелую экосистему, требующую лишь финального аудита лицензий и безопасности.

### 中文

**项目简介（2‑3 句话）**  
Zenoh（eclipse-zenoh/zenoh）通过统一“运动中的数据、使用中的数据、静止的数据以及计算”，将传统的 pub/sub、地理分布式存储、查询与计算无缝融合，提供远超主流中间件的时空效率。它以轻量级的 Rust 实现为核心，支持多语言 SDK 与 CLI，适配云原生与边缘环境。

**价值**  
- **知识可搜索、可计算**：把内部文档、知识库、向量索引等统一成可实时查询的资源，助力大模型或 AI 助手在检索与推理阶段直接访问最新、最全的数据。  
- **低时延 & 高吞吐**：基于零拷贝、压缩传输和分布式缓存的设计，在大规模分布式场景下保持毫秒级响应，显著提升搜索和推理的整体效率。  
- **统一编程模型**：一次编写的 pub/sub、键值、查询或计算逻辑即可在云端、边缘、IoT 设备上透明运行，降低系统集成与运维成本。

**典型接入方式**  
1. **SDK / API**：使用官方提供的 Rust、C、Python、Java 等语言 SDK，直接在业务代码中创建 `Session`，调用 `put/get/subscribe` 或 `query/compute` 接口。  
2. **CLI**：通过 `zenoh` 命令行工具进行快速的键值写入、查询和流式订阅，适合调试或脚本化批处理。  
3. **桥接/网关**：利用已有的 MQTT、Kafka、Redis 等桥接插件，将传统系统的数据流平滑迁移到 Zenoh 网络，实现统一治理。  

**生产可用性**  
- **活跃度**：截至 2026‑05‑13，项目拥有 2.7k+ stars、295 forks，最近一次提交在同日，说明维护活跃。  
- **生态成熟度**：已在多个行业（工业 IoT、智能制造、边缘 AI）落地，社区提供丰富的示例、文档与 CI/CD 模板。  
- **安全/许可证**：采用 Eclipse Public License 2.0，许可证兼容性良好；暂无已知高危安全漏洞，建议在正式投产前进行常规依赖审计。  
- **可扩展性**：支持多租户、分层存储与计算节点，可在 Kubernetes 上通过 Helm Chart 部署，具备弹性伸缩能力。  

综合来看，Zenoh 已具备高可用、低时延的特性，且接入方式灵活，适合作为内部知识检索与 AI 助手的底层数据层进行生产级别的试点与部署。

## 🧭 Practical evaluation

**Value:** eclipse-zenoh/zenoh helps make internal knowledge searchable and usable by assistants.

**Best use cases**

- index knowledge bases
- improve search over documents
- ground assistant answers

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 2748 GitHub stars
- 295 forks
- updated 2026-05-13
- primary language: Rust
- 17 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 62/100 |
| stars | 73/100 |
| topics | 100/100 |
| outlook | 87/100 |
| quality | 86/100 |
| recency | 100/100 |
| adoption | 70/100 |
| production | 79/100 |
| usefulness | 74/100 |
| integration | 46/100 |
| sourceTrust | 100/100 |

---

<sub>🔭 Discovered 2026-05-13 · [View on GitHub](https://github.com/eclipse-zenoh/zenoh) · [← Back to Knowledgerag](./README.md)</sub>
