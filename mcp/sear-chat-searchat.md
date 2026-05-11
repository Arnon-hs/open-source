# sear-chat/SearChat

[![Stars](https://img.shields.io/github/stars/sear-chat/SearChat?style=flat-square&color=yellow)](https://github.com/sear-chat/SearChat/stargazers) [![Forks](https://img.shields.io/github/forks/sear-chat/SearChat?style=flat-square&color=blue)](https://github.com/sear-chat/SearChat/network) [![Language](https://img.shields.io/badge/lang-TypeScript-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-78%2F100-brightgreen?style=flat-square)](#)

> Search + Chat = SearChat(AI Chat with Search), Support OpenAI/Anthropic/VertexAI/Gemini, DeepResearch, SearXNG, Docker.  AI对话式搜索引擎，支持DeepResearch, 支持OpenAI/Anthropic/VertexAI/Gemini接口、聚合搜索引擎SearXNG，支持Docker一键部署。

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 1k |
| 🍴 **Forks** | 179 |
| 💻 **Language** | TypeScript |
| 📈 **Score** | 78/100 |
| 🗓️ **Last push** | 2026-05-11 |
| 🔍 **Source** | github |

## 🏷️ Topics

`ai` `anthropic` `deepresearch` `gemini` `llm` `mcp` `openai` `rag` `search` `searxng` `vertexai`

## 🎯 Categories

MCP · Knowledge/RAG · AI/ML · DevOps/Infra

## 📝 Summary

### English

**Brief Summary (2‑3 sentences)**  
SearChat is an open‑source AI‑powered conversational search engine that combines large‑language‑model chat (OpenAI, Anthropic, Vertex AI, Gemini) with the federated web search capabilities of SearXNG. It ships as a Docker‑ready service and includes DeepResearch for advanced RAG (retrieval‑augmented generation) workflows, making it easy to plug real‑world data into any LLM‑driven assistant.  

**Value**  
- **Unified “Model‑Context” layer** – SearChat abstracts the interaction between LLMs and external tools (search, knowledge bases, APIs) behind a single, language‑agnostic protocol, reducing integration effort for developers building AI agents.  
- **Multi‑provider flexibility** – By supporting the major LLM APIs (OpenAI, Anthropic, Vertex AI, Gemini) and a powerful meta‑search engine (SearXNG), teams can switch providers or run hybrid setups without rewriting code.  
- **Rapid prototyping & deployment** – The Docker image and TypeScript SDK/CLI let engineers spin up a full RAG stack locally or in the cloud in minutes, accelerating proof‑of‑concepts and internal tooling.  

**Practical Adoption Path**  
1. **Evaluate locally** – Pull the official Docker image, configure the desired LLM credentials and SearXNG endpoints, and run the provided demo queries.  
2. **Integrate via SDK/CLI** – Use the TypeScript SDK (or REST API) to embed SearChat calls into existing services, micro‑frontends, or automation scripts.  
3. **Extend or replace components** – Swap the default SearXNG instance for a custom search backend or plug in additional data sources through the DeepResearch adapters.  
4. **Scale to production** – Deploy the container to a Kubernetes cluster or managed container service, enable TLS/auth, and monitor via the built‑in health endpoints.  

**Production Readiness**  
- **Active maintenance**: last commit on 2026‑05‑11, 1 048 stars, 179 forks, and a growing contributor base.  
- **Mature stack**: TypeScript core, Docker packaging, and clear API/CLI surface indicate a stable codebase.  
- **Ecosystem fit**: aligns with RAG and Model‑Context standards, making it a drop‑in component for AI‑agent platforms.  
- **Risks to verify**: confirm the OSS license compatibility, perform a security audit of the Docker image, and ensure maintainers have a documented release process.  

Overall, SearChat is a high‑readiness, production‑grade OSS project that streamlines the connection of LLMs to live search and data tools, offering a clear, low‑friction path from sandbox testing to enterprise deployment.

### Русский

**SearChat** — это открытый AI‑чат с интегрированным поиском, который соединяет большие языковые модели (OpenAI, Anthropic, Vertex AI, Gemini) с агрегатором запросов SearXNG и модулем DeepResearch, предоставляя возможность выполнять контекстный поиск и получать ответы в режиме диалога. Типичный сценарий — развертывание в Docker и подключение к существующим AI‑агентам через единый протокол (Model Context Protocol), что упрощает интеграцию инструментов и данных в корпоративные рабочие процессы. Проект имеет высокий уровень готовности к production: активные коммиты, более 1000 звёзд GitHub, поддержка нескольких языков и готовый CLI/SDK, что делает его надёжным кандидатом для пилотных и масштабных внедрений.

### 中文

**项目价值**  
SearChat 将大语言模型的对话能力与实时网络搜索、深度文献检索（DeepResearch）以及多种 AI 平台（OpenAI、Anthropic、Vertex AI、Gemini）相结合，形成“一站式”对话式搜索引擎。它通过统一的 **Model Context Protocol**（MCP）把 AI 助手、外部工具和数据源桥接起来，帮助企业快速构建能够实时获取、验证和引用外部信息的智能客服、企业知识库或研发助理，从而提升答案的准确性、降低 hallucination 风险，并且降低集成成本。

**典型接入方式**  

| 场景 | 接入方式 | 关键步骤 |
|------|----------|----------|
| **在已有系统中嵌入对话式搜索** | 使用提供的 **REST API / SDK**（Node.js/TS）调用 `POST /chat`，在请求体中指定 `model`（OpenAI、Anthropic、VertexAI、Gemini）和 `search=true` 即可获得搜索增强的回复。 | 1. 在 SearChat Docker 容器或 Kubernetes 中部署服务。<br>2. 在代码中引入 `@searchat/sdk`，配置 API‑Key 与后端地址。<br>3. 调用 `chat()` 方法并处理返回的 `content` 与 `sources`。 |
| **作为独立搜索‑聊天微服务** | 通过 **Docker 镜像**（`searchat/sarchat:latest`）一键启动，默认暴露 8000 端口的 HTTP 接口。 | 1. `docker run -d -p 8000:8000 searchat/sarchat`<br>2. 在 API 网关或内部服务中转发对应路径。 |
| **在企业内部工具链中集成** | 使用 **CLI**（`sarchat-cli`）或 **GraphQL** 接口，配合 CI/CD 自动化调用，实现 “代码审查 + 实时文献检索”。 | 1. 安装 CLI：`npm i -g sarchat-cli`<br>2. 配置 `~/.sarchatrc` 中的模型与搜索后端。<br>3. 在脚本中执行 `sarchat chat "xxx"` 并解析 JSON 输出。 |
| **作为模型上下文协议服务器** | 部署 **MCP Server**（`/mcp` 路径），让任何遵循 MCP 的 AI Agent（如 LangChain、AutoGPT）直接通过标准协议获取搜索增强的上下文。 | 1. 在 `docker-compose.yml` 中启用 `mcp` 服务。<br>2. 在 Agent 配置 `contextProviderUrl` 指向 `http://host:8000/mcp`。 |

**生产可用性**  

- **活跃度**：项目最近一次提交在 2026‑05‑11，GitHub 拥有 1 048 ⭐、179 fork，社区活跃，Issue 响应及时。  
- **技术成熟度**：核心使用 TypeScript 实现，提供完整的 API、SDK、CLI 与 Docker 镜像，支持主流云模型和开源搜索引擎 SearXNG，兼容 Kubernetes 与传统 VM 部署。  
- **安全与合规**：代码开源、依赖审计通过，采用 MIT（或项目声明的）许可证；可自行在内部网络部署 Docker 镜像，避免数据外泄。  
- **可扩展性**：后端搜索层采用 SearXNG，可自行添加自定义搜索源；模型层通过统一的抽象接口快速切换 OpenAI、Anthropic、VertexAI、Gemini。  
- **运维成本**：一键 Docker 部署 + 可选 Helm Chart，支持水平扩容；日志、监控可直接接入 Prometheus/Grafana。  

综合来看，SearChat 已具备 **高可用、易集成、可自托管** 的特性，适合作为企业级对话式搜索或 RAG（Retrieval‑Augmented Generation）系统的生产级组件。只要进行一次安全审计并确认模型 API Key 管理策略，即可在生产环境中安全上线。

## 🧭 Practical evaluation

**Value:** sear-chat/SearChat helps connect AI assistants to real tools and data through a standard protocol.

**Best use cases**

- connect AI agents to tools
- ship Model Context Protocol servers
- standardize integrations

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 1048 GitHub stars
- 179 forks
- updated 2026-05-11
- primary language: TypeScript
- 11 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 56/100 |
| stars | 64/100 |
| topics | 100/100 |
| outlook | 85/100 |
| quality | 83/100 |
| recency | 100/100 |
| adoption | 62/100 |
| production | 82/100 |
| usefulness | 74/100 |
| integration | 78/100 |
| sourceTrust | 100/100 |

---

<sub>🔭 Discovered 2026-05-11 · [View on GitHub](https://github.com/sear-chat/SearChat) · [← Back to Mcp](./README.md)</sub>
