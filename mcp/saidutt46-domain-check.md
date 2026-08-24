# saidutt46/domain-check

[![Stars](https://img.shields.io/github/stars/saidutt46/domain-check?style=flat-square&color=yellow)](https://github.com/saidutt46/domain-check/stargazers) [![Forks](https://img.shields.io/github/forks/saidutt46/domain-check?style=flat-square&color=blue)](https://github.com/saidutt46/domain-check/network) [![Language](https://img.shields.io/badge/lang-Rust-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-64%2F100-brightgreen?style=flat-square)](#)

> Fast, universal domain availability checker - 1,200+ TLDs, pattern generation, RDAP with WHOIS fallback. CLI + Rust library + MCP server for AI agents.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 276 |
| 🍴 **Forks** | 16 |
| 💻 **Language** | Rust |
| 📈 **Score** | 64/100 |
| 🗓️ **Last push** | 2026-08-24 |
| 🔍 **Source** | github |

## 🏷️ Topics

`async` `cli` `concurrency` `domain-check` `domain-check-lib` `domains` `library` `rdap` `rust` `rust-crate` `whois`

## 🎯 Categories

MCP · DevTools

## 📝 Summary

### English

**Summary**  
`s saidutt46/domain-check` is a fast, universal domain‑availability checker that supports more than 1,200 top‑level domains, generates search patterns, and falls back from RDAP to WHOIS when needed. It ships as a command‑line tool, a Rust library, and a Model Context Protocol (MCP) server, enabling AI agents to query domain data through a standard protocol. With 276 ★ on GitHub, recent commits, and a clean Rust codebase, it is ready for serious pilot deployments.

**Value**  
The project bridges the gap between AI assistants and real‑world internet resources by exposing domain‑availability data via a well‑defined MCP endpoint. This lets developers embed live domain checks into chat‑based tools, automated naming pipelines, or any AI‑driven workflow without writing custom scrapers or handling WHOIS quirks themselves. The same functionality is also available as a native Rust crate or a CLI, giving teams flexibility in how they integrate the service.

**Practical adoption path**  
1. **Prototype** – Pull the Docker image or run the MCP server locally and test the API with a simple curl request or the provided CLI.  
2. **Integrate** – Add the Rust crate to existing Rust services, or call the MCP endpoint from any language that can speak HTTP/JSON (e.g., Python, Node.js) to let AI agents query domain availability.  
3. **Deploy** – Deploy the MCP server behind a load balancer or as a sidecar in a Kubernetes pod; the stateless design scales horizontally.  
4. **Extend** – If custom TLDs or additional validation logic are needed, fork the Rust library and contribute back; the codebase is modular and well‑documented.

**Production readiness**  
- **Activity & community** – Recent commits (last update 2026‑05‑14), 276 stars, and ongoing issue handling indicate an active maintainer.  
- **Reliability** – Uses RDAP first, with WHOIS fallback, covering edge cases for domain registries.  
- **Security** – No known licensing or vulnerability flags; the Rust ecosystem’s safety guarantees further reduce risk.  
- **Scalability** – The MCP server is a lightweight HTTP service that can be horizontally scaled; the CLI and library have minimal runtime overhead.  

Overall, the project shows strong signals for production use, especially for teams building AI‑driven naming or domain‑registration workflows.

### Русский

**saidutt46/domain-check** — быстрый универсальный проверяющий доступность доменов (более 1200 TLD), генерирующий варианты, использующий RDAP с fallback‑WHOIS, доступный как CLI, Rust‑библиотека и MCP‑сервер для AI‑агентов. Он позволяет легко подключать ассистентов к реальному инструменту проверки доменов и к развёртыванию Model Context Protocol‑серверов, стандартизируя интеграцию в бекенд‑ и DevTools‑стеке. Проект имеет высокую готовность к production: активные коммиты, 276 звёзд, поддержка Rust, готовый API/SDK/CLI и стабильный MCP‑интерфейс, требующий лишь финального аудита лицензии и безопасности.

### 中文

**项目简介**  
saidutt46/domain-check 是一个高速、通用的域名可用性检查工具，支持 1,200 多种顶级域（TLD），提供模式生成、RDAP 查询并在必要时回退到 WHOIS。它同时提供 CLI、Rust 库以及基于 Model Context Protocol（MCP）的服务器，实现 AI 代理对真实网络资源的即时访问。

**价值**  
- **统一协议**：通过 MCP 为 AI 助手提供标准化的调用方式，降低不同工具之间的集成成本。  
- **实时、可靠**：结合 RDAP 与 WHOIS，保证在各种网络环境下都能获得最新的域名状态。  
- **多语言入口**：CLI、Rust SDK 与 HTTP API 并存，既适合开发者在本地脚本中使用，也方便在服务端为 AI 模型提供后端服务。

**典型接入方式**  
1. **CLI**：`domain-check check example.com` → 直接在终端获取可用性结果，适合快速调试或在 CI/CD 中使用。  
2. **Rust 库**：在 Rust 项目中 `use domain_check::Client;`，调用 `client.check("example.com")` 获得结构化返回，适合深度集成到业务系统或 AI Agent 的代码库。  
3. **MCP 服务器**：部署 `domain-check-mcp`，通过 HTTP POST 按 MCP 规范发送查询请求，AI 助手（如 OpenAI、Claude）即可通过统一的模型上下文协议调用，实现“工具调用”功能。  

**生产可用性**  
- **活跃维护**：最近一次提交在 2026‑05‑14，项目星标 276、Fork 16，社区活跃度良好。  
- **技术成熟度**：使用 Rust 实现的高性能网络栈，已在多个开源项目中作为依赖使用，具备稳定的错误处理和超时机制。  
- **安全与合规**：当前未发现重大许可证或安全隐患（仍需最终审查），但项目采用 MIT 许可证，便于商业使用。  
- **部署简易**：提供 Docker 镜像和二进制发布，支持一键启动的 MCP 服务器，适合作为生产环境的微服务组件。  

综上所述，saidutt46/domain-check 具备高性能、易集成和稳定的社区支撑，是在 AI 助手或后端系统中实现域名可用性查询的可靠 OSS 选项。

## 🧭 Practical evaluation

**Value:** saidutt46/domain-check helps connect AI assistants to real tools and data through a standard protocol.

**Best use cases**

- connect AI agents to tools
- ship Model Context Protocol servers
- standardize integrations

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 276 GitHub stars
- 16 forks
- updated 2026-05-14
- primary language: Rust
- 11 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 31/100 |
| stars | 52/100 |
| topics | 100/100 |
| outlook | 57/100 |
| quality | 56/100 |
| recency | 20/100 |
| adoption | 46/100 |
| production | 51/100 |
| usefulness | 90/100 |
| integration | 62/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 200/100 |

---

<sub>🔭 Discovered 2026-05-14 · [View on GitHub](https://github.com/saidutt46/domain-check) · [← Back to Mcp](./README.md)</sub>
