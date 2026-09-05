# zhensherlock/intellij-platform-git-stats-plugin

[![Stars](https://img.shields.io/github/stars/zhensherlock/intellij-platform-git-stats-plugin?style=flat-square&color=yellow)](https://github.com/zhensherlock/intellij-platform-git-stats-plugin/stargazers) [![Forks](https://img.shields.io/github/forks/zhensherlock/intellij-platform-git-stats-plugin?style=flat-square&color=blue)](https://github.com/zhensherlock/intellij-platform-git-stats-plugin/network) [![Language](https://img.shields.io/badge/lang-Kotlin-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-59%2F100-brightgreen?style=flat-square)](#)

> Git activity statistics for IntelliJ Platform IDEs, with date/author filters, excluded paths, copy, and CSV export.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 194 |
| 🍴 **Forks** | 2 |
| 💻 **Language** | Kotlin |
| 📈 **Score** | 59/100 |
| 🗓️ **Last push** | 2026-09-05 |
| 🔍 **Source** | github |

## 🏷️ Topics

`code-metrics` `developer-tools` `git` `git-statistics` `git-stats` `gradle` `intellij` `intellij-idea` `intellij-idea-plugin` `intellij-platform` `intellij-plugin` `jetbrains`

## 🎯 Categories

Productivity · DevTools · Observability

## 📝 Summary

### English

**Brief Summary**  
The *intellij‑platform‑git‑stats‑plugin* adds a lightweight dashboard to any IntelliJ‑based IDE that shows Git activity statistics (commits per day, per author, etc.) with built‑in date/author filters, path exclusions, copy‑to‑clipboard, and CSV export. It is written in Kotlin, has ~194 GitHub stars, and is actively maintained as of June 2026.

**Value Proposition**  
- **Instant observability**: Developers can see who is working on which files and when, without leaving the IDE.  
- **Data export**: CSV output makes it easy to feed commit metrics into downstream analytics, dashboards, or AI‑driven tooling (e.g., RAG pipelines that need recent change history).  
- **Customizable filters**: Date ranges, author selection, and excluded paths let teams focus on the code areas that matter for a given investigation or model‑training run.  

**Practical Adoption Path**  
1. **Install** the plugin from the JetBrains Marketplace or build from source (Kotlin/Gradle).  
2. **Configure** the optional exclusion patterns and default date windows in the plugin settings.  
3. **Use** the UI panel to explore stats, copy values, or export CSV files.  
4. **Integrate** the exported CSV into AI/ML pipelines (e.g., feeding recent commit logs to a code‑summarisation model or a RAG system).  
5. **Automate**: For internal tooling, wrap the plugin’s CLI (or invoke the underlying Git‑stats library) in CI scripts to generate periodic reports.

**Production‑Readiness Assessment**  
- **Maturity**: Medium. The plugin is functional, has a modest user base, and is updated regularly, but it is primarily aimed at developer productivity rather than enterprise‑grade monitoring.  
- **Dependencies**: Pure Kotlin/IntelliJ SDK; no heavyweight external services, making it easy to sandbox.  
- **Maintenance**: Activity is recent, but the maintainer count is low; a production rollout should include a plan for monitoring upstream changes and possibly forking the repo for internal fixes.  
- **Security & Licensing**: No obvious red‑flags, but a formal license review and vulnerability scan of the bundled IntelliJ SDK are advisable before wide deployment.  

Overall, the plugin is a solid building block for prototypes or internal tooling that need quick access to Git activity data and can be safely introduced into production environments after a brief dependency and security audit.

### Русский

Резюме:

Плагин "zhensherlock/intellij-platform-git-stats-plugin" предоставляет функцию отображения статистики Git-активности в IntelliJ Platform IDEs, позволяя фильтровать данные по дате и автору, исключать конкретные пути, копировать и экспортировать в CSV-формат. Он идеально подходит для прототипирования AI-функций, построения RAG или агентных потоков, оценки инструментов моделирования. Плагин готов к использованию в прототипах или внутренних потоках, но требует тщательного просмотра зависимостей и поддержки перед внедрением в производство.

### 中文

**简短介绍**

zhensherlock/intellij-platform-git-stats-plugin 是一个开源项目，提供了 Git 活动统计功能，支持 IntelliJ 平台 IDEs，具有日期/作者过滤、排除路径、复制和 CSV 导出功能。该插件适用于开发者，帮助他们添加 AI 能力并评估模型工具。

**价值**

该插件的价值在于它提供了 Git 活动统计功能，帮助开发者了解项目的开发情况和趋势。它还支持日期/作者过滤、排除路径、复制和 CSV 导出功能，方便开发者分析和理解项目数据。

**典型接入方式**

该插件可以通过以下方式接入：

1. 在 IntelliJ IDE 中安装插件。
2. 在项目中配置插件，指定 Git 仓库路径和过滤条件。
3. 使用插件的功能来分析和理解项目数据。

**生产可用性**

该插件的生产可用性为中等。它适用于开发者在内部工作流中使用的 prototype 或内部工作流程，需要进行依赖检查和维护检查后才能用于生产环境。

## 🧭 Practical evaluation

**Value:** zhensherlock/intellij-platform-git-stats-plugin helps add AI capability without starting from a blank model stack.

**Best use cases**

- prototype AI features
- build RAG or agent workflows
- evaluate model tooling

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** Medium: useful for prototypes or internal workflows, with dependency and maintenance checks before production.

**Quality signals**

- 194 GitHub stars
- 2 forks
- updated 2026-06-29
- primary language: Kotlin
- 16 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 12/100 |
| stars | 49/100 |
| topics | 100/100 |
| outlook | 69/100 |
| quality | 67/100 |
| recency | 80/100 |
| adoption | 38/100 |
| production | 67/100 |
| usefulness | 58/100 |
| integration | 46/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 300/100 |

---

<sub>🔭 Discovered 2026-06-29 · [View on GitHub](https://github.com/zhensherlock/intellij-platform-git-stats-plugin) · [← Back to Productivity](./README.md)</sub>
