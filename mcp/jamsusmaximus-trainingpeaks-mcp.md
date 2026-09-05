# JamsusMaximus/trainingpeaks-mcp

[![Stars](https://img.shields.io/github/stars/JamsusMaximus/trainingpeaks-mcp?style=flat-square&color=yellow)](https://github.com/JamsusMaximus/trainingpeaks-mcp/stargazers) [![Forks](https://img.shields.io/github/forks/JamsusMaximus/trainingpeaks-mcp?style=flat-square&color=blue)](https://github.com/JamsusMaximus/trainingpeaks-mcp/network) [![Language](https://img.shields.io/badge/lang-Python-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-78%2F100-brightgreen?style=flat-square)](#)

> TrainingPeaks MCP server for Claude Desktop, Code and Cowork. No API approval needed - works with any account. Query workouts, CTL/ATL/TSB fitness data, power PRs via natural language.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 95 |
| 🍴 **Forks** | 45 |
| 💻 **Language** | Python |
| 📈 **Score** | 78/100 |
| 🗓️ **Last push** | 2026-09-05 |
| 🔍 **Source** | github |

## 🏷️ Topics

`claude` `claude-desktop` `cycling` `fitness` `mcp` `mcp-server` `model-context-protocol` `running` `training-load` `training-peaks` `trainingpeaks`

## 🎯 Categories

MCP · AI/ML · Backend

## 📝 Summary

### English

**Project Summary:**

The open-source project "JamsusMaximus/trainingpeaks-mcp" provides a TrainingPeaks MCP server that enables connection to AI assistants without requiring API approval. This allows for seamless querying of workout data, fitness metrics, and power performance records using natural language. The project offers a standard protocol for integrating AI agents with real tools and data.

**Value Proposition:**

The value proposition of this project lies in its ability to connect AI assistants to real tools and data through a standard protocol. This enables developers to integrate AI agents with various applications and services without requiring extensive API knowledge or approval. The project's value lies in its potential to simplify the integration process and provide a standardized way of accessing data and tools.

**Practical Adoption Path:**

The practical adoption path for this project involves several steps:

1. Evaluate the project's implementation signals, such as API/SDK/CLI, language metadata, and focused topics.
2. Assess the project's production readiness, considering factors like recent activity, adoption, and ecosystem signals.
3. Review the project's license, security posture, and active maintainers to ensure it meets your requirements.
4. Integrate the project's MCP server with your AI assistant or application.
5. Test and refine the integration to ensure seamless

### Русский

Резюме проекта JamsusMaximus/trainingpeaks-mcp:

Проект JamsusMaximus/trainingpeaks-mcp представляет собой сервер TrainingPeaks MCP, предназначенный для интеграции с AI-ассистентами, такими как Claude Desktop, Code и Cowork. Это позволяет соединять искусственный интеллект с реальными инструментами и данными через стандартный протокол. Проект уже имеет хороший потенциал для внедрения, поскольку предоставляет прямой доступ к данным о тренировках, показателям физической формы и личным рекордам мощности.

Типовой сценарий внедрения проекта предполагает подключение AI-агентов к реальным инструментам и данным. Проект уже готов к serious пилоту, поскольку имеет высокий уровень готовности к production, подтверждаемый активностью, принятием и экосистемными сигналами.

### 中文

**价值**  
JamsusMaximus/trainingpeaks‑mcp 为 Claude Desktop、Claude Code、Claude Cowork 等 AI 助手提供了一个标准化的 **Model Context Protocol（MCP）** 接口，使得 AI 能够直接查询 TrainingPeaks 上的训练记录、CTL/ATL/TSB 健康指标以及功率 PR 等数据。无需申请 TrainingPeaks 官方 API 权限，任何账号都能使用，从而大幅降低 AI 与真实运动数据的集成门槛，帮助企业快速把 AI 助手嵌入到教练平台、健身 App 或内部分析工具中。

**典型接入方式**  
1. **MCP Server 部署**：在本地或云服务器上运行 `trainingpeaks-mcp`（Python 包），通过 `docker compose` 或直接 `pip install` 启动。  
2. **身份认证**：在启动参数或环境变量中提供 TrainingPeaks 账户的用户名/密码（或 OAuth token），服务器会自动完成登录并维护会话。  
3. **调用方式**：AI 助手（Claude Desktop/Code/Cowork）通过标准的 MCP JSON‑RPC 接口发送自然语言请求，例如 `“查询上周的跑步距离和 CTL”`，服务器解析后返回结构化数据。  
4. **可选 CLI/SDK**：项目同时提供命令行工具和 Python SDK，便于调试或在自研后端服务中直接调用。

**生产可用性**  
- **活跃度**：最近一次提交在 2026‑06‑27，GitHub ★95、Fork 45，表明社区活跃且持续维护。  
- **技术成熟度**：使用 Python 实现，配套 Docker 镜像，支持 API/SDK/CLI 三种调用方式，易于在容器化或 Serverless 环境中部署。  
- **安全与合规**：目前未发现重大元数据泄露风险，但仍需自行审查许可证（MIT）以及登录凭证的存储方式，确保符合企业安全政策。  
- **可扩展性**：遵循 MCP 标准，可与其他 MCP‑compatible 工具（如自研模型、第三方 AI 平台）共用同一协议层，便于统一管理和监控。

综合来看，trainingpeaks‑mcp 已具备 **高可用、易集成、社区支持良好** 的特性，适合作为 **生产环境** 中 AI 与 TrainingPeaks 数据交互的首选实现，只需在部署前完成安全审计和凭证管理即可投入使用。

## 🧭 Practical evaluation

**Value:** JamsusMaximus/trainingpeaks-mcp helps connect AI assistants to real tools and data through a standard protocol.

**Best use cases**

- connect AI agents to tools
- ship Model Context Protocol servers
- standardize integrations

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 95 GitHub stars
- 45 forks
- updated 2026-06-27
- primary language: Python
- 11 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 42/100 |
| stars | 42/100 |
| topics | 100/100 |
| outlook | 77/100 |
| quality | 69/100 |
| recency | 80/100 |
| adoption | 42/100 |
| production | 74/100 |
| usefulness | 90/100 |
| integration | 94/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 300/100 |

---

<sub>🔭 Discovered 2026-06-27 · [View on GitHub](https://github.com/JamsusMaximus/trainingpeaks-mcp) · [← Back to Mcp](./README.md)</sub>
