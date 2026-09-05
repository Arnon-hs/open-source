# mistweaverco/kulala.nvim

[![Stars](https://img.shields.io/github/stars/mistweaverco/kulala.nvim?style=flat-square&color=yellow)](https://github.com/mistweaverco/kulala.nvim/stargazers) [![Forks](https://img.shields.io/github/forks/mistweaverco/kulala.nvim?style=flat-square&color=blue)](https://github.com/mistweaverco/kulala.nvim/network) [![Language](https://img.shields.io/badge/lang-Lua-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-68%2F100-brightgreen?style=flat-square)](#)

> A fully-featured ⚡️ HTTP/GraphQL/gRPC/Websocket-client 🐼 interface 🖥️ for Neovim ❤️, that supports the Jetbrains .http spec (with full scripting support).

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 2.1k |
| 🍴 **Forks** | 99 |
| 💻 **Language** | Lua |
| 📈 **Score** | 68/100 |
| 🗓️ **Last push** | 2026-09-05 |
| 🔍 **Source** | github |

## 🏷️ Topics

`cli` `curl` `gh-action` `graphql` `graphql-client` `grpc` `grpc-client` `http-client` `jetbrains-http-client` `lua` `neovim` `neovim-plugin`

## 🎯 Categories

Networking · Backend · DevTools · Security

## 📝 Summary

### English

**Brief Summary (2‑3 sentences)**  
kulala.nvim is a Lua‑based Neovim plugin that turns the editor into a full‑featured HTTP/GraphQL/gRPC/WebSocket client, supporting the JetBrains `.http` specification and offering scriptable request handling. With over 2 000 GitHub stars and recent activity, it provides a convenient, in‑editor way to test and interact with APIs, making it especially useful for developers building AI‑augmented workflows.  

**Value**  
- **AI‑ready testing ground:** By letting you send arbitrary HTTP, GraphQL, gRPC, or WebSocket calls directly from Neovim, kulala.nvim becomes a lightweight front‑end for prototyping AI services, RAG pipelines, or agent‑based integrations without leaving your coding environment.  
- **JetBrains `.http` compatibility:** Reuse existing request files and scripts, lowering the barrier for teams already using JetBrains tools.  
- **Extensible scripting:** Lua hooks let you programmatically modify requests/responses, enabling dynamic credential injection, prompt generation, or result post‑processing for AI experiments.  

**Practical Adoption Path**  
1. **Install the plugin** (e.g., via `packer.nvim` or `lazy.nvim`).  
2. **Add a `.http` file** or create requests with the provided commands (`:Kulala`, `:KulalaRun`).  
3. **Leverage Lua callbacks** to inject AI model endpoints, API keys, or custom headers, turning the plugin into a thin SDK for your AI service.  
4. **Integrate with CI/CD** by invoking the CLI mode (`kulala-cli`) in test suites to validate API contracts automatically.  

**Production Readiness**  
- **Activity & community:** 2 082 stars, 99 forks, recent commits (as of 2026‑06‑25), and a solid Lua codebase indicate an active, maintained project.  
- **Stability:** The plugin follows Neovim’s stable API, and its core request‑handling logic is well‑tested through community usage.  
- **Risk considerations:** No major metadata or licensing red flags have been identified, but a final review of the MIT‑style license, dependency security (LuaRocks modules), and maintainer responsiveness is advisable before wide‑scale deployment.  

Overall, kulala.nvim is production‑ready for pilots and can be smoothly adopted as a developer‑centric API client that accelerates AI feature prototyping and testing within Neovim.

### Русский

**Краткое резюме:**  
`mistweaverco/kulala.nvim` — это полнофункциональный клиент HTTP/GraphQL/gRPC/WebSocket, реализованный на Lua и интегрированный в Neovim, который поддерживает спецификацию JetBrains `.http` и позволяет писать скрипты для динамического формирования запросов. Проект идеален для быстрого прототипирования AI‑фич, построения RAG‑ и агентных пайплайнов и оценки различных моделей, так как предоставляет готовый API/SDK/CLI и метаданные языка прямо в редакторе. По состоянию на 2026‑06‑25 репозиторий демонстрирует высокую готовность к production: активные коммиты, более 2000 звёзд, 99 форков и широкую экосистемную поддержку, хотя окончательная проверка лицензии и безопасности всё‑ещё требуется.

### 中文

mistweaverco/kulala.nvim 是一款功能齐全的 Neovim HTTP/GraphQL/gRPC/WebSocket 客户端，支持 JetBrains .http 规范并提供完整的脚本化能力，能够快速为编辑器添加 AI 功能而无需从零构建模型栈。它通过暴露 API/SDK/CLI、语言元数据等接口，使得原型 AI 特性、RAG 或 Agent 工作流以及模型工具评估的集成变得十分直接。得益于最近的活跃更新、2082 颗星标和强劲的生态信号，该项目在开源候选者中具有较高的

## 🧭 Practical evaluation

**Value:** mistweaverco/kulala.nvim helps add AI capability without starting from a blank model stack.

**Best use cases**

- prototype AI features
- build RAG or agent workflows
- evaluate model tooling

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 2082 GitHub stars
- 99 forks
- updated 2026-06-25
- primary language: Lua
- 20 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 50/100 |
| stars | 71/100 |
| topics | 100/100 |
| outlook | 76/100 |
| quality | 79/100 |
| recency | 80/100 |
| adoption | 65/100 |
| production | 74/100 |
| usefulness | 58/100 |
| integration | 62/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 400/100 |

---

<sub>🔭 Discovered 2026-06-25 · [View on GitHub](https://github.com/mistweaverco/kulala.nvim) · [← Back to Networking](./README.md)</sub>
