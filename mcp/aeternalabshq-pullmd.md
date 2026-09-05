# AeternaLabsHQ/pullmd

[![Stars](https://img.shields.io/github/stars/AeternaLabsHQ/pullmd?style=flat-square&color=yellow)](https://github.com/AeternaLabsHQ/pullmd/stargazers) [![Forks](https://img.shields.io/github/forks/AeternaLabsHQ/pullmd?style=flat-square&color=blue)](https://github.com/AeternaLabsHQ/pullmd/network) [![Language](https://img.shields.io/badge/lang-JavaScript-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-63%2F100-brightgreen?style=flat-square)](#)

> Self-hosted URL-to-Markdown service for humans and AI agents. PWA + REST + MCP + Claude Code skill, with Reddit support and refreshable share links.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 137 |
| 🍴 **Forks** | 9 |
| 💻 **Language** | JavaScript |
| 📈 **Score** | 63/100 |
| 🗓️ **Last push** | 2026-09-05 |
| 🔍 **Source** | github |

## 🏷️ Topics

_no topics_

## 🎯 Categories

MCP · AI/ML · Documents

## 📝 Summary

### English

**Brief Summary (2‑3 sentences)**  
PullMD is a self‑hosted service that converts any URL into clean Markdown, exposing the result via a Progressive Web App, a REST API, and the Model Context Protocol (MCP) with built‑in Claude code‑skill support. It also offers Reddit‑specific handling and generates shareable, refreshable links, making it a convenient bridge between web content and both human users and AI agents.

**Value**  
- **Unified data access:** By normalising web pages to Markdown and exposing them through MCP, PullMD lets AI assistants fetch, parse, and act on real‑world information without custom scrapers.  
- **Standardised integration:** The REST and MCP endpoints follow widely‑adopted conventions, so existing tooling (e.g., LangChain, AutoGPT, Claude plugins) can plug in with minimal glue code.  
- **Human‑friendly UI:** The PWA gives non‑technical users a quick way to generate and share markdown snapshots, supporting collaborative workflows.  

**Practical Adoption Path**  
1. **Proof‑of‑concept (PoC):** Deploy the Docker image (or run the JavaScript server locally) and test the `/fetch` endpoint with a few URLs relevant to your domain.  
2. **MCP integration:** Register the PullMD server as a Model Context Protocol provider in your AI platform (e.g., Claude, OpenAI plugins) and call the `pullmd.get` skill to retrieve markdown content.  
3. **Workflow automation:** Wrap the REST calls in your existing orchestration layer (CI/CD, RPA, or internal bots) to replace ad‑hoc scraping scripts.  
4. **Scale & harden:** Add HTTPS, rate‑limiting, and persistent storage for cached markdown; optionally extend the Reddit module for community‑driven data pipelines.  

**Production Readiness**  
- **Maturity:** Medium. The project is actively maintained (last update 2026‑05‑13), has 137 stars and a modest fork count, indicating community interest but limited large‑scale validation.  
- **Strengths:** Clear API surface, PWA UI, and MCP support make it ready for internal prototypes and low‑risk production use cases.  
- **Caveats:**  
  * Verify the open‑source license compatibility with your stack.  
  * Conduct a security audit of the URL‑fetching logic (potential SSRF or malicious content).  
  * Monitor dependency health (JavaScript ecosystem) and plan for regular updates.  
- **Recommendation:** Deploy a sandbox instance for a pilot, perform the above security and dependency checks, and once stable, promote the service to production for internal tools or as a shared service for AI‑driven applications.

### Русский

**AeternaLabsHQ/pullmd** — это self‑hosted сервис, преобразующий URL‑адреса в Markdown и предоставляющий PWA, REST‑API и поддержку Model Context Protocol (MCP) с интеграцией Claude Code и Reddit; он позволяет AI‑агентам получать актуальные данные из внешних ресурсов через единый протокол. Типичный сценарий — быстрое прототипирование или внутренний воркфлоу, где AI‑ассистент запрашивает контент по ссылке, получает готовый Markdown и использует его в дальнейшей обработке; также сервис подходит для развертывания собственного MCP‑сервера и стандартизации интеграций. Готовность к production — средняя: проект уже имеет 137 звёзд, активные обновления и рабочий код на JavaScript, но перед масштабным внедрением требуется проверка лицензии, безопасности и поддерживаемости зависимостей.

### 中文

**项目简介**  
AeternaLabsHQ/pullmd 是一个自托管的 URL‑to‑Markdown 服务，面向人类和 AI 代理。它提供 PWA、REST 接口以及 Model Context Protocol（MCP）实现，并内置 Claude Code 技能、Reddit 支持和可刷新分享链接。

**价值主张**  
- **统一协议**：通过标准化的 MCP/REST 接口，让 AI 助手能够像调用本地工具一样安全、可靠地获取外部网页内容并转化为结构化的 Markdown。  
- **加速集成**：开发者只需部署一个服务，即可为多个 AI 模型或内部工具提供统一的数据入口，省去各自实现爬取、清洗的工作。  
- **人机协同**：PWA 前端让普通用户也能直接使用该服务，生成的 Markdown 可即时在聊天、文档或代码编辑器中复用，提升人机交互效率。

**典型接入方式**  
1. **快速原型**：在本地或云服务器上 `docker run`（或 `npm install`）启动服务，使用 README 中的示例请求 `POST /v1/pull`，传入目标 URL，即可得到 Markdown 响应。  
2. **AI 代理集成**：在 Claude、ChatGPT 等模型的插件或自定义工具链中，配置 MCP 端点（如 `mcp://pullmd.example.com`），模型即可通过 `pull` 动作直接获取网页内容。  
3. **内部工作流**：将服务作为微服务部署在企业 K8s 集群，配合 API 网关进行鉴权，内部业务系统（如报表生成、知识库同步）调用 REST 接口实现自动化内容抓取。  

**生产可用性评估**  
- **成熟度**：已有 137 ⭐、9 fork，最近一次提交在 2026‑05‑13，代码以 JavaScript 为主，适合快速迭代。  
- **适用场景**：非常适合作为原型、内部工具或低风险的业务流程自动化；在对可靠性和 SLA 有严格要求的对外业务中仍需进行安全审计、依赖锁定和容错设计。  
- **准备度**：中等（Medium）——功能完整、文档基本可用，但仍建议在生产环境前：  
  1. 完成安全评估（依赖漏洞、输入过滤、访问控制）。  
  2. 实施监控与日志，确保服务异常可快速定位。  
  3. 通过小规模 PoC 验证与现有系统的兼容性后，再逐步扩大使用范围。  

总体而言，pullmd 为 AI 与真实网络资源之间搭建了一个简洁、可自托管的桥梁，适合作为原型验证或内部自动化的核心组件，经过适当的安全和运维加固后即可投入生产使用。

## 🧭 Practical evaluation

**Value:** AeternaLabsHQ/pullmd helps connect AI assistants to real tools and data through a standard protocol.

**Best use cases**

- connect AI agents to tools
- ship Model Context Protocol servers
- standardize integrations

**Integration notes:** Looks feasible to evaluate, but integration should start with a small proof of concept and README check.

**Production readiness:** Medium: useful for prototypes or internal workflows, with dependency and maintenance checks before production.

**Quality signals**

- 137 GitHub stars
- 9 forks
- updated 2026-05-13
- primary language: JavaScript

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 25/100 |
| stars | 46/100 |
| topics | 0/100 |
| outlook | 66/100 |
| quality | 53/100 |
| recency | 80/100 |
| adoption | 40/100 |
| production | 62/100 |
| usefulness | 90/100 |
| integration | 46/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 300/100 |

---

<sub>🔭 Discovered 2026-05-13 · [View on GitHub](https://github.com/AeternaLabsHQ/pullmd) · [← Back to Mcp](./README.md)</sub>
