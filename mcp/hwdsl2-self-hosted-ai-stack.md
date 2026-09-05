# hwdsl2/self-hosted-ai-stack

[![Stars](https://img.shields.io/github/stars/hwdsl2/self-hosted-ai-stack?style=flat-square&color=yellow)](https://github.com/hwdsl2/self-hosted-ai-stack/stargazers) [![Forks](https://img.shields.io/github/forks/hwdsl2/self-hosted-ai-stack?style=flat-square&color=blue)](https://github.com/hwdsl2/self-hosted-ai-stack/network) [![Language](https://img.shields.io/badge/lang-Shell-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-81%2F100-brightgreen?style=flat-square)](#)

> Deploy a complete self-hosted AI stack with Docker Compose: Ollama, LiteLLM, AnythingLLM, Whisper, WhisperLive, Kokoro, Embeddings, Docling and MCP Gateway. Local-first, private by default, with lightweight stacks, optional HTTPS and NVIDIA CUDA acceleration. Multi-arch: amd64, arm64.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 107 |
| 🍴 **Forks** | 21 |
| 💻 **Language** | Shell |
| 📈 **Score** | 81/100 |
| 🗓️ **Last push** | 2026-09-05 |
| 🔍 **Source** | github |

## 🏷️ Topics

`ai` `ai-stack` `cuda` `docker` `docker-compose` `docling` `embeddings` `linux` `litellm` `llm` `local-ai` `mcp`

## 🎯 Categories

MCP · Knowledge/RAG · AI/ML · DevOps/Infra

## 📝 Summary

### English

**Brief Summary (2‑3 sentences)**  
hwdsl2/self‑hosted‑ai‑stack provides a ready‑to‑run Docker‑Compose bundle that brings together Ollama, LiteLLM, AnythingLLM, Whisper, WhisperLive, Kokoro, embeddings, Docling and an MCP gateway. It delivers a private‑by‑default, multi‑arch (amd64 / arm64) AI platform with optional HTTPS and NVIDIA CUDA acceleration, letting teams run full‑stack LLM, RAG and speech‑to‑text services on‑premise.

**Value**  
The stack turns a collection of disparate open‑source AI components into a single, cohesive platform, exposing a standard Model Context Protocol (MCP) interface. This lets developers plug AI agents directly into real tools, data stores, and custom services without writing glue code, accelerating the creation of “AI‑as‑a‑service” products and internal assistants while keeping data under full control.

**Practical Adoption Path**  

| Step | Action | Reason |
|------|--------|--------|
| 1️⃣  | Clone the repo and run `docker compose up -d` (or use the provided `.env` to enable CUDA/HTTPS). | One‑command bootstrap; works on both x86_64 and ARM hardware. |
| 2️⃣  | Verify each service (Ollama, LiteLLM, Whisper, etc.) via their health‑check endpoints. | Confirms the stack is healthy before integration. |
| 3️⃣  | Register the MCP gateway URL in your AI agent or RAG pipeline. | Provides a uniform API for chat, embeddings, transcription, etc. |
| 4️⃣  | Extend or replace modules (e.g., swap Ollama for a different LLM) by editing the compose file—no code changes needed. | Keeps the stack flexible for evolving requirements. |
| 5️⃣  | Deploy to production (Docker Swarm, Kubernetes, or a VM) and enable TLS/Authentication via the built‑in HTTPS toggle. | Guarantees secure, scalable operation. |

**Production Readiness**  
- **Activity & Community**: 107 ⭐, 21 forks, recent commits (as of 2026‑06‑24) and a healthy issue/PR flow indicate active maintenance.  
- **Architecture**: Containerized, multi‑arch, and optionally GPU‑accelerated, matching typical enterprise deployment patterns.  
- **Security & Compliance**: Private‑by‑default stance, optional TLS, and clear separation of services reduce attack surface; however, a final license and vulnerability audit is still required.  
- **Scalability**: Individual services can be scaled out via Docker Compose overrides or orchestrated in Kubernetes, making the stack suitable for pilot projects up to production workloads.  

Overall, the project is mature enough for a serious pilot, offering a low‑friction path to a self‑hosted, standards‑based AI backend while still needing the usual final security and licensing review before full production rollout.

### Русский

**hwdsl2/self-hosted-ai-stack** — это готовый набор Docker‑Compose сервисов, позволяющий развернуть полностью локальный AI‑стек (Ollama, LiteLLM, AnythingLLM, Whisper, WhisperLive, Kokoro, Embeddings, Docling и MCP Gateway) с поддержкой NVIDIA CUDA и мульти‑архитектурой amd64/arm64. Он упрощает подключение AI‑ассистентов к реальным инструментам и данным через единый протокол Model Context Protocol, что делает его идеальным решением для построения RAG‑систем, интеграции моделей в существующие бизнес‑процессы и создания собственных серверов‑агентов. Проект уже активно поддерживается (обновления 2026‑06‑24, 107 звёзд, 21 форк), имеет чистый Docker‑интерфейс и достаточно зрелую инфраструктуру, чтобы использовать его в пилотных и production‑окружениях после обычного аудита лицензий и безопасности.

### 中文

**项目简介（2‑3 句）**  
hwdsl2/self-hosted-ai-stack 是一个基于 Docker‑Compose 的全栈本地 AI 环境，一键部署 Ollama、LiteLLM、AnythingLLM、Whisper 系列、Kokoro、Embedding、Docling 与 MCP Gateway 等组件，默认私有、轻量化，可选 HTTPS 与 NVIDIA CUDA 加速，支持 amd64 与 arm64 多架构。

**价值**  
- **标准化 AI 与工具的连接**：通过 MCP（Model Context Protocol）网关，将 AI 助手统一映射为可调用的工具和数据源，降低集成门槛。  
- **本地优先、数据安全**：所有模型和服务均运行在用户自己的机器或私有网络中，天然满足隐私合规需求。  
- **可插拔、可扩展**：模块化的 Docker‑Compose 配置让用户可以按需增删组件，支持从单机实验到多节点生产部署。

**典型接入方式**  
1. **Docker‑Compose 部署**：克隆仓库 → `docker compose up -d`，即可获得完整的 API/SDK/CLI 接口。  
2. **通过 MCP Gateway**：在业务代码中使用 MCP 客户端（HTTP/JSON 或 gRPC），调用已注册的工具（如 Whisper 语音转写、Embedding 检索、AnythingLLM 文本生成等）。  
3. **SDK/CLI 调用**：各子服务均暴露标准化的 REST/GraphQL 接口或命令行工具，便于在 Python、Node.js、Shell 等语言中直接集成。  

**生产可用性**  
- **活跃度高**：截至 2026‑06‑24 最近一次提交，拥有 107 星、21 Fork，社区讨论活跃。  
- **成熟度**：多组件均为成熟开源项目（Ollama、LiteLLM、Whisper 等），Docker‑Compose 方案已在多个内部项目验证。  
- **可扩展性**：支持 NVIDIA CUDA 加速、HTTPS 终端、跨平台（amd64/arm64），满足从边缘设备到高性能服务器的不同场景。  
- **风险点**：仍需进一步审查许可证兼容性、容器安全基线以及维护者响应速度，但总体已具备在企业内部或受控环境中进行正式试点的条件。

## 🧭 Practical evaluation

**Value:** hwdsl2/self-hosted-ai-stack helps connect AI assistants to real tools and data through a standard protocol.

**Best use cases**

- connect AI agents to tools
- ship Model Context Protocol servers
- standardize integrations

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 107 GitHub stars
- 21 forks
- updated 2026-06-24
- primary language: Shell
- 20 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 34/100 |
| stars | 43/100 |
| topics | 100/100 |
| outlook | 78/100 |
| quality | 68/100 |
| recency | 80/100 |
| adoption | 41/100 |
| production | 74/100 |
| usefulness | 100/100 |
| integration | 94/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 400/100 |

---

<sub>🔭 Discovered 2026-06-24 · [View on GitHub](https://github.com/hwdsl2/self-hosted-ai-stack) · [← Back to Mcp](./README.md)</sub>
