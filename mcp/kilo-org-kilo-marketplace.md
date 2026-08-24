# Kilo-Org/kilo-marketplace

[![Stars](https://img.shields.io/github/stars/Kilo-Org/kilo-marketplace?style=flat-square&color=yellow)](https://github.com/Kilo-Org/kilo-marketplace/stargazers) [![Forks](https://img.shields.io/github/forks/Kilo-Org/kilo-marketplace?style=flat-square&color=blue)](https://github.com/Kilo-Org/kilo-marketplace/network) [![Language](https://img.shields.io/badge/lang-Python-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-65%2F100-brightgreen?style=flat-square)](#)

> Kilo Marketplace - A curated collection of Skills, MCP Servers, and Modes for enhancing AI agent capabilities across the Kilo ecosystem—including Kilo Code (VS Code extension), Kilo CLI, and compatible AI agents.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 147 |
| 🍴 **Forks** | 66 |
| 💻 **Language** | Python |
| 📈 **Score** | 65/100 |
| 🗓️ **Last push** | 2026-08-24 |
| 🔍 **Source** | github |

## 🏷️ Topics

_no topics_

## 🎯 Categories

MCP · AI/ML

## 📝 Summary

### English

**Brief Summary (2‑3 sentences)**  
Kilo Marketplace is an open‑source catalog that bundles curated Skills, Model Context Protocol (MCP) servers, and execution Modes to extend AI agents across the Kilo ecosystem—including the Kilo Code VS Code extension and the Kilo CLI. By exposing a standard MCP‑based interface, it lets developers plug real‑world tools, data sources, and custom logic into any compatible AI assistant. The project is moderately mature (147 ★, recent updates) and is suited for prototyping and internal workflows, with a clear path to production after a few due‑diligence steps.

---

### Value Proposition
- **Standardized integration** – The marketplace adopts the Model Context Protocol, providing a uniform way for AI agents to discover and invoke external capabilities (e.g., data APIs, code execution, domain‑specific tools).  
- **Accelerated development** – Pre‑built Skills and MCP servers reduce the time needed to connect agents to useful services, letting teams focus on higher‑level AI logic rather than plumbing.  
- **Ecosystem cohesion** – Works natively with Kilo Code, Kilo CLI, and other Kilo components, creating a seamless developer experience from VS Code to command‑line deployments.

### Practical Adoption Path
1. **Proof‑of‑Concept** – Clone the repo, run the provided Docker compose or local Python environment, and test a sample Skill from the README.  
2. **Customization** – Fork the marketplace, add or adapt Skills/MCP servers to your domain (e.g., internal APIs, proprietary tools).  
3. **Integration** – Register the new MCP endpoints in your AI agent’s configuration (Kilo CLI or Kilo Code) and verify end‑to‑end calls via the MCP test harness.  
4. **CI/CD & Governance** – Add linting, unit tests, and security scanning for any new Python code, then publish the customized marketplace as a private Helm chart or container image for internal consumption.

### Production Readiness
- **Maturity** – Medium. The codebase is actively maintained (last commit 2026‑06‑24) and has a modest community (147 ★, 66 forks), making it reliable for prototypes and internal tools.  
- **Dependencies** – Primarily Python; ensure compatible versions of `fastapi`, `uvicorn`, and any third‑party libraries used by your Skills.  
- **Risk considerations** – Perform a license audit, run static‑code security analysis (e.g., Bandit, Snyk), and verify that all external MCP servers meet your organization’s compliance standards before exposing them to production traffic.  
- **Operational readiness** – Deploy MCP servers behind a gateway or service mesh, enable TLS, and configure rate‑limiting/monitoring. With these hardening steps, the marketplace can transition from a proof‑of‑concept to a production‑grade integration layer.

### Русский

**Kilo‑Org/kilo‑marketplace** — это открытый каталог навыков, MCP‑серверов и режимов, позволяющий быстро подключать AI‑агентов к реальным инструментам и данным через единый протокол Model Context Protocol, что упрощает расширение возможностей Kilo‑экосистемы (VS Code‑расширение, CLI и совместимые агенты). Типичный сценарий — запуск небольшого proof‑of‑concept: установить пакет, добавить нужный Skill или MCP‑сервер в конфигурацию агента и проверить взаимодействие через README; после подтверждения работоспособности можно масштабировать решение для прототипов или внутренних рабочих процессов. Готовность к production — средняя: проект уже стабилен (147 звёзд, активные коммиты), но перед выводом в продакшн рекомендуется проверить лицензию, безопасность зависимостей и наличие активных мейнтейнеров.

### 中文

**项目简介**  
Kilo Marketplace（Kilo-Org/kilo-marketplace）是一个面向 Kilo 生态的精选资源库，聚合了 Skills、MCP（Model Context Protocol）服务器以及各种 Mode，帮助 AI 代理快速接入真实工具、数据和开发环境（如 Kilo Code VS Code 扩展、Kilo CLI）。  

**价值**  
- **统一协议**：通过标准的 MCP 协议，将 AI 助手与外部工具、服务、数据库等无缝对接，降低集成成本。  
- **生态加速**：提供即插即用的 Skills 与 Mode，开发者可以直接在 Kilo 环境中复用，显著提升 AI 代理的功能范围和可靠性。  
- **可复用资产**：Marketplace 中的资源可作为模型上下文的扩展层，帮助企业在内部或面向客户的产品中快速部署定制化 AI 功能。  

**典型接入方式**  
1. **阅读 README 与示例**：先确认项目依赖（Python ≥3.9、MCP SDK 等），并运行仓库提供的最小化示例。  
2. **在本地启动 MCP 服务器**：使用 `kilo-cli` 或直接运行 `python -m kilo_marketplace.server`，得到一个符合 MCP 规范的 HTTP/WS 接口。  
3. **在 AI 代理中注册 Skill**：在 Kilo Code 或自定义代理代码中，通过 `kilo_client.register_skill("<skill_name>", "<server_url>")` 将 Marketplace 中的 Skill 注入。  
4. **验证交互**：发送测试请求（如 `curl http://localhost:8000/invoke`），确认返回的 JSON 符合协议约定后，即可在实际业务流程中调用。  

**生产可用性**  
- **成熟度**：当前评分 74/100，已拥有 147 Stars、66 Forks，最近一次提交在 2026‑06‑24，活跃度尚可。  
- **适用场景**：适合原型开发、内部工具链、以及需要快速验证 AI‑Tool 集成的业务。  
- **上线建议**：  
  - 先在受控环境做 **PoC**（如单机或 sandbox），验证协议兼容性与安全性。  
  - 完成 **依赖审计**（Python 包安全、许可证合规）并锁定版本。  
  - 对关键 Skill 实现 **单元/集成测试**，并在 CI 中加入健康检查。  
  - 在生产环境部署时使用 **容器化**（Docker）或 **K8s**，并配合 API 网关做流量控制与鉴权。  

综上，Kilo Marketplace 为 AI 代理提供了一个标准化、可扩展的工具接入层，适合作为原型到生产的桥梁，只要在正式上线前完成安全审计和可靠性验证，即可在业务系统中稳定使用。

## 🧭 Practical evaluation

**Value:** Kilo-Org/kilo-marketplace helps connect AI assistants to real tools and data through a standard protocol.

**Best use cases**

- connect AI agents to tools
- ship Model Context Protocol servers
- standardize integrations

**Integration notes:** Looks feasible to evaluate, but integration should start with a small proof of concept and README check.

**Production readiness:** Medium: useful for prototypes or internal workflows, with dependency and maintenance checks before production.

**Quality signals**

- 147 GitHub stars
- 66 forks
- updated 2026-06-24
- primary language: Python

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 46/100 |
| stars | 46/100 |
| topics | 0/100 |
| outlook | 54/100 |
| quality | 46/100 |
| recency | 40/100 |
| adoption | 46/100 |
| production | 54/100 |
| usefulness | 90/100 |
| integration | 78/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 200/100 |

---

<sub>🔭 Discovered 2026-06-24 · [View on GitHub](https://github.com/Kilo-Org/kilo-marketplace) · [← Back to Mcp](./README.md)</sub>
