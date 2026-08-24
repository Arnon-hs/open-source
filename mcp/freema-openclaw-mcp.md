# freema/openclaw-mcp

[![Stars](https://img.shields.io/github/stars/freema/openclaw-mcp?style=flat-square&color=yellow)](https://github.com/freema/openclaw-mcp/stargazers) [![Forks](https://img.shields.io/github/forks/freema/openclaw-mcp?style=flat-square&color=blue)](https://github.com/freema/openclaw-mcp/network) [![Language](https://img.shields.io/badge/lang-TypeScript-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-67%2F100-brightgreen?style=flat-square)](#)

> 🦞 MCP server for OpenClaw - secure bridge between Claude.ai and your self-hosted OpenClaw assistant with OAuth2 authentication

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 174 |
| 🍴 **Forks** | 25 |
| 💻 **Language** | TypeScript |
| 📈 **Score** | 67/100 |
| 🗓️ **Last push** | 2026-08-24 |
| 🔍 **Source** | github |

## 🏷️ Topics

`docker-compose` `mcp-server` `open-claw` `productivity` `security` `typescript`

## 🎯 Categories

MCP · Backend · DevOps/Infra · Security

## 📝 Summary

### English

**Brief summary (2‑3 sentences)**  
freema/openclaw‑mcp is a TypeScript‑based MCP (Model Context Protocol) server that acts as a secure bridge between Claude.ai and a self‑hosted OpenClaw assistant, enforcing OAuth2 authentication for every request. It lets developers expose real‑world tools, data, and services to AI agents through a standardized protocol, making it easy to build “AI‑as‑a‑service” integrations. With active maintenance, 174 ★ on GitHub, and recent releases, it is ready for pilot deployments in production environments.  

**Value**  
- **Standardised AI‑tool integration** – By implementing the MCP spec, the server provides a common API surface so any MCP‑compatible AI (Claude, others) can invoke your OpenClaw functions without custom adapters.  
- **Secure, token‑based access** – OAuth2 enforcement protects your backend and makes it straightforward to integrate with existing identity providers and RBAC policies.  
- **Extensible backend** – Built in TypeScript, it can be extended or embedded in existing Node.js services, and it ships a minimal CLI/SDK for rapid prototyping.  

**Practical adoption path**  
1. **Spin up the server** – Clone the repo, run `npm install && npm start` (Docker images are also provided).  
2. **Configure OAuth2** – Register a client with your identity provider, add the client‑id/secret to the `.env` file, and define scopes for each OpenClaw tool you wish to expose.  
3. **Register MCP endpoints** – Use the supplied SDK or edit the `routes/` folder to map OpenClaw commands to HTTP handlers.  
4. **Connect Claude.ai** – In Claude’s integration settings, point the MCP URL and supply the OAuth2 token; Claude can now call your OpenClaw functions as part of its reasoning.  
5. **Iterate & monitor** – Leverage the built‑in health checks and logging, add rate‑limiting or audit hooks, and promote the container to your staging/production cluster.  

**Production readiness**  
- **Active development** – Last commit on 2026‑07‑03, frequent releases, and clear issue triage.  
- **Community traction** – 174 GitHub stars, 25 forks, and several open‑source projects already referencing the repo.  
- **Security posture** – OAuth2 enforcement and a minimal attack surface; no known critical CVEs, but a formal security audit is still advisable.  
- **Operational maturity** – Docker images, Helm chart, and health‑check endpoints make it cloud‑native ready; the TypeScript codebase is well‑typed and includes CI linting/tests.  

Overall, freema/openclaw‑mcp offers a production‑grade, standards‑based way to expose self‑hosted OpenClaw assistants to Claude.ai and other MCP‑compatible models, with a low‑friction onboarding path for teams looking to augment AI agents with real‑world capabilities.

### Русский

freema/openclaw-mcp — это сервер MCP для OpenClaw, который безопасно соединяет Claude.ai (или другие LLM‑агенты) с вашим самохостингом OpenClaw через OAuth2, позволяя моделям получать доступ к реальным инструментам и данным. Типичный сценарий — развертывание сервера в инфраструктуре компании и настройка OAuth2‑токенов, после чего AI‑агент может вызывать функции OpenClaw через стандартный Model Context Protocol, упрощая интеграцию и стандартизацию. Проект считается готовым к production: активные коммиты, 174 ★, поддержка TypeScript, наличие API/SDK/CLI и положительные сигналы экосистемы, хотя окончательная проверка лицензии и безопасности всё же рекомендуется.

### 中文

**简短介绍**

freema/openclaw-mcp 是一个开源项目，提供了一个安全的桥梁（MCP server），连接Claude.ai和自主托管的OpenClaw助手，使用OAuth2身份验证。它帮助连接AI助手与真实工具和数据，通过标准协议。

**价值**

freema/openclaw-mcp 的价值在于，它简化了AI助手与工具和数据的连接，通过标准协议（MCP）提供了一个统一的接口。这种接口使得开发者能够轻松地连接AI助手与各种工具和数据源。

**典型接入方式**

接入freema/openclaw-mcp 可以通过以下方式：

1. 使用OAuth2身份验证，连接Claude.ai和自主托管的OpenClaw助手。
2. 使用MCP协议，连接AI助手与各种工具和数据源。

**生产可用性**

freema/openclaw-mcp 具有高生产可用性，主要原因是：

1. 近期活动：最近更新于2026-07-03。
2. 强大社区支持：GitHub星标数为174，fork数为25

## 🧭 Practical evaluation

**Value:** freema/openclaw-mcp helps connect AI assistants to real tools and data through a standard protocol.

**Best use cases**

- connect AI agents to tools
- ship Model Context Protocol servers
- standardize integrations

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 174 GitHub stars
- 25 forks
- updated 2026-07-03
- primary language: TypeScript
- 6 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 35/100 |
| stars | 48/100 |
| topics | 75/100 |
| outlook | 57/100 |
| quality | 56/100 |
| recency | 40/100 |
| adoption | 44/100 |
| production | 60/100 |
| usefulness | 74/100 |
| integration | 94/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 400/100 |

---

<sub>🔭 Discovered 2026-07-03 · [View on GitHub](https://github.com/freema/openclaw-mcp) · [← Back to Mcp](./README.md)</sub>
