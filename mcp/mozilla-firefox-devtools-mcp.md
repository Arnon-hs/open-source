# mozilla/firefox-devtools-mcp

[![Stars](https://img.shields.io/github/stars/mozilla/firefox-devtools-mcp?style=flat-square&color=yellow)](https://github.com/mozilla/firefox-devtools-mcp/stargazers) [![Forks](https://img.shields.io/github/forks/mozilla/firefox-devtools-mcp?style=flat-square&color=blue)](https://github.com/mozilla/firefox-devtools-mcp/network) [![Language](https://img.shields.io/badge/lang-TypeScript-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-60%2F100-brightgreen?style=flat-square)](#)

> Model Context Protocol server for Firefox DevTools - enables AI assistants to inspect and control Firefox browser through the Remote Debugging Protocol

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 238 |
| 🍴 **Forks** | 39 |
| 💻 **Language** | TypeScript |
| 📈 **Score** | 60/100 |
| 🗓️ **Last push** | 2026-08-24 |
| 🔍 **Source** | github |

## 🏷️ Topics

`claude-code` `firefox` `mcp` `mcp-server`

## 🎯 Categories

MCP · Backend

## 📝 Summary

### English

**Brief Summary**  
Mozilla’s **firefox-devtools-mcp** implements the Model Context Protocol (MCP) server for Firefox DevTools, letting AI assistants inspect and control a running Firefox instance via the Remote Debugging Protocol. By exposing a standard MCP interface, it bridges generative AI agents with real‑world browser tooling, making it possible to automate debugging, testing, and UI inspection tasks.

**Value**  
- **Standardized AI‑to‑tool integration**: MCP provides a language‑agnostic contract, so any AI model that understands the protocol can interact with Firefox without custom adapters.  
- **Accelerates AI‑augmented workflows**: Developers can prototype agents that automatically capture page state, manipulate the DOM, or run performance audits, turning AI from a “chat‑only” assistant into an actionable tool.  
- **Reusable building block**: The server can be deployed alongside existing DevTools pipelines, enabling multiple agents or services to share a single, secure debugging endpoint.

**Practical Adoption Path**  
1. **Prototype** – Clone the repo, run the TypeScript server locally, and point an AI model (e.g., OpenAI function‑calling or LangChain tool) at the MCP endpoint. Use the provided CLI/SDK examples to issue simple commands like `navigate`, `querySelector`, or `takeScreenshot`.  
2. **Integration** – Containerize the server (Dockerfile is included) and expose it behind your internal network. Update your AI orchestration layer to register the MCP service as a tool with appropriate authentication (e.g., token‑based or mTLS).  
3. **Validation** – Write end‑to‑end tests that simulate typical agent workflows (e.g., automated regression testing, accessibility checks). Verify that the server correctly forwards Remote Debugging Protocol messages and that the browser remains stable under load.  
4. **Productionization** – Harden the deployment: enable TLS, enforce least‑privilege permissions on the Firefox instance, and monitor resource usage. Integrate with your CI/CD pipeline to keep the server version in sync with Firefox updates.

**Production Readiness**  
- **Maturity**: Medium. The project is actively maintained (last update 2026‑06‑26) and has a modest community (≈ 240 ★, 39 forks). It is suitable for prototypes and internal tooling, but it still requires a review of licensing, security hardening, and long‑term maintainer commitment before mission‑critical rollout.  
- **Dependencies**: Built in TypeScript and depends on Firefox’s Remote Debugging Protocol; ensure compatible Firefox versions and keep the Node runtime up‑to‑date.  
- **Operational considerations**: Deploy in a controlled environment, enable logging and health checks, and plan for periodic updates aligned with Firefox releases. With these steps, the server can be a reliable component in production AI‑assistant pipelines.

### Русский

**Краткое резюме:**  
Mozilla / firefox-devtools-mcp — это сервер Model Context Protocol для Firefox DevTools, позволяющий AI‑ассистентам напрямую инспектировать и управлять браузером через Remote Debugging Protocol. Типичный сценарий — подключение AI‑агентов к реальным инструментам (например, автоматическое тестирование, отладка или сбор метрик) с помощью единого стандартизированного протокола, а также развертывание собственных MCP‑серверов для интеграций. Проект находится на среднем уровне готовности к production: подходит для прототипов и внутренних воркфлоу, но требует проверки зависимостей, лицензии и безопасности перед масштабным использованием.

### 中文

**项目简介**  
mozilla/firefox-devtools-mcp 是 Firefox DevTools 的 Model Context Protocol（MCP）服务器，实现了通过 Remote Debugging Protocol 让 AI 助手实时检查、控制浏览器的能力。  

**价值**  
- 为 AI 代理提供统一、标准化的接口，直接对真实的浏览器环境进行查询与操作，弥补了“AI 只能在模拟数据上演练”的缺口。  
- 通过 MCP 可以快速搭建 AI‑to‑Tool 场景，降低集成成本，促进 AI 与开发者工具生态的协同。  

**典型接入方式**  
1. **作为本地或容器化服务运行**：克隆仓库后 `npm install && npm run start` 启动 MCP 服务器，默认监听 127.0.0.1:...。  
2. **通过 SDK/CLI 调用**：项目提供 TypeScript SDK 与 CLI，AI 框架（如 LangChain、OpenAI Function Calling）只需引用对应库，即可向 MCP 发送 `inspect`, `navigate`, `evaluate` 等指令。  
3. **在 CI/CD 或内部工具链中嵌入**：利用 Docker 镜像（已在 GitHub Packages 中发布）在自动化脚本里启动，配合浏览器的 Remote Debugging 端口即可完成端到端的 AI‑驱动测试。  

**生产可用性**  
- **成熟度**：GitHub 238 星、39 Fork，活跃于 2026 年 6 月更新，代码基于 TypeScript，结构清晰。  
- **适用场景**：非常适合原型开发、内部工作流、AI‑辅助调试与自动化测试；在生产环境使用前建议完成：  
  - 依赖审计（第三方 npm 包的安全性）  
  - 性能基准（并发会话数、网络延迟）  
  - 运维监控（日志、异常上报）  
- **风险**：许可证、长期维护者活跃度以及安全审计仍需进一步确认。总体上，项目具备 **中等** 的生产就绪度，可在受控环境中部署并逐步推广。

## 🧭 Practical evaluation

**Value:** mozilla/firefox-devtools-mcp helps connect AI assistants to real tools and data through a standard protocol.

**Best use cases**

- connect AI agents to tools
- ship Model Context Protocol servers
- standardize integrations

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** Medium: useful for prototypes or internal workflows, with dependency and maintenance checks before production.

**Quality signals**

- 238 GitHub stars
- 39 forks
- updated 2026-06-26
- primary language: TypeScript
- 4 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 40/100 |
| stars | 51/100 |
| topics | 50/100 |
| outlook | 56/100 |
| quality | 54/100 |
| recency | 40/100 |
| adoption | 48/100 |
| production | 55/100 |
| usefulness | 74/100 |
| integration | 62/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 200/100 |

---

<sub>🔭 Discovered 2026-06-26 · [View on GitHub](https://github.com/mozilla/firefox-devtools-mcp) · [← Back to Mcp](./README.md)</sub>
