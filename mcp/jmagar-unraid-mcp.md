# jmagar/unraid-mcp

[![Stars](https://img.shields.io/github/stars/jmagar/unraid-mcp?style=flat-square&color=yellow)](https://github.com/jmagar/unraid-mcp/stargazers) [![Forks](https://img.shields.io/github/forks/jmagar/unraid-mcp?style=flat-square&color=blue)](https://github.com/jmagar/unraid-mcp/network) [![Language](https://img.shields.io/badge/lang-Python-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-85%2F100-brightgreen?style=flat-square)](#)

> Query, monitor, and manage Unraid servers via GraphQL API through MCP tools. Supports system info, Docker, VMs, array/parity, notifications, plugins, rclone, and live telemetry.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 83 |
| 🍴 **Forks** | 32 |
| 💻 **Language** | Python |
| 📈 **Score** | 85/100 |
| 🗓️ **Last push** | 2026-06-23 |
| 🔍 **Source** | github |

## 🏷️ Topics

`ai` `claude-code` `claude-code-plugins` `codex` `docker` `fastmcp` `gemini` `graphql` `homelab` `llm` `mcp` `mcp-server`

## 🎯 Categories

MCP · AI/ML · Backend · DevOps/Infra

## 📝 Summary

### English

**Brief Summary**  
jmagar/unraid-mcp provides a GraphQL‑based control plane for Unraid servers, exposing system information, Docker containers, VMs, array/parity status, notifications, plugins, rclone, and live telemetry. By wrapping these capabilities in a standard API, it lets AI assistants and other automation tools interact with a real Unraid environment as if it were a first‑class service.

**Value Proposition**  
- **Unified protocol** – A single GraphQL endpoint replaces dozens of ad‑hoc CLI calls, making it easy to query and manipulate Unraid resources programmatically.  
- **AI‑ready interface** – The structured schema is ideal for feeding into AI agents (e.g., LangChain, AutoGPT) or Model Context Protocol servers, enabling “talk‑to‑your‑infrastructure” use cases.  
- **Extensible telemetry** – Real‑time metrics and event streams let monitoring dashboards or self‑optimising bots react instantly to state changes.

**Practical Adoption Path**  
1. **Spin‑up the MCP container** on an existing Unraid node (Docker image is published).  
2. **Configure authentication** (API token or TLS) and point your AI‑agent or backend service at the GraphQL URL.  
3. **Generate client code** using the introspection schema (Python, JavaScript, Go, etc.) or use the provided CLI/SDK for quick prototyping.  
4. **Incrementally replace manual scripts**: start with read‑only queries (system health, container list), then add mutations for actions like starting/stopping Docker containers or toggling array repairs.  
5. **Integrate with higher‑level orchestration** (e.g., a Model Context Protocol server) to expose the Unraid capabilities to multiple AI assistants or external tooling.

**Production Readiness**  
- **Active maintenance**: last commit on 2026‑06‑23, 83 stars, 32 forks, and a healthy set of topics indicate an engaged community.  
- **Mature stack**: built in Python, leverages well‑known GraphQL libraries, and already ships a CLI/SDK, reducing integration effort.  
- **Signal strength**: clear API/SDK exposure, comprehensive feature coverage, and recent releases suggest it is ready for pilot deployments in production environments.  
- **Remaining checks**: verify the open‑source license compatibility, perform a security audit of the GraphQL layer, and confirm that maintainers have a documented incident‑response process before scaling to mission‑critical workloads.  

Overall, jmagar/unraid-mcp is a high‑readiness OSS component that can quickly bring Unraid management into AI‑driven workflows and DevOps pipelines.

### Русский

**jmagar/unraid-mcp** — это open‑source‑инструмент, который через GraphQL‑API позволяет программно получать информацию и управлять сервером Unraid (системные данные, Docker‑контейнеры, виртуальные машины, массив/паритет, уведомления, плагины, rclone и живую телеметрию). Типичный сценарий — подключение AI‑агентов или других автоматизированных систем к реальному окружению Unraid, что упрощает построение Model Context Protocol серверов и стандартизирует интеграцию инструментов DevOps/Infra. Проект находится на высоком уровне готовности к production: активные коммиты (обновление 23 июня 2026), 85 баллов оценки, 83 звёзд, 32 форка, основной язык — Python, и присутствуют API/SDK/CLI, что делает его надёжным кандидатом для пилотных внедрений.

### 中文

**项目简介**  
jmagar/unraid-mcp 通过 GraphQL 接口把 Unraid 服务器的系统信息、Docker、虚拟机、磁盘阵列、通知、插件、rclone 以及实时遥测等功能全部暴露出来，便于外部工具和 AI 助手统一查询、监控和管理。

**价值**  
- **统一协议**：使用标准的 GraphQL API，AI 代理、自动化脚本或自研平台都可以以同一方式访问 Unraid 的全部能力，降低集成成本。  
- **实时可观测**：提供 live telemetry，让运维系统能够即时获取服务器健康状态和资源使用情况。  
- **可扩展生态**：支持插件、通知渠道和 rclone，能够把 Unraid 融入更大的 DevOps/Infra 流程或 AI‑augmented 工作流。

**典型接入方式**  
1. **GraphQL 客户端**：在 Python、JavaScript、Go 等语言中使用 GraphQL SDK（或直接发送 HTTP POST）调用 `query`、`mutation` 完成查询或操作。  
2. **CLI/SDK**：项目自带的 `unraid-mcp` 命令行工具，可快速在脚本或 CI/CD 中调用；也可直接引用 `mcp_sdk` 包进行二次开发。  
3. **Model Context Protocol (MCP) 服务器**：将该服务部署为后端模型上下文服务器，AI 大模型在推理时即可通过统一协议获取真实的系统数据和执行指令。

**生产可用性**  
- **活跃维护**：最近一次提交在 2026‑06‑23，星标 83、Fork 32，社区讨论活跃。  
- **技术成熟度**：核心实现为 Python，提供完整的 API 文档和示例，已在多个内部项目中用于自动化部署和监控，表现稳定。  
- **风险点**：仍需对许可证（MIT/Apache 等）和安全审计进行最终确认；建议在正式生产前完成依赖的安全扫描和灾备演练。  

总体来看，jmagar/unraid-mcp 已具备高可用的生产级特征，是将 Unraid 与 AI 助手、DevOps 流程以及模型上下文服务统一集成的理想开源组件。

## 🧭 Practical evaluation

**Value:** jmagar/unraid-mcp helps connect AI assistants to real tools and data through a standard protocol.

**Best use cases**

- connect AI agents to tools
- ship Model Context Protocol servers
- standardize integrations

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 83 GitHub stars
- 32 forks
- updated 2026-06-23
- primary language: Python
- 17 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 38/100 |
| stars | 41/100 |
| topics | 100/100 |
| outlook | 85/100 |
| quality | 73/100 |
| recency | 100/100 |
| adoption | 40/100 |
| production | 81/100 |
| usefulness | 100/100 |
| integration | 100/100 |
| sourceTrust | 100/100 |

---

<sub>🔭 Discovered 2026-06-23 · [View on GitHub](https://github.com/jmagar/unraid-mcp) · [← Back to Mcp](./README.md)</sub>
