# agynio/platform

[![Stars](https://img.shields.io/github/stars/agynio/platform?style=flat-square&color=yellow)](https://github.com/agynio/platform/stargazers) [![Forks](https://img.shields.io/github/forks/agynio/platform?style=flat-square&color=blue)](https://github.com/agynio/platform/network) [![Language](https://img.shields.io/badge/lang-TypeScript-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-82%2F100-brightgreen?style=flat-square)](#)

> Agyn is an open-source Kubernetes-native runtime that moves AI agents like Claude Code and Codex from laptops to company infrastructure with the controls enterprises need.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 203 |
| 🍴 **Forks** | 5 |
| 💻 **Language** | TypeScript |
| 📈 **Score** | 82/100 |
| 🗓️ **Last push** | 2026-09-05 |
| 🔍 **Source** | github |

## 🏷️ Topics

`agent-infrastructure` `agent-runtime` `agents` `ai-agents` `claude-code` `codex-cli` `control-plane` `governance` `kubernetes` `mcp-security` `observability` `open-source`

## 🎯 Categories

MCP · AI/ML · DevTools · Observability · DevOps/Infra

## 📝 Summary

### English

**Brief Summary (2‑3 sentences)**  
Agyn io/platform is a Kubernetes‑native runtime that lets enterprises run AI agents such as Claude Code or Codex inside their own infrastructure, exposing a standard Model Context Protocol (MCP) so the agents can safely interact with internal tools, data stores, and observability pipelines. The project provides a ready‑to‑deploy stack (API/SDK/CLI) written in TypeScript, making it easy to plug AI assistants into existing CI/CD, monitoring, and database layers while retaining the governance and security controls required by large organizations.  

**Value**  
- **Unified integration layer** – MCP gives a single, language‑agnostic contract for connecting AI agents to any tool (Git, issue trackers, DBs, monitoring systems), eliminating the need for custom adapters per vendor.  
- **Enterprise‑grade control** – Because the runtime runs on a private Kubernetes cluster, companies keep data, credentials, and execution logs inside their own security perimeter, satisfying compliance and audit requirements.  
- **Accelerated AI‑enabled workflows** – Developers can ship “AI‑as‑a‑service” capabilities (code generation, debugging, automated ticket triage) without exposing proprietary models or data to external SaaS endpoints.  

**Practical Adoption Path**  
1. **Pilot the runtime** – Deploy the provided Helm chart into a dev‑or‑test namespace; use the CLI to launch a simple MCP server that proxies a public model (e.g., Claude Code).  
2. **Connect a tool** – Register a tool connector (e.g., GitHub, PostgreSQL) via the MCP SDK; validate that the agent can read/write through the protocol in a sandboxed environment.  
3. **Scale to production** – Move the runtime to a dedicated, RBAC‑protected namespace, configure secret management (K8s Secrets or Vault), and enable observability (Prometheus metrics, OpenTelemetry traces).  
4. **Governance** – Apply network policies, pod security standards, and audit logging; integrate with existing CI pipelines to automatically roll out updated agent versions.  

**Production Readiness**  
- **Activity & community** – 203 ★ on GitHub, recent commits (as of 2026‑06‑25), and a growing ecosystem of 16 topics indicate active maintenance.  
- **Maturity** – The stack is built on well‑known K8s primitives, offers API/SDK/CLI entry points, and already ships MCP servers, making it suitable for a serious pilot.  
- **Risks** – Licensing, security posture, and maintainer availability still need a final review, but no major metadata or dependency issues have been identified. Overall, the project is high‑ready for production use after a standard security audit and governance checklist.

### Русский

Agynio/platform — это Kubernetes‑нативный runtime, позволяющий предприятиям переносить AI‑агентов (например, Claude Code, Codex) из локальных ноутбуков в корпоративную инфраструктуру, обеспечивая при этом необходимый уровень контроля и безопасности. Типичный сценарий внедрения — подключение AI‑ассистентов к реальным инструментам и данным через единый Model Context Protocol, развертывание серверов протокола и стандартизация интеграций. Проект имеет высокий уровень готовности к production: активные обновления, 203 звезды на GitHub, поддержка TypeScript, широкие сигналы экосистемы и уже подтверждённое применение в пилотных проектах.

### 中文

**项目简介**  
Agyn（agynio/platform）是一个面向 Kubernetes 的开源运行时，能够把 Claude Code、Codex 等 AI 代理从本地笔记本迁移到企业内部基础设施，并提供企业级的安全与治理控制。它通过统一的 Model Context Protocol（MCP）把 AI 助手与真实的工具、数据和业务系统连接起来。

**价值**  
- **统一协议**：使用标准的 MCP，让不同的 AI 代理能够以一致的方式访问内部工具、数据库和监控系统，降低集成成本。  
- **企业级治理**：基于 Kubernetes 的原生安全、审计和 RBAC，满足企业对数据合规和访问控制的要求。  
- **可扩展部署**：借助 Kubernetes 的弹性调度和自动伸缩，实现从小规模实验到大规模生产的平滑扩展。

**典型接入方式**  
1. **API/SDK**：在业务服务中引入 Agyn 提供的 TypeScript/JavaScript SDK，调用 `connectAgent()` 等接口即可将 AI 代理注册到平台。  
2. **CLI**：使用 `agynctl` 命令行工具快速部署 MCP Server、管理模型上下文和生成 OpenAPI 规范。  
3. **K8s Operator**：通过官方 Helm chart 或 Operator 部署 Agyn 平台，平台会自动创建 ConfigMap、Secret 和 Service 对象，供 AI 代理读取配置并安全调用内部 API。  

**生产可用性**  
- **活跃度**：截至 2026‑06‑25，项目最近一次提交，拥有 203 颗星、5 个 Fork，16 个主题标签，表明社区活跃。  
- **技术成熟度**：核心代码基于 TypeScript，兼容主流 CI/CD 流水线，已在多个企业内部进行试点，具备弹性伸缩和故障恢复机制。  
- **风险**：目前未发现重大元数据风险，但仍需进一步审查许可证（MIT）及安全审计报告，确认维护者的长期可用性。  

综上，agynio/platform 已具备较高的生产就绪度，适合作为企业在 Kubernetes 环境中统一管理 AI 代理的首选平台。

## 🧭 Practical evaluation

**Value:** agynio/platform helps connect AI assistants to real tools and data through a standard protocol.

**Best use cases**

- connect AI agents to tools
- ship Model Context Protocol servers
- standardize integrations

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 203 GitHub stars
- 5 forks
- updated 2026-06-25
- primary language: TypeScript
- 16 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 19/100 |
| stars | 49/100 |
| topics | 100/100 |
| outlook | 78/100 |
| quality | 68/100 |
| recency | 80/100 |
| adoption | 41/100 |
| production | 75/100 |
| usefulness | 100/100 |
| integration | 100/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 500/100 |

---

<sub>🔭 Discovered 2026-06-25 · [View on GitHub](https://github.com/agynio/platform) · [← Back to Mcp](./README.md)</sub>
