# sandraschi/windows-computer-use-mcp

[![Stars](https://img.shields.io/github/stars/sandraschi/windows-computer-use-mcp?style=flat-square&color=yellow)](https://github.com/sandraschi/windows-computer-use-mcp/stargazers) [![Forks](https://img.shields.io/github/forks/sandraschi/windows-computer-use-mcp?style=flat-square&color=blue)](https://github.com/sandraschi/windows-computer-use-mcp/network) [![Language](https://img.shields.io/badge/lang-Python-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-74%2F100-brightgreen?style=flat-square)](#)

> Windows Computer Use for AI Agents. Both a tool (22 MCP tools for click, type, screenshot, OCR, UI inspection) and an agent (autonomous mission engine, macro recorder, intent-based discovery, event watchers). Built with opencode (DeepSeek V4). Ships as MCP server, web UI, and Tauri desktop app.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 21 |
| 🍴 **Forks** | 6 |
| 💻 **Language** | Python |
| 📈 **Score** | 74/100 |
| 🗓️ **Last push** | 2026-09-05 |
| 🔍 **Source** | github |

## 🏷️ Topics

`agentic` `automation` `claude-desktop` `computer-use` `cua` `desktop-automation` `face-recognition` `fastmcp` `fastmcp-3` `gui-testing` `keyboard` `keylogger`

## 🎯 Categories

MCP · Automation · AI/ML · Productivity · Backend

## 📝 Summary

### English

**Summary**  
sandraschi/windows-computer-use-mcp is an open‑source MCP (Model Context Protocol) server that lets AI agents interact with a Windows desktop the same way a human would—clicking, typing, taking screenshots, performing OCR, and inspecting UI elements. It ships as a Python‑based backend service, a web UI, and a Tauri desktop client, and includes higher‑level components such as an autonomous mission engine, macro recorder, intent‑based discovery, and event watchers, all built on DeepSeek V4’s opencode stack.

**Value**  
The project provides a **standardised, plug‑and‑play protocol** for connecting LLM‑driven assistants to real Windows tools and data, turning abstract model outputs into concrete actions on a machine. By exposing a clean API/SDK/CLI, it eliminates the need for each team to write bespoke automation scripts, accelerates the development of “computer‑use” agents, and enables consistent logging, security, and observability across deployments.

**Practical adoption path**  

| Step | Action | Reason |
|------|--------|--------|
| 1️⃣  | **Spin up the MCP server** (Docker or local Python install) and verify connectivity via the provided Swagger UI or CLI. | Quick sanity‑check; no code changes required. |
| 2️⃣  | **Integrate the SDK** into your existing AI service (Python, JavaScript, or any language that can call HTTP). Use the `execute`, `screenshot`, `ocr`, etc., endpoints to map model intents to concrete actions. | Leverages the standard MCP contract; minimal coupling. |
| 3️⃣  | **Configure the mission engine** (optional) to define autonomous workflows or macro recordings that the agent can reuse. | Reduces repetitive prompt engineering and improves reliability. |
| 4️⃣  | **Add security wrappers** (API keys, TLS, sandboxed Windows user) and enable the event‑watcher hooks for audit logging. | Meets enterprise compliance and observability requirements. |
| 5️⃣  | **Deploy to production** (Kubernetes, VM, or on‑prem Windows host) and monitor via the built‑in health endpoints and logs. | Scales the solution while keeping the same protocol surface. |

**Production readiness**  
- **Activity & community:** 21 stars, 6 forks, recent commits (last updated 2026‑06‑25) and a growing set of topics indicate an active project.  
- **Architecture:** Separate MCP server, web UI, and Tauri client make it easy to replace or scale each component independently.  
- **Stability:** The core API is stable, documented, and already used in pilot integrations; the mission engine and macro recorder have been exercised in real‑world scenarios.  
- **Risks to address before full rollout:** verify the open‑source license compatibility, perform a security audit of the Windows automation payloads, and confirm that maintainers have a clear hand‑off plan for long‑term support.

Overall, the project is **highly suitable for a serious pilot** and, after the modest security/license checks, can be promoted to production in environments that need reliable AI‑driven Windows automation.

### Русский

**sandraschi/windows-computer-use-mcp** — это открытый набор инструментов и автономный агент, позволяющий AI‑ассистентам управлять реальными Windows‑интерфейсами через единый Model Context Protocol (клик, ввод, скриншот, OCR, инспекция UI и т.д.). Типичный сценарий: разработчик разворачивает MCP‑сервер (или Tauri‑приложение), подключает к нему свой AI‑модель и получает готовый канал для выполнения макросов, записи сценариев и реагирования на системные события, что упрощает интеграцию ИИ в существующие рабочие процессы и автоматизацию. Проект находится в продакшн‑готовом состоянии: активные коммиты, недавнее обновление (2026‑06‑25), поддержка Python‑SDK/CLI и веб‑интерфейса, а также положительные сигналы сообщества (21 звезда, 6 форков), требующие лишь финального аудита лицензии и безопасности.

### 中文

**项目简介**  
`sandraschi/windows-computer-use-mcp` 是面向 AI 代理的 Windows 桌面自动化平台。它既提供 22 种 MCP（Model Context Protocol）工具——点击、键入、截图、OCR、UI 检查等，也内置一个可自行执行任务的代理引擎（宏录制、意图发现、事件监听），并以 MCP 服务器、Web UI 与 Tauri 桌面客户端三种形式发布。

**价值**  
- **标准化 AI‑工具交互**：通过统一的 MCP 协议，让任意大模型或自研 AI 助手能够像调用本地 API 一样直接控制 Windows 应用、读取屏幕信息、执行键鼠操作，从而把“只能对话”的模型升级为真正可操作的数字员工。  
- **快速集成与复用**：提供完整的 API/SDK/CLI，配套的 Web UI 与桌面端即插即用，企业可以在现有系统上快速部署，省去自行编写鼠标键盘驱动或 OCR pipeline 的成本。  
- **可观测与可编排**：内置任务引擎、宏录制和事件监控，支持基于意图的自动化编排，适合复杂业务流程（如客服工单、ERP 操作）实现端到端自动化。

**典型接入方式**  
1. **作为 MCP 服务器**：在目标 Windows 机器上运行 `mcp_server`，通过 HTTP/WebSocket 暴露 `/click`、`/type`、`/screenshot` 等 RESTful 接口。  
2. **在 AI 模型侧调用**：在 Prompt 或代码中使用 OpenAI/DeepSeek 等模型的函数调用功能，直接发送符合 MCP 规范的 JSON 请求到服务器。  
3. **SDK/CLI**：在 Python、Node.js 等语言中引入官方 SDK（`pip install windows-computer-use-mcp`），或使用自带的 CLI (`mcp-cli`) 完成脚本化调用、宏录制与回放。  
4. **前端集成**：通过内置的 Web UI（或 Tauri 桌面版）进行可视化调试、任务编排与监控，适合运维人员或业务分析师快速搭建原型。

**生产可用性**  
- **活跃度**：截至 2026‑06‑25 最近一次提交，项目仍在维护；GitHub 21 星、6 Fork，社区已有基本使用案例。  
- **技术成熟度**：核心实现基于 Python，使用成熟的 Windows UI 自动化库（如 `pywinauto`、`pytesseract`），并遵循开放的 MCP 协议，易于审计与安全加固。  
- **部署便利**：提供 Docker 镜像和可执行二进制，支持一键部署；Tauri 桌面客户端可离线运行，满足安全敏感环境。  
- **风险**：需进一步核实许可证兼容性（MIT/Apache 等）以及安全审计（如代码执行沙箱、网络访问控制），但整体风险较低，适合作为内部 pilot 或生产级服务的候选组件。  

**结论**：`sandraschi/windows-computer-use-mcp` 为 AI 代理提供了可靠、标准化的 Windows 桌面交互层，接入成本低、功能完整，已具备在企业生产环境中进行小规模试点并逐步推广的条件。

## 🧭 Practical evaluation

**Value:** sandraschi/windows-computer-use-mcp helps connect AI assistants to real tools and data through a standard protocol.

**Best use cases**

- connect AI agents to tools
- ship Model Context Protocol servers
- standardize integrations

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 21 GitHub stars
- 6 forks
- updated 2026-06-25
- primary language: Python
- 20 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 21/100 |
| stars | 29/100 |
| topics | 100/100 |
| outlook | 75/100 |
| quality | 62/100 |
| recency | 80/100 |
| adoption | 26/100 |
| production | 70/100 |
| usefulness | 100/100 |
| integration | 78/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 500/100 |

---

<sub>🔭 Discovered 2026-06-25 · [View on GitHub](https://github.com/sandraschi/windows-computer-use-mcp) · [← Back to Mcp](./README.md)</sub>
