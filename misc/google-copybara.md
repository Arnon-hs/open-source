# google/copybara

[![Stars](https://img.shields.io/github/stars/google/copybara?style=flat-square&color=yellow)](https://github.com/google/copybara/stargazers) [![Forks](https://img.shields.io/github/forks/google/copybara?style=flat-square&color=blue)](https://github.com/google/copybara/network) [![Language](https://img.shields.io/badge/lang-Java-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-61%2F100-brightgreen?style=flat-square)](#)

> Copybara: A tool for transforming and moving code between repositories.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 2.8k |
| 🍴 **Forks** | 310 |
| 💻 **Language** | Java |
| 📈 **Score** | 61/100 |
| 🗓️ **Last push** | 2026-09-05 |
| 🔍 **Source** | github |

## 🏷️ Topics

_no topics_

## 🎯 Categories

Misc

## 📝 Summary

### English

Copybara is a Java‑based tool that streamlines moving and transforming code across repositories, letting teams persist, query, and relocate data with far less custom plumbing. Adoption requires a manual inspection of its sparse integration signals and a review of license, security, and maintainer activity before it can be safely incorporated. Rated as medium‑production readiness, it is best suited for prototypes or internal workflows, pending dependency and maintenance checks for broader production use.

### Русский

Copybara — инструмент от Google для автоматизированного преобразования и переноса кода между репозиториями, позволяющий сократить ручные скрипты и поддерживать согласованность веток. Его типичное применение — настройка конвейеров CI/CD, где требуется мигрировать изменения из одной VCS (Git, Perforce и др.) в другую с возможностью кастомных трансформаций. Проект имеет умеренный уровень готовности к production: достаточно зрелый (2760 ★, активные коммиты), но перед вводом в продакшн рекомендуется проверить лицензирование, безопасность и наличие поддержки.

### 中文

**价值**  
Copybara 是 Google 开源的代码迁移与转换工具，能够把代码从一个仓库自动同步、重写或分支到另一个仓库。它通过统一的配置文件把常见的迁移规则（如路径重写、作者映射、提交过滤等）抽象出来，帮助团队省去手写脚本和人工审查的工作，从而在多仓库、多平台（Git、GitHub、GitLab、Perforce 等）之间实现可靠、可审计的代码流转。

**典型接入方式**  

| 步骤 | 说明 |
|------|------|
| 1️⃣ 环境准备 | 在 CI/CD 机器或本地工作站安装 JDK 11+，克隆 `google/copybara` 项目并使用 `./gradlew installDist` 编译生成可执行脚本。 |
| 2️⃣ 编写配置 | 在项目根目录新建 `copy.bara.sky`（Skyframe DSL），声明 **origin**（源仓库）和 **destination**（目标仓库），并使用 `core.workflow` 定义转换步骤（路径映射、文件过滤、提交信息模板等）。 |
| 3️⃣ 认证配置 | 为涉及的仓库提供凭证（SSH key、OAuth token 或 Perforce ticket），可通过环境变量或 `~/.netrc`、`~/.ssh/config` 等方式让 Copybara 自动读取。 |
| 4️⃣ 运行 & 验证 | 在 CI 步骤中执行 `copybara copy.bara.sky <workflow_name>`，首次运行建议加 `--dry-run` 或 `--force` 参数，仅打印计划的变更；确认无误后去掉 dry‑run 完成实际迁移。 |
| 5️⃣ 自动化 & 监控 | 将上述命令写入 Jenkins、GitHub Actions、GitLab CI 等流水线，配合邮件/Slack 通知，实现每日或 PR 触发的持续同步。 |

**生产可用性**  

- **成熟度**：GitHub ★ 2.8k，活跃度仍然保持（最近一次提交 2026‑06‑25），代码基于 Java，易于在企业内部编译和二次定制。  
- **适用场景**：内部代码库迁移、跨组织同步、历史仓库清理、从单一主仓库向微服务子仓库分发代码等。对外部用户而言，功能已相对稳定，适合作为 **原型** 或 **内部工作流** 的核心组件。  
- **风险与注意事项**：  
  - 需要在正式使用前进行 **手动审查**（尤其是复杂的路径映射或作者重写），因为元数据中缺少完整的集成测试报告。  
  - 许可证为 Apache‑2.0，基本商业友好，但仍建议审查公司合规部门的批准。  
  - 依赖 Java 运行时和 Gradle 构建系统，需确保对应版本在生产环境中得到维护。  
- **推荐级别**：**中等**（Medium）——适合在内部或受控的生产环境中使用，前提是做好依赖管理、定期升级以及安全审计后再推广至关键业务。  

> **一句话概括**：Copybara 通过声明式配置把跨仓库的代码迁移自动化，接入方式简洁（配置文件 + CI 步骤），在内部流程中已具备可用性，只要做好审查和维护即可在生产环境安全使用。

## 🧭 Practical evaluation

**Value:** google/copybara helps teams persist, query, and move data with less custom plumbing.

**Best use cases**

- manage persistence
- speed up data access
- prototype database-backed apps

**Integration notes:** Needs manual inspection before adoption because integration signals are sparse in the discovered metadata.

**Production readiness:** Medium: useful for prototypes or internal workflows, with dependency and maintenance checks before production.

**Quality signals**

- 2760 GitHub stars
- 310 forks
- updated 2026-06-25
- primary language: Java

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 62/100 |
| stars | 73/100 |
| topics | 0/100 |
| outlook | 67/100 |
| quality | 67/100 |
| recency | 80/100 |
| adoption | 70/100 |
| production | 67/100 |
| usefulness | 58/100 |
| integration | 46/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 0/100 |

---

<sub>🔭 Discovered 2026-06-25 · [View on GitHub](https://github.com/google/copybara) · [← Back to Misc](./README.md)</sub>
