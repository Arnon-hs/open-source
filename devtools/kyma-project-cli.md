# kyma-project/cli

[![Stars](https://img.shields.io/github/stars/kyma-project/cli?style=flat-square&color=yellow)](https://github.com/kyma-project/cli/stargazers) [![Forks](https://img.shields.io/github/forks/kyma-project/cli?style=flat-square&color=blue)](https://github.com/kyma-project/cli/network) [![Language](https://img.shields.io/badge/lang-Go-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-51%2F100-brightgreen?style=flat-square)](#)

> Simple set of commands to manage a Kyma cluster

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 121 |
| 🍴 **Forks** | 124 |
| 💻 **Language** | Go |
| 📈 **Score** | 51/100 |
| 🗓️ **Last push** | 2026-08-24 |
| 🔍 **Source** | github |

## 🏷️ Topics

`cli` `kyma`

## 🎯 Categories

DevTools

## 📝 Summary

### English

**Brief Summary (2‑3 sentences)**  
Kyma CLI is a lightweight, Go‑based command‑line tool that streamlines common operations on a Kyma cluster—such as provisioning, component management, and local development tasks. With over a hundred stars and recent activity, it offers a quick way for engineers to accelerate daily development and review loops while keeping the cluster state in sync.

**Value**  
- **Time savings:** Automates repetitive cluster actions (installing modules, syncing resources, running local tests), reducing manual CLI gymnastics.  
- **Consistent workflows:** Provides a single, versioned interface that can be scripted in CI pipelines, improving feedback speed and reproducibility.  
- **Developer experience:** Enables local Kyma setups and rapid iteration, which is especially valuable for teams building extensions or micro‑services on top of Kyma.

**Practical Adoption Path**  
1. **Proof‑of‑concept:** Clone the repo, run the CLI against a sandbox Kyma cluster, and verify that the commands you need (e.g., `kyma install`, `kyma deploy`) work as expected.  
2. **README validation:** Follow the official README to set up the binary and test basic commands; this also surfaces any missing dependencies.  
3. **Pilot integration:** Wrap the required CLI calls in simple scripts or Makefile targets and incorporate them into a feature branch CI job.  
4. **Scale up:** Once the pilot proves stable, replace ad‑hoc scripts across the team with the Kyma CLI, and document the standard usage patterns in your internal wiki.

**Production Readiness**  
- **Maturity:** Medium – the project is actively maintained (last commit on 2026‑05‑12) and has a modest but healthy community (≈120 ★, 124 forks).  
- **Suitability:** Ideal for prototypes, internal tooling, and CI automation; it can be used in production for non‑critical workflows after a brief dependency audit.  
- **Considerations before production:** Verify the license compatibility, run a security scan of the binary, and confirm that the maintainers are responsive to issues. Once these checks are done, the CLI can be safely promoted to production environments for routine Kyma cluster management.

### Русский

**Kyma‑project/cli** — это набор простых команд‑строк на Go, позволяющих инженерам быстро управлять кластером Kyma, автоматизировать локальные задачи и ускорять CI‑feedback. Для внедрения рекомендуется начать с небольшого proof‑of‑concept: установить CLI, проверить основные команды и убедиться в совместимости с текущими процессами разработки, а затем расширять использование в прототипах и внутренних workflow. Готовность к production — средняя: инструмент уже активно поддерживается (обновление 2026‑05‑12, 121 ★, 124 fork), но перед выводом в продакшн стоит провести окончательную проверку лицензии, безопасности и стабильности зависимостей.

### 中文

**项目简介**  
Kyma CLI（`kyma-project/cli`）是一套轻量级的命令行工具，提供创建、删除、升级以及本地调试 Kyma 集群的常用操作，帮助开发者在本地或 CI 环境中快速搭建和管理 Kyma。

**价值**  
- **提升开发效率**：通过一条命令即可完成集群的启动、模块部署和日志查看，显著缩短每日开发与代码审查的循环时间。  
- **自动化支持**：可在脚本或 CI/CD 流水线中调用，实现本地工程任务的自动化和持续反馈。  
- **一致性与可重复性**：统一的 CLI 界面保证不同成员、不同环境下的操作行为保持一致，降低因手工步骤导致的错误。

**典型接入方式**  
1. **本地原型**：在开发机器上 `go install github.com/kyma-project/cli@latest`，随后在项目根目录执行 `kyma init`、`kyma deploy` 等命令，即可快速启动本地 Kyma 环境。  
2. **CI/CD 集成**：在 CI 脚本（如 GitHub Actions、GitLab CI）中添加安装步骤，然后使用 `kyma install`、`kyma test` 等子命令完成集群的临时搭建、测试运行和清理。  
3. **Proof‑of‑Concept**：先在一个小型仓库或实验分支中编写 README 示例，验证 CLI 与现有工作流的兼容性，再逐步推广到全项目。

**生产可用性**  
- **成熟度**：当前在 GitHub 上拥有 121 ⭐、124 fork，最近一次更新（2026‑05‑12）显示仍在活跃维护。  
- **适用场景**：适合原型开发、内部工具链以及对 Kyma 集群有快速迭代需求的团队。直接用于面向外部用户的生产环境仍需进行依赖审计、许可证合规以及安全审查。  
- **准备度**：属于 **中等**（Medium）级别——在完成依赖、维护者和安全评估后，可在内部生产环境中使用；若要对外提供服务，建议增加自动化测试、灾备方案以及升级策略。

## 🧭 Practical evaluation

**Value:** kyma-project/cli helps engineers save time in daily development and review loops.

**Best use cases**

- speed up developer workflows
- automate local engineering tasks
- improve CI feedback

**Integration notes:** Looks feasible to evaluate, but integration should start with a small proof of concept and README check.

**Production readiness:** Medium: useful for prototypes or internal workflows, with dependency and maintenance checks before production.

**Quality signals**

- 121 GitHub stars
- 124 forks
- updated 2026-05-12
- primary language: Go
- 2 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 52/100 |
| stars | 44/100 |
| topics | 25/100 |
| outlook | 43/100 |
| quality | 45/100 |
| recency | 20/100 |
| adoption | 47/100 |
| production | 47/100 |
| usefulness | 58/100 |
| integration | 62/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 100/100 |

---

<sub>🔭 Discovered 2026-05-12 · [View on GitHub](https://github.com/kyma-project/cli) · [← Back to DevTools](./README.md)</sub>
