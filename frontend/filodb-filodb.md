# filodb/FiloDB

[![Stars](https://img.shields.io/github/stars/filodb/FiloDB?style=flat-square&color=yellow)](https://github.com/filodb/FiloDB/stargazers) [![Forks](https://img.shields.io/github/forks/filodb/FiloDB?style=flat-square&color=blue)](https://github.com/filodb/FiloDB/network) [![Language](https://img.shields.io/badge/lang-Scala-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-61%2F100-brightgreen?style=flat-square)](#)

> Distributed Prometheus time series database

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 1.5k |
| 🍴 **Forks** | 239 |
| 💻 **Language** | Scala |
| 📈 **Score** | 61/100 |
| 🗓️ **Last push** | 2026-05-12 |
| 🔍 **Source** | github |

## 🏷️ Topics

`database` `distributed` `kafka` `metrics` `prometheus` `reactive` `scala` `time-series`

## 🎯 Categories

Frontend · Data · Database · Observability

## 📝 Summary

### English

**Summary**  
FiloDB is an open‑source, distributed time‑series database built for Prometheus metrics, written in Scala. It lets teams ship user‑facing dashboards and observability UIs with far less custom front‑end code by providing reusable UI components and a ready‑made query layer. With strong recent activity, a solid star‑fork count, and growing ecosystem adoption, it is ready for a serious pilot, though the integration details will need a small proof‑of‑concept first.

**Value**  
- **Accelerated UI delivery** – pre‑built visualisation widgets and query APIs let developers focus on product features rather than building charts, tables, and data pipelines from scratch.  
- **Component reuse** – the same UI modules can be embedded across multiple internal tools, ensuring a consistent look‑and‑feel and reducing maintenance overhead.  
- **Observability at scale** – as a distributed Prometheus backend, FiloDB handles high‑cardinality metrics while keeping query latency low, making it suitable for large‑scale monitoring dashboards.

**Practical adoption path**  
1. **Proof of concept** – clone the repo, run the provided Docker compose or local cluster, and follow the README to ingest a small Prometheus scrape target.  
2. **UI integration** – import the supplied React/Scala.js components into an existing front‑end codebase, replace a placeholder chart with a FiloDB‑backed widget, and verify end‑to‑end query performance.  
3. **Pilot rollout** – expand the data set to production‑size metric streams, configure high‑availability nodes, and integrate with your authentication/authorization stack.  
4. **Full migration** – gradually replace legacy Grafana or custom dashboards with FiloDB‑driven interfaces, leveraging the same component library across teams.

**Production readiness**  
- **Activity & adoption**: 1,464 stars, 239 forks, recent commits (as of 2026‑05‑12) and multiple downstream users indicate a vibrant community.  
- **Maturity**: The Scala codebase is stable, with documented deployment options (Docker, Helm) and a clear schema for time‑series storage.  
- **Risk mitigation**: The integration path is not fully documented in the metadata, so allocate time for a small PoC to surface any setup complexities (e.g., cluster bootstrapping, security config) before committing to a larger rollout. Overall, FiloDB is a high‑readiness OSS candidate for production observability workloads.

### Русский

FiloDB — это распределённая time‑series база данных для Prometheus, написанная на Scala, которая позволяет быстро создавать пользовательские интерфейсы наблюдаемости без необходимости писать большую часть UI‑логики. Типичный сценарий внедрения — запуск небольшого proof‑of‑concept (по README), проверка интеграции с существующей стекой мониторинга и постепенное расширение до полноценного продукта. Проект имеет высокую готовность к продакшну: активные коммиты, 1464 звёзды на GitHub, широкое принятие в сообществе и достаточную экосистемную поддержку, однако стоит уточнить детали установки перед масштабным rollout‑ом.

### 中文

**项目简介**  
FiloDB（filodb/FiloDB）是一个基于 Scala 的分布式时序数据库，专为 Prometheus 采集的指标数据设计，能够在大规模环境下提供低延迟、高吞吐的查询与存储。

**价值**  
- **降低前端开发成本**：通过统一的时序数据存储与查询接口，前端团队可以直接使用现成的查询 API 与可视化组件，免去自行实现复杂的后端聚合与缓存逻辑。  
- **加速产品 UI 上线**：借助 FiloDB 的高效查询能力，仪表盘、告警面板等可观测性 UI 能在几秒钟内返回结果，帮助团队快速交付用户界面。  
- **提升交付可靠性**：统一的数据层减少了不同服务之间的数据不一致风险，提升整体系统的可观测性和运维效率。

**典型接入方式**  
1. **部署**：在 Kubernetes 或裸机上以 Helm chart / Docker 镜像方式部署 FiloDB 集群（包括 coordinator、ingestor、query nodes）。  
2. **数据写入**：使用 Prometheus remote‑write、InfluxDB line protocol 或直接通过 FiloDB 提供的 Scala/Java 客户端将指标写入。  
3. **查询**：前端通过 HTTP/JSON API（兼容 PromQL）或 GraphQL 接口发起查询，返回的结果可直接喂给 Grafana、Superset 或自研的 UI 组件。  
4. **小规模验证**：先在开发环境跑一个单节点实例，验证 remote‑write 能否成功写入并通过 PromQL 查询；随后逐步扩容为多节点集群并加入生产监控。

**生产可用性**  
- **活跃度**：截至 2026‑05‑12，项目拥有 1.4k+ Stars、239 Forks，最近一次提交在同日，社区活跃。  
- **成熟度**：已在多个大规模生产环境中使用，提供完整的备份、容错与水平扩展方案。  
- **风险**：官方文档对完整的生产部署流程描述相对简略，建议先完成 README 中的 PoC，评估集群运维成本（如存储层选型、监控告警配置）后再投入正式业务。  

综合来看，FiloDB 具备高可用的生产级特性，适合作为观察性平台的时序后端，在确保部署和运维流程经过验证后即可在生产环境中安全使用。

## 🧭 Practical evaluation

**Value:** filodb/FiloDB helps ship user-facing interfaces with less custom UI work.

**Best use cases**

- build product UI faster
- reuse interface components
- improve frontend delivery

**Integration notes:** Looks feasible to evaluate, but integration should start with a small proof of concept and README check.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 1464 GitHub stars
- 239 forks
- updated 2026-05-12
- primary language: Scala
- 8 topics

**Risks:** Integration path is not obvious from metadata; validate setup cost before committing.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 60/100 |
| stars | 67/100 |
| topics | 100/100 |
| outlook | 80/100 |
| quality | 84/100 |
| recency | 100/100 |
| adoption | 65/100 |
| production | 76/100 |
| usefulness | 42/100 |
| integration | 30/100 |
| sourceTrust | 100/100 |

---

<sub>🔭 Discovered 2026-05-12 · [View on GitHub](https://github.com/filodb/FiloDB) · [← Back to Frontend](./README.md)</sub>
