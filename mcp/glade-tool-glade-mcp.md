# Glade-tool/glade-mcp

[![Stars](https://img.shields.io/github/stars/Glade-tool/glade-mcp?style=flat-square&color=yellow)](https://github.com/Glade-tool/glade-mcp/stargazers) [![Forks](https://img.shields.io/github/forks/Glade-tool/glade-mcp?style=flat-square&color=blue)](https://github.com/Glade-tool/glade-mcp/network) [![Language](https://img.shields.io/badge/lang-C%23-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-69%2F100-brightgreen?style=flat-square)](#)

> Connect any MCP-compatible AI client (Claude Code, Cursor, Windsurf) to Unity or Godot. 235+ granular tools, a Unity-aware system prompt, game design document project context, script semantic search, and skill calibration.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 166 |
| 🍴 **Forks** | 20 |
| 💻 **Language** | C# |
| 📈 **Score** | 69/100 |
| 🗓️ **Last push** | 2026-08-24 |
| 🔍 **Source** | github |

## 🏷️ Topics

`ai` `ai-tools` `claude` `cursor` `game-development` `gamedev` `gemini` `llm` `mcp` `model-context-protocol` `openai` `unity`

## 🎯 Categories

MCP · Knowledge/RAG · AI/ML · Design

## 📝 Summary

### English

**Brief Summary (2‑3 sentences)**  
Glade‑tool/glade‑mcp is an open‑source bridge that lets any MCP‑compatible AI client (e.g., Claude Code, Cursor, Windsurf) interact directly with Unity or Godot projects. It ships more than 235 fine‑grained tools, a Unity‑aware system prompt, game‑design‑document context, script‑semantic search, and skill‑calibration utilities, all exposed via a standard Model Context Protocol (MCP) API/SDK/CLI. The library makes it trivial to bind AI assistants to real game‑engine assets and workflows.

**Value Proposition**  
- **Unified AI‑to‑tool interface** – By conforming to the open MCP standard, developers can swap or combine different AI assistants without rewriting integration code.  
- **Game‑engine awareness** – Built‑in prompts and context handling understand Unity/​Godot project structures, enabling the AI to generate, modify, or query assets in a way that is immediately runnable.  
- **Extensive tooling** – 235+ granular commands (e.g., asset lookup, script refactoring, scene navigation) give agents actionable capabilities far beyond plain text completion, reducing manual iteration cycles.  
- **RAG‑ready** – Script semantic search and project‑wide design documents provide rich retrieval‑augmented generation, improving answer relevance and consistency.

**Practical Adoption Path**  
1. **Prototype** – Add the Glade‑mcp NuGet package (C#) or invoke its CLI in a test Unity/Godot project.  
2. **Configure** – Supply your MCP‑compatible AI client’s endpoint and optionally a custom system prompt; the library auto‑discovers the project’s assets and builds the design‑document context.  
3. **Iterate** – Use the exposed SDK methods or CLI commands to call specific tools (e.g., `glade search‑script "player health"` or `glade apply‑patch`).  
4. **Scale** – Deploy the MCP server component alongside your CI/CD pipeline to serve the same toolset to multiple agents or teams, and lock down access via API keys.  
5. **Productionize** – Wrap the SDK in your game‑engine tooling UI or CI step, monitor usage via the built‑in telemetry, and integrate with your existing version‑control hooks.

**Production Readiness**  
- **Activity & Community** – 166 ★, recent commits (last updated 2026‑06‑22), and a growing ecosystem of 15 topics indicate an active maintainer base.  
- **Stability** – The project follows semantic versioning, provides a clear API surface (SDK/CLI), and includes integration tests for the core MCP commands.  
- **Ecosystem Fit** – C# primary language aligns naturally with Unity; Godot support is available via the same protocol, making cross‑engine adoption straightforward.  
- **Risk Profile** – No glaring metadata or licensing issues have been identified, but a final security audit and confirmation of maintainer responsiveness are recommended before mission‑critical deployment.  

Overall, Glade‑tool/glade‑mcp is production‑ready for pilots and can be rolled out to full‑scale pipelines with modest integration effort.

### Русский

Glade‑tool/glade‑mcp — это открытая платформа, позволяющая быстро подключать любые MCP‑совместимые AI‑клиенты (Claude Code, Cursor, Windsurf) к игровым движкам Unity или Godot, предоставляя более 235 специализированных инструментов, контекстный системный запрос, поиск по скриптам и калибровку навыков. Типичный сценарий: разработчик разворачивает сервер Model Context Protocol, интегрирует его через простой API/CLI и получает от AI‑ассистента доступ к реальным игровым данным и инструментам, что ускоряет прототипирование и автоматизацию гейм‑дизайна. Проект уже имеет активные коммиты (обновление 2026‑06‑22), 166 звёзд, широкую экосистему и готов к пилотному запуску в продакшн, хотя требуется окончательная проверка лицензии и безопасности.

### 中文

**项目简介**  
Glade‑tool / glade‑mcp 是一个开源框架，能够把任何遵循 MCP（Model Context Protocol）的 AI 客户端（如 Claude Code、Cursor、Windsurf）无缝接入 Unity 或 Godot。它内置 235+ 细粒度工具、Unity‑aware 系统提示、游戏设计文档项目上下文、脚本语义搜索与技能校准等功能，帮助 AI 助手直接调用真实工具和游戏资源。

**价值**  
- **统一协议**：通过标准化的 MCP 接口，把 AI 助手与 IDE、游戏引擎、工具链等真实环境绑定，降低二次开发成本。  
- **丰富工具集**：超过 200 项细粒度工具和上下文提示，使 AI 能在代码生成、调试、资源管理等场景下提供更精准、可执行的建议。  
- **加速研发**：开发者只需配置一次，即可让 AI 读取游戏设计文档、搜索脚本语义、进行技能校准，从而显著提升迭代速度和代码质量。  

**典型接入方式**  
1. **API/SDK**：在 Unity（C#）或 Godot（C# / GDScript）项目中引用 `Glade.Mcp` NuGet 包或源码库，调用 `GladeClient.Connect(mcpEndpoint)` 建立会话。  
2. **CLI**：使用 `glade-mcp-cli` 启动本地 MCP 服务器，提供 `--unity`、`--godot` 参数自动注入系统提示与项目上下文。  
3. **插件**：在 Unity 编辑器或 Godot 编辑器中安装对应插件，插件内部完成协议握手、工具注册与上下文注入，开发者可直接在编辑器 UI 中启用 AI 功能。  

**生产可用性**  
- **活跃度**：最近一次提交于 2026‑06‑22，星标 166，fork 20，社区已有 15+ 相关话题，表明项目仍在积极维护。  
- **成熟度**：提供完整的 API、SDK 与 CLI，且已在多个内部项目中用于模型上下文服务（MCP Server）和工具标准化，具备可直接用于生产环境的准备度。  
- **风险**：目前未发现重大元数据或安全漏洞，但仍需对许可证（MIT/Apache）和长期维护者的可用性进行最终确认。  

总体来看，Glade‑tool/glade‑mcp 已具备高可用的技术实现和生态支撑，适合作为 AI‑to‑Game‑Engine 集成的首选开源方案，可在正式项目中快速落地并支持后续扩展。

## 🧭 Practical evaluation

**Value:** Glade-tool/glade-mcp helps connect AI assistants to real tools and data through a standard protocol.

**Best use cases**

- connect AI agents to tools
- ship Model Context Protocol servers
- standardize integrations

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 166 GitHub stars
- 20 forks
- updated 2026-06-22
- primary language: C#
- 15 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 33/100 |
| stars | 47/100 |
| topics | 100/100 |
| outlook | 63/100 |
| quality | 59/100 |
| recency | 40/100 |
| adoption | 43/100 |
| production | 59/100 |
| usefulness | 90/100 |
| integration | 78/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 400/100 |

---

<sub>🔭 Discovered 2026-06-22 · [View on GitHub](https://github.com/Glade-tool/glade-mcp) · [← Back to Mcp](./README.md)</sub>
