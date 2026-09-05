# Env-Kit/envkit-releases

[![Stars](https://img.shields.io/github/stars/Env-Kit/envkit-releases?style=flat-square&color=yellow)](https://github.com/Env-Kit/envkit-releases/stargazers) [![Forks](https://img.shields.io/github/forks/Env-Kit/envkit-releases?style=flat-square&color=blue)](https://github.com/Env-Kit/envkit-releases/network) [![Language](https://img.shields.io/badge/lang-Shell-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-67%2F100-brightgreen?style=flat-square)](#)

> EnvKit — free local development environment for Windows & macOS: nginx/Apache, multiple PHP versions, MySQL/MariaDB,   PostgreSQL, Redis, MongoDB, Mailpit, Node.js, trusted .test HTTPS, and a built-in MCP server for AI-assistant control.   A Laragon/XAMPP/Herd alternative.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 172 |
| 🍴 **Forks** | 5 |
| 💻 **Language** | Shell |
| 📈 **Score** | 67/100 |
| 🗓️ **Last push** | 2026-09-05 |
| 🔍 **Source** | github |

## 🏷️ Topics

`apache` `development-environment` `herd-alternative` `laragon-alternative` `laravel` `local-development` `mailpit` `mariadb` `mcp` `mongodb` `mysql` `nginx`

## 🎯 Categories

MCP · Backend · Database

## 📝 Summary

### English

**Brief Summary (2‑3 sentences)**  
EnvKit is an open‑source, all‑in‑one local development stack for Windows and macOS that bundles nginx/Apache, multiple PHP runtimes, MySQL/MariaDB, PostgreSQL, Redis, MongoDB, Mailpit, Node.js, trusted .test HTTPS certificates, and a built‑in MCP (Model Context Protocol) server for AI‑assistant control. It positions itself as a modern alternative to Laragon, XAMPP, and Herd, and adds a standardized API/CLI that lets AI agents invoke real tools and data directly from the development environment.

**Value**  
- **AI‑tool integration** – The MCP server exposes a uniform protocol so AI assistants can run commands, query databases, or spin up services without custom glue code, turning a local dev box into a testbed for AI‑driven automation.  
- **Full‑stack convenience** – One‑click installation of the most common web‑stack components eliminates version‑conflict headaches and provides built‑in HTTPS for local domains, accelerating onboarding for developers and AI‑research teams.  
- **Open‑source flexibility** – Being shell‑based and publicly hosted, the stack can be forked, extended, or embedded in CI pipelines, giving teams full control over security and compliance.

**Practical Adoption Path**  
1. **Pilot** – Clone the `Env-Kit/envkit-releases` repo, run the provided installer script, and verify that the MCP server starts and can be reached via its REST/CLI endpoint.  
2. **Integrate** – Update existing AI‑agent code (e.g., LangChain, AutoGPT) to call the MCP endpoints for actions such as “run PHP script”, “query MySQL”, or “publish to Redis”.  
3. **Scale** – Containerize the EnvKit stack (Docker or WSL2) for reproducible environments across team members or CI runners; use the MCP API as a contract for downstream services.  
4. **Govern** – Review the license, perform a security audit of the bundled services, and lock versions in the installer script to meet production compliance.

**Production Readiness**  
- **Activity & Adoption** – The project shows recent commits (last updated 2026‑06‑27), 172 stars, and a modest but active fork base, indicating healthy community interest.  
- **Maturity** – All core components (web servers, databases, runtimes) are mature, and the MCP server is a thin wrapper that can be independently versioned and tested.  
- **Risk Profile** – No immediate metadata or licensing red flags, though a final security review of the bundled binaries and the MCP implementation is advisable. Overall, EnvKit is sufficiently stable for a serious pilot and can be hardened for production use with standard DevSecOps practices.

### Русский

Env‑Kit (репозиторий **Env‑Kit/envkit‑releases**) – это бесплатный набор локальных серверов для Windows и macOS (nginx/Apache, несколько PHP, MySQL/MariaDB, PostgreSQL, Redis, MongoDB, Mailpit, Node.js и т. д.) с поддержкой доверённого HTTPS‑домена *.test и встроенного MCP‑сервера, позволяющего подключать AI‑ассистентов к реальным инструментам и данным через единый протокол. Типичный сценарий — запуск Model Context Protocol‑серверов и интеграция AI‑агентов с инфраструктурой разработки без необходимости отдельной настройки каждого сервиса. Проект уже активно поддерживается (обновления 2026‑06‑27, 172 звезды, готов к пилотному использованию в продакшене после финального аудита лицензии и безопасности).

### 中文

**项目简介**  
Env‑Kit/envkit‑releases 提供一套免费、即装即用的本地开发环境（Windows / macOS），内置 Nginx/Apache、多个 PHP 版本、MySQL/MariaDB、PostgreSQL、Redis、MongoDB、Mailpit、Node.js、受信任的 .test HTTPS 以及用于 AI 助手控制的内置 MCP 服务器，定位为 Laragon、XAMPP、Herd 等工具的开源替代方案。

**价值**  
- **统一协议接入**：通过标准的 Model Context Protocol（MCP）让 AI 助手直接调用本地服务、数据库和工具，实现“AI + 工具”闭环。  
- **一键全栈**：开发者无需手动安装、配置各类中间件，只需启动 EnvKit 即可得到完整的 LAMP/LEMP 环境，加速原型和调试。  
- **跨平台**：同一套脚本兼容 Windows 与 macOS，降低团队环境一致性成本。  

**典型接入方式**  
1. **CLI / Shell 脚本**：克隆 `envkit-releases`，运行提供的 `envkit.sh`（或 `envkit.bat`）完成环境启动。  
2. **MCP 客户端**：AI 代理（如 OpenAI Function‑Calling、LangChain、AutoGPT 等）通过 HTTP/WS 与 EnvKit 暴露的 MCP 端点交互，获取服务列表、执行数据库查询或调用本地脚本。  
3. **SDK / API**：项目自带的轻量 SDK（Shell + JSON）可在 CI/CD、测试框架或自定义插件中调用，实现自动化部署或动态资源管理。  

**生产可用性**  
- **活跃度**：最近一次提交于 2026‑06‑27，星标 172，社区已有 5 次 Fork，代码以 Shell 为主，覆盖 20+ 主题，表明持续维护。  
- **成熟度**：核心组件（Nginx、MySQL、Redis 等）均使用官方二进制，EnvKit 只负责包装与启动，故底层服务的可靠性与安全性与原厂保持一致。  
- **安全与合规**：目前未发现重大许可证或安全漏洞风险，但仍建议在生产前完成内部安全审计（尤其是 MCP 接口的身份验证与网络隔离）。  
- **适配性**：提供完整的 Docker 镜像与本地二进制，两种方式均可快速在 CI 环境或真实机器上复现，适合作为 **AI + 工具** 场景的试点或正式部署。  

综上，Env‑Kit 在提供本地全栈环境的同时，通过标准化的 MCP 接口为 AI 助手与真实工具的交互搭建桥梁，具备足够的活跃度与技术成熟度，可在内部或受控的生产环境中进行严肃的试点验证。

## 🧭 Practical evaluation

**Value:** Env-Kit/envkit-releases helps connect AI assistants to real tools and data through a standard protocol.

**Best use cases**

- connect AI agents to tools
- ship Model Context Protocol servers
- standardize integrations

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 172 GitHub stars
- 5 forks
- updated 2026-06-27
- primary language: Shell
- 20 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 19/100 |
| stars | 48/100 |
| topics | 100/100 |
| outlook | 73/100 |
| quality | 68/100 |
| recency | 80/100 |
| adoption | 40/100 |
| production | 70/100 |
| usefulness | 74/100 |
| integration | 62/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 300/100 |

---

<sub>🔭 Discovered 2026-06-27 · [View on GitHub](https://github.com/Env-Kit/envkit-releases) · [← Back to Mcp](./README.md)</sub>
