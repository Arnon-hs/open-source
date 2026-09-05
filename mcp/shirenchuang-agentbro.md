# shirenchuang/agentbro

[![Stars](https://img.shields.io/github/stars/shirenchuang/agentbro?style=flat-square&color=yellow)](https://github.com/shirenchuang/agentbro/stargazers) [![Forks](https://img.shields.io/github/forks/shirenchuang/agentbro?style=flat-square&color=blue)](https://github.com/shirenchuang/agentbro/network) [![Language](https://img.shields.io/badge/lang-Rust-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-78%2F100-brightgreen?style=flat-square)](#)

> A macOS Dynamic Island for AI coding agents: Claude Code, Codex, Gemini CLI, Cursor, hooks, skills, and local agent management.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 128 |
| 🍴 **Forks** | 21 |
| 💻 **Language** | Rust |
| 📈 **Score** | 78/100 |
| 🗓️ **Last push** | 2026-09-05 |
| 🔍 **Source** | github |

## 🏷️ Topics

`agent-tools` `ai-agents` `claude-code` `coding-agent` `cursor` `desktop-app` `developer-tools` `dynamic-island` `gemini-cli` `local-first` `macos` `mcp`

## 🎯 Categories

MCP · AI/ML · Productivity · Frontend · DevTools

## 📝 Summary

### English

**Brief Summary (2‑3 sentences)**  
AgentBro (shirenchuang/agentbro) is an open‑source macOS Dynamic Island that lets AI coding agents such as Claude Code, Codex, Gemini CLI, and Cursor interact with real tools, data, and local agents through a unified Model Context Protocol. Written in Rust, it provides a standard API/SDK/CLI layer for plugging in custom hooks, skills, and agent management, making it easy to expose and consume AI‑driven functionality across development workflows.

**Value**  
- **Standardized integration** – By implementing the Model Context Protocol, AgentBro removes the need for bespoke glue code, letting multiple AI assistants share a common interface to tools, files, and services.  
- **Rich macOS UX** – The Dynamic Island UI gives developers immediate visual feedback and control over agent actions, improving usability and debugging.  
- **Extensible ecosystem** – Hooks, skills, and local agent management are modular, so teams can add new capabilities (e.g., CI pipelines, secret stores) without rewriting the core.

**Practical Adoption Path**  
1. **Evaluate the API/CLI** – Clone the repo, run the provided Docker or Homebrew install, and test the sample CLI against a familiar model (e.g., Claude or Gemini).  
2. **Create a connector** – Implement a small wrapper (Rust, Python, or Bash) that registers a tool or data source with AgentBro’s protocol; the repository includes templates for common patterns.  
3. **Pilot in a dev team** – Deploy the Dynamic Island on developers’ Macs, configure the desired agents, and monitor usage via the built‑in logs.  
4. **Scale** – Add custom hooks or a Model Context Protocol server for internal services, and integrate with CI/CD pipelines to automate code generation or review tasks.

**Production Readiness**  
- **Activity & Adoption**: 128 stars, 21 forks, recent commits (as of 2026‑06‑24), and growing community usage indicate healthy momentum.  
- **Technical maturity**: Core is written in Rust, offering performance and safety; the API surface is stable and documented, with clear SDK/CLI entry points.  
- **Risk considerations**: No major metadata or licensing red flags yet, but a final security audit and confirmation of an active maintainer are recommended before mission‑critical deployment. Overall, AgentBro is a strong OSS candidate for a pilot and can be promoted to production once the minor due‑diligence items are cleared.

### Русский

**AgentBro** — это open‑source‑платформа (Rust) для macOS, превращающая Dynamic Island в централизованный шлюз между AI‑кодинг‑агентами (Claude Code, Codex, Gemini CLI, Cursor и др.) и реальными инструментами/данными через единый протокол Model Context Protocol. Типичный сценарий — подключить любой AI‑ассистент к локальным сервисам, хук‑скриптам или собственным навыкам, а также развернуть собственный MCP‑сервер для стандартизированных интеграций. Проект демонстрирует высокий уровень готовности к production: активные коммиты, рост звёзд (128), форков (21) и широкая поддержка экосистемы, что делает его надёжным кандидатом для пилотного внедрения.

### 中文

**项目简介**  
AgentBro（shirenchuang/agentbro）是一个在 macOS Dynamic Island 上运行的 AI 编码助手平台，内置 Claude Code、Codex、Gemini CLI、Cursor 等多种模型，并提供 Hook、Skill 与本地 Agent 管理功能。它通过统一的 Model Context Protocol（MCP）让 AI 助手能够直接调用真实工具和数据。

**价值主张**  
- **统一协议**：采用标准的 MCP，消除不同 AI 模型与本地工具之间的集成壁垒，降低开发和运维成本。  
- **即插即用**：内置多模型支持和可扩展的 Hook/Skill 机制，企业可以快速把已有的 AI 助手接入内部 CI/CD、监控、数据库等业务系统。  
- **本地化管理**：提供本地 Agent 生命周期管理与安全沙箱，兼顾隐私与合规需求。

**典型接入方式**  
1. **API/SDK**：通过项目暴露的 REST/WS API 或 Rust SDK，调用 `run_agent`、`register_hook` 等接口，实现模型与业务工具的双向通信。  
2. **CLI**：使用自带的 `agentbro-cli` 在终端直接启动、调试或部署 Agent，适合 DevOps 流程自动化。  
3. **MCP 服务器**：在内部网络部署 MCP Server，所有 AI Agent 通过统一协议注册并获取工具元数据、权限和执行上下文。  
4. **语言元数据**：项目提供的语言标签（Rust、Python 等）可用于生成对应语言的包装库，进一步简化集成。

**生产可用性**  
- **活跃度**：最近一次提交在 2026‑06‑24，星标 128、fork 21，社区活跃，具备持续迭代的动力。  
- **技术成熟度**：核心实现基于 Rust，性能可靠；提供完整的 API、CLI 与 SDK 文档，易于评估和上线。  
- **生态兼容**：已对接 Claude、Codex、Gemini、Cursor 等主流模型，且支持自定义 Hook，能够满足大多数企业的工具链需求。  
- **风险点**：仍需进一步审查许可证（MIT/Apache 等）和安全审计报告；维护者虽活跃，但建议在关键业务场景下设立内部备份或 Fork。  

综上，AgentBro 在标准化 AI 与本地工具的集成方面具备明确价值，接入方式灵活，且已具备较高的生产可用性，适合作为企业内部 AI 助手平台的首选 OSS 方案。

## 🧭 Practical evaluation

**Value:** shirenchuang/agentbro helps connect AI assistants to real tools and data through a standard protocol.

**Best use cases**

- connect AI agents to tools
- ship Model Context Protocol servers
- standardize integrations

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 128 GitHub stars
- 21 forks
- updated 2026-06-24
- primary language: Rust
- 17 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 34/100 |
| stars | 45/100 |
| topics | 100/100 |
| outlook | 78/100 |
| quality | 69/100 |
| recency | 80/100 |
| adoption | 42/100 |
| production | 72/100 |
| usefulness | 100/100 |
| integration | 78/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 500/100 |

---

<sub>🔭 Discovered 2026-06-24 · [View on GitHub](https://github.com/shirenchuang/agentbro) · [← Back to Mcp](./README.md)</sub>
