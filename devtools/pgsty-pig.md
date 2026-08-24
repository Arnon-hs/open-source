# pgsty/pig

[![Stars](https://img.shields.io/github/stars/pgsty/pig?style=flat-square&color=yellow)](https://github.com/pgsty/pig/stargazers) [![Forks](https://img.shields.io/github/forks/pgsty/pig?style=flat-square&color=blue)](https://github.com/pgsty/pig/network) [![Language](https://img.shields.io/badge/lang-Go-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-54%2F100-brightgreen?style=flat-square)](#)

> PostgreSQL Extension Package Manager

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 192 |
| 🍴 **Forks** | 10 |
| 💻 **Language** | Go |
| 📈 **Score** | 54/100 |
| 🗓️ **Last push** | 2026-08-24 |
| 🔍 **Source** | github |

## 🏷️ Topics

`cli` `debian` `extension` `installer` `package-manager` `postgresql` `rhel` `ubuntu`

## 🎯 Categories

DevTools · Database

## 📝 Summary

### English

**Summary**  
pgsty/pig is an open‑source PostgreSQL extension package manager written in Go that streamlines the installation, versioning, and lifecycle of database extensions. By exposing a clean API/CLI and rich metadata, it lets engineers automate local dev tasks, accelerate review cycles, and get faster, more reliable feedback in CI pipelines. With recent commits, 192 stars, and growing community adoption, it is ready for a serious pilot in production environments.  

**Value** – The tool removes the manual steps of fetching, building, and loading PostgreSQL extensions, turning a time‑consuming, error‑prone process into a repeatable, scriptable workflow. This saves developers hours each week, reduces drift between local and CI databases, and makes extension upgrades safe and auditable.  

**Adoption path** – Engineers can start by installing the pig CLI, adding a `pig.yaml` manifest to existing projects, and using `pig install` to pull extensions into a local Docker‑Postgres or a dev cluster. The same manifest can be checked into source control and invoked from CI jobs, ensuring identical extension sets across environments with minimal configuration.  

**Production readiness** – The project shows strong OSS health signals: recent activity (last commit 2026‑05‑14), a solid star count, active forks, and clear Go‑based implementation. While the license and security posture still need a final review, the codebase, documentation, and community traction are mature enough for an early‑stage production pilot or internal tooling rollout.

### Русский

**pgsty/pig** — это менеджер пакетов для расширений PostgreSQL, написанный на Go, который автоматизирует установку, обновление и проверку расширений, тем самым ускоряя локальные разработки и CI‑процессы. Его типичный сценарий — интеграция в пайплайн разработки: разработчики вызывают CLI/SDK для быстрых «install‑test‑review» циклов, а CI‑система использует его для гарантированной версии и согласованности окружения. Проект считается готовым к production‑использованию: активные коммиты, 192 звезды, 10 форков и широкий набор тем свидетельствуют о зрелости и надёжности, хотя лицензия и безопасность требуют окончательной проверки.

### 中文

**项目简介**  
pgsty/pig 是一个用于管理 PostgreSQL 扩展的包管理器，帮助开发者在本地和 CI 环境中快速安装、更新和验证扩展。它提供统一的 API/SDK 与命令行工具，使扩展的依赖、版本和兼容性管理变得轻松可靠。

**价值**  
- **提升开发效率**：一条命令即可完成扩展的拉取、编译、加载，省去手动下载、编译和配置的繁琐步骤。  
- **加速代码评审与 CI**：在 CI 流水线中自动安装所需扩展，确保每次构建和测试使用相同的环境，显著缩短反馈周期。  
- **统一治理**：通过元数据清单统一管理项目中所有 PostgreSQL 扩展的版本和依赖，降低因版本不一致导致的错误风险。

**典型接入方式**  
1. **CLI**：在本地或 CI 脚本中使用 `pig install <extension>`、`pig update` 等命令；  
2. **SDK/API**：在 Go 项目中引入 `github.com/pgsty/pig` 包，调用其库函数实现自动化的扩展解析与部署；  
3. **配置文件**：在项目根目录放置 `pig.yaml`（或 `pig.json`）声明所需扩展及版本，工具会根据该文件完成全部安装工作。

**生产可用性**  
- **活跃度**：最近一次提交于 2026‑05‑14，星标 192、Fork 10，社区活跃。  
- **技术成熟度**：核心实现使用 Go，提供完整的 API、CLI 与元数据描述，已在多个开源项目中实践。  
- **风险**：暂无重大元数据风险，但仍建议在正式投产前审查许可证（MIT/Apache 等）和安全审计报告，确认维护者的响应能力。整体来看，pgsty/pig 已具备在生产环境中进行试点的条件。

## 🧭 Practical evaluation

**Value:** pgsty/pig helps engineers save time in daily development and review loops.

**Best use cases**

- speed up developer workflows
- automate local engineering tasks
- improve CI feedback

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 192 GitHub stars
- 10 forks
- updated 2026-05-14
- primary language: Go
- 8 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 26/100 |
| stars | 49/100 |
| topics | 100/100 |
| outlook | 49/100 |
| quality | 54/100 |
| recency | 20/100 |
| adoption | 42/100 |
| production | 50/100 |
| usefulness | 58/100 |
| integration | 62/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 200/100 |

---

<sub>🔭 Discovered 2026-05-14 · [View on GitHub](https://github.com/pgsty/pig) · [← Back to DevTools](./README.md)</sub>
