# kdeps/kdeps

[![Stars](https://img.shields.io/github/stars/kdeps/kdeps?style=flat-square&color=yellow)](https://github.com/kdeps/kdeps/stargazers) [![Forks](https://img.shields.io/github/forks/kdeps/kdeps?style=flat-square&color=blue)](https://github.com/kdeps/kdeps/network) [![Language](https://img.shields.io/badge/lang-Go-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-63%2F100-brightgreen?style=flat-square)](#)

> AI agent framework in YAML — workflow pipelines + autonomous agent loop. NVIDIA Inception member. Build, deploy, export as Docker/K8s/ISO.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 34 |
| 🍴 **Forks** | 4 |
| 💻 **Language** | Go |
| 📈 **Score** | 63/100 |
| 🗓️ **Last push** | 2026-08-24 |
| 🔍 **Source** | github |

## 🏷️ Topics

`agent` `ai` `llamafile` `llms` `nvidia` `orchestration` `workflow` `yaml`

## 🎯 Categories

Orchestration · Automation · AI/ML · DevOps/Infra

## 📝 Summary

### English

**Brief Summary**  
kdeps/kdeps is an open‑source AI‑agent framework written in Go that lets you describe workflow pipelines and autonomous agent loops in plain YAML. It supports building, deploying, and exporting the resulting agents as Docker containers, Kubernetes manifests, or even bootable ISO images, making it easy to move from prototype to production‑grade deployments.

**Value Proposition**  
- **From prompts to repeatable pipelines** – kdeps turns ad‑hoc prompts and single‑tool calls into version‑controlled, reusable agent workflows, reducing duplication and onboarding time.  
- **Multi‑agent orchestration** – The YAML DSL lets you coordinate several agents, inject tool‑use stages, and manage shared memory, enabling complex, end‑to‑end AI solutions without writing custom glue code.  
- **Portable deployment** – With built‑in exporters for Docker, K8s, and ISO, the same definition can run locally, in the cloud, or on edge devices, simplifying CI/CD and environment consistency.

**Practical Adoption Path**  
1. **Prototype** – Define a simple YAML pipeline (e.g., “fetch data → LLM summarise → store result”) and run it via the CLI to validate logic.  
2. **Integrate** – Use the provided SDK or REST API to embed kdeps pipelines in existing services, or call the CLI from CI scripts.  
3. **Standardise** – Create a library of reusable YAML modules (memory handling, tool wrappers, error‑recovery) that teams can share across projects.  
4. **Deploy** – Export the pipeline as a Docker image or Helm chart for Kubernetes, or generate an ISO for edge/air‑gap installations.  
5. **Monitor & Iterate** – Leverage the framework’s signalling hooks (API/SDK/CLI) to plug in observability, logging, and version control.

**Production Readiness**  
- **Maturity** – Medium. The project is actively maintained (last commit 2026‑06‑23) and has modest community traction (34 stars, 4 forks).  
- **Strengths** – Clear YAML DSL, multi‑target exporters, and Go’s static binary model give a solid base for reliability and performance.  
- **Considerations** – Before production use, verify the license compatibility, perform a security audit of the Docker/K8s images it generates, and assess the maintainers’ capacity for long‑term support. Adding automated tests for your specific pipelines and monitoring the upstream repository for breaking changes will mitigate the remaining risks.

### Русский

kdeps/kdeps — это открытый фреймворк для создания AI‑агентов на основе YAML, позволяющий описывать конвейеры инструментов и автономный цикл работы агента, а затем быстро собирать, развёртывать и экспортировать решения в Docker, Kubernetes или ISO‑образ. Он упрощает превращение разрозненных подсказок и утилит в повторяемые, масштабируемые многопоточные рабочие процессы (координация нескольких агентов, добавление пайплайнов с использованием инструментов, стандартизация памяти агента). Готовность к продакшену — средняя: проект подходит для прототипов и внутренних автоматизаций, но требует дополнительной проверки лицензий, безопасности и поддержки перед масштабным внедрением.

### 中文

**项目简介**  
kdeps/kdeps 是一个基于 YAML 的 AI Agent 框架，提供工作流管道 + 自主 Agent 循环，支持一键构建、部署并导出为 Docker、K8s 或 ISO 镜像。项目已入选 NVIDIA Inception，适合快速搭建可复用的多 Agent、工具调用和记忆管理的 AI 流程。

**价值**  
- **把孤立的 Prompt 与工具转化为可重复的 Agent 工作流**，降低研发成本并提升协作效率。  
- **统一的 YAML 配置** 让业务人员和开发者都能直观编辑、审查和版本化 AI 流程。  
- 支持多 Agent 编排、工具链集成和统一记忆存储，帮助企业构建可扩展的智能系统。

**典型接入方式**  
1. **API/SDK**：通过项目提供的 Go SDK 或 REST API 调用工作流的创建、启动、监控等功能。  
2. **CLI**：使用 `kdeps` 命令行工具在本地或 CI 中快速提交 YAML 定义、构建镜像并推送到容器仓库。  
3. **Docker/K8s/ISO**：一键将完整的 Agent 环境打包为容器镜像或 Kubernetes 部署清单，亦可导出为可离线运行的 ISO 镜像，适配云端、边缘或内部数据中心。

**生产可用性**  
- **成熟度**：目前在 GitHub 上拥有 34 星、4 个 Fork，最近一次更新（2026‑06‑23）显示项目仍在活跃维护。  
- **适用场景**：非常适合原型开发、内部业务流程自动化以及需要快速迭代的 AI 项目；在正式生产环境使用前，建议进行依赖审计、容器安全扫描以及持续维护计划。  
- **风险**：需进一步确认许可证兼容性、长期维护者承诺及安全审计结果后方可投入关键业务。  

总体而言，kdeps/kdeps 为企业提供了一个低代码、可部署的 AI 编排平台，能够在保证灵活性的同时，加速从概念验证到生产落地的转化。

## 🧭 Practical evaluation

**Value:** kdeps/kdeps helps turn isolated prompts and tools into repeatable agent workflows.

**Best use cases**

- coordinate multi-agent workflows
- add tool-use pipelines
- standardize agent memory

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** Medium: useful for prototypes or internal workflows, with dependency and maintenance checks before production.

**Quality signals**

- 34 GitHub stars
- 4 forks
- updated 2026-06-23
- primary language: Go
- 8 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 17/100 |
| stars | 33/100 |
| topics | 100/100 |
| outlook | 59/100 |
| quality | 53/100 |
| recency | 40/100 |
| adoption | 29/100 |
| production | 55/100 |
| usefulness | 90/100 |
| integration | 62/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 400/100 |

---

<sub>🔭 Discovered 2026-06-23 · [View on GitHub](https://github.com/kdeps/kdeps) · [← Back to Orchestration](./README.md)</sub>
