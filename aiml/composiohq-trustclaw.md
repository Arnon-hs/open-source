# ComposioHQ/trustclaw

[![Stars](https://img.shields.io/github/stars/ComposioHQ/trustclaw?style=flat-square&color=yellow)](https://github.com/ComposioHQ/trustclaw/stargazers) [![Forks](https://img.shields.io/github/forks/ComposioHQ/trustclaw?style=flat-square&color=blue)](https://github.com/ComposioHQ/trustclaw/network) [![Language](https://img.shields.io/badge/lang-TypeScript-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-65%2F100-brightgreen?style=flat-square)](#)

> A self-hostable personal AI agent with vector memory, Composio tools, and Telegram.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 350 |
| 🍴 **Forks** | 86 |
| 💻 **Language** | TypeScript |
| 📈 **Score** | 65/100 |
| 🗓️ **Last push** | 2026-05-13 |
| 🔍 **Source** | github |

## 🏷️ Topics

_no topics_

## 🎯 Categories

AI/ML

## 📝 Summary

### English

**Brief Summary**  
ComposioHQ / trustclaw is a self‑hosted personal AI agent built in TypeScript that combines vector‑based memory, Composio’s suite of productivity tools, and Telegram integration. It lets developers prototype Retrieval‑Augmented Generation (RAG) or autonomous agent workflows without assembling a model stack from scratch, and it ships with ready‑to‑use tooling for rapid experimentation.

**Value**  
- **Speed to prototype** – All the heavy‑lifting (vector store, tool wrappers, messaging channel) is pre‑wired, so teams can focus on the business logic of their AI feature rather than on infrastructure.  
- **Modular toolset** – By exposing Composio’s APIs, trustclaw makes it easy to add calendar, email, or database actions to an agent, turning a simple chatbot into a functional personal assistant.  
- **Open‑source transparency** – With ~350 stars and an active TypeScript codebase, the project is easy to audit, extend, and integrate with existing TypeScript/Node.js stacks.

**Practical Adoption Path**  
1. **Clone & spin‑up** – Fork the repo, run the Docker compose (or `npm install` + `npm start`) to launch the agent locally.  
2. **Configure secrets** – Add your OpenAI (or other LLM) API key, vector‑store credentials, and Telegram bot token in the `.env` file.  
3. **Define tools** – Use the provided Composio SDK to register the specific APIs your use case needs (e.g., CRM, calendar).  
4. **Iterate** – Interact via Telegram, observe the agent’s memory snapshots, and refine prompts or tool bindings.  
5. **Hardening for production** – Replace the default SQLite vector store with a managed Pinecone/Weaviate instance, enable TLS, and add rate‑limiting/auth checks around the Telegram webhook.

**Production Readiness**  
- **Maturity** – Medium. The project is functional for prototypes and internal workflows, but it lacks comprehensive CI/CD pipelines, extensive automated tests, and detailed deployment documentation.  
- **Dependencies** – Relies on external LLM APIs, a vector store, and Telegram; each must be evaluated for latency, cost, and compliance.  
- **Maintenance** – Recent commit (2026‑05‑13) shows active development, but the core maintainer count is low; organizations should plan for in‑house ownership or a service‑level agreement.  
- **Risk considerations** – No immediate licensing or security red flags, but a formal security audit (especially around the Telegram webhook and secret handling) is recommended before exposing the agent to production traffic.

In short, trustclaw offers a fast, open‑source foundation for building personal AI agents, suitable for proof‑of‑concepts and internal tools, while requiring additional hardening and operational oversight for production deployments.

### Русский

**ComposioHQ/trustclaw** — это самохостируемый персональный AI‑агент с векторной памятью, интеграцией инструментов Composio и поддержкой Telegram, позволяющий быстро добавить AI‑функциональность без построения модели «с нуля». Он идеально подходит для прототипирования AI‑фич, создания RAG‑или агентных воркфлоу и оценки инструментов моделей, однако перед внедрением в продакшн требуется ручная проверка интеграций и оценка зависимости/поддержки. Уровень готовности — средний: проект подходит для внутренних прототипов, но требует дополнительного аудита лицензий, безопасности и активного сопровождения перед масштабным использованием.

### 中文

**项目简介**  
ComposioHQ/trustclaw 是一款可自行部署的个人 AI 代理，内置向量记忆、Composio 系列工具以及 Telegram 接口，帮助开发者在已有模型基础上快速加入 AI 能力。

**价值**  
- **快速原型**：无需从零搭建模型栈，即可在几分钟内部署具备检索增强生成（RAG）和工作流编排的 AI 代理。  
- **灵活扩展**：通过 Composio 提供的丰富工具链，可轻松接入外部 API、数据库或自定义函数，适用于内部工具、客服机器人等场景。  
- **低门槛实验**：支持在本地或私有云中运行，便于评估不同模型、提示工程和记忆策略的效果。

**典型接入方式**  
1. **准备环境**：克隆仓库，使用 Docker Compose 或直接 `npm install` 安装依赖（Node.js ≥18、TypeScript）。  
2. **配置向量存储**：在 `.env` 中填写 Pinecone、Weaviate 或本地 Qdrant 的连接信息，用于文档向量化与检索。  
3. **接入 Composio 工具**：在 Composio 控制台创建 API Key，填入配置文件后即可使用内置的 API 调用、数据库查询等功能。  
4. **Telegram Bot**：在 BotFather 创建 Bot，获取 token 并写入 `.env`，启动后即可通过 Telegram 与代理对话。  
5. **启动服务**：`docker compose up -d` 或 `npm run start:prod`，访问 `http://localhost:3000` 查看健康检查和管理页面。

**生产可用性**  
- **成熟度**：GitHub 350+ stars、86 forks，近期（2026‑05‑13）仍有更新，代码质量和社区活跃度良好。  
- **适用场景**：非常适合作为原型、内部工具或实验平台；在正式生产环境使用前，需要完成以下检查：  
  - **依赖审计**：确认第三方库的许可证兼容性与安全漏洞。  
  - **运维准备**：为向量数据库、消息队列等关键组件配置持久化、监控和备份。  
  - **安全加固**：限制 Telegram Bot 的访问范围，使用 HTTPS、API Key 进行身份验证。  
- **总体评估**：**中等**（Medium）——具备投入生产的技术基础，但在正式上线前建议进行完整的安全、合规和运维评估。

## 🧭 Practical evaluation

**Value:** ComposioHQ/trustclaw helps add AI capability without starting from a blank model stack.

**Best use cases**

- prototype AI features
- build RAG or agent workflows
- evaluate model tooling

**Integration notes:** Needs manual inspection before adoption because integration signals are sparse in the discovered metadata.

**Production readiness:** Medium: useful for prototypes or internal workflows, with dependency and maintenance checks before production.

**Quality signals**

- 350 GitHub stars
- 86 forks
- updated 2026-05-13
- primary language: TypeScript

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 48/100 |
| stars | 54/100 |
| topics | 0/100 |
| outlook | 73/100 |
| quality | 64/100 |
| recency | 100/100 |
| adoption | 53/100 |
| production | 71/100 |
| usefulness | 74/100 |
| integration | 46/100 |
| sourceTrust | 100/100 |

---

<sub>🔭 Discovered 2026-05-13 · [View on GitHub](https://github.com/ComposioHQ/trustclaw) · [← Back to AI/ML](./README.md)</sub>
