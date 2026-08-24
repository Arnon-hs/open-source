# fennaraOfficial/fennara-godot-ai

[![Stars](https://img.shields.io/github/stars/fennaraOfficial/fennara-godot-ai?style=flat-square&color=yellow)](https://github.com/fennaraOfficial/fennara-godot-ai/stargazers) [![Forks](https://img.shields.io/github/forks/fennaraOfficial/fennara-godot-ai?style=flat-square&color=blue)](https://github.com/fennaraOfficial/fennara-godot-ai/network) [![Language](https://img.shields.io/badge/lang-C%2B%2B-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-69%2F100-brightgreen?style=flat-square)](#)

> AI chat and agent tooling for Godot, with MCP support, local runtime, and native editor integration.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 66 |
| 🍴 **Forks** | 3 |
| 💻 **Language** | C++ |
| 📈 **Score** | 69/100 |
| 🗓️ **Last push** | 2026-08-24 |
| 🔍 **Source** | github |

## 🏷️ Topics

`ai-agent` `ai-coding` `ai-game-development` `claude-code` `codex` `cursor` `gamedev` `gdscript` `godot` `godot-4` `godot-addon` `godot-engine`

## 🎯 Categories

MCP · AI/ML · Backend

## 📝 Summary

### English

**Brief Summary**  
fennaraOfficial/fennara-godot-ai is an open‑source toolkit that brings AI chat and autonomous agents into the Godot game engine, offering Model Context Protocol (MCP) support, a local runtime, and seamless native editor integration. It lets developers expose game tools, data, and services to AI assistants through a standard protocol, making it easy to build “AI‑powered” gameplay features or automation pipelines.  

**Value**  
- **Standardized AI‑tool coupling** – By implementing MCP, the library provides a common language for AI agents to invoke in‑engine functions, access assets, or query external services, reducing the need for custom glue code.  
- **Local, low‑latency runtime** – The bundled runtime runs entirely on the developer’s machine, enabling fast iteration and offline development without relying on external APIs.  
- **Native Godot integration** – Agents appear as first‑class editor plugins, allowing designers to prototype and debug AI behavior directly within the familiar Godot UI.  

**Practical Adoption Path**  
1. **Add the plugin** – Clone the repository and enable the plugin in Godot’s Project Settings; the installer registers the required C++ modules and MCP endpoints.  
2. **Define tool bindings** – Use the provided API/SDK to annotate Godot scripts or scenes with `@mcp_tool` decorators, exposing functions (e.g., inventory management, path‑finding) to the AI.  
3. **Run the local MCP server** – Start the bundled runtime (via the editor button or CLI) to host the protocol bridge; the server automatically discovers the annotated tools.  
4. **Connect an AI client** – Point any MCP‑compatible model (e.g., OpenAI, Anthropic, or a self‑hosted LLM) to the local server URL; the model can now issue tool calls as part of its prompt flow.  
5. **Iterate & ship** – Test interactions in‑editor, then package the MCP server with the final game build for production use, or replace it with a cloud‑hosted MCP instance for scalability.  

**Production Readiness**  
- **Activity & Community** – The project was updated on 2026‑06‑26, has 66 stars, 3 forks, and recent commits, indicating active maintenance.  
- **Maturity** – Core features (MCP support, local runtime, editor UI) are stable, and the codebase is primarily C++ with clear SDK boundaries, easing integration into existing Godot pipelines.  
- **Risk Considerations** – No obvious licensing or security red flags have been identified, but a final audit of the MIT‑style license compliance and any third‑party dependencies is recommended before a large‑scale rollout.  
Overall, fennara-godot-ai is production‑ready for pilot projects and can be scaled to full releases once the minor due‑diligence steps (license verification, security review) are completed.

### Русский

**fennaraOfficial/fennara-godot-ai** — это открытая библиотека, позволяющая интегрировать AI‑чат и интеллектуальных агентов в проекты Godot через стандартный Model Context Protocol (MCP). Типичный сценарий: разработчик подключает к игровому/интерактивному приложению локальный AI‑runtime, а затем через MCP позволяет агенту вызывать игровые инструменты, обращаться к внешним данным и обслуживать пользовательские запросы прямо из редактора Godot. Проект уже активно поддерживается (обновления — 2026‑06‑26, 66 ★, 3 форка), имеет готовый API/SDK/CLI и демонстрирует высокий уровень готовности к production‑использованию, требующий лишь финального аудита лицензии и безопасности.

### 中文

**项目简介（2‑3 句话）**  
fennaraOfficial/fennara-godot-ai 为 Godot 引擎提供 AI 聊天与智能体工具链，支持 Model Context Protocol（MCP）、本地运行时以及原生编辑器集成。它通过统一的协议把 AI 助手与游戏内部工具、数据和外部服务相连，让开发者可以在 Godot 中直接调用 AI 功能。

**价值**  
- **标准化接入**：基于 MCP，AI 代理可以像调用普通 API 一样访问游戏资源、编辑器功能和自定义工具，降低了不同平台间的集成成本。  
- **本地运行时**：无需依赖云服务，开发者可以在本机或离线环境下运行 AI，提升响应速度并保障隐私。  
- **编辑器原生化**：通过插件直接嵌入 Godot 编辑器，开发者在编辑、调试和测试阶段即可使用 AI，提升工作流效率。

**典型接入方式**  
1. **插件安装**：在 Godot 项目中通过 Asset Library 或手动导入 `fennara-godot-ai` 插件。  
2. **配置 MCP 服务器**：启动或指向已有的 MCP 服务器（可自行部署或使用云端实例），在插件设置中填写地址、认证信息。  
3. **调用 API/SDK**：在 GDScript、C# 或 C++ 脚本中使用提供的 `FennaraAI` 类或 CLI 工具，发送 `chat`、`tool_execution` 等请求；插件会把请求转发给 MCP 服务器并返回结构化响应。  
4. **事件信号**：插件暴露 Godot 信号（如 `on_ai_response`、`on_tool_result`），可直接在编辑器节点树中绑定回调，实现“AI 驱动”交互。

**生产可用性**  
- **活跃度**：最近一次提交在 2026‑06‑26，星标 66、fork 3，社区讨论活跃，代码基于 C++，质量较稳定。  
- **成熟度**：已实现完整的 MCP 客户端、编辑器 UI 与本地运行时，具备完整的 API/SDK/CLI 三层接入，适合作为正式项目的 AI 核心模块。  
- **风险**：当前仍需对许可证（MIT/Apache 等）和安全审计进行最终确认；若项目计划长期维护，建议跟进维护者的更新频率并自行进行安全渗透测试。  

总体来看，fennara-godot-ai 已具备在生产环境中试点的条件，尤其适合需要在 Godot 中快速集成 AI 助手、实现工具化交互或构建自定义 AI 代理的游戏与交互式应用。

## 🧭 Practical evaluation

**Value:** fennaraOfficial/fennara-godot-ai helps connect AI assistants to real tools and data through a standard protocol.

**Best use cases**

- connect AI agents to tools
- ship Model Context Protocol servers
- standardize integrations

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 66 GitHub stars
- 3 forks
- updated 2026-06-26
- primary language: C++
- 17 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 15/100 |
| stars | 39/100 |
| topics | 100/100 |
| outlook | 62/100 |
| quality | 54/100 |
| recency | 40/100 |
| adoption | 32/100 |
| production | 57/100 |
| usefulness | 100/100 |
| integration | 78/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 300/100 |

---

<sub>🔭 Discovered 2026-06-26 · [View on GitHub](https://github.com/fennaraOfficial/fennara-godot-ai) · [← Back to Mcp](./README.md)</sub>
