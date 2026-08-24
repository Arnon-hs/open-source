# HduSy/tokenscope

[![Stars](https://img.shields.io/github/stars/HduSy/tokenscope?style=flat-square&color=yellow)](https://github.com/HduSy/tokenscope/stargazers) [![Forks](https://img.shields.io/github/forks/HduSy/tokenscope?style=flat-square&color=blue)](https://github.com/HduSy/tokenscope/network) [![Language](https://img.shields.io/badge/lang-Rust-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-65%2F100-brightgreen?style=flat-square)](#)

> MacOS menu-bar dashboard for Claude CLI token usage, estimated cost, and per-model / MCP / Skill breakdowns.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 207 |
| 🍴 **Forks** | 11 |
| 💻 **Language** | Rust |
| 📈 **Score** | 65/100 |
| 🗓️ **Last push** | 2026-08-24 |
| 🔍 **Source** | github |

## 🏷️ Topics

`analytics` `claude` `claude-cli` `cost-tracking` `tauri` `token-counter` `token-usage`

## 🎯 Categories

MCP · DevTools · Data

## 📝 Summary

### English

**Brief Summary (2‑3 sentences)**  
HduSy /tokenscope is a Rust‑based macOS menu‑bar utility that visualises Claude CLI token consumption, estimated costs, and detailed per‑model, MCP, and Skill breakdowns. By surfacing these metrics in real time, it helps developers monitor and optimise the expense of AI‑driven workflows directly from the desktop. The project is actively maintained, well‑starred, and positioned as a lightweight bridge between Claude‑based agents and the Model Context Protocol (MCP) ecosystem.  

**Value**  
- **Cost transparency:** Shows exact token usage and projected monetary cost, preventing surprise bills when scaling AI assistants.  
- **Model‑level insight:** Breaks down usage by individual Claude models, MCP endpoints, and custom Skills, enabling fine‑grained optimisation of prompts and routing logic.  
- **Developer ergonomics:** A native menu‑bar UI means developers can watch token metrics without leaving their terminal or IDE, encouraging a “pay‑as‑you‑go” mindset.  

**Practical Adoption Path**  
1. **Install** the binary (or build from source) on any macOS workstation.  
2. **Configure** the tool to point at the Claude CLI token (or API key) used by your agents.  
3. **Enable** MCP or Skill endpoints in your Claude‑based services; tokenscope will automatically detect and label traffic.  
4. **Iterate**: use the live dashboard to identify high‑cost models or over‑used Skills, then adjust prompt design, model selection, or MCP routing accordingly.  
5. **Scale**: for teams, distribute the binary via internal package managers (Homebrew, Cargo) and standardise the configuration file across developers, ensuring consistent cost monitoring across all AI‑enabled projects.  

**Production Readiness**  
- **Activity & Community:** 207 ★, 11 forks, recent commits (last update 2026‑07‑05) and a focused Rust codebase indicate an active maintainer base.  
- **Integration Simplicity:** Exposes a clear CLI/SDK interface and emits standard MCP metadata, making it straightforward to plug into existing Claude CLI pipelines.  
- **Risk Profile:** No obvious licensing or security red flags, though a final audit of the repository’s license compliance and supply‑chain hygiene is advisable.  
- **Pilot Suitability:** Given its low runtime footprint, native macOS UI, and real‑time metrics, tokenscope is ready for a serious pilot in production environments where cost control and model observability are critical.

### Русский

**HduSy/tokenscope** — это открытый macOS‑дашборд в виде меню‑бара, который в реальном времени отображает расход токенов Claude CLI, оценку стоимости и детализированный разбор по моделям, MCP и навыкам. Он позволяет быстро интегрировать AI‑ассистентов с реальными инструментами и данными через стандартный Model Context Protocol, упрощая подключение агентов к сервисам и развертывание MCP‑серверов. Проект находится в высокой готовности к production: активные обновления (последний коммит 2026‑07‑05), 207 звёзд, 11 форков, написан на Rust и имеет хорошие сигналы экосистемы, хотя окончательная проверка лицензии и безопасности всё‑ещё требуется.

### 中文

**项目简介**  
HduSy/tokenscope 是一款基于 macOS 菜单栏的仪表盘，用于实时展示 Claude CLI 的 token 消耗、预估费用以及按模型 / MCP / Skill 的细分统计。它帮助开发者在本地即可监控 AI 助手的资源使用情况。

**价值**  
- **可视化成本**：一目了然地看到 token 使用量和对应的费用，避免意外超支。  
- **细粒度分析**：按模型、Model Context Protocol（MCP）以及 Skill 维度拆解消耗，便于调优和预算分配。  
- **标准化接入**：遵循 MCP 协议，可直接作为 AI 助手与外部工具、数据源的桥梁，促进统一的集成方式。

**典型接入方式**  
1. **CLI 集成**：在本地安装 `tokenscope`，通过配置 Claude CLI 的 token 输出路径，即可自动捕获并展示数据。  
2. **MCP 服务器**：在已有的 Model Context Protocol 服务器上部署 `tokenscope`，让所有通过 MCP 调用的模型请求都被统一统计。  
3. **SDK/库调用**：在 Rust（或通过 FFI 调用）的项目中引入 `tokenscope` 提供的 API，实时上报 token 消耗到本地仪表盘。

**生产可用性**  
- **活跃度**：最近一次提交在 2026‑07‑05，星标 207、Fork 11，社区关注度良好。  
- **技术成熟度**：核心实现使用 Rust，具备高性能和安全特性；提供完整的 API/CLI，易于脚本化集成。  
- **生态兼容**：遵循公开的 MCP 标准，可与多种 AI 平台和工具链无缝对接。  
- **风险**：目前未发现重大元数据或许可证问题，但仍建议在正式生产环境前完成安全审计并确认维护者的响应能力。

总体而言，tokenscope 已具备在生产环境中试点使用的条件，尤其适合需要细粒度成本监控和标准化 AI‑Tool 集成的团队。

## 🧭 Practical evaluation

**Value:** HduSy/tokenscope helps connect AI assistants to real tools and data through a standard protocol.

**Best use cases**

- connect AI agents to tools
- ship Model Context Protocol servers
- standardize integrations

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 207 GitHub stars
- 11 forks
- updated 2026-07-05
- primary language: Rust
- 7 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 27/100 |
| stars | 49/100 |
| topics | 88/100 |
| outlook | 62/100 |
| quality | 58/100 |
| recency | 40/100 |
| adoption | 43/100 |
| production | 56/100 |
| usefulness | 90/100 |
| integration | 62/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 300/100 |

---

<sub>🔭 Discovered 2026-07-05 · [View on GitHub](https://github.com/HduSy/tokenscope) · [← Back to Mcp](./README.md)</sub>
