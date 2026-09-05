# playcanvas/editor-mcp-server

[![Stars](https://img.shields.io/github/stars/playcanvas/editor-mcp-server?style=flat-square&color=yellow)](https://github.com/playcanvas/editor-mcp-server/stargazers) [![Forks](https://img.shields.io/github/forks/playcanvas/editor-mcp-server?style=flat-square&color=blue)](https://github.com/playcanvas/editor-mcp-server/network) [![Language](https://img.shields.io/badge/lang-TypeScript-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-67%2F100-brightgreen?style=flat-square)](#)

> MCP Server for AI automation of the PlayCanvas Editor

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 116 |
| 🍴 **Forks** | 25 |
| 💻 **Language** | TypeScript |
| 📈 **Score** | 67/100 |
| 🗓️ **Last push** | 2026-09-05 |
| 🔍 **Source** | github |

## 🏷️ Topics

`javascript` `mcp` `mcp-server` `playcanvas` `typescript` `vibe-coding` `webgl` `webgpu` `webxr`

## 🎯 Categories

MCP · Automation · Games & Graphics · Backend

## 📝 Summary

### English

**Brief Summary**  
playcanvas/editor‑mcp‑server is an open‑source MCP (Model Context Protocol) backend that lets AI assistants interact with the PlayCanvas editor and other development tools via a standardized API/SDK/CLI surface. By exposing implementation signals such as language metadata and focused tool topics, it makes it easy to plug AI agents into real‑world workflows, ship custom MCP servers, and unify integrations across the PlayCanvas ecosystem.  

**Value**  
The project turns the PlayCanvas editor from a closed UI into a programmable service, enabling AI‑driven automation (e.g., code generation, asset management, scene editing) without bespoke scraping or UI‑botting. Its protocol‑first design encourages reuse across different AI models and third‑party tools, reducing integration overhead and fostering a marketplace of AI‑powered extensions.  

**Practical Adoption Path**  
1. **Prototype** – Clone the repo, run the TypeScript server locally, and use the provided CLI/SDK to issue simple MCP calls (e.g., “create entity”, “list assets”).  
2. **Integrate** – Replace the prototype calls with your AI agent’s request handler, wiring the MCP client into your existing CI/CD or editor‑extension pipeline.  
3. **Deploy** – Containerize the server (Dockerfile is included), push to your cloud/edge environment, and configure PlayCanvas projects to point to the new MCP endpoint.  
4. **Extend** – Add custom topics or language‑metadata handlers to expose project‑specific data (e.g., proprietary asset pipelines) and publish the extended MCP server for other teams.  

**Production Readiness**  
The repository shows strong OSS health: 116 ★, 25 forks, recent commits (last updated 2026‑06‑30), active maintainers, and a TypeScript codebase with clear typing. These signals, combined with its modular API surface, make it suitable for a serious pilot in production. The remaining due‑diligence items are a final license audit, security review of the server’s network exposure, and confirmation of long‑term maintainer commitment, but no major blockers have been identified.

### Русский

**playcanvas/editor-mcp-server** — это открытый MCP‑сервер, позволяющий подключать AI‑ассистентов к реальному редактору PlayCanvas через единый протокол. Он упрощает интеграцию агентов с инструментами и данными, поддерживает запуск Model Context Protocol‑серверов и стандартизирует взаимодействие с API/SDK/CLI, что делает его идеальной базой для автоматизации рабочих процессов в игровых и визуальных проектах. Проект активно поддерживается (обновления до 30 июня 2026 г., 116 звёзд, 25 форков), написан на TypeScript и готов к пилотному использованию в продакшене после окончательной проверки лицензии и безопасности.

### 中文

**PlayCanvas 编辑器 MCP 服务器**

PlayCanvas 编辑器 MCP 服务器是一款开源项目，旨在通过标准协议连接 AI 助手到真实工具和数据。它帮助开发者通过 Model Context Protocol (MCP) 服务器实现 AI 自动化，提高开发效率。

**价值**

该项目的价值在于：

* 连接 AI 代理到工具
* 部署 MCP 服务器
* 标准化集成

**典型接入方式**

该项目支持多种接入方式，包括：

* API
* SDK
* CLI
* 语言元数据
* 专注话题

**生产可用性**

该项目的生产可用性非常高，主要原因是：

* 近期活跃度
* 良好的采用率
* 强大的生态系统信号
* 高评分 (70/100)

**注意**

虽然该项目有很高的生产可用性，但仍然需要进行最终的审查，特别是需要关注许可、安全防护和活跃维护者的风险。

## 🧭 Practical evaluation

**Value:** playcanvas/editor-mcp-server helps connect AI assistants to real tools and data through a standard protocol.

**Best use cases**

- connect AI agents to tools
- ship Model Context Protocol servers
- standardize integrations

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 116 GitHub stars
- 25 forks
- updated 2026-06-30
- primary language: TypeScript
- 9 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 35/100 |
| stars | 44/100 |
| topics | 100/100 |
| outlook | 73/100 |
| quality | 69/100 |
| recency | 80/100 |
| adoption | 42/100 |
| production | 70/100 |
| usefulness | 74/100 |
| integration | 62/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 400/100 |

---

<sub>🔭 Discovered 2026-06-30 · [View on GitHub](https://github.com/playcanvas/editor-mcp-server) · [← Back to Mcp](./README.md)</sub>
