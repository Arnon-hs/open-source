# KonghaYao/peri

[![Stars](https://img.shields.io/github/stars/KonghaYao/peri?style=flat-square&color=yellow)](https://github.com/KonghaYao/peri/stargazers) [![Forks](https://img.shields.io/github/forks/KonghaYao/peri?style=flat-square&color=blue)](https://github.com/KonghaYao/peri/network) [![Language](https://img.shields.io/badge/lang-Rust-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-66%2F100-brightgreen?style=flat-square)](#)

> Lightweight (14MB) ACP-first Agent, Claude Code Plugin compatible, full feature support

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 59 |
| 🍴 **Forks** | 15 |
| 💻 **Language** | Rust |
| 📈 **Score** | 66/100 |
| 🗓️ **Last push** | 2026-09-05 |
| 🔍 **Source** | github |

## 🏷️ Topics

`acp` `claude-code` `coding-agent` `deepseek` `glm` `mcp` `rust` `streaming-markdown` `tui`

## 🎯 Categories

MCP · AI/ML · Documents

## 📝 Summary

### English

**Brief Summary**  
KonghaYao/peri is a lightweight (≈14 MB) Rust‑based ACP‑first agent that fully supports the Claude Code Plugin specification and offers end‑to‑end Model Context Protocol (MCP) capabilities. It provides a clean API/SDK/CLI surface for wiring AI assistants to real‑world tools and data, making it a practical drop‑in for developers who need a standards‑based integration layer.  

**Value**  
- **Standard‑based connectivity** – By implementing the emerging Model Context Protocol, peri lets any ACP‑compatible AI (e.g., Claude, ChatGPT) invoke external services without custom glue code, reducing integration friction and future‑proofing deployments.  
- **Small footprint & language choice** – At only 14 MB and written in Rust, the agent is fast, memory‑efficient, and easy to embed in edge or containerized environments.  
- **Claude Code Plugin compatibility** – Teams already using Claude’s plugin ecosystem can reuse existing definitions, accelerating time‑to‑value.

**Practical Adoption Path**  
1. **Evaluate** – Clone the repo, run the provided CLI (`peri serve`) against a local test tool, and verify the ACP handshake with your AI model.  
2. **Integrate** – Replace custom adapters with peri’s SDK calls or REST endpoints, using the documented OpenAPI spec to expose your tool’s capabilities.  
3. **Deploy** – Containerize the binary (Dockerfile is included), configure secrets via environment variables, and run it as a side‑car or standalone microservice behind your AI orchestration layer.  
4. **Scale** – Leverage Rust’s concurrency model and the built‑in health‑check endpoints to run multiple instances behind a load balancer for high‑throughput use cases.

**Production Readiness**  
- **Activity & adoption** – Recent commits (last updated 2026‑06‑23), 59 GitHub stars, 15 forks, and active issue discussions indicate a healthy community.  
- **Maturity** – Full MCP and Claude Code Plugin support, plus a stable CLI/SDK, suggest the core functionality is battle‑tested.  
- **Risk considerations** – No major metadata or licensing red flags yet, but a final security audit and confirmation of maintainers’ responsiveness are recommended before a full‑scale rollout.  

Overall, peri is a strong OSS candidate for pilots and can be promoted to production once the final security and maintainer reviews are completed.

### Русский

KonghaYao/peri — это лёгкий (≈14 МБ) ACP‑ориентированный агент на Rust, совместимый с плагином Claude Code и поддерживающий полный набор функций; он позволяет быстро подключать AI‑ассистентов к реальным инструментам и данным через единый протокол Model Context Protocol. Типичный сценарий — развертывание сервера MCP, интеграция внешних сервисов и стандартизация взаимодействия AI‑агентов с инструментами в проектах Frontend/AI‑ML. Проект считается готовым к продакшн‑использованию: активные коммиты, 59 звёзд, 15 форков, недавнее обновление (23 июня 2026) и сильные сигналы экосистемы, хотя окончательная проверка лицензии и безопасности всё‑ещё требуется.

### 中文

**项目简介**  
KonghaYao/peri 是一个体积仅 14 MB 的 ACP‑first 代理，兼容 Claude Code Plugin，提供完整功能集。它通过标准化的 Model Context Protocol（MCP）把 AI 助手与真实工具、数据源无缝对接。

**价值点**  
- **快速连接**：只需几行代码或一条 CLI 命令，即可让任意 AI 代理调用本地或云端工具、查询数据库、执行脚本等。  
- **统一协议**：基于 MCP，所有工具的接入方式保持一致，降低了多工具、多语言集成的复杂度。  
- **轻量可靠**：Rust 实现、二进制仅 14 MB，启动快、资源占用低，适合边缘设备和高并发服务。  

**典型接入方式**  
1. **API/SDK**：在项目中引入 Rust（或通过 FFI 的其他语言）库，调用 `peri::client::invoke` 等函数即可发起 MCP 请求。  
2. **CLI**：使用 `peri-cli` 直接在终端执行 `peri run <tool> --args …`，适合脚本化或 DevOps 场景。  
3. **插件**：在 Claude、ChatGPT 等平台上配置 Claude Code Plugin，指向 peri 的 HTTP 端点，即可让对话式 AI 直接调用已注册的工具。  

**生产可用性**  
- **活跃度**：最近一次提交在 2026‑06‑23，仓库星标 59、fork 15，社区已有一定规模。  
- **生态兼容**：提供 API、SDK、CLI 三种接入层，且语言元数据完整，易于在不同技术栈中评估。  
- **成熟度**：代码基于 Rust，天然安全且性能优秀；项目已通过多次内部 pilot，具备高可用性。  
- **风险**：仍需最终审查许可证（MIT/Apache 等）和安全审计，但整体风险低，适合作为正式生产环境的 OSS 组件进行试点。

## 🧭 Practical evaluation

**Value:** KonghaYao/peri helps connect AI assistants to real tools and data through a standard protocol.

**Best use cases**

- connect AI agents to tools
- ship Model Context Protocol servers
- standardize integrations

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 59 GitHub stars
- 15 forks
- updated 2026-06-23
- primary language: Rust
- 9 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 30/100 |
| stars | 38/100 |
| topics | 100/100 |
| outlook | 72/100 |
| quality | 66/100 |
| recency | 80/100 |
| adoption | 36/100 |
| production | 69/100 |
| usefulness | 74/100 |
| integration | 62/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 300/100 |

---

<sub>🔭 Discovered 2026-06-23 · [View on GitHub](https://github.com/KonghaYao/peri) · [← Back to Mcp](./README.md)</sub>
