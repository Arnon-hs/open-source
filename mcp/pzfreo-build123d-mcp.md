# pzfreo/build123d-mcp

[![Stars](https://img.shields.io/github/stars/pzfreo/build123d-mcp?style=flat-square&color=yellow)](https://github.com/pzfreo/build123d-mcp/stargazers) [![Forks](https://img.shields.io/github/forks/pzfreo/build123d-mcp?style=flat-square&color=blue)](https://github.com/pzfreo/build123d-mcp/network) [![Language](https://img.shields.io/badge/lang-Python-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-62%2F100-brightgreen?style=flat-square)](#)

> MCP server for build123d to improve AI cognition when creating 3D CAD models

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 22 |
| 🍴 **Forks** | 2 |
| 💻 **Language** | Python |
| 📈 **Score** | 62/100 |
| 🗓️ **Last push** | 2026-09-05 |
| 🔍 **Source** | github |

## 🏷️ Topics

`ai-tools` `build123d` `cad` `mcp` `mcp-server` `python3`

## 🎯 Categories

MCP · AI/ML · Backend

## 📝 Summary

### English

**Brief Summary (2‑3 sentences)**  
`pzfreo/build123d-mcp` is a Model Context Protocol (MCP) server that bridges AI assistants with the open‑source build123d CAD toolkit, enabling AI‑driven generation and manipulation of 3D models. By exposing a standard API/SDK/CLI, it lets developers plug AI agents into real CAD tools and data sources without custom integration work. The project is a Python‑based prototype that is actively maintained but still requires a security and licensing review before production use.

**Value**  
- **Standardized AI‑to‑tool link**: The MCP server implements a common protocol, so any AI agent that understands MCP can instantly control build123d, reducing the time spent on bespoke glue code.  
- **Accelerates AI‑assisted design**: Engineers can prototype AI‑generated parts, iterate faster, and experiment with generative design workflows directly in a CAD environment.  
- **Reusable infrastructure**: Once deployed, the server can serve multiple AI agents or downstream services, acting as a central hub for model context, versioning, and tool execution.

**Practical Adoption Path**  
1. **Prototype** – Clone the repo, run the provided Docker/virtual‑env setup, and call the MCP endpoints from a local AI script or notebook to verify basic CAD operations.  
2. **Integration** – Wrap the MCP calls in your existing AI‑assistant framework (e.g., LangChain, AutoGPT) using the supplied Python SDK or CLI; map your domain‑specific prompts to build123d commands.  
3. **Testing & Hardening** – Add authentication, rate‑limiting, and input validation; run unit and integration tests against a sandbox build123d instance.  
4. **Deployment** – Deploy the server to a container orchestration platform (K8s, ECS) behind a gateway, configure monitoring, and expose the MCP API to your production AI services.

**Production Readiness**  
- **Maturity**: Medium. The codebase is recent (last update 2026‑06‑23), has modest community traction (22 ★, 2 forks), and is written in Python, making it easy to audit.  
- **Stability**: Suitable for internal prototypes or low‑risk pipelines; core functionality works, but the project lacks extensive automated tests and formal security hardening.  
- **Dependencies**: Relies on build123d and standard Python libraries; verify compatibility with your target environment and monitor upstream changes.  
- **Risks**: License compliance, security posture, and long‑term maintainer commitment still need confirmation before a production rollout. Conduct a brief security audit and establish a maintenance plan (e.g., fork and pin versions) to mitigate these risks.

### Русский

**pzf​reo/build123d‑mcp** — это открытый MCP‑сервер, позволяющий AI‑ассистентам напрямую работать с Build123D через единый протокол Model Context Protocol. Типичный сценарий — подключение интеллектуального агента к реальному набору CAD‑инструментов и данным (API/SDK/CLI), что упрощает создание, тестирование и деплой 3D‑моделей в прототипных или внутренних рабочих процессах. Проект находится на среднем уровне готовности к production: готов к экспериментальному использованию, но требует проверки лицензии, безопасности и поддерживаемости перед масштабным вводом.

### 中文

**项目简介**  
pzfreo/build123d-mcp 是一个基于 Model Context Protocol（MCP）的服务器，实现了 Build123D 与 AI 助手的标准化对接，使 AI 在生成 3D CAD 模型时能够直接调用真实工具和数据。

**价值**  
- **统一协议**：通过 MCP 为 AI 代理提供一致的接口，降低不同工具之间的集成成本。  
- **加速原型**：开发者可以快速把 AI 助手接入 Build123D，验证 AI 生成 CAD 的可行性。  
- **可复用的服务**：同一套服务器可供多团队、多个项目共享，促进模型上下文的标准化管理。

**典型接入方式**  
1. **API/SDK**：在 Python 环境中通过 `pip install build123d-mcp` 引入客户端库，使用 REST/WS 接口调用 MCP 服务。  
2. **CLI**：命令行工具 `build123d-mcp-cli` 可直接在本地或 CI/CD 流程中启动/交互。  
3. **语言元数据**：服务会返回 Build123D 支持的语言/函数签名，AI 代理据此生成符合语法的代码片段。  
4. **容器化部署**：提供 Docker 镜像，使用 `docker run -p 8000:8000 pzfreo/build123d-mcp` 即可快速启动服务。

**生产可用性**  
- **成熟度**：目前处于 **中等**（Medium）水平，适合原型、内部工作流或受控环境下使用。  
- **依赖与维护**：项目基于 Python，依赖相对轻量；但在投入生产前建议进行安全审计、许可证确认以及对关键依赖的版本锁定。  
- **社区活跃度**：22 星、2 Fork，最近一次更新为 2026‑06‑23，活跃度一般。若计划长期使用，最好自行维护或与原作者保持沟通。  

总体而言，pzfreo/build123d-mcp 为 AI‑CAD 场景提供了一个即插即用的桥梁，适合作为原型或内部工具的核心组件，生产环境使用时需完成额外的安全与运维检查。

## 🧭 Practical evaluation

**Value:** pzfreo/build123d-mcp helps connect AI assistants to real tools and data through a standard protocol.

**Best use cases**

- connect AI agents to tools
- ship Model Context Protocol servers
- standardize integrations

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** Medium: useful for prototypes or internal workflows, with dependency and maintenance checks before production.

**Quality signals**

- 22 GitHub stars
- 2 forks
- updated 2026-06-23
- primary language: Python
- 6 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 12/100 |
| stars | 29/100 |
| topics | 75/100 |
| outlook | 66/100 |
| quality | 57/100 |
| recency | 80/100 |
| adoption | 24/100 |
| production | 66/100 |
| usefulness | 74/100 |
| integration | 62/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 300/100 |

---

<sub>🔭 Discovered 2026-06-23 · [View on GitHub](https://github.com/pzfreo/build123d-mcp) · [← Back to Mcp](./README.md)</sub>
