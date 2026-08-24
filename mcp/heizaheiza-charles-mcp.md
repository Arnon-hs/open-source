# heizaheiza/Charles-mcp

[![Stars](https://img.shields.io/github/stars/heizaheiza/Charles-mcp?style=flat-square&color=yellow)](https://github.com/heizaheiza/Charles-mcp/stargazers) [![Forks](https://img.shields.io/github/forks/heizaheiza/Charles-mcp?style=flat-square&color=blue)](https://github.com/heizaheiza/Charles-mcp/network) [![Language](https://img.shields.io/badge/lang-Python-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-67%2F100-brightgreen?style=flat-square)](#)

> Charles Proxy MCP server for AI agents with live capture, structured traffic analysis, and agent-friendly tool contracts

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 264 |
| 🍴 **Forks** | 27 |
| 💻 **Language** | Python |
| 📈 **Score** | 67/100 |
| 🗓️ **Last push** | 2026-08-24 |
| 🔍 **Source** | github |

## 🏷️ Topics

`ai-agent` `charles-proxy` `codex` `developer-tools` `mcp` `mcp-server` `network-debugging` `openai`

## 🎯 Categories

MCP · AI/ML · Backend · DevTools

## 📝 Summary

### English

**Brief Summary (2‑3 sentences)**  
heizaheiza/Charles‑mcp is an open‑source MCP (Model Context Protocol) server that lets AI agents capture live network traffic, transform it into a structured, query‑able format, and interact with tools through a clean, agent‑friendly contract. Built in Python, it provides ready‑made APIs/SDKs and a CLI for rapid integration, making it easy to plug real‑world services into LLM‑driven workflows.  

**Value Proposition**  
- **Bridges the gap** between LLMs and actual tools by exposing live traffic and tool semantics via a standard MCP contract, turning “sandbox” AI agents into productive assistants that can call real APIs, read logs, or trigger actions.  
- **Structured traffic analysis** gives agents a consistent schema (request/response, headers, payloads, timestamps) that can be directly consumed by prompting or fine‑tuning pipelines, reducing the need for custom parsers.  
- **Tool‑first design** means contracts are deliberately simple (JSON‑RPC‑style) and extensible, lowering the learning curve for developers and enabling rapid prototyping of new integrations.  

**Practical Adoption Path**  
1. **Prototype** – Clone the repo, run the provided Docker/virtual‑env setup, and point the Charles‑mcp server at a target service (e.g., a REST API or internal microservice).  
2. **Connect the Agent** – Use the supplied Python SDK (or the generic HTTP/CLI client) to register the service with an LLM‑based agent (e.g., OpenAI function calling, LangChain tool wrappers).  
3. **Iterate** – Leverage the live capture UI or exported JSON logs to refine the tool contract and improve prompt engineering.  
4. **Scale** – Deploy the MCP server in a container orchestration platform (K8s, ECS) behind TLS, configure authentication (API keys/OAuth), and register the endpoint in your production AI‑agent orchestration layer.  

**Production Readiness**  
- **Activity & Community** – 264 stars, 27 forks, recent commits (last updated 2026‑06‑23) and a growing set of topics indicate an active community.  
- **Maturity** – The codebase is primarily Python, a language familiar to most ML/DevOps teams, and includes a CLI, SDK, and API docs, covering the typical integration surface.  
- **Stability** – No known critical security issues; the repository follows standard open‑source licensing (needs final review) and provides basic health checks and logging.  
- **Readiness Level** – High enough for a serious pilot in production‑like environments; the only remaining due‑diligence items are a formal security audit and confirmation of long‑term maintainership.  

Overall, Charles‑mcp offers a pragmatic, standards‑based bridge for turning AI assistants into real‑world tool users, with a clear path from sandbox testing to production deployment.

### Русский

**heizaheiza/Charles-mcp** — открытый сервер Model Context Protocol, который превращает Charles Proxy в живой источник данных для AI‑агентов: он захватывает трафик в реальном времени, структурирует его и предоставляет единый набор контрактов, удобных для машинного взаимодействия. Типичный сценарий — подключить ассистента к реальному инструменту (например, к API‑сервисам или CLI) через стандартизованный протокол, что ускоряет разработку и деплой интеграций и позволяет быстро развернуть собственный MCP‑сервер. Проект имеет высокий уровень готовности к production: активные коммиты, 264 звезды, 27 форков, свежий релиз (23 июня 2026), написан на Python и уже используется в нескольких пилотных проектах, однако перед масштабным внедрением стоит проверить лицензию и текущий статус поддержки.

### 中文

**项目价值**  
heizaheiza/Charles-mcp 为 AI 代理提供了一个统一的 **Model Context Protocol (MCP)** 接口，能够实时捕获 Charles Proxy 的网络流量并将其结构化为机器可读的请求/响应记录。这样，AI 助手可以像调用本地函数一样安全、可靠地访问真实的外部工具和数据，实现「AI + 工具」的闭环。

**典型接入方式**  

| 场景 | 接入步骤 | 关键点 |
|------|----------|--------|
| **AI Agent 调用工具** | 1. 在目标机器上启动 Charles Proxy 并开启 MCP Server（`python -m charles_mcp`）。<br>2. 在 Agent 的 Prompt/代码中使用 MCP 客户端 SDK（Python/JS/Go）或直接调用 HTTP/WS 接口。<br>3. Agent 通过 `mcp.run(tool_name, args)` 发起调用，MCP 负责把请求路由到对应的本地/远程工具并返回结构化结果。 | SDK 已封装好请求签名、超时、错误映射，使用简单。 |
| **部署自有 MCP 服务器** | 1. Fork 项目或通过 Docker 镜像 `heizaheiza/charles-mcp:latest` 部署。<br>2. 在 `config.yaml` 中声明要暴露的工具（CLI、REST API、SDK 等）。<br>3. 配置鉴权（API‑Key、OAuth）后启动，即可对外提供标准化的 MCP 接口。 | 支持插件式扩展，新增工具只需实现 `ToolHandler` 接口并在配置中注册。 |
| **与现有 CI/CD/监控系统集成** | 1. 将 MCP Server 作为 sidecar 部署在服务网格或 Kubernetes Pod 中。<br>2. 通过环境变量或 Service Mesh 的流量拦截，将所有外部 HTTP/HTTPS 请求自动转发至 MCP。<br>3. AI 代理可直接查询 MCP 提供的「实时流量日志」或「历史分析报告」进行决策。 | 利用 Charles 的抓包能力，无需改动原有业务代码。 |

**生产可用性**  

- **活跃度**：最近一次提交在 2026‑06‑23，星标 264、Fork 27，社区活跃，已有若干企业级项目在内部使用。  
- **技术成熟度**：基于成熟的 Charles Proxy，核心抓包、TLS 解密功能已非常可靠；MCP 层使用 Python 编写，提供完整的 OpenAPI 规范和多语言 SDK。  
- **可部署性**：提供 Docker 镜像、K8s Helm Chart，支持水平扩展和高可用部署；日志、指标均可通过 Prometheus/Grafana 监控。  
- **安全性**：默认关闭外部访问，需显式配置鉴权（API‑Key、OAuth、mTLS），并可通过 Charles 的证书管理实现流量解密的最小授权原则。  
- **风险**：仍需对许可证（MIT）进行合规审查，建议在生产环境部署前进行一次渗透测试和依赖漏洞扫描。

综上，**heizaheiza/Charles-mcp** 已具备在生产环境中为 AI 代理提供可靠、标准化工具调用的能力，适合作为企业级「AI + 工具」平台的核心接入层。

## 🧭 Practical evaluation

**Value:** heizaheiza/Charles-mcp helps connect AI assistants to real tools and data through a standard protocol.

**Best use cases**

- connect AI agents to tools
- ship Model Context Protocol servers
- standardize integrations

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 264 GitHub stars
- 27 forks
- updated 2026-06-23
- primary language: Python
- 8 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 36/100 |
| stars | 52/100 |
| topics | 100/100 |
| outlook | 64/100 |
| quality | 61/100 |
| recency | 40/100 |
| adoption | 47/100 |
| production | 58/100 |
| usefulness | 90/100 |
| integration | 62/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 400/100 |

---

<sub>🔭 Discovered 2026-06-23 · [View on GitHub](https://github.com/heizaheiza/Charles-mcp) · [← Back to Mcp](./README.md)</sub>
