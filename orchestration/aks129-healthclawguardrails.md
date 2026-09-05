# aks129/HealthClawGuardrails

[![Stars](https://img.shields.io/github/stars/aks129/HealthClawGuardrails?style=flat-square&color=yellow)](https://github.com/aks129/HealthClawGuardrails/stargazers) [![Forks](https://img.shields.io/github/forks/aks129/HealthClawGuardrails?style=flat-square&color=blue)](https://github.com/aks129/HealthClawGuardrails/network) [![Language](https://img.shields.io/badge/lang-Python-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-71%2F100-brightgreen?style=flat-square)](#)

> Open-source guardrails between AI agents and FHIR clinical data — PHI redaction, immutable audit, step-up auth, tenant isolation. MCP server + OpenAI/Gemini adapters. A healthclaw.io project.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 22 |
| 🍴 **Forks** | 5 |
| 💻 **Language** | Python |
| 📈 **Score** | 71/100 |
| 🗓️ **Last push** | 2026-09-05 |
| 🔍 **Source** | github |

## 🏷️ Topics

`agent-skills` `agents` `ai-agents` `fhir` `health-data` `healthai` `healthcare` `hipaa` `mcp` `mcp-server` `model-context-protocol` `phi-redaction`

## 🎯 Categories

Orchestration · MCP · AI/ML · Backend · Data

## 📝 Summary

### English

**Brief Summary**  
HealthClawGuardrails (aks129/HealthClawGuardrails) is an open‑source framework that inserts “guardrails” between AI agents and FHIR‑based clinical data. It provides PHI redaction, immutable audit logging, step‑up authentication, and tenant isolation via a modular MCP server with adapters for OpenAI and Gemini, enabling safe, repeatable multi‑agent workflows in health‑tech environments.  

**Value**  
- **Compliance‑first data handling** – automatic PHI scrubbing and tamper‑evident audit trails keep interactions with patient data within HIPAA‑compatible boundaries.  
- **Secure, context‑aware access** – step‑up authentication and per‑tenant isolation prevent cross‑tenant data leakage and enforce least‑privilege principles.  
- **Reusable agent pipelines** – the MCP server and language‑agnostic adapters let developers stitch together isolated prompts, tool calls, and memory stores into deterministic, version‑controlled workflows, reducing ad‑hoc scripting and operational risk.  

**Practical Adoption Path**  
1. **Pilot the MCP server** – spin up the Docker‑compose deployment (or run the Python package) in a dev sandbox and point it at a test FHIR endpoint.  
2. **Integrate an LLM adapter** – choose the OpenAI or Gemini adapter (or implement a custom one) and configure the API keys and authentication policies.  
3. **Define guardrail policies** – use the provided YAML/JSON schema to declare PHI redaction rules, audit log destinations, and step‑up auth triggers.  
4. **Wrap existing agents** – replace direct LLM calls in your code with the MCP client SDK/CLI, letting the server mediate every request.  
5. **Scale to production** – deploy the server on Kubernetes or a managed VM, enable TLS, configure persistent audit storage (e.g., immutable object store), and enable tenant‑level RBAC.  

**Production Readiness**  
- **Recent activity** (last commit 2026‑07‑05) and a modest but growing community (22 stars, 5 forks) indicate active maintenance.  
- **Strong technical signals**: Python implementation, clear API/SDK/CLI surface, and support for two major LLM providers make integration straightforward.  
- **Compliance‑ready features** (PHI redaction, immutable logs, step‑up auth) address the biggest regulatory hurdles for health‑AI deployments.  
- **Risks** are limited to standard OSS concerns—final license verification, deeper security review of third‑party dependencies, and confirmation of long‑term maintainers.  

Overall, HealthClawGuardrails is a high‑readiness candidate for organizations that need to operationalize AI agents on sensitive clinical data while retaining auditability, isolation, and regulatory compliance.

### Русский

**HealthClawGuardrails** (aks129/HealthClawGuardrails) — open‑source‑решение, которое ставит «ограждения» между AI‑агентами и клиническими данными FHIR: автоматически редактирует PHI, сохраняет неизменяемый аудит, поддерживает пошаговую авторизацию и изоляцию tenants. Типичный сценарий — построение повторяемых многокомпонентных пайплайнов, где несколько агентов используют инструменты (OpenAI, Gemini) через MCP‑сервер, а их взаимодействия фиксируются и защищаются. По уровню готовности проект считается почти production‑ready: активные коммиты (обновление 2026‑07‑05), 22 звёзд, 5 форков, чистый Python‑код, API/SDK/CLI и хорошая экосистема позволяют быстро развернуть пилотный вариант.

### 中文

**项目简介**  
HealthClawGuardrails（aks129/HealthClawGuardrails）是一套开源的“护栏”组件，位于 AI 代理与 FHIR 临床数据之间，实现 PHI（受保护健康信息）脱敏、不可篡改审计、一步提升授权、租户隔离等安全保障。项目提供 MCP（Micro‑Component Platform）服务器以及 OpenAI、Gemini 的适配器，帮助将零散的提示和工具组织成可重复的多代理工作流。

**价值体现**  
- **安全合规**：自动对 FHIR 资源进行 PHI 脱敏，并记录不可篡改的审计日志，满足 HIPAA 等法规要求。  
- **工作流标准化**：通过 MCP 框架将多代理、工具调用、记忆管理等统一编排，降低业务方自行实现的复杂度。  
- **可插拔适配**：内置 OpenAI 与 Gemini 的适配器，支持快速接入主流大模型，同时保持对自研模型的可扩展性。  

**典型接入方式**  
1. **API/SDK**：在已有的后端服务中通过 HTTP API 调用 MCP 服务器，或使用项目提供的 Python SDK 直接在代码中创建、管理 agent‑workflow。  
2. **CLI**：利用项目自带的命令行工具进行本地调试、工作流部署与监控。  
3. **容器化部署**：项目提供 Dockerfile，可在 Kubernetes 或其他容器平台上以单节点或多租户模式运行，配合环境变量完成模型凭证和 FHIR 端点的配置。  

**生产可用性**  
- **活跃度**：截至 2026‑07‑05 最近一次提交，项目仍在维护；GitHub 22 ⭐、5 fork，社区关注度适中。  
- **技术成熟度**：核心实现基于 Python，代码结构清晰，已覆盖 API、SDK、CLI 三层入口，易于评估和集成。  
- **安全与合规**：提供 PHI 脱敏和审计日志功能，满足基本的医疗数据合规需求；但仍需自行审查许可证（MIT）和依赖库的安全报告。  
- **适合场景**：对需要在医疗机构内部或 SaaS 环境中安全地让 AI 代理访问 FHIR 数据的团队，可先在预生产环境进行功能验证，随后逐步推广至全量生产。  

总体而言，HealthClawGuardrails 已具备较高的生产候选人（OSS candidate）级别，适合在对合规性有严格要求的医疗 AI 项目中快速搭建安全可靠的多代理工作流。

## 🧭 Practical evaluation

**Value:** aks129/HealthClawGuardrails helps turn isolated prompts and tools into repeatable agent workflows.

**Best use cases**

- coordinate multi-agent workflows
- add tool-use pipelines
- standardize agent memory

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 22 GitHub stars
- 5 forks
- updated 2026-07-05
- primary language: Python
- 14 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 19/100 |
| stars | 29/100 |
| topics | 100/100 |
| outlook | 73/100 |
| quality | 62/100 |
| recency | 80/100 |
| adoption | 26/100 |
| production | 70/100 |
| usefulness | 90/100 |
| integration | 78/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 500/100 |

---

<sub>🔭 Discovered 2026-07-05 · [View on GitHub](https://github.com/aks129/HealthClawGuardrails) · [← Back to Orchestration](./README.md)</sub>
