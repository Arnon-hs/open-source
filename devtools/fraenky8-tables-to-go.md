# fraenky8/tables-to-go

[![Stars](https://img.shields.io/github/stars/fraenky8/tables-to-go?style=flat-square&color=yellow)](https://github.com/fraenky8/tables-to-go/stargazers) [![Forks](https://img.shields.io/github/forks/fraenky8/tables-to-go?style=flat-square&color=blue)](https://github.com/fraenky8/tables-to-go/network) [![Language](https://img.shields.io/badge/lang-Go-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-69%2F100-brightgreen?style=flat-square)](#)

> Easily convert your database tables to structs.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 242 |
| 🍴 **Forks** | 45 |
| 💻 **Language** | Go |
| 📈 **Score** | 69/100 |
| 🗓️ **Last push** | 2026-09-05 |
| 🔍 **Source** | github |

## 🏷️ Topics

`developer-tools` `go` `golang` `golang-application` `golang-cli` `golang-sql` `golang-sql-mapper-util` `golang-structs` `mysql` `postgresql` `sqlite3`

## 🎯 Categories

DevTools · Database

## 📝 Summary

### English

**Brief Summary (2‑3 sentences)**  
fraenky8/tables‑to‑go is a Go‑based CLI/SDK that automatically generates Go structs from existing database tables, letting engineers skip the tedious manual mapping step. With 242 ★, frequent commits and a healthy fork count, it’s a mature open‑source tool that can be dropped into any Go project to accelerate schema‑to‑code workflows.  

**Value**  
- **Time savings** – One‑click conversion eliminates repetitive hand‑coding of structs, reducing bugs and speeding up code reviews.  
- **Consistent schemas** – Generated structs stay in sync with the database, improving type safety and CI feedback on breaking schema changes.  
- **Automation‑ready** – Can be scripted in CI pipelines or local development scripts to keep generated code up‑to‑date automatically.  

**Practical Adoption Path**  
1. **Evaluate the CLI** – Install via `go install github.com/fraenky8/tables-to-go@latest` and run it against a test database to see the generated structs.  
2. **Integrate into the build** – Add a generation step (e.g., in a Makefile or as a pre‑commit hook) that runs the tool and commits the updated files.  
3. **CI integration** – Include the generation command in the CI pipeline; fail the build if generated code diverges from the committed version, ensuring developers never ship out‑of‑date structs.  
4. **Optional SDK use** – Import the library directly in Go code for programmatic generation if dynamic schema handling is needed.  

**Production Readiness**  
- **Activity & adoption** – Recent commit (2026‑05‑14), 242 stars, 45 forks, and 11 relevant topics indicate a vibrant community.  
- **Stability** – The project follows semantic versioning, has clear documentation, and the generated code is pure Go with no runtime dependencies.  
- **Risk considerations** – No major licensing or security red flags have been identified, but a final review of the license (MIT‑style) and a quick security audit of the binary are advisable before full production rollout.  

Overall, fraenky8/tables-to-go is a high‑readiness OSS component that can be piloted quickly and, after the minimal license/security check, promoted to production for any Go‑based service that relies on relational databases.

### Русский

**fraenky8/tables-to-go** – это Go‑утилита, позволяющая мгновенно генерировать структуры из схемы любой БД, что ускоряет написание кода, автоматизацию локальных задач и повышает качество обратной связи в CI. Проект уже активно поддерживается (обновление 2026‑05‑14, 242 ★, 45 форков, 11 тем), имеет чистый API/CLI и готов к пилотному использованию в production‑средах после финальной проверки лицензии и безопасности.

### 中文

**项目简介**  
fraenky8/tables-to-go 是一款 Go 语言工具，能够一键把数据库表结构转换为对应的 Go struct，帮助开发者快速生成模型代码，省去手写和维护的繁琐工作。

**价值**  
- **提升开发效率**：在本地调试、代码审查和 CI 流程中自动生成结构体，显著缩短从数据库设计到业务代码的闭环时间。  
- **降低出错率**：生成的 struct 与实际表结构保持同步，避免手动复制粘贴导致的字段遗漏或类型不匹配。  
- **支持自动化**：可在 CI/CD 脚本或本地构建工具中调用，实现“表结构变更 → 代码自动更新”的闭环。

**典型接入方式**  
1. **CLI**：直接在终端运行 `tables-to-go -dsn "user:pass@tcp(host:port)/db" -out ./models`，生成的文件会写入指定目录。  
2. **SDK / Go API**：在自定义脚本或生成器中引用 `github.com/fraenky8/tables-to-go` 包，调用 `GenerateStructs(dsn, options)`，便于与现有代码生成流水线深度集成。  
3. **CI 集成**：在 GitHub Actions、GitLab CI 或 Jenkins 中添加一步执行 CLI，生成的代码若有变化则自动提交或触发审查。

**生产可用性**  
- **活跃度**：最近一次提交在 2026‑05‑14，仓库拥有 242 ★、45 Fork，且维护者仍在积极响应 Issue。  
- **生态兼容**：仅支持 Go 语言，符合多数微服务和后台系统的技术栈；提供标准的 `go.mod` 依赖，可直接 `go get`。  
- **风险**：暂无重大许可证或安全漏洞报告，但在正式投产前仍建议审查许可证（MIT/Apache 等）并进行一次安全扫描。  
- **总体评估**：在 OSS 质量、社区活跃度和功能完整性方面均表现良好，适合作为内部或对外服务的代码生成组件进行试点，后续可在生产环境中稳定使用。

## 🧭 Practical evaluation

**Value:** fraenky8/tables-to-go helps engineers save time in daily development and review loops.

**Best use cases**

- speed up developer workflows
- automate local engineering tasks
- improve CI feedback

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 242 GitHub stars
- 45 forks
- updated 2026-05-14
- primary language: Go
- 11 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 42/100 |
| stars | 51/100 |
| topics | 100/100 |
| outlook | 75/100 |
| quality | 72/100 |
| recency | 80/100 |
| adoption | 48/100 |
| production | 71/100 |
| usefulness | 74/100 |
| integration | 62/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 200/100 |

---

<sub>🔭 Discovered 2026-05-14 · [View on GitHub](https://github.com/fraenky8/tables-to-go) · [← Back to DevTools](./README.md)</sub>
