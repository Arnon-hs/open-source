# FunplayAI/funplay-godot-mcp

[![Stars](https://img.shields.io/github/stars/FunplayAI/funplay-godot-mcp?style=flat-square&color=yellow)](https://github.com/FunplayAI/funplay-godot-mcp/stargazers) [![Forks](https://img.shields.io/github/forks/FunplayAI/funplay-godot-mcp?style=flat-square&color=blue)](https://github.com/FunplayAI/funplay-godot-mcp/network) [![Language](https://img.shields.io/badge/lang-GDScript-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-68%2F100-brightgreen?style=flat-square)](#)

> The Most Advanced MCP Server for Godot Editor with execute_code, prompts/resources, project maps, runtime inspection, asset workflows, and safe AI automation.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 22 |
| 🍴 **Forks** | 2 |
| 💻 **Language** | GDScript |
| 📈 **Score** | 68/100 |
| 🗓️ **Last push** | 2026-08-24 |
| 🔍 **Source** | github |

## 🏷️ Topics

`ai` `ai-tools` `claude-code` `codex` `csharp` `cursor` `game-development` `gdscript` `github-copilot` `godot` `godot-editor` `godot-engine`

## 🎯 Categories

MCP · Automation · AI/ML · Backend

## 📝 Summary

### English

**Brief Summary**  
FunplayAI’s *funplay‑godot‑mcp* is an open‑source Model Context Protocol (MCP) server that runs inside the Godot editor, exposing a rich set of hooks such as `execute_code`, prompt/resource libraries, project‑map queries, runtime inspection, asset‑pipeline automation, and safe AI‑driven workflows. It lets AI assistants interact with Godot projects through a standardized API, enabling automated tooling, AI‑assisted development, and seamless integration of external models.

**Value**  
- **Standardized AI‑to‑tool bridge** – By implementing the MCP spec, the server turns Godot into a first‑class “real‑world” tool that any MCP‑compatible AI can query and control, eliminating ad‑hoc integrations.  
- **End‑to‑end automation** – Built‑in commands for code execution, resource fetching, map navigation, and asset handling let AI agents perform tasks that normally require manual editor interaction (e.g., generating scripts, placing nodes, tweaking materials).  
- **Safety & observability** – The server isolates AI actions, logs every request, and provides runtime inspection, making it suitable for controlled production use where auditability is required.

**Practical Adoption Path**  
1. **Prototype** – Clone the repo, run the provided Docker/CLI starter, and point an MCP‑compatible AI (e.g., OpenAI function‑calling, LangChain, or a custom agent) at the server’s HTTP endpoint.  
2. **Integrate with your pipeline** – Replace the default Godot editor workflow with the MCP server for tasks such as automated asset import, batch script generation, or CI‑driven level validation.  
3. **Secure & Harden** – Enable authentication (API keys or OAuth), restrict `execute_code` to a sandboxed subset, and configure logging/monitoring.  
4. **Scale** – Deploy the server as a microservice behind a load balancer; multiple Godot editor instances can share the same MCP endpoint for team‑wide AI assistance.

**Production Readiness**  
- **Activity & Ecosystem** – Updated on 2026‑07‑13, 22 stars, 2 forks, and 18 relevant topics indicate an active community and recent maintenance.  
- **Maturity** – The core MCP features (code execution, asset workflow, inspection) are already implemented and exposed via a clear API/SDK/CLI, making pilot deployments straightforward.  
- **Risks** – Licensing and long‑term maintainer commitment still need a final check, and a security audit of the code‑execution sandbox is advisable before full production rollout.  

Overall, *funplay‑godot‑mcp* is a high‑readiness OSS component that can be quickly evaluated and, after modest hardening, used in production to give AI agents reliable, safe access to Godot’s editor capabilities.

### Русский

FunplayAI / funplay‑godot‑mcp — это самый продвинутый MCP‑сервер для Godot‑Editor, который позволяет подключать AI‑ассистентов к реальным инструментам и данным через единый протокол, предоставляя функции execute_code, работу с промптами/ресурсами, картами проектов, инспекцией рантайма и безопасной автоматизацией. Типичный сценарий — интеграция AI‑агентов в пайплайны разработки (инспекция кода, генерация контента, управление ассетами) либо развёртывание Model Context Protocol серверов для стандартизированных подключений. Проект считается готовым к production‑использованию: активные коммиты, рост звёзд, поддержка API/SDK/CLI и широкая экосистема, хотя лицензия и безопасность требуют окончательной проверки.

### 中文

**项目简介（2‑3 句话）**  
FunplayAI/funplay‑godot‑mcp 是面向 Godot 编辑器的最先进的 MCP（Model Context Protocol）服务器，提供代码执行、提示/资源管理、项目映射、运行时检查、资产工作流以及安全的 AI 自动化功能。它通过统一协议把 AI 助手直接连接到真实的编辑器工具和项目数据，实现“AI + Godot” 的高效协作。

**价值主张**  
- **AI‑工具桥梁**：让任何遵循 MCP 的 AI 代理能够调用 Godot 编辑器的功能（如运行脚本、查询资源、修改场景），实现真正的“代码即服务”。  
- **标准化集成**：提供统一的 API/SDK/CLI 接口，帮助团队快速搭建模型上下文服务或在 CI/CD 流程中嵌入 AI 自动化。  
- **安全与可审计**：内置执行沙箱与运行时检查，确保 AI 生成的代码在受控环境中运行，降低安全风险。

**典型接入方式**  
1. **作为本地或容器化服务启动**：克隆仓库后直接运行 `godot -s mcp_server.gd`（或使用提供的 Dockerfile），服务器会在指定端口暴露 MCP 接口。  
2. **通过 SDK 调用**：项目提供的 GDScript/HTTP 客户端库封装了 `execute_code`、`list_prompts`、`inspect_runtime` 等 RPC，开发者只需在自己的插件或外部服务中引入即可。  
3. **CLI/脚本集成**：命令行工具 `funplay-mcp-cli` 支持一键发送代码片段、查询项目映射或触发资产流水线，适合 CI、自动化测试或批处理场景。  

**生产可用性**  
- **活跃度**：截至 2026‑07‑13 最近一次提交，仓库拥有 22 星、2 个 fork，且持续接受社区 PR，表明维护状态良好。  
- **技术成熟度**：实现了完整的 MCP 信号（API/SDK/CLI），并在 Godot 主流版本（4.x）上通过实测，可直接用于生产环境。  
- **风险点**：需进一步审查许可证兼容性、依赖的第三方库安全性以及维护者的长期可用性；但就当前代码质量和社区反馈来看，已具备作为 OSS 组件投入正式项目的条件。  

综上，FunplayAI/funplay‑godot‑mcp 为希望将 AI 助手深度集成到 Godot 工作流的团队提供了即插即用、可审计且相对成熟的解决方案。

## 🧭 Practical evaluation

**Value:** FunplayAI/funplay-godot-mcp helps connect AI assistants to real tools and data through a standard protocol.

**Best use cases**

- connect AI agents to tools
- ship Model Context Protocol servers
- standardize integrations

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 22 GitHub stars
- 2 forks
- updated 2026-07-13
- primary language: GDScript
- 18 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 12/100 |
| stars | 29/100 |
| topics | 100/100 |
| outlook | 60/100 |
| quality | 51/100 |
| recency | 40/100 |
| adoption | 24/100 |
| production | 56/100 |
| usefulness | 100/100 |
| integration | 78/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 400/100 |

---

<sub>🔭 Discovered 2026-07-13 · [View on GitHub](https://github.com/FunplayAI/funplay-godot-mcp) · [← Back to Mcp](./README.md)</sub>
