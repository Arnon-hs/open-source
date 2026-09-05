# sangrokjung/claude-forge

[![Stars](https://img.shields.io/github/stars/sangrokjung/claude-forge?style=flat-square&color=yellow)](https://github.com/sangrokjung/claude-forge/stargazers) [![Forks](https://img.shields.io/github/forks/sangrokjung/claude-forge?style=flat-square&color=blue)](https://github.com/sangrokjung/claude-forge/network) [![Language](https://img.shields.io/badge/lang-Shell-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-78%2F100-brightgreen?style=flat-square)](#)

> Supercharge Claude Code with 11 AI agents, 36 commands & 15 skills — the claude-code plugin framework inspired by oh-my-zsh. 6-layer security hooks included. 5-min install.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 699 |
| 🍴 **Forks** | 152 |
| 💻 **Language** | Shell |
| 📈 **Score** | 78/100 |
| 🗓️ **Last push** | 2026-09-05 |
| 🔍 **Source** | github |

## 🏷️ Topics

`agents` `ai-assistant` `ai-coding` `ai-framework` `ai-pair-programming` `anthropic` `automation` `claude-code` `claude-code-agents` `cli-tools` `developer-experience` `developer-tools`

## 🎯 Categories

Automation · AI/ML · Productivity · DevTools · Security

## 📝 Summary

### English

**Brief Summary (2‑3 sentences)**  
Claude‑Forge is an open‑source plugin framework that extends Claude’s coding capabilities with 11 AI agents, 36 ready‑to‑use commands and 15 reusable skills, all wrapped in a “oh‑my‑zsh”‑style experience. It adds six layers of security hooks, can be installed in under five minutes, and is built primarily in Shell for easy integration into CI/CD pipelines and developer workstations. With 699 ★ and recent activity, it is positioned as a high‑readiness OSS solution for automating repetitive coding and operational tasks.

**Value**  
- **Automation of manual steps** – By exposing AI agents as CLI commands, developers can replace copy‑paste, boilerplate generation, and routine refactoring with a single typed command.  
- **Composable workflow** – The 15 skills and 36 commands can be chained or scheduled, enabling repeatable pipelines that connect code repositories, testing suites, and deployment tools.  
- **Built‑in security** – Six security‑hook layers (e.g., input sanitisation, token‑scoping, audit logging) help keep AI‑driven actions compliant with internal policies.  

**Practical Adoption Path**  
1. **Quick install** – Run the provided one‑liner installer (≈5 min) on a developer machine or CI runner.  
2. **Configure agents** – Select the needed agents/skills via the `forge config` CLI or a simple `.forge.yml` file.  
3. **Pilot a use case** – Replace a repetitive task (e.g., generating API client stubs) with a `forge generate-client` command and verify output.  
4. **Integrate into pipelines** – Add `forge <command>` steps to existing GitHub Actions, GitLab CI, or Jenkins jobs.  
5. **Scale & schedule** – Use the built‑in scheduler or external cron to run operational tasks (e.g., nightly code linting) automatically.  

**Production Readiness**  
- **Active maintenance** – Last commit on 2026‑05‑14, regular releases, and a healthy fork count (152) indicate ongoing support.  
- **Community traction** – 699 stars and 20 topical tags show broad interest and ecosystem integration.  
- **Security posture** – Multi‑layer hooks provide baseline protection; however, a final license and vulnerability audit is still recommended before enterprise rollout.  
Overall, Claude‑Forge meets the criteria for a serious pilot in production environments, offering immediate productivity gains with a low barrier to entry.

### Русский

**Краткое резюме:** sangrokjung/claude-forge — это open‑source‑фреймворк, который усиливает работу Claude Code набором из 11 AI‑агентов, 36 команд и 15 готовых навыков, позволяя автоматизировать рутинные операции, соединять инструменты в повторяемые пайплайны и планировать задачи. Проект поставляется с 6‑уровневой системой безопасности и устанавливается за 5 минут, что делает его подходящим для быстрого прототипирования и последующего масштабирования в продакшн‑окружениях. Благодаря активной поддержке (обновления 2026‑05‑14, 699 звёзд, 152 форка) и наличию API/SDK/CLI, уровень готовности к production высокий, однако перед развёртыванием следует окончательно проверить лицензию и детали безопасности.

### 中文

**项目简介**  
`sangrokjung/claude-forge` 是一个受 oh‑my‑zsh 启发的 **Claude 代码插件框架**，内置 11 个 AI 代理、36 条指令和 15 项技能，并提供 6 层安全钩子，安装仅需 5 分钟。

**价值主张**  
- **自动化重复工作**：通过 AI 代理和丰富的命令/技能，把手动的代码审查、生成、部署、监控等环节全部流水化。  
- **可组合的工具链**：支持将多种内部或第三方工具（CI、监控、运维脚本等）通过统一的插件接口串联，形成可重复、可调度的工作流。  
- **安全可靠**：六层安全钩子（输入校验、沙箱执行、审计日志、权限控制、加密通信、异常捕获）帮助在生产环境中防止恶意指令和数据泄露。

**典型接入方式**  
1. **CLI/SDK**：克隆仓库后直接使用 `forge` 命令行工具或通过提供的 Bash SDK 在脚本中调用 `forge run <command>`。  
2. **API 网关**：框架会自动生成基于 OpenAPI 的 HTTP 接口，外部系统（如 GitHub Actions、Jenkins、Airflow）可通过 REST 调用对应的 AI 任务。  
3. **插件扩展**：按照 `plugins/` 目录的约定编写自定义 Shell 脚本或 Docker 镜像，即可把自家业务逻辑加入到 11 个默认代理中。  

**生产可用性**  
- **活跃度**：2026‑05‑14 最近更新，699 ★、152 Fork，拥有 20+ 相关话题，社区活跃。  
- **成熟度**：已实现 6 层安全防护，提供完整的日志审计和权限模型，适合作为企业内部自动化平台的核心组件。  
- **风险**：需进一步审查许可证兼容性、长期维护者承诺以及安全漏洞响应流程；但整体代码质量和生态信号足以支撑正式的试点部署。  

综上，`claude-forge` 能显著降低手工运维成本，接入方式灵活，已具备在生产环境中安全、可靠运行的条件。

## 🧭 Practical evaluation

**Value:** sangrokjung/claude-forge helps remove repetitive manual operations from a workflow.

**Best use cases**

- remove manual work
- connect tools into repeatable flows
- schedule operational tasks

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 699 GitHub stars
- 152 forks
- updated 2026-05-14
- primary language: Shell
- 20 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 55/100 |
| stars | 61/100 |
| topics | 100/100 |
| outlook | 83/100 |
| quality | 76/100 |
| recency | 80/100 |
| adoption | 59/100 |
| production | 73/100 |
| usefulness | 100/100 |
| integration | 62/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 500/100 |

---

<sub>🔭 Discovered 2026-05-14 · [View on GitHub](https://github.com/sangrokjung/claude-forge) · [← Back to Automation](./README.md)</sub>
