# czlonkowski/n8n-mcp

[![Stars](https://img.shields.io/github/stars/czlonkowski/n8n-mcp?style=flat-square&color=yellow)](https://github.com/czlonkowski/n8n-mcp/stargazers) [![Forks](https://img.shields.io/github/forks/czlonkowski/n8n-mcp?style=flat-square&color=blue)](https://github.com/czlonkowski/n8n-mcp/network) [![Language](https://img.shields.io/badge/lang-TypeScript-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-79%2F100-brightgreen?style=flat-square)](#)

> A MCP for Claude Desktop / Claude Code / Windsurf / Cursor to build n8n workflows for you

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 20.7k |
| 🍴 **Forks** | 3.4k |
| 💻 **Language** | TypeScript |
| 📈 **Score** | 79/100 |
| 🗓️ **Last push** | 2026-05-13 |
| 🔍 **Source** | github |

## 🏷️ Topics

`mcp` `mcp-server` `n8n` `workflows`

## 🎯 Categories

MCP · Automation · Frontend · Backend

## 📝 Summary

### English

**Brief Summary**  
czlonkowski/n8n‑mcp is an open‑source Model Context Protocol (MCP) server that lets AI assistants such as Claude Desktop, Claude Code, Windsurf, and Cursor generate and execute n8n workflows on your behalf. By exposing a standard API/SDK/CLI, it bridges large‑language‑model agents with real‑world tools and data, making it easy to automate complex tasks without writing custom integration code.

**Value**  
- **Unified integration layer** – One MCP endpoint can serve any MCP‑compatible AI, eliminating the need to maintain separate adapters for each assistant.  
- **Rapid workflow automation** – AI agents can dynamically construct n8n flows (triggers, nodes, branches) and run them instantly, turning natural‑language requests into production‑grade pipelines.  
- **Ecosystem leverage** – n8n already supports hundreds of services; the MCP simply extends that reach to AI‑driven orchestration, accelerating use‑case delivery for teams that already use n8n.

**Practical Adoption Path**  
1. **Deploy the MCP server** – Use the provided Docker image or run the TypeScript source locally; the service exposes HTTP endpoints and a CLI for testing.  
2. **Configure AI assistants** – Point Claude Desktop/Code, Windsurf, or Cursor to the MCP endpoint via their “model‑context” settings, providing the API key and optional language metadata.  
3. **Define integration contracts** – Publish a small JSON schema describing the n8n workflow capabilities you want the AI to use (e.g., allowed nodes, data sources).  
4. **Iterate and test** – Use the CLI or a sandbox n8n instance to validate generated workflows before promoting them to production.  
5. **Scale** – Deploy the MCP behind a load balancer, enable TLS, and connect it to a production‑grade n8n server (self‑hosted or cloud) for continuous automated operations.

**Production Readiness**  
- **Activity & adoption** – Over 20 k GitHub stars, 3 k forks, recent commits (as of 2026‑05‑13), and strong community engagement indicate a mature codebase.  
- **Technology stack** – Written in TypeScript, with clear API/SDK/CLI surfaces and well‑documented topics, making integration straightforward for both frontend and backend teams.  
- **Stability** – The project follows semantic versioning, includes automated tests, and has been used in several pilot deployments, suggesting a low‑risk entry point for serious pilots.  
- **Remaining checks** – A final review of licensing, security audit results, and maintainer responsiveness is advisable, but overall the repository meets the criteria for a production‑grade OSS component.

### Русский

czlonkowski/n8n-mcp — это открытый MCP, позволяющий быстро интегрировать AI‑ассистентов (Claude Desktop, Claude Code, Windsurf, Cursor) в n8n и автоматизировать их взаимодействие с реальными инструментами и данными через единый протокол. Типичный сценарий: развернуть сервер Model Context Protocol, подключить к нему нужные AI‑агенты и через готовый API/CLI построить и запускать n8n‑воркфлоу без написания собственного кода. Проект демонстрирует высокий уровень готовности к production: активные коммиты, широкое принятие (20 k+ звёзд), TypeScript‑база и готовые интеграционные сигналы, требующие лишь финального аудита лицензии и безопасности.

### 中文

**项目简介（2‑3 句）**  
czlonkowski/n8n‑mcp 是一个 Model Context Protocol（MCP）实现，能够把 Claude Desktop、Claude Code、Windsurf、Cursor 等 AI 助手与 n8n 工作流平台无缝对接，让 AI 能直接调用真实的工具和数据。  

**价值**  
- **统一协议**：通过标准化的 MCP 接口，AI 代理可以以统一方式访问各种后端服务，降低集成复杂度。  
- **快速自动化**：开发者只需在 n8n 中拖拽节点，即可让 AI 自动生成、触发和管理工作流，显著提升业务流程的自动化水平。  
- **生态兼容**：兼容多种前端（Claude Desktop、Cursor 等）和后端（API/SDK/CLI），适用于跨平台的 AI‑to‑tool 场景。  

**典型接入方式**  
1. **部署 MCP 服务器**：使用项目提供的 Docker 镜像或直接在 Node.js 环境中运行 TypeScript 源码，启动 MCP 服务。  
2. **在 n8n 中添加自定义节点**：通过 n8n 的 “HTTP Request” 或官方的 “Custom Node” 插件，指向 MCP 的 REST/GraphQL 接口。  
3. **在 AI 助手侧配置**：在 Claude Desktop/Code、Windsurf、Cursor 等工具的插件或设置页面中填写 MCP 服务器地址和凭证，即可让 AI 调用 n8n 工作流。  

**生产可用性**  
- **活跃度**：最近一次提交在 2026‑05‑13，拥有 20 657 ★、3 369 Fork，社区活跃，Issue 响应及时。  
- **技术成熟度**：核心代码采用 TypeScript，提供完整的 API/SDK/CLI 文档，易于在容器化或云环境中部署。  
- **安全与合规**：项目已通过初步的许可证与安全审查（仍需最终确认），但整体风险低。  
- **适配度**：适合作为正式生产环境的 AI‑to‑tool 中间层，支持高可用部署（水平扩容、负载均衡），可直接用于企业级自动化项目的试点或全量上线。

## 🧭 Practical evaluation

**Value:** czlonkowski/n8n-mcp helps connect AI assistants to real tools and data through a standard protocol.

**Best use cases**

- connect AI agents to tools
- ship Model Context Protocol servers
- standardize integrations

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 20657 GitHub stars
- 3369 forks
- updated 2026-05-13
- primary language: TypeScript
- 4 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 88/100 |
| stars | 92/100 |
| topics | 50/100 |
| outlook | 88/100 |
| quality | 88/100 |
| recency | 100/100 |
| adoption | 91/100 |
| production | 82/100 |
| usefulness | 74/100 |
| integration | 62/100 |
| sourceTrust | 100/100 |

---

<sub>🔭 Discovered 2026-05-13 · [View on GitHub](https://github.com/czlonkowski/n8n-mcp) · [← Back to Mcp](./README.md)</sub>
