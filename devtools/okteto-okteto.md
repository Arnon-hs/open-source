# okteto/okteto

[![Stars](https://img.shields.io/github/stars/okteto/okteto?style=flat-square&color=yellow)](https://github.com/okteto/okteto/stargazers) [![Forks](https://img.shields.io/github/forks/okteto/okteto?style=flat-square&color=blue)](https://github.com/okteto/okteto/network) [![Language](https://img.shields.io/badge/lang-Go-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-67%2F100-brightgreen?style=flat-square)](#)

> Develop your applications directly in your Kubernetes Cluster

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 3.5k |
| 🍴 **Forks** | 315 |
| 💻 **Language** | Go |
| 📈 **Score** | 67/100 |
| 🗓️ **Last push** | 2026-08-24 |
| 🔍 **Source** | github |

## 🏷️ Topics

`cloud-native` `cloud-native-developers` `debug` `developer-tools` `development` `docker` `hacktoberfest` `helm` `kubernetes` `okteto`

## 🎯 Categories

DevTools · DevOps/Infra

## 📝 Summary

### English

**Brief Summary (2‑3 sentences)**  
Okteto (okteto/okteto) lets developers write, test, and debug code directly inside their Kubernetes clusters, turning the cluster into a live development environment. By syncing local changes to the cluster in real time, it cuts the feedback loop for building, reviewing, and iterating on applications, which speeds up developer workflows and improves CI visibility. The project is a mature, actively maintained Go‑based OSS tool with strong community adoption (3.5 k stars) and solid integration points (API, SDK, CLI).

**Value**  
- **Time savings:** Eliminates the “push‑code‑to‑container‑rebuild‑redeploy” cycle, allowing engineers to see changes instantly in a real cluster.  
- **Consistent environments:** Developers work in the same Kubernetes configuration that runs in production, reducing “it works on my machine” issues.  
- **Better CI feedback:** Changes are validated in the target runtime early, leading to faster, more reliable CI pipelines.

**Practical Adoption Path**  
1. **Pilot:** Deploy Okteto in a sandbox namespace of an existing cluster; use the CLI (`okteto up`) to spin up a development container for a single microservice.  
2. **Integrate:** Add Okteto manifests to the repo (e.g., `okteto.yml`) and incorporate the CLI into local developer onboarding scripts.  
3. **Scale:** Extend the approach to multiple services, configure shared resources (databases, message queues) via Okteto’s `sync` and `forward` features, and link the workflow into CI pipelines for pre‑merge validation.  
4. **Govern:** Define RBAC policies and resource quotas to limit developer‑driven workloads, and monitor usage through existing Kubernetes observability tools.

**Production Readiness**  
- **Activity & Adoption:** Recent commits (as of 2026‑06‑23), 3,511 stars, 315 forks, and a growing ecosystem of topics indicate strong community momentum.  
- **Stability:** Written in Go, the codebase follows conventional Kubernetes patterns and provides a stable API/CLI surface.  
- **Risk Profile:** No major metadata or licensing concerns identified, though a final security audit and verification of maintainers’ activity are advisable before a full‑scale rollout. Overall, Okteto is ready for a serious pilot in production‑like environments.

### Русский

Okteto (okteto/okteto) — это open‑source платформа, позволяющая разрабатывать и отлаживать приложения непосредственно в кластере Kubernetes, что существенно сокращает время цикла разработки и ревью. Типичный сценарий — разработчики запускают свои сервисы в «облачном» окружении через CLI/SDK, автоматизируют локальные задачи и получают быстрый CI‑feedback без необходимости локального стека. Проект демонстрирует высокий уровень готовности к production: активные коммиты, более 3500 звёзд, широкое принятие в сообществе и стабильный набор функций, хотя лицензия и безопасность требуют окончательной проверки.

### 中文

**项目简介**  
Okteto（`okteto/okteto`）是一款开源开发平台，旨在让开发者直接在 Kubernetes 集群上编写、调试和预览应用。通过在真实集群中运行代码，工程师可以显著缩短本地环境搭建和 CI 反馈的时间。

**价值主张**  
- **加速开发循环**：无需本地容器或虚拟机，代码改动即时在集群中生效，极大提升编写、测试和审查的效率。  
- **自动化日常工程任务**：提供 CLI、API 与 SDK，支持一键同步本地文件、热重载以及远程调试，省去繁琐的手工配置。  
- **提升 CI 反馈速度**：在真实的 Kubernetes 环境中运行预览分支，可让 CI 检测到更真实的运行时问题，减少回滚成本。

**典型接入方式**  
1. **CLI 安装**：`curl -L https://okteto.com/install.sh | sh`，随后使用 `okteto up` 在集群中启动开发环境。  
2. **API/SDK**：通过 Go、Python 或 Bash SDK 调用 Okteto API，实现自动化创建/销毁开发空间、同步代码等流程。  
3. **GitHub Action 集成**：在 CI 中加入 `okteto/preview-action`，自动为每个 PR 启动预览环境并返回访问链接。  

**生产可用性**  
- **活跃度高**：2026‑06‑23 最近一次提交，3511 星、315 Fork，社区活跃，Issue 响应及时。  
- **技术成熟**：核心实现使用 Go，已在多个企业内部生产环境验证，支持多租户、RBAC 与网络策略。  
- **风险点**：仍需完成对许可证（Apache‑2.0）合规性、容器安全基线以及维护者长期可用性的最终审查。总体而言，项目已具备 **高** 级别的生产就绪度，适合作为正式业务的 Pilot 或全量推广。

## 🧭 Practical evaluation

**Value:** okteto/okteto helps engineers save time in daily development and review loops.

**Best use cases**

- speed up developer workflows
- automate local engineering tasks
- improve CI feedback

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 3511 GitHub stars
- 315 forks
- updated 2026-06-23
- primary language: Go
- 10 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 62/100 |
| stars | 75/100 |
| topics | 100/100 |
| outlook | 64/100 |
| quality | 72/100 |
| recency | 40/100 |
| adoption | 72/100 |
| production | 64/100 |
| usefulness | 58/100 |
| integration | 78/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 200/100 |

---

<sub>🔭 Discovered 2026-06-23 · [View on GitHub](https://github.com/okteto/okteto) · [← Back to DevTools](./README.md)</sub>
