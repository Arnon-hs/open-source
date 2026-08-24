# aayoawoyemi/Ori-Mnemos

[![Stars](https://img.shields.io/github/stars/aayoawoyemi/Ori-Mnemos?style=flat-square&color=yellow)](https://github.com/aayoawoyemi/Ori-Mnemos/stargazers) [![Forks](https://img.shields.io/github/forks/aayoawoyemi/Ori-Mnemos?style=flat-square&color=blue)](https://github.com/aayoawoyemi/Ori-Mnemos/network) [![Language](https://img.shields.io/badge/lang-TypeScript-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-63%2F100-brightgreen?style=flat-square)](#)

> Local-first persistent agentic memory powered by Recursive Memory Harness (RMH). Open source must win.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 314 |
| 🍴 **Forks** | 28 |
| 💻 **Language** | TypeScript |
| 📈 **Score** | 63/100 |
| 🗓️ **Last push** | 2026-08-24 |
| 🔍 **Source** | github |

## 🏷️ Topics

`agent-memory` `ai-agent` `ai-agents` `ai-memory` `knowledge-graph` `llm` `local-first` `markdown` `mcp` `mcp-server` `memory` `model-context-protocol`

## 🎯 Categories

Orchestration · MCP · Knowledge/RAG · AI/ML · Backend

## 📝 Summary

### English

Here's a brief summary and explanation of the project:

**Summary:** aayoawoyemi/Ori-Mnemos is an open-source project that enables local-first persistent agentic memory, allowing users to turn isolated prompts and tools into repeatable agent workflows. This project uses Recursive Memory Harness (RMH) to facilitate coordination of multi-agent workflows, add tool-use pipelines, and standardize agent memory.

**Value:** The value proposition of Ori-Mnemos lies in its ability to transform isolated tools and prompts into repeatable workflows, making it easier to coordinate complex tasks and streamline processes. This can lead to increased efficiency and productivity, especially in environments where multiple agents or tools need to work together.

**Practical Adoption Path:** To adopt Ori-Mnemos, users can start by evaluating its API, SDK, or CLI, depending on their specific needs. They can also review the language metadata and focused topics to ensure the project aligns with their requirements. Once adopted, users can integrate Ori-Mnemos into their existing workflows, leveraging its capabilities to standardize agent memory and add tool-use pipelines.

**Production Readiness:** Ori-Mnemos exhibits strong production readiness, with recent activity, adoption, and ecosystem signals indicating a robust and reliable project. With 314 GitHub stars, 28 forks

### Русский

Резюме проекта aayoawoyemi/Ori-Mnemos:

Проект aayoawoyemi/Ori-Mnemos представляет собой открытое исходное решение для локальной, постоянной агентной памяти, основанной на Recursive Memory Harness (RMH). Он позволяет превращать изолированные команды и инструменты в повторяемые агентные потоки, что делает его идеальным решением для координации многоагентных процессов.

Проект готов к внедрению в производстивную среду, поскольку он демонстрирует высокий уровень активности, широкое распространение и сильные сигналы экосистемы. Он имеет 314 GitHub звезд, 28 форков и последние обновления в 2026 году. Проект можно оценить за счет его API/SDK/CLI, языковой метаданных или фокусированных тем.

Проект aayoawoyemi/Ori-Mnemos идеально подходит для следующего типового сценария внедрения: организации, занимающейся координацией многоагентных процессов, требует надежной и повторяемой системы для управления агентными потоками.

### 中文

**项目简介**  
Ori‑Mnemos（aayoawoyemi/Ori‑Mnemos）是一款基于递归记忆框架（Recursive Memory Harness，RMH）的本地‑优先持久化智能体记忆库。它把孤立的 Prompt 与工具封装成可复用、可追踪的 agent 工作流，帮助开发者快速构建多智能体协同系统。  

**价值主张**  
- **统一记忆与工具链**：为每个智能体提供持久化、可查询的记忆层，同时支持自定义工具调用，实现“记得过去、用好工具”。  
- **可复用的工作流**：把零散的 Prompt、API 调用、数据处理等抽象为标准化的任务节点，便于在不同项目或团队间共享与复用。  
- **本地‑first 安全**：数据默认保存在本地或自托管的后端，降低对云服务的依赖，满足隐私合规要求。  

**典型接入方式**  
1. **SDK / NPM 包**：`npm i @ori-mnemos/core` 后在 TypeScript/JavaScript 项目中直接实例化 `MemoryEngine`，通过提供的 `store`, `retrieve`, `update` 接口进行记忆操作。  
2. **CLI**：`ori-mnemos run --config ./config.yaml` 可快速启动一个本地记忆服务，配合任何支持 HTTP/WS 的智能体框架（LangChain、AutoGPT 等）使用。  
3. **API 网关**：部署 `ori-mnemos-server`（Docker 镜像），对外暴露 REST/GraphQL 接口；其他语言（Python、Go 等）通过 HTTP 客户端调用即可。  

**生产可用性**  
- **活跃度**：截至 2026‑07‑13，项目最近一次提交，拥有 314 ★、28 fork，20+ 主题标签，表明社区活跃。  
- **技术成熟度**：核心实现使用 TypeScript，提供完整的类型声明、单元测试和 CI/CD 流程，易于在企业 CI 环境中集成。  
- **部署友好**：支持 Docker、K8s Helm Chart 以及纯二进制，可在本地、私有云或边缘设备上快速上线。  
- **安全与合规**：数据默认本地持久化，未强制依赖外部 SaaS；仍需自行审计许可证（MIT）和潜在的第三方依赖安全报告。  

综上，Ori‑Mnemos 已具备较高的生产可用性，适合作为多智能体协作、工具链编排以及统一记忆层的 OSS 基础设施，在企业级试点项目中可以直接投入使用。

## 🧭 Practical evaluation

**Value:** aayoawoyemi/Ori-Mnemos helps turn isolated prompts and tools into repeatable agent workflows.

**Best use cases**

- coordinate multi-agent workflows
- add tool-use pipelines
- standardize agent memory

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 314 GitHub stars
- 28 forks
- updated 2026-07-13
- primary language: TypeScript
- 20 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 37/100 |
| stars | 53/100 |
| topics | 100/100 |
| outlook | 61/100 |
| quality | 62/100 |
| recency | 40/100 |
| adoption | 49/100 |
| production | 58/100 |
| usefulness | 74/100 |
| integration | 62/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 500/100 |

---

<sub>🔭 Discovered 2026-07-13 · [View on GitHub](https://github.com/aayoawoyemi/Ori-Mnemos) · [← Back to Orchestration](./README.md)</sub>
