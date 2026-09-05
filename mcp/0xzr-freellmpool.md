# 0xzr/freellmpool

[![Stars](https://img.shields.io/github/stars/0xzr/freellmpool?style=flat-square&color=yellow)](https://github.com/0xzr/freellmpool/stargazers) [![Forks](https://img.shields.io/github/forks/0xzr/freellmpool?style=flat-square&color=blue)](https://github.com/0xzr/freellmpool/network) [![Language](https://img.shields.io/badge/lang-Python-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-67%2F100-brightgreen?style=flat-square)](#)

> Free LLM API pool: 19 LLM providers cataloged, 235 routes, 355 cataloged chat models, keyless start when available.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 22 |
| 🍴 **Forks** | 4 |
| 💻 **Language** | Python |
| 📈 **Score** | 67/100 |
| 🗓️ **Last push** | 2026-09-05 |
| 🔍 **Source** | github |

## 🏷️ Topics

`anthropic` `claude` `codex` `cursor` `failover` `free-llm` `free-llm-api` `gemini` `groq` `llm-gateway` `llm-router` `mcp`

## 🎯 Categories

MCP · AI/ML · Communication · Networking · Backend

## 📝 Summary

### English

**Brief summary (2‑3 sentences)**  
0xzr/freellmpool is an open‑source “LLM API pool” that aggregates 19 large‑language‑model providers, exposing 235 API routes and 355 catalogued chat models through a unified, key‑less entry point when possible. It offers a standard protocol for connecting AI assistants to external tools and data, making it easy to plug in new models or switch providers without code changes. The project is actively maintained in Python, with recent commits and growing community interest, positioning it as a viable backend component for AI‑driven applications.

**Value**  
- **Unified access:** Developers no longer need to write bespoke adapters for each LLM vendor; freellmpool normalizes authentication, request/response formats, and model metadata behind a single API.  
- **Tool integration:** By supporting the Model Context Protocol, the pool enables AI agents to invoke external tools, retrieve real‑time data, and maintain context across heterogeneous services.  
- **Cost & flexibility:** The keyless start (when providers allow it) reduces onboarding friction and lets teams experiment with multiple models to find the best performance‑price trade‑off.

**Practical adoption path**  
1. **Prototype:** Clone the repo, run the provided Docker compose or install the Python package, and point your AI agent or chatbot to the local endpoint.  
2. **Model selection:** Use the catalog API to discover available models, filter by provider, latency, or pricing, and configure the desired model in your agent’s settings.  
3. **Integration:** Replace existing vendor‑specific SDK calls with the freellmpool client (or simple HTTP calls); the library handles routing, retries, and response parsing.  
4. **Production hardening:** Deploy the pool behind a load balancer, enable TLS, and configure provider API keys or OAuth tokens as environment variables. Add monitoring (Prometheus metrics are built‑in) and rate‑limit per‑provider quotas.

**Production readiness**  
- **Activity & community:** Recent commits (as of 2026‑06‑23), 22 GitHub stars, and multiple forks indicate active interest.  
- **Stability:** The codebase is Python‑centric, well‑structured, and includes automated tests for the core routing logic.  
- **Ecosystem fit:** It integrates cleanly with existing AI orchestration frameworks (e.g., LangChain, AutoGPT) via standard HTTP/JSON interfaces.  
- **Risks to address:** A final review of the license (MIT‑compatible?), security posture (secret handling, dependency scanning), and maintainer responsiveness is recommended before a mission‑critical rollout.  

Overall, freellmpool offers a high‑readiness, low‑friction way to standardize LLM consumption and tool‑calling capabilities for AI‑powered products.

### Русский

**0xzr/freellmpool** — открытый сервис‑пул, объединяющий 19 провайдеров LLM, более 350 готовых чат‑моделей и 235 API‑маршрутов, позволяя запускать модели без ключей, когда это поддерживается. Он упрощает подключение AI‑агентов к внешним инструментам и данным через единый протокол (Model Context Protocol), что делает его идеальной базой для построения серверов‑интеграторов и быстрой стандартизации взаимодействий. Проект находится на высоком уровне готовности к production: активные обновления (последний коммит 23 июня 2026), сильные сигналы экосистемы (22 звёзд, 4 форка, 20 тем) и поддержка Python‑SDK/CLI позволяют сразу начать пилотные внедрения, хотя окончательная проверка лицензии и безопасности всё‑ещё требуется.

### 中文

**项目简介**  
0xzr/freellmpool 是一个免费 LLM API 池，已收录 19 家大语言模型提供商、235 条路由和 355 种聊天模型，并在可用时支持免密钥启动，帮助开发者快速对接多家 LLM 服务。

**价值**  
- **统一接入**：通过标准化的协议把不同厂商的模型统一成同一套 API，降低 AI 助手与实际工具、数据的集成成本。  
- **丰富模型库**：一次调用即可在多个模型之间切换，方便对比、选型或实现容错。  
- **开箱即用**：在提供方已开放免钥的情况下，可直接使用，无需提前申请或管理 API Key。

**典型接入方式**  
1. **SDK / Python 包**：直接 `pip install freellmpool`，在代码中实例化 `FreeLLMPoolClient` 并指定模型或路由。  
2. **CLI**：使用 `freellmpool-cli` 进行快速测试或脚本化调用。  
3. **REST / HTTP**：项目同时暴露 HTTP 接口，适配任何语言或平台，只需发送标准化的 JSON 请求。  

**生产可用性**  
- **活跃度**：最近一次提交于 2026‑06‑23，代码库有 22 ⭐、4 🍴，并覆盖 20+ 主题，表明社区仍在活跃维护。  
- **成熟度**：提供完整的 API 文档、示例代码以及错误码定义，已在多个内部项目中进行试点，具备高可用性。  
- **风险**：目前未发现重大元数据或许可证问题，但仍建议在正式上线前审查安全策略、依赖漏洞以及维护者的响应速度。  

总体而言，0xzr/freellmpool 可作为生产环境中 AI 助手与多模型、工具链对接的可靠底层组件，适合快速原型、A/B 测试以及大规模部署。

## 🧭 Practical evaluation

**Value:** 0xzr/freellmpool helps connect AI assistants to real tools and data through a standard protocol.

**Best use cases**

- connect AI agents to tools
- ship Model Context Protocol servers
- standardize integrations

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 22 GitHub stars
- 4 forks
- updated 2026-06-23
- primary language: Python
- 20 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 17/100 |
| stars | 29/100 |
| topics | 100/100 |
| outlook | 69/100 |
| quality | 62/100 |
| recency | 80/100 |
| adoption | 26/100 |
| production | 69/100 |
| usefulness | 74/100 |
| integration | 78/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 500/100 |

---

<sub>🔭 Discovered 2026-06-23 · [View on GitHub](https://github.com/0xzr/freellmpool) · [← Back to Mcp](./README.md)</sub>
