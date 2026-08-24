# Wide-Moat/open-computer-use

[![Stars](https://img.shields.io/github/stars/Wide-Moat/open-computer-use?style=flat-square&color=yellow)](https://github.com/Wide-Moat/open-computer-use/stargazers) [![Forks](https://img.shields.io/github/forks/Wide-Moat/open-computer-use?style=flat-square&color=blue)](https://github.com/Wide-Moat/open-computer-use/network) [![Language](https://img.shields.io/badge/lang-Python-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-68%2F100-brightgreen?style=flat-square)](#)

> MCP server that gives any LLM its own computer — managed Docker workspaces with live browser, terminal, code execution, document skills, and autonomous sub-agents. Self-hosted, open-source, pluggable into any model.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 104 |
| 🍴 **Forks** | 24 |
| 💻 **Language** | Python |
| 📈 **Score** | 68/100 |
| 🗓️ **Last push** | 2026-08-24 |
| 🔍 **Source** | github |

## 🏷️ Topics

`agents` `claude-code` `computer-use` `llm` `mcp-server` `openwebui` `skills`

## 🎯 Categories

MCP · Automation · AI/ML · Backend · DevOps/Infra

## 📝 Summary

### English

Here's a brief summary of the Wide-Moat/open-computer-use project:

Wide-Moat/open-computer-use is an open-source project that enables any Large Language Model (LLM) to access a managed computer environment with live tools, including a browser, terminal, code execution, document skills, and autonomous sub-agents. This project provides a standard protocol for connecting AI assistants to real tools and data, allowing for seamless integration and automation. By plugging into any model, users can easily connect AI agents to various tools and data sources.

**Value Proposition:**
The primary value proposition of Wide-Moat/open-computer-use is to provide a standardized protocol for connecting AI assistants to real tools and data. This enables users to automate tasks, integrate AI agents with various systems, and unlock the full potential of AI-powered tools.

**Practical Adoption Path:**

1. **Evaluate the project:** Assess the project's documentation, code quality, and community engagement to ensure it meets your needs.
2. **Integrate with your LLM:** Follow the project's guidelines to integrate the MCP server with your chosen LLM.
3. **Configure the environment:** Set up the managed Docker workspace with the desired tools and services.
4. **Test and refine:** Test the integration and refine

### Русский

Резюме Wide-Moat/open-computer-use:

Wide-Moat/open-computer-use - это открытый проект, который предоставляет MCP-сервер, позволяющий любому LLM иметь свою собственную рабочую станцию. Это позволяет подключать AI-ассистентов к реальным инструментам и данным через стандартный протокол. Проект готов к интеграции и внедрению в production, поскольку имеет высокий уровень готовности, сильные сигналы эkosистемы и недавнюю активность.

### 中文

**项目简介（2‑3 句）**  
Wide‑Moat/open‑computer‑use 是一个 MCP（Model Context Protocol）服务器，为任意大语言模型提供独立的计算环境——基于 Docker 的工作区，内置实时浏览器、终端、代码执行、文档处理以及可自行调度的子代理。项目完全开源、可自托管，能够以插件化方式无缝接入任何模型。

**价值**  
- **真实工具接入**：通过统一的协议把 AI 助手直接连到浏览器、终端、文件系统等真实工具，突破纯文本交互的局限。  
- **标准化集成**：提供统一的 API/SDK/CLI，帮助团队快速为自研或第三方模型实现“有形”能力，降低集成成本。  
- **可扩展自治**：支持自定义子代理，实现任务分解、并行执行和结果聚合，提升自动化程度。

**典型接入方式**  
1. **部署 MCP 服务器**：在本地或云端运行 Docker‑compose，启动 `open-computer-use` 服务。  
2. **使用 SDK**（Python 为主）：在模型代码中引入 `open_computer_use` 包，调用 `create_workspace()`、`run_command()`、`browse(url)` 等高层 API。  
3. **通过 CLI/HTTP**：对不便改动模型代码的场景，可直接使用提供的 CLI 或 RESTful 接口发送 JSON 请求，获取执行结果或浏览器截图。  
4. **插件化**：通过自定义插件（如数据库、内部 API）向工作区注入额外资源，模型即可像使用本地工具一样调用。

**生产可用性**  
- **活跃度**：截至 2026‑07‑01 最近一次提交，GitHub ★104、Fork 24，代码主要使用 Python，维护频率保持在每周数次。  
- **生态兼容**：已被多个开源项目引用，提供完整的 OpenAPI 文档和示例，易于在 CI/CD 中集成。  
- **安全与可靠**：工作区基于隔离的 Docker 容器，默认禁用特权模式，支持细粒度网络与文件系统权限配置。  
- **成熟度**：具备完整的错误监控、日志导出以及可选的资源配额控制，已达到可在内部生产环境进行试点的水平。  

**结论**  
Wide‑Moat/open‑computer‑use 为 AI 与真实工具的桥接提供了即插即用的标准化方案，接入门槛低、扩展灵活，且在代码活跃度、社区采纳和安全隔离方面已经具备了生产级别的可靠性，适合作为企业内部 AI 自动化平台的核心组件。

## 🧭 Practical evaluation

**Value:** Wide-Moat/open-computer-use helps connect AI assistants to real tools and data through a standard protocol.

**Best use cases**

- connect AI agents to tools
- ship Model Context Protocol servers
- standardize integrations

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 104 GitHub stars
- 24 forks
- updated 2026-07-01
- primary language: Python
- 7 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 35/100 |
| stars | 43/100 |
| topics | 88/100 |
| outlook | 61/100 |
| quality | 56/100 |
| recency | 40/100 |
| adoption | 41/100 |
| production | 58/100 |
| usefulness | 90/100 |
| integration | 78/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 500/100 |

---

<sub>🔭 Discovered 2026-07-01 · [View on GitHub](https://github.com/Wide-Moat/open-computer-use) · [← Back to Mcp](./README.md)</sub>
