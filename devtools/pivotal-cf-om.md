# pivotal-cf/om

[![Stars](https://img.shields.io/github/stars/pivotal-cf/om?style=flat-square&color=yellow)](https://github.com/pivotal-cf/om/stargazers) [![Forks](https://img.shields.io/github/forks/pivotal-cf/om?style=flat-square&color=blue)](https://github.com/pivotal-cf/om/network) [![Language](https://img.shields.io/badge/lang-Go-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-53%2F100-brightgreen?style=flat-square)](#)

> General command line utility for working with VMware Tanzu Operations Manager

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 137 |
| 🍴 **Forks** | 112 |
| 💻 **Language** | Go |
| 📈 **Score** | 53/100 |
| 🗓️ **Last push** | 2026-08-24 |
| 🔍 **Source** | github |

## 🏷️ Topics

`cli` `golang` `hacktoberfest` `ops-manager`

## 🎯 Categories

DevTools

## 📝 Summary

### English

**Brief Summary (2‑3 sentences)**  
pivotal‑cf/om is a Go‑based command‑line tool that streamlines interaction with VMware Tanzu Operations Manager, letting engineers script common tasks, automate local workflows, and integrate Ops Manager actions into CI pipelines. With 137 GitHub stars and recent activity, it offers a lightweight, extensible way to accelerate development and review cycles for Tanzu‑based projects.

**Value**  
- **Time savings** – By exposing Ops Manager’s API through a simple CLI, developers can replace manual UI clicks with reproducible scripts, cutting down repetitive setup and teardown work.  
- **Automation‑ready** – The tool’s output is machine‑parseable, making it easy to embed in CI/CD pipelines for continuous feedback on infrastructure changes.  
- **Consistent environments** – Teams can version‑control the exact OM commands used in local development, ensuring that every engineer works against the same Ops Manager configuration.

**Practical Adoption Path**  
1. **Pilot** – Clone the repository, run `om --version` to confirm the binary works on your OS, and try the “quick‑start” commands from the README against a non‑production Ops Manager instance.  
2. **Integrate** – Wrap the needed `om` calls in shell scripts or Makefile targets and add them to your existing developer tooling (e.g., `make deploy‑cf`).  
3. **CI Hook** – Add the binary to your CI image (Dockerfile or CI cache) and use it in pipeline stages that provision or validate Tanzu resources.  
4. **Governance** – Pin the version in a `go.mod`‑style lockfile or use a checksum‑verified release to avoid drift across environments.

**Production Readiness**  
- **Maturity** – Medium. The project is actively maintained (last commit 2026‑05‑12) and has a modest community (137 stars, 112 forks), but it is primarily positioned for prototyping and internal tooling.  
- **Dependencies** – Written in Go with a single binary artifact, which simplifies deployment, though you should audit any external SDKs it bundles for security updates.  
- **Risks** – License and long‑term maintainer commitment need verification; perform a security scan of the binary and confirm that the repository’s contribution guidelines align with your organization’s policies before production rollout.  

Overall, om can be adopted quickly for development and CI automation, and with proper vetting it can evolve into a reliable component of a production Tanzu Ops Manager workflow.

### Русский

pivotal‑cf/om — это CLI‑утилита на Go для управления VMware Tanzu Operations Manager, позволяющая инженерам автоматизировать типовые задачи (настройка окружения, деплой, проверка статуса) и ускорить циклы разработки и CI‑feedback. Проект уже имеет 137 звёзд, активно поддерживается (обновление – 12 мая 2026) и подходит для прототипов и внутренних workflow, однако перед выводом в продакшн рекомендуется проверить лицензию, безопасность зависимостей и наличие постоянных мейнтейнеров.

### 中文

**项目简介**  
pivotal‑cf/om 是一款基于 Go 实现的通用命令行工具，专用于与 VMware Tanzu Operations Manager（原 Pivotal Cloud Foundry Ops Manager）交互。它提供 API/SDK/CLI 封装，帮助工程师在本地或 CI 环境中快速完成部署、配置、升级等日常运维任务。

**价值**  
- **提升效率**：通过脚本化的 CLI，开发者可以在几秒钟内完成原本需要手动点击的 Ops Manager 操作，显著缩短开发、测试和代码审查的循环时间。  
- **自动化支持**：天然适配 CI/CD 流水线，可在构建、部署阶段自动执行 BOSH 部署、产品导入、证书管理等步骤，提升反馈速度并降低人为错误。  
- **统一入口**：将 Ops Manager 的 REST API 封装为一致的命令行语法，降低学习成本，便于团队内部共享和复用。

**典型接入方式**  
1. **本地开发**：在开发机器上 `go install github.com/pivotal-cf/om/...`，或直接下载预编译的二进制文件；随后通过环境变量或 `om login` 配置 Ops Manager 地址、用户名、密码或 UAA token，即可在终端执行 `om configure-product`、`om deploy-product` 等子命令。  
2. **CI/CD 集成**：在 Jenkins、GitHub Actions、GitLab CI 等流水线中添加步骤，使用 Docker 镜像 `pivotalcf/om`（或自行构建）运行相应命令；通过安全凭证（Vault、K8s Secret）注入登录信息，实现全自动化部署。  
3. **脚本化工作流**：将常用操作封装为 Bash/PowerShell 脚本或 Makefile 目标，配合 `om` 的 `--json` 输出进行结果解析和后续处理。

**生产可用性**  
- **成熟度**：项目已有 137 星、112 Fork，最近一次提交于 2026‑05‑12，活跃度尚可。代码基于 Go，易于审计和二进制交付。  
- **适用场景**：适合原型开发、内部工具链以及对 Ops Manager 进行频繁迭代的团队；在生产环境使用前，建议完成以下检查：  
  - 评估依赖的第三方库是否仍受维护（尤其是 BOSH、UAA 相关）。  
  - 确认许可证兼容性（项目采用 Apache‑2.0）。  
  - 进行安全审计，确保凭证不在日志或 CI 配置中泄露。  
- **风险**：缺乏官方长期维护承诺，若在关键业务中使用，需要自行制定故障恢复和版本锁定策略。  

总体而言，pivotal-cf/om 在提升 Tanzu Ops Manager 工作流自动化方面价值明显，接入成本低，适合作为内部 CI/CD 的加速器；在生产环境使用时，只要做好依赖、许可证和安全的审查，即可达到中等可靠性水平。

## 🧭 Practical evaluation

**Value:** pivotal-cf/om helps engineers save time in daily development and review loops.

**Best use cases**

- speed up developer workflows
- automate local engineering tasks
- improve CI feedback

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** Medium: useful for prototypes or internal workflows, with dependency and maintenance checks before production.

**Quality signals**

- 137 GitHub stars
- 112 forks
- updated 2026-05-12
- primary language: Go
- 4 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 51/100 |
| stars | 46/100 |
| topics | 50/100 |
| outlook | 45/100 |
| quality | 49/100 |
| recency | 20/100 |
| adoption | 47/100 |
| production | 48/100 |
| usefulness | 58/100 |
| integration | 62/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 100/100 |

---

<sub>🔭 Discovered 2026-05-12 · [View on GitHub](https://github.com/pivotal-cf/om) · [← Back to DevTools](./README.md)</sub>
