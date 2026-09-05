# Doist/todoist-ai

[![Stars](https://img.shields.io/github/stars/Doist/todoist-ai?style=flat-square&color=yellow)](https://github.com/Doist/todoist-ai/stargazers) [![Forks](https://img.shields.io/github/forks/Doist/todoist-ai?style=flat-square&color=blue)](https://github.com/Doist/todoist-ai/network) [![Language](https://img.shields.io/badge/lang-TypeScript-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-69%2F100-brightgreen?style=flat-square)](#)

> A set of tools to connect to AI agents, to allow them to use Todoist on a user's behalf. Includes MCP support.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 477 |
| 🍴 **Forks** | 43 |
| 💻 **Language** | TypeScript |
| 📈 **Score** | 69/100 |
| 🗓️ **Last push** | 2026-09-05 |
| 🔍 **Source** | github |

## 🏷️ Topics

_no topics_

## 🎯 Categories

MCP

## 📝 Summary

### English

**Brief summary (2‑3 sentences)**  
Doist / todoist‑ai is an open‑source TypeScript library that implements the Model Context Protocol (MCP) so AI agents can interact with a user’s Todoist account on their behalf. It provides ready‑made connectors and server scaffolding for exposing Todoist functionality (tasks, projects, labels, etc.) to any MCP‑compatible LLM or assistant. With 477 stars and recent updates, the project is a practical starting point for building AI‑driven productivity tools.

**Value**  
- **Bridges AI and real‑world data**: By exposing Todoist through a standard MCP interface, developers can plug any LLM‑based assistant into a trusted task‑management system without writing custom API glue code.  
- **Accelerates AI‑tool integration**: The library ships both client‑side helpers and a reference MCP server, turning a “bare‑bones” AI prototype into a functional, user‑centric assistant in days rather than weeks.  
- **Reusable pattern**: Because MCP is a generic protocol, the same architecture can be extended to other SaaS tools, giving teams a repeatable way to expose internal services to AI agents.

**Practical adoption path**  
1. **Proof‑of‑concept** – Clone the repo, run the provided README steps, and connect a local LLM (e.g., OpenAI GPT‑4) to the demo MCP server. Verify that the assistant can list, create, and complete Todoist tasks.  
2. **Customization** – Extend the TypeScript handlers to map additional Todoist endpoints (e.g., reminders, filters) or to enforce business rules such as task‑ownership checks.  
3. **Secure deployment** – Containerize the MCP server, add OAuth 2.0 token handling for each user, and place it behind your organization’s API gateway.  
4. **Scale & monitor** – Deploy to a managed Kubernetes or serverless environment, instrument request logs, and add rate‑limiting to protect the Todoist API.  

**Production readiness**  
- **Maturity**: Medium. The codebase is actively maintained (last commit 2026‑05‑11) and has a modest but healthy community (≈ 500 stars, 40 forks). It is suitable for prototypes, internal tools, or beta releases.  
- **Dependencies**: Pure TypeScript with standard Todoist and MCP client libraries, making dependency management straightforward.  
- **Risks**: No major metadata or licensing issues identified, but a final security audit (OAuth token storage, input validation) and confirmation of long‑term maintainers are advisable before a full production rollout.  

Overall, todoist‑ai offers a low‑friction way to give AI assistants real productivity power, with a clear incremental path from a sandbox demo to a hardened production service.

### Русский

Doist /todoist‑ai — набор TypeScript‑инструментов, позволяющих AI‑ассистентам взаимодействовать с Todoist через Model Context Protocol, что упрощает подключение искусственного интеллекта к реальному рабочему инструменту. Типичный сценарий: быстро развернуть прототип интеграции (например, небольшую POC‑службу MCP) и, после проверки README и базовых зависимостей, масштабировать её до внутренних или клиентских процессов. Готовность к production — средняя: проект стабилен и активно поддерживается (477 ★, последние коммиты), но перед выводом в продакшн требуется окончательная проверка лицензии, безопасности и поддержки.

### 中文

**项目简介（2‑3 句）**  
Doist/todoist‑ai 是一套用于把 AI 代理与 Todoist 账户绑定的工具包，支持 Model Context Protocol（MCP），让 AI 能在用户授权下直接创建、查询、更新任务。该项目通过标准化的协议把 AI 助手与真实业务数据和操作桥接起来。

**价值**  
- **统一协议**：使用 MCP 为 AI 与外部工具（如 Todoist）提供一致的交互方式，降低多平台集成的复杂度。  
- **加速开发**：开发者只需调用封装好的 SDK，即可让任意语言模型（ChatGPT、Claude、Gemini 等）直接操作任务列表，快速原型化 AI 助手。  
- **可扩展**：除了 Todoist，还可以在同一协议框架下接入其他生产力工具，形成统一的 AI‑to‑Tool 生态。

**典型接入方式**  
1. **阅读 README**，确认项目依赖（Node.js、TypeScript）并完成本地构建。  
2. **在 Todoist 开发者后台创建 API Token**，并在项目的 `.env` 中配置 `TODOIST_API_TOKEN`。  
3. **启动 MCP 服务器**（`npm run start:mcp`），该服务器实现了标准的 `model-context` 接口。  
4. **在 AI 代理（如 OpenAI Function Calling、LangChain、LLM‑Ops）中注册该 MCP 端点**，即可在提示中使用 `create_task`, `list_tasks` 等函数调用。  
5. **先做 PoC**：在本地或沙盒环境发送几条任务指令验证权限、响应格式和错误处理，随后在 README 中记录集成步骤。

**生产可用性**  
- **成熟度**：GitHub 477 ★、43 Fork，最近一次提交在 2026‑05‑11，代码活跃度尚可。  
- **适用场景**：适合内部工具、原型项目或受控的业务流程自动化；若要在面向用户的产品中使用，建议进行安全审计、依赖锁定和容错设计。  
- **风险**：需进一步确认许可证兼容性、依赖安全（尤其是 OAuth/Token 管理）以及维护者响应速度。  
- **准备度**：中等（Medium）— 在完成安全、监控和容错措施后，可投入生产环境；在此之前建议先在小规模、受控环境中验证。

## 🧭 Practical evaluation

**Value:** Doist/todoist-ai helps connect AI assistants to real tools and data through a standard protocol.

**Best use cases**

- connect AI agents to tools
- ship Model Context Protocol servers
- standardize integrations

**Integration notes:** Looks feasible to evaluate, but integration should start with a small proof of concept and README check.

**Production readiness:** Medium: useful for prototypes or internal workflows, with dependency and maintenance checks before production.

**Quality signals**

- 477 GitHub stars
- 43 forks
- updated 2026-05-11
- primary language: TypeScript

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 41/100 |
| stars | 57/100 |
| topics | 0/100 |
| outlook | 69/100 |
| quality | 59/100 |
| recency | 80/100 |
| adoption | 53/100 |
| production | 66/100 |
| usefulness | 90/100 |
| integration | 62/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 100/100 |

---

<sub>🔭 Discovered 2026-05-11 · [View on GitHub](https://github.com/Doist/todoist-ai) · [← Back to Mcp](./README.md)</sub>
