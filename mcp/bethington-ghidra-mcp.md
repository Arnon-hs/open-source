# bethington/ghidra-mcp

[![Stars](https://img.shields.io/github/stars/bethington/ghidra-mcp?style=flat-square&color=yellow)](https://github.com/bethington/ghidra-mcp/stargazers) [![Forks](https://img.shields.io/github/forks/bethington/ghidra-mcp?style=flat-square&color=blue)](https://github.com/bethington/ghidra-mcp/network) [![Language](https://img.shields.io/badge/lang-Java-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-86%2F100-brightgreen?style=flat-square)](#)

> Ghidra MCP Server — 200+ MCP tools for AI-powered reverse engineering. GUI plugin + headless server, lazy tool loading, convention enforcement, batch operations, Ghidra Server integration, and Docker deployment.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 2.6k |
| 🍴 **Forks** | 43 |
| 💻 **Language** | Java |
| 📈 **Score** | 86/100 |
| 🗓️ **Last push** | 2026-06-26 |
| 🔍 **Source** | github |

## 🏷️ Topics

`ai` `binary-analysis` `ghidra` `ghidra-extension` `java` `mcp` `mcp-server` `model-context-protocol` `python` `reverse-engineering` `static-analysis`

## 🎯 Categories

MCP · AI/ML · Frontend · Backend · DevOps/Infra

## 📝 Summary

### English

**Summary**  
The ghidra‑mcp project delivers a Ghidra‑based Model Context Protocol (MCP) server that bundles more than 200 ready‑to‑use reverse‑engineering tools, exposing them through a standardized API/CLI and a GUI plugin. It supports lazy loading, batch operations, Ghidra Server integration, and can be run head‑less or inside Docker, making it easy to plug AI assistants into real analysis workflows.

**Value**  
By providing a common “MCP” interface, the project lets AI agents invoke concrete reverse‑engineering actions (e.g., decompilation, data‑type inference, script execution) without custom scripting for each tool. This standardization accelerates the development of AI‑driven analysis pipelines, reduces integration friction, and enables organizations to reuse a single, well‑maintained toolset across projects.

**Practical adoption path**  
1. **Prototype** – Pull the Docker image or launch the headless server, point your AI agent to the MCP endpoint, and call a few simple commands (e.g., `list-tools`, `run-tool`).  
2. **Integrate** – Add the GUI plugin to an existing Ghidra installation for interactive debugging, or embed the Java SDK/CLI in your CI/CD pipeline for batch processing.  
3. **Scale** – Deploy the server behind a load balancer, configure Ghidra Server authentication, and use the built‑in batch features to process large codebases automatically.

**Production readiness**  
The repository shows strong community traction (2 593 stars, recent commits, active issue handling) and a mature codebase (Java, 200+ tools, Docker support). Its modular architecture, clear API contract, and existing Ghidra Server integration suggest it is ready for pilot deployments, though a final security and licensing audit is recommended before full‑scale production use.

### Русский

**Ghidra MCP Server** (bethington/ghidra-mcp) — это набор из более чем 200 MCP‑инструментов, позволяющих подключать AI‑ассистентов к реальному функционалу Ghidra через единый протокол Model Context Protocol. Типичный сценарий: развертываете сервер (GUI‑плагин, headless‑режим или Docker‑контейнер), задаёте конвенции и пакетные операции, а затем AI‑агент получает доступ к анализу кода, загрузке данных и интеграции с Ghidra Server. Проект уже имеет активную поддержку, более 2,5 k звёзд, частые обновления и готов к production‑использованию в пилотных и масштабных проектах.

### 中文

**项目简介**  
Ghidra MCP Server（bethington/ghidra-mcp）在 Ghidra 上实现了 200+ Model Context Protocol（MCP）工具，提供 GUI 插件和无头服务器两种模式，支持惰性加载、约定强制、批量操作、Ghidra Server 集成以及 Docker 部署。

**价值**  
- **AI 与逆向工程深度融合**：通过统一的 MCP 协议，把 AI 助手直接挂接到真实的逆向工具和数据，使模型能够执行具体的分析、重构或自动化任务，而不仅是文字交互。  
- **标准化、可复用的工具链**：所有工具遵循同一协议和元数据约定，降低了不同 AI Agent 与逆向工具之间的集成成本，适合构建内部或 SaaS 型的 AI‑assisted reverse‑engineering 平台。  
- **一站式部署**：提供 Docker 镜像、Headless Server 与 Ghidra GUI 插件，既能在本地工作站快速试用，也能在 CI/CD 或云环境中以服务方式运行。

**典型接入方式**  
1. **作为本地插件**：在 Ghidra GUI 中安装 `ghidra-mcp` 插件，启动后即可在 Ghidra 界面直接调用 MCP 工具，适合交互式分析。  
2. **Headless Server + API**：在服务器上以 Docker 方式启动 `ghidra-mcp` 的无头实例，使用其 REST/JSON‑RPC 接口或提供的 Java SDK、CLI 与外部 AI Agent（如 ChatGPT、Claude）通信。  
3. **与 Ghidra Server 集成**：将 MCP Server 配置为 Ghidra Server 的后端服务，实现多人协作项目中 AI 自动化分析的统一入口。  

**生产可用性**  
- **活跃度高**：截至 2026‑06‑26，项目仍在持续更新，拥有 2.6k+ ⭐、43 fork，社区讨论活跃。  
- **技术成熟**：基于 Java 实现，兼容 Ghidra 官方插件体系；提供完整的 Docker 镜像和 CI 支持，易于在容器化环境中部署。  
- **安全与合规**：暂无重大元数据风险，仍需对许可证（Apache‑2.0）和依赖库的安全审计进行最终确认。  
- **适配度强**：提供 API/SDK/CLI、语言元数据以及明确的工具约定，便于快速评估并在生产环境中进行 Pilot 项目。  

综上，`bethington/ghidra-mcp` 已具备较高的生产就绪度，是将 AI 助手与逆向工程工具链深度结合的首选开源方案。

## 🧭 Practical evaluation

**Value:** bethington/ghidra-mcp helps connect AI assistants to real tools and data through a standard protocol.

**Best use cases**

- connect AI agents to tools
- ship Model Context Protocol servers
- standardize integrations

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 2593 GitHub stars
- 43 forks
- updated 2026-06-26
- primary language: Java
- 11 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 41/100 |
| stars | 73/100 |
| topics | 100/100 |
| outlook | 89/100 |
| quality | 84/100 |
| recency | 100/100 |
| adoption | 64/100 |
| production | 84/100 |
| usefulness | 90/100 |
| integration | 94/100 |
| sourceTrust | 100/100 |

---

<sub>🔭 Discovered 2026-06-26 · [View on GitHub](https://github.com/bethington/ghidra-mcp) · [← Back to Mcp](./README.md)</sub>
