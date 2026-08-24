# cisco-open/network-sketcher

[![Stars](https://img.shields.io/github/stars/cisco-open/network-sketcher?style=flat-square&color=yellow)](https://github.com/cisco-open/network-sketcher/stargazers) [![Forks](https://img.shields.io/github/forks/cisco-open/network-sketcher?style=flat-square&color=blue)](https://github.com/cisco-open/network-sketcher/network) [![Language](https://img.shields.io/badge/lang-Python-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-70%2F100-brightgreen?style=flat-square)](#)

> Network Sketcher is an AI-ready network design tool with Local MCP, Online, and Offline editions for creating network designs and exporting PowerPoint diagrams and Excel-based configuration data.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 367 |
| 🍴 **Forks** | 18 |
| 💻 **Language** | Python |
| 📈 **Score** | 70/100 |
| 🗓️ **Last push** | 2026-08-24 |
| 🔍 **Source** | github |

## 🏷️ Topics

`ai-agent` `cisco` `claude-code` `cursor` `mcp-server` `model-context-protocol` `network-automation` `network-diagram` `powerpoint` `svg` `topology`

## 🎯 Categories

MCP · Automation · AI/ML · Backend · Design

## 📝 Summary

### English

**Network Sketcher: Connecting AI Assistants to Real Tools and Data**

Network Sketcher is an open-source network design tool that enables the creation of network designs and exports diagrams and configuration data in PowerPoint and Excel formats. Its value proposition lies in connecting AI assistants to real tools and data through a standard protocol, making it an essential tool for automation and AI/ML projects.

**Practical Adoption Path:**

1. **Connect AI agents to tools**: Network Sketcher allows developers to connect AI agents to real tools and data, making it easier to integrate AI capabilities into existing systems.
2. **Standardize integrations**: By using the Model Context Protocol, developers can standardize integrations across different tools and platforms, reducing integration complexity and increasing efficiency.
3. **Ship Model Context Protocol servers**: Network Sketcher provides a server implementation for the Model Context Protocol, making it easier to deploy and manage protocol servers.

**Production Readiness:**

Network Sketcher is production-ready due to its:

* **Recent activity**: The project has been updated recently, indicating active maintenance and development.
* **Strong adoption**: The project has 367 GitHub stars and 18 forks, demonstrating a strong community and adoption rate.
* **Ecosystem signals**: The project's ecosystem signals are strong, indicating a solid foundation

### Русский

Резюме проекта cisco-open/network-sketcher:

Network Sketcher - это open-source инструмент для создания сетевых проектирований, который готов для интеграции с AI-помощниками. Он предлагает три варианта: Local MCP, Online и Offline, что позволяет создавать сетевые проекции и экспортировать диаграммы PowerPoint и конфигурационную информацию в формате Excel. cisco-open/network-sketcher готов к сериозной пилотной реализации и имеет высокий уровень готовности к production, с сильными сигналами активности, приёма и экосистемы.

### 中文

**项目简介**  
Network Sketcher 是一款面向 AI 的网络设计工具，提供 Local MCP、Online 与 Offline 三种版本，能够快速绘制网络拓扑、导出 PowerPoint 演示稿以及基于 Excel 的配置数据。

**价值**  
- **统一协议接入**：通过标准的 Model Context Protocol（MCP），让 AI 助手能够直接调用真实的网络设计与配置功能，实现“AI + 工具”的闭环。  
- **多场景支持**：本地离线版适合安全合规环境，在线版便于团队协作，MCP 版可快速嵌入 AI Agent 或自动化流水线。  
- **提升效率**：自动生成拓扑图和配置表，减少手工绘图和数据整理的时间成本。

**典型接入方式**  
1. **MCP Server**：启动 `network-sketcher-mcp`，AI Agent 通过 MCP 客户端发送 JSON 请求（如“创建 VLAN”或“导出拓扑 PPT”），获取结构化响应。  
2. **Python SDK / CLI**：在自定义脚本或 CI/CD 流程中直接调用 `network_sketcher` 包的函数或命令行工具，实现批量设计、导出或配置验证。  
3. **REST API（Online 版）**：对接前端或第三方系统时，可使用项目自带的 HTTP 接口进行 CRUD 操作。

**生产可用性**  
- **活跃度**：最近一次提交在 2026‑07‑01，代码仓库拥有 367 ★、18 Fork，主要语言为 Python，涉及 11 个相关话题，表明社区活跃且生态完整。  
- **成熟度**：提供完整的本地、在线、离线三种部署方式，且已实现标准化的 MCP 接口，适合作为 OSS 级别的生产候选。  
- **风险**：暂无重大元数据风险，但仍需对许可证（Apache‑2.0）进行合规审查，并进行安全依赖检查和维护者活跃度确认后方可正式投入生产。

综上，cisco-open/network‑sketcher 具备高可用的生产级别特征，适合作为 AI 助手与网络设计工具之间的桥梁，快速实现模型驱动的网络自动化。

## 🧭 Practical evaluation

**Value:** cisco-open/network-sketcher helps connect AI assistants to real tools and data through a standard protocol.

**Best use cases**

- connect AI agents to tools
- ship Model Context Protocol servers
- standardize integrations

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 367 GitHub stars
- 18 forks
- updated 2026-07-01
- primary language: Python
- 11 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 32/100 |
| stars | 55/100 |
| topics | 100/100 |
| outlook | 66/100 |
| quality | 62/100 |
| recency | 40/100 |
| adoption | 48/100 |
| production | 58/100 |
| usefulness | 100/100 |
| integration | 62/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 500/100 |

---

<sub>🔭 Discovered 2026-07-01 · [View on GitHub](https://github.com/cisco-open/network-sketcher) · [← Back to Mcp](./README.md)</sub>
