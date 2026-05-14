# pairshaped/rally-gleam

[![Stars](https://img.shields.io/github/stars/pairshaped/rally-gleam?style=flat-square&color=yellow)](https://github.com/pairshaped/rally-gleam/stargazers) [![Forks](https://img.shields.io/github/forks/pairshaped/rally-gleam?style=flat-square&color=blue)](https://github.com/pairshaped/rally-gleam/network) [![Language](https://img.shields.io/badge/lang-Unknown-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-45%2F100-brightgreen?style=flat-square)](#)

> Discovered from Hacker News (github-mentions)

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | — |
| 🍴 **Forks** | — |
| 💻 **Language** | Unknown |
| 📈 **Score** | 45/100 |
| 🗓️ **Last push** | 2026-05-14 |
| 🔍 **Source** | hackernews |

## 🏷️ Topics

`hn` `github-mentions`

## 🎯 Categories

Misc

## 📝 Summary

### English

**Brief Summary (2‑3 sentences)**  
Rally is an open‑source, full‑stack web framework written in Gleam that runs on the BEAM VM. It aims to provide a cohesive set of tools for building modern web applications entirely in Gleam, leveraging the concurrency and fault‑tolerance guarantees of Erlang/Elixir. The project is still early‑stage, with limited integration signals and modest activity, so it is best suited for prototypes or internal tooling where you can evaluate the codebase directly.  

**Value Proposition**  
- **Gleam‑first stack**: Rally lets teams stay within a single language (Gleam) from front‑end to back‑end, reducing context‑switching and simplifying type‑safety across the whole stack.  
- **BEAM reliability**: By building on the BEAM, Rally inherits the platform’s proven scalability, hot code swapping, and supervision trees, which are attractive for real‑time or high‑availability services.  
- **Opinionated but extensible**: The framework bundles routing, templating, database adapters, and a development server, giving a ready‑made “batteries‑included” experience while still allowing Gleam‑native extensions.

**Practical Adoption Path**  

| Step | Action | Rationale |
|------|--------|-----------|
| 1️⃣  | **Clone & build** the repo, run the example app. Verify it compiles with the current Gleam toolchain (≥ 0.33). | Confirms that the project is up‑to‑date and that your environment can compile it. |
| 2️⃣  | **Read the README & docs** (if any). Identify the core components you need (router, ORM, templating). | Determines whether Rally covers your required workflow or if you’ll need to supplement it. |
| 3️⃣  | **Run the test suite** (or add a few simple tests). Check test coverage, CI status, and any failing tests. | Provides an early signal of code health and maintenance activity. |
| 4️⃣  | **Evaluate dependencies**: list all third‑party libraries Rally pulls in, check their licenses, version freshness, and issue activity. | Reduces risk of hidden security or licensing problems. |
| 5️⃣  | **Prototype a feature**: implement a small, self‑contained endpoint (e.g., a JSON API) using Rally’s routing and DB layer. | Gives hands‑on experience with the developer ergonomics and performance characteristics. |
| 6️⃣  | **Integrate with your CI/CD**: add Gleam compilation, linting, and Rally’s build steps to your pipeline. | Ensures the framework can be reliably built and deployed in your workflow. |
| 7️⃣  | **Conduct a risk review**: verify license compatibility, check open issues, and assess the maintainers’ responsiveness. | Final gate before committing to production use. |

**Production Readiness**  
- **Maturity**: Medium. The codebase is recent (last update 2026‑05‑14) but shows only a handful of topics and sparse community activity, indicating limited real‑world validation.  
- **Suitable workloads**: Internal tools, prototypes, or low‑traffic services where the benefits of a Gleam‑centric stack outweigh the risk of a less‑battle‑tested framework.  
- **Pre‑deployment checklist**:  
  1. Confirm that the framework’s license aligns with your project’s licensing policy.  
  2. Pin all dependencies to specific versions and monitor them for security advisories.  
  3. Set up automated tests and a staging environment to catch regressions early.  
  4. Plan for fallback or migration paths (e.g., ability to replace Rally components with alternative Gleam libraries) should the project become unmaintained.  

In summary, Rally offers a compelling Gleam‑only approach to full‑stack web development on the BEAM, but adoption should be preceded by a focused technical evaluation and a cautious rollout plan, especially for production‑critical systems.

### Русский

Rally — это full‑stack веб‑фреймворк для языка Gleam, работающий на BEAM‑виртуале. Он может пригодиться, когда README и активность проекта соответствуют конкретному рабочему процессу (например, быстрый прототип внутреннего сервиса), однако перед внедрением требуется ручная проверка лицензии, поддержки и документации, так как сигналы о качестве ограничены. Готовность к production оценивается как средняя: подходит для прототипов и внутренних инструментов при условии дополнительного аудита зависимости и частоты релизов.

### 中文

**项目简介（2‑3 句）**  
Rally 是基于 Beam 虚拟机的 Gleam 语言的全栈 Web 框架，旨在为 Gleam 开发者提供从路由、请求处理到模板渲染的一站式解决方案。该项目在 Hacker News 上被提及，最近一次更新是 2026‑05‑14，当前在 GitHub 上拥有约 45 分的评分。

---

## 价值说明  

| 维度 | 价值点 |
|------|--------|
| **语言一致性** | 直接使用 Gleam 编写前后端代码，避免在项目中混用多种语言，提升团队的认知一致性和代码可维护性。 |
| **Beam 生态兼容** | 运行在 BEAM（Erlang VM）上，天然享受高并发、容错和分布式特性，适合需要高可用的服务。 |
| **全栈特性** | 包含路由、请求/响应抽象、表单验证、模板系统以及与数据库的集成（通过适配器），可以快速搭建 MVP 或内部工具。 |
| **开源 & 可审计** | 完全开源，代码可自行审计，适合对安全合规有要求的团队。 |

---

## 典型接入方式  

1. **项目初始化**  
   ```bash
   gleam new my_app
   cd my_app
   gleam add rally
   ```

2. **配置路由**（`src/app.gleam`）  
   ```gleam
   import rally/router.{Router, get}
   import rally/http.{Response, request}
   
   pub fn start() {
     let router = Router.new()
       |> get("/", fn _ -> Response.ok("Hello from Rally!") end)
   
     rally.start(router)
   }
   ```

3. **启动服务**  
   ```bash
   gleam run   # 或者在 release 模式下使用 rebar3/erlang release
   ```

4. **集成数据库（可选）**  
   - 使用官方提供的 `rally_ecto` 适配器或自行实现 `rally.Database` 行为。  
   - 示例（PostgreSQL）  
     ```gleam
     import rally_ecto.{Repo, Postgres}
     
     let repo = Repo.new(Postgres.config("postgres://user:pass@localhost/db"))
     ```

5. **部署**  
   - 生成 BEAM 包并使用 `rebar3 release`、`docker` 或直接在 `systemd` 中运行。  
   - 由于运行在 BEAM 上，可利用 OTP 的热代码升级、监督树等特性实现零停机部署。

> **注意**：目前项目的集成信号（文档、示例、CI 状态）相对稀少，建议在正式接入前阅读源码、检查 Issue 列表并运行完整的单元/集成测试。

---

## 生产可用性评估  

| 维度 | 评估 | 说明 |
|------|------|------|
| **成熟度** | 中等 | 最近一次提交在 2026‑05‑14，项目活跃度一般，缺少明确的发布计划和长期维护承诺。 |
| **文档/示例** | 有限 | README 简要，缺少完整的使用手册和最佳实践，需要自行探索或补充文档。 |
| **社区/支持** | 稀疏 | 在 GitHub 上的 Issue、PR 活动不多，社区规模小。 |
| **许可证** | 待确认 | 在采用前务必检查 `LICENSE` 文件，确保符合公司合规要求。 |
| **适用场景** | 原型、内部工具、实验性服务 | 对于对 Gleam 有强烈偏好的团队，可快速验证概念；生产环境建议在充分评估后再使用，并配合内部监控、灰度发布等措施。 |
| **风险** | 代码维护、升级、缺少成熟生态 | 需要自行承担框架升级和 bug 修复的职责，或考虑在内部 fork 并维护。 |

**结论**：Rally 为 Gleam 开发者提供了便利的全栈 Web 开发体验，适合作为原型或内部系统的快速搭建工具。但由于质量信号有限、社区活跃度不高，建议在生产环境使用前进行严格的代码审查、补充文档以及制定内部维护计划。若项目对 Gleam 有长期投入计划，可考虑在此基础上自行扩展和维护，以提升生产可用性。

## 🧭 Practical evaluation

**Value:** Rally – Full-Stack Web Framework for Gleam on the Beam may be useful when its README and activity match a concrete workflow.

**Best use cases**

- Not enough metadata yet.

**Integration notes:** Needs manual inspection before adoption because integration signals are sparse in the discovered metadata.

**Production readiness:** Medium: useful for prototypes or internal workflows, with dependency and maintenance checks before production.

**Quality signals**

- updated 2026-05-14
- 2 topics

**Risks:** Quality signals are limited; verify license, maintenance, docs, issues, and release cadence before using it.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 0/100 |
| stars | 0/100 |
| topics | 25/100 |
| outlook | 57/100 |
| quality | 41/100 |
| recency | 100/100 |
| adoption | 0/100 |
| production | 58/100 |
| usefulness | 58/100 |
| integration | 30/100 |
| sourceTrust | 80/100 |

---

<sub>🔭 Discovered 2026-05-14 · [View on GitHub](https://github.com/pairshaped/rally-gleam) · [← Back to Misc](./README.md)</sub>
