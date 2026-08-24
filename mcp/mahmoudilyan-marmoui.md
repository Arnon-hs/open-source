# mahmoudilyan/marmoui

[![Stars](https://img.shields.io/github/stars/mahmoudilyan/marmoui?style=flat-square&color=yellow)](https://github.com/mahmoudilyan/marmoui/stargazers) [![Forks](https://img.shields.io/github/forks/mahmoudilyan/marmoui?style=flat-square&color=blue)](https://github.com/mahmoudilyan/marmoui/network) [![Language](https://img.shields.io/badge/lang-TypeScript-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-56%2F100-brightgreen?style=flat-square)](#)

> The AI agentic designer — open-source React design system + MCP that lets Claude, Codex, Cursor & Gemini build production UI in minutes. No AI slop.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 28 |
| 🍴 **Forks** | — |
| 💻 **Language** | TypeScript |
| 📈 **Score** | 56/100 |
| 🗓️ **Last push** | 2026-08-24 |
| 🔍 **Source** | github |

## 🏷️ Topics

`ai-agents` `claude` `components` `design-system` `mcp` `react`

## 🎯 Categories

MCP · AI/ML · Frontend · Design

## 📝 Summary

### English

**Brief Summary (2‑3 sentences)**  
Marmoui is an open‑source React design system paired with a Model Context Protocol (MCP) server that lets AI assistants such as Claude, Codex, Cursor, and Gemini generate production‑ready UI components in minutes—without the “AI fluff.” By exposing a standard protocol for connecting AI agents to real tools and data, Marmoui enables developers to plug AI‑driven design workflows directly into their front‑end stacks.

**Value Proposition**  
- **Unified AI‑to‑Tool Bridge:** Marmoui implements the Model Context Protocol, turning abstract language‑model outputs into concrete UI code, API calls, or SDK actions. This eliminates the need for bespoke glue code each time an AI assistant is used.  
- **Accelerated UI Production:** Designers and engineers can prompt an AI to create or modify React components that instantly conform to the project's design system, dramatically shortening prototyping cycles.  
- **Standardized Integration:** Because the protocol is open and language‑agnostic, the same Marmoui server can serve multiple AI providers (Claude, Gemini, etc.) and be reused across projects, fostering consistency and reducing integration debt.

**Practical Adoption Path**  

| Step | Action | Reason |
|------|--------|--------|
| 1️⃣  | **Spin up the MCP server** (via the provided Docker image, CLI, or npm script). | Provides the API endpoint that AI agents will call to request UI generation or data access. |
| 2️⃣  | **Add the React design system** (`@marmoui/ui`) to your front‑end monorepo. | Gives you the component library and styling tokens that the AI will target. |
| 3️⃣  | **Configure AI agents** (Claude, Gemini, etc.) with the server’s endpoint and authentication token. | Allows the LLM to invoke the protocol for code generation, data queries, or tool actions. |
| 4️⃣  | **Define usage contracts** (e.g., “generate a Card component with props X”) in a JSON schema or TypeScript type that the MCP validates. | Guarantees that generated code meets type safety and design guidelines. |
| 5️⃣  | **Integrate into CI/CD** – run a lint/format/type‑check step on AI‑generated code before merge. | Catches regressions early and ensures production‑grade quality. |
| 6️⃣  | **Iterate & monitor** – collect telemetry from the MCP server (request latency, error rates) and refine prompts or schemas. | Improves reliability and helps you gauge ROI. |

**Production Readiness Assessment**  

- **Maturity:** Medium. The repo is actively maintained (last commit 2026‑07‑13) and has modest community traction (≈28 stars). The TypeScript codebase and clear API/CLI surface make it easy to evaluate in a sandbox.  
- **Risk Areas:**  
  * **License & security:** The license is not highlighted in the summary; a review is needed to confirm it aligns with your organization’s policies.  
  * **Dependency health:** The project pulls in typical React and UI‑tooling packages; a dependency audit is recommended before production use.  
  * **Maintainer continuity:** Only a single primary maintainer is listed; consider forking or contributing to ensure long‑term support.  
- **Fit for Production:** Suitable for internal tools, prototypes, or as a “pilot” UI generation layer. For customer‑facing production, add a gate‑keeping step (code review, automated testing) and perform a security audit of the MCP server.

**Bottom Line**  
Marmoui offers a practical, standards‑based way to harness LLMs for front‑end development, turning AI prompts into ready‑to‑ship React components. With a straightforward setup and clear integration steps, teams can start experimenting quickly, but should perform the usual license, security, and maintenance checks before scaling to mission‑critical production environments.

### Русский

Резюме проекта mahmoudilyan/marmoui:

mahmoudilyan/marmoui — это открытое исходное кода решение для интеграции AI-ассистентов с реальными инструментами и данными через единый протокол. Этот проект позволяет быстро создавать производительную UI с помощью AI-агентов, таких как Claude, Codex, Cursor и Gemini. mahmoudilyan/marmoui готов к использованию в прототипах или внутренних процессах, но требует проверки зависимостей и технической поддержки до использования в производстве.

### 中文

**项目简介（2–3 句）**  
Marmoui 是一个开源的 React 设计系统 + Model‑Context‑Protocol（MCP）实现，旨在让 Claude、Codex、Cursor、Gemini 等 AI 助手能够在几分钟内生成可直接投产的 UI，且不带任何“AI 垃圾”。它通过统一的协议把 AI 与真实的前端工具和数据连接起来，帮助开发者快速搭建和交付界面。

**价值**  
- **统一协议**：提供标准化的 MCP 接口，让各种大模型 AI 能以同一方式调用 UI 组件、获取设计系统元数据，从而实现“一次接入，多模型复用”。  
- **加速开发**：AI 可以直接在设计系统中生成、修改、预览组件，显著缩短原型到生产的周期。  
- **降低门槛**：前端团队只需维护一次 React 组件库，即可为所有 AI 助手提供一致的 UI 输出，避免重复实现。

**典型接入方式**  
1. **SDK / NPM 包**：在项目中 `npm install @marmoui/react`（或对应的 MCP SDK），通过 TypeScript 接口调用 `MCPClient` 与 AI 交互。  
2. **CLI**：使用 `marmoui-cli` 启动本地 MCP 服务器，配置好模型凭证后，AI 只需发送标准化的 JSON 请求即可获取组件代码或渲染指令。  
3. **REST / WebSocket API**：部署 `marmoui-server`（Docker 镜像或直接 `node server.js`），对外提供 HTTP/WS 接口，供内部工具或第三方 AI 平台调用。  

**生产可用性**  
- **成熟度**：当前评分 65/100，GitHub 28 星，最近一次提交在 2026‑07‑13，代码以 TypeScript 编写，结构清晰。适合作为内部原型或业务流程自动化的底层框架。  
- **依赖与维护**：依赖主要是 React、TypeScript 与少量网络库，社区活跃度一般，建议在生产环境前进行安全审计并锁定依赖版本。  
- **上线建议**：先在预生产环境部署 MCP 服务器，做一次完整的 AI‑→‑Marmoui‑→‑前端流水线验证；确认性能、权限控制和日志审计后，再逐步推广到正式业务。  

总体而言，Marmoui 在连接 AI 与前端设计系统方面提供了清晰的标准和易用的实现，适合作为内部工具链的加速层；在正式生产使用前需完成安全、依赖锁定和运维监控等检查。

## 🧭 Practical evaluation

**Value:** mahmoudilyan/marmoui helps connect AI assistants to real tools and data through a standard protocol.

**Best use cases**

- connect AI agents to tools
- ship Model Context Protocol servers
- standardize integrations

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** Medium: useful for prototypes or internal workflows, with dependency and maintenance checks before production.

**Quality signals**

- 28 GitHub stars
- updated 2026-07-13
- primary language: TypeScript
- 6 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 0/100 |
| stars | 31/100 |
| topics | 75/100 |
| outlook | 52/100 |
| quality | 46/100 |
| recency | 40/100 |
| adoption | 22/100 |
| production | 52/100 |
| usefulness | 74/100 |
| integration | 62/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 400/100 |

---

<sub>🔭 Discovered 2026-07-13 · [View on GitHub](https://github.com/mahmoudilyan/marmoui) · [← Back to Mcp](./README.md)</sub>
