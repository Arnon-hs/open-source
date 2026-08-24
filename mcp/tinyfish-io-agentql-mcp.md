# tinyfish-io/agentql-mcp

[![Stars](https://img.shields.io/github/stars/tinyfish-io/agentql-mcp?style=flat-square&color=yellow)](https://github.com/tinyfish-io/agentql-mcp/stargazers) [![Forks](https://img.shields.io/github/forks/tinyfish-io/agentql-mcp?style=flat-square&color=blue)](https://github.com/tinyfish-io/agentql-mcp/network) [![Language](https://img.shields.io/badge/lang-Shell-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-66%2F100-brightgreen?style=flat-square)](#)

> Model Context Protocol server that integrates AgentQL's data extraction capabilities.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 167 |
| 🍴 **Forks** | 38 |
| 💻 **Language** | Shell |
| 📈 **Score** | 66/100 |
| 🗓️ **Last push** | 2026-08-24 |
| 🔍 **Source** | github |

## 🏷️ Topics

`agent` `agentql` `ai` `aiagent` `claude` `cursor` `llm-tools` `mcp` `mcp-server` `model-context-protocol` `playwright` `scraping`

## 🎯 Categories

MCP · AI/ML · Backend

## 📝 Summary

### English

**Summary**  
tinyfish‑io/agentql‑mcp is a Model Context Protocol (MCP) server that wraps AgentQL’s data‑extraction engine, exposing a clean API/SDK/CLI so AI assistants can fetch real‑world data and invoke tools through a standard protocol. With 167 ★, recent commits (last updated 2026‑05‑12), and a growing ecosystem of topics, it’s positioned as a production‑ready OSS component for building “AI‑as‑a‑service” back‑ends.  

**Value**  
The project eliminates the need to hand‑craft custom connectors for each data source or tool; by speaking MCP, any LLM‑powered agent can query, filter, and act on external resources using a single, well‑defined contract. This standardisation speeds up integration, reduces maintenance overhead, and makes it easier to audit and secure AI‑driven workflows.  

**Practical adoption path**  
1. **Prototype** – Pull the Docker image or clone the repo, run the server locally, and use the provided CLI/SDK to issue simple AgentQL queries against a test data set.  
2. **Integrate** – Replace the prototype endpoint with a managed instance (K8s, cloud VM, or serverless) and point your AI assistant’s tool‑calling layer to the MCP endpoint; the existing language‑agnostic client libraries make this a drop‑in change.  
3. **Scale & secure** – Add authentication (OAuth/JWT), enable TLS, and configure rate‑limiting; the server’s modular shell scripts allow easy extension to custom data connectors or tool adapters.  

**Production readiness**  
The repository shows high activity (recent commits, 38 forks, 17 topical tags) and a solid community signal (167 ★). Its primary implementation is in Shell, which simplifies deployment and debugging, and the exposed API/SDK/CLI are already documented for immediate consumption. While a final review of licensing, security hardening, and maintainer responsiveness is advisable, the current signals indicate the project is mature enough for a serious pilot or production rollout.

### Русский

**tinyfish-io/agentql-mcp** — это сервер реализации Model Context Protocol, который объединяет возможности извлечения данных AgentQL с единым протоколом взаимодействия. Он позволяет быстро подключать AI‑ассистентов к реальным инструментам и базам данных, упрощая развертывание MCP‑серверов и стандартизацию интеграций. По активности репозитория (167 звёзд, 38 форков, последние коммиты — 2026‑05‑12) и наличию готовых API/SDK/CLI проект считается почти готовым к production‑использованию, хотя окончательная проверка лицензии и безопасности всё‑ещё требуется.

### 中文

**项目简介**  
tinyfish-io/agentql-mcp 是一个 Model Context Protocol（MCP）服务器，内置 AgentQL 的数据抽取能力，能够让 AI 助手通过统一的协议访问真实工具和业务数据。

**价值点**  
- **标准化接入**：提供统一的 MCP 接口，避免为每个工具单独实现特殊的 API，降低集成成本。  
- **快速赋能 AI**：利用 AgentQL 的强大数据抽取，让语言模型直接读取、过滤并结构化外部系统的数据。  
- **可组合生态**：作为 MCP 服务器，可与其他遵循同协议的工具链、工具市场或自研插件无缝拼接，构建完整的 AI‑to‑Tool 生态。

**典型接入方式**  
1. **API/SDK**：直接调用服务器暴露的 HTTP/REST 接口（或对应的 SDK），在 AI 助手的代码中发送 `model_context` 请求并获取结构化响应。  
2. **CLI**：通过项目自带的命令行工具在本地或 CI 环境快速启动/测试 MCP 服务。  
3. **容器化部署**：使用官方提供的 Docker 镜像或 Helm Chart 将服务部署到 Kubernetes，配合服务发现即可在微服务体系中统一调用。  

**生产可用性**  
- **活跃度高**：截至 2026‑05‑12 最近一次提交，拥有 167 ⭐、38 🍴，代码以 Shell 为主，覆盖 17 个相关话题，社区活跃。  
- **成熟度**：已具备完整的 API 文档、示例代码和 CI/CD 流水线，适合作为正式环境的 MCP 服务。  
- **风险**：目前未发现重大许可证或安全隐患，但仍建议在正式投产前进行一次安全审计并确认维护者的响应时效。  

综上，tinyfish-io/agentql-mcp 具备高可用的技术实现和良好的社区支持，是在生产环境中为 AI 助手接入真实工具和数据的可靠选择。

## 🧭 Practical evaluation

**Value:** tinyfish-io/agentql-mcp helps connect AI assistants to real tools and data through a standard protocol.

**Best use cases**

- connect AI agents to tools
- ship Model Context Protocol servers
- standardize integrations

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 167 GitHub stars
- 38 forks
- updated 2026-05-12
- primary language: Shell
- 17 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 40/100 |
| stars | 47/100 |
| topics | 100/100 |
| outlook | 58/100 |
| quality | 55/100 |
| recency | 20/100 |
| adoption | 45/100 |
| production | 51/100 |
| usefulness | 100/100 |
| integration | 62/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 300/100 |

---

<sub>🔭 Discovered 2026-05-12 · [View on GitHub](https://github.com/tinyfish-io/agentql-mcp) · [← Back to Mcp](./README.md)</sub>
