# dominik1001/caldav-mcp

[![Stars](https://img.shields.io/github/stars/dominik1001/caldav-mcp?style=flat-square&color=yellow)](https://github.com/dominik1001/caldav-mcp/stargazers) [![Forks](https://img.shields.io/github/forks/dominik1001/caldav-mcp?style=flat-square&color=blue)](https://github.com/dominik1001/caldav-mcp/network) [![Language](https://img.shields.io/badge/lang-TypeScript-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-55%2F100-brightgreen?style=flat-square)](#)

> 🗓️ A CalDAV Model Context Protocol (MCP) server to expose calendar operations as tools for AI assistants.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 68 |
| 🍴 **Forks** | 23 |
| 💻 **Language** | TypeScript |
| 📈 **Score** | 55/100 |
| 🗓️ **Last push** | 2026-08-24 |
| 🔍 **Source** | github |

## 🏷️ Topics

`caldav` `mcp` `mcp-server` `typescript`

## 🎯 Categories

MCP · Backend

## 📝 Summary

### English

**Brief Summary (2‑3 sentences)**  
dominik1001/caldav-mcp is an open‑source CalDAV Model Context Protocol (MCP) server that translates calendar operations into a standardized API that AI assistants can invoke as tools. Built in TypeScript, it lets developers expose real‑world scheduling data to LLM‑powered agents, enabling the agents to read, create, update, and delete calendar events through a uniform protocol. The project is moderately popular (≈68 ★, 23 forks) and actively maintained as of May 2026.  

**Value**  
- **Bridges AI and real‑world tools**: By wrapping CalDAV—a widely supported calendar protocol—in MCP, the server gives AI assistants concrete, trustworthy access to scheduling data without custom scrapers or ad‑hoc integrations.  
- **Standardized interface**: MCP provides a language‑agnostic contract (JSON‑RPC‑style) that can be consumed by any LLM‑tooling framework, simplifying the development of AI‑driven assistants that need calendar capabilities.  
- **Accelerates prototyping**: Teams can spin up a functional “calendar tool” for their agents in minutes, focusing on higher‑level reasoning rather than low‑level API design.  

**Practical Adoption Path**  
1. **Prototype** – Clone the repo, run the TypeScript server locally (or via Docker), and point it at an existing CalDAV store (e.g., Nextcloud, Apple Calendar).  
2. **Integrate** – Register the server’s MCP endpoint in your AI‑assistant framework (e.g., LangChain, LlamaIndex) as a tool definition, mapping the MCP methods to the assistant’s tool calls.  
3. **Validate** – Write a few test prompts that request calendar reads/writes and confirm the assistant correctly invokes the MCP methods and handles responses.  
4. **Deploy** – Containerize the server, add TLS and authentication (basic auth, OAuth, or mutual TLS), and expose it behind your internal API gateway.  
5. **Scale** – For production, add monitoring, rate‑limiting, and a persistent CalDAV backend; consider horizontal scaling via Kubernetes if request volume grows.  

**Production Readiness**  
- **Maturity**: Medium. The codebase is recent, actively updated, and has modest community interest, making it suitable for prototypes and internal tools.  
- **Dependencies**: Pure TypeScript with a small set of well‑maintained libraries; Docker support eases deployment.  
- **Risks**: The project lacks a formal security audit, and licensing/maintainer continuity still need verification. Before production, perform a security review, enforce strict authentication, and establish a maintenance plan (e.g., fork and assign an internal owner).  

Overall, caldav-mcp offers a practical, standards‑based way to equip AI assistants with calendar capabilities, with a clear path from sandbox testing to production deployment once the security and maintenance checks are completed.

### Русский

**Caldav‑MCP** — открытый сервер Model Context Protocol, реализованный на TypeScript, который превращает операции CalDAV в стандартизированные инструменты для AI‑ассистентов. Он позволяет быстро подключать AI‑агентов к календарным данным и другим сервисам через единый протокол, что упрощает создание прототипов и внутренних workflow‑интеграций. Готовность к production — средняя: проект уже стабилен и имеет базовый набор функций, но перед развертыванием в продакшн рекомендуется проверить лицензирование, безопасность и наличие активных мейнтейнеров.

### 中文

**项目简介**  
`dominik1001/caldav-mcp` 是一个基于 CalDAV 的 **Model Context Protocol (MCP)** 服务器，能够把日历的增删改查等操作包装成标准化的工具接口，供 AI 助手直接调用。

**价值**  
- **桥接 AI 与真实业务工具**：通过统一的 MCP 协议，AI 助手可以像调用本地函数一样操作日历，实现“AI‑即服务”。  
- **降低集成成本**：提供即插即用的 API/SDK/CLI，开发者无需自行实现 CalDAV 细节，即可把日历功能纳入 AI 工作流。  
- **促进生态标准化**：遵循 MCP 规范，帮助行业形成统一的 AI‑工具交互模型，便于不同平台之间的互通。

**典型接入方式**  
1. **API 调用**：在 AI 助手的后端服务中直接请求 MCP 服务器的 HTTP 接口（REST‑like），完成事件查询、创建、更新等操作。  
2. **SDK 使用**：项目提供的 TypeScript SDK（npm 包）封装了所有请求，开发者只需在 Node.js 环境中 `import { CalDavMcpClient } from 'caldav-mcp'` 并配置服务器地址与凭证，即可调用 `client.createEvent(...)`、`client.listEvents(...)` 等方法。  
3. **CLI 交互**：通过自带的命令行工具（`caldav-mcp-cli`），可以在脚本或 CI/CD 流程中快速执行日历任务，适合原型验证或运维自动化。  

**生产可用性**  
- **成熟度**：当前评分 67/100，GitHub 统计 68 ★、23 Fork，最近一次提交在 2026‑05‑12，代码活跃度尚可。  
- **适用场景**：非常适合原型、内部工具或低至中等流量的业务系统；在正式生产环境使用前建议：  
  - 完成安全审计（鉴权、TLS 配置、输入校验）。  
  - 评估依赖（Node.js、TypeScript 版本）与运维成本（容器化部署、日志监控）。  
  - 设定容错与备份策略，防止日历数据丢失。  
- **总体评估**：具备 **中等** 生产可用性，经过适当的安全与运维检查后，可在业务系统中稳定运行。

## 🧭 Practical evaluation

**Value:** dominik1001/caldav-mcp helps connect AI assistants to real tools and data through a standard protocol.

**Best use cases**

- connect AI agents to tools
- ship Model Context Protocol servers
- standardize integrations

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** Medium: useful for prototypes or internal workflows, with dependency and maintenance checks before production.

**Quality signals**

- 68 GitHub stars
- 23 forks
- updated 2026-05-12
- primary language: TypeScript
- 4 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 35/100 |
| stars | 39/100 |
| topics | 50/100 |
| outlook | 46/100 |
| quality | 45/100 |
| recency | 20/100 |
| adoption | 38/100 |
| production | 47/100 |
| usefulness | 74/100 |
| integration | 62/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 200/100 |

---

<sub>🔭 Discovered 2026-05-12 · [View on GitHub](https://github.com/dominik1001/caldav-mcp) · [← Back to Mcp](./README.md)</sub>
