# databricks/cli

[![Stars](https://img.shields.io/github/stars/databricks/cli?style=flat-square&color=yellow)](https://github.com/databricks/cli/stargazers) [![Forks](https://img.shields.io/github/forks/databricks/cli?style=flat-square&color=blue)](https://github.com/databricks/cli/network) [![Language](https://img.shields.io/badge/lang-Go-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-65%2F100-brightgreen?style=flat-square)](#)

> Databricks CLI

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 335 |
| 🍴 **Forks** | 167 |
| 💻 **Language** | Go |
| 📈 **Score** | 65/100 |
| 🗓️ **Last push** | 2026-05-11 |
| 🔍 **Source** | github |

## 🏷️ Topics

`command-line-interface` `databricks`

## 🎯 Categories

DevTools · Data

## 📝 Summary

### English

**Brief summary**  
The Databricks CLI is an open‑source command‑line tool (written in Go) that lets engineers interact with Databricks workspaces from their local terminals. By scripting common tasks—such as job submission, secret management, and cluster control—it speeds up daily development, automates routine engineering chores, and provides faster feedback in CI pipelines. With ~335 stars and recent activity, it’s a mature yet still community‑driven utility suitable for prototype or internal use.

**Value**  
- **Time savings:** One‑line commands replace manual UI clicks, accelerating feature iteration and code review cycles.  
- **Automation:** The CLI can be embedded in scripts or CI jobs to provision resources, run notebooks, and manage artifacts, delivering consistent, repeatable workflows.  
- **Developer experience:** Provides a familiar shell interface that integrates with existing tooling (git, make, Docker), reducing context switching.

**Practical adoption path**  
1. **Proof‑of‑concept:** Clone the repo, run the built‑in `databricks --version` check, and follow the README to configure a test workspace token.  
2. **Pilot script:** Replace a small, manual step (e.g., uploading a notebook or triggering a job) with a CLI call in a local script or CI stage.  
3. **Expand coverage:** Gradually migrate other repetitive tasks (secret handling, cluster start/stop) into reusable CLI‑based scripts, adding unit tests and documentation.  
4. **Governance:** Review the license, perform a lightweight security scan of the Go binary, and lock the version in your dependency manifest before promoting to production.

**Production readiness**  
- **Maturity:** Medium – the project is actively maintained (last commit 2026‑05‑11) and has a solid user base, but it is still community‑driven with limited formal support.  
- **Considerations:** Verify the licensing terms, conduct a security audit of the binary and its dependencies, and establish an internal maintainer to monitor upstream updates.  
- **Fit:** Ideal for internal prototypes, developer tooling, and CI automation; with the above checks, it can be hardened for production‑grade pipelines.

### Русский

Databricks CLI — это набор командных утилит на Go, позволяющих инженерам автоматизировать повседневные задачи работы с Databricks, ускорять локальные разработки и получать быстрый фидбэк в CI‑процессах. Для начала интеграции рекомендуется реализовать небольшой proof‑of‑concept, проверив README и базовую работу CLI, после чего оценить зависимости и планировать поддержку. Готовность к production — средняя: инструмент пригоден для прототипов и внутренних пайплайнов, но перед масштабным использованием требуется проверка лицензии, безопасности и наличия активных мейнтейнеров.

### 中文

**价值**  
Databricks CLI 为 Databricks 工作空间提供一套轻量级的命令行工具，能够在本地快速创建、管理和运行笔记本、作业、集群等资源。通过脚本化这些操作，工程师可以显著缩短开发、调试和代码审查的回路，并在 CI/CD 流水线中实现自动化部署和状态校验，从而提升整体开发效率和反馈速度。

**典型接入方式**  
1. **本地安装**：`pip install databricks-cli`（或使用 Go 二进制），在开发机器或 CI 容器中完成。  
2. **身份认证**：在 CI 环境中配置 `DATABRICKS_HOST`、`DATABRICKS_TOKEN` 环境变量；在本地可以通过 `databricks configure --token` 交互式设置。  
3. **脚本化使用**：在 Makefile、bash 脚本或 GitHub Actions 中调用 `databricks workspace import/export`、`databricks jobs create`、`databricks clusters create` 等子命令，实现资源的自动化创建、更新和清理。  
4. **最小化验证**：先在 README 中列出常用命令，写一个 “hello‑world” 工作流（如创建临时集群、运行一个 Notebook），确认 CLI 与组织的 Databricks 实例兼容后，再逐步扩展到完整的 CI/CD 流程。

**生产可用性**  
- **成熟度**：项目已有 335 Stars、167 Forks，最近一次提交在 2026‑05‑11，活跃度尚可。主语言为 Go，二进制体积小，部署成本低。  
- **适用场景**：非常适合原型开发、内部工具链以及 CI 中的自动化任务；在生产环境使用前，需要完成以下检查：  
  1. **许可证合规**：确认项目的开源许可证（Apache‑2.0）符合企业政策。  
  2. **安全审计**：评估依赖的 Go 包是否存在已知漏洞，必要时使用 SCA 工具进行扫描。  
  3. **维护者活跃度**：关注 issue/PR 响应速度，若社区活跃度下降，可考虑内部 fork 并自行维护。  
- **风险等级**：中等。对原型或内部流程使用风险可控；在面向外部客户的生产系统中部署前，建议进行依赖锁定、版本固定以及灾备回滚方案的验证。  

综上，Databricks CLI 是提升 Databricks 开发与运维效率的实用工具，适合作为小规模 PoC 进入企业技术栈，经过上述合规与安全检查后即可在生产环境中安全使用。

## 🧭 Practical evaluation

**Value:** databricks/cli helps engineers save time in daily development and review loops.

**Best use cases**

- speed up developer workflows
- automate local engineering tasks
- improve CI feedback

**Integration notes:** Looks feasible to evaluate, but integration should start with a small proof of concept and README check.

**Production readiness:** Medium: useful for prototypes or internal workflows, with dependency and maintenance checks before production.

**Quality signals**

- 335 GitHub stars
- 167 forks
- updated 2026-05-11
- primary language: Go
- 2 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 56/100 |
| stars | 54/100 |
| topics | 25/100 |
| outlook | 73/100 |
| quality | 68/100 |
| recency | 100/100 |
| adoption | 54/100 |
| production | 74/100 |
| usefulness | 58/100 |
| integration | 62/100 |
| sourceTrust | 100/100 |

---

<sub>🔭 Discovered 2026-05-11 · [View on GitHub](https://github.com/databricks/cli) · [← Back to DevTools](./README.md)</sub>
