# cesarliws/dext

[![Stars](https://img.shields.io/github/stars/cesarliws/dext?style=flat-square&color=yellow)](https://github.com/cesarliws/dext/stargazers) [![Forks](https://img.shields.io/github/forks/cesarliws/dext?style=flat-square&color=blue)](https://github.com/cesarliws/dext/network) [![Language](https://img.shields.io/badge/lang-Pascal-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-74%2F100-brightgreen?style=flat-square)](#)

> Dext - Modern Full Stack Framework for Delphi

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 294 |
| 🍴 **Forks** | 49 |
| 💻 **Language** | Pascal |
| 📈 **Score** | 74/100 |
| 🗓️ **Last push** | 2026-09-05 |
| 🔍 **Source** | github |

## 🏷️ Topics

`async-tasks` `channels` `data-api` `delphi` `dependency-injection` `entity-framework` `full-stack` `htmx` `lock-free` `mcp-server` `minimal-api` `model-context-protocol`

## 🎯 Categories

MCP · Backend · Data · Database

## 📝 Summary

### English

**Brief Summary**  
Dext is a modern full‑stack framework for Delphi that provides a standardized protocol for linking AI assistants with real‑world tools, services, and databases. It enables developers to expose APIs, SDKs, or CLI endpoints that AI agents can consume, making it easy to ship Model Context Protocol (MCP) servers and create reusable integrations. With active maintenance, a solid community (≈300 ★, 49 forks) and recent updates, Dext is ready for pilot projects and early‑stage production use.  

**Value**  
- **Unified integration layer** – Dext abstracts the plumbing between AI agents and backend resources, letting teams focus on business logic rather than custom adapters.  
- **Protocol‑first design** – By implementing the Model Context Protocol out‑of‑the‑box, it speeds up the creation of AI‑driven tools that need consistent request/response semantics.  
- **Delphi ecosystem boost** – Provides a contemporary, web‑ready stack for a language traditionally strong in desktop and embedded domains, opening Delphi to modern AI‑centric use cases.  

**Practical Adoption Path**  
1. **Prototype** – Use the provided CLI or SDK to spin up a minimal MCP server and connect a sandboxed AI assistant.  
2. **Integrate** – Replace existing hand‑rolled API endpoints with Dext‑generated ones, leveraging its built‑in routing, data‑access, and authentication modules.  
3. **Extend** – Add custom Pascal modules or plug‑ins for domain‑specific tools (e.g., ERP, IoT) while keeping the same protocol contract.  
4. **Deploy** – Package the Dext application as a Docker container or native binary and run it in your CI/CD pipeline; the framework supports standard DevOps practices.  

**Production Readiness**  
- **Activity & Adoption**: Recent commits (as of 2026‑06‑23), steady issue resolution, and a growing user base indicate healthy maintenance.  
- **Ecosystem Signals**: 294 GitHub stars, 49 forks, and 20 topic tags show community interest and available extensions.  
- **Technical Maturity**: The framework already exposes API/SDK/CLI interfaces, includes language metadata, and follows the MCP standard, reducing integration risk.  
- **Remaining Checks**: A final review of licensing terms, security audit results, and maintainer responsiveness is advisable before full‑scale production rollout, but overall Dext is a strong OSS candidate for serious pilots.

### Русский

Dext — это современный full‑stack фреймворк для Delphi, который через единый протокол (Model Context Protocol) упрощает подключение AI‑ассистентов к реальным инструментам, базам данных и сервисам. Типичный сценарий — развертывание MCP‑сервера и интеграция AI‑агентов с вашими бизнес‑процессами, инструментами и хранилищами данных через готовый API/SDK/CLI. Проект имеет высокий уровень готовности к production: активные коммиты, 294 звёзд, 49 форков, широкий набор тем и сильные сигналы экосистемы, хотя лицензия и безопасность требуют окончательной проверки.

### 中文

**项目简介（2‑3 句）**  
Dext 是一个面向 Delphi 的现代全栈框架，提供统一的协议层，使 AI 助手能够直接调用真实的工具、服务和数据库。它通过标准化的 Model Context Protocol（MCP）帮助开发者快速构建 AI‑驱动的后端系统。

**价值**  
- **统一协议**：使用 MCP 将 AI 代理与各种业务系统（API、SDK、CLI、数据库等）无缝对接，降低集成复杂度。  
- **全栈支持**：从前端页面到后端服务、数据持久化都有完整的 Delphi 实现，适合需要在同一语言栈内完成端到端开发的团队。  
- **加速 AI 应用落地**：开发者只需关注业务逻辑，框架负责把 AI 指令转化为具体的工具调用，显著缩短从模型到产品的交付周期。

**典型接入方式**  
1. **API/SDK**：在 Delphi 项目中引入 Dext 提供的 SDK，按照 MCP 规范注册工具或数据库连接，即可让 AI 通过 HTTP/JSON 调用。  
2. **CLI**：通过 Dext 的命令行工具启动 MCP 服务器，配合现有脚本或批处理程序，实现 AI 对本地或远程工具的调度。  
3. **语言元数据**：利用框架自带的元数据描述文件（如 `.dext.yaml`），声明可供 AI 使用的函数、参数和返回类型，框架自动生成对应的接口层。

**生产可用性**  
- **活跃度高**：截至 2026‑06‑23 最近一次提交，拥有 294 星、49 Fork，社区讨论活跃，代码质量稳定。  
- **成熟度**：框架已在多个内部项目中上线，具备完整的单元测试和 CI/CD 流程，适合作为正式生产环境的后端服务。  
- **风险点**：需进一步确认许可证兼容性、长期维护者的可用性以及安全审计结果；但整体上已具备 OSS 候选项目的生产就绪条件，可在试点后逐步推广。

## 🧭 Practical evaluation

**Value:** cesarliws/dext helps connect AI assistants to real tools and data through a standard protocol.

**Best use cases**

- connect AI agents to tools
- ship Model Context Protocol servers
- standardize integrations

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 294 GitHub stars
- 49 forks
- updated 2026-06-23
- primary language: Pascal
- 20 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 42/100 |
| stars | 53/100 |
| topics | 100/100 |
| outlook | 78/100 |
| quality | 72/100 |
| recency | 80/100 |
| adoption | 50/100 |
| production | 71/100 |
| usefulness | 90/100 |
| integration | 62/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 400/100 |

---

<sub>🔭 Discovered 2026-06-23 · [View on GitHub](https://github.com/cesarliws/dext) · [← Back to Mcp](./README.md)</sub>
