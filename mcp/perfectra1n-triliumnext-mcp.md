# perfectra1n/triliumnext-mcp

[![Stars](https://img.shields.io/github/stars/perfectra1n/triliumnext-mcp?style=flat-square&color=yellow)](https://github.com/perfectra1n/triliumnext-mcp/stargazers) [![Forks](https://img.shields.io/github/forks/perfectra1n/triliumnext-mcp?style=flat-square&color=blue)](https://github.com/perfectra1n/triliumnext-mcp/network) [![Language](https://img.shields.io/badge/lang-TypeScript-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-62%2F100-brightgreen?style=flat-square)](#)

> An MCP server for interacting with a Trilium instance

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 33 |
| 🍴 **Forks** | 8 |
| 💻 **Language** | TypeScript |
| 📈 **Score** | 62/100 |
| 🗓️ **Last push** | 2026-05-12 |
| 🔍 **Source** | github |

## 🏷️ Topics

`chatgpt` `claude` `mcp` `notes` `trilium`

## 🎯 Categories

MCP · Backend

## 📝 Summary

### English

**Brief Summary (2‑3 sentences)**  
perfectra1n/triliumnext‑mcp is a TypeScript‑based MCP (Model Context Protocol) server that lets AI assistants communicate with a Trilium notes instance via a standard, language‑agnostic API. By exposing a clean REST/SDK/CLI surface, it enables developers to plug AI agents into real‑world knowledge bases and tooling without writing custom connectors. The project is modestly popular (33 ★, 8 forks) and was refreshed as recently as 2026‑05‑12.  

**Value**  
- **Standardised integration** – Implements the MCP spec, so the same client code can talk to any MCP‑compatible backend, reducing lock‑in and simplifying multi‑tool AI workflows.  
- **Rapid prototyping** – Provides ready‑made endpoints for creating, reading, updating, and searching Trilium notes, turning a powerful personal knowledge graph into an AI‑accessible data source in minutes.  
- **Extensibility** – Because it ships both an HTTP API and a TypeScript SDK, developers can embed the server in existing Node.js services or call it from other languages via the generated OpenAPI client.  

**Practical Adoption Path**  
1. **Evaluate** – Clone the repo, run `npm install && npm run dev`, and point the server at a local Trilium instance using the provided configuration file.  
2. **Prototype** – Use the bundled SDK or generated OpenAPI client to build a simple AI agent that queries notes or writes new entries, confirming that the MCP contract matches your use case.  
3. **Secure & Harden** – Add authentication (e.g., JWT or API keys), enable TLS, and run static analysis (npm audit, Snyk) to address any disclosed vulnerabilities.  
4. **Deploy** – Containerise the server (Dockerfile is included), push to your registry, and orchestrate it alongside your AI service (K8s, Docker‑Compose, or serverless).  
5. **Monitor & Scale** – Hook into existing observability stacks (Prometheus metrics, log aggregation) and configure horizontal scaling if request volume grows.  

**Production Readiness**  
- **Maturity** – Medium. The codebase is functional and actively maintained, but it lacks formal CI/CD pipelines, extensive test coverage, and production‑grade documentation.  
- **Dependencies** – Relies on a typical Node/TypeScript stack; ensure compatible versions of Trilium and any security patches are kept up‑to‑date.  
- **Operational Considerations** – Before production, perform a thorough security review (license compliance, dependency vulnerabilities, authentication/authorization), add health‑check endpoints, and implement graceful shutdown handling.  

Overall, triliumnext‑mcp is well‑suited for internal tools, prototypes, or as a stepping stone toward a fully‑featured MCP ecosystem, provided the necessary hardening steps are taken before mission‑critical deployment.

### Русский

perfectra1n/triliumnext-mcp — это сервер MCP, реализованный на TypeScript, который позволяет AI‑ассистентам взаимодействовать с экземпляром Trilium через единый протокол Model Context Protocol. Типичный сценарий — подключение AI‑агентов к Trilium как к инструменту для хранения и поиска заметок, что упрощает создание прототипов и внутренних workflow‑интеграций. Готовность к production — средняя: проект уже стабильно работает и имеет базовую документацию, но перед развертыванием в продакшн требуется проверка лицензии, безопасности и поддержка зависимостей.

### 中文

**项目简介**  
perfectra1n/triliumnext-mcp 是一个基于 Model Context Protocol（MCP）的服务器，实现了对 Trilium 知识库的统一交互接口，帮助 AI 助手以标准化方式读取、写入和搜索笔记数据。

**价值**  
- **统一协议**：通过 MCP 将 AI 代理与 Trilium 连接，避免为每个工具单独实现专属 API。  
- **快速集成**：使用已有的 API/SDK/CLI 即可让 AI 直接调用 Trilium 的功能，适用于原型、内部工具以及面向用户的 AI 产品。  
- **可扩展**：遵循标准协议后，后续可以无缝对接其他 MCP 兼容服务，实现工具链的统一治理。

**典型接入方式**  
1. **作为 MCP 服务器运行**：在 Node.js 环境中启动 `npm start`，服务器会监听指定端口并暴露 MCP 接口。  
2. **使用官方 SDK**：项目提供 TypeScript/JavaScript SDK，直接在 AI 代理代码中 `import { TriliumMCPClient } from 'triliumnext-mcp'`，调用 `client.getNote(id)`、`client.createNote(payload)` 等方法。  
3. **CLI 调用**：通过 `triliumnext-mcp-cli` 可在脚本或 CI 中执行 CRUD 操作，适合不想引入完整 SDK 的场景。  

**生产可用性**  
- **成熟度**：目前处于 **Medium** 级别，适合原型验证或内部工作流使用。  
- **依赖与维护**：项目基于 TypeScript，依赖较少且更新活跃（截至 2026‑05‑12），但仍需自行审查许可证、潜在安全漏洞以及维护者响应速度后再用于生产。  
- **质量指标**：33 ⭐、8 🍴、5 个主题标签，代码结构清晰，文档提供了基本的部署与使用指南。  

总体而言，perfectra1n/triliumnext-mcp 为 AI 与 Trilium 的集成提供了一个标准化、易上手的桥梁，适合作为原型或内部系统的后端服务；在正式生产环境使用前建议进行安全审计和运维监控。

## 🧭 Practical evaluation

**Value:** perfectra1n/triliumnext-mcp helps connect AI assistants to real tools and data through a standard protocol.

**Best use cases**

- connect AI agents to tools
- ship Model Context Protocol servers
- standardize integrations

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** Medium: useful for prototypes or internal workflows, with dependency and maintenance checks before production.

**Quality signals**

- 33 GitHub stars
- 8 forks
- updated 2026-05-12
- primary language: TypeScript
- 5 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 24/100 |
| stars | 33/100 |
| topics | 63/100 |
| outlook | 70/100 |
| quality | 63/100 |
| recency | 100/100 |
| adoption | 30/100 |
| production | 73/100 |
| usefulness | 58/100 |
| integration | 62/100 |
| sourceTrust | 100/100 |

---

<sub>🔭 Discovered 2026-05-12 · [View on GitHub](https://github.com/perfectra1n/triliumnext-mcp) · [← Back to Mcp](./README.md)</sub>
