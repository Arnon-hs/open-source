# hickory-dns/hickory-dns

[![Stars](https://img.shields.io/github/stars/hickory-dns/hickory-dns?style=flat-square&color=yellow)](https://github.com/hickory-dns/hickory-dns/stargazers) [![Forks](https://img.shields.io/github/forks/hickory-dns/hickory-dns?style=flat-square&color=blue)](https://github.com/hickory-dns/hickory-dns/network) [![Language](https://img.shields.io/badge/lang-Rust-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-59%2F100-brightgreen?style=flat-square)](#)

> A Rust based DNS client, server, and resolver

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 5.2k |
| 🍴 **Forks** | 583 |
| 💻 **Language** | Rust |
| 📈 **Score** | 59/100 |
| 🗓️ **Last push** | 2026-08-24 |
| 🔍 **Source** | github |

## 🏷️ Topics

`dns` `dns-client` `dns-server` `dnssec` `dynamic-dns` `hickory-dns` `rust` `rust-lang` `trust-dns`

## 🎯 Categories

Backend

## 📝 Summary

### English

**Brief Summary**  
hickory-dns is a Rust‑native DNS client, server, and resolver that lets teams reuse a battle‑tested DNS stack instead of building one from scratch. With over 5 000 stars, active maintenance, and a clean API/CLI, it’s positioned as a high‑readiness OSS component for modern backend services.

**Value**  
- **Reusable infrastructure** – Provides a fully‑featured DNS implementation (recursive resolver, authoritative server, and client) that can be embedded directly in services, eliminating the need to operate separate DNS tooling.  
- **Performance & safety** – Rust’s zero‑cost abstractions and memory safety give low latency lookups and high reliability, which is critical for latency‑sensitive APIs.  
- **Standardization** – By adopting a single, well‑documented DNS library, teams can enforce consistent service‑discovery patterns across microservices, reducing operational drift.

**Practical Adoption Path**  
1. **Prototype** – Add the `hickory-dns` crate to a sandbox service and use the provided CLI to run a local resolver or authoritative server.  
2. **Integration** – Replace existing DNS client calls (e.g., `trust-dns`, system resolver) with the `hickory-dns` API; the crate offers both async and sync interfaces that fit into Tokio‑based stacks.  
3. **Configuration as a sidecar** – Deploy the server component as a sidecar container or a dedicated pod in Kubernetes, exposing DNS over UDP/TCP on the cluster’s DNS port.  
4. **Observability** – Enable built‑in metrics (Prometheus, logs) to monitor query latency and cache hit‑rates, then roll out to staging for performance validation.  
5. **Production rollout** – Gradually shift traffic from the legacy DNS solution to the hickory‑dns sidecar using canary deployments, verifying fallback paths and security policies.

**Production Readiness**  
- **Active development** – Last commit on 2026‑05‑12, frequent releases, and a healthy fork count indicate strong maintainership.  
- **Community adoption** – >5 k stars and numerous downstream projects demonstrate real‑world usage.  
- **Maturity** – Offers both client and server roles, comprehensive test coverage, and built‑in TLS/DoH support, meeting enterprise DNS requirements.  
- **Risk considerations** – License (MIT/Apache‑2.0) is permissive, but a final security audit and confirmation of a dedicated maintainer team are recommended before mission‑critical deployment.  

Overall, hickory-dns is a production‑grade, Rust‑first DNS solution that can be adopted quickly as a library or sidecar, providing a solid foundation for reliable service discovery and API performance.

### Русский

**hickory-dns/hickory-dns** — это высокопроизводительный DNS‑клиент, сервер и резолвер, написанный на Rust, который позволяет командам быстро подключать готовую сетевую инфраструктуру вместо собственного её построения. Его типичный сценарий — ускоренная доставка API‑сервисов и стандартизация сервисных паттернов за счёт единого, проверенного решения для DNS‑резолвинга. Проект обладает высокой готовностью к продакшн: активные коммиты, более 5 тыс. звёзд на GitHub, широкая экосистема и стабильные релизы, хотя окончательная проверка лицензии и безопасности всё‑ещё требуется.

### 中文

**项目简介**  
hickory-dns 是用 Rust 编写的高性能 DNS 客户端、服务器和解析器，提供统一的 API/SDK/CLI，帮助团队复用成熟的 DNS 基础设施，避免重复实现底层网络服务。

**价值**  
- **统一复用**：一次实现即可在服务间共享 DNS 解析、递归查询和本地缓存等通用功能，降低运维成本。  
- **加速交付**：通过成熟的 Rust 实现，团队可以快速为 API 服务配备可靠的 DNS 解析层，缩短上线时间。  
- **标准化**：统一的配置和接口帮助团队在微服务架构中保持一致的网络访问模式，提升可维护性。

**典型接入方式**  
1. **作为库**：在 Rust 项目中通过 `cargo add hickory-dns` 引入，调用 `AsyncResolver`、`ServerFuture` 等 API 完成解析或提供 DNS 服务。  
2. **CLI 工具**：直接使用 `hickory-dns-cli` 进行查询、调试或启动本地 DNS 服务器，适合运维脚本和临时测试。  
3. **容器化部署**：将 `hickory-dns` 编译为二进制，放入 Docker 镜像，作为 sidecar 或独立服务运行，提供统一的 DNS 解析入口。  

**生产可用性**  
- **活跃度高**：截至 2026‑05‑12，项目仍在持续更新，拥有 5 234+ 星、583+ Fork，社区活跃。  
- **成熟生态**：支持 DNSSEC、EDNS0、异步 I/O 等现代特性，已在多个开源项目和内部系统中使用。  
- **安全与维护**：暂无重大许可证或安全风险，核心维护者活跃，适合作为正式生产环境的 OSS 组件进行试点。  

综上，hickory-dns 具备高性能、易集成和稳健的社区支撑，是在 Rust 生态中构建或替换 DNS 服务的可靠选择。

## 🧭 Practical evaluation

**Value:** hickory-dns/hickory-dns helps teams reuse service infrastructure instead of rebuilding common backend pieces.

**Best use cases**

- ship API services faster
- reuse backend infrastructure
- standardize service patterns

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 5234 GitHub stars
- 583 forks
- updated 2026-05-12
- primary language: Rust
- 9 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 69/100 |
| stars | 79/100 |
| topics | 100/100 |
| outlook | 58/100 |
| quality | 69/100 |
| recency | 20/100 |
| adoption | 76/100 |
| production | 53/100 |
| usefulness | 58/100 |
| integration | 46/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 100/100 |

---

<sub>🔭 Discovered 2026-05-12 · [View on GitHub](https://github.com/hickory-dns/hickory-dns) · [← Back to Backend](./README.md)</sub>
