# zotonic/zotonic

[![Stars](https://img.shields.io/github/stars/zotonic/zotonic?style=flat-square&color=yellow)](https://github.com/zotonic/zotonic/stargazers) [![Forks](https://img.shields.io/github/forks/zotonic/zotonic?style=flat-square&color=blue)](https://github.com/zotonic/zotonic/network) [![Language](https://img.shields.io/badge/lang-Erlang-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-53%2F100-brightgreen?style=flat-square)](#)

> Zotonic - The Erlang Web Framework & CMS

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 846 |
| 🍴 **Forks** | 207 |
| 💻 **Language** | Erlang |
| 📈 **Score** | 53/100 |
| 🗓️ **Last push** | 2026-08-24 |
| 🔍 **Source** | github |

## 🏷️ Topics

`cms` `erlang` `framework` `web` `zotonic`

## 🎯 Categories

Misc

## 📝 Summary

### English

**Brief Summary**  
Zotonic is an open‑source web framework and content‑management system built on Erlang, offering a highly concurrent, fault‑tolerant platform for building dynamic sites and APIs. With a solid community (≈846 ★, 207 forks) and active maintenance (last commit 2026‑06‑30), it is a viable option for teams already comfortable with Erlang or looking to leverage its scalability for internal tools or prototypes.

**Value**  
- **Scalability & reliability** – Erlang’s lightweight processes and “let it crash” philosophy give Zotonic native support for high‑traffic, real‑time applications without complex infrastructure.  
- **Built‑in CMS features** – Content editing, versioning, media handling, and templating are provided out of the box, reducing the need for third‑party plugins.  
- **Extensible architecture** – Modules are written in Erlang and can be hot‑reloaded, making it easy to add custom business logic while keeping the core stable.

**Practical Adoption Path**  
1. **Proof‑of‑concept** – Clone the repo, follow the README to spin up the default site in a Docker container or local Erlang node. Verify that the build pipeline (rebar3/mix) works in your environment.  
2. **Feature mapping** – Compare Zotonic’s built‑in modules (e.g., authentication, SEO, REST API) with your project requirements; implement missing pieces as custom modules.  
3. **Integration testing** – Hook Zotonic into your existing services (databases, message queues) using its Erlang APIs or HTTP endpoints, and run automated tests.  
4. **Gradual rollout** – Deploy the PoC to a staging environment, monitor performance, and iterate before moving any production traffic.

**Production Readiness**  
Zotonic is **medium‑ready**: it is mature enough for internal tools, prototypes, or low‑to‑moderate traffic production sites, but you should perform due diligence on:  

- **Dependency management** – Verify the versions of Erlang/OTP and third‑party libraries match your infrastructure.  
- **Operational expertise** – Ensure your ops team can maintain Erlang nodes, handle releases, and monitor BEAM‑specific metrics.  
- **Long‑term support** – Review the project’s release cadence and community activity to gauge future maintenance.  

With these checks in place, Zotonic can be a robust foundation for Erlang‑centric web applications.

### Русский

Резюме проекта Zotonic:

Зотоник - это open-source веб-фреймворк и система управления содержимым на основе Erlang, который может быть полезен в сценариях, когда его README и активность соответствуют конкретному рабочему процессу. Этот фреймворк наиболее подходит для прототипирования или внутренних рабочих процессов, но требует тщательного проверки зависимостей и поддержки перед использованием в производственной среде. Zotonic можно оценить на предмет целесообразности использования, но начать интеграцию следует с малым proof of concept и проверкой README.

### 中文

**项目简介（2‑3 句话）**  
Zotonic 是基于 Erlang 的全栈 Web 框架与内容管理系统（CMS），提供高并发、分布式和实时特性的开箱即用解决方案。它拥有模块化的插件体系、强大的模板语言以及内置的身份验证、搜索和 API 支持，适合构建从小型站点到大型企业门户的各种 Web 应用。

**价值**  
- **高并发与低延迟**：得益于 Erlang/OTP 的轻量级进程模型，Zotonic 能在数千甚至数万并发连接下保持稳定。  
- **分布式原生**：天然支持节点间的负载均衡和故障转移，适合云原生部署。  
- **完整 CMS 功能**：无需额外插件即可实现页面编辑、媒体管理、用户权限、工作流等常见需求。  
- **模块化可扩展**：通过自定义模块和模板可以快速实现业务特有的功能，降低二次开发成本。  

**典型接入方式**  
1. **本地快速原型**：  
   ```bash
   git clone https://github.com/zotonic/zotonic.git
   cd zotonic
   make deps   # 安装 Erlang 依赖
   make dev    # 启动开发服务器（http://localhost:8000）
   ```  
   通过 `zotonicctl` 创建站点、添加模块，即可在几分钟内看到可运行的 CMS。  

2. **容器化部署**：官方提供 Dockerfile，常见做法是基于 `erlang:26` 镜像构建，配合 `docker-compose` 将 PostgreSQL、Redis 等后端服务一起启动，适合 CI/CD 流水线。  

3. **与现有系统集成**：利用其 REST/JSON‑API 或 GraphQL 插件，可把 Zotonic 当作后台内容服务，前端使用 React/Vue 等框架消费数据；也可以通过 Erlang/Elixir 的节点互联（`-name`、`-setcookie`）实现跨语言服务调用。  

**生产可用性**  
- **成熟度**：项目已有 846+ ⭐、207+ 🍴，活跃维护至 2026‑06‑30，社区提供丰富的模块和文档。  
- **适用场景**：非常适合内部系统、原型、以及需要高并发或分布式特性的企业门户。对外公开的大流量站点亦可使用，但需做好以下检查：  
  - Erlang/OTP 版本兼容性（建议使用 OTP 26+）  
  - 依赖的数据库（PostgreSQL）和缓存（Redis）高可用配置  
  - 监控与日志（如 `observer`, `telemetry`）的集成  
- **风险**：相较于主流的 Node/Python/Django 生态，Erlang 开发人才相对稀缺，学习曲线较陡；项目的官方文档虽完整，但部分高级功能（如自定义分布式路由）需要深入源码。  

**结论**：Zotonic 在需要高并发、实时推送或分布式部署的 Web 项目中提供了强大的即插即用能力，适合作为内部原型或中等规模生产系统的技术选型。若团队已有 Erlang 背景或愿意投入学习成本，先通过小型 PoC 验证其部署和扩展流程，再决定是否在关键业务中全面采用。

## 🧭 Practical evaluation

**Value:** zotonic/zotonic may be useful when its README and activity match a concrete workflow.

**Best use cases**

- Not enough metadata yet.

**Integration notes:** Looks feasible to evaluate, but integration should start with a small proof of concept and README check.

**Production readiness:** Medium: useful for prototypes or internal workflows, with dependency and maintenance checks before production.

**Quality signals**

- 846 GitHub stars
- 207 forks
- updated 2026-06-30
- primary language: Erlang
- 5 topics

**Risks:** Integration path is not obvious from metadata; validate setup cost before committing.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 58/100 |
| stars | 62/100 |
| topics | 63/100 |
| outlook | 57/100 |
| quality | 62/100 |
| recency | 40/100 |
| adoption | 61/100 |
| production | 53/100 |
| usefulness | 58/100 |
| integration | 30/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 0/100 |

---

<sub>🔭 Discovered 2026-06-30 · [View on GitHub](https://github.com/zotonic/zotonic) · [← Back to Misc](./README.md)</sub>
