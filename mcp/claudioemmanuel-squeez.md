# claudioemmanuel/squeez

[![Stars](https://img.shields.io/github/stars/claudioemmanuel/squeez?style=flat-square&color=yellow)](https://github.com/claudioemmanuel/squeez/stargazers) [![Forks](https://img.shields.io/github/forks/claudioemmanuel/squeez?style=flat-square&color=blue)](https://github.com/claudioemmanuel/squeez/network) [![Language](https://img.shields.io/badge/lang-Rust-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-72%2F100-brightgreen?style=flat-square)](#)

> Hook-based token compressor for 5 AI CLI hosts (Claude Code, Copilot CLI, OpenCode, Gemini CLI, Codex CLI). Up to 95% bash compression, signature-mode for code reads, cross-call dedup, MCP server, self-teaching protocol. Zero runtime deps.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 160 |
| 🍴 **Forks** | 15 |
| 💻 **Language** | Rust |
| 📈 **Score** | 72/100 |
| 🗓️ **Last push** | 2026-09-05 |
| 🔍 **Source** | github |

## 🏷️ Topics

`ai-cli` `bash-hook` `claude-code` `codex-cli` `context-engineering` `context-window` `copilot-cli` `gemini-cli` `llm` `llm-tools` `mcp-server` `opencode`

## 🎯 Categories

MCP · AI/ML · Backend · DevTools

## 📝 Summary

### English

**Brief Summary**  
Claudioemmanuel/squeez is a Rust‑based, zero‑dependency hook system that compresses token streams for five AI‑CLI hosts (Claude Code, Copilot CLI, OpenCode, Gemini CLI, Codex CLI), achieving up to 95 % reduction in Bash payloads. It adds a “signature‑mode” for safe code reads, cross‑call deduplication, an MCP (Model Context Protocol) server, and a self‑teaching protocol that lets AI agents learn from prior interactions.

**Value**  
- **Token efficiency:** By shrinking prompts and responses, squeez cuts API costs and speeds up LLM calls, especially for long Bash or code snippets.  
- **Standardised integration:** The MCP server and hook API give every supported AI CLI a common way to expose tools, data, and execution results, turning ad‑hoc scripts into a reusable, discoverable service layer.  
- **Self‑learning:** The built‑in teaching protocol records successful tool‑calls and feeds them back into the model context, improving agent performance over time without manual prompt engineering.  

**Practical Adoption Path**  
1. **Prototype:** Drop the `squeez` binary (or add the Rust crate) into an existing CI pipeline, configure the MCP endpoint for the target AI CLI, and enable the `--compress` flag.  
2. **Tool‑binding:** Register your internal tools (e.g., deployment scripts, data‑fetchers) via the provided hook manifest; the system will automatically deduplicate repeated calls.  
3. **Production rollout:** Deploy the MCP server behind a reverse proxy, point all AI‑assistant instances to it, and enable the signature‑mode for read‑only code inspections.  
4. **Iterate:** Use the self‑teaching logs to refine hook definitions and optionally feed the learned context back into custom model fine‑tuning.  

**Production Readiness**  
- **Activity & adoption:** 160 ★, 15 forks, recent commits (as of 2026‑06‑30) and usage across multiple AI CLI projects indicate an active community.  
- **Technical maturity:** Zero runtime dependencies, a single compiled binary, and a well‑documented Rust API reduce operational overhead.  
- **Risk considerations:** License and security posture still need a final audit, and long‑term maintainership should be confirmed, but the current signals are strong enough for a serious pilot in a controlled environment.  

Overall, squeez offers a low‑friction, high‑impact way to make AI agents more cost‑effective and tool‑aware, making it a viable candidate for production‑grade deployments after the standard compliance checks.

### Русский

**cl​audioemmanuel/squeez** — это лёгкий, полностью без внешних зависимостей, hook‑based компрессор токенов, позволяющий сократить до 95 % объём Bash‑команд для пяти популярных AI‑CLI (Claude Code, Copilot CLI, OpenCode, Gemini CLI, Codex CLI), а также поддерживает режим подписи для чтения кода, кросс‑вызов‑дедупликацию, MCP‑сервер и протокол самообучения. Типичный сценарий — подключение AI‑агентов к реальным инструментам и данным через единый Model Context Protocol, развертывание собственного MCP‑сервера и стандартизация интеграций в DevTools‑стеке. Проект имеет высокий уровень готовности к production: активные коммиты (последний 30 июня 2026), 160 звёзд, 15 форков, написан на Rust и уже используется в нескольких пилотных проектах, однако перед масштабным внедрением следует уточнить лицензию, безопасность и наличие активных мейнтейнеров.

### 中文

**简短介绍**

Claudio Emmanuel 的 Squeez 项目是一个基于 Hook 的令牌压缩器，用于连接 5 个 AI CLI 主机（Claude Code、Copilot CLI、OpenCode、Gemini CLI 和 Codex CLI）。该项目可以压缩 bash 脚本，实现高达 95% 的压缩率，并提供签名模式、跨调用去重、MCP 服务器和自我学习协议等功能。该项目使用 Rust 编写，具有零运行时依赖。

**价值**

Claudio Emmanuel 的 Squeez 项目的价值在于它帮助连接 AI 助手到真实工具和数据，通过标准协议标准化集成。它可以帮助开发者连接 AI 代理到工具，部署 Model Context Protocol 服务器，并标准化集成。

**典型接入方式**

该项目提供了 API/SDK/CLI 等接入方式，可以方便地接入到 AI CLI 主机。开发者可以通过 GitHub 仓库获取更多的信息和文档。

**生产可用性**

该项目具有高生产可用性，最近活动、采用和生态信号都强劲 enough 为严重的试验做好准备。

## 🧭 Practical evaluation

**Value:** claudioemmanuel/squeez helps connect AI assistants to real tools and data through a standard protocol.

**Best use cases**

- connect AI agents to tools
- ship Model Context Protocol servers
- standardize integrations

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 160 GitHub stars
- 15 forks
- updated 2026-06-30
- primary language: Rust
- 18 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 30/100 |
| stars | 47/100 |
| topics | 100/100 |
| outlook | 77/100 |
| quality | 69/100 |
| recency | 80/100 |
| adoption | 42/100 |
| production | 70/100 |
| usefulness | 90/100 |
| integration | 62/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 400/100 |

---

<sub>🔭 Discovered 2026-06-30 · [View on GitHub](https://github.com/claudioemmanuel/squeez) · [← Back to Mcp](./README.md)</sub>
