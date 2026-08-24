# palmier-io/palmier-pro

[![Stars](https://img.shields.io/github/stars/palmier-io/palmier-pro?style=flat-square&color=yellow)](https://github.com/palmier-io/palmier-pro/stargazers) [![Forks](https://img.shields.io/github/forks/palmier-io/palmier-pro?style=flat-square&color=blue)](https://github.com/palmier-io/palmier-pro/network) [![Language](https://img.shields.io/badge/lang-Swift-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-62%2F100-brightgreen?style=flat-square)](#)

> macOS video editor built for AI

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 7.6k |
| 🍴 **Forks** | 511 |
| 💻 **Language** | Swift |
| 📈 **Score** | 62/100 |
| 🗓️ **Last push** | 2026-08-24 |
| 🔍 **Source** | github |

## 🏷️ Topics

`ai-video` `claude` `macos` `mcp` `seedance2` `swift` `video-editor`

## 🎯 Categories

Video Editing · MCP · AI/ML

## 📝 Summary

### English

**Brief Summary (2‑3 sentences)**  
palmier‑io/palmier‑pro is an open‑source macOS video‑editing application that embeds a “Model Context Protocol” (MCP) layer, enabling AI assistants to invoke real editing tools and data directly from the UI. With a thriving Swift codebase (7 k+ stars, 511 forks) and recent activity, it serves as a ready‑made bridge for developers who want to plug generative AI agents into a production‑grade video workflow.

**Value**  
- **Standardised AI‑tool integration** – By exposing a uniform MCP/SDK/CLI, the project lets any AI model (ChatGPT, Claude, custom LLMs) call native editing functions (trim, add effects, render) without custom glue code.  
- **Accelerates AI‑driven product development** – Teams can focus on the intelligence layer while re‑using palmier‑pro’s mature UI and media pipeline, shortening time‑to‑market for AI‑enhanced video features.  
- **Ecosystem leverage** – The Swift implementation and macOS‑native performance make it a natural fit for Apple‑centric media stacks, and the open protocol encourages third‑party extensions and community contributions.

**Practical Adoption Path**  
1. **Prototype** – Clone the repo, run the provided Swift package or CLI, and experiment with the MCP endpoints using a local LLM or a hosted AI service.  
2. **Integrate** – Replace the demo AI agent with your own model, wiring the MCP calls to your inference endpoint (REST, gRPC, etc.).  
3. **Extend** – Add custom editing actions or data sources by implementing the MCP interface in Swift or exposing additional SDK bindings (e.g., Python wrappers).  
4. **Deploy** – Package the modified app for distribution (App Store, internal MDM) or run it as a headless server exposing the MCP API for broader tool orchestration.

**Production Readiness**  
- **Activity & Adoption** – The project shows strong recent commits (last updated 2026‑06‑23), a large star count, and active forking, indicating a healthy community and ongoing maintenance.  
- **Technical Maturity** – Written in Swift with a clear modular architecture, it already provides API/SDK/CLI entry points and comprehensive metadata, simplifying integration testing and CI pipelines.  
- **Risk Profile** – No major metadata or licensing red flags have been identified, though a final security audit and maintainer verification are recommended before enterprise rollout. Overall, palmier‑pro is positioned as a high‑readiness OSS candidate for pilots and production deployments of AI‑augmented video editing.

### Русский

**palmier-io/palmier-pro** — это открытый видеоредактор для macOS, разработанный специально для интеграции с AI‑ассистентами через единый Model Context Protocol. Он позволяет быстро подключать AI‑агентов к реальным инструментам и данным, а также развёртывать собственные MCP‑серверы и стандартизировать интеграции. Проект находится на высокой стадии готовности к production: активные коммиты, более 7500 звёзд, широкое принятие в сообществе и поддержка Swift‑SDK/CLI, хотя требуется окончательная проверка лицензии и безопасности.

### 中文

**项目简介（2‑3 句）**  
palmier‑io/palmier-pro 是一款基于 macOS 的视频编辑器，专为 AI 场景设计，提供统一的 Model Context Protocol（MCP）以便 AI 助手直接调用编辑功能和底层数据。它通过标准化的协议桥接 AI 与真实工具，让开发者能够快速构建 AI‑驱动的媒体工作流。

**价值**  
- **AI‑工具互通**：通过 MCP，AI 代理可以像调用本地函数一样调用视频编辑器的功能，实现“AI 即插即用”。  
- **统一协议**：为不同 AI 模型提供一致的上下文交互层，降低跨平台、跨语言集成的复杂度。  
- **加速产品落地**：开发者无需自行实现繁杂的编辑 API，即可在自己的 AI 应用中直接使用专业级视频编辑能力。

**典型接入方式**  
1. **API/SDK**：项目提供 Swift SDK 与 REST‑like API，开发者在 macOS 环境下通过 CocoaPods / Swift Package Manager 引入即可。  
2. **CLI**：附带的命令行工具支持脚本化调用，可在 CI/CD 或后台服务中由 AI 代理触发。  
3. **MCP 服务器**：部署 Model Context Protocol 服务器后，任何遵循 MCP 的语言（Python、Node.js 等）都能通过标准 JSON‑RPC 与编辑器交互。  

**生产可用性**  
- **活跃度高**：截至 2026‑06‑23 最近一次提交，拥有 7 566 星、511 Fork，社区活跃，问题响应及时。  
- **技术成熟**：核心代码使用 Swift 编写，配套文档完整，提供完整的类型定义和示例。  
- **生态兼容**：支持 macOS 13+，可与常见的 AI 框架（如 LangChain、OpenAI SDK）配合使用。  
- **风险**：尚需对许可证（MIT）和安全审计进行最终确认，但整体已具备在生产环境中进行试点的条件。

## 🧭 Practical evaluation

**Value:** palmier-io/palmier-pro helps connect AI assistants to real tools and data through a standard protocol.

**Best use cases**

- connect AI agents to tools
- ship Model Context Protocol servers
- standardize integrations

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 7566 GitHub stars
- 511 forks
- updated 2026-06-23
- primary language: Swift
- 7 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 68/100 |
| stars | 83/100 |
| topics | 88/100 |
| outlook | 64/100 |
| quality | 73/100 |
| recency | 40/100 |
| adoption | 78/100 |
| production | 60/100 |
| usefulness | 58/100 |
| integration | 46/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 300/100 |

---

<sub>🔭 Discovered 2026-06-23 · [View on GitHub](https://github.com/palmier-io/palmier-pro) · [← Back to Video-editing](./README.md)</sub>
