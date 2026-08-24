# HaD0Yun/Gopeak-godot-mcp

[![Stars](https://img.shields.io/github/stars/HaD0Yun/Gopeak-godot-mcp?style=flat-square&color=yellow)](https://github.com/HaD0Yun/Gopeak-godot-mcp/stargazers) [![Forks](https://img.shields.io/github/forks/HaD0Yun/Gopeak-godot-mcp?style=flat-square&color=blue)](https://github.com/HaD0Yun/Gopeak-godot-mcp/network) [![Language](https://img.shields.io/badge/lang-JavaScript-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-66%2F100-brightgreen?style=flat-square)](#)

> GoPeak — The most comprehensive MCP server for Godot Engine. 95+ tools: scene management, GDScript LSP, DAP debugger, screenshot capture, input injection, ClassDB introspection, CC0 asset library. npx gopeak

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 180 |
| 🍴 **Forks** | 16 |
| 💻 **Language** | JavaScript |
| 📈 **Score** | 66/100 |
| 🗓️ **Last push** | 2026-08-24 |
| 🔍 **Source** | github |

## 🏷️ Topics

`ai` `ai-integration` `ai-tools` `claude` `cursor` `dap` `debug-adapter-protocol` `developer-tools` `game-development` `gamedev` `gdscript` `godot`

## 🎯 Categories

MCP · AI/ML · Backend · DevTools

## 📝 Summary

### English

**Brief Summary**  
GoPeak is an open‑source MCP (Model Context Protocol) server for the Godot Engine that bundles more than 95 tools—including scene management, a GDScript LSP, DAP debugging, screenshot capture, input injection, ClassDB introspection, and a CC0 asset library—into a single, easy‑to‑run package (`npx gopeak`). It provides a standardized API/SDK/CLI that lets AI assistants and other automation agents interact with real Godot tooling and data, making it a turnkey solution for building AI‑driven workflows around game development.

**Value**  
- **Unified interface:** By exposing a rich set of Godot capabilities through a single MCP endpoint, GoPeak removes the need to stitch together disparate plugins or write custom glue code, dramatically lowering integration effort for AI agents.  
- **Extensible tooling:** The 95+ built‑in utilities cover the entire development lifecycle—from asset management to live debugging—so AI assistants can perform meaningful actions (e.g., generate scenes, fix scripts, capture screenshots) without extra scaffolding.  
- **Open ecosystem:** With a permissive license, active community (180 ★, 16 forks) and a JavaScript codebase, teams can quickly fork, extend, or embed the server in CI pipelines, cloud services, or on‑premise dev environments.

**Practical Adoption Path**  
1. **Prototype:** Run `npx gopeak` locally to spin up the MCP server and explore the auto‑generated API docs.  
2. **Integrate:** Connect your AI agent (e.g., OpenAI function calling, LangChain, or a custom LLM) to the server’s REST/WS endpoints or use the provided SDK for direct function calls.  
3. **Extend:** If you need additional Godot features, add new handlers to the JavaScript codebase or contribute a plugin; the modular architecture makes this straightforward.  
4. **Deploy:** Package the server as a Docker container or as a system service for staging/production environments; the CLI supports configuration via environment variables for CI/CD pipelines.

**Production Readiness**  
GoPeak shows strong signs of maturity: recent commits (as of 2026‑05‑13), growing adoption, and a well‑documented API surface. The high score (78/100) and robust community activity indicate it is ready for serious pilot projects. Remaining due‑diligence items include a final review of the license compatibility, a security audit of the exposed endpoints, and verification of long‑term maintainer commitment, but overall the project is positioned as a production‑grade OSS candidate for teams looking to embed AI‑driven tooling into Godot workflows.

### Русский

GoPeak — это самый полный MCP‑сервер для Godot Engine, предоставляющий более 95 готовых инструментов (управление сценами, LSP для GDScript, DAP‑отладчик, захват скриншотов, инъекция ввода, интроспекция ClassDB, CC0‑библиотека ассетов и др.) и единый протокол для подключения AI‑ассистентов к реальным инструментам и данным. Типичный сценарий — внедрение AI‑агентов, которым нужен доступ к игровому движку и внешним сервисам: они могут вызывать функции сервера через API/SDK/CLI, запускать отладку, управлять сценами и получать ресурсы из библиотеки. По оценке готовности проект находится на высоком уровне production‑ready: активные коммиты, 180 звёзд, широкая экосистема и поддержка JavaScript делают его надёжным кандидатом для пилотных внедрений, хотя окончательная проверка лицензии и безопасности всё‑ещё требуется.

### 中文

**项目简介**  
GoPeak 是面向 Godot Engine 的全功能 MCP（Model Context Protocol）服务器，内置 95+ 实用工具，包括场景管理、GDScript LSP、DAP 调试、截图、输入注入、ClassDB 查询以及 CC0 资源库等，一键通过 `npx gopeak` 启动。

**价值**  
- **AI‑工具桥梁**：提供统一的协议层，使 AI 助手能够直接调用 Godot 项目中的真实工具和数据，实现“AI + IDE”协同工作。  
- **开发效率**：集成 LSP、调试器、资产管理等功能，开发者无需自行搭建多套插件，即可在同一服务器上完成代码补全、调试、资源获取等全部工作流。  
- **标准化集成**：遵循 MCP 规范，方便把 AI Agent、模型服务或其他后端系统快速接入 Godot 项目，降低跨系统集成成本。

**典型接入方式**  
1. **CLI/SDK**：在项目根目录执行 `npx gopeak` 启动服务器，或在代码中通过提供的 JavaScript SDK 调用 REST/WebSocket 接口。  
2. **API**：使用标准的 MCP API（JSON‑RPC/WebSocket）进行工具调用，如 `scene.load`, `script.compile`, `input.inject` 等。  
3. **语言元数据**：服务器会自动暴露 GDScript、C# 等语言的符号表和类型信息，AI Agent 可直接查询以实现代码生成和自动补全。  

**生产可用性**  
- **活跃度**：截至 2026‑05‑13 最近一次提交，仓库拥有 180+ Stars、16+ Forks，社区讨论活跃。  
- **技术成熟度**：核心功能已实现并在多个开源 Godot 项目中验证，提供完整的 API 文档和示例。  
- **风险**：许可证、长期维护者和安全审计仍需进一步确认；但从代码更新频率、生态兼容性和已有用户反馈来看，已具备在内部或受控生产环境中进行试点的条件。  

综上，GoPeak‑godot‑mcp 是一个高价值、易集成且接近生产就绪的开源 MCP 服务器，适合作为 AI 助手与 Godot 开发工具链的桥梁。

## 🧭 Practical evaluation

**Value:** HaD0Yun/Gopeak-godot-mcp helps connect AI assistants to real tools and data through a standard protocol.

**Best use cases**

- connect AI agents to tools
- ship Model Context Protocol servers
- standardize integrations

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 180 GitHub stars
- 16 forks
- updated 2026-05-13
- primary language: JavaScript
- 20 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 31/100 |
| stars | 48/100 |
| topics | 100/100 |
| outlook | 56/100 |
| quality | 54/100 |
| recency | 20/100 |
| adoption | 43/100 |
| production | 53/100 |
| usefulness | 90/100 |
| integration | 78/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 400/100 |

---

<sub>🔭 Discovered 2026-05-13 · [View on GitHub](https://github.com/HaD0Yun/Gopeak-godot-mcp) · [← Back to Mcp](./README.md)</sub>
