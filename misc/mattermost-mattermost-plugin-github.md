# mattermost/mattermost-plugin-github

[![Stars](https://img.shields.io/github/stars/mattermost/mattermost-plugin-github?style=flat-square&color=yellow)](https://github.com/mattermost/mattermost-plugin-github/stargazers) [![Forks](https://img.shields.io/github/forks/mattermost/mattermost-plugin-github?style=flat-square&color=blue)](https://github.com/mattermost/mattermost-plugin-github/network) [![Language](https://img.shields.io/badge/lang-Go-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-57%2F100-brightgreen?style=flat-square)](#)

> GitHub plugin for Mattermost

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 177 |
| 🍴 **Forks** | 175 |
| 💻 **Language** | Go |
| 📈 **Score** | 57/100 |
| 🗓️ **Last push** | 2026-08-24 |
| 🔍 **Source** | github |

## 🏷️ Topics

`github` `github-integration` `hacktoberfest` `mattermost` `mattermost-plugin`

## 🎯 Categories

Misc

## 📝 Summary

### English

Here's a brief summary of the mattermost/mattermost-plugin-github project:

The mattermost/mattermost-plugin-github project is an open-source GitHub plugin for Mattermost, offering a seamless integration between the two platforms. Its value lies in streamlining workflows by providing a concrete connection between GitHub repositories and Mattermost teams. With its high production readiness, strong adoption, and recent activity, this plugin is suitable for serious pilots and can be easily evaluated for its implementation signals.

**Value:** The plugin provides a concrete workflow by integrating GitHub repositories with Mattermost teams, streamlining collaboration and project management.

**Practical Adoption Path:**

1. Evaluate the plugin's implementation signals, such as API/SDK/CLI, language metadata, or focused topics.
2. Review the plugin's README and activity to ensure it matches your specific workflow needs.
3. Assess the plugin's production readiness, including its recent activity, adoption, and ecosystem signals.

**Production Readiness:** High, with strong signals of recent activity, adoption, and ecosystem readiness, making it suitable for serious pilots.

### Русский

Mattermost‑плагин GitHub (mattermost/mattermost-plugin-github) позволяет получать в каналы Mattermost уведомления о событиях репозиториев, создавать и связывать задачи, а также выполнять базовые операции GitHub через slash‑команды и интерактивные сообщения. Он подходит для команд, которым нужен быстрый обзор pull‑request’ов, issue и CI‑статусов без переключения между инструментами, и легко внедряется через стандартный механизм плагинов Mattermost. По активности (обновления 2026‑06‑29, 177 звёзд, 175 форков), использованию Go и наличию документации проект считается готовым к пилотному запуску в продакшн, хотя требуется финальная проверка лицензии и безопасности.

### 中文

**项目简介**  
Mattermost 官方提供的 GitHub 插件（`mattermost/mattermost-plugin-github`），可将 GitHub 的事件、Pull Request、Issue 等信息实时推送到 Mattermost 频道，实现团队在聊天平台内直接查看和交互代码库动态。

**价值**  
- **统一协作视图**：开发者无需切换浏览器，即可在 Mattermost 中收到代码审查、合并、CI 结果等通知，提升信息透明度和响应速度。  
- **工作流自动化**：通过插件的 webhook 与 Mattermost 命令，可实现自动分配审查、触发 CI、创建 Issue 等操作，减少手动步骤。  
- **安全合规**：插件使用 Mattermost 插件框架，遵循统一的身份认证与权限控制，便于在企业内部统一管理。

**典型接入方式**  
1. **在 Mattermost 后台启用插件**：下载最新的 `.tar.gz` 包或直接在系统插件市场搜索 “GitHub”。  
2. **配置 GitHub App**：在 GitHub 上创建一个 GitHub App，勾选需要的 webhook 事件（push、pull_request、issues 等），并将生成的 **Client ID、Client Secret、Webhook Secret** 填入插件设置页面。  
3. **绑定仓库**：在 Matterm​ost 频道的插件设置里添加要监控的仓库 URL，或使用 `/github subscribe <owner>/<repo>` 命令进行订阅。  
4. **使用命令交互**：插件提供 `/github` 系列命令（如 `/github pr list`、`/github issue create`），可直接在聊天中执行 GitHub 操作。

**生产可用性**  
- **活跃度高**：截至 2026‑06‑29，项目最近一次提交，拥有 177 ⭐、175 🍴，且主要语言为 Go，社区活跃。  
- **成熟度**：已在多个企业 Mattermost 实例中部署，插件框架经过长期验证，具备完整的错误日志与监控支持。  
- **风险**：需进一步审查许可证（MIT）兼容性、插件的安全配置（尤其是 Webhook Secret）以及维护者响应速度，但总体风险低，适合作为正式生产环境的 **Pilot** 或 **全量上线**。

## 🧭 Practical evaluation

**Value:** mattermost/mattermost-plugin-github may be useful when its README and activity match a concrete workflow.

**Best use cases**

- Not enough metadata yet.

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 177 GitHub stars
- 175 forks
- updated 2026-06-29
- primary language: Go
- 5 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 56/100 |
| stars | 48/100 |
| topics | 63/100 |
| outlook | 54/100 |
| quality | 57/100 |
| recency | 40/100 |
| adoption | 50/100 |
| production | 56/100 |
| usefulness | 58/100 |
| integration | 62/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 0/100 |

---

<sub>🔭 Discovered 2026-06-29 · [View on GitHub](https://github.com/mattermost/mattermost-plugin-github) · [← Back to Misc](./README.md)</sub>
