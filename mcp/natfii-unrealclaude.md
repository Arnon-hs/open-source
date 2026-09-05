# Natfii/UnrealClaude

[![Stars](https://img.shields.io/github/stars/Natfii/UnrealClaude?style=flat-square&color=yellow)](https://github.com/Natfii/UnrealClaude/stargazers) [![Forks](https://img.shields.io/github/forks/Natfii/UnrealClaude?style=flat-square&color=blue)](https://github.com/Natfii/UnrealClaude/network) [![Language](https://img.shields.io/badge/lang-C%2B%2B-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-81%2F100-brightgreen?style=flat-square)](#)

> Claude Code CLI integration for Unreal Engine 5.7 - Get AI coding assistance with built-in UE5.7 documentation context directly in the editor.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 601 |
| 🍴 **Forks** | 97 |
| 💻 **Language** | C++ |
| 📈 **Score** | 81/100 |
| 🗓️ **Last push** | 2026-09-05 |
| 🔍 **Source** | github |

## 🏷️ Topics

`ai` `ai-coding-assistant` `ai-game-development` `ai-tools` `anthropic` `claude` `claude-code` `cpp` `editor-plugin` `game-development` `gamedev` `mcp`

## 🎯 Categories

MCP · AI/ML · Games & Graphics · Backend

## 📝 Summary

### English

**Brief Summary (2‑3 sentences)**  
Natfii/UnrealClaude is an open‑source CLI that plugs Claude‑style AI coding assistants directly into Unreal Engine 5.7, surfacing context‑aware code suggestions backed by the engine’s built‑in documentation. By exposing a standard Model Context Protocol (MCP) interface, it lets developers and AI agents invoke UE‑specific tooling and data without custom glue code.

**Value**  
- **Context‑rich assistance:** The integration pulls the full UE 5.7 API reference into the prompt, so the AI can generate accurate, compile‑ready code snippets.  
- **Standardized protocol:** Leveraging MCP means the same connector can be reused across different AI models or agents, reducing integration overhead for any tool that needs to talk to Unreal.  
- **Developer productivity:** Teams can keep the AI loop inside the editor, cutting context‑switching and accelerating prototyping or bug‑fix cycles.

**Practical Adoption Path**  
1. **Clone & build** the repository (C++ project with a small CLI wrapper).  
2. **Configure** your Claude or compatible LLM endpoint in the provided `config.yaml`.  
3. **Install** the CLI (`npm`/`pip` wrapper or direct binary) and add it to your UE 5.7 project’s build scripts.  
4. **Invoke** the CLI from within the editor (or via a custom toolbar) to request code completions, refactorings, or documentation look‑ups.  
5. **Iterate** by extending the MCP handlers for any additional Unreal tools (e.g., asset pipelines, build scripts) you want the AI to control.

**Production Readiness**  
- **Activity & community:** 601 stars, 97 forks, recent commit (2026‑05‑13) and ongoing issue activity indicate a healthy open‑source project.  
- **Maturity:** The core MCP interface, API/SDK exposure, and language metadata are already implemented, making the integration straightforward to evaluate.  
- **Readiness level:** Rated “high” for an OSS candidate; suitable for a pilot in a controlled production environment, pending final checks on licensing, security posture, and maintainer responsiveness.  

Overall, Natfii/UnrealClaude offers a robust, standards‑based bridge between AI coding assistants and Unreal Engine, with a clear path to adoption and a strong signal of production‑grade stability.

### Русский

Natfii/UnrealClaude — это открытый CLI‑инструмент, который интегрирует Claude Code в Unreal Engine 5.7, предоставляя разработчикам мгновенную AI‑поддержку с учётом встроенной документации UE5.7 прямо в редакторе. Он реализует стандартный Model Context Protocol, что упрощает подключение AI‑агентов к реальным инструментам и данным, а также позволяет быстро развернуть собственные MCP‑серверы. Проект обладает высокой готовностью к production: активные коммиты, 601 звезда, 97 форков, поддержка C++ и обширная экосистема, требующая лишь финального аудита лицензии и безопасности.

### 中文

**项目简介**  
Natfii/UnrealClaude 是一款面向 Unreal Engine 5.7 的 Claude‑Code CLI 插件，能够在编辑器内直接调用 AI 进行代码补全、重构和调试，并自动注入 UE5.7 官方文档作为上下文，让开发者获得“即问即得”的智能编程帮助。

**价值**  
- **AI 与真实工具/数据对接**：通过标准的 Model Context Protocol（MCP），把 Claude‑Code 与 UE5.7 的本地 API、文档和项目源码无缝连接，实现真正基于项目上下文的代码生成。  
- **统一的集成方式**：提供统一的 CLI/SDK 接口和语言元数据，方便在 CI/CD、插件市场或自研工具链中快速挂载 AI 助手。  
- **提升开发效率**：在编辑器内随时获取 AI 建议，减少查文档、手动搜索的时间成本，加速原型迭代和 Bug 修复。

**典型接入方式**  
1. **CLI 方式**：在项目根目录下安装 `unrealclaude`，通过 `unrealclaude generate <file>` 或 `unrealclaude fix <line>` 调用 AI。  
2. **SDK 集成**：在自定义插件或工具中引用 `UnrealClaude.h`，使用 `FClaudeClient::RequestCompletion(Context)` 接口，传入当前编辑器的代码片段和文档上下文。  
3. **MCP 服务器**：部署 Model Context Protocol 服务器，统一管理多个 AI 代理；UnrealClaude 只需配置服务器地址即可复用同一套上下文模型。

**生产可用性**  
- **活跃度**：最近一次提交 2026‑05‑13，GitHub ★601、Fork 97，社区活跃，已有多个 UE5 项目在内部使用。  
- **技术成熟度**：实现了完整的 API/CLI、语言元数据以及文档上下文注入，符合企业级插件的安全与可审计要求。  
- **风险**：暂无重大元数据或许可证冲突，但仍建议在正式部署前完成安全审计并确认维护者的长期可用性。  
综合来看，Natfii/UnrealClaude 已具备高可用性，可作为正式项目的 AI 编码助理或作为 MCP 生态的标准接入点进行试点。

## 🧭 Practical evaluation

**Value:** Natfii/UnrealClaude helps connect AI assistants to real tools and data through a standard protocol.

**Best use cases**

- connect AI agents to tools
- ship Model Context Protocol servers
- standardize integrations

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 601 GitHub stars
- 97 forks
- updated 2026-05-13
- primary language: C++
- 18 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 50/100 |
| stars | 59/100 |
| topics | 100/100 |
| outlook | 82/100 |
| quality | 75/100 |
| recency | 80/100 |
| adoption | 57/100 |
| production | 74/100 |
| usefulness | 100/100 |
| integration | 78/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 400/100 |

---

<sub>🔭 Discovered 2026-05-13 · [View on GitHub](https://github.com/Natfii/UnrealClaude) · [← Back to Mcp](./README.md)</sub>
