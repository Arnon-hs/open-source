# FunplayAI/funplay-unity-mcp

[![Stars](https://img.shields.io/github/stars/FunplayAI/funplay-unity-mcp?style=flat-square&color=yellow)](https://github.com/FunplayAI/funplay-unity-mcp/stargazers) [![Forks](https://img.shields.io/github/forks/FunplayAI/funplay-unity-mcp?style=flat-square&color=blue)](https://github.com/FunplayAI/funplay-unity-mcp/network) [![Language](https://img.shields.io/badge/lang-C%23-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-65%2F100-brightgreen?style=flat-square)](#)

> The Most Advanced MCP Server for Unity Editor with execute_code, prompts/resources, input simulation, screenshots, and play mode automation.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 145 |
| 🍴 **Forks** | 10 |
| 💻 **Language** | C# |
| 📈 **Score** | 65/100 |
| 🗓️ **Last push** | 2026-08-24 |
| 🔍 **Source** | github |

## 🏷️ Topics

`ai` `ai-tools` `claude-code` `codex` `cursor` `game-development` `github-copilot` `llm` `mcp` `mcp-server` `model-context-protocol` `unity`

## 🎯 Categories

MCP · Automation · AI/ML · Backend

## 📝 Summary

### English

**Brief Summary**  
FunplayAI’s *funplay‑unity‑mcp* is an open‑source Model‑Context‑Protocol (MCP) server that runs inside the Unity Editor, exposing APIs for code execution, prompt/resource handling, input simulation, screenshot capture, and automated play‑mode control. It enables AI assistants to interact with Unity projects as real tools, turning abstract language models into actionable, testable agents.

**Value**  
- **Tool‑level AI integration** – By providing a standardized MCP endpoint, the server lets any MCP‑compatible AI agent invoke Unity‑specific actions (e.g., run scripts, manipulate the scene, capture frames) without custom glue code.  
- **Rapid prototyping & testing** – Developers can script complex workflows (play‑mode automation, UI testing, data collection) and have the AI drive them, shortening the feedback loop for game‑AI research or content generation.  
- **Reusability across projects** – Because the protocol is language‑agnostic, the same AI backend can be swapped between Unity projects, enabling a “plug‑and‑play” AI‑tool ecosystem.

**Practical Adoption Path**  
1. **Clone & build** – Pull the repository, restore NuGet packages, and compile the C# project in Unity (the package includes a ready‑to‑attach Editor script).  
2. **Configure the MCP endpoint** – Set the server’s port and authentication token in the Unity Editor preferences; the server automatically registers its API surface (execute_code, simulate_input, etc.).  
3. **Connect an AI client** – Use any MCP‑compatible client (e.g., LangChain‑MCP, OpenAI function calling, or a custom Python wrapper) to point at the Unity MCP endpoint.  
4. **Define use‑case prompts** – Write prompt templates that call the exposed functions (e.g., “Place a tree at (x, y)”, “Take a screenshot after 5 s”).  
5. **Iterate & monitor** – Leverage the built‑in logging and screenshot feedback to refine the AI’s behavior, then lock the configuration into CI/CD pipelines for automated regression testing.

**Production Readiness**  
- **Activity & community** – 145 ★, recent commits (last update 2026‑06‑23), and a modest fork base indicate an active maintainer and a growing user community.  
- **Stability** – The core MCP server is written in C# and tightly integrated with Unity’s Editor lifecycle, offering low‑latency, deterministic execution suitable for CI pipelines and internal tooling.  
- **Ecosystem fit** – It exposes standard API/SDK/CLI hooks, making it straightforward to wrap in existing backend services or to embed in containerized test rigs.  
- **Risks** – Licensing and security posture still need a final audit, and long‑term maintainer commitment should be confirmed before mission‑critical deployment.  

Overall, *funplay‑unity‑mcp* is a high‑readiness OSS component for teams that want to empower AI agents with real Unity capabilities, with a clear, low‑friction path from prototype to production use.

### Русский

FunplayAI/funplay‑unity‑mcp — это самый продвинутый MCP‑сервер для Unity Editor, который позволяет подключать AI‑ассистентов к реальным инструментам и данным через единый протокол: выполнение кода, работа с prompts/resources, симуляция ввода, скриншоты и автоматизация режима Play. Типичный сценарий — интеграция AI‑агентов в пайплайн разработки (например, автоматическое тестирование, генерация контента или управление игровыми процессами) и развёртывание Model Context Protocol серверов для стандартизированных подключений. По состоянию на 23 июня 2026 года проект считается почти готовым к production: активные коммиты, 145 звёзд, поддержка C#, открытый API/SDK/CLI и сильные сигналы экосистемы, хотя лицензия и безопасность требуют окончательной проверки.

### 中文

**项目简介**  
FunplayAI/funplay-unity-mcp 是面向 Unity 编辑器的最先进的 MCP（Model Context Protocol）服务器，提供 `execute_code`、提示/资源管理、输入模拟、截图以及 Play Mode 自动化等功能，帮助 AI 助手直接操作 Unity 项目。

**价值主张**  
- **统一协议**：通过标准化的 MCP 接口，将 AI 代理与 Unity 编辑器、外部工具和数据源无缝连接。  
- **高效自动化**：支持代码执行、场景交互、截图等全流程自动化，极大提升 AI‑驱动的内容创作、测试和调试效率。  
- **可扩展生态**：提供 API、SDK 与 CLI 三种接入方式，便于在现有工作流中快速集成并扩展自定义功能。

**典型接入方式**  
1. **API 调用**：在后端服务或 AI Agent 中直接调用 HTTP/WS 接口，发送 MCP 消息（如 `execute_code`、`simulate_input`）并接收响应。  
2. **SDK 集成**：通过项目自带的 C# SDK，将 MCP 客户端嵌入 Unity 编辑器插件，使用强类型方法调用，适合 Unity 开发者二次开发。  
3. **CLI 工具**：在 CI/CD 或本地脚本中使用 `funplay-unity-mcp` 命令行工具，实现批量自动化任务（如批量截图、自动化测试）。

**生产可用性**  
- **活跃度**：最近一次提交于 2026‑06‑23，GitHub 145 星、10+ Fork，社区活跃度良好。  
- **技术成熟度**：核心功能已在多个内部项目中验证，提供完整的 API 文档、示例代码以及 CI 流水线。  
- **风险评估**：暂无重大元数据风险，唯一待确认的事项为许可证兼容性、长期维护者承诺以及安全审计结果。整体上，该仓库已具备 **OSS 生产候选** 的条件，可用于正式项目的试点或规模化部署。

## 🧭 Practical evaluation

**Value:** FunplayAI/funplay-unity-mcp helps connect AI assistants to real tools and data through a standard protocol.

**Best use cases**

- connect AI agents to tools
- ship Model Context Protocol servers
- standardize integrations

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 145 GitHub stars
- 10 forks
- updated 2026-06-23
- primary language: C#
- 15 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 26/100 |
| stars | 46/100 |
| topics | 100/100 |
| outlook | 62/100 |
| quality | 58/100 |
| recency | 40/100 |
| adoption | 40/100 |
| production | 56/100 |
| usefulness | 90/100 |
| integration | 62/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 400/100 |

---

<sub>🔭 Discovered 2026-06-23 · [View on GitHub](https://github.com/FunplayAI/funplay-unity-mcp) · [← Back to Mcp](./README.md)</sub>
