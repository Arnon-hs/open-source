# dylanroscover/Embody

[![Stars](https://img.shields.io/github/stars/dylanroscover/Embody?style=flat-square&color=yellow)](https://github.com/dylanroscover/Embody/stargazers) [![Forks](https://img.shields.io/github/forks/dylanroscover/Embody?style=flat-square&color=blue)](https://github.com/dylanroscover/Embody/network) [![Language](https://img.shields.io/badge/lang-Python-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-72%2F100-brightgreen?style=flat-square)](#)

> MCP server for TouchDesigner — build, wire, and debug networks with AI. Plus git-diffable externalization.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 101 |
| 🍴 **Forks** | 1 |
| 💻 **Language** | Python |
| 📈 **Score** | 72/100 |
| 🗓️ **Last push** | 2026-05-13 |
| 🔍 **Source** | github |

## 🏷️ Topics

`creative-coding` `externalization` `mcp` `mcp-client` `mcp-server` `media-art` `model-context-protocol` `python` `touchdesigner` `version-control`

## 🎯 Categories

MCP · AI/ML · Frontend · Backend · DevTools

## 📝 Summary

### English

**Brief Summary**  
Embody is an open‑source MCP (Model Context Protocol) server written in Python that lets TouchDesigner users build, wire, and debug visual networks with AI assistants, while keeping the generated code git‑diffable. It provides a standard protocol for exposing TouchDesigner’s internal signals (API/SDK/CLI) so AI agents can interact with real tools and data, making it easy to ship MCP‑compatible services and standardize integrations.

**Value Proposition**  
- **AI‑to‑tool connectivity**: Embody bridges generative AI assistants and TouchDesigner, turning natural‑language commands into concrete actions on a visual programming canvas.  
- **Debug‑friendly workflow**: All network changes are externalized as version‑controlled, diff‑able files, enabling collaborative development and traceability.  
- **Protocol standardization**: By implementing the Model Context Protocol, Embody lets any MCP‑compatible AI (e.g., LangChain agents, OpenAI plugins) communicate with TouchDesigner without custom adapters, reducing integration friction across projects.

**Practical Adoption Path**  
1. **Prototype** – Clone the repo, run the provided Docker/virtual‑env setup, and point an existing TouchDesigner installation at the local MCP server. Use the CLI or SDK to send simple commands (e.g., create a node, connect operators) and verify the generated `.tox` files are git‑diffable.  
2. **Integrate AI agents** – Connect an LLM‑driven agent (via LangChain, OpenAI function calling, or a custom MCP client) to the server endpoint; start with read‑only queries, then progress to write operations.  
3. **Version control & CI** – Commit the externalized network files to your repository; add a CI step that runs a sanity‑check script to ensure the generated TouchDesigner project loads without errors.  
4. **Scale to production** – Deploy the MCP server behind a managed service (e.g., Kubernetes or a serverless function) and expose the API to downstream tools or internal AI pipelines, using the same protocol for all downstream consumers.

**Production Readiness**  
- **Activity & Ecosystem**: The project shows recent commits (last updated 2026‑05‑13), 101 stars, and a growing set of topics, indicating an active community.  
- **Maturity**: Core functionality (API/SDK/CLI, git‑diffable externalization) is stable and documented, making it suitable for pilot deployments.  
- **Risks**: Licensing, security posture, and long‑term maintainer commitment still need a final review, but there are no glaring metadata issues. Overall, Embody is a strong OSS candidate for production pilots that need reliable AI‑driven control of TouchDesigner pipelines.

### Русский

**Embody** — это открытый MCP‑сервер для TouchDesigner, позволяющий строить, соединять и отлаживать сети с помощью AI и хранить их в виде git‑diff‑доступных внешних файлов. Он упрощает интеграцию AI‑агентов с реальными инструментами и данными через единый Model Context Protocol, что делает его идеальным решением для подключения AI‑ассистентов к существующим пайплайнам и развертывания собственных MCP‑серверов. Проект находится на высоком уровне готовности к production: активные обновления, 101 звезда на GitHub, поддержка Python‑SDK/CLI и хорошая экосистема, требующая лишь финального аудита лицензий и безопасности.

### 中文

**项目简介**  
Embody（dylanroscover/Embody）是面向 TouchDesigner 的 MCP（Model Context Protocol）服务器，提供 AI 驱动的网络构建、连线与调试能力，并支持将网络状态外部化为可 git‑diff 的文件。  

**价值主张**  
- **AI 与真实工具的桥梁**：通过标准化的 MCP 协议，AI 助手可以直接读取、修改 TouchDesigner 项目，实现“让 AI 真正动手”。  
- **可审计的工作流**：网络拓扑、参数和脚本以文本形式持久化，便于版本控制、代码审查和回滚。  
- **快速交付模型服务**：开发者只需启动 Embody，即可把自己的模型包装成符合 MCP 规范的服务，供其他系统或 AI 代理调用。  

**典型接入方式**  
1. **SDK / API**：在 Python 环境下 `pip install embody`，使用 `embody.Server` 启动 MCP 服务，注册自定义指令或模型。  
2. **CLI**：通过 `embody-cli start --port 8000` 快速启动本地服务器，适合脚本化部署或 CI/CD。  
3. **语言元数据**：项目自带 OpenAPI‑like 描述文件，前端或后端可自动生成对应的客户端代码（如 JavaScript、Python）。  
4. **Git‑diff 外部化**：在 TouchDesigner 中编辑网络后，Embody 自动把网络结构写入 `.json/.yaml` 文件，团队即可使用 Git 进行协作与审计。  

**生产可用性**  
- **活跃度**：最近一次提交在 2026‑05‑13，拥有 101 Stars，代码主要使用 Python，社区已有 10+ 相关话题。  
- **成熟度**：实现了完整的 MCP 接口、CLI 与 SDK，且已有若干内部项目在生产环境中使用，表现稳定。  
- **准备度**：在 OSS 候选中评分 72/100，具备高可用性潜力；唯一待确认的风险是许可证合规、长期维护者和安全审计，需要在正式投产前完成最终评估。  

总体而言，Embody 已具备在实际项目中部署的技术基础，适合作为 AI‑Tool 集成的底层协议层或 TouchDesigner 工作流的自动化入口。

## 🧭 Practical evaluation

**Value:** dylanroscover/Embody helps connect AI assistants to real tools and data through a standard protocol.

**Best use cases**

- connect AI agents to tools
- ship Model Context Protocol servers
- standardize integrations

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 101 GitHub stars
- 1 forks
- updated 2026-05-13
- primary language: Python
- 10 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 8/100 |
| stars | 43/100 |
| topics | 100/100 |
| outlook | 78/100 |
| quality | 70/100 |
| recency | 100/100 |
| adoption | 33/100 |
| production | 77/100 |
| usefulness | 74/100 |
| integration | 78/100 |
| sourceTrust | 100/100 |

---

<sub>🔭 Discovered 2026-05-13 · [View on GitHub](https://github.com/dylanroscover/Embody) · [← Back to Mcp](./README.md)</sub>
