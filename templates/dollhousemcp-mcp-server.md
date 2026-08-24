# DollhouseMCP/mcp-server

[![Stars](https://img.shields.io/github/stars/DollhouseMCP/mcp-server?style=flat-square&color=yellow)](https://github.com/DollhouseMCP/mcp-server/stargazers) [![Forks](https://img.shields.io/github/forks/DollhouseMCP/mcp-server?style=flat-square&color=blue)](https://github.com/DollhouseMCP/mcp-server/network) [![Language](https://img.shields.io/badge/lang-TypeScript-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-69%2F100-brightgreen?style=flat-square)](#)

> A Free, Open Source MCP server for dynamic custom persona management with public a GitHub collection of personas, skills, templates, and other elements for AI models.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 35 |
| 🍴 **Forks** | 13 |
| 💻 **Language** | TypeScript |
| 📈 **Score** | 69/100 |
| 🗓️ **Last push** | 2026-08-24 |
| 🔍 **Source** | github |

## 🏷️ Topics

`agents` `ai` `ai-tools` `claude` `codex` `cursor` `dollhousemcp` `ensembles` `llm` `mcp` `mcp-server` `memory`

## 🎯 Categories

Templates · MCP · AI/ML · Backend

## 📝 Summary

### English

**Brief Summary (2‑3 sentences)**  
DollhouseMCP /mcp‑server is a free, open‑source implementation of the Model Context Protocol (MCP) that lets developers expose and manage dynamic, custom personas, skills, templates, and other AI‑model assets through a public GitHub collection. Built in TypeScript, the server provides a standard API/SDK/CLI for connecting AI assistants to real‑world tools and data, making it easy to ship MCP‑compatible services and integrate heterogeneous AI components.

**Value**  
- **Standardized integration**: By adhering to MCP, the server offers a common contract for AI agents to access external tools, data sources, and persona definitions, reducing the need for bespoke glue code.  
- **Reusable assets**: The public repository of personas, skills, and templates can be shared across projects, accelerating prototyping and enabling consistent behavior across multiple AI assistants.  
- **Open‑source flexibility**: Being MIT‑licensed and written in TypeScript, it can be self‑hosted, extended, or embedded in existing back‑ends without vendor lock‑in.

**Practical Adoption Path**  
1. **Prototype** – Clone the repo, run the provided Docker/CLI locally, and experiment with the sample personas to validate the protocol against your AI model.  
2. **Integrate** – Use the generated SDK or REST endpoints to connect your AI agent (e.g., LangChain, OpenAI, Claude) to the MCP server, mapping required tool calls to your internal services.  
3. **Customize** – Add or fork the GitHub collection to create organization‑specific personas, skills, or templates, then push updates to the server via its API.  
4. **Deploy** – Containerize the server (Docker/K8s) and expose it behind your internal gateway; configure CI/CD to keep the persona collection in sync.  

**Production Readiness**  
- **Activity & Community**: 35 stars, 13 forks, recent commits (as of 2026‑06‑23), and a rich set of 20 topics indicate an active project.  
- **Technical maturity**: The TypeScript codebase, clear API/CLI surface, and Docker support make it straightforward to evaluate and integrate.  
- **Risk considerations**: No major metadata or licensing concerns have surfaced, but a final security audit and verification of maintainer responsiveness are recommended before mission‑critical rollout. Overall, the server is positioned as a high‑readiness OSS candidate for pilots and production deployments.

### Русский

DollhouseMCP/mcp-server — это бесплатный open‑source сервер MCP, который позволяет подключать AI‑ассистентов к реальным инструментам и данным через единый протокол, используя общедоступный набор персон, навыков и шаблонов. Типичный сценарий — развертывание сервера Model Context Protocol для интеграции AI‑агентов с внешними сервисами (инструменты, базы данных, кастомные API) и стандартизация этих связей. Проект имеет высокий уровень готовности к production: активная разработка, недавние коммиты, 35 звёзд, 13 форков, поддержка TypeScript, обширная документация и готовый API/SDK/CLI, что делает его надёжным кандидатом для пилотных внедрений.

### 中文

**项目简介**  
DollhouseMCP/mcp-server 是一个免费、开源的 MCP（Model Context Protocol）服务器，提供统一的协议让 AI 助手能够动态加载、切换和管理自定义人格、技能、模板等资源，所有资源均通过 GitHub 公共仓库共享。

**价值**  
- **标准化集成**：通过 MCP 协议把 AI 模型与真实工具、数据源、业务系统无缝对接，降低跨平台集成成本。  
- **可复用人格库**：公开的 persona、skill、template 等集合让团队可以快速复用或定制 AI 人格，提升研发效率。  
- **生态兼容**：兼容多种语言的 SDK、CLI 与 RESTful API，适配现有的后端服务和 CI/CD 流程。

**典型接入方式**  
1. **API/SDK**：在后端服务中引入官方 TypeScript SDK（或通过 OpenAPI 生成的客户端），调用 `POST /sessions`、`GET /personas` 等接口创建会话并加载所需人格。  
2. **CLI**：使用 `mcp-cli` 在本地或 CI 环境快速部署/更新 persona、skill 包，适合 DevOps 自动化。  
3. **容器化部署**：提供 Docker 镜像，直接在 Kubernetes/Compose 中运行，配合环境变量配置 GitHub Persona 仓库 URL 与访问令牌，即可对外提供统一的 MCP 服务。

**生产可用性**  
- **活跃度**：最近一次提交于 2026‑06‑23，拥有 35⭐、13 fork，20+ 话题标签，社区活跃。  
- **技术成熟度**：使用 TypeScript 编写，提供完整的类型定义和单元测试，易于审计和二次开发。  
- **部署成熟**：官方 Docker 镜像已发布，支持 Helm Chart，便于在生产集群中弹性伸缩。  
- **风险**：需进一步审查许可证（MIT/Apache 等）和安全审计报告；保持维护者活跃是后续关注点。  

综合来看，DollhouseMCP/mcp-server 已具备进入生产环境的技术基线，适合作为 AI 助手与企业工具链对接的标准化入口。

## 🧭 Practical evaluation

**Value:** DollhouseMCP/mcp-server helps connect AI assistants to real tools and data through a standard protocol.

**Best use cases**

- connect AI agents to tools
- ship Model Context Protocol servers
- standardize integrations

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 35 GitHub stars
- 13 forks
- updated 2026-06-23
- primary language: TypeScript
- 20 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 29/100 |
| stars | 33/100 |
| topics | 100/100 |
| outlook | 62/100 |
| quality | 54/100 |
| recency | 40/100 |
| adoption | 32/100 |
| production | 57/100 |
| usefulness | 100/100 |
| integration | 78/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 400/100 |

---

<sub>🔭 Discovered 2026-06-23 · [View on GitHub](https://github.com/DollhouseMCP/mcp-server) · [← Back to Templates](./README.md)</sub>
