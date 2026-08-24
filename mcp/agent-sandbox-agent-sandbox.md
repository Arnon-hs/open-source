# agent-sandbox/agent-sandbox

[![Stars](https://img.shields.io/github/stars/agent-sandbox/agent-sandbox?style=flat-square&color=yellow)](https://github.com/agent-sandbox/agent-sandbox/stargazers) [![Forks](https://img.shields.io/github/forks/agent-sandbox/agent-sandbox?style=flat-square&color=blue)](https://github.com/agent-sandbox/agent-sandbox/network) [![Language](https://img.shields.io/badge/lang-Go-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-65%2F100-brightgreen?style=flat-square)](#)

> Agent-Sandbox is an E2B compatible easy-to-use enterprise-grade sandboxes for AI Agents. Allows Agents to securely run untrusted LLM-generated Code, Browser use, Computer use, and deploy Website etc.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 154 |
| 🍴 **Forks** | 14 |
| 💻 **Language** | Go |
| 📈 **Score** | 65/100 |
| 🗓️ **Last push** | 2026-08-24 |
| 🔍 **Source** | github |

## 🏷️ Topics

`agent` `agent-sandbox` `ai-infra` `ai-sandbox` `browser-use` `code-executor` `computer-use` `container` `e2b-compatible` `kubernetes-native` `mcp` `sandbox`

## 🎯 Categories

MCP · AI/ML · DevOps/Infra

## 📝 Summary

### English

**Summary**  
Agent‑Sandbox is an open‑source, E2B‑compatible sandbox platform that lets AI agents safely execute untrusted LLM‑generated code, browse the web, control a virtual computer, or deploy websites. By exposing a standard Model Context Protocol (MCP) API/SDK/CLI, it bridges AI assistants with real‑world tools and data while maintaining enterprise‑grade isolation.

**Value**  
The project provides a turnkey, language‑agnostic runtime that removes the security and integration friction of letting LLMs interact with external systems. Teams can quickly prototype “agent‑as‑a‑service” capabilities—such as automated browsing, data extraction, or CI/CD orchestration—without building custom sandboxes from scratch.

**Practical adoption path**  

1. **Evaluate the API/SDK** – Clone the repo, run the provided Docker image or binary, and call the MCP endpoints from a test LLM prompt.  
2. **Integrate** – Replace existing ad‑hoc tool calls with the sandbox’s `runCode`, `openBrowser`, `controlComputer`, or `deployWebsite` methods via the Go client or the generated OpenAPI client for other languages.  
3. **Secure & scale** – Configure resource limits, network policies, and authentication (OAuth/JWT) as documented; then deploy the sandbox service behind your internal gateway or as a managed SaaS component.  
4. **Productionize** – Add monitoring (Prometheus metrics), logging, and CI pipelines to roll out updates; optionally run multiple sandbox instances for multi‑tenant isolation.

**Production readiness**  
With 154 ★, recent commits (as of 2026‑06‑24), active community activity, and an enterprise‑grade Go codebase, Agent‑Sandbox shows strong signals for a serious pilot. The clear API surface, Docker/CLI distribution, and modest dependency footprint make it easy to test in staging. While the license and long‑term maintainer commitment still need a final check, the project’s maturity and ecosystem adoption suggest it is ready for production use after standard security review.

### Русский

**Agent‑Sandbox** — это open‑source платформа (Go) совместимая с E2B, предоставляющая корпоративные «песочницы» для безопасного выполнения кода, браузерных и компьютерных действий, а также развертывания веб‑сайтов, генерируемых LLM‑агентами. Типичный сценарий — подключение AI‑ассистентов к реальным инструментам и данным через единый протокол (Model Context Protocol), что упрощает интеграцию, построение серверов контекста модели и стандартизацию взаимодействий. Проект имеет высокий уровень готовности к production: активные коммиты, 154 звёзд, широкую экосистему и готовые API/SDK/CLI, хотя окончательная проверка лицензии и безопасности всё‑ещё требуется.

### 中文

**项目简介**  
Agent‑Sandbox（`agent-sandbox/agent-sandbox`）是一款兼容 E2B 的企业级沙箱，专为 AI Agent 设计。它能够安全地执行 LLM 生成的代码、浏览器操作、桌面交互以及网站部署等不受信任的任务，为 AI 助手提供真实工具和数据的接入层。

**价值主张**  
- **安全可信**：在隔离的沙箱环境中运行外部代码，防止恶意行为影响主机。  
- **统一协议**：通过标准的 Model Context Protocol（MCP）让不同 AI 助手以一致的方式调用浏览器、文件系统、网络等资源。  
- **快速落地**：提供 API、SDK 与 CLI，开发者只需几行代码即可将 AI Agent 与实际工具、数据源对接，显著缩短集成周期。

**典型接入方式**  
1. **API/HTTP**：直接调用沙箱提供的 RESTful 接口，提交任务（代码、浏览指令等）并获取执行结果。  
2. **SDK**：使用官方 Go（或其他语言）SDK，封装好请求、认证与结果轮询，适合服务端或微服务集成。  
3. **CLI**：通过 `agent-sandbox` 命令行工具本地调试或在 CI/CD 流水线中执行沙箱任务。  

**生产可用性**  
- **活跃维护**：最近一次提交于 2026‑06‑24，仓库星标 154，Fork 14，持续迭代。  
- **技术成熟**：核心实现使用 Go，拥有 12+ 主题标签，覆盖浏览器、文件系统、网络等常用场景。  
- **生态兼容**：兼容 E2B 标准，易与现有 MCP 服务器或其他 AI 平台对接。  
- **风险提示**：仍需对许可证（MIT/Apache 等）和安全审计进行最终确认，但整体成熟度足以支撑正式的生产试点。

## 🧭 Practical evaluation

**Value:** agent-sandbox/agent-sandbox helps connect AI assistants to real tools and data through a standard protocol.

**Best use cases**

- connect AI agents to tools
- ship Model Context Protocol servers
- standardize integrations

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 154 GitHub stars
- 14 forks
- updated 2026-06-24
- primary language: Go
- 12 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 29/100 |
| stars | 47/100 |
| topics | 100/100 |
| outlook | 59/100 |
| quality | 59/100 |
| recency | 40/100 |
| adoption | 42/100 |
| production | 59/100 |
| usefulness | 74/100 |
| integration | 78/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 300/100 |

---

<sub>🔭 Discovered 2026-06-24 · [View on GitHub](https://github.com/agent-sandbox/agent-sandbox) · [← Back to Mcp](./README.md)</sub>
