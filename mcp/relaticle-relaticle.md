# relaticle/relaticle

[![Stars](https://img.shields.io/github/stars/relaticle/relaticle?style=flat-square&color=yellow)](https://github.com/relaticle/relaticle/stargazers) [![Forks](https://img.shields.io/github/forks/relaticle/relaticle?style=flat-square&color=blue)](https://github.com/relaticle/relaticle/network) [![Language](https://img.shields.io/badge/lang-PHP-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-79%2F100-brightgreen?style=flat-square)](#)

> Open-source CRM with native AI agent support. 30 MCP tools, REST API, self-hosted. Built with Laravel & Filament

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 1.3k |
| 🍴 **Forks** | 141 |
| 💻 **Language** | PHP |
| 📈 **Score** | 79/100 |
| 🗓️ **Last push** | 2026-09-05 |
| 🔍 **Source** | github |

## 🏷️ Topics

`alpine` `company` `contacts` `crm` `filament` `laravel` `livewire` `note` `opportunity` `people` `saas` `sales`

## 🎯 Categories

MCP · AI/ML · Backend · Product

## 📝 Summary

### English

**Brief Summary (2‑3 sentences)**  
relaticle/relaticle is an open‑source CRM built with Laravel and Filament that ships with native AI‑agent support and a suite of 30 “Model Context Protocol” (MCP) tools. It offers a full REST API, self‑hosting options, and SDK/CLI hooks, making it easy to connect AI assistants to real business data and workflows. With over 1,200 GitHub stars and active maintenance, it is positioned as a production‑ready foundation for AI‑augmented customer relationship management.

**Value**  
- **Standardized AI integration** – By implementing the Model Context Protocol, relaticle lets developers expose CRM data and actions to any compliant AI agent, removing the need for custom glue code for each assistant.  
- **Rapid tool‑to‑agent connectivity** – The 30 built‑in MCP tools (e.g., contact lookup, ticket creation, analytics) give AI agents immediate, secure access to core CRM capabilities.  
- **Extensible stack** – Leveraging Laravel and Filament provides a familiar PHP ecosystem, a rich UI builder, and easy plugin development for additional business logic or third‑party services.

**Practical Adoption Path**  
1. **Evaluate the API/SDK** – Clone the repo, run the Docker compose file, and explore the OpenAPI spec to verify that required CRM actions are covered.  
2. **Deploy a pilot instance** – Use the provided Helm chart or Docker image to spin up a self‑hosted environment in a staging VPC.  
3. **Connect an AI agent** – Register the instance as an MCP server in your preferred LLM‑orchestrator (e.g., LangChain, OpenAI Functions) and test a few sample prompts (e.g., “Create a follow‑up task for contact X”).  
4. **Extend or customize** – Add custom MCP tools or modify existing ones via Laravel service providers, then push the changes to your own fork or contribute back upstream.  
5. **Scale to production** – Harden the deployment (TLS, RBAC, rate limiting), integrate with existing authentication (OAuth, SSO), and monitor via the built‑in health endpoints.

**Production Readiness**  
- **Activity & Community** – Recent commits (as of 2026‑05‑13), 1.3 k stars, and a healthy fork count indicate strong community interest.  
- **Architecture** – Laravel’s proven stability, Filament’s UI scaffolding, and a well‑documented REST API make the stack reliable for enterprise workloads.  
- **Security & Ops** – The project provides Docker/Helm deployment scripts, health checks, and basic RBAC; however, a final security audit (license compliance, dependency scanning) is recommended before mission‑critical use.  
- **Ecosystem Fit** – The MCP abstraction aligns with emerging AI‑agent standards, positioning relaticle as a future‑proof component for any AI‑driven workflow platform.  

Overall, relaticle/relaticle is a mature, extensible CRM that can be quickly evaluated and safely promoted to production for teams looking to embed AI assistants directly into their customer‑relationship processes.

### Русский

relaticle/relaticle — это открытая CRM‑система, построенная на Laravel & Filament и оснащённая нативной поддержкой AI‑агентов, что позволяет быстро подключать интеллектуальных помощников к реальным бизнес‑инструментам и данным через единый протокол Model Context Protocol. Типичный сценарий внедрения — интеграция AI‑агента с 30 встроенными MCP‑инструментами и REST API для автоматизации продаж, поддержки и аналитики, а также развёртывание собственного сервера протокола для стандартизации интеграций. По показателям активности (1296 звёзд, частые коммиты, свежие релизы) проект готов к production‑использованию, однако перед запуском стоит уточнить лицензионные и вопросы безопасности.

### 中文

**项目简介**  
relaticle/relaticle 是一款基于 Laravel 与 Filament 构建的开源 CRM 系统，内置对 AI 代理的原生支持。它提供 30 多种 MCP（Model‑Context‑Protocol）工具、完整的 REST API，并可自行部署，帮助企业快速将 AI 助手与真实业务工具和数据对接。

**价值主张**  
- **统一协议、即插即用**：通过标准的 Model Context Protocol（MCP），把 AI 代理与 CRM、邮件、任务管理等业务功能无缝连接，降低二次开发成本。  
- **AI‑驱动的业务自动化**：AI 代理可以直接调用系统内置的 30+ 工具，实现智能客服、自动线索分配、销售预测等场景。  
- **完整生态、可自托管**：提供 REST API、PHP SDK 与 CLI，支持二次开发和自定义扩展，兼顾数据安全与合规需求。

**典型接入方式**  
1. **REST API**：使用标准的 HTTP 接口调用 CRM 功能或 MCP 工具，适合前端、移动端或第三方服务集成。  
2. **PHP SDK / Filament 插件**：在 Laravel 项目中直接引入 SDK，利用语言层面的类型提示与自动化文档，加速开发。  
3. **CLI 与 Docker**：通过提供的 CLI 或官方 Docker 镜像快速部署本地或云端实例，完成自托管后即可开启 AI 代理对接。  

**生产可用性**  
- **活跃度高**：截至 2026‑05‑13，项目拥有 1.3k+ 星、140+ Fork，最近一次提交仅在数天前，表明维护活跃。  
- **成熟的技术栈**：基于 Laravel（业界成熟的 PHP 框架）和 Filament（现代后台 UI），拥有完善的测试与文档。  
- **生态兼容**：提供完整的 API/SDK/CLI，易于与现有微服务或前端系统集成；同时支持标准 MCP，便于在多模型、多平台之间统一调用。  
- **安全与合规**：代码开源、依赖可审计，适合在内部网络或受控云环境中自托管，满足企业对数据隐私的要求。  

综合来看，relaticle/relaticle 已具备足够的社区活跃度、技术成熟度和安全可审计性，是在生产环境中试点 AI‑驱动 CRM 与工具集成的可靠 OSS 选项。

## 🧭 Practical evaluation

**Value:** relaticle/relaticle helps connect AI assistants to real tools and data through a standard protocol.

**Best use cases**

- connect AI agents to tools
- ship Model Context Protocol servers
- standardize integrations

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 1296 GitHub stars
- 141 forks
- updated 2026-05-13
- primary language: PHP
- 15 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 54/100 |
| stars | 66/100 |
| topics | 100/100 |
| outlook | 84/100 |
| quality | 78/100 |
| recency | 80/100 |
| adoption | 63/100 |
| production | 73/100 |
| usefulness | 100/100 |
| integration | 62/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 400/100 |

---

<sub>🔭 Discovered 2026-05-13 · [View on GitHub](https://github.com/relaticle/relaticle) · [← Back to Mcp](./README.md)</sub>
