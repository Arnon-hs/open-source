# passbolt/go-passbolt-cli

[![Stars](https://img.shields.io/github/stars/passbolt/go-passbolt-cli?style=flat-square&color=yellow)](https://github.com/passbolt/go-passbolt-cli/stargazers) [![Forks](https://img.shields.io/github/forks/passbolt/go-passbolt-cli?style=flat-square&color=blue)](https://github.com/passbolt/go-passbolt-cli/network) [![Language](https://img.shields.io/badge/lang-Go-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-64%2F100-brightgreen?style=flat-square)](#)

> A CLI tool to interact  with Passbolt, a Open source Password Manager for Teams

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 137 |
| 🍴 **Forks** | 31 |
| 💻 **Language** | Go |
| 📈 **Score** | 64/100 |
| 🗓️ **Last push** | 2026-09-05 |
| 🔍 **Source** | github |

## 🏷️ Topics

`cli` `passbolt`

## 🎯 Categories

DevTools

## 📝 Summary

### English

**Summary:** passbolt/go-passbolt-cli is an open-source command-line interface (CLI) tool that enables developers to interact with Passbolt, a team password manager. This tool helps engineers save time by streamlining daily development and review loops, making it easier to automate local engineering tasks and improve continuous integration (CI) feedback. With its medium production readiness, it is suitable for use in prototypes or internal workflows after thorough dependency and maintenance checks.

**Value:** The primary value proposition of passbolt/go-passbolt-cli lies in its ability to speed up developer workflows, automate local engineering tasks, and improve CI feedback. By leveraging this tool, engineers can save time and increase productivity, making it an attractive solution for teams looking to optimize their development processes.

**Practical Adoption Path:** To adopt passbolt/go-passbolt-cli, follow these steps:

1. Evaluate the tool's feasibility by reviewing the README documentation and implementing a small proof of concept.
2. Assess the tool's integration with your existing infrastructure and development workflows.
3. Conduct a thorough review of the tool's dependencies, license, security posture, and maintainers to ensure it meets your project's requirements.
4. Implement the tool in a controlled environment, such as a prototype or internal workflow, to test its effectiveness and identify any potential issues

### Русский

Резюме проекта passbolt/go-passbolt-cli:

passbolt/go-passbolt-cli - это утилита командной строки, предназначенная для взаимодействия с Passbolt - открытым исходным кодом менеджером паролей для команд. Эта утилита помогает инженерам экономить время в повседневных циклах разработки и отзыва, speeding up разработку, автоматизацию локальных задач инженеров и улучшение обратной связи в процессе CI.

Внедрение passbolt/go-passbolt-cli может быть полезно для ускорения разработки и автоматизации локальных задач инженеров. Однако, перед использованием в производстве, необходимо детально проверить зависимости и поддержку.

Проект находится на среднем уровне готовности к производству (Medium), что означает, что он может быть полезен для прототипов или внутренних рабочих процессов, но требует дополнительной проверки и проверки, прежде чем его можно будет использовать в производственном окружении.

### 中文

**项目简介**  
`passbolt/go-passbolt-cli` 是一款用 Go 编写的命令行工具，能够在终端直接与开源密码管理平台 Passbolt 交互，实现密码的查询、创建、更新和删除等常用操作。

**价值**  
- **提升开发效率**：在本地或 CI 环境中快速获取或更新凭证，避免手动复制密码或频繁切换到 Web UI。  
- **自动化工作流**：可在脚本、Makefile 或 CI/CD pipeline 中调用，实现凭证的自动注入、环境准备和安全审计。  
- **团队协作**：通过 Passbolt 的团队共享机制，确保所有成员使用统一、受控的密码库，降低泄露风险。

**典型接入方式**  
1. **本地原型**：在开发机器上 `go install github.com/passbolt/go-passbolt-cli@latest`，配置 Passbolt API Token 与服务器地址后，即可在终端执行 `passbolt-cli get <entry>` 等命令。  
2. **CI/CD 集成**：在构建脚本或 GitHub Actions 中添加步骤，使用已加密的 Passbolt Token（如 GitHub Secrets）调用 CLI，自动把凭证写入环境变量或配置文件。  
3. **脚本化任务**：将常用操作封装为 Bash/PowerShell 脚本或 Makefile 目标，例如 `make db-setup` 里调用 `passbolt-cli create db-password`。

**生产可用性**  
- **成熟度**：当前得分 67/100，GitHub 137 星、31 Fork，最近一次提交为 2026‑07‑02，活跃度尚可。适合作为内部原型或非关键业务的自动化工具。  
- **准备度**：属于 **Medium** 级别。投入生产前建议：  
  1. **安全审计**：确认 Passbolt 服务器的 TLS 配置、API Token 权限以及 CLI 本身的依赖安全性。  
  2. **依赖管理**：锁定 Go module 版本，使用 vendoring 或 Go proxy，防止供应链风险。  
  3. **维护计划**：关注项目的后续更新或考虑自行 fork 并维护关键 bug。  

总体而言，`go-passbolt-cli` 能显著简化开发者在本地和 CI 环境中对密码的获取与管理，是提升工程效率的实用工具，只要做好安全和依赖审查，即可在生产环境中安全使用。

## 🧭 Practical evaluation

**Value:** passbolt/go-passbolt-cli helps engineers save time in daily development and review loops.

**Best use cases**

- speed up developer workflows
- automate local engineering tasks
- improve CI feedback

**Integration notes:** Looks feasible to evaluate, but integration should start with a small proof of concept and README check.

**Production readiness:** Medium: useful for prototypes or internal workflows, with dependency and maintenance checks before production.

**Quality signals**

- 137 GitHub stars
- 31 forks
- updated 2026-07-02
- primary language: Go
- 2 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 38/100 |
| stars | 46/100 |
| topics | 25/100 |
| outlook | 66/100 |
| quality | 58/100 |
| recency | 80/100 |
| adoption | 43/100 |
| production | 66/100 |
| usefulness | 74/100 |
| integration | 62/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 100/100 |

---

<sub>🔭 Discovered 2026-07-02 · [View on GitHub](https://github.com/passbolt/go-passbolt-cli) · [← Back to DevTools](./README.md)</sub>
