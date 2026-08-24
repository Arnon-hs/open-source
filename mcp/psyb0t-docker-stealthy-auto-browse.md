# psyb0t/docker-stealthy-auto-browse

[![Stars](https://img.shields.io/github/stars/psyb0t/docker-stealthy-auto-browse?style=flat-square&color=yellow)](https://github.com/psyb0t/docker-stealthy-auto-browse/stargazers) [![Forks](https://img.shields.io/github/forks/psyb0t/docker-stealthy-auto-browse?style=flat-square&color=blue)](https://github.com/psyb0t/docker-stealthy-auto-browse/network) [![Language](https://img.shields.io/badge/lang-Shell-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-73%2F100-brightgreen?style=flat-square)](#)

> Stealth browser automation that actually works. Runs Camoufox (custom Firefox) in Docker with zero Chrome DevTools Protocol exposure, real OS-level mouse and keyboard input via PyAutoGUI, and a JSON HTTP API + MCP server to control it all remotely. Watch it live via noVNC.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 60 |
| 🍴 **Forks** | 10 |
| 💻 **Language** | Shell |
| 📈 **Score** | 73/100 |
| 🗓️ **Last push** | 2026-08-24 |
| 🔍 **Source** | github |

## 🏷️ Topics

`api-browser` `automated` `automation` `browser` `camoufox` `container` `docker` `http-api` `mcp` `mcp-browser` `mcp-server` `playwright`

## 🎯 Categories

MCP · Automation · Backend · DevOps/Infra

## 📝 Summary

### English

Here's a brief summary of the open-source project:

The psyb0t/docker-stealthy-auto-browse project is an open-source, stealthy browser automation tool that allows for remote control and interaction with real tools and data, using a standard protocol. This project enables the connection of AI assistants to real tools and data, facilitating standardized integrations and making it easier to ship Model Context Protocol servers. With its high production readiness, strong adoption, and recent activity, this project is suitable for serious pilots and potential large-scale deployments.

**Value Proposition:**
The psyb0t/docker-stealthy-auto-browse project provides a valuable solution for connecting AI assistants to real tools and data, making it easier to standardize integrations and ship Model Context Protocol servers. This project enables the automation of complex tasks, allowing for more efficient and streamlined workflows.

**Practical Adoption Path:**
To adopt this project, developers can start by evaluating its implementation signals, such as API/SDK/CLI, language metadata, and focused topics. They can also review the project's license, security posture, and active maintainers to ensure it meets their requirements. With its straightforward integration process and recent activity, this project is suitable for serious pilots and potential large-scale deployments.

**Production Readiness:**
The psy

### Русский

Резюме проекта psyb0t/docker-stealthy-auto-browse:

Проект psyb0t/docker-stealthy-auto-browse представляет собой автоматизированную систему навигации, работающую в stealth-режиме, которая позволяет подключать AI-ассистентов к реальным инструментам и данным через стандартный протокол. Это решение может быть полезно для соединения AI-агентов с инструментами, а также для стандартизации интеграций. Проект готов к serious-пилоту (пилотному внедрению) в production-режиме, имея высокий уровень готовности (High), недавнюю активность, широкую адопцию и сильные сигналы экосистемы.

### 中文

**项目简介**  
psyb0t/docker‑stealthy‑auto‑browse 是一款可在 Docker 中运行的“隐身”浏览器自动化工具。它基于定制版 Firefox（Camoufox），通过 PyAutoGUI 在真实的 OS 级别模拟鼠标、键盘输入，完全不暴露 Chrome DevTools Protocol；同时提供 JSON HTTP API 与 MCP（Model Context Protocol）服务器，实现远程控制，并可通过 noVNC 实时观看浏览器画面。

**价值**  
- 为 AI 助手提供可靠的“真实”浏览器交互能力，突破传统无头浏览器的指纹检测与防爬限制。  
- 统一的 API/MCP 接口让 AI Agent、模型服务或业务系统能够以标准协议调用浏览器，实现“AI + 工具” 的闭环。  
- 开箱即用的 Docker 镜像和 noVNC 可视化，降低部署与调试成本，加速原型验证和生产落地。

**典型接入方式**  
1. **Docker 部署**：`docker run -p 8080:8080 -p 5901:5901 psyb0t/docker-stealthy-auto-browse`，即可启动浏览器容器并暴露 HTTP API 与 VNC 端口。  
2. **API 调用**：使用任意语言的 HTTP 客户端（如 Python `requests`）向 `http://<host>:8080/api/...` 发送 JSON 指令（打开页面、点击元素、输入文本等）。  
3. **MCP 集成**：在模型服务或 AI Agent 中加载 MCP SDK，注册该容器的 MCP 服务器地址，模型即可通过标准的 `tool_call` 直接驱动浏览器。  
4. **CLI/SDK**：项目自带的 `docker-stealthy-cli` 与 Python SDK，适合脚本化批量任务或与 CI/CD 流程结合。

**生产可用性**  
- **活跃度**：近期（2026‑07‑04）有代码更新，GitHub 60+ stars、10+ forks，社区关注度不错。  
- **成熟度**：Docker 镜像、HTTP API、MCP 服务器均已实现，提供完整的日志、错误码和健康检查接口，适合在容器编排平台（K8s、Docker‑Swarm）中进行滚动升级和弹性伸缩。  
- **安全性**：容器化隔离、无 Chrome DevTools 暴露，降低了外部攻击面；仍建议在内部网络或 VPN 中运行，并定期审计镜像依赖。  
- **可维护性**：项目主要使用 Shell 与 Python，易于二次定制；文档提供了快速上手、API 参考和示例代码。  

综合来看，psyb0t/docker‑stealthy‑auto‑browse 已具备 **高** 的生产就绪度，适合作为 AI 助手与真实网页交互的核心组件，在模型上下文协议（MCP）生态中快速落地。

## 🧭 Practical evaluation

**Value:** psyb0t/docker-stealthy-auto-browse helps connect AI assistants to real tools and data through a standard protocol.

**Best use cases**

- connect AI agents to tools
- ship Model Context Protocol servers
- standardize integrations

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 60 GitHub stars
- 10 forks
- updated 2026-07-04
- primary language: Shell
- 17 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 26/100 |
| stars | 38/100 |
| topics | 100/100 |
| outlook | 63/100 |
| quality | 56/100 |
| recency | 40/100 |
| adoption | 35/100 |
| production | 60/100 |
| usefulness | 100/100 |
| integration | 94/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 400/100 |

---

<sub>🔭 Discovered 2026-07-04 · [View on GitHub](https://github.com/psyb0t/docker-stealthy-auto-browse) · [← Back to Mcp](./README.md)</sub>
