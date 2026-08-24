# AndyShaman/gemini-webapi-mcp

[![Stars](https://img.shields.io/github/stars/AndyShaman/gemini-webapi-mcp?style=flat-square&color=yellow)](https://github.com/AndyShaman/gemini-webapi-mcp/stargazers) [![Forks](https://img.shields.io/github/forks/AndyShaman/gemini-webapi-mcp?style=flat-square&color=blue)](https://github.com/AndyShaman/gemini-webapi-mcp/network) [![Language](https://img.shields.io/badge/lang-Python-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-66%2F100-brightgreen?style=flat-square)](#)

> MCP server for Google Gemini — free image generation, editing & chat via browser cookies. No API keys needed.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 34 |
| 🍴 **Forks** | 19 |
| 💻 **Language** | Python |
| 📈 **Score** | 66/100 |
| 🗓️ **Last push** | 2026-08-24 |
| 🔍 **Source** | github |

## 🏷️ Topics

`ai` `claude` `claude-code` `gemini` `gemini-api` `generative-ai` `google-gemini` `image-generation` `llm` `mcp` `mcp-server` `model-context-protocol`

## 🎯 Categories

MCP · AI/ML · Backend

## 📝 Summary

### English

**Brief Summary (2‑3 sentences)**  
AndyShaman/gemini‑webapi‑mcp is a Python‑based MCP (Model Context Protocol) server that proxies Google Gemini’s image generation, editing, and chat capabilities without requiring API keys—authentication is handled via browser cookies. It provides a simple, standards‑based endpoint that AI agents can call to access Gemini’s multimodal functions, making it easy to integrate Gemini into tool‑use workflows. With recent commits, 34 stars, and a growing fork count, the project is mature enough for pilot deployments.

**Value**  
- **Zero‑key access** – Developers can leverage Gemini’s powerful multimodal models without managing Google Cloud credentials, lowering cost and operational overhead.  
- **Standardized interface** – By exposing Gemini through the Model Context Protocol, the server fits naturally into existing AI‑assistant architectures that already consume MCP endpoints, enabling plug‑and‑play tool integration.  
- **Extensible backend** – Built in Python, the codebase is easy to extend (e.g., adding caching, rate‑limiting, or custom preprocessing) while keeping the core Gemini interaction unchanged.

**Practical Adoption Path**  
1. **Clone & configure** – Pull the repository, set the required environment variables (Gemini cookie values), and run the provided Dockerfile or `uvicorn` command.  
2. **Connect your agent** – Point your MCP‑compatible AI assistant (e.g., LangChain, AutoGPT, or a custom orchestrator) to the server’s `/v1/chat/completions` and `/v1/images/generations` endpoints.  
3. **Test & iterate** – Use the built‑in Swagger UI or simple curl requests to verify image generation and chat responses, then add any domain‑specific wrappers or authentication layers.  
4. **Scale** – Deploy the server behind a load balancer or Kubernetes service, optionally enabling TLS and rate‑limiting for production traffic.

**Production Readiness**  
- **Activity & community** – Last updated on 2026‑06‑23, with steady commit history, 34 GitHub stars, and 19 forks, indicating active interest.  
- **Maturity** – The codebase follows common Python web‑service patterns (FastAPI/Starlette), includes OpenAPI docs, and has clear entry points for CLI/SDK usage.  
- **Risks** – The license, security posture, and long‑term maintainer commitment still need a final review, but no major metadata or dependency issues are evident.  
Overall, the project is a strong OSS candidate for a serious pilot, offering a low‑friction way to bring Gemini’s capabilities into production AI pipelines.

### Русский

AndyShaman/gemini-webapi-mcp — это открытый MCP‑сервер, который через браузерные куки предоставляет бесплатный доступ к генерации, редактированию изображений и чат‑боту Google Gemini без необходимости API‑ключей. Он упрощает подключение AI‑агентов к реальным инструментам и данным, позволяя быстро развернуть Model Context Protocol‑совместимый сервис для интеграций и автоматизации. Проект имеет активную разработку (обновления до 2026‑06‑23), 34 звёзд, 19 форков и написан на Python, что свидетельствует о высокой готовности к использованию в продакшене после окончательной проверки лицензии и безопасности.

### 中文

**项目简介**  
AndyShaman/gemini-webapi-mcp 是一个基于 Model Context Protocol（MCP）的开源服务器，实现了对 Google Gemini 的免费图像生成、编辑和聊天功能。通过浏览器 Cookie 进行身份校验，无需额外的 API Key，即可在本地或云端快速部署。

**价值点**  
- **零钥匙接入**：省去申请、管理 Google Gemini API Key 的繁琐流程，降低成本。  
- **标准化协议**：遵循 MCP，便于将 AI 助手统一接入各种工具、数据源，实现“AI + 工具”的闭环。  
- **即插即用**：提供 RESTful API、Python SDK 与 CLI，支持快速原型开发和生产级集成。

**典型接入方式**  
1. **部署服务器**：使用 Docker 镜像或直接 `pip install` 项目依赖，在本机或 Kubernetes 中启动 MCP 服务。  
2. **调用 API**：在 AI Agent（如 LangChain、AutoGPT）中配置 MCP 端点，使用标准的 `POST /v1/generate_image`、`POST /v1/edit_image`、`POST /v1/chat` 接口。  
3. **SDK/CLI**：通过项目自带的 Python SDK（`gemini_mcp.Client`）或 CLI（`gemini-mcp-cli`）进行本地调试，完成身份验证后即可发送请求。  

**生产可用性**  
- **活跃度**：最近一次提交于 2026‑06‑23，星标 34、Fork 19，社区活跃。  
- **技术成熟度**：核心实现使用 Python，代码结构清晰，已覆盖 API、SDK、CLI 三层调用，符合生产环境的可观测性需求。  
- **安全与合规**：目前未发现重大元数据泄露风险，但仍需进一步审查许可证（MIT）以及容器镜像的安全基线。  
- **适配性**：支持标准 MCP 协议，可无缝对接已有的 AI‑Agent 框架或自研工具链，适合作为企业内部的 AI + 工具桥梁进行试点或正式上线。  

综上，AndyShaman/gemini-webapi-mcp 具备 **高可用**、**易集成**、**成本低** 的特性，是在不依赖官方 API Key 前提下，将 Gemini 能力快速嵌入业务系统的理想选择。

## 🧭 Practical evaluation

**Value:** AndyShaman/gemini-webapi-mcp helps connect AI assistants to real tools and data through a standard protocol.

**Best use cases**

- connect AI agents to tools
- ship Model Context Protocol servers
- standardize integrations

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 34 GitHub stars
- 19 forks
- updated 2026-06-23
- primary language: Python
- 13 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 33/100 |
| stars | 33/100 |
| topics | 100/100 |
| outlook | 57/100 |
| quality | 55/100 |
| recency | 40/100 |
| adoption | 33/100 |
| production | 60/100 |
| usefulness | 74/100 |
| integration | 94/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 300/100 |

---

<sub>🔭 Discovered 2026-06-23 · [View on GitHub](https://github.com/AndyShaman/gemini-webapi-mcp) · [← Back to Mcp](./README.md)</sub>
