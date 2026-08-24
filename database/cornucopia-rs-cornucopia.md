# cornucopia-rs/cornucopia

[![Stars](https://img.shields.io/github/stars/cornucopia-rs/cornucopia?style=flat-square&color=yellow)](https://github.com/cornucopia-rs/cornucopia/stargazers) [![Forks](https://img.shields.io/github/forks/cornucopia-rs/cornucopia?style=flat-square&color=blue)](https://github.com/cornucopia-rs/cornucopia/network) [![Language](https://img.shields.io/badge/lang-Rust-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-48%2F100-brightgreen?style=flat-square)](#)

> Generate type-checked Rust from your PostgreSQL.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 1.1k |
| 🍴 **Forks** | 71 |
| 💻 **Language** | Rust |
| 📈 **Score** | 48/100 |
| 🗓️ **Last push** | 2026-08-24 |
| 🔍 **Source** | github |

## 🏷️ Topics

`database` `postgres` `postgresql` `rust` `sql`

## 🎯 Categories

Database

## 📝 Summary

### English

**Brief Summary**  
Cornucopia‑rs / cornucopia is an open‑source Rust library that generates type‑checked Rust code from PostgreSQL queries, letting developers write SQL inline while getting compile‑time guarantees that the query matches the database schema. With over a thousand stars and active maintenance, it is a practical choice for Rust‑centric data pipelines and reporting tools.

**Value**  
- **Safety & Productivity** – By turning SQL into Rust types, Cornucopia eliminates a whole class of runtime errors (e.g., mismatched column names or wrong data types) and lets IDEs provide autocomplete and refactoring for both Rust and SQL.  
- **Performance** – The generated code uses native `tokio‑postgres`/`deadpool` drivers, so there is no extra ORM overhead; you get raw‑SQL speed with compile‑time checks.  
- **Consistency** – Because the generated code is regenerated whenever the schema changes, the Rust codebase stays in sync with the database automatically, reducing drift in analytics or reporting pipelines.

**Practical Adoption Path**  
1. **Proof‑of‑Concept** – Clone the repo, run `cargo install cornucopia-cli`, and generate code for a small, self‑contained query set (e.g., a single reporting view). Verify that the generated types compile against your existing Rust project.  
2. **CI Integration** – Add a step to your CI pipeline that runs `cornucopia generate` on every schema migration, committing the generated files or checking them in as part of the build.  
3. **Gradual Migration** – Replace hand‑written query modules with Cornucopia‑generated ones module‑by‑module, starting with low‑risk analytics jobs.  
4. **Documentation & Training** – Use the README and example projects as onboarding material for developers unfamiliar with the CLI.

**Production Readiness**  
- **Maturity**: Medium. The project is actively maintained (last commit 2026‑06‑25) and has a healthy community (≈1.1 k stars, 71 forks), indicating stability for internal or prototype use.  
- **Dependencies**: Relies on `tokio-postgres` and standard async Rust ecosystem; ensure version compatibility with your existing stack.  
- **Risks**: Integration steps are not fully documented in the README, so expect some initial setup effort to align schema migrations with code generation. Conduct a small pilot to measure generation time, build impact, and any edge‑case handling (e.g., custom types or extensions).  
- **Recommendation**: Suitable for internal services, analytics pipelines, or micro‑services where type safety is a priority. Before promoting to mission‑critical production, perform a thorough dependency audit, add integration tests around generated queries, and lock the Cornucopia version to avoid breaking changes.

### Русский

**cornucopia-rs/cornucopia** — это open‑source библиотека, генерирующая типобезопасный Rust‑код из схем PostgreSQL, что позволяет писать запросы с полной проверкой на этапе компиляции. Типичный сценарий — быстрое прототипирование или построение внутренних аналитических/ETL‑конвейеров, где запросы к базе проверяются компилятором и легко интегрируются в существующий Rust‑проекты. Готовность к production — средняя: проект стабилен и активно поддерживается (1100 ★, обновления в 2026 г.), но перед выводом в продакшн стоит проверить зависимости, процесс настройки и покрытие тестами в небольшом proof‑of‑concept.

### 中文

**项目简介（2‑3 句）**  
Cornucopia（cornucopia‑rs/cornucopia）是一款 Rust 宏库，能够根据 PostgreSQL 数据库的 schema 生成类型安全的 Rust 代码，让编写数据库查询时拥有编译期检查、自动映射和 IDE 提示。它把原始 SQL 直接转化为 Rust 的结构体与函数，从而在 Rust 项目中安全、便捷地使用 PostgreSQL。

**价值**  
- **类型安全**：SQL 语句在编译阶段即被校验，避免运行时的字段名/类型错误。  
- **开发效率**：自动生成的结构体和查询函数省去手写 DTO 与手动映射的工作，加快原型和业务实现。  
- **可维护性**：数据库 schema 变更后只需重新生成代码，即可同步更新 Rust 端模型，降低因 schema 漏改导致的 bug。  

**典型接入方式**  
1. **依赖引入**：在 `Cargo.toml` 中添加 `cornucopia` 与 `postgres`（或 `tokio-postgres`）依赖。  
2. **生成代码**：在项目根目录创建 `cornucopia.toml` 配置文件，指定数据库连接信息与生成目录，然后运行 `cargo cornucopia generate`（或使用 `cargo install cornucopia-cli` 后的 `cornucopia generate`）生成对应的 Rust 模块。  
3. **在代码中使用**：`mod db { include!("src/generated/cornucopia.rs"); }`，随后通过 `db::queries::your_query::fetch(&mut client, …).await?` 调用生成的查询函数，返回的结构体已经是强类型。  
4. **CI/CD 集成**：在 CI 流程中加入生成步骤，确保每次 schema 变更后代码保持同步。

**生产可用性**  
- **成熟度**：已有 1.1k+ Stars、71 Forks，活跃维护至 2026‑06‑25，社区反馈良好。  
- **适用场景**：非常适合内部工具、数据分析服务、原型验证以及对类型安全要求高的微服务。对外部高并发、超大规模生产环境仍需自行评估其与现有连接池、事务管理的兼容性。  
- **准备度**：中等（Medium）。在投入生产前建议：  
  1. **小范围 PoC**：先在单一业务模块实现并跑测试，验证生成代码与业务逻辑的匹配度。  
  2. **依赖审计**：检查 `cornucopia` 及其生成的代码对 `postgres` 驱动的版本要求，确保与现有栈兼容。  
  3. **监控与回滚**：在 CI 中加入生成代码的差异检查，防止 schema 变更意外破坏生产查询。  

总体而言，Cornucopia 为 Rust + PostgreSQL 项目提供了可靠的类型安全层，适合作为内部数据处理或分析管道的基础设施，只要在正式上线前完成上述验证，即可安全投入生产使用。

## 🧭 Practical evaluation

**Value:** cornucopia-rs/cornucopia helps convert raw data into searchable, analyzable, or automated pipelines.

**Best use cases**

- organize analytics pipelines
- process datasets
- improve reporting workflows

**Integration notes:** Looks feasible to evaluate, but integration should start with a small proof of concept and README check.

**Production readiness:** Medium: useful for prototypes or internal workflows, with dependency and maintenance checks before production.

**Quality signals**

- 1100 GitHub stars
- 71 forks
- updated 2026-06-25
- primary language: Rust
- 5 topics

**Risks:** Integration path is not obvious from metadata; validate setup cost before committing.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 46/100 |
| stars | 65/100 |
| topics | 63/100 |
| outlook | 54/100 |
| quality | 61/100 |
| recency | 40/100 |
| adoption | 60/100 |
| production | 53/100 |
| usefulness | 42/100 |
| integration | 30/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 100/100 |

---

<sub>🔭 Discovered 2026-06-25 · [View on GitHub](https://github.com/cornucopia-rs/cornucopia) · [← Back to Database](./README.md)</sub>
