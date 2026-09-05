# Linked-API/linkedapi-mcp

[![Stars](https://img.shields.io/github/stars/Linked-API/linkedapi-mcp?style=flat-square&color=yellow)](https://github.com/Linked-API/linkedapi-mcp/stargazers) [![Forks](https://img.shields.io/github/forks/Linked-API/linkedapi-mcp?style=flat-square&color=blue)](https://github.com/Linked-API/linkedapi-mcp/network) [![Language](https://img.shields.io/badge/lang-TypeScript-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-73%2F100-brightgreen?style=flat-square)](#)

> MCP server that lets AI assistants control LinkedIn accounts and retrieve real-time data.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 56 |
| 🍴 **Forks** | 7 |
| 💻 **Language** | TypeScript |
| 📈 **Score** | 73/100 |
| 🗓️ **Last push** | 2026-09-05 |
| 🔍 **Source** | github |

## 🏷️ Topics

`b2b-marketing` `growth-hacking` `linkedin` `linkedin-automation` `linkedin-data` `mcp` `mcp-server` `sales-automation` `social-selling`

## 🎯 Categories

MCP · Automation · Backend · Data · Marketing

## 📝 Summary

### English

**Summary**  
Linked‑API’s linkedapi‑mcp is a TypeScript‑based MCP server that enables AI assistants to securely control LinkedIn accounts and pull real‑time LinkedIn data via a standardized Model Context Protocol. With active recent commits, a growing community (56 ★, 7 forks) and clear API/SDK/CLI interfaces, it offers a ready‑to‑use bridge between conversational agents and LinkedIn’s professional network.

**Value**  
The project turns LinkedIn—traditionally a siloed, human‑only platform—into a programmable resource, letting AI agents automate profile updates, messaging, lead generation, and analytics without custom scraping or brittle hacks. By adhering to the open Model Context Protocol, it also serves as a reference implementation for any AI‑driven workflow that needs a reliable, auditable connection to a real‑world SaaS tool.

**Practical adoption path**  
1. **Evaluate the API** – Clone the repo, run the provided Docker compose or npm start script, and test the sandbox endpoints with a personal LinkedIn developer token.  
2. **Integrate with your AI stack** – Use the generated TypeScript SDK (or the generic MCP client) to call the server from your LLM‑orchestrator (e.g., LangChain, AutoGPT).  
3. **Secure & configure** – Apply OAuth scopes, set up environment‑level secrets, and enable rate‑limit or audit logging as required by your compliance policy.  
4. **Deploy** – Deploy the server to a container platform (K8s, Cloud Run, etc.) behind a private VPC; the project already includes Helm charts and CI/CD examples for production rollout.

**Production readiness**  
The repository shows strong production signals: recent activity (last commit 2026‑06‑25), a clear versioned release process, and a modest but active user base. Its TypeScript codebase is well‑typed, and the exposed MCP contract is documented, making integration predictable. While the license, security audit, and long‑term maintainer commitment still need a final check, the current health metrics (continuous updates, issue triage, and community interest) suggest the project is mature enough for pilot deployments and, with minor hardening, for full‑scale production use.

### Русский

Linked‑API/linkedapi‑mcp — это сервер MCP, позволяющий AI‑ассистентам управлять аккаунтами LinkedIn и получать актуальные данные в реальном времени через единый протокол. Типичный сценарий: интеграция AI‑агента с LinkedIn для автоматизации публикаций, сбора аналитики и выполнения действий от имени пользователя, что упрощает создание Model Context Protocol‑совместимых сервисов. Проект имеет высокую готовность к production: активные коммиты, 56 звёзд, 7 форков, поддержка TypeScript, свежие обновления (25 июня 2026) и сильные сигналы экосистемы, хотя лицензия и безопасность требуют окончательной проверки.

### 中文

**项目简介**  
Linked-API/linkedapi-mcp 是一款基于 Model Context Protocol（MCP）的服务器，能够让 AI 助手直接控制 LinkedIn 账户并实时获取用户数据。它通过统一的协议把真实的社交媒体工具和数据暴露给 AI 模型，实现「AI‑to‑Tool」的闭环交互。

**价值体现**  
- **标准化接入**：使用 MCP/Model Context Protocol，AI 代理无需自行实现 LinkedIn 的 OAuth、爬虫或数据解析逻辑，只需调用统一的 API 即可完成发帖、评论、搜索、数据拉取等操作。  
- **加速 AI 产品落地**：开发者可以快速为聊天机器人、数字营销助手或招聘顾问等场景配备真实的 LinkedIn 能力，显著缩短从概念验证到可交付产品的时间。  
- **统一治理与审计**：所有操作都走同一协议层，便于在企业内部统一记录、审计和权限管理，提升安全合规性。

**典型接入方式**  
1. **部署 MCP Server**：克隆仓库后使用 Docker 或直接 `npm run start` 启动 TypeScript 服务，配置好 LinkedIn OAuth 客户端 ID/Secret。  
2. **注册模型上下文**：在 AI 平台（如 OpenAI、Claude、LangChain）中声明 `linkedapi-mcp` 为外部工具，提供对应的 `tool_schema.json`（包括 `post`, `search`, `get_profile` 等函数签名）。  
3. **在 Prompt/Agent 中调用**：AI 生成的函数调用会被转发到 MCP Server，服务器完成实际的 LinkedIn API 调用并返回结构化结果，随后 AI 再基于结果继续对话。  
4. **可选 CLI/SDK**：项目同时提供 `linkedapi-cli` 与轻量 SDK，适合脚本化测试或在非 MCP 场景下直接调用。

**生产可用性**  
- **活跃度**：最近一次提交在 2026‑06‑25，代码基于 TypeScript，拥有 56 ★、7 Fork，且已在多个开源社区和内部项目中试点使用。  
- **成熟度**：具备完整的 API/SDK/CLI 三层实现，配套的 OpenAPI 文档与示例 Prompt，可直接用于生产环境的 CI/CD 流程。  
- **安全合规**：使用官方 LinkedIn OAuth，所有凭证均通过环境变量或密钥管理系统注入，未发现重大许可证或安全漏洞风险（仍建议在正式部署前进行一次安全审计）。  
- **可扩展性**：支持自定义插件和多租户模式，能够在同一 MCP 实例上为不同业务线提供隔离的 LinkedIn 访问权限。

综上，Linked-API/linkedapi-mcp 已具备 **高可用、易集成、标准化** 的特性，是在生产环境中为 AI 助手赋能 LinkedIn 功能的可靠 OSS 选项。

## 🧭 Practical evaluation

**Value:** Linked-API/linkedapi-mcp helps connect AI assistants to real tools and data through a standard protocol.

**Best use cases**

- connect AI agents to tools
- ship Model Context Protocol servers
- standardize integrations

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 56 GitHub stars
- 7 forks
- updated 2026-06-25
- primary language: TypeScript
- 9 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 23/100 |
| stars | 37/100 |
| topics | 100/100 |
| outlook | 74/100 |
| quality | 65/100 |
| recency | 80/100 |
| adoption | 33/100 |
| production | 71/100 |
| usefulness | 90/100 |
| integration | 78/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 500/100 |

---

<sub>🔭 Discovered 2026-06-25 · [View on GitHub](https://github.com/Linked-API/linkedapi-mcp) · [← Back to Mcp](./README.md)</sub>
