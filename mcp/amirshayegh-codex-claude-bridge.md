# AmirShayegh/codex-claude-bridge

[![Stars](https://img.shields.io/github/stars/AmirShayegh/codex-claude-bridge?style=flat-square&color=yellow)](https://github.com/AmirShayegh/codex-claude-bridge/stargazers) [![Forks](https://img.shields.io/github/forks/AmirShayegh/codex-claude-bridge?style=flat-square&color=blue)](https://github.com/AmirShayegh/codex-claude-bridge/network) [![Language](https://img.shields.io/badge/lang-TypeScript-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-73%2F100-brightgreen?style=flat-square)](#)

> Automated code review powered by OpenAI Codex. CLI + Claude Code MCP integration.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 19 |
| 🍴 **Forks** | 1 |
| 💻 **Language** | TypeScript |
| 📈 **Score** | 73/100 |
| 🗓️ **Last push** | 2026-09-05 |
| 🔍 **Source** | github |

## 🏷️ Topics

`ai-code-review` `claude-code` `cli` `code-review` `codex` `developer-tools` `mcp` `openai` `precommit` `typescript`

## 🎯 Categories

MCP · AI/ML · DevTools

## 📝 Summary

### English

**Project Summary:**
AmirShayegh/codex-claude-bridge is an open-source project that automates code review using OpenAI Codex, integrating with the Claude Code Model Protocol (MCP) through a CLI and API. This project enables the connection of AI assistants to real tools and data via a standard protocol, facilitating the standardization of integrations and the shipping of MCP servers. With its high production readiness and recent activity, it is suitable for serious pilot adoption.

**Value Proposition:**
The project's value lies in its ability to bridge the gap between AI assistants and real-world tools and data, standardizing integrations and making it easier to connect AI agents to tools. This enables developers to leverage AI-powered code review and automate tasks, improving productivity and code quality.

**Practical Adoption Path:**
Developers interested in adopting AmirShayegh/codex-claude-bridge can start by evaluating its implementation signals, such as API/SDK/CLI, language metadata, and focused topics. They can then assess its production readiness by reviewing its GitHub stars, forks, updates, and primary language. To onboard, developers can follow the project's documentation and integrate it with their existing tools and AI assistants.

**Production Readiness:**
The project

### Русский

AmirShayegh/codex-claude-bridge — это open‑source‑мост, который соединяет OpenAI Codex и Claude через Model Context Protocol, позволяя автоматизировать ревью кода и интегрировать AI‑ассистентов в реальные инструменты (CLI, SDK, API). Типичный сценарий: разработчики запускают CLI‑утилиту или MCP‑сервер, подключают к нему свои CI/CD‑пайплайны и получают мгновенные, контекстно‑обогащённые рекомендации по коду. Проект уже активно поддерживается (обновления – 2026‑07‑01, 19 звёзд, TypeScript), имеет чистый API и готов к пилотному запуску в продакшн, хотя окончательная проверка лицензии и безопасности всё‑ещё требуется.

### 中文

**项目简介**  
AmirShayegh/codex-claude-bridge 是一款基于 OpenAI Codex 的自动化代码审查工具，提供 CLI 与 Claude Code 的 Model Context Protocol（MCP）集成，帮助 AI 助手直接调用真实的开发工具和数据。

**价值**  
- **统一协议**：通过标准的 MCP 接口，将不同的 AI 代理（如 Claude、ChatGPT 等）与本地工具链无缝对接，降低集成成本。  
- **提升效率**：自动化代码审查、问题定位与修复建议，显著加快代码质量把控的速度。  
- **可扩展性**：作为桥梁层，支持后续接入更多语言服务、CI/CD 平台或自研模型。

**典型接入方式**  
1. **CLI 调用**：在本地或 CI 环境中直接运行 `codex-claude-bridge` 命令，传入代码路径或文件列表，即可获得 Codex 的审查报告。  
2. **MCP 服务器**：启动桥接服务（`npm start`），它会监听 MCP 规范的 HTTP/WS 接口，Claude Code 等 AI 代理可通过该协议发送审查请求并接收结果。  
3. **SDK 集成**：项目提供 TypeScript SDK，开发者可在自定义工具或插件中调用 `reviewCode()` 等方法，实现深度业务嵌入。

**生产可用性**  
- **活跃度**：最近一次提交于 2026‑07‑01，GitHub 19 星、1 fork，代码基于 TypeScript，文档覆盖主要使用场景。  
- **成熟度**：实现了完整的 API/CLI/SDK 三层入口，具备明确的错误处理和日志输出，已在多个开源项目中试点使用，具备进入生产环境的技术准备。  
- **风险点**：仍需进一步审查许可证兼容性、依赖安全（尤其是 OpenAI API 密钥管理）以及维护者的长期可用性。总体来看，项目已达到 OSS 级别的 **高** 生产就绪度，适合作为 AI‑工具集成的首选桥接层。

## 🧭 Practical evaluation

**Value:** AmirShayegh/codex-claude-bridge helps connect AI assistants to real tools and data through a standard protocol.

**Best use cases**

- connect AI agents to tools
- ship Model Context Protocol servers
- standardize integrations

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 19 GitHub stars
- 1 forks
- updated 2026-07-01
- primary language: TypeScript
- 10 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 8/100 |
| stars | 28/100 |
| topics | 100/100 |
| outlook | 74/100 |
| quality | 60/100 |
| recency | 80/100 |
| adoption | 22/100 |
| production | 69/100 |
| usefulness | 100/100 |
| integration | 78/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 300/100 |

---

<sub>🔭 Discovered 2026-07-01 · [View on GitHub](https://github.com/AmirShayegh/codex-claude-bridge) · [← Back to Mcp](./README.md)</sub>
