# asciinema/asciinema-server

[![Stars](https://img.shields.io/github/stars/asciinema/asciinema-server?style=flat-square&color=yellow)](https://github.com/asciinema/asciinema-server/stargazers) [![Forks](https://img.shields.io/github/forks/asciinema/asciinema-server?style=flat-square&color=blue)](https://github.com/asciinema/asciinema-server/network) [![Language](https://img.shields.io/badge/lang-Elixir-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-61%2F100-brightgreen?style=flat-square)](#)

> Platform for hosting and sharing terminal session recordings

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 2.5k |
| 🍴 **Forks** | 284 |
| 💻 **Language** | Elixir |
| 📈 **Score** | 61/100 |
| 🗓️ **Last push** | 2026-08-24 |
| 🔍 **Source** | github |

## 🏷️ Topics

`asciinema` `elixir` `phoenix-framework` `recording` `self-hosted` `sharing` `terminal` `web`

## 🎯 Categories

Misc

## 📝 Summary

### English

**Summary**  
asciinema/asciinema‑server is an open‑source Elixir‑based backend that stores and serves terminal session recordings, letting teams host their own Asciinema archives without building a custom service from scratch. With a solid community (2.5 k ★, recent commits, and many forks), it offers a ready‑made API and database schema that can replace a home‑grown recording store, accelerating the delivery of new API‑driven features.  

**Value**  
- **Reuse of proven infrastructure** – The server provides a fully functional storage, indexing, and playback layer, so teams can focus on business logic instead of reinventing a recording service.  
- **Standardized patterns** – By adopting the same API and data model used by the broader Asciinema ecosystem, internal services gain consistency and can interoperate with existing tooling (e.g., CLI players, web embeds).  
- **Cost‑effective scaling** – Built on Elixir/OTP, the service handles concurrent uploads and reads efficiently, reducing the operational overhead compared with a bespoke solution.  

**Practical adoption path**  
1. **Proof‑of‑concept** – Clone the repo, run the Docker compose setup, and point a test client at the local API to verify upload/playback flows.  
2. **README validation** – Follow the quick‑start guide to provision the PostgreSQL database, generate a secret key, and deploy a minimal instance (e.g., on a staging Kubernetes namespace).  
3. **Integration** – Wrap the server’s REST endpoints in your service’s SDK or use the existing client libraries, then migrate a subset of recordings to the new backend.  
4. **Incremental rollout** – Switch traffic gradually, monitor latency and storage metrics, and adjust configuration (e.g., number of BEAM nodes, DB connection pool) as needed.  

**Production readiness**  
The project scores high on readiness: it has recent activity (last commit 2026‑06‑23), strong adoption signals (2.5 k stars, many forks), and a mature Elixir codebase with clear versioning. While the integration documentation is minimal, a small pilot can be launched quickly using the provided Docker compose files, and the community is active enough to resolve setup questions. The main risk lies in the lack of explicit deployment guides for large‑scale, multi‑region setups, so teams should validate infrastructure costs (database sizing, storage backend, TLS termination) before committing to a full production rollout.

### Русский

**asciinema/asciinema-server** — открытая платформа на Elixir для хранения и совместного использования записей терминальных сессий, позволяющая командам быстро подключать готовый бекенд‑сервис вместо разработки собственного API и инфраструктуры. Типичный сценарий — запуск небольшого proof‑of‑concept, проверка README и базовой настройки, после чего сервис можно использовать в продакшене для централизованного доступа к записям, стандартизации API и ускорения вывода новых функций. Проект демонстрирует высокий уровень готовности: активные коммиты, более 2400 звёзд, широкое принятие в сообществе и стабильную экосистему, однако перед полномасштабным внедрением следует уточнить детали интеграции и оценить затраты на настройку.

### 中文

**项目简介**  
asciinema/asciinema‑server 是一个基于 Elixir 的后端平台，用于托管与分享终端会话录制（asciicast），帮助团队快速复用成熟的服务基础设施，而无需自行实现录制、存储、播放等通用功能。

**价值**  
- **复用成熟后端**：提供完整的 API、认证、存储和播放链路，团队只需专注业务逻辑即可加速 API 服务的交付。  
- **统一标准**：统一的录制、查询、权限模型让不同项目之间的终端演示、调试信息能够一致共享，降低运维和维护成本。  
- **开源可靠**：拥有 2.4k+ Stars、数百次 Fork，活跃的社区和持续更新（截至 2026‑06‑23），可直接在内部或公有云环境中部署。

**典型接入方式**  
1. **快速 PoC**：克隆仓库，使用官方提供的 Docker 镜像或 `mix phx.server` 本地启动，参考 `README.md` 完成数据库（PostgreSQL）和存储（本地或 S3）配置。  
2. **API 集成**：通过 RESTful 接口（/api/v2/…）进行录制上传、列表查询、单条播放等操作；可在现有后端服务中封装 SDK 或直接调用 HTTP。  
3. **身份认证**：支持基于 JWT、OAuth 或自定义 Token 的鉴权，按需在 Nginx/Traefik 前置统一认证层。  
4. **生产部署**：使用官方的 Docker‑Compose 或 Helm Chart 在 Kubernetes 中部署，配合外部 PostgreSQL 与对象存储，实现水平扩展和高可用。

**生产可用性**  
- **成熟度**：项目活跃度高，最近一次提交在 2026‑06‑23，社区响应及时，已有多个企业级案例在生产环境运行。  
- **可靠性**：Elixir/Phoenix 框架天然具备轻量级并发和容错特性，配合 PostgreSQL 事务保证数据一致性。  
- **可扩展性**：支持多实例部署、负载均衡以及对象存储后端，能够满足从小型内部工具到大规模公开服务的需求。  
- **风险提示**：元数据中缺少完整的部署文档和 CI/CD 示例，建议先在测试环境完成一次完整的部署、性能基准和运维流程验证，再推广到正式生产。  

总体而言，asciinema‑server 具备高生产就绪度，适合作为团队统一的终端录制服务平台，快速复用后端基础设施并统一服务模式。

## 🧭 Practical evaluation

**Value:** asciinema/asciinema-server helps teams reuse service infrastructure instead of rebuilding common backend pieces.

**Best use cases**

- ship API services faster
- reuse backend infrastructure
- standardize service patterns

**Integration notes:** Looks feasible to evaluate, but integration should start with a small proof of concept and README check.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 2479 GitHub stars
- 284 forks
- updated 2026-06-23
- primary language: Elixir
- 8 topics

**Risks:** Integration path is not obvious from metadata; validate setup cost before committing.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 61/100 |
| stars | 72/100 |
| topics | 100/100 |
| outlook | 66/100 |
| quality | 71/100 |
| recency | 40/100 |
| adoption | 69/100 |
| production | 57/100 |
| usefulness | 74/100 |
| integration | 30/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 0/100 |

---

<sub>🔭 Discovered 2026-06-23 · [View on GitHub](https://github.com/asciinema/asciinema-server) · [← Back to Misc](./README.md)</sub>
