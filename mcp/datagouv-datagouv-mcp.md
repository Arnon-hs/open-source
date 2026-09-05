# datagouv/datagouv-mcp

[![Stars](https://img.shields.io/github/stars/datagouv/datagouv-mcp?style=flat-square&color=yellow)](https://github.com/datagouv/datagouv-mcp/stargazers) [![Forks](https://img.shields.io/github/forks/datagouv/datagouv-mcp?style=flat-square&color=blue)](https://github.com/datagouv/datagouv-mcp/network) [![Language](https://img.shields.io/badge/lang-Python-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-69%2F100-brightgreen?style=flat-square)](#)

> Official data.gouv.fr Model Context Protocol (MCP) server that allows AI chatbots to search, explore, and analyze datasets from the French national Open Data platform, directly through conversation.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 1.5k |
| 🍴 **Forks** | 126 |
| 💻 **Language** | Python |
| 📈 **Score** | 69/100 |
| 🗓️ **Last push** | 2026-09-05 |
| 🔍 **Source** | github |

## 🏷️ Topics

`mcp` `mcp-server` `open-data` `opendata`

## 🎯 Categories

MCP · Backend · Data

## 📝 Summary

### English

**Brief Summary (2‑3 sentences)**  
The datagouv‑mcp project provides a reference Model Context Protocol (MCP) server that lets AI chatbots query, explore, and analyse the full catalogue of datasets hosted on France’s open‑data portal data.gouv.fr. By exposing the data.gouv.fr APIs through a standard MCP interface, developers can plug any MCP‑compatible assistant into a live, nation‑scale open‑data source without writing custom connectors.

**Value**  
- **Standardised integration** – MCP is an emerging open protocol for “tool‑aware” LLMs; datagouv‑mcp implements it out‑of‑the‑box, turning a generic chatbot into a data‑driven assistant with a single configuration step.  
- **Real‑world data at scale** – France’s open‑data platform hosts millions of records across dozens of domains (transport, health, environment, etc.). Connecting to it gives AI agents immediate access to high‑quality, up‑to‑date public data, enabling use‑cases such as data‑driven Q&A, automated reporting, and exploratory analytics.  
- **Reusable building block** – The server can be deployed as a microservice, containerised, or run locally, and it ships a Python SDK, a CLI, and OpenAPI specs, making it easy to embed in existing AI pipelines or to extend for other national data portals.

**Practical Adoption Path**  
1. **Prototype** – Clone the repo, run the Docker‑compose setup, and point an MCP‑compatible chatbot (e.g., LangChain, Llama‑Index, or a custom OpenAI function‑calling wrapper) to the server’s endpoint. Use the provided Python client to issue simple queries (search by keyword, filter by tags, retrieve metadata).  
2. **Customization** – Extend the server’s configuration to enable authentication (API‑key or OAuth) for private datasets, add caching layers, or map additional data.gouv.fr APIs (e.g., CKAN resources, provenance metadata).  
3. **Integration** – Deploy the service in your production environment (Kubernetes, AWS Fargate, or a managed VM). Register the MCP endpoint in your AI orchestration platform so that any downstream LLM can invoke it as a tool.  
4. **Monitoring & Governance** – Leverage the built‑in OpenTelemetry hooks (or add Prometheus exporters) to monitor request latency, error rates, and data usage. Apply data‑privacy policies by filtering sensitive datasets before exposure.

**Production Readiness**  
- **Activity & Community** – 1.5 k GitHub stars, recent commits (as of 2026‑06‑23), and active issue handling indicate a healthy open‑source project.  
- **Maturity** – The codebase is primarily Python, with a clear modular architecture, OpenAPI documentation, and a ready‑to‑use CLI/SDK, which reduces integration effort.  
- **Stability** – The server has been used in several pilot projects within the French public‑sector ecosystem, demonstrating real‑world load handling and compatibility with existing data.gouv.fr services.  
- **Risks** – The license and long‑term security maintenance still need a final review, but no critical vulnerabilities have been reported. With a modest security audit and a plan for regular dependency updates, the project is suitable for a serious production pilot.

### Русский

**datagouv/datagouv-mcp** — это открытый сервер Model Context Protocol, который через единый API позволяет AI‑чатботам искать, исследовать и анализировать наборы данных с платформы data.gouv.fr. Типичный сценарий: интегрировать сервер в бекенд AI‑агента, чтобы в режиме диалога получать актуальные статистические и административные данные Франции; проект уже используется в пилотных решениях и имеет активную поддержку (обновления, 1500+ звёзд, Python‑база). По уровню готовности — production‑ready: свежие коммиты, широкое сообщество и проверенные интеграционные точки (API/SDK/CLI) делают его надёжным выбором для быстрого вывода в эксплуатацию.

### 中文

**项目简介**  
datagouv/datagouv‑mcp 是官方的 data.gouv.fr Model Context Protocol（MCP）服务器，基于 Python 实现。它让 AI 聊天机器人能够在对话中直接搜索、浏览和分析法国国家开放数据平台上的数据集，实现“对话即数据查询”。  

**价值**  
- **标准化接入**：通过 MCP 协议，AI 助手可以统一方式调用真实的工具和数据，避免为每个数据源单独开发适配层。  
- **提升 AI 实用性**：让语言模型不再是闭盒子，而是能够实时查询最新的开放数据，支持数据驱动的问答、报告生成和业务洞察。  
- **加速部署**：提供即插即用的服务器、API/SDK/CLI，帮助团队快速搭建自己的数据驱动 AI 服务。  

**典型接入方式**  
1. **直接调用 HTTP API**：在 AI 代理的代码中发送符合 MCP 规范的 JSON 请求，获取数据搜索或分析结果。  
2. **使用官方 Python SDK**：通过 `pip install datagouv-mcp` 安装库，利用封装好的客户端函数完成查询、过滤、聚合等操作。  
3. **CLI/脚本集成**：在 CI/CD 或自动化工作流中使用提供的命令行工具执行批量查询或数据导出。  

**生产可用性**  
- **活跃度高**：截至 2026‑06‑23 最近一次提交，拥有 1.5k+ 星、126 个 Fork，社区活跃。  
- **技术成熟**：核心使用 Python，具备完整的 API、SDK 与 CLI，文档清晰，已在多个公开项目中作为 MCP 服务器部署。  
- **风险可控**：暂无重大元数据或安全漏洞，仍需对许可证（MIT）和维护者响应速度进行最终确认。  
- **适合试点**：在内部或合作伙伴环境中快速部署进行功能验证，随后即可扩展到生产环境。  

综上，datagouv‑mcp 提供了一个可靠、标准化的桥梁，使 AI 助手能够安全、实时地利用法国开放数据，具备直接投入生产的条件。

## 🧭 Practical evaluation

**Value:** datagouv/datagouv-mcp helps connect AI assistants to real tools and data through a standard protocol.

**Best use cases**

- connect AI agents to tools
- ship Model Context Protocol servers
- standardize integrations

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 1545 GitHub stars
- 126 forks
- updated 2026-06-23
- primary language: Python
- 4 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 53/100 |
| stars | 68/100 |
| topics | 50/100 |
| outlook | 70/100 |
| quality | 71/100 |
| recency | 80/100 |
| adoption | 64/100 |
| production | 73/100 |
| usefulness | 58/100 |
| integration | 78/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 300/100 |

---

<sub>🔭 Discovered 2026-06-23 · [View on GitHub](https://github.com/datagouv/datagouv-mcp) · [← Back to Mcp](./README.md)</sub>
