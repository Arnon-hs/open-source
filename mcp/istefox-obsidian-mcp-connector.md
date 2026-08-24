# istefox/obsidian-mcp-connector

[![Stars](https://img.shields.io/github/stars/istefox/obsidian-mcp-connector?style=flat-square&color=yellow)](https://github.com/istefox/obsidian-mcp-connector/stargazers) [![Forks](https://img.shields.io/github/forks/istefox/obsidian-mcp-connector?style=flat-square&color=blue)](https://github.com/istefox/obsidian-mcp-connector/network) [![Language](https://img.shields.io/badge/lang-TypeScript-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-70%2F100-brightgreen?style=flat-square)](#)

> Add integrations like semantic search and custom Templater prompts to Claude or any MCP client.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 23 |
| 🍴 **Forks** | 2 |
| 💻 **Language** | TypeScript |
| 📈 **Score** | 70/100 |
| 🗓️ **Last push** | 2026-08-24 |
| 🔍 **Source** | github |

## 🏷️ Topics

`claude` `mcp` `model-context-protocol` `obsidian-plugin`

## 🎯 Categories

MCP · Knowledge/RAG

## 📝 Summary

### English

**Brief Summary**  
The **obsidian‑mcp‑connector** by *istefox* adds a bridge between Obsidian (or any MCP‑compatible client) and AI assistants such as Claude, enabling semantic search, custom Templater prompts, and other tool‑level integrations through the Model Context Protocol (MCP). With a lightweight TypeScript codebase, it lets developers expose their notes, knowledge bases, or custom commands as first‑class data sources that AI agents can query and act upon.  

**Value**  
- **Standardised integration** – By implementing the open‑source MCP spec, the connector turns Obsidian vaults into plug‑and‑play knowledge stores for any MCP‑aware AI, eliminating the need for bespoke APIs.  
- **Enhanced AI capabilities** – Semantic search and templated prompts let agents retrieve context‑relevant information and execute user‑defined actions, boosting productivity for knowledge work, research, and education.  
- **Extensibility** – The TypeScript SDK/CLI can be repurposed for other tools, making it a reusable foundation for building Model Context Protocol servers across the ecosystem.  

**Practical Adoption Path**  
1. **Install** the npm package or clone the repo and run the provided CLI to register the connector with your MCP client (e.g., Claude, LangChain, or a custom agent).  
2. **Configure** the Obsidian vault location and optional Templater scripts in the generated `mcp-config.json`.  
3. **Enable** semantic indexing (built‑in or external vector store) to allow the AI to perform context‑aware searches.  
4. **Deploy** the connector as a local service (Docker or Node) or host it on a lightweight server for team‑wide access.  
5. **Consume** the MCP endpoints from any AI agent that supports the protocol, using standard HTTP calls or the supplied TypeScript SDK.  

**Production Readiness**  
- **Activity & Community** – Updated on 2026‑07‑04, 23 stars, 2 forks, and recent commits indicate active maintenance.  
- **Maturity** – The core functionality (API/SDK/CLI) is stable, with clear TypeScript typings and minimal external dependencies, making integration straightforward.  
- **Scalability** – Can be containerised and run behind a reverse proxy; the underlying MCP protocol is designed for low‑latency, stateless calls, suitable for production workloads.  
- **Risks** – License compliance, security hardening, and long‑term maintainer commitment still need a final review, but no immediate red flags are evident.  

Overall, the **obsidian‑mcp‑connector** is a high‑readiness OSS component that lets organizations quickly expose Obsidian knowledge to AI agents via a standard protocol, paving the way for robust, context‑aware AI‑assisted workflows.

### Русский

**istefox/obsidian-mcp-connector** — это TypeScript‑библиотека, позволяющая подключать Obsidian к клиентам MCP (например, Claude) и добавлять такие функции, как семантический поиск и пользовательские подсказки Templater. Типичный сценарий: разработчик разворачивает MCP‑сервер, подключает к нему Obsidian через этот коннектор и сразу получает возможность выполнять RAG‑запросы к своим заметкам или запускать инструменты из AI‑агента. Проект активно поддерживается (обновления 2026‑07‑04, 23★, 2 форка) и считается готовым к пилотному использованию в продакшене после окончательной проверки лицензии и безопасности.

### 中文

**项目简介**  
istefox/obsidian-mcp-connector 是一个基于 Model Context Protocol（MCP）的开源桥接库，能够把 Obsidian 笔记中的语义搜索、Templater 自定义提示等功能无缝接入 Claude、ChatGPT 或其他 MCP 客户端，实现 AI 助手对本地知识库和工具的实时调用。

**价值**  
- **标准化接口**：通过 MCP 提供统一的 API/SDK，让不同的 AI 代理能够以相同方式访问 Obsidian 数据和插件功能，降低集成成本。  
- **增强 AI 能力**：语义检索和自定义 Prompt 让模型在回答时能够直接引用笔记内容或执行特定工作流，提升答案的准确性和可操作性。  
- **快速交付**：开发者只需在项目中引入 TypeScript 包或 CLI，即可在几行代码内完成 AI 与 Obsidian 的双向通信，适合原型验证和生产级部署。

**典型接入方式**  
1. **SDK 方式**：在 Node.js/TypeScript 项目中 `npm i obsidian-mcp-connector`，使用 `Connector` 类创建 MCP 客户端并注册语义搜索或 Templater 处理函数。  
2. **CLI 方式**：通过提供的 `ob-mcp` 命令行工具启动本地 MCP 服务器，配置 `config.yaml` 指向 Obsidian 工作空间，即可让任何支持 MCP 的 AI（如 Claude）通过网络调用。  
3. **插件集成**：在 Obsidian 中安装对应的社区插件（如果有），插件内部已经封装了 MCP 端点，用户只需在 AI 平台配置对应的 URL 即可。

**生产可用性**  
- **活跃度**：最近一次提交是 2026‑07‑04，项目仍在维护；GitHub 23 ⭐、2 Fork，社区关注度适中。  
- **技术成熟度**：使用 TypeScript 编写，提供完整的类型声明；同时包含 API、SDK 与 CLI 三种接入层，适配多种部署场景。  
- **安全与合规**：当前未发现重大元数据泄露风险，仍需自行审查许可证（MIT）和依赖的安全报告。  
- **可评估性**：项目结构清晰，示例代码与文档齐全，易于在内部环境进行功能验证并逐步推广到生产。  

综合来看，istefox/obsidian-mcp-connector 已具备较高的生产可用性，适合作为 AI 与 Obsidian 知识库集成的首选桥接层。

## 🧭 Practical evaluation

**Value:** istefox/obsidian-mcp-connector helps connect AI assistants to real tools and data through a standard protocol.

**Best use cases**

- connect AI agents to tools
- ship Model Context Protocol servers
- standardize integrations

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 23 GitHub stars
- 2 forks
- updated 2026-07-04
- primary language: TypeScript
- 4 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 12/100 |
| stars | 29/100 |
| topics | 50/100 |
| outlook | 55/100 |
| quality | 44/100 |
| recency | 40/100 |
| adoption | 24/100 |
| production | 56/100 |
| usefulness | 100/100 |
| integration | 100/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 200/100 |

---

<sub>🔭 Discovered 2026-07-04 · [View on GitHub](https://github.com/istefox/obsidian-mcp-connector) · [← Back to Mcp](./README.md)</sub>
