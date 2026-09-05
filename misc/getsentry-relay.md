# getsentry/relay

[![Stars](https://img.shields.io/github/stars/getsentry/relay?style=flat-square&color=yellow)](https://github.com/getsentry/relay/stargazers) [![Forks](https://img.shields.io/github/forks/getsentry/relay?style=flat-square&color=blue)](https://github.com/getsentry/relay/network) [![Language](https://img.shields.io/badge/lang-Rust-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-51%2F100-brightgreen?style=flat-square)](#)

> Sentry event forwarding and ingestion service.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 378 |
| 🍴 **Forks** | 116 |
| 💻 **Language** | Rust |
| 📈 **Score** | 51/100 |
| 🗓️ **Last push** | 2026-09-05 |
| 🔍 **Source** | github |

## 🏷️ Topics

`tag-production`

## 🎯 Categories

Misc

## 📝 Summary

### English

**Brief Summary (2‑3 sentences)**  
`getsentry/relay` is an open‑source Rust service that forwards and ingests Sentry events, acting as a lightweight, self‑hosted proxy between your applications and the Sentry backend. With a solid community presence (≈380 ★, 116 ✂) and recent updates, it can be a practical building block for teams that need tighter control over event routing, data sanitisation, or on‑premise deployments.  

**Value**  
Relay lets you run a Sentry edge node that reduces latency, enforces custom filtering or enrichment, and isolates sensitive data before it reaches Sentry’s SaaS or self‑hosted instance. This is especially valuable for regulated industries, multi‑tenant SaaS platforms, or any workflow where you want to audit or transform events centrally without modifying every client SDK.

**Practical Adoption Path**  

1. **Evaluate Fit** – Review the README and existing issues to confirm that Relay’s feature set (event rate limiting, data scrubbing, custom processing) aligns with your use case.  
2. **Prototype** – Deploy the official Docker image (or compile from source) in a staging environment, point a test application’s DSN to the Relay endpoint, and verify that events appear in your Sentry instance.  
3. **Configure** – Use the provided `relay.toml` to set up authentication, upstream Sentry URL, and any custom processing pipelines.  
4. **Integrate** – Update your production apps to send events to the Relay endpoint instead of directly to Sentry; no SDK changes are required beyond the DSN.  
5. **Validate** – Monitor Relay logs, health checks, and Sentry dashboards to ensure no event loss or latency regressions.  

**Production Readiness**  
Relay sits at a **medium** readiness level: it’s mature enough for internal tools, prototypes, and controlled production workloads, but the integration path isn’t fully documented in the discovered metadata. Before committing to a critical production deployment, perform the following checks:  

- **Dependency hygiene** – Confirm the Rust toolchain version and any native libraries are compatible with your infrastructure.  
- **Operational monitoring** – Set up alerting on Relay’s health endpoints and log aggregation.  
- **Fail‑over strategy** – Plan for fallback to direct Sentry ingestion if Relay becomes unavailable.  
- **Security review** – Verify TLS configuration, authentication tokens, and any custom data‑scrubbing rules.  

With these steps, Relay can be safely adopted for controlled production use, while keeping the option to replace or remove it if the integration cost outweighs the benefits.

### Русский

**getsentry/relay** — это сервис на Rust для приёма, обработки и переадресации событий в Sentry. Он подходит для прототипов и внутренних систем, где требуется гибкая маршрутизация событий перед отправкой в Sentry, но перед запуском в продакшн стоит проверить совместимость с текущим пайплайном и оценить нагрузку и требования к обслуживанию. Готовность к production — средняя: проект активен, имеет 378 звёзд и регулярные обновления, однако путь интеграции неочевиден и требует ручного анализа.

### 中文

**项目简介**  
`getsentry/relay` 是 Sentry 官方提供的事件转发与接入服务，使用 Rust 编写，负责在客户端 SDK 与 Sentry 后端之间安全、可靠地传输错误、性能和审计事件。它能够在网络受限或需要额外控制的环境中充当代理层，实现事件的批量上报、加密、压缩以及自定义路由。

**价值主张**  
- **安全与合规**：在内部网络或私有云中部署 Relay，可避免直接将原始事件暴露到公网，满足数据合规和防火墙穿透的需求。  
- **可扩展的转发**：支持批量上报、流量限速和重试机制，减轻后端 Sentry 服务的压力。  
- **灵活的插件**：通过自定义过滤器和处理管道，可在事件进入 Sentry 前进行脱敏、聚合或路由到不同的组织/项目。

**典型接入方式**  
1. **Docker / Kubernetes 部署**  
   - 拉取官方镜像 `getsentry/relay:latest`，在 `docker-compose.yml` 或 K8s `Deployment` 中配置 `RELAY_ID`, `RELAY_SECRET`, `SENTRY_URL` 等环境变量。  
   - 使用 `relay config generate` 生成 `relay.yml`，其中定义项目映射、缓存路径和 TLS 证书。  
2. **二进制直接运行**  
   - 在目标机器上 `cargo install sentry-relay`（或下载预编译二进制），运行 `relay --config /path/to/relay.yml`。  
3. **与 Sentry SDK 集成**  
   - 在各语言 SDK（如 `sentry-java`, `sentry-python`）的 DSN 中使用 `http://<relay-host>:<port>/api/<project-id>/store/` 替代官方 DSN，即可把事件发送到本地 Relay，Relay 再转发到 Sentry Cloud 或自托管的 Sentry 实例。

**生产可用性评估**  
- **成熟度**：项目已有 378 ★、116 Fork，活跃维护，最近一次提交就在 2026‑05‑12，代码基于 Rust，具备良好的性能和安全特性。  
- **适用场景**：适合内部原型、企业内部监控、受限网络环境以及需要自定义事件处理的场景。  
- **上线前检查**：  
  1. 确认部署环境（Docker/K8s/裸机）满足 Rust 运行时依赖。  
  2. 验证 `relay.yml` 中的项目映射、TLS 证书和限流策略是否符合业务需求。  
  3. 在预生产环境进行一次完整的事件流测试，确认重试、压缩和过滤行为。  
- **风险**：元数据中未提供完整的集成指南，需自行阅读官方 README 与代码示例，评估运维成本（日志、监控、升级）后再投入生产。  

总体而言，`getsentry/relay` 在安全、可扩展的事件转发方面提供了明确价值，经过适当的配置与验证后，可在生产环境中稳定运行，尤其适合对数据合规和内部路由有特殊要求的组织。

## 🧭 Practical evaluation

**Value:** getsentry/relay may be useful when its README and activity match a concrete workflow.

**Best use cases**

- Not enough metadata yet.

**Integration notes:** Needs manual inspection before adoption because integration signals are sparse in the discovered metadata.

**Production readiness:** Medium: useful for prototypes or internal workflows, with dependency and maintenance checks before production.

**Quality signals**

- 378 GitHub stars
- 116 forks
- updated 2026-05-12
- primary language: Rust
- 1 topics

**Risks:** Integration path is not obvious from metadata; validate setup cost before committing.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 52/100 |
| stars | 55/100 |
| topics | 13/100 |
| outlook | 61/100 |
| quality | 61/100 |
| recency | 80/100 |
| adoption | 54/100 |
| production | 63/100 |
| usefulness | 42/100 |
| integration | 30/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 0/100 |

---

<sub>🔭 Discovered 2026-05-12 · [View on GitHub](https://github.com/getsentry/relay) · [← Back to Misc](./README.md)</sub>
