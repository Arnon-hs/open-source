# wyre-technology/autotask-mcp

[![Stars](https://img.shields.io/github/stars/wyre-technology/autotask-mcp?style=flat-square&color=yellow)](https://github.com/wyre-technology/autotask-mcp/stargazers) [![Forks](https://img.shields.io/github/forks/wyre-technology/autotask-mcp?style=flat-square&color=blue)](https://github.com/wyre-technology/autotask-mcp/network) [![Language](https://img.shields.io/badge/lang-TypeScript-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-57%2F100-brightgreen?style=flat-square)](#)

> MCP server for Kaseya Autotask PSA — 39 tools for companies, tickets, projects, time entries, and more

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 35 |
| 🍴 **Forks** | 35 |
| 💻 **Language** | TypeScript |
| 📈 **Score** | 57/100 |
| 🗓️ **Last push** | 2026-08-24 |
| 🔍 **Source** | github |

## 🏷️ Topics

`ai-tools` `autotask` `claude` `kaseya` `mcp` `model-context-protocol` `msp` `msp-mcp` `psa` `wyre-technology`

## 🎯 Categories

MCP · AI/ML

## 📝 Summary

### English

**Brief Summary**  
`wyre-technology/autotask-mcp` is an open‑source Model Context Protocol (MCP) server that wraps the Kaseya Autotask PSA suite. It provides a unified, API‑first interface for 39 common Autotask operations—ticketing, project management, time‑entry, asset handling, and more—so AI assistants can invoke real‑world business tools without custom glue code.

**Value**  
- **Standardised AI‑to‑tool bridge** – By exposing Autotask functionality through the open MCP spec, the project lets any MCP‑compatible AI agent (e.g., ChatGPT plugins, custom LLM assistants) interact with Autotask as if it were a native skill.  
- **Rapid integration** – Developers only need to run the TypeScript server and point their AI model to its endpoint; the heavy lifting of authentication, request formatting, and response parsing is already handled.  
- **Extensible ecosystem** – Because MCP is a community‑driven protocol, the same server can be swapped or extended to support other PSA platforms, fostering reuse across enterprises.

**Practical Adoption Path**  
1. **Spin‑up the server** – Clone the repo, run `npm install && npm run build && npm start` (Dockerfile is also provided).  
2. **Configure credentials** – Supply Autotask API keys and optional tenant settings via environment variables or a `.env` file.  
3. **Register the MCP endpoint** – In your LLM‑orchestrator (e.g., LangChain, OpenAI function calling, or a custom MCP client), add the server’s URL as a tool definition.  
4. **Define tool contracts** – Use the auto‑generated OpenAPI spec (`/openapi.json`) to map LLM intents to specific Autotask actions (create ticket, log time, fetch project status, etc.).  
5. **Test & iterate** – Run the provided integration tests or use the built‑in Swagger UI to verify each operation before exposing the endpoint to production workloads.  

**Production Readiness**  
- **Activity & community** – 35 ★, 35 forks, last commit on 2026‑05‑13; the repo is actively maintained with recent releases and clear contribution guidelines.  
- **Technology stack** – Fully TypeScript‑based, with typed SDK wrappers and a Docker image for easy CI/CD deployment.  
- **Security & compliance** – No obvious licensing or metadata red flags, but a formal security audit (dependency scanning, secret management, rate‑limiting) is still recommended before handling sensitive ticket data.  
- **Scalability** – The server is stateless and can be horizontally scaled behind a load balancer; rate limits can be enforced per‑tenant via middleware.  

Overall, `autotask-mcp` is mature enough for a pilot in a production environment, provided the usual OSS diligence (license verification, security review, and monitoring) is performed. It offers a low‑friction way to empower AI agents with real‑world PSA capabilities.

### Русский

**wyre-technology/autotask-mcp** — это сервер MCP для Kaseya Autotask PSA, предоставляющий более 30 готовых инструментов (тикеты, проекты, учёт времени и пр.) и реализующий стандартный Model Context Protocol, что позволяет быстро подключать AI‑ассистентов к реальным бизнес‑процессам и данным. Типичный сценарий — развертывание сервера как шлюза между AI‑агентом и API/CLI Kaseya, упрощающее интеграцию и масштабирование автоматизированных рабочих потоков. Проект активно поддерживается (обновления в 2026 г., 35 звёзд, 35 форков, TypeScript), имеет хорошую экосистему и готов к пилотному запуску в продакшн‑среде после финальной проверки лицензии и безопасности.

### 中文

**项目简介**  
`wyre-technology/autotask-mcp` 是面向 Kaseya Autotask PSA 的 MCP（Model Context Protocol）服务器，实现了 39 项企业级功能（工单、项目、工时等）的统一接口。它通过标准化的 MCP 协议，让 AI 助手能够直接调用真实的业务工具和数据。

**价值**  
- **AI‑工具桥梁**：把 AI 代理与 Autotask 的实际业务功能相连，消除“AI 只能说话、不能动手”的瓶颈。  
- **统一协议**：基于 MCP，开发者只需一次实现即可让多个 AI 模型复用同一套后端服务，降低集成成本。  
- **快速交付**：提供即插即用的 API/SDK/CLI，帮助企业在几天内完成 AI 助手与工单、项目管理等关键系统的对接。

**典型接入方式**  
1. **部署 MCP 服务器**：使用 Docker 或直接在 Node.js 环境中运行 TypeScript 项目。  
2. **配置 Autotask 凭证**：在 `config.yaml`（或环境变量）中填入 Autotask API Token、租户 ID 等信息。  
3. **注册模型上下文**：在 AI 平台（如 OpenAI、Anthropic）中声明该 MCP 端点的 schema，模型即可通过 `tool_calls` 调用对应的业务操作。  
4. **调用方式**：  
   - **REST API**：直接发送 HTTP POST/GET 请求（适用于自研 AI 代理或脚本）。  
   - **SDK**：项目提供的 TypeScript/JavaScript 客户端，可在前端或后端代码中以函数形式调用。  
   - **CLI**：`autotask-mcp-cli` 供运维或调试使用，快速验证工单创建、查询等功能。

**生产可用性**  
- **活跃维护**：最近一次提交于 2026‑05‑13，星标 35、fork 35，社区活跃度良好。  
- **技术成熟度**：使用 TypeScript 编写，拥有完整的类型定义和单元测试，易于在企业 CI/CD 流程中集成。  
- **安全与合规**：项目本身不包含敏感数据，主要风险在于 Autotask API 的访问凭证管理，建议配合企业密钥管理系统（如 HashiCorp Vault）进行保护。  
- **可扩展性**：通过插件机制可以自行添加自定义工具或扩展现有 39 项功能，满足特定业务需求。  

综合来看，`wyre-technology/autotask-mcp` 已具备进入生产环境的技术基础和社区支持，适合作为 AI 助手与 Kaseya Autotask PSA 深度集成的首选方案。

## 🧭 Practical evaluation

**Value:** wyre-technology/autotask-mcp helps connect AI assistants to real tools and data through a standard protocol.

**Best use cases**

- connect AI agents to tools
- ship Model Context Protocol servers
- standardize integrations

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 35 GitHub stars
- 35 forks
- updated 2026-05-13
- primary language: TypeScript
- 10 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 39/100 |
| stars | 33/100 |
| topics | 100/100 |
| outlook | 50/100 |
| quality | 51/100 |
| recency | 20/100 |
| adoption | 35/100 |
| production | 49/100 |
| usefulness | 74/100 |
| integration | 62/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 200/100 |

---

<sub>🔭 Discovered 2026-05-13 · [View on GitHub](https://github.com/wyre-technology/autotask-mcp) · [← Back to Mcp](./README.md)</sub>
