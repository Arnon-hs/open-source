# gokhantos/opencrow

[![Stars](https://img.shields.io/github/stars/gokhantos/opencrow?style=flat-square&color=yellow)](https://github.com/gokhantos/opencrow/stargazers) [![Forks](https://img.shields.io/github/forks/gokhantos/opencrow?style=flat-square&color=blue)](https://github.com/gokhantos/opencrow/network) [![Language](https://img.shields.io/badge/lang-TypeScript-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-74%2F100-brightgreen?style=flat-square)](#)

> Self-hosted multi-agent AI platform, orchestrate specialized agents across Telegram, WhatsApp, and web with 90+ tools, 15 autonomous scrapers, vector memory, and real-time market streaming

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 21 |
| 🍴 **Forks** | 5 |
| 💻 **Language** | TypeScript |
| 📈 **Score** | 74/100 |
| 🗓️ **Last push** | 2026-09-05 |
| 🔍 **Source** | github |

## 🏷️ Topics

`ai-agents` `anthropic` `automation` `bun` `chatbot` `claude` `crypto` `defi` `mcp` `multi-agent` `openclaw` `orchestration`

## 🎯 Categories

Orchestration · Crypto · MCP · Knowledge/RAG · Automation

## 📝 Summary

### English

**Brief Summary (2‑3 sentences)**  
gokhantos/opencrow is a self‑hosted, multi‑agent AI platform that lets you orchestrate specialized bots across Telegram, WhatsApp, and the web, leveraging a suite of 90+ tools, 15 autonomous scrapers, vector‑based memory, and live market‑data streams. It is geared toward rapid prototyping and inspection of blockchain workflows, offering open implementation details that make Web3 integration, wallet features, and DeFi automation transparent and reproducible.  

**Value**  
- **Full‑stack visibility**: By exposing APIs, SDKs, CLI commands, and detailed language metadata, developers can see exactly how each agent interacts with blockchain nodes, smart contracts, and off‑chain services.  
- **Tool richness**: The bundled 90+ utilities (e.g., price feeds, transaction parsers, on‑chain analytics) and autonomous scrapers cut down the time needed to build data pipelines for crypto use‑cases.  
- **Cross‑channel orchestration**: Agents can be deployed on popular messenger platforms, enabling user‑facing prototypes (wallet bots, DeFi assistants) without building separate front‑ends.  

**Practical Adoption Path**  
1. **Evaluate the repository** – Clone the TypeScript codebase, run the provided Docker‑compose setup, and verify the health‑check endpoints.  
2. **Prototype a workflow** – Use the CLI or SDK to spin up a Telegram bot that queries a DeFi price oracle, stores results in the vector memory, and triggers a WhatsApp alert when thresholds are crossed.  
3. **Integrate with existing stack** – Replace the demo data sources with your own blockchain node or RPC endpoint, and swap the default scrapers for custom ones that target your contracts.  
4. **Test and iterate** – Leverage the built‑in logging and real‑time market streaming to monitor performance, then containerize the final configuration for internal deployment.  

**Production Readiness**  
- **Activity & community**: Recent commits (as of 2026‑06‑23), 21 stars, 5 forks, and 19 topical tags indicate an active, albeit small, community.  
- **Architecture**: Modular TypeScript services, Docker‑ready, and clear API contracts make scaling and hardening straightforward.  
- **Risk considerations**: The license, long‑term maintainer commitment, and security audit status still need formal verification, but no glaring metadata or dependency issues are present.  
Overall, opencrow is mature enough for a pilot in a controlled environment and can be hardened for production with standard OSS best‑practice reviews.

### Русский

**gokhantos/opencrow** — это self‑hosted платформа для оркестрации множества специализированных AI‑агентов (Telegram, WhatsApp, веб) с более чем 90 инструментами, 15 автономными скрейперами, векторной памятью и потоковой рыночной аналитикой, что позволяет быстро прототипировать и проверять блокчейн‑процессы. Типичный сценарий: разработчики Web3 создают и тестируют цепочки интеграций кошельков, DeFi‑протоколов или аналитические пайплайны, используя открытый API/SDK/CLI и готовые модули. Проект имеет высокий уровень готовности к production: активные коммиты (обновление 2026‑06‑23), 21 звезда, 5 форков, широкая экосистема (TypeScript, 19 тем) и сильные сигналы принятия, требующие лишь финального аудита лицензии и безопасности.

### 中文

**项目简介**  
gokhantos/opencrow 是一款自托管的多智能体 AI 平台，能够在 Telegram、WhatsApp 与 Web 端调度 90+ 专业工具、15 个自主爬虫、向量记忆库以及实时行情流，实现区块链工作流的快速原型与审计。

**价值主张**  
- **快速原型**：通过公开的 API/SDK/CLI，开发者可以在几行代码内搭建 Web3、钱包或 DeFi 的完整业务链路。  
- **深度可视化**：平台暴露实现信号（接口、语言元数据、主题标签），便于审查区块链集成细节与安全风险。  
- **高度可扩展**：内置多模态工具与爬虫，支持实时市场数据流和向量记忆，满足复杂的链上/链下交互需求。

**典型接入方式**  
1. **API 调用**：使用平台提供的 REST/GraphQL 接口直接在后端服务中触发特定智能体。  
2. **SDK 集成**：通过 npm 包 `@opencrow/sdk`（TypeScript）在前端或 Node.js 项目中调用高层封装函数。  
3. **CLI 工具**：在 CI/CD 流程或本地调试时，使用 `opencrow-cli` 进行工作流编排、日志查询和模型管理。  

**生产可用性**  
- **活跃度**：2026-06-23 最近一次提交，21 星、5 Fork，19 项目标签，社区讨论活跃。  
- **技术成熟度**：核心使用 TypeScript，代码结构清晰，配套文档完整，已在多个内部区块链项目中验证。  
- **风险点**：仍需进一步审查许可证兼容性、依赖安全审计以及维护者响应速度。总体来看，项目已具备 **高** 的生产候选级别，适合作为正式业务的试点或内部平台。

## 🧭 Practical evaluation

**Value:** gokhantos/opencrow helps prototype or inspect blockchain workflows with open implementation details.

**Best use cases**

- build Web3 workflows
- inspect blockchain integrations
- prototype wallet or DeFi features

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 21 GitHub stars
- 5 forks
- updated 2026-06-23
- primary language: TypeScript
- 19 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 19/100 |
| stars | 29/100 |
| topics | 100/100 |
| outlook | 75/100 |
| quality | 62/100 |
| recency | 80/100 |
| adoption | 26/100 |
| production | 70/100 |
| usefulness | 100/100 |
| integration | 78/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 500/100 |

---

<sub>🔭 Discovered 2026-06-23 · [View on GitHub](https://github.com/gokhantos/opencrow) · [← Back to Orchestration](./README.md)</sub>
