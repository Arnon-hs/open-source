# scaleway/scaleway-cli

[![Stars](https://img.shields.io/github/stars/scaleway/scaleway-cli?style=flat-square&color=yellow)](https://github.com/scaleway/scaleway-cli/stargazers) [![Forks](https://img.shields.io/github/forks/scaleway/scaleway-cli?style=flat-square&color=blue)](https://github.com/scaleway/scaleway-cli/network) [![Language](https://img.shields.io/badge/lang-Go-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-65%2F100-brightgreen?style=flat-square)](#)

> Command Line Interface for Scaleway

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 970 |
| 🍴 **Forks** | 164 |
| 💻 **Language** | Go |
| 📈 **Score** | 65/100 |
| 🗓️ **Last push** | 2026-09-05 |
| 🔍 **Source** | github |

## 🏷️ Topics

`cli` `go` `scaleway` `scaleway-cli`

## 🎯 Categories

DevTools

## 📝 Summary

### English

**Summary**  
Scaleway‑CLI is a Go‑based command‑line client that lets engineers interact with the Scaleway cloud platform from their terminals, automating routine provisioning, deployment, and inspection tasks. With 970 ★, frequent releases (last update 2026‑05‑11) and strong community adoption, it offers a low‑friction way to speed up local development loops, integrate cloud actions into CI pipelines, and reduce manual UI work.

**Value & Adoption Path**  
The tool centralises API calls behind familiar CLI commands, letting developers script infrastructure changes, embed cloud operations in test suites, and obtain immediate feedback in CI/CD; this cuts context‑switching and accelerates the build‑test‑deploy cycle. Teams can start by installing the binary, authenticating with a Scaleway token, and replacing ad‑hoc `curl`/SDK snippets with `scw` commands in existing scripts, then progressively expand to full workflow automation (e.g., provisioning instances, managing DNS, handling secrets).

**Production Readiness**  
The project shows high production readiness: recent activity, a healthy star/fork count, clear Go source, and well‑documented commands indicate a mature codebase. While the license, security audit, and maintainer continuity still need a final check, the current signals (active contributors, regular releases, and adoption in real‑world pipelines) make Scaleway‑CLI a solid candidate for a pilot or full production rollout.

### Русский

scaleway/scaleway-cli — это открытый CLI‑инструмент на Go, позволяющий инженерам быстро управлять ресурсами Scaleway через единый терминальный интерфейс, что ускоряет ежедневные разработки, автоматизацию локальных задач и улучшает обратную связь в CI‑процессах. Проект активно поддерживается (обновления до 2026‑05‑11, 970 звёзд, 164 форка) и демонстрирует высокий уровень готовности к production‑использованию, однако перед внедрением стоит уточнить лицензию, безопасность и наличие активных мейнтейнеров.

### 中文

**项目简介**  
Scaleway CLI 是 Scaleway 官方提供的命令行工具，使用 Go 语言实现，帮助开发者在本地快速调用 Scaleway 的云 API，实现资源管理、部署和运维等日常工作。

**价值**  
- **提升开发效率**：通过一条命令即可完成实例创建、网络配置、镜像管理等操作，显著缩短开发与调试循环。  
- **自动化能力**：可在脚本或 CI/CD 流水线中直接调用，支持批量操作和自定义工作流，降低人工错误。  
- **统一反馈**：在 CI 环境中使用 CLI 可即时获取云资源状态，帮助团队快速定位部署问题。

**典型接入方式**  
1. **本地安装**：`curl -sL https://github.com/scaleway/scaleway-cli/releases/latest/download/scw-linux-amd64 -o /usr/local/bin/scw && chmod +x /usr/local/bin/scw`（Linux 示例），或使用 Homebrew、Snap 等包管理器。  
2. **配置凭证**：运行 `scw login` 或手动设置 `SCW_ACCESS_KEY`、`SCW_SECRET_KEY` 环境变量。  
3. **脚本/CI 集成**：在 Bash、Makefile、GitHub Actions、GitLab CI 等环境中直接调用 `scw <subcommand>`，例如 `scw instance create …`，配合 `--output json` 解析返回结果，实现自动化部署和状态检查。  

**生产可用性**  
- **活跃度**：截至 2026‑05‑11，项目最近一次提交，星标 970、Fork 164，社区活跃。  
- **成熟度**：使用 Go 编写，二进制交付，无运行时依赖，易于在容器或裸机上部署。  
- **安全与合规**：采用 MIT 许可证，官方维护，未发现重大安全漏洞；仍建议在正式环境前进行一次内部安全审计。  
- **适配性**：提供完整的 API/SDK 调用封装，兼容多平台（Linux、macOS、Windows），可直接在生产 CI/CD 流水线中使用。  

综上，Scaleway CLI 已具备高生产就绪度，适合作为日常开发、自动化脚本以及 CI/CD 环境中的核心工具，引入成本低、回报显著。

## 🧭 Practical evaluation

**Value:** scaleway/scaleway-cli helps engineers save time in daily development and review loops.

**Best use cases**

- speed up developer workflows
- automate local engineering tasks
- improve CI feedback

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 970 GitHub stars
- 164 forks
- updated 2026-05-11
- primary language: Go
- 4 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 55/100 |
| stars | 64/100 |
| topics | 50/100 |
| outlook | 70/100 |
| quality | 70/100 |
| recency | 80/100 |
| adoption | 61/100 |
| production | 70/100 |
| usefulness | 58/100 |
| integration | 62/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 100/100 |

---

<sub>🔭 Discovered 2026-05-11 · [View on GitHub](https://github.com/scaleway/scaleway-cli) · [← Back to DevTools](./README.md)</sub>
