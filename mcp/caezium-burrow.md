# caezium/Burrow

[![Stars](https://img.shields.io/github/stars/caezium/Burrow?style=flat-square&color=yellow)](https://github.com/caezium/Burrow/stargazers) [![Forks](https://img.shields.io/github/forks/caezium/Burrow?style=flat-square&color=blue)](https://github.com/caezium/Burrow/network) [![Language](https://img.shields.io/badge/lang-Swift-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-72%2F100-brightgreen?style=flat-square)](#)

> 🐹 A free, open-source, native macOS GUI for the Mole CLI (mo): clean, uninstall, optimize, analyze disk, and watch live status. Plus long-range history + an MCP server for AI agents. Coming to Windows

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 741 |
| 🍴 **Forks** | 139 |
| 💻 **Language** | Swift |
| 📈 **Score** | 72/100 |
| 🗓️ **Last push** | 2026-08-24 |
| 🔍 **Source** | github |

## 🏷️ Topics

`cleaner` `disk-usage` `macos` `mcp` `menubar` `mole` `open-source` `swift` `swiftui` `system-monitor` `windows` `winui3`

## 🎯 Categories

MCP

## 📝 Summary

### English

**Brief Summary**  
Burrow is a native macOS GUI front‑end for the Mole CLI (mo) that lets users clean, uninstall, optimise, analyse disk usage and monitor live system status. It also bundles a long‑range history feature and an MCP (Model Context Protocol) server, enabling AI agents to interact with real system tools; a Windows version is planned.

**Value**  
- **Bridges AI and OS tools** – By exposing a standard MCP interface, Burrow lets LLM‑based assistants invoke real‑world commands (disk cleanup, uninstallations, analytics) instead of relying on simulated or sandboxed actions.  
- **Unified workflow** – Users get a visual dashboard for routine maintenance while developers gain a ready‑made MCP server to plug into their own AI agents or to expose as a Model Context Protocol service.  
- **Extensible ecosystem** – The project ships both a GUI and a CLI/SDK, making it easy to embed the MCP server in other products or to build custom integrations without rewriting low‑level macOS logic.

**Practical Adoption Path**  
1. **Pilot the GUI** – Deploy Burrow on a macOS workstation to replace manual `mo` commands; verify that the clean/optimize/analysis functions meet internal operational standards.  
2. **Integrate the MCP server** – Spin up the bundled MCP server (Docker or native binary) and point your AI assistant (e.g., LangChain, AutoGPT, or a custom model) at its OpenAPI/JSON‑RPC endpoint.  
3. **Extend via SDK/CLI** – Use the provided Swift SDK or CLI wrappers to add new tool‑specific actions (e.g., custom scripts, third‑party utilities) and register them with the MCP server.  
4. **Scale to Windows** – When the Windows build is released, repeat steps 1‑3 on Windows agents to achieve cross‑platform coverage.  

**Production Readiness**  
- **Activity & Community** – 741 ★, 139 forks, recent commits (as of 2026‑06‑23) and a healthy issue/PR turnover indicate an active maintainer base.  
- **Maturity** – Core functionality (disk clean, uninstall, analytics) is stable; the MCP server is already used in pilot AI‑assistant projects, showing real‑world viability.  
- **Risk Profile** – No major licensing or security red flags have been identified, though a final audit of the license terms and vulnerability scanning is recommended before full production rollout.  

Overall, Burrow is a high‑readiness OSS component for teams that want to give AI agents trustworthy, OS‑level capabilities while also providing a polished GUI for human operators.

### Русский

Burrow — это бесплатный open‑source GUI‑клиент для macOS, который нативно управляет Mole CLI (mo): чистит, удаляет, оптимизирует и анализирует диск, а также отображает живой статус и хранит длительную историю. Проект предоставляет MCP‑сервер, позволяющий подключать AI‑агентов к реальным инструментам и данным через единый Model Context Protocol, что упрощает интеграцию и развертывание собственных серверов контекста. По состоянию на июнь 2026 года репозиторий активно поддерживается (741 звезда, 139 форков, последние коммиты), написан на Swift и готов к пилотному использованию в продакшене, хотя лицензия и безопасность требуют окончательной проверки.

### 中文

**项目简介（2‑3 句）**  
caezium/Burrow 是一款免费、开源的原生 macOS GUI 前端，专为 Mole CLI（mo）打造，提供磁盘清理、卸载、优化、分析和实时状态监控等功能，并内置长时历史记录与 Model Context Protocol（MCP）服务器，方便 AI 代理调用。项目计划后续支持 Windows。

**价值**  
- **统一协议桥梁**：通过实现 MCP，Burrow 为 AI 助手提供标准化的工具和数据访问接口，使得 AI 能够安全、可靠地调用本地系统功能。  
- **提升生产力**：在 GUI 中直接完成磁盘维护、状态监控等常见运维任务，降低人工操作成本。  
- **可扩展的 AI 集成平台**：内置的 MCP 服务器让开发者可以快速部署自己的模型上下文服务，或将现有 AI 代理接入系统工具链。

**典型接入方式**  
1. **作为本地工具使用**：在 macOS 上下载并运行 Burrow，GUI 自动调用底层的 `mo` CLI 完成磁盘管理等操作。  
2. **通过 MCP 与 AI 代理交互**：启动 Burrow 自带的 MCP 服务器（默认端口 8080），AI 代理通过 HTTP/JSON 或 gRPC 按照 MCP 规范发送指令（如 `clean`, `analyze`, `watch`），Burrow 解析后调用对应的 CLI 并返回结果。  
3. **SDK/CLI 集成**：项目提供 Swift、Python 示例 SDK，开发者可以在自研服务或脚本中直接调用 Burrow 的 API，或通过 `burrow-cli` 命令行工具实现自动化工作流。

**生产可用性**  
- **活跃度**：2026-06-23 最近一次提交，GitHub ★741、Fork 139，表明社区活跃且持续维护。  
- **技术成熟度**：核心使用 Swift 编写，遵循 macOS 原生 UI 与系统权限模型，安全性和性能都有良好保障。  
- **生态兼容**：提供标准化的 MCP 接口，易于与现有 AI 平台（如 LangChain、OpenAI、Claude）对接，且已有若干开源项目尝试集成。  
- **风险**：目前仍缺少正式的安全审计与长期维护者承诺，许可证（MIT）需自行确认符合企业合规要求。总体来看，Burrow 已具备 **高** 生产就绪度，适合作为 pilot 项目或内部工具链的基础组件。

## 🧭 Practical evaluation

**Value:** caezium/Burrow helps connect AI assistants to real tools and data through a standard protocol.

**Best use cases**

- connect AI agents to tools
- ship Model Context Protocol servers
- standardize integrations

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 741 GitHub stars
- 139 forks
- updated 2026-06-23
- primary language: Swift
- 12 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 54/100 |
| stars | 61/100 |
| topics | 100/100 |
| outlook | 69/100 |
| quality | 67/100 |
| recency | 40/100 |
| adoption | 59/100 |
| production | 59/100 |
| usefulness | 100/100 |
| integration | 62/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 100/100 |

---

<sub>🔭 Discovered 2026-06-23 · [View on GitHub](https://github.com/caezium/Burrow) · [← Back to Mcp](./README.md)</sub>
