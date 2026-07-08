# JUNKDOGE-JOE/after-effects-mcp

[![Stars](https://img.shields.io/github/stars/JUNKDOGE-JOE/after-effects-mcp?style=flat-square&color=yellow)](https://github.com/JUNKDOGE-JOE/after-effects-mcp/stargazers) [![Forks](https://img.shields.io/github/forks/JUNKDOGE-JOE/after-effects-mcp?style=flat-square&color=blue)](https://github.com/JUNKDOGE-JOE/after-effects-mcp/network) [![Language](https://img.shields.io/badge/lang-JavaScript-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-77%2F100-brightgreen?style=flat-square)](#)

> Agent-driven Adobe After Effects automation. MCP server + CEP plugin enabling Codex/Cursor/Claude Code to drive AE through 30 ae.* tools.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 24 |
| 🍴 **Forks** | 2 |
| 💻 **Language** | JavaScript |
| 📈 **Score** | 77/100 |
| 🗓️ **Last push** | 2026-07-08 |
| 🔍 **Source** | github |

## 🏷️ Topics

`adobe-after-effects` `agent` `cep` `extendscript` `mcp` `model-context-protocol` `motion-graphics` `python`

## 🎯 Categories

MCP · Automation · AI/ML · Backend

## 📝 Summary

### English

**Brief summary**  
JUNKDOGE‑JOE/after‑effects‑mcp is an open‑source stack that lets AI agents (Codex, Cursor, Claude, etc.) control Adobe After Effects via a Model Context Protocol (MCP) server and a CEP plugin, exposing 30 native `ae.*` commands. By standardising the “AI‑to‑tool” interface, it makes it possible to drive real‑world video‑editing workflows with code‑generated instructions.

**Value**  
The project bridges the gap between large‑language‑model assistants and production‑grade creative software, turning natural‑language prompts into concrete After Effects actions without manual scripting. This enables rapid prototyping of AI‑driven motion‑graphics pipelines, reduces the need for custom ExtendScript code, and creates a reusable protocol that other tools can adopt.

**Practical adoption path**  

1. **Prototype** – Clone the repo, run the MCP server (Node.js) locally, and install the CEP plugin into After Effects. Use the provided CLI or REST endpoint to send simple `ae.*` commands (e.g., create a composition, add a layer).  
2. **Integrate** – Wrap the MCP calls in your preferred AI‑agent framework (e.g., LangChain, AutoGPT). Map high‑level intents (“add a lower‑third with fade‑in”) to the corresponding `ae.*` calls.  
3. **Scale** – Deploy the MCP server as a containerized microservice (Docker/K8s) and expose it to multiple agents or a CI/CD pipeline that generates video assets automatically.  
4. **Standardise** – Share the MCP schema with other teams or open‑source projects, allowing different AI models to speak the same “After Effects” language.

**Production readiness**  
The repository shows strong recent activity (last commit 2026‑07‑08), a modest but growing community (24 stars, 2 forks), and clear API/CLI entry points, indicating a mature codebase for pilot projects. While the license and security posture still need a final audit, the core components (MCP server, CEP plugin) are stable, documented, and written in JavaScript, making integration straightforward for teams already using Node.js and After Effects. Consequently, it is suitable for a serious production trial, especially for internal automation or proof‑of‑concept deployments.

### Русский

Резюме проекта JUNKDOGE-JOE/after-effects-mcp:

Проект JUNKDOGE-JOE/after-effects-mcp представляет собой набор инструментов для автоматизации Adobe After Effects с помощью агентов-ассистентов. Он позволяет соединять AI-ассистентов с реальными инструментами и данными через стандартный протокол, что делает его пригодным для различных применений.

Типовой сценарий внедрения: проект может быть использован для подключения AI-ассистентов к инструментам, развертывания серверов Model Context Protocol и стандартизации интеграций.

Проект готов к производственной эксплуатации на высоком уровне, поскольку он демонстрирует recent активность, широкое распространение и сильные сигналы экосистемы, что делает его подходящим кандидатом для серьезной пилотной версии.

### 中文

**简短介绍**
JUNKDOGE-JOE/after-effects-mcp 是一个开源项目，旨在通过 Agent 驱动的方式自动化 Adobe After Effects。它提供 MCP 服务器 + CEP 插件，支持通过 30 个 ae.* 工具与 Codex/Cursor/Claude Code 进行交互。

**价值**
JUNKDOGE-JOE/after-effects-mcp 帮助连接 AI 辅助器到真实的工具和数据，通过标准协议实现。

**典型接入方式**
连接 AI 代理到工具，部署 Model Context Protocol 服务器，标准化集成。

**生产可用性**
该项目的生产可用性为高，最近有活跃的更新，采用率和生态系统信号都很强，足以进行严肃的试验。

## 🧭 Practical evaluation

**Value:** JUNKDOGE-JOE/after-effects-mcp helps connect AI assistants to real tools and data through a standard protocol.

**Best use cases**

- connect AI agents to tools
- ship Model Context Protocol servers
- standardize integrations

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 24 GitHub stars
- 2 forks
- updated 2026-07-08
- primary language: JavaScript
- 8 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 12/100 |
| stars | 30/100 |
| topics | 100/100 |
| outlook | 81/100 |
| quality | 66/100 |
| recency | 100/100 |
| adoption | 25/100 |
| production | 76/100 |
| usefulness | 100/100 |
| integration | 78/100 |
| sourceTrust | 100/100 |

---

<sub>🔭 Discovered 2026-07-08 · [View on GitHub](https://github.com/JUNKDOGE-JOE/after-effects-mcp) · [← Back to Mcp](./README.md)</sub>
