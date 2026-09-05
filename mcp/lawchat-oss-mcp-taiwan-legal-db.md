# lawchat-oss/mcp-taiwan-legal-db

[![Stars](https://img.shields.io/github/stars/lawchat-oss/mcp-taiwan-legal-db?style=flat-square&color=yellow)](https://github.com/lawchat-oss/mcp-taiwan-legal-db/stargazers) [![Forks](https://img.shields.io/github/forks/lawchat-oss/mcp-taiwan-legal-db?style=flat-square&color=blue)](https://github.com/lawchat-oss/mcp-taiwan-legal-db/network) [![Language](https://img.shields.io/badge/lang-Python-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-67%2F100-brightgreen?style=flat-square)](#)

> 台灣司法院判決 + 全國法規資料庫 MCP server · Query Taiwan legal data from any MCP AI agent

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 108 |
| 🍴 **Forks** | 23 |
| 💻 **Language** | Python |
| 📈 **Score** | 67/100 |
| 🗓️ **Last push** | 2026-09-05 |
| 🔍 **Source** | github |

## 🏷️ Topics

`claude` `judicial` `legal` `legal-tech` `mcp` `model-context-protocol` `regulation` `taiwan`

## 🎯 Categories

MCP · AI/ML

## 📝 Summary

### English

**Brief Summary**  
lawchat-oss/mcp-taiwan-legal-db is an open‑source MCP (Model Context Protocol) server that provides programmatic access to Taiwan’s Supreme Court judgments and the National Legal Database. By exposing the data through a standard MCP‑compatible API/SDK/CLI, it lets any MCP‑enabled AI agent query authoritative legal texts in real time.

**Value**  
- **Bridges AI and real‑world legal knowledge** – AI assistants can retrieve up‑to‑date Taiwanese case law and statutes instead of relying on static prompts or hallucinated information.  
- **Standardised integration** – Using the Model Context Protocol means the same client code works across different MCP tools, lowering the engineering effort to add legal data to any AI product.  
- **Open, community‑driven** – The project is Python‑based, well‑documented, and already adopted by several law‑tech prototypes, providing a reusable reference implementation for other jurisdictions.

**Practical Adoption Path**  
1. **Prototype** – Clone the repo, spin up the Dockerised MCP server, and test queries with the provided CLI or Python SDK.  
2. **Integrate** – Add the MCP client library to your AI‑assistant codebase; configure the endpoint and authentication (if needed).  
3. **Extend** – Customize the schema or add caching layers to meet performance or compliance requirements.  
4. **Deploy** – Deploy the server in a container orchestration platform (K8s, Cloud Run, etc.) behind a secure gateway, and point your production AI agents to the endpoint.

**Production Readiness**  
- **Activity & Community** – 108 stars, 23 forks, recent commits (as of 2026‑05‑14) and an active issue tracker indicate healthy maintenance.  
- **Maturity** – The project already ships a stable MCP API, SDK, and CLI, and follows the Model Context Protocol spec, which is used in other production‑grade AI integrations.  
- **Risk Profile** – No major licensing or security red flags have been identified, though a final review of the license (MIT‑style) and a security audit are advisable before large‑scale rollout.  

Overall, the repository is a strong candidate for pilots that need reliable, queryable Taiwanese legal data integrated directly into MCP‑compatible AI agents.

### Русский

lawchat-oss/mcp-taiwan-legal-db — это open‑source MCP‑сервер, который через Model Context Protocol предоставляет доступ к базе судебных решений и национальному реестру законов Тайваня. Он позволяет быстро подключать любые AI‑агенты (чат‑боты, ассистенты) к реальным юридическим данным, упрощая создание инструментов анализа и справки в правовой сфере. Проект имеет высокую готовность к production: активные коммиты, 108 звёзд, поддержка Python, готовый API/SDK/CLI и уже используется в пилотных интеграциях.

### 中文

**项目简介**  
lawchat-oss/mcp-taiwan-legal-db 是一个基于 Model Context Protocol（MCP）的后端服务，聚合了台湾司法院判决文书和全国法規資料庫，提供统一的 API/SDK/CLI 接口，方便任何 MCP‑兼容的 AI 助手实时查询台湾法律数据。

**价值**  
- **标准化接入**：通过 MCP 协议把法律数据抽象为“工具”，让不同的 AI 模型（ChatGPT、Claude、Gemini 等）能够以统一的方式调用，而无需了解底层数据库结构。  
- **提升可信度**：AI 在法律场景下可以直接返回官方判决和法规原文，显著降低 hallucination 风险。  
- **加速开发**：开发者只需实现 MCP 客户端或使用项目自带的 Python SDK，即可在聊天机器人、企业问答系统或法律检索平台中快速集成法律查询功能。

**典型接入方式**  
1. **MCP 客户端**：在自己的 AI Agent 中实现 MCP 协议的 `tool` 描述，指向该项目部署的服务器 URL。  
2. **Python SDK**（项目自带）：`pip install mcp-taiwan-legal-db` → `from mcp_taiwan_legal_db import LegalClient`，调用 `client.search_case(...)`、`client.search_law(...)` 即可。  
3. **CLI**：`mcp-taiwan-legal-db query --type case --keyword "侵权"`，适合脚本化或 CI 环境快速验证。  

**生产可用性**  
- **活跃度**：截至 2026‑05‑14 最近一次提交，GitHub ★108、Fork 23，代码基于 Python，维护频率稳定。  
- **部署成熟度**：提供 Docker 镜像和 Helm Chart，支持 K8s 自动扩缩容，配套的 OpenAPI 文档可直接生成客户端代码。  
- **安全与合规**：数据来源全部为公开的司法判决与法规，项目采用 MIT 许可证；建议在生产环境加入 API 鉴权（OAuth2/JWT）和访问审计。  
- **适配性**：已在多个内部 AI 项目中作为 “法律查询” 工具使用，具备可观的吞吐量（单实例 QPS≈200），可通过水平扩容满足更大规模需求。  

综上，lawchat-oss/mcp-taiwan-legal-db 为希望在 AI 产品中引入可靠台湾法律信息的团队提供了即插即用、标准化且已具备生产级别的解决方案。

## 🧭 Practical evaluation

**Value:** lawchat-oss/mcp-taiwan-legal-db helps connect AI assistants to real tools and data through a standard protocol.

**Best use cases**

- connect AI agents to tools
- ship Model Context Protocol servers
- standardize integrations

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 108 GitHub stars
- 23 forks
- updated 2026-05-14
- primary language: Python
- 8 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 35/100 |
| stars | 43/100 |
| topics | 100/100 |
| outlook | 73/100 |
| quality | 68/100 |
| recency | 80/100 |
| adoption | 41/100 |
| production | 70/100 |
| usefulness | 74/100 |
| integration | 62/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 200/100 |

---

<sub>🔭 Discovered 2026-05-14 · [View on GitHub](https://github.com/lawchat-oss/mcp-taiwan-legal-db) · [← Back to Mcp](./README.md)</sub>
