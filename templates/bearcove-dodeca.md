# bearcove/dodeca

[![Stars](https://img.shields.io/github/stars/bearcove/dodeca?style=flat-square&color=yellow)](https://github.com/bearcove/dodeca/stargazers) [![Forks](https://img.shields.io/github/forks/bearcove/dodeca?style=flat-square&color=blue)](https://github.com/bearcove/dodeca/network) [![Language](https://img.shields.io/badge/lang-Rust-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-52%2F100-brightgreen?style=flat-square)](#)

> A query-system-based static site generator

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 210 |
| 🍴 **Forks** | 16 |
| 💻 **Language** | Rust |
| 📈 **Score** | 52/100 |
| 🗓️ **Last push** | 2026-08-24 |
| 🔍 **Source** | github |

## 🏷️ Topics

`rust` `server` `ssg` `template` `website`

## 🎯 Categories

Templates · Backend

## 📝 Summary

### English

**Brief Summary (2‑3 sentences)**  
Bearcove / dodeca is a Rust‑based, query‑system‑driven static site generator that lets teams describe their backend services as declarative queries and then materialise them into ready‑to‑run API scaffolds. By reusing a common infrastructure layer, it speeds up the delivery of new API services and enforces consistent service patterns across an organization.  

**Value**  
- **Infrastructure reuse:** dodeca abstracts common backend concerns (routing, data access, authentication, CI/CD hooks) into a shared query language, so teams can avoid reinventing the same plumbing for each microservice.  
- **Speed to market:** With a single command‑line or SDK call you can generate a fully‑functional service skeleton, dramatically cutting the time needed to ship a new API.  
- **Standardisation:** Because every generated service follows the same query‑driven contract, code reviews, onboarding, and operational monitoring become more uniform across the organization.  

**Practical Adoption Path**  
1. **Pilot:** Spin up a small internal prototype (e.g., a simple CRUD service) using the CLI to validate the query syntax and generated code.  
2. **Integrate:** Add dodeca as a development dependency in your monorepo; expose the query files as part of the service definition repository.  
3. **Automate:** Hook the generation step into your CI pipeline so that any change to the query automatically updates the service scaffold.  
4. **Extend:** Write custom Rust modules or plug‑ins for any domain‑specific logic that the generic generator does not cover, then contribute back to the open‑source project if useful.  

**Production Readiness**  
- **Maturity:** Medium – the project has 210 ★, recent updates (June 2026), and a modest fork count, indicating active interest but limited large‑scale validation.  
- **Fit for use:** Ideal for prototypes, internal tools, or early‑stage microservices where rapid iteration outweighs the need for battle‑tested stability.  
- **Considerations before production:**  
  * Perform a security audit of the generated code and its dependencies.  
  * Verify the licensing terms are compatible with your product.  
  * Assess the maintainers’ activity and plan for a fallback if the project becomes unmaintained.  
  * Conduct dependency‑upgrade testing to ensure long‑term maintainability.  

Overall, dodeca offers a compelling way to standardise and accelerate backend service creation, provided you run the necessary checks and adopt it incrementally before relying on it for critical production workloads.

### Русский

**bearcove/dodeca** — это генератор статических сайтов на основе системы запросов, написанный на Rust. Он позволяет командам быстро запускать API‑сервисы, переиспользуя готовую инфраструктуру бекенда и стандартизируя типовые паттерны, что ускоряет прототипирование и внутренние рабочие процессы. Проект имеет средний уровень готовности к продакшну — подходит для прототипов и внутренних сервисов, но перед запуском в продакшн требуется проверка зависимостей, лицензии и безопасности.

### 中文

**项目简介（2‑3 句）**  
`bearcove/dodeca` 是基于查询系统的静态站点生成器，使用 Rust 编写，能够通过统一的 API/SDK/CLI 将查询逻辑直接渲染为静态网页。它帮助团队复用已有的服务基础设施，避免为每个项目重新实现常见的后端功能。

**价值**  
- **复用基础设施**：把已有的查询、缓存、鉴权等后端能力直接搬到静态站点生成流程中，省去重复开发。  
- **加速 API 服务交付**：通过声明式查询即可生成文档或前端页面，显著缩短从接口设计到可视化交付的周期。  
- **统一服务模式**：提供统一的实现信号（API、SDK、CLI）和语言元数据，帮助团队在多个项目间保持一致的后端模式和最佳实践。

**典型接入方式**  
1. **CLI**：在 CI/CD 流程中调用 `dodeca build`，指定查询文件和模板，即可输出完整的静态站点。  
2. **SDK**：在 Rust（或通过 FFI 的其他语言）代码中引入 `dodeca` 包，调用 `render(query, context)` 动态生成页面，适用于需要在运行时生成文档的内部工具。  
3. **API**：部署 `dodeca` 为微服务，外部系统通过 HTTP POST 提交查询请求，返回渲染好的 HTML/JSON，适合与现有 API 网关集成。

**生产可用性**  
- **成熟度**：GitHub 210 星、16 Fork，最近一次更新在 2026‑06‑24，代码活跃度尚可。  
- **适用场景**：适合原型、内部工具或文档站点；在生产环境使用前需完成依赖安全审计、版本锁定以及维护者响应能力的评估。  
- **风险**：许可证、长期维护者活跃度和安全漏洞尚未完成最终审查，建议在关键业务前进行额外的合规和安全检查。  

总体而言，`bearcove/dodeca` 是一款能够快速搭建查询驱动静态站点的工具，适合希望在内部项目中复用已有后端设施并统一服务模式的团队。

## 🧭 Practical evaluation

**Value:** bearcove/dodeca helps teams reuse service infrastructure instead of rebuilding common backend pieces.

**Best use cases**

- ship API services faster
- reuse backend infrastructure
- standardize service patterns

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** Medium: useful for prototypes or internal workflows, with dependency and maintenance checks before production.

**Quality signals**

- 210 GitHub stars
- 16 forks
- updated 2026-06-24
- primary language: Rust
- 5 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 31/100 |
| stars | 49/100 |
| topics | 63/100 |
| outlook | 53/100 |
| quality | 54/100 |
| recency | 40/100 |
| adoption | 44/100 |
| production | 53/100 |
| usefulness | 58/100 |
| integration | 46/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 200/100 |

---

<sub>🔭 Discovered 2026-06-24 · [View on GitHub](https://github.com/bearcove/dodeca) · [← Back to Templates](./README.md)</sub>
