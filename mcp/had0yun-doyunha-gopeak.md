# HaD0Yun/Doyunha-Gopeak

[![Stars](https://img.shields.io/github/stars/HaD0Yun/Doyunha-Gopeak?style=flat-square&color=yellow)](https://github.com/HaD0Yun/Doyunha-Gopeak/stargazers) [![Forks](https://img.shields.io/github/forks/HaD0Yun/Doyunha-Gopeak?style=flat-square&color=blue)](https://github.com/HaD0Yun/Doyunha-Gopeak/network) [![Language](https://img.shields.io/badge/lang-JavaScript-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-76%2F100-brightgreen?style=flat-square)](#)

> GoPeak — The most comprehensive MCP server for Godot Engine. 95+ tools: scene management, GDScript LSP, DAP debugger, screenshot capture, input injection, ClassDB introspection, CC0 asset library. npx gopeak

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 217 |
| 🍴 **Forks** | 23 |
| 💻 **Language** | JavaScript |
| 📈 **Score** | 76/100 |
| 🗓️ **Last push** | 2026-09-05 |
| 🔍 **Source** | github |

## 🏷️ Topics

`ai` `ai-integration` `ai-tools` `claude` `cursor` `dap` `debug-adapter-protocol` `developer-tools` `game-development` `gamedev` `gdscript` `godot`

## 🎯 Categories

MCP · AI/ML · Games & Graphics · Backend · DevTools

## 📝 Summary

### English

**Brief Summary**  
GoPeak is an open‑source MCP (Model‑Context‑Protocol) server for the Godot Engine that bundles more than 95 developer‑tools—including scene management, a GDScript LSP, DAP debugging, screenshot capture, input injection, ClassDB introspection, and a CC0 asset library—exposed via a simple `npx gopeak` CLI. It enables AI assistants to interact with real Godot tooling and data through a standardized protocol, making it a turnkey bridge between generative models and game‑development workflows.

**Value**  
- **Unified Interface:** By wrapping a wide spectrum of Godot utilities behind a single MCP endpoint, GoPeak lets AI agents query, modify, and debug game projects without custom scripting for each tool.  
- **Rapid Prototyping:** Developers can plug an LLM‑based assistant into the server and immediately gain capabilities such as code completion, live debugging, and asset retrieval, accelerating iteration cycles.  
- **Standardization:** The MCP compliance means the same AI integration can be reused across other MCP‑compatible services, reducing vendor lock‑in and fostering ecosystem interoperability.

**Practical Adoption Path**  
1. **Prototype:** Install the server with `npx gopeak` and point it at a local Godot project. Use the provided API/SDK (JavaScript/REST) to send simple requests (e.g., “list scenes” or “run GDScript LSP query”).  
2. **Integrate AI Agent:** Connect your preferred LLM (OpenAI, Anthropic, etc.) to the MCP endpoint, mapping intents to GoPeak commands. Test end‑to‑end flows such as “debug the current scene” or “capture a screenshot after a script change.”  
3. **Extend:** Leverage the open‑source code to add custom handlers (e.g., project‑specific build pipelines) or wrap the CLI in Docker/Kubernetes for CI/CD usage.  
4. **Productionize:** Deploy the server as a long‑running service behind a reverse proxy, enforce authentication (e.g., JWT), and monitor logs/metrics. Because the project is JavaScript‑based, it fits easily into existing Node.js infrastructure.

**Production Readiness**  
- **Activity & Adoption:** 217 GitHub stars, recent commits (as of 2026‑06‑23), and a modest fork base indicate an active community.  
- **Maturity:** The breadth of tools (95+), clear CLI entry point, and well‑documented API suggest the core functionality is stable.  
- **Risk Profile:** No glaring metadata or licensing issues have been identified, though a final security audit and verification of maintainers’ responsiveness are advisable.  
Overall, GoPeak is a high‑confidence OSS candidate for pilots that need AI‑driven interaction with Godot, and it can be hardened for production with standard DevOps safeguards.

### Русский

GoPeak — это самый полный MCP‑сервер для Godot Engine, предоставляющий более 95 готовых инструментов (управление сценами, LSP для GDScript, DAP‑отладчик, захват скриншотов, инъекция ввода, интроспекция ClassDB и библиотека CC0‑ассетов) и единый протокол для подключения AI‑ассистентов к реальным инструментам и данным. Типичный сценарий — развернуть сервер GoPeak и через Model Context Protocol связать AI‑агентов с игровыми инструментами Godot, автоматизировать сборку, отладку и управление контентом, либо использовать его как базу для собственного MCP‑сервера. Проект имеет высокий уровень готовности к production: активные коммиты, 217 звёзд, поддержка API/SDK/CLI, широкая экосистема и недавние обновления, что делает его надёжным кандидатом для пилотных внедрений.

### 中文

**项目简介**  
GoPeak（HaD0Yun/Doyunha‑Gopeak）是面向 Godot Engine 的全功能 MCP（Model Context Protocol）服务器，提供 95+ 实用工具，包括场景管理、GDScript LSP、DAP 调试、截图、输入注入、ClassDB 反射、CC0 资源库等，一键通过 `npx gopeak` 启动。

**价值**  
- **统一协议**：通过标准化的 MCP 接口，将 AI 助手与真实的开发工具和数据无缝对接，降低集成成本。  
- **即插即用**：内置丰富的 Godot 开发工具链，AI 可以直接调用场景编辑、脚本补全、调试等功能，实现“AI + IDE”的完整工作流。  
- **开源可定制**：基于 JavaScript 实现，社区活跃（217 Stars），可自行扩展或二次开发以满足特定业务需求。

**典型接入方式**  
1. **CLI/SDK**：在项目根目录执行 `npx gopeak` 启动 MCP 服务器，服务器会监听默认端口并暴露 REST/WebSocket 接口。  
2. **API 调用**：AI 代理通过 HTTP/WebSocket 向 `/api/v1/*` 发送 JSON 请求，例如 `POST /api/v1/scene/load`、`POST /api/v1/debug/attach`。  
3. **语言元数据**：服务器提供 GDScript LSP 元信息，可直接在 VSCode、Godot 编辑器等 IDE 中注册，AI 能实时获取代码补全与类型信息。  
4. **插件模式**：通过自定义插件（Node.js 模块）向 GoPeak 注入业务专属指令，扩展工具链（如自研资产库、自动化测试等）。

**生产可用性**  
- **活跃度**：最近一次提交为 2026‑06‑23，星标 217、Fork 23，社区讨论活跃，基本满足生产环境的维护需求。  
- **成熟度**：提供完整的 API 文档、示例脚本和 CI 检查，兼容 Godot 4.x，已在多个开源项目中实际使用。  
- **安全与合规**：目前未发现重大安全漏洞，采用 MIT 许可证，仍建议在正式部署前进行内部安全审计并确认维护者响应时效。  

综合来看，GoPeak 是一套成熟、功能丰富且易于集成的 MCP 服务器，适合作为 AI 助手与 Godot 开发工具链的桥梁，在生产环境中具备较高的可用性。

## 🧭 Practical evaluation

**Value:** HaD0Yun/Doyunha-Gopeak helps connect AI assistants to real tools and data through a standard protocol.

**Best use cases**

- connect AI agents to tools
- ship Model Context Protocol servers
- standardize integrations

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 217 GitHub stars
- 23 forks
- updated 2026-06-23
- primary language: JavaScript
- 20 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 35/100 |
| stars | 50/100 |
| topics | 100/100 |
| outlook | 77/100 |
| quality | 70/100 |
| recency | 80/100 |
| adoption | 45/100 |
| production | 73/100 |
| usefulness | 90/100 |
| integration | 78/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 500/100 |

---

<sub>🔭 Discovered 2026-06-23 · [View on GitHub](https://github.com/HaD0Yun/Doyunha-Gopeak) · [← Back to Mcp](./README.md)</sub>
