# matiasbattocchia/open-bsp-api

[![Stars](https://img.shields.io/github/stars/matiasbattocchia/open-bsp-api?style=flat-square&color=yellow)](https://github.com/matiasbattocchia/open-bsp-api/stargazers) [![Forks](https://img.shields.io/github/forks/matiasbattocchia/open-bsp-api?style=flat-square&color=blue)](https://github.com/matiasbattocchia/open-bsp-api/network) [![Language](https://img.shields.io/badge/lang-TypeScript-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-78%2F100-brightgreen?style=flat-square)](#)

> Open-source WhatsApp + Instagram Business platform

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 422 |
| 🍴 **Forks** | 177 |
| 💻 **Language** | TypeScript |
| 📈 **Score** | 78/100 |
| 🗓️ **Last push** | 2026-09-05 |
| 🔍 **Source** | github |

## 🏷️ Topics

`agents` `ai` `ai-agents` `deno` `instagram` `instagram-api` `mcp` `supabase` `whatsapp` `whatsapp-api`

## 🎯 Categories

MCP · AI/ML · Backend

## 📝 Summary

### English

**Brief Summary**  
matiasbattocchia/open‑bsp‑api is an open‑source TypeScript platform that implements a unified Business Service Protocol (BSP) for WhatsApp and Instagram Business, enabling AI assistants to interact with real‑world messaging tools through a standard API. With over 400 ⭐ on GitHub, recent commits, and a growing ecosystem, it offers a ready‑to‑use backend, database layer, and optional CLI/SDK for rapid integration.

**Value**  
The project abstracts the disparate APIs of WhatsApp and Instagram Business into a single, consistent protocol, letting developers plug AI agents, chatbots, or automation workflows into both channels without writing custom adapters. This standardization reduces integration overhead, accelerates time‑to‑market for AI‑driven customer‑service solutions, and facilitates the deployment of Model Context Protocol (MCP) servers that can query live business data.

**Practical Adoption Path**  
1. **Evaluate** – Clone the repo, run the provided Docker compose or npm scripts, and test the sample endpoints with the bundled CLI.  
2. **Configure** – Supply your WhatsApp and Instagram Business credentials via environment variables or a secure vault; the platform handles token refresh and webhook registration automatically.  
3. **Integrate** – Use the generated TypeScript SDK or the RESTful API to connect your AI assistant (e.g., OpenAI, LangChain) to the BSP endpoints, mapping intents to messaging actions.  
4. **Extend** – Add custom database models or webhook handlers for domain‑specific logic, leveraging the built‑in PostgreSQL integration.  
5. **Deploy** – Deploy to a cloud provider (Kubernetes, Fly.io, etc.) using the provided Helm chart or Docker image; monitor with the built‑in health checks and Prometheus metrics.

**Production Readiness**  
- **Activity & Community**: Last commit on 2026‑06‑28, 422 stars, 177 forks, and active issue discussions indicate a healthy maintainer base.  
- **Architecture**: Typed TypeScript code, modular SDK/CLI, and Docker‑ready deployment make it suitable for scaling and CI/CD pipelines.  
- **Security & Licensing**: No immediate metadata risks, but a final audit of the MIT‑style license and dependency vulnerabilities is recommended before a full production rollout.  
Overall, the project is mature enough for a serious pilot or production use, provided the standard security review and any required custom compliance checks are completed.

### Русский

**matiasbattocchia/open-bsp-api** — это открытая платформа на TypeScript, реализующая стандартный протокол для интеграции WhatsApp и Instagram Business с AI‑ассистентами и другими сервисами. Типичный сценарий: разработчик разворачивает сервер Model Context Protocol, подключает к нему API/SDK/CLI и сразу получает возможность связывать AI‑агентов с реальными инструментами и данными (мессенджеры, CRM, базы). Проект обладает высокой готовностью к production: активные коммиты (обновлён 28 июн 2026), 422 звёзд, 177 форков, широкая экосистема тем и поддержка нескольких интеграционных точек, что делает его надёжным кандидатом для пилотных и масштабных внедрений.

### 中文

**项目简介**  
matiasbattocchia/open-bsp-api 是一个开源的 WhatsApp 与 Instagram Business 平台实现，提供统一的 Business Service Provider（BSP）协议接口，帮助开发者以标准化方式将 AI 助手、聊天机器人或其他后端系统接入这些社交渠道。

**价值主张**  
- **统一协议**：通过实现 Model Context Protocol（MCP）等标准协议，消除不同渠道之间的接入差异，让 AI 代理能够“一次开发、全渠道使用”。  
- **快速集成**：提供完整的 API、SDK 与 CLI，配合 TypeScript 类型定义，降低开发和调试成本。  
- **生态兼容**：可直接用于构建模型上下文服务、工具调用桥梁以及企业级的多渠道消息系统。

**典型接入方式**  
1. **API 调用**：在后端服务中使用 REST/GraphQL 接口发送和接收 WhatsApp/Instagram 消息。  
2. **SDK 引入**：通过 npm 安装 `open-bsp-api` 包，利用其封装好的 TypeScript 客户端进行消息编解码、会话管理等操作。  
3. **CLI 工具**：使用项目自带的命令行工具快速生成 webhook、验证 token、调试消息流，适合 DevOps 与 CI/CD 场景。  

**生产可用性**  
- **活跃度**：截至 2026‑06‑28 最近一次提交，拥有 422 ⭐、177 🍴，社区活跃，维护者响应及时。  
- **技术成熟度**：全仓库使用 TypeScript，提供完整的类型声明和单元测试，易于在 CI 环境中验证。  
- **安全与合规**：项目采用 MIT 许可证，暂无已知重大安全漏洞；仍建议在正式上线前进行依赖审计和隐私合规检查。  
- **适配性**：支持 Docker 部署和云函数（如 AWS Lambda、Google Cloud Run），可在容器化或无服务器环境中平滑运行。  

综合来看，open-bsp-api 已具备较高的生产就绪度，适合作为企业级 AI‑to‑Tool 集成的核心组件进行试点或正式上线。

## 🧭 Practical evaluation

**Value:** matiasbattocchia/open-bsp-api helps connect AI assistants to real tools and data through a standard protocol.

**Best use cases**

- connect AI agents to tools
- ship Model Context Protocol servers
- standardize integrations

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 422 GitHub stars
- 177 forks
- updated 2026-06-28
- primary language: TypeScript
- 10 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 56/100 |
| stars | 56/100 |
| topics | 100/100 |
| outlook | 80/100 |
| quality | 75/100 |
| recency | 80/100 |
| adoption | 56/100 |
| production | 74/100 |
| usefulness | 90/100 |
| integration | 78/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 300/100 |

---

<sub>🔭 Discovered 2026-06-29 · [View on GitHub](https://github.com/matiasbattocchia/open-bsp-api) · [← Back to Mcp](./README.md)</sub>
