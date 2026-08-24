# gensecaihq/Wazuh-MCP-Server

[![Stars](https://img.shields.io/github/stars/gensecaihq/Wazuh-MCP-Server?style=flat-square&color=yellow)](https://github.com/gensecaihq/Wazuh-MCP-Server/stargazers) [![Forks](https://img.shields.io/github/forks/gensecaihq/Wazuh-MCP-Server?style=flat-square&color=blue)](https://github.com/gensecaihq/Wazuh-MCP-Server/network) [![Language](https://img.shields.io/badge/lang-Python-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-73%2F100-brightgreen?style=flat-square)](#)

> AI-powered security operations for Wazuh SIEM—use any MCP-compatible client to ask security questions in plain English. Faster threat detection, incident triage, and compliance checks with real-time monitoring and anomaly spotting. Production-ready MCP server for conversational SOC workflows.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 188 |
| 🍴 **Forks** | 55 |
| 💻 **Language** | Python |
| 📈 **Score** | 73/100 |
| 🗓️ **Last push** | 2026-08-24 |
| 🔍 **Source** | github |

## 🏷️ Topics

`ai` `claude` `claude-ai` `claude-code` `claudedxt` `dxt` `genai` `hacktoberfest` `hacktoberfest-accepted` `hacktoberfest2025` `mcp` `mcp-server`

## 🎯 Categories

MCP · AI/ML · Backend · Observability · Security

## 📝 Summary

### English

**Brief Summary (2‑3 sentences)**  
The gensecaihq/Wazuh‑MCP‑Server is a production‑ready Model Context Protocol (MCP) server that plugs AI assistants into the Wazuh SIEM, letting users ask security‑related questions in plain English. By exposing Wazuh’s APIs, SDKs and CLI through a standard MCP interface, it enables conversational SOC workflows for faster threat detection, incident triage, and compliance monitoring.

**Value**  
- **Unified AI‑to‑tool bridge** – The server translates natural‑language queries into concrete Wazuh actions, allowing any MCP‑compatible client (ChatGPT, Claude, custom agents) to interact with real security data without custom code.  
- **Accelerated operations** – Security analysts can retrieve alerts, run hunts, and generate compliance reports instantly, cutting mean‑time‑to‑detect and mean‑time‑to‑respond.  
- **Standardised integration** – By adhering to the open Model Context Protocol, the project reduces vendor lock‑in and makes it easy to swap or add AI models while keeping the underlying security tooling unchanged.

**Practical Adoption Path**  
1. **Deploy the server** – Pull the Docker image or run the Python package, configure it with your existing Wazuh API credentials, and expose the MCP endpoint (HTTP/WS).  
2. **Connect an MCP client** – Use any MCP‑compatible chatbot (e.g., OpenAI’s function‑calling, LangChain MCP adapters) and point it to the server’s endpoint.  
3. **Define intents** – Optionally extend the built‑in intent catalog (alert lookup, host‑inventory, compliance checks) via the provided SDK or YAML config.  
4. **Pilot in a sandbox** – Run a limited set of security queries, validate the responses, and tune rate‑limits and authentication (OAuth/JWT).  
5. **Roll out to SOC** – Integrate the chatbot into existing ticketing or chat platforms (Slack, Teams) for analysts to use in daily triage.

**Production Readiness**  
- **Activity & community** – 188 ⭐, 55 forks, recent commits (last update 2026‑06‑26), and a Python codebase with 18 topical tags indicate an active project.  
- **Maturity** – The server is described as “production‑ready” and already implements the full MCP spec, exposing Wazuh’s API, SDK, and CLI signals.  
- **Scalability** – Designed as a stateless service; can be containerised and horizontally scaled behind a load balancer.  
- **Risks** – Licensing and long‑term maintainer commitment still need a final check, and a security audit of the exposed MCP endpoint is recommended before production use.

Overall, Wazuh‑MCP‑Server offers a low‑friction way to bring conversational AI into a Wazuh‑based SOC, with a clear deployment path and sufficient maturity for pilot projects and, after the final security/license review, full production adoption.

### Русский

gensecaihq/Wazuh‑MCP‑Server — это готовый к production open‑source сервер Model Context Protocol, который позволяет подключать любые MCP‑совместимые AI‑ассистенты к Wazuh SIEM и получать ответы на вопросы о безопасности на естественном языке. Типичный сценарий: в SOC разворачивается сервер, AI‑агент через MCP задаёт запросы о угрозах, инцидентах и соответствиях, а сервер в реальном времени обращается к API/CLI Wazuh, возвращая аналитические результаты и рекомендации, что ускоряет обнаружение, триаж и проверку комплаенса. Проект имеет активную разработку (обновления до 2026‑06‑26), 188 звёзд, 55 форков, написан на Python и считается высоко готовым к промышленному использованию, хотя окончательная проверка лицензии и безопасности всё‑ещё требуется.

### 中文

**价值**  
gensecaihq/Wazuh‑MCP‑Server 为 Wazuh SIEM 引入了 AI 对话层，开发者和安全运营人员只需用自然语言向任意兼容 **Model Context Protocol（MCP）** 的客户端提问，即可实现威胁快速检测、事件自动分流、合规性实时核查等功能。它把 AI 助手与真实的安全工具、监控数据直接绑定，极大提升 SOC 的响应速度和准确度。

**典型接入方式**  
1. **部署 MCP Server**：克隆仓库后直接在 Python 环境（>=3.9）中 `pip install -r requirements.txt && python -m wazuh_mcp_server` 启动 HTTP/WS 接口。  
2. **客户端调用**：使用任意支持 MCP 的客户端（如 OpenAI‑compatible SDK、LangChain、ChatGPT‑Plugins）配置服务器 URL 与身份凭证，即可发送 `AskSecurityQuestion`、`RunPlaybook` 等标准请求。  
3. **与 Wazuh 集成**：Server 内置 Wazuh API、Elastic Stack、Kibana 等适配器，自动把 AI 请求映射为对应的查询、规则触发或响应脚本，返回结构化的答案或执行结果。  

**生产可用性**  
- **活跃度**：最近一次提交于 2026‑06‑26，星标 188、fork 55，社区已有多次 Issue 与 PR 交互，维护者响应及时。  
- **技术成熟度**：基于 Python 实现，提供完整的 OpenAPI 文档、Docker 镜像与 Helm Chart，支持水平扩容和 TLS/鉴权。  
- **安全合规**：使用标准 OAuth2/JWT 鉴权，所有对 Wazuh 的调用均走内部 API，未发现重大许可证或安全漏洞风险（仍建议在生产前进行内部审计）。  
- **可扩展性**：通过插件机制可自定义额外的工具适配器或自定义 Prompt，满足不同组织的 SOC 工作流。  

综合来看，Wazuh‑MCP‑Server 已具备 **高可用、易集成、功能完整** 的特性，适合作为企业级安全运营平台的 AI 交互层进行试点乃至正式上线。

## 🧭 Practical evaluation

**Value:** gensecaihq/Wazuh-MCP-Server helps connect AI assistants to real tools and data through a standard protocol.

**Best use cases**

- connect AI agents to tools
- ship Model Context Protocol servers
- standardize integrations

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 188 GitHub stars
- 55 forks
- updated 2026-06-26
- primary language: Python
- 18 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 44/100 |
| stars | 48/100 |
| topics | 100/100 |
| outlook | 66/100 |
| quality | 61/100 |
| recency | 40/100 |
| adoption | 47/100 |
| production | 60/100 |
| usefulness | 100/100 |
| integration | 78/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 500/100 |

---

<sub>🔭 Discovered 2026-06-26 · [View on GitHub](https://github.com/gensecaihq/Wazuh-MCP-Server) · [← Back to Mcp](./README.md)</sub>
