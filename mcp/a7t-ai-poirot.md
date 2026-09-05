# a7t-ai/poirot

[![Stars](https://img.shields.io/github/stars/a7t-ai/poirot?style=flat-square&color=yellow)](https://github.com/a7t-ai/poirot/stargazers) [![Forks](https://img.shields.io/github/forks/a7t-ai/poirot?style=flat-square&color=blue)](https://github.com/a7t-ai/poirot/network) [![Language](https://img.shields.io/badge/lang-Swift-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-65%2F100-brightgreen?style=flat-square)](#)

> A native macOS companion for Claude Code that lets you browse sessions, explore diffs, and re-run commands.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 195 |
| 🍴 **Forks** | 13 |
| 💻 **Language** | Swift |
| 📈 **Score** | 65/100 |
| 🗓️ **Last push** | 2026-09-05 |
| 🔍 **Source** | github |

## 🏷️ Topics

`ai` `claude` `claude-code` `codex` `companion-app` `dev-tools` `homebrew-cask` `macos` `mcp` `native-macos` `open-ai` `session-viewer`

## 🎯 Categories

MCP · AI/ML

## 📝 Summary

### English

**Brief Summary**  
Poirot (a7t‑ai/poirot) is a native macOS companion for Claude Code that lets developers browse past sessions, view code diffs, and re‑run commands from a convenient UI. It implements the Model Context Protocol (MCP), providing a standard way to hook AI assistants into real tools and data sources.  

**Value**  
- **Standardised integration** – By exposing MCP endpoints, Poirot makes it trivial to connect Claude or any MCP‑compatible AI agent to a macOS development environment, eliminating ad‑hoc glue code.  
- **Rapid prototyping** – The UI surface for session history, diff inspection, and command replay accelerates the feedback loop when building AI‑driven tooling, reducing the time to validate ideas.  
- **Reusable backend** – The same MCP server can be reused across different front‑ends or CI pipelines, allowing teams to ship consistent AI‑tool integrations without rewriting protocol logic.  

**Practical Adoption Path**  
1. **Prototype** – Clone the repo, run the Swift package locally, and point your Claude Code instance (or any MCP client) to the provided endpoint.  
2. **Integrate** – Use the exposed API/SDK to embed Poirot’s session‑browsing and diff‑view capabilities into internal tools or CI scripts.  
3. **Extend** – Add custom commands or data sources by implementing the MCP interfaces in Swift or another language, then redeploy the server alongside your existing infrastructure.  
4. **Scale** – Containerise the MCP server, add authentication/role‑based access, and integrate with your production monitoring stack.  

**Production Readiness**  
- **Maturity**: Medium. The project is actively maintained (last update 2026‑07‑06), has 195 stars and 13 forks, and its core Swift implementation is stable, but it still requires a review of licensing, security hardening, and long‑term maintainer commitment.  
- **Dependencies**: Relies on macOS‑only APIs and Swift toolchains, so it fits well for internal macOS‑centric workflows but may need additional abstraction for cross‑platform deployments.  
- **Next steps for production**: Conduct a security audit (especially around the MCP endpoint), verify licensing compliance, add CI/CD pipelines for automated testing, and establish a maintenance plan (e.g., assign a dedicated owner). Once these checks are in place, Poirot can move from prototyping to a reliable component in internal or customer‑facing AI‑tool integrations.

### Русский

Резюме проекта a7t-ai/poirot:

Пойрот - это native macOS-компаньон для Клод Кода, который позволяет просматривать сессии, изучать разницы и перезапускать команды. Это проект, который помогает соединить AI-ассистентов с реальными инструментами и данными посредством стандартного протокола. Он готов к внедрению в прототипах или внутренних рабочих процессах, но требует проверки зависимостей и обслуживания перед выпуском в production.

### 中文

**项目简介**

a7t-ai/poirot 是一款原生 macOS 的 Claude Code 陪伴工具，允许用户浏览会话、探索差异和重新运行命令。它通过标准协议连接 AI 辅助器到真实工具和数据。

**价值**

a7t-ai/poirot 帮助连接 AI 辅助器到真实工具和数据通过标准协议，提高了整体的可用性和易用性。

**典型接入方式**

该项目主要适用于以下场景：

1. 连接 AI 代理到工具
2. 部署 Model Context Protocol 服务器
3. 标准化集成

**生产可用性**

该项目的生产可用性评估为中等（Medium），适合用于原型或内部工作流程，但需要进行依赖和维护检查后再用于生产环境。

## 🧭 Practical evaluation

**Value:** a7t-ai/poirot helps connect AI assistants to real tools and data through a standard protocol.

**Best use cases**

- connect AI agents to tools
- ship Model Context Protocol servers
- standardize integrations

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** Medium: useful for prototypes or internal workflows, with dependency and maintenance checks before production.

**Quality signals**

- 195 GitHub stars
- 13 forks
- updated 2026-07-06
- primary language: Swift
- 16 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 29/100 |
| stars | 49/100 |
| topics | 100/100 |
| outlook | 74/100 |
| quality | 69/100 |
| recency | 80/100 |
| adoption | 43/100 |
| production | 68/100 |
| usefulness | 74/100 |
| integration | 46/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 200/100 |

---

<sub>🔭 Discovered 2026-07-06 · [View on GitHub](https://github.com/a7t-ai/poirot) · [← Back to Mcp](./README.md)</sub>
