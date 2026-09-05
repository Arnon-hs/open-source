# apache/stormcrawler

[![Stars](https://img.shields.io/github/stars/apache/stormcrawler?style=flat-square&color=yellow)](https://github.com/apache/stormcrawler/stargazers) [![Forks](https://img.shields.io/github/forks/apache/stormcrawler?style=flat-square&color=blue)](https://github.com/apache/stormcrawler/network) [![Language](https://img.shields.io/badge/lang-Java-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-56%2F100-brightgreen?style=flat-square)](#)

> A scalable, mature and versatile web crawler based on Apache Storm

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 982 |
| 🍴 **Forks** | 282 |
| 💻 **Language** | Java |
| 📈 **Score** | 56/100 |
| 🗓️ **Last push** | 2026-09-05 |
| 🔍 **Source** | github |

## 🏷️ Topics

`apache-storm` `crawler` `distributed` `java` `stormcrawler` `web-crawler`

## 🎯 Categories

Misc

## 📝 Summary

### English

**Brief Summary (2‑3 sentences)**  
Apache StormCrawler is an open‑source, Java‑based web‑crawling framework that runs on top of Apache Storm, offering a scalable and extensible solution for large‑scale data acquisition. It provides ready‑made components for fetching, parsing, and persisting web content, while allowing custom plug‑ins to handle domain‑specific logic. With a solid community (≈ 1 k stars) and active maintenance, it serves as a practical foundation for building data pipelines that need high‑throughput crawling.

**Value**  
- **Unified crawling & data pipeline** – StormCrawler bundles the whole crawl lifecycle (URL queue, fetch, parse, storage) into a single Storm topology, eliminating the need to stitch together disparate tools.  
- **Scalability out of the box** – Leveraging Storm’s distributed stream processing lets you scale horizontally from a single node to a full cluster with minimal code changes.  
- **Extensibility** – Plug‑in interfaces for fetchers, parsers, URL filters, and storage back‑ends let teams reuse existing components and add custom logic without rewriting core functionality.  
- **Reduced engineering overhead** – By handling persistence, deduplication, and fault tolerance, StormCrawler cuts the amount of custom plumbing required to move crawled data into databases or downstream analytics.

**Practical Adoption Path**  

| Phase | Activities | Success Criteria |
|-------|------------|------------------|
| **1. Exploration** | Clone the repo, run the official “basic‑crawl” example; verify that the README and Docker compose files work on a dev machine. | Crawl completes on a small seed list; logs show successful Storm topology deployment. |
| **2. Proof‑of‑Concept** | Replace the default storage (e.g., Elasticsearch) with your target DB (PostgreSQL, Cassandra, etc.) using the provided `Persistence` interface; add a simple custom parser for your content type. | Data appears in your DB; crawl throughput meets a baseline (e.g., 10 k URLs/hr). |
| **3. Integration** | Wire StormCrawler into your existing data pipeline (e.g., feed URLs from a message queue, push results to a downstream processing job). Deploy to a modest Storm cluster (2–3 workers) for load testing. | End‑to‑end flow works reliably; failure scenarios (node loss, malformed pages) are gracefully handled. |
| **4. Production Roll‑out** | Harden the topology: enable metrics, configure back‑pressure, set up monitoring (Storm UI, Prometheus). Implement CI/CD for topology packaging and automated schema migrations for the persistence layer. | Stable operation under production traffic, observability in place, and a rollback plan. |

**Production Readiness**  
- **Maturity:** Medium. The project is actively maintained (last commit 2026‑06‑29) and has a healthy contributor base, but it is primarily positioned as a framework rather than a turnkey product.  
- **Stability:** Core components (fetcher, parser, URL filters) are battle‑tested, yet integration points (custom storage, authentication schemes) may require additional testing and code.  
- **Operational Overhead:** Requires an Apache Storm cluster and a compatible persistence store; teams need expertise in both Storm and Java build tooling.  
- **Risk Mitigation:** Start with a small‑scale proof of concept to validate the integration effort, assess resource consumption, and confirm that the required extensions (e.g., custom parsers) are straightforward to implement.  

Overall, StormCrawler is well‑suited for internal prototypes, data‑science pipelines, or production crawls where the organization already runs Storm or is willing to adopt it. With proper testing and monitoring, it can be hardened for production use, but the integration path is not completely transparent from the repository metadata, so early validation is essential.

### Русский

Apache StormCrawler — это масштабируемый и гибкий веб‑краулер, построенный на Apache Storm, который позволяет быстро собирать и сохранять большие объёмы веб‑данных с минимальными усилиями по написанию собственного кода. Типичный сценарий внедрения — запуск небольшого proof‑of‑concept (по инструкциям в README) для оценки интеграции, а затем автоматизация процессов извлечения, хранения и последующего доступа к данным в прототипах или внутренних сервисах. Готовность к production — средняя: проект стабилен и активно поддерживается (982★, 282 форка), но требует проверки зависимостей и настройки инфраструктуры перед использованием в критически важных системах.

### 中文

**价值**  
StormCrawler 是基于 Apache Storm 的分布式爬虫框架，提供了成熟、可扩展且高度可定制的抓取能力。它内置了 URL 去重、调度、抓取、解析、存储等核心模块，帮助团队快速搭建大规模网页抓取系统，省去自行编写爬虫底层逻辑的工作量，从而更专注于业务层面的数据抽取与分析。

**典型接入方式**  
1. **依赖引入**：在 Maven/Gradle 项目中添加 `storm‑crawler` 依赖。  
2. **快速原型**：复制官方提供的 `crawler-example`（或 `README` 中的最小示例），修改 `spout`、`bolt` 配置以及 `crawler-conf.yaml`，即可在本地或小规模 Storm 集群上跑通一次抓取。  
3. **持久化集成**：通过内置的 `ElasticSearchBolt`、`CassandraBolt` 或自定义 `Bolt` 将抓取结果写入所需的存储系统；也可以使用 `KafkaSpout` 将 URL 队列接入 Kafka，实现与已有数据管道的无缝对接。  
4. **扩展插件**：利用 StormCrawler 的插件机制（如 `httpclient`, `protocol-httpclient`, `parse-tika` 等）按需添加协议、解析或过滤功能，保持代码的模块化与可维护性。

**生产可用性**  
- **成熟度**：项目已有 982+ ⭐、282+ 🍴，活跃维护至 2026‑06‑29，核心语言为 Java，社区提供丰富的文档与示例。  
- **可扩展性**：依托 Apache Storm 的分布式流处理模型，能够横向扩展到数百甚至上千个节点，适合大规模爬取。  
- **风险**：官方文档对部署与运维细节的说明相对简略，集成路径（尤其是与现有数据平台的对接）需要通过小规模 PoC 验证；此外，要关注 Storm 版本兼容性和依赖的第三方库（如 Elasticsearch、Cassandra）的运维成本。  
- **建议**：先在测试环境完成一次完整的抓取‑存储链路（如 Storm + Elasticsearch），评估资源消耗、错误恢复与监控能力后，再考虑在生产环境推广。总体而言，StormCrawler 适合作为内部原型或中等规模的生产爬虫系统，只要做好依赖管理和运维监控，即可投入使用。

## 🧭 Practical evaluation

**Value:** apache/stormcrawler helps teams persist, query, and move data with less custom plumbing.

**Best use cases**

- manage persistence
- speed up data access
- prototype database-backed apps

**Integration notes:** Looks feasible to evaluate, but integration should start with a small proof of concept and README check.

**Production readiness:** Medium: useful for prototypes or internal workflows, with dependency and maintenance checks before production.

**Quality signals**

- 982 GitHub stars
- 282 forks
- updated 2026-06-29
- primary language: Java
- 6 topics

**Risks:** Integration path is not obvious from metadata; validate setup cost before committing.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 61/100 |
| stars | 64/100 |
| topics | 75/100 |
| outlook | 70/100 |
| quality | 75/100 |
| recency | 80/100 |
| adoption | 63/100 |
| production | 67/100 |
| usefulness | 42/100 |
| integration | 30/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 0/100 |

---

<sub>🔭 Discovered 2026-06-29 · [View on GitHub](https://github.com/apache/stormcrawler) · [← Back to Misc](./README.md)</sub>
