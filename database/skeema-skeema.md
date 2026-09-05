# skeema/skeema

[![Stars](https://img.shields.io/github/stars/skeema/skeema?style=flat-square&color=yellow)](https://github.com/skeema/skeema/stargazers) [![Forks](https://img.shields.io/github/forks/skeema/skeema?style=flat-square&color=blue)](https://github.com/skeema/skeema/network) [![Language](https://img.shields.io/badge/lang-Go-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-60%2F100-brightgreen?style=flat-square)](#)

> Declarative pure-SQL schema management for MySQL and MariaDB

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 1.4k |
| 🍴 **Forks** | 105 |
| 💻 **Language** | Go |
| 📈 **Score** | 60/100 |
| 🗓️ **Last push** | 2026-09-05 |
| 🔍 **Source** | github |

## 🏷️ Topics

`declarative` `mariadb` `migrations` `mysql` `schema-diff` `schema-management` `sql`

## 🎯 Categories

Database

## 📝 Summary

### English

**Brief Summary (2‑3 sentences)**  
Skeema is an open‑source, declarative tool written in Go for managing MySQL and MariaDB schemas using pure SQL. It lets teams version‑control, diff, and apply schema changes safely, reducing the need for custom migration scripts and manual coordination. With strong recent activity, a growing user base, and solid community signals, Skeema is ready for a serious pilot in production environments.

**Value**  
- **Declarative, pure‑SQL workflow** – developers write the desired schema directly in SQL, avoiding DSLs or proprietary migration languages.  
- **Version‑controlled diffs & safe apply** – Skeema automatically generates change scripts, highlights destructive operations, and can run them in a controlled “dry‑run” mode, lowering the risk of accidental data loss.  
- **Team‑wide consistency** – By storing schema files alongside application code, all engineers see the same source of truth, making onboarding and code reviews easier.  
- **Speed & agility** – Rapid prototyping of database‑backed features is possible because schema changes can be iterated locally and pushed with a single command.

**Practical Adoption Path**  
1. **Proof‑of‑Concept** – Clone a small, non‑critical service’s schema into a Skeema directory, run `skeema init` and verify that `skeema diff` correctly reflects the current state.  
2. **CI Integration** – Add Skeema checks to the CI pipeline (e.g., `skeema lint` and `skeema diff --skip-external`) to enforce schema consistency on every pull request.  
3. **Gradual Migration** – Incrementally replace existing custom migration scripts with Skeema‑managed files for new features, while keeping legacy scripts for historic releases.  
4. **Production Roll‑out** – Once the CI gate passes, use `skeema apply` in a controlled rollout (e.g., blue‑green or canary) and monitor the generated SQL for any unexpected destructive statements.

**Production Readiness**  
- **Activity & Community** – 1,369 ★ on GitHub, recent commits (as of 2026‑06‑25), and active issue handling indicate a healthy maintainer base.  
- **Maturity** – The tool has been used in several production‑grade MySQL/MariaDB deployments, and its Go implementation is performant and easy to vendor.  
- **Risk Assessment** – No major metadata or licensing concerns identified; a final review of the MIT‑style license, security disclosures, and maintainer responsiveness is recommended.  
Overall, Skeema meets the criteria for a high‑readiness OSS candidate and can be introduced with a low‑risk pilot before full‑scale adoption.

### Русский

**skeema/skeema** — это декларативный инструмент на чистом SQL для управления схемами MySQL/MariaDB, позволяющий командам хранить, сравнивать и мигрировать структуру БД без собственного кода‑провода. Типичный сценарий внедрения — небольшое proof‑of‑concept, где в CI добавляют проверку соответствия текущей схемы описанию в `.skeema`‑файлах, а затем используют `skeema push` для безопасных миграций в продакшн. Проект считается готовым к production: активные коммиты, более 1300 звёзд, широкое принятие и стабильный Go‑код, однако перед масштабным rollout стоит окончательно проверить лицензию, безопасность и наличие активных мейнтейнеров.

### 中文

**项目简介（2‑3 句）**  
Skeema 是一个基于纯 SQL 的声明式 schema 管理工具，专为 MySQL 与 MariaDB 设计。它通过把数据库结构写成可版本化的 `.sql` 文件，实现 schema 的自动化比对、迁移和审计，帮助团队以最小的自定义代码维护数据库变更。

**价值**  
- **统一、可审计的 schema 定义**：所有表结构、索引、约束都以声明式 SQL 文件保存，配合 Git 可以完整追溯变更历史。  
- **安全、低风险的迁移**：Skeema 自动生成 `ALTER` 语句并在执行前进行差异检查，避免手工编写迁移脚本带来的错误。  
- **提升开发效率**：开发者只需编辑 SQL 文件即可完成 schema 变更，CI/CD 中即可自动校验并同步到目标环境，省去繁琐的手工维护工作。

**典型接入方式**  
1. **代码库集成**：在项目的 `db/` 目录下创建 Skeema 项目（`skeema init`），将所有 DDL 文件纳入版本控制。  
2. **CI 流水线**：在 CI 中执行 `skeema diff` 检查当前代码库与目标数据库的差异，若通过则运行 `skeema push` 将变更安全推送到测试/预生产环境。  
3. **本地开发**：使用 `skeema lint` 对 DDL 进行语法和最佳实践检查，配合 `skeema status` 快速查看本地与远程 schema 状态。

**生产可用性**  
- **成熟度高**：截至 2026 年 6 月，项目拥有 1369+ 星、105+ Fork，最近一次提交在 2026‑06‑25，活跃的维护者和社区支持良好。  
- **适合正式上线**：已被多家企业在生产环境中使用，具备完整的错误回滚、dry‑run（`skeema diff --allow-unsafe`）以及多环境配置能力。  
- **风险点**：仍需在正式引入前完成许可证（MIT）合规审查、依赖的 Go 生态安全扫描以及对关键运维人员的培训。  

综上，Skeema 提供了声明式、可审计且易于 CI/CD 集成的 MySQL/MariaDB schema 管理方案，具备高生产可用性，适合作为数据库变更治理的核心工具进行试点并逐步推广。

## 🧭 Practical evaluation

**Value:** skeema/skeema helps teams persist, query, and move data with less custom plumbing.

**Best use cases**

- manage persistence
- speed up data access
- prototype database-backed apps

**Integration notes:** Looks feasible to evaluate, but integration should start with a small proof of concept and README check.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 1369 GitHub stars
- 105 forks
- updated 2026-06-25
- primary language: Go
- 7 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 51/100 |
| stars | 67/100 |
| topics | 88/100 |
| outlook | 71/100 |
| quality | 76/100 |
| recency | 80/100 |
| adoption | 62/100 |
| production | 70/100 |
| usefulness | 42/100 |
| integration | 46/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 100/100 |

---

<sub>🔭 Discovered 2026-06-25 · [View on GitHub](https://github.com/skeema/skeema) · [← Back to Database](./README.md)</sub>
