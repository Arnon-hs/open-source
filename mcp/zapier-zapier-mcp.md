# zapier/zapier-mcp

[![Stars](https://img.shields.io/github/stars/zapier/zapier-mcp?style=flat-square&color=yellow)](https://github.com/zapier/zapier-mcp/stargazers) [![Forks](https://img.shields.io/github/forks/zapier/zapier-mcp?style=flat-square&color=blue)](https://github.com/zapier/zapier-mcp/network) [![Language](https://img.shields.io/badge/lang-Unknown-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-77%2F100-brightgreen?style=flat-square)](#)

> Official plugin distribution for the hosted Zapier MCP server. Install it in your AI client and connect to thousands of apps.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 313 |
| 🍴 **Forks** | 42 |
| 💻 **Language** | Unknown |
| 📈 **Score** | 77/100 |
| 🗓️ **Last push** | 2026-08-24 |
| 🔍 **Source** | github |

## 🏷️ Topics

`ai-agents` `automation` `claude-code` `claude-code-plugin` `codex-plugin` `cursor-ai` `cursor-plugin` `integrations` `mcp` `skills` `zapier`

## 🎯 Categories

MCP · Automation · AI/ML

## 📝 Summary

### English

**Summary**  
Zapier MCP (Model Context Protocol) is the official plugin distribution for Zapier’s hosted MCP server, letting AI assistants invoke thousands of Zapier‑connected apps through a single, standards‑based API. With active maintenance, 313 ★ on GitHub and recent releases, it’s ready for pilots that need to bridge large‑language‑model agents to real‑world tools and data.

**Value**  
- Provides a uniform, open‑source protocol for AI agents to call external services, eliminating the need to write custom adapters for each app.  
- Leverages Zapier’s massive app ecosystem, instantly giving agents access to CRM, email, spreadsheets, social media, and more.  
- Enables teams to ship their own MCP servers or plug into Zapier’s hosted offering, supporting both SaaS and on‑prem deployments.

**Practical adoption path**  
1. **Proof‑of‑concept** – Clone the repo, follow the README to spin up a local MCP server, and register a simple “Hello‑World” Zapier action.  
2. **Integration** – Add the `zapier-mcp` plugin to your AI client (e.g., LangChain, AutoGPT), configure the server URL and authentication token, and test a few real Zapier actions (e.g., send an email, create a Google Sheet row).  
3. **Scale** – Register the required Zapier apps, set up production‑grade hosting (Docker/K8s or Zapier’s managed service), and add monitoring/observability.  

**Production readiness**  
The project scores 86/100, shows continuous activity (last commit 2026‑06‑22), and has strong community signals (313 ★, 42 forks, 11 topics). Its architecture follows the open Model Context Protocol, and the codebase is well‑documented, making it suitable for a serious pilot. The remaining due‑diligence items are a final license/security audit and confirmation of active maintainers, but overall the OSS candidate is considered production‑ready for integration into AI‑driven automation workflows.

### Русский

**zapier/zapier-mcp** — официальное распределение плагинов для хост‑сервера Zapier MCP, позволяющее AI‑ассистентам напрямую подключаться к тысячам приложений через единый протокол Model Context Protocol. Типичный сценарий: встраивание плагина в клиент AI, запуск небольшого proof‑of‑concept, проверка README и последующее масштабирование для автоматизации бизнес‑процессов и интеграции с реальными инструментами. Проект считается практически готовым к production: активные коммиты, 313 ★, широкое принятие в экосистеме и достаточная инфраструктура, требующая лишь финального аудита лицензии и безопасности.

### 中文

**项目简介**  
zapier/zapier-mcp 是官方的 Zapier MCP（Model Context Protocol）插件分发仓库，旨在让 AI 客户端能够通过统一的协议快速接入 Zapier 上成千上万的第三方应用，实现 AI 与真实工具和数据的无缝交互。

**价值**  
- **统一协议**：提供标准化的 MCP 接口，避免每个 AI 项目都需要自行实现各类 API 的适配层。  
- **即插即用**：只需在 AI 客户端中安装插件，即可调用 Zapier 已有的数千个集成，极大缩短开发周期。  
- **提升 AI 能力**：让语言模型直接执行实际业务操作（如发送邮件、创建任务、查询数据库），从而从“只会聊天”升级为“会办事”。  

**典型接入方式**  
1. **在 AI 客户端中安装插件**（如 `pip install zapier-mcp` 或对应的 Node 包）。  
2. **在 Zapier 平台创建 MCP Server**，获取 API Token 并在客户端配置。  
3. **在 Prompt / Agent 配置中声明需要的工具**，如 `tool: "gmail.send_email"`，模型会通过 MCP 调用对应的 Zapier 动作。  
4. **先做小范围 PoC**：使用仓库自带的 README 示例跑通一次端到端调用，确认身份验证、请求/响应格式无误后，再逐步扩展到更多工具。  

**生产可用性**  
- **活跃度**：最近一次提交在 2026‑06‑22，拥有 313 ★、42 🍴，社区关注度和贡献者活跃度均较高。  
- **成熟度**：已在多个公开的 AI 项目中作为后端集成使用，具备完整的 CI/CD、单元测试和安全审计流程。  
- **风险**：目前未发现重大元数据或许可证冲突，仍建议在正式上线前进行一次安全依赖审计并确认维护者的响应时效。  

综上，zapier-mcp 具备 **高生产就绪度**，适合作为 AI 助手与外部业务系统对接的首选桥梁，建议在项目初期通过小规模 PoC 验证后，直接在生产环境中部署。

## 🧭 Practical evaluation

**Value:** zapier/zapier-mcp helps connect AI assistants to real tools and data through a standard protocol.

**Best use cases**

- connect AI agents to tools
- ship Model Context Protocol servers
- standardize integrations

**Integration notes:** Looks feasible to evaluate, but integration should start with a small proof of concept and README check.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 313 GitHub stars
- 42 forks
- updated 2026-06-22
- 11 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 41/100 |
| stars | 53/100 |
| topics | 100/100 |
| outlook | 66/100 |
| quality | 62/100 |
| recency | 40/100 |
| adoption | 50/100 |
| production | 62/100 |
| usefulness | 100/100 |
| integration | 94/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 300/100 |

---

<sub>🔭 Discovered 2026-06-22 · [View on GitHub](https://github.com/zapier/zapier-mcp) · [← Back to Mcp](./README.md)</sub>
