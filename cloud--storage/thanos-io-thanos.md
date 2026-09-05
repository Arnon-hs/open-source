# thanos-io/thanos

[![Stars](https://img.shields.io/github/stars/thanos-io/thanos?style=flat-square&color=yellow)](https://github.com/thanos-io/thanos/stargazers) [![Forks](https://img.shields.io/github/forks/thanos-io/thanos?style=flat-square&color=blue)](https://github.com/thanos-io/thanos/network) [![Language](https://img.shields.io/badge/lang-Go-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-75%2F100-brightgreen?style=flat-square)](#)

> Highly available Prometheus setup with long term storage capabilities. A CNCF Incubating project.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 14.1k |
| 🍴 **Forks** | 2.3k |
| 💻 **Language** | Go |
| 📈 **Score** | 75/100 |
| 🗓️ **Last push** | 2026-09-05 |
| 🔍 **Source** | github |

## 🏷️ Topics

`cncf` `go` `google-cloud-storage` `hacktoberfest` `high-availability` `metrics` `monitoring` `observability` `prometheus` `prometheus-ha-pairs` `prometheus-setup` `s3`

## 🎯 Categories

Cloud & Storage · Observability

## 📝 Summary

### English

**Brief Summary (2‑3 sentences)**  
Thanos is an open‑source, CNCF‑incubating project that extends Prometheus with high‑availability clustering, global query across multiple Prometheus instances, and durable long‑term storage backed by object stores. Written in Go and backed by a large community (14 k+ stars, 2.3 k forks), it enables you to retain metrics for months or years while still serving them with low latency. The project is actively maintained (latest commit 2026‑07‑01) and widely adopted in production environments.  

**Value**  
Thanos turns raw Prometheus metrics into a searchable, persistent knowledge base that can be queried by AI assistants or other observability tools. By indexing metric histories in object storage, it provides a single source of truth for performance trends, capacity planning, and incident post‑mortems, making internal knowledge instantly retrievable and usable for automated diagnostics or LLM‑powered assistants.  

**Practical Adoption Path**  

| Step | Action | Goal |
|------|--------|------|
| 1️⃣  | **Proof‑of‑Concept** – Deploy a minimal Thanos sidecar with an existing Prometheus and point it at a test S3/GS bucket. Verify that metrics are being uploaded and can be queried via the Thanos Query UI. | Validate integration simplicity and storage cost. |
| 2️⃣  | **Documentation Review** – Follow the official README and “Getting Started” guide; run the provided Docker‑Compose demo to become familiar with Store, Compactor, Query, and Ruler components. | Ensure team can reproduce the setup. |
| 3️⃣  | **Pilot in Staging** – Add a Thanos Store gateway for a production‑grade bucket, enable compaction, and route a subset of services’ Prometheus instances through Thanos. Monitor latency, storage growth, and query correctness. | Test scalability and reliability under realistic load. |
| 4️⃣  | **Full‑Scale Rollout** – Deploy the full Thanos stack (Sidecar, Store, Compactor, Query, Ruler) across all clusters, configure bucket retention policies, and integrate with existing alerting/visualisation pipelines (Grafana, Alertmanager). | Achieve global, HA metric view and long‑term retention. |
| 5️⃣  | **AI/ML Integration** – Export selected metric series to a vector store or feed them directly to an LLM‑based assistant to enable “Ask‑my‑metrics” style queries. | Leverage the searchable knowledge base for automated insights. |

**Production Readiness**  
- **Activity & Community**: 14 k+ stars, 2.3 k forks, frequent commits, and multiple active maintainers indicate a healthy ecosystem.  
- **Maturity**: CNCF incubation, proven deployments at large cloud providers and enterprises, and a stable API surface.  
- **Reliability**: Built‑in HA via sidecars and query federation; long‑term storage uses object stores with strong durability guarantees.  
- **Risk Assessment**: No critical metadata or licensing concerns identified, but a final security audit (dependency scanning, SBOM) and verification of the project’s governance model are recommended before production use.  

Overall, Thanos is a high‑readiness OSS candidate for organizations that need durable, globally queryable Prometheus metrics and want to expose that data to downstream AI/ML or observability workflows. A small PoC followed by a staged rollout will mitigate integration risk and confirm that it meets your performance and compliance requirements.

### Русский

Резюме проекта thanos-io/thanos:

Проект thanos-io/thanos представляет собой высокодоступную систему мониторинга Prometheus с возможностью долгосрочного хранения данных. Он позволяет создавать индексы знаний, улучшать поиск по документам и обеспечивать основу для ответов виртуальных ассистентов. Проект уже достиг высокого уровня готовности к производственному использованию (Production Readiness: High), демонстрируя сильные признаки активности, адопции и экосистемных сигналов.

### 中文

**项目价值**  
Thanos 为 Prometheus 提供了高可用的多集群聚合层，并将监控数据持久化到对象存储，实现长期存储、跨地域查询和全局告警。它让运维团队能够在统一的视图下检索历史指标，避免因单点失效或存储容量不足导致的数据丢失，从而提升监控可靠性和业务可观测性。

**典型接入方式**  

| 步骤 | 关键操作 | 说明 |
|------|----------|------|
| 1️⃣ 环境准备 | 部署 Prometheus（每个集群） + 对象存储（S3、GCS、Azure Blob 等） | Thanos 通过 sidecar 与本地 Prometheus 通信，将指标写入对象存储。 |
| 2️⃣ 部署 Thanos Sidecar | 在每个 Prometheus 实例旁运行 `thanos sidecar`（Docker、K8s Sidecar、systemd） | 负责把本地 TSDB 同步到对象存储，并暴露 gRPC/HTTP 接口供查询层使用。 |
| 3️⃣ 部署查询层（Querier） | 在中心位置启动 `thanos query`（或 `thanos query-frontend`） | 聚合所有 Sidecar、Store、Rule、Compactor 的数据，实现跨集群全局查询。 |
| 4️⃣ 可选组件 | **Store**（直接读取对象存储）、**Compactor**（定期压缩块）、**Rule**（全局告警/录制规则） | 根据业务规模和查询性能需求选择性部署。 |
| 5️⃣ 集成 Grafana | 在 Grafana 中添加数据源 `Thanos`（Prometheus 兼容） | 即可在已有仪表盘上使用全局视图，无需改动查询语句。 |

> **快速验证**：可以先在本地或单节点 K8s 环境里跑 `docker compose` 示例（官方 repo 中提供），验证 Sidecar 与对象存储的同步、Querier 的跨集群查询是否正常，然后再扩展到生产集群。

**生产可用性**  
- **活跃度**：截至 2026‑07‑01，项目仍在积极维护，最近一次提交在当日；GitHub ★14.1k、Fork 2.3k，社区活跃。  
- **成熟度**：已进入 CNCF **Incubating** 阶段，拥有多个大厂（如 Uber、Red Hat、DigitalOcean）在生产环境的成功案例。  
- **可靠性特性**：Sidecar 自动重试、对象存储写入幂等、Querier 支持查询容错和负载均衡；Compactor 提供块压缩和数据去重，降低存储成本。  
- **安全/合规**：使用 Apache 2.0 许可证；支持 TLS、basic auth、OAuth 等安全配置；建议在生产前进行容器镜像签名和漏洞扫描。  
- **上线建议**：先在预生产环境完成 **Sidecar + Querier** 的 PoC，验证指标同步延迟、查询性能和对象存储成本；随后逐步加入 **Compactor** 与 **Rule**，并在 Grafana 中切换仪表盘数据源。  

综上所述，Thanos 具备高可用、长期存储和跨集群查询能力，接入门槛适中，且已具备生产级成熟度，适合作为 Prometheus 监控体系的长期存储与统一查询层。

## 🧭 Practical evaluation

**Value:** thanos-io/thanos helps make internal knowledge searchable and usable by assistants.

**Best use cases**

- index knowledge bases
- improve search over documents
- ground assistant answers

**Integration notes:** Looks feasible to evaluate, but integration should start with a small proof of concept and README check.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 14130 GitHub stars
- 2324 forks
- updated 2026-07-01
- primary language: Go
- 14 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 84/100 |
| stars | 88/100 |
| topics | 100/100 |
| outlook | 85/100 |
| quality | 89/100 |
| recency | 80/100 |
| adoption | 87/100 |
| production | 75/100 |
| usefulness | 74/100 |
| integration | 46/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 200/100 |

---

<sub>🔭 Discovered 2026-07-01 · [View on GitHub](https://github.com/thanos-io/thanos) · [← Back to Cloud--storage](./README.md)</sub>
