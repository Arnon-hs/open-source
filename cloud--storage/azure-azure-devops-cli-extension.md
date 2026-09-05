# Azure/azure-devops-cli-extension

[![Stars](https://img.shields.io/github/stars/Azure/azure-devops-cli-extension?style=flat-square&color=yellow)](https://github.com/Azure/azure-devops-cli-extension/stargazers) [![Forks](https://img.shields.io/github/forks/Azure/azure-devops-cli-extension?style=flat-square&color=blue)](https://github.com/Azure/azure-devops-cli-extension/network) [![Language](https://img.shields.io/badge/lang-Python-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-72%2F100-brightgreen?style=flat-square)](#)

> Azure DevOps Extension for Azure CLI

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 675 |
| 🍴 **Forks** | 268 |
| 💻 **Language** | Python |
| 📈 **Score** | 72/100 |
| 🗓️ **Last push** | 2026-09-05 |
| 🔍 **Source** | github |

## 🏷️ Topics

`agile` `artifacts` `azure` `azure-cli` `azure-cli-extension` `azure-devops` `azure-devops-extension` `boards` `cicd` `command-line` `command-line-tool` `devops`

## 🎯 Categories

Cloud & Storage · DevTools · DevOps/Infra

## 📝 Summary

### English

**Summary**  
Azure DevOps CLI Extension (azure‑devops‑cli‑extension) adds first‑class Azure DevOps commands to the Azure CLI, letting engineers manage pipelines, repos, work items and other DevOps resources directly from their terminal. Built in Python, the project is actively maintained (last update 2026‑05‑14), has strong community traction (≈675 ★, 268 forks) and clear API/SDK exposure, making it a solid candidate for production use.

**Value**  
The extension streamlines daily development cycles by letting developers script and automate common Azure DevOps tasks—creating work items, triggering builds, querying test results, etc.—without leaving the CLI. This reduces context switching, accelerates feedback loops in CI/CD pipelines, and enables reproducible, version‑controlled engineering workflows.

**Adoption Path**  
1. **Install** the extension with `az extension add --name azure-devops`.  
2. **Configure** a service connection (`az devops configure --defaults organization=<org> project=<project>`).  
3. **Integrate** the new `az devops` commands into existing scripts, CI jobs, or local tooling to replace manual portal actions or ad‑hoc `curl` calls.  
4. **Validate** in a staging environment, then roll out to developer workstations and CI agents.

**Production Readiness**  
The project shows high production readiness: recent commits, active issue handling, and a healthy adoption signal from the Azure ecosystem. While the license and security posture still need a final review, the combination of frequent updates, robust community support, and clear integration points makes it suitable for a serious pilot in production environments.

### Русский

**Azure/azure-devops-cli-extension** — это официальное расширение Azure CLI, позволяющее управлять Azure DevOps напрямую из командной строки. Оно ускоряет ежедневные циклы разработки и обзора кода, автоматизируя локальные задачи (создание и управление Work Items, пайплайнами, репозиториями) и улучшая обратную связь в CI. Проект имеет высокую готовность к production: активные коммиты, более 600 звёзд, широкое принятие в сообществе и стабильный Python‑стек, что делает его надёжным выбором для пилотного внедрения в инженерные процессы.

### 中文

**项目简介**  
Azure/azure-devops-cli-extension 是为 Azure CLI 提供的 Azure DevOps 扩展，使用 Python 实现，可让开发者在命令行中直接管理 Azure DevOps 资源和流水线。

**价值**  
- **提升效率**：在本地终端即可完成工作项、构建、发布等日常操作，省去切换到 Web UI 的时间。  
- **自动化**：配合脚本或 CI/CD 流程，可实现代码审查、构建触发、部署批准等任务的全链路自动化。  
- **一致的开发体验**：统一使用 Azure CLI，降低学习成本，便于在多项目、多团队间复用。

**典型接入方式**  
1. **安装**：`az extension add --name azure-devops`（或通过 `pip install azure-devops` 手动安装）。  
2. **配置**：使用 `az devops configure --defaults organization=https://dev.azure.com/YourOrg project=YourProject` 设置默认组织和项目。  
3. **使用**：通过 `az devops <subcommand>`（如 `az devops work item create`、`az pipelines run`）在脚本或 CI 中调用，或直接在终端交互使用。  

**生产可用性**  
- **活跃度**：截至 2026‑05‑14 最近一次提交，拥有 675 ⭐、268 🍴，15 个主题标签，社区活跃。  
- **成熟度**：代码基于 Python，遵循 Azure CLI 扩展规范，具备完整的 API/SDK 调用封装，易于审计和二次集成。  
- **风险**：目前未发现重大元数据或许可证冲突，仍需完成安全审计和维护者确认。整体来看，已具备在生产环境中进行试点或正式使用的条件。

## 🧭 Practical evaluation

**Value:** Azure/azure-devops-cli-extension helps engineers save time in daily development and review loops.

**Best use cases**

- speed up developer workflows
- automate local engineering tasks
- improve CI feedback

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 675 GitHub stars
- 268 forks
- updated 2026-05-14
- primary language: Python
- 15 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 61/100 |
| stars | 60/100 |
| topics | 100/100 |
| outlook | 78/100 |
| quality | 77/100 |
| recency | 80/100 |
| adoption | 60/100 |
| production | 73/100 |
| usefulness | 74/100 |
| integration | 62/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 300/100 |

---

<sub>🔭 Discovered 2026-05-14 · [View on GitHub](https://github.com/Azure/azure-devops-cli-extension) · [← Back to Cloud--storage](./README.md)</sub>
