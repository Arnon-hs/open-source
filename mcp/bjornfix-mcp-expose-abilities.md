# bjornfix/mcp-expose-abilities

[![Stars](https://img.shields.io/github/stars/bjornfix/mcp-expose-abilities?style=flat-square&color=yellow)](https://github.com/bjornfix/mcp-expose-abilities/stargazers) [![Forks](https://img.shields.io/github/forks/bjornfix/mcp-expose-abilities?style=flat-square&color=blue)](https://github.com/bjornfix/mcp-expose-abilities/network) [![Language](https://img.shields.io/badge/lang-PHP-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-69%2F100-brightgreen?style=flat-square)](#)

> Let AI agents do real WordPress work via MCP. 61 core abilities, 12 add-ons, 280+ ecosystem abilities for content, builders, SEO, security, files, and operations.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 33 |
| 🍴 **Forks** | 7 |
| 💻 **Language** | PHP |
| 📈 **Score** | 69/100 |
| 🗓️ **Last push** | 2026-09-05 |
| 🔍 **Source** | github |

## 🏷️ Topics

`agentic-ai` `ai-agents` `claude` `codex` `mcp` `model-context-protocol` `wordpress` `wordpress-ai` `wordpress-automation` `wordpress-plugin`

## 🎯 Categories

MCP · Automation · AI/ML · Security · Marketing

## 📝 Summary

### English

**Brief Summary**  
bjornfix/mcp-expose-abilities is an open‑source PHP library that publishes 61 core “abilities” (plus 12 add‑ons and 280+ community‑contributed actions) for WordPress through the Model Context Protocol (MCP). It lets AI agents invoke real WordPress functionality—content creation, page‑builder operations, SEO tweaks, security checks, file handling, and site administration—using a standard, language‑agnostic API.

**Value**  
- **Standardised AI‑to‑tool bridge** – By exposing WordPress capabilities via MCP, the project removes the need for custom adapters for each AI model, enabling any MCP‑compatible assistant (e.g., OpenAI, Anthropic, or self‑hosted LLMs) to perform concrete site‑maintenance tasks.  
- **Rich ecosystem** – With more than 340 ready‑to‑use abilities, developers can quickly prototype AI‑driven workflows such as automated post generation, bulk meta‑tag optimisation, vulnerability scans, or media library management.  
- **Extensibility** – New abilities can be added as simple PHP classes, and the library already supports plug‑in style add‑ons, making it easy to tailor the protocol to bespoke site requirements.

**Practical Adoption Path**  
1. **Prototype** – Clone the repo, run `composer install`, and spin up a local MCP server (the library includes a minimal CLI/SDK).  
2. **Integrate with an AI agent** – Configure your LLM’s tool‑use plugin to call the MCP endpoint; the agent can now request abilities like `wp.create_post` or `wp.run_seo_audit`.  
3. **Extend** – Add custom abilities for site‑specific plugins or internal APIs by implementing the `AbilityInterface`.  
4. **Deploy** – Containerise the MCP server (Dockerfile is provided) and place it behind your WordPress site’s firewall or a private network.  
5. **Monitor & Secure** – Use the built‑in logging hooks to audit calls, and restrict exposed abilities via role‑based policies.

**Production Readiness**  
- **Maturity**: Medium. The codebase is actively maintained (last commit 2026‑07‑02) and has modest community adoption (33 ★, 7 forks). It is suitable for internal tools, proof‑of‑concepts, and low‑risk automation.  
- **Dependencies**: Pure PHP with Composer; no heavyweight runtime requirements, but you should verify compatibility with your WordPress version and any security plugins.  
- **Security**: No known license or metadata issues, but you must perform a thorough security audit—especially around authentication, ability scoping, and input sanitisation—before exposing the server to the internet.  
- **Operational considerations**: Implement rate‑limiting, logging, and role‑based access controls; plan for regular updates of the underlying WordPress core and any third‑party abilities you rely on.  

In short, bjornfix/mcp-expose-abilities offers a practical, standards‑based way to let AI agents manipulate WordPress sites, with a clear path from prototype to production provided you address the usual security and maintenance checks.

### Русский

Резюме проекта bjornfix/mcp-expose-abilities:

Проект bjornfix/mcp-expose-abilities позволяет подключать искусственные интеллектовые агенты к реальным инструментам и данным через стандартный протокол. Это обеспечивает возможность автоматизации различных задач, включая содержание, строительство, SEO, безопасность файлов и операции. Проект готов к внедрению в прототипах или внутренних рабочих процессах, но требует проверки зависимостей и поддержки перед выпуском в производство.

Типовой сценарий внедрения: подключение AI-агентов к инструментам и данным для автоматизации различных задач.

Уровень готовности к production: средний (Medium), что означает, что проект может быть полезен для прототипов или внутренних рабочих процессов, но требует дополнительной проверки и поддержки перед выпуском в производство.

### 中文

**项目简介**  
bjornfix/mcp-expose-abilities 为 WordPress 提供了 61 项核心能力、12 项插件扩展以及 280+ 生态系统能力，涵盖内容编辑、页面构建、SEO、安防、文件管理和运维等场景。通过标准化的 Model Context Protocol（MCP），AI 代理可以直接调用这些能力，实现真正的 WordPress 自动化工作流。

**价值**  
- **AI 与真实工具的桥梁**：把 AI 助手与 WordPress 的实际功能、数据和插件对接，让模型不再只能生成文字，而能执行创建、更新、审计等具体操作。  
- **统一协议**：MCP 为所有能力提供统一的请求/响应结构，降低不同插件、主题或第三方服务的集成成本。  
- **生态扩展**：核心 + 插件 + 社区贡献的 350+ 能力，使得几乎所有常见的站点需求都能通过同一接口完成，提升开发效率和自动化水平。

**典型接入方式**  
1. **部署 MCP Server**：在 WordPress 环境中运行 `mcp-expose-abilities`，它会自动注册所有可用能力并暴露 HTTP/JSON（或 gRPC）端点。  
2. **AI 代理调用**：在你的 AI 应用（如 OpenAI、Claude、Gemini）中配置 MCP 的 endpoint 与认证信息，使用标准的 `invokeAbility` 请求调用具体能力（如 `create_post`, `run_seo_audit` 等）。  
3. **SDK/CLI 辅助**：项目提供 PHP SDK 与 CLI 工具，方便在本地脚本或 CI/CD 流程中直接调用能力，亦可通过 OpenAPI 规范生成其他语言的客户端。  
4. **插件/主题集成**：如果已有自定义插件，只需在插件代码中实现 `MCP\AbilityInterface` 并注册，即可即时在 AI 侧可用。

**生产可用性**  
- **成熟度**：目前评分 72/100，适合原型、内部工具或受控生产环境。核心能力稳定，社区贡献的能力质量参差，需要自行审计。  
- **依赖与维护**：基于 PHP，依赖 WordPress 核心与部分常用插件；建议在生产前锁定依赖版本并开启自动安全扫描。  
- **安全与合规**：项目本身未发现重大元数据泄露风险，但仍需审查许可证（MIT）与代码安全审计，尤其是涉及文件系统和用户权限的能力。  
- **运维建议**：  
  - 将 MCP Server 部署在受限的容器或子站点中，使用 HTTPS 与 API Token 鉴权。  
  - 配置速率限制与日志审计，防止滥用。  
  - 定期同步上游更新（当前最新提交 2026‑07‑02），并监控 GitHub Star/Fork 动向以评估社区活跃度。  

总体而言，bjornfix/mcp-expose-abilities 为将 AI 代理与 WordPress 实际业务深度结合提供了一个可扩展、标准化的入口，适合在验证概念后逐步推进到正式生产环境。

## 🧭 Practical evaluation

**Value:** bjornfix/mcp-expose-abilities helps connect AI assistants to real tools and data through a standard protocol.

**Best use cases**

- connect AI agents to tools
- ship Model Context Protocol servers
- standardize integrations

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** Medium: useful for prototypes or internal workflows, with dependency and maintenance checks before production.

**Quality signals**

- 33 GitHub stars
- 7 forks
- updated 2026-07-02
- primary language: PHP
- 10 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 23/100 |
| stars | 33/100 |
| topics | 100/100 |
| outlook | 73/100 |
| quality | 63/100 |
| recency | 80/100 |
| adoption | 30/100 |
| production | 68/100 |
| usefulness | 90/100 |
| integration | 62/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 500/100 |

---

<sub>🔭 Discovered 2026-07-02 · [View on GitHub](https://github.com/bjornfix/mcp-expose-abilities) · [← Back to Mcp](./README.md)</sub>
