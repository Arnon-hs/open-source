# use-novamira/novamira

[![Stars](https://img.shields.io/github/stars/use-novamira/novamira?style=flat-square&color=yellow)](https://github.com/use-novamira/novamira/stargazers) [![Forks](https://img.shields.io/github/forks/use-novamira/novamira?style=flat-square&color=blue)](https://github.com/use-novamira/novamira/network) [![Language](https://img.shields.io/badge/lang-PHP-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-61%2F100-brightgreen?style=flat-square)](#)

> MCP server that gives AI agents full access to WordPress through PHP execution and filesystem operations

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 296 |
| 🍴 **Forks** | 44 |
| 💻 **Language** | PHP |
| 📈 **Score** | 61/100 |
| 🗓️ **Last push** | 2026-09-05 |
| 🔍 **Source** | github |

## 🏷️ Topics

_no topics_

## 🎯 Categories

MCP

## 📝 Summary

### English

**Brief Summary**  
Novamira is an open‑source MCP (Model Context Protocol) server written in PHP that lets AI agents interact directly with a WordPress site—executing arbitrary PHP code and performing filesystem operations. By exposing WordPress as a first‑class tool through a standard protocol, it enables AI assistants to read, write, and manage site content programmatically.

**Value Proposition**  
- **Tool‑enabled AI** – Moves AI assistants beyond text‑only prompts, giving them concrete read/write access to a live WordPress installation.  
- **Standardised integration** – Implements the Model Context Protocol, so the same client code can be reused across different MCP servers and tooling ecosystems.  
- **Rapid prototyping** – Developers can quickly prototype AI‑driven content creation, automated plugin management, or custom workflow automation without building bespoke WordPress APIs.

**Practical Adoption Path**  
1. **Proof‑of‑Concept** – Clone the repo, follow the README to spin up a local MCP server against a test WordPress instance. Verify basic commands (e.g., `list_posts`, `create_page`).  
2. **Security Hardening** – Restrict PHP execution to a sandboxed environment (e.g., Docker, `open_basedir`, or PHP’s `disable_functions`) and limit filesystem scope to the WordPress directory.  
3. **Integration** – Connect your AI model (e.g., OpenAI, Anthropic) using an MCP client library, register the Novamira endpoint, and map desired actions to model prompts.  
4. **Iterate & Extend** – Add custom MCP actions for site‑specific plugins or data pipelines, then move the setup to a staging environment for broader testing.  

**Production Readiness**  
- **Maturity** – Medium. The project has a respectable community signal (≈300 stars, 44 forks) and recent activity (updated 2026‑05‑13), making it suitable for internal prototypes or low‑risk production workloads.  
- **Considerations before full rollout**  
  * **Security** – Unrestricted PHP execution is powerful but risky; enforce strict sandboxing, audit allowed functions, and monitor logs.  
  * **License & Maintenance** – Verify the repository’s license compatibility with your stack and confirm that maintainers are responsive to security issues.  
  * **Dependency Management** – Keep PHP and WordPress versions aligned, and pin MCP client libraries to known‑good releases.  

In short, Novamira offers a compelling way to give AI agents actionable control over WordPress via a standardized protocol. Start with a small, sandboxed proof‑of‑concept, harden the execution environment, and then scale to production once security and maintenance concerns are addressed.

### Русский

**use-novamira/novamira** — это MCP‑сервер, позволяющий AI‑агентам полностью управлять WordPress через исполнение PHP‑кода и операции с файловой системой. Типичный сценарий — быстрое подключение интеллектуального помощника к реальному инструменту: запускаете небольшое proof‑of‑concept, проверяете README, а затем используете сервер как Model Context Protocol (MCP) шлюз для автоматизации контент‑менеджмента или интеграций. Готовность к production — средняя: проект уже стабилен и популярен (296 звёзд, активные обновления), но перед развёртыванием в продакшн требуется проверка лицензии, безопасности и зависимости.

### 中文

**项目简介（2‑3 句）**  
`use-novamira/novamira` 是一个 MCP（Model Context Protocol）服务器，实现了通过 PHP 代码执行和文件系统操作，让 AI 代理能够完整、实时地访问和操控 WordPress 实例。它提供统一的协议层，帮助开发者把聊天机器人、自动化助手等 AI 模型直接连接到真实的 WordPress 环境中。

**价值**  
- **桥接 AI 与真实工具**：把 AI 助手从“语言模型”提升为可以直接读写 WordPress 数据、调用插件 API 的实际工具，从而大幅提升自动化和内容生成的实用性。  
- **标准化集成**：遵循 MCP 协议，统一了 AI 与后端系统的交互方式，降低了每次对接新工具时的重复工作量。  
- **快速原型**：只需启动一个 PHP 服务器，即可让任何支持 MCP 的模型（如 OpenAI、Claude 等）即刻拥有 WordPress 操作能力，加速业务验证和内部工作流自动化。

**典型接入方式**  
1. **部署服务器**：在能够访问目标 WordPress 实例的机器上运行 `novamira`（PHP 7.4+），配置好 `novamira.yaml`（包括 WordPress 路径、数据库凭证等）。  
2. **启动 MCP 服务**：`php -S 0.0.0.0:8080 -t public/`（或使用 Docker 镜像），服务会监听 MCP 请求。  
3. **在 AI 平台注册**：在 OpenAI、Anthropic、LangChain 等平台的 “tool” 或 “custom endpoint” 配置中填入服务器的 URL 与协议描述（OpenAPI/JSON‑RPC），并授权相应的 API 密钥。  
4. **调用示例**：在 Prompt 中使用 `tool:wordpress.create_post`、`tool:wordpress.update_option` 等已注册的工具函数，AI 即可通过 MCP 调用对应的 PHP 脚本完成实际操作。  

**生产可用性**  
- **成熟度**：GitHub 296 星、44 Fork，最近一次提交于 2026‑05‑13，代码活跃度尚可。适合作为 **原型/内部工具** 使用，已具备基本功能和文档。  
- **依赖与运维**：依赖 PHP 环境及 WordPress 文件系统，需自行审计插件安全性、数据库访问权限以及代码执行的沙箱化（防止任意代码注入）。  
- **风险**：暂无明显的元数据泄露风险，但仍需确认许可证兼容性、长期维护者活跃度以及对 PHP 执行的安全加固（如限制执行目录、使用 SELinux/AppArmor）。  
- **推荐做法**：先在测试环境做小规模 PoC，验证 AI 调用链路、权限控制和错误处理后，再逐步推广到生产；配合代码审计、日志监控和速率限制，以确保安全可靠。  

总体而言，`use-novamira/novamira` 为 AI 与 WordPress 的深度集成提供了一个快速、标准化的入口，适合需要将语言模型转化为实际业务工具的团队在原型阶段快速验证，并在完成安全加固后逐步向生产环境迁移。

## 🧭 Practical evaluation

**Value:** use-novamira/novamira helps connect AI assistants to real tools and data through a standard protocol.

**Best use cases**

- connect AI agents to tools
- ship Model Context Protocol servers
- standardize integrations

**Integration notes:** Looks feasible to evaluate, but integration should start with a small proof of concept and README check.

**Production readiness:** Medium: useful for prototypes or internal workflows, with dependency and maintenance checks before production.

**Quality signals**

- 296 GitHub stars
- 44 forks
- updated 2026-05-13
- primary language: PHP

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 41/100 |
| stars | 53/100 |
| topics | 0/100 |
| outlook | 65/100 |
| quality | 57/100 |
| recency | 80/100 |
| adoption | 49/100 |
| production | 63/100 |
| usefulness | 74/100 |
| integration | 46/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 100/100 |

---

<sub>🔭 Discovered 2026-05-13 · [View on GitHub](https://github.com/use-novamira/novamira) · [← Back to Mcp](./README.md)</sub>
