# Th0rgal/sandboxed.sh

[![Stars](https://img.shields.io/github/stars/Th0rgal/sandboxed.sh?style=flat-square&color=yellow)](https://github.com/Th0rgal/sandboxed.sh/stargazers) [![Forks](https://img.shields.io/github/forks/Th0rgal/sandboxed.sh?style=flat-square&color=blue)](https://github.com/Th0rgal/sandboxed.sh/network) [![Language](https://img.shields.io/badge/lang-Rust-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-77%2F100-brightgreen?style=flat-square)](#)

> Self-hosted orchestrator for AI autonomous agents. Run Claude Code & Open Code in isolated linux workspaces. Manage your skills, configs and encrypted secrets with a git repo.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 422 |
| 🍴 **Forks** | 44 |
| 💻 **Language** | Rust |
| 📈 **Score** | 77/100 |
| 🗓️ **Last push** | 2026-05-11 |
| 🔍 **Source** | github |

## 🏷️ Topics

`ai-agents` `autonomous-agents` `claude` `claude-code` `coding-assistant` `containerization` `developer-tools` `llm` `mcp` `opencode` `orchestration` `self-hosted`

## 🎯 Categories

Orchestration · MCP · Automation · AI/ML · DevTools

## 📝 Summary

### English

**Brief Summary**  
Th0rgal / sandboxed.sh is a self‑hosted orchestrator that runs Claude‑code and open‑source AI agents inside isolated Linux workspaces, letting you version‑control skills, configurations, and encrypted secrets with a Git repository. It turns ad‑hoc prompts and tool calls into repeatable, multi‑agent workflows that can be managed via a simple CLI/SDK.

**Value**  
- **Isolation & Security** – Each agent runs in its own sandboxed container, preventing cross‑contamination and protecting sensitive data.  
- **Version‑controlled Ops** – Skills, prompts, and secrets live in Git, giving you auditability, roll‑backs, and CI/CD‑style deployment of AI logic.  
- **Workflow Automation** – By chaining agents and tools, you can build complex pipelines (e.g., data extraction → analysis → report generation) that are reproducible and shareable across teams.

**Practical Adoption Path**  
1. **Pilot Setup** – Clone the repo, configure the required Docker/Podman environment, and add your Claude‑code or open‑source model binaries.  
2. **Define Skills & Secrets** – Store prompts, tool wrappers, and encrypted secrets in a dedicated Git branch; use the provided CLI to register them.  
3. **Create Workflows** – Write YAML/JSON workflow definitions that specify agent order, input/output bindings, and resource limits.  
4. **Integrate** – Call the orchestrator from existing CI pipelines, internal APIs, or a custom SDK to trigger workflows on demand.  
5. **Scale** – Deploy the orchestrator on a Kubernetes node pool or a VM fleet; the built‑in health checks and metrics let you monitor performance and add more sandbox instances as load grows.

**Production Readiness**  
- **Activity & Community** – 422 stars, 44 forks, recent commits (as of 2026‑05‑11), and a Rust codebase indicate active maintenance and a growing user base.  
- **Maturity** – The project already exposes a stable CLI/SDK, supports encrypted secret handling, and follows a Git‑Ops model, which aligns with typical enterprise DevOps practices.  
- **Risks to Verify** – Final due‑diligence should confirm the license compatibility, review any open security issues, and ensure at least one maintainer is responsive for critical patches.  

Overall, sandboxed.sh is production‑grade for a serious pilot, especially for teams that need secure, reproducible AI agent pipelines and want to manage them through familiar Git‑centric workflows.

### Русский

**Th0rgal/sandboxed.sh** — это self‑hosted оркестратор для автономных AI‑агентов, позволяющий запускать Claude Code и Open Code в полностью изолированных Linux‑рабочих пространствах, управлять навыками, конфигурациями и зашифрованными секретами через Git‑репозиторий. Он упрощает построение повторяемых рабочих потоков: от координации нескольких агентов и создания конвейеров с инструментами до стандартизации памяти агентов, что делает его идеальным решением для компаний, желающих автоматизировать сложные multi‑agent сценарии. Проект имеет высокий уровень готовности к production: активные обновления (последний commit 2026‑05‑11), 422 звёзд, 44 форка, написан на Rust и предоставляет API/SDK/CLI, что упрощает интеграцию и пилотирование.

### 中文

**项目简介（2‑3 句话）**  
Th0rgal/sandboxed.sh 是一款自托管的 AI 代理编排器，能够在相互隔离的 Linux 工作空间中安全运行 Claude Code 与 Open‑Code。通过 Git 仓库统一管理技能、配置和加密密钥，让提示与工具的组合可以被复用为可靠的自动化工作流。

**价值**  
- **安全隔离**：每个代理在独立的容器/沙箱中执行，防止代码互相干扰或泄露敏感信息。  
- **可重复的工作流**：把“一次性提示+工具”固化为 Git‑版本化的流程，实现 agent 的记忆、配置和技能的标准化管理。  
- **多代理协同**：天然支持多代理协作、工具链拼接和结果持久化，适用于复杂的业务编排、数据处理和 AI‑驱动的自动化场景。

**典型接入方式**  
1. **CLI / SDK**：项目提供可直接调用的 `sandboxed.sh` 脚本和 Rust 库，使用命令行或在自研服务中嵌入 SDK 即可启动/管理 sandbox。  
2. **Git‑Ops 配置**：在专用的 Git 仓库中维护 `skills/`, `configs/` 与 `secrets/` 目录，提交即触发工作流更新，实现声明式部署。  
3. **API 网关**：通过暴露的 HTTP API（或 OpenAPI 文档）将外部系统（CI/CD、业务系统、监控平台）与 sandbox 进行集成，完成任务提交、状态查询和结果回调。  

**生产可用性**  
- **活跃度**：截至 2026‑05‑11，项目仍在积极维护，最近一次提交在当日；GitHub 统计 422 星、44 Fork，社区活跃。  
- **技术成熟度**：核心实现使用 Rust，具备高性能和内存安全；提供完整的实现信号（API/CLI/语言元数据），便于评估与二次开发。  
- **安全与合规**：所有代理均运行在隔离的 Linux 沙箱，敏感信息通过 Git 加密管理；仍需进一步审查许可证（MIT/Apache 等）和长期维护者承诺。  
- **适配度**：适合作为内部 AI 编排平台的底层引擎，支持从原型验证到正式生产的全链路迁移。  

综上，sandboxed.sh 在安全、可重复性和多代理编排方面提供了完整的 OSS 解决方案，具备足够的社区与技术支撑，可在企业内部进行试点并逐步推广到生产环境。

## 🧭 Practical evaluation

**Value:** Th0rgal/sandboxed.sh helps turn isolated prompts and tools into repeatable agent workflows.

**Best use cases**

- coordinate multi-agent workflows
- add tool-use pipelines
- standardize agent memory

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 422 GitHub stars
- 44 forks
- updated 2026-05-11
- primary language: Rust
- 13 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 41/100 |
| stars | 56/100 |
| topics | 100/100 |
| outlook | 88/100 |
| quality | 78/100 |
| recency | 100/100 |
| adoption | 52/100 |
| production | 76/100 |
| usefulness | 100/100 |
| integration | 46/100 |
| sourceTrust | 100/100 |

---

<sub>🔭 Discovered 2026-05-11 · [View on GitHub](https://github.com/Th0rgal/sandboxed.sh) · [← Back to Orchestration](./README.md)</sub>
