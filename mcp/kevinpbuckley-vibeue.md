# kevinpbuckley/VibeUE

[![Stars](https://img.shields.io/github/stars/kevinpbuckley/VibeUE?style=flat-square&color=yellow)](https://github.com/kevinpbuckley/VibeUE/stargazers) [![Forks](https://img.shields.io/github/forks/kevinpbuckley/VibeUE?style=flat-square&color=blue)](https://github.com/kevinpbuckley/VibeUE/network) [![Language](https://img.shields.io/badge/lang-C%2B%2B-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-77%2F100-brightgreen?style=flat-square)](#)

> Unreal Engine Vibe Coding tool

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 350 |
| 🍴 **Forks** | 80 |
| 💻 **Language** | C++ |
| 📈 **Score** | 77/100 |
| 🗓️ **Last push** | 2026-09-05 |
| 🔍 **Source** | github |

## 🏷️ Topics

`ai` `ai-tools` `automation` `blueprint` `claude` `copilot` `cursor` `game-development` `gamedev` `landscape` `mcp` `mcp-server`

## 🎯 Categories

MCP · Automation · AI/ML · Games & Graphics · Backend

## 📝 Summary

### English

**Summary**  
kevinpbuckley/VibeUE is an open‑source Unreal Engine “Vibe Coding” toolkit that implements a standard protocol for linking AI assistants with real‑world tools and data. It enables developers to expose Unreal‑based functionality through API/SDK/CLI interfaces, making it easy to integrate AI agents, run Model Context Protocol servers, and standardize tool‑to‑AI communication.  

**Value**  
By providing a unified protocol layer, VibeUE removes the friction of building bespoke connectors for each Unreal Engine feature, allowing AI assistants to invoke engine tools, query assets, and trigger gameplay logic directly. This accelerates AI‑driven workflows such as automated level design, real‑time testing, and dynamic content generation, while keeping the integration codebase small and maintainable.  

**Practical adoption path**  
1. **Evaluate the SDK/API** – Clone the repo, build the C++ library, and run the provided CLI examples to verify connectivity with your Unreal project.  
2. **Integrate with your AI stack** – Register the VibeUE endpoints in your Model Context Protocol server or preferred AI orchestration layer, using the generated language bindings (C++/Python).  
3. **Pilot a use case** – Start with a low‑risk scenario (e.g., AI‑driven asset lookup or script execution) and iterate, adding more complex tool calls as confidence grows.  

**Production readiness**  
The project shows strong OSS maturity: 350 ★, 80 forks, recent commits (as of 2026‑06‑23), and active community interest across 20 topics. Its C++ core and clear API/CLI surface make integration straightforward, and the repository’s health indicators suggest it is ready for a serious pilot. Final due‑diligence should still confirm licensing compliance, security posture, and maintainer responsiveness, but overall VibeUE appears production‑ready for teams looking to embed AI agents into Unreal Engine pipelines.

### Русский

**kevinpbuckley/VibeUE** — это open‑source‑инструмент для Unreal Engine, который реализует единый протокол связи AI‑ассистентов с реальными инструментами и данными. Он позволяет быстро подключать AI‑агентов к игровым и серверным сервисам, разворачивать Model Context Protocol‑серверы и стандартизировать интеграцию через API/SDK/CLI. Проект демонстрирует высокий уровень готовности к продакшену: активные коммиты, 350 звёзд, 80 форков, поддержка C++ и 20 тематических меток, что делает его надёжным кандидатом для пилотного внедрения, хотя лицензия и безопасность требуют окончательной проверки.

### 中文

**项目简介**  
kevinpbuckley/VibeUE 是一个基于 Unreal Engine 的「Vibe Coding」工具，提供统一的协议（Model Context Protocol）让 AI 助手能够直接调用真实的 UE4/UE5 功能、插件和数据，实现「AI + 工具」的无缝协作。

**价值**  
- **标准化接入**：通过统一的协议层，AI 代理可以像调用本地函数一样使用 UE 的编辑、渲染、资产管理等能力，降低了每次集成的工作量。  
- **快速原型**：开发者只需在项目中引入 VibeUE，即可让 LLM/ChatGPT 等模型直接操控场景、生成蓝图或运行自定义脚本，加速 AI‑驱动的内容创作与自动化测试。  
- **生态兼容**：支持 API、SDK、CLI 三种接入方式，配套的语言元数据和主题标签帮助团队快速定位所需功能，适配现有 CI/CD 与后台服务。

**典型接入方式**  
1. **API 接口**：在 UE 项目中启动 VibeUE 服务器，AI 通过 HTTP/JSON‑RPC 调用 `CreateActor、SetMaterial、RunBlueprint` 等端点。  
2. **SDK（C++/Python）**：在自定义插件或外部脚本中链接 VibeUE 提供的库，直接使用 C++ 类或 Python 包进行函数调用，适合高频交互或实时控制。  
3. **CLI 工具**：通过命令行执行 `vibeue-cli`，可在构建流水线或自动化测试中触发批量操作，如批量导入资产、执行渲染任务等。

**生产可用性**  
- **活跃度高**：截至 2026‑06‑23 最近一次提交，GitHub 获得 350+ stars、80+ forks，社区讨论活跃。  
- **成熟度**：项目已实现完整的 Model Context Protocol 服务器，提供完整的 API 文档与示例，适合作为正式项目的后端服务。  
- **风险评估**：暂无重大元数据风险，唯一待确认的是许可证兼容性、长期安全维护计划以及核心维护者的持续投入。总体上，VibeUE 已具备 OSS 候选者的高可用性，适合在生产环境中进行试点或全量部署。

## 🧭 Practical evaluation

**Value:** kevinpbuckley/VibeUE helps connect AI assistants to real tools and data through a standard protocol.

**Best use cases**

- connect AI agents to tools
- ship Model Context Protocol servers
- standardize integrations

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 350 GitHub stars
- 80 forks
- updated 2026-06-23
- primary language: C++
- 20 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 48/100 |
| stars | 54/100 |
| topics | 100/100 |
| outlook | 79/100 |
| quality | 74/100 |
| recency | 80/100 |
| adoption | 52/100 |
| production | 74/100 |
| usefulness | 90/100 |
| integration | 78/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 500/100 |

---

<sub>🔭 Discovered 2026-06-23 · [View on GitHub](https://github.com/kevinpbuckley/VibeUE) · [← Back to Mcp](./README.md)</sub>
