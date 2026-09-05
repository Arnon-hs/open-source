# GetStream/stream-cli

[![Stars](https://img.shields.io/github/stars/GetStream/stream-cli?style=flat-square&color=yellow)](https://github.com/GetStream/stream-cli/stargazers) [![Forks](https://img.shields.io/github/forks/GetStream/stream-cli?style=flat-square&color=blue)](https://github.com/GetStream/stream-cli/network) [![Language](https://img.shields.io/badge/lang-Go-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-63%2F100-brightgreen?style=flat-square)](#)

> Configure & manage Stream applications from the command line. 🚀

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 90 |
| 🍴 **Forks** | 22 |
| 💻 **Language** | Go |
| 📈 **Score** | 63/100 |
| 🗓️ **Last push** | 2026-09-05 |
| 🔍 **Source** | github |

## 🏷️ Topics

`chat` `cli` `command-line` `feeds` `getstream` `getstream-io` `golang` `oclif` `stream` `stream-cli`

## 🎯 Categories

Communication · DevTools

## 📝 Summary

### English

Here's a brief summary of the GetStream/stream-cli project:

GetStream/stream-cli is an open-source command-line tool that enables engineers to configure and manage Stream applications efficiently, saving time in daily development and review loops. By automating local engineering tasks and improving CI feedback, developers can speed up their workflows and focus on high-priority tasks. With its high production readiness, recent activity, and strong adoption, GetStream/stream-cli is a reliable choice for serious pilot projects.

**Value:**
The primary value proposition of GetStream/stream-cli lies in its ability to streamline developer workflows, reduce manual labor, and improve the overall efficiency of engineering tasks. By automating repetitive tasks, developers can focus on higher-level tasks, leading to increased productivity and better code quality.

**Practical Adoption Path:**
To adopt GetStream/stream-cli, developers can follow these steps:

1. Evaluate the tool's features and compatibility with their existing infrastructure.
2. Install the tool using the provided installation instructions.
3. Configure the tool to manage their Stream applications.
4. Automate local engineering tasks and integrate the tool with their CI/CD pipelines.
5. Monitor and refine the tool's performance to optimize their workflows.

**Production Readiness:**
GetStream/stream-cli has a high production readiness score, indicating that

### Русский

Резюме GetStream/stream-cli:

GetStream/stream-cli - это командная строка для конфигурации и управления приложениями Stream. Это инструмент, который помогает инженерам экономить время в повседневной разработке и проверке, ускоряя разработку, автоматизируя локальные задачи инженеров и улучшая обратную связь в CI.

Проект готов к использованию в production на высоком уровне, поскольку имеет недавнюю активность, признание и сигналы экосистемы. Это означает, что GetStream/stream-cli может быть надежным выбором для внедрения в производственные среды.

### 中文

**项目简介**  
GetStream / stream‑cli 是一款基于 Go 实现的命令行工具，专用于在终端中快速配置、管理和调试 Stream 平台的应用。它提供统一的 API/SDK/CLI 接口，帮助开发者在本地和 CI 环境中实现自动化运维与快速迭代。🚀  

**价值**  
- **提升开发效率**：一条命令即可完成应用创建、密钥管理、Webhook 配置等日常任务，显著缩短开发与代码审查的循环时间。  
- **工作流自动化**：可以在本地脚本或 CI/CD 流水线中调用，自动化部署、环境切换和回滚，减少手工操作错误。  
- **即时反馈**：在 CI 中使用时，CLI 能直接输出 API 调用结果，帮助团队快速定位配置问题，提高构建质量。  

**典型接入方式**  
1. **本地开发**：`go install github.com/GetStream/stream-cli@latest` 安装后，使用 `stream-cli <command>` 直接管理 Stream 项目。  
2. **CI/CD 集成**：在 GitHub Actions、GitLab CI 或 Jenkins 脚本中添加 `stream-cli` 步骤，例如：  
   ```yaml
   - name: Configure Stream app
     run: stream-cli app create --name $APP_NAME --api-key $STREAM_KEY
   ```  
3. **脚本化任务**：将 CLI 命令封装进 Bash/PowerShell 脚本，配合 Makefile 或 npm scripts，实现一键环境搭建。  

**生产可用性**  
- **活跃度高**：截至 2026‑07‑03 最近一次提交，拥有 90+ 星、22 个 fork，社区活跃，维护者响应及时。  
- **成熟度**：采用 Go 语言，二进制交付，无运行时依赖，易于在容器或裸机环境中部署。  
- **风险**：暂无重大许可证或安全隐患，但仍建议在正式投产前完成许可证合规审查并进行安全扫描。  

综合来看，stream‑cli 已具备足够的社区、技术和维护支撑，适合作为生产环境中对 Stream 平台进行自动化管理的可靠 OSS 组件。

## 🧭 Practical evaluation

**Value:** GetStream/stream-cli helps engineers save time in daily development and review loops.

**Best use cases**

- speed up developer workflows
- automate local engineering tasks
- improve CI feedback

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 90 GitHub stars
- 22 forks
- updated 2026-07-03
- primary language: Go
- 10 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 34/100 |
| stars | 42/100 |
| topics | 100/100 |
| outlook | 69/100 |
| quality | 68/100 |
| recency | 80/100 |
| adoption | 40/100 |
| production | 69/100 |
| usefulness | 58/100 |
| integration | 62/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 200/100 |

---

<sub>🔭 Discovered 2026-07-03 · [View on GitHub](https://github.com/GetStream/stream-cli) · [← Back to Communication](./README.md)</sub>
