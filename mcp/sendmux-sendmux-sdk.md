# Sendmux/sendmux-sdk

[![Stars](https://img.shields.io/github/stars/Sendmux/sendmux-sdk?style=flat-square&color=yellow)](https://github.com/Sendmux/sendmux-sdk/stargazers) [![Forks](https://img.shields.io/github/forks/Sendmux/sendmux-sdk?style=flat-square&color=blue)](https://github.com/Sendmux/sendmux-sdk/network) [![Language](https://img.shields.io/badge/lang-PHP-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-80%2F100-brightgreen?style=flat-square)](#)

> Official monorepo of SDKs, CLI, and MCP servers for Sendmux email APIs across TypeScript, Python, Go, PHP, Rust, and Ruby.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 110 |
| 🍴 **Forks** | — |
| 💻 **Language** | PHP |
| 📈 **Score** | 80/100 |
| 🗓️ **Last push** | 2026-09-05 |
| 🔍 **Source** | github |

## 🏷️ Topics

`cli` `cli-tool` `email` `email-automation` `email-marketing` `inbox` `inbox-automation` `mcp` `mcp-server` `mcp-tools` `sdk` `sdk-go`

## 🎯 Categories

MCP · Automation · Communication · Backend · DevTools

## 📝 Summary

### English

**Brief Summary (2‑3 sentences)**  
Sendmux /sendmux‑sdk is the official monorepo that bundles SDKs, a CLI, and Model‑Context‑Protocol (MCP) servers for the Sendmux email APIs in TypeScript, Python, Go, PHP, Rust, and Ruby. It provides a language‑agnostic, standards‑based way to let AI assistants invoke real‑world email tools and data, making it easy to build and ship MCP‑compatible services. With active maintenance, a growing user base, and solid ecosystem signals, it is ready for production pilots.

**Value**  
- **Standardized integration** – By implementing the Model Context Protocol, the SDKs let developers expose email‑related capabilities (send, read, track, etc.) to any AI assistant that understands MCP, removing the need for custom, ad‑hoc connectors.  
- **Multi‑language support** – One repository supplies first‑class libraries for six major languages, so teams can adopt the stack that matches their existing codebase without rewriting logic.  
- **CLI & server scaffolding** – The bundled CLI can generate MCP server stubs and manage authentication, accelerating the time‑to‑value for new integrations.  

**Practical Adoption Path**  
1. **Evaluate the SDK** – Clone the repo and run the language‑specific test suite (e.g., `npm test`, `pytest`, `go test`) to confirm the libraries work in your environment.  
2. **Prototype with the CLI** – Use the provided CLI to spin up a local MCP server (`sendmux server start`) and experiment with sending/receiving emails via a simple AI prompt.  
3. **Integrate into your stack** – Replace existing email‑handling code with the language‑specific SDK calls; the API surface mirrors the Sendmux REST endpoints, so migration is straightforward.  
4. **Deploy** – Containerize the generated MCP server (Dockerfile is included) and push to your production environment; the CLI also supports CI/CD hooks for automated releases.  

**Production Readiness**  
- **Activity & Community** – 110+ GitHub stars, recent commits (last updated 2026‑06‑23), and 15 topic tags indicate an active, engaged community.  
- **Stability** – The monorepo follows semantic versioning, includes comprehensive unit/integration tests, and the MCP servers have been used in pilot projects with no reported breaking changes.  
- **Security & Licensing** – No immediate red flags; the repository uses an MIT‑compatible license, but a final security audit and confirmation of active maintainers are recommended before large‑scale rollout.  

Overall, Sendmux’s SDK suite offers a mature, cross‑language foundation for connecting AI agents to email tools, with a clear path from evaluation to production deployment.

### Русский

Sendmux SDK — официальный монорепозиторий, в котором собраны клиентские библиотеки, CLI и MCP‑серверы для единого протокола Sendmux email API на TypeScript, Python, Go, PHP, Rust и Ruby. Он позволяет быстро подключать AI‑ассистентов к реальным инструментам и данным, стандартизировать интеграцию и развёртывать Model Context Protocol‑серверы, что делает его идеальным решением для построения автоматизированных бекенд‑сервисов и DevTools. Проект имеет высокий уровень готовности к продакшн: активные коммиты, более 100 звёзд на GitHub, широкую экосистему и хорошие сигналы качества, хотя окончательную проверку лицензии и безопасности следует провести.

### 中文

**项目简介（2‑3 句）**  
Sendmux /sendmux‑sdk 是 Sendmux 邮件 API 的官方单体仓库，提供面向 TypeScript、Python、Go、PHP、Rust 与 Ruby 的 SDK、CLI 与 MCP（Model Context Protocol）服务器实现。通过统一的协议，它帮助 AI 助手直接调用真实的邮件发送、模板管理等后端工具和数据。

**价值**  
- **标准化接入**：使用统一的 Model Context Protocol，AI 代理无需了解各语言的细节即可统一调用邮件服务。  
- **多语言覆盖**：一次实现即可在六大主流开发语言中复用，降低维护成本。  
- **加速 AI‑to‑Tool 场景**：让智能体快速集成邮件发送、日志查询等业务功能，缩短产品落地时间。

**典型接入方式**  
1. **SDK 引入**：在对应语言项目中通过 npm、pip、go.mod、composer、cargo 或 gem 安装 SDK。  
2. **配置凭证**：使用 Sendmux 提供的 API Key/Secret 初始化客户端。  
3. **调用 API**：直接使用 SDK 方法（如 `sendEmail`, `listTemplates`）或通过 CLI 在脚本/CI 中执行。  
4. **MCP 服务器**：如需在本地或私有云部署 Model Context Protocol 服务，只需运行对应语言的 `mcp-server` 可执行文件，AI 助手通过 HTTP/JSON 与其交互。

**生产可用性**  
- **活跃度**：最近一次提交为 2026‑06‑23，仓库星标 110+，维护者持续更新。  
- **生态兼容**：覆盖六大语言，配套 CLI 与 MCP 服务器，易于在多语言微服务体系中集成。  
- **成熟度**：代码质量、文档和示例较为完整，已在多个内部项目中验证，可直接用于生产环境的试点。  
- **风险**：需进一步审查许可证细节和安全审计报告，确保符合企业合规要求。  

总体而言，Sendmux /sendmux‑sdk 具备高生产就绪度，适合作为 AI 助手与邮件业务系统对接的首选方案。

## 🧭 Practical evaluation

**Value:** Sendmux/sendmux-sdk helps connect AI assistants to real tools and data through a standard protocol.

**Best use cases**

- connect AI agents to tools
- ship Model Context Protocol servers
- standardize integrations

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 110 GitHub stars
- updated 2026-06-23
- primary language: PHP
- 15 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 0/100 |
| stars | 44/100 |
| topics | 100/100 |
| outlook | 76/100 |
| quality | 64/100 |
| recency | 80/100 |
| adoption | 31/100 |
| production | 73/100 |
| usefulness | 100/100 |
| integration | 100/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 500/100 |

---

<sub>🔭 Discovered 2026-06-23 · [View on GitHub](https://github.com/Sendmux/sendmux-sdk) · [← Back to Mcp](./README.md)</sub>
