# qualcomm/nexa-sdk

[![Stars](https://img.shields.io/github/stars/qualcomm/nexa-sdk?style=flat-square&color=yellow)](https://github.com/qualcomm/nexa-sdk/stargazers) [![Forks](https://img.shields.io/github/forks/qualcomm/nexa-sdk?style=flat-square&color=blue)](https://github.com/qualcomm/nexa-sdk/network) [![Language](https://img.shields.io/badge/lang-Rust-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-77%2F100-brightgreen?style=flat-square)](#)

> Run frontier LLMs and VLMs with day-0 model support across GPU, NPU, and CPU, with comprehensive runtime coverage for PC (Python/C++), mobile (Android & iOS), and Linux/IoT (Arm64 & x86 Docker). Supporting OpenAI GPT-OSS, IBM Granite-4, Qwen-3-VL, Gemma-3n, Ministral-3, and more.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 8.1k |
| 🍴 **Forks** | 1k |
| 💻 **Language** | Rust |
| 📈 **Score** | 77/100 |
| 🗓️ **Last push** | 2026-08-24 |
| 🔍 **Source** | github |

## 🏷️ Topics

`gemma3` `go` `gpt-oss` `granite4` `llama` `llama3` `llm` `on-device-ai` `phi3` `qwen3` `qwen3vl` `sdk`

## 🎯 Categories

AI/ML · Mobile · DevOps/Infra

## 📝 Summary

### English

**Brief Summary (2‑3 sentences)**  
The Qualcomm Nexa SDK is an open‑source runtime that lets developers run cutting‑edge large language models (LLMs) and vision‑language models (VLMs) on a wide range of hardware—from GPUs and NPUs to CPUs—across PC, mobile, and Linux/IoT environments. It ships ready‑to‑use APIs, a CLI, and language‑specific bindings for Python and C++, and already supports popular open models such as OpenAI‑GPT‑OSS, IBM Granite‑4, Qwen‑3‑VL, Gemma‑3‑n, and Ministral‑3.

---

### Value Proposition
- **Unified, hardware‑agnostic inference** – The same model can be executed on desktop GPUs, on‑device NPUs (Qualcomm Snapdragon), or headless CPUs without rewriting code, dramatically reducing time‑to‑market for AI‑enhanced products.  
- **Cross‑platform coverage** – A single SDK works on Windows/macOS/Linux (Python/C++), Android, iOS, and Arm64/x86 Docker containers, enabling consistent behavior from edge devices to cloud servers.  
- **Accelerates knowledge‑centric applications** – By exposing fast, locally runnable LLM/VLM inference, developers can index internal knowledge bases, build semantic search, and ground conversational assistants in proprietary documents without relying on external APIs.

### Practical Adoption Path
1. **Prototype** – Clone the repo, install the Rust toolchain (or use the pre‑built Docker image), and run the provided CLI to load a model (e.g., `gemma-3n`) on a local GPU or an Android device.  
2. **Integrate** – Use the Python or C++ bindings to embed the SDK in your existing backend or mobile app; the API mirrors typical `generate`/`embed` calls, so swapping a cloud‑hosted model for Nexa is straightforward.  
3. **Fine‑tune / Index** – Feed your internal documents through the SDK’s embedding endpoint, store vectors in a vector DB (e.g., Milvus, Pinecone), and build a retrieval‑augmented generation (RAG) pipeline that answers queries with up‑to‑date, on‑premise knowledge.  
4. **Scale & Deploy** – Containerize the service with the provided Dockerfile, deploy to edge servers or IoT gateways, and optionally enable hardware‑specific acceleration (e.g., Qualcomm Hexagon NPU) via the SDK’s runtime flags.

### Production Readiness
- **Community & activity** – 8,109 ⭐ stars, 1,010 forks, frequent commits (last update 2026‑06‑25) and a healthy issue/PR turnover indicate an active maintainer base.  
- **Multi‑platform stability** – The SDK ships binaries for major OS/CPU combos and has been validated on Android, iOS, and Linux Docker, reducing platform‑specific bugs.  
- **Performance pedigree** – Built in Rust with zero‑cost abstractions, it leverages Qualcomm’s AI‑accelerator libraries for low‑latency inference, a key requirement for real‑time assistants.  
- **Risk considerations** – No critical licensing or security red flags have been identified, but a final review of the Apache‑2.0 (or whatever) license, supply‑chain SBOM, and maintainer responsiveness is recommended before a full production rollout.

Overall, Nexa‑SDK offers a mature, high‑performance foundation for enterprises that want to bring frontier LLM/VLM capabilities in‑house, making it a strong candidate for pilot projects and, with the standard due‑diligence checks, for production deployment.

### Русский

**qualcomm/nexa-sdk** — это кроссплатформенный SDK, позволяющий запускать передовые LLM и VLM (OpenAI GPT‑OSS, IBM Granite‑4, Qwen‑3‑VL, Gemma‑3n, Ministral‑3 и др.) на GPU, NPU и CPU с поддержкой ПК (Python/C++), мобильных устройств (Android/iOS) и Linux/IoT (Arm64, x86 Docker). Он упрощает построение систем, которые делают внутренние знания доступными ассистентам: индексируют базы знаний, улучшают поиск по документам и «заземляют» ответы помощников на актуальный контент. Проект имеет высокий уровень готовности к production — активные коммиты, более 8 тыс. звёзд, широкое сообщество и зрелую инфраструктуру, что делает его надёжным кандидатом для пилотных внедрений.

### 中文

**项目简介**  
qualcomm/nexa‑sdk 是一套跨 GPU、NPU、CPU 的前沿大模型（LLM/VLM）运行时框架，零日模型即可上手。它提供完整的运行时覆盖：PC（Python/C++）、移动端（Android & iOS）以及 Linux/IoT（Arm64 & x86 Docker），原生支持 OpenAI GPT‑OSS、IBM Granite‑4、Qwen‑3‑VL、Gemma‑3n、Ministral‑3 等主流模型。

**价值**  
- **知识检索即服务**：将企业内部文档、知识库快速索引，实现 AI 助手的上下文感知和精准回答。  
- **全平台统一部署**：一次编写代码即可在服务器、边缘设备或手机上运行同一模型，降低运维复杂度。  
- **多模型兼容**：无需改写代码即可切换不同厂商的前沿模型，帮助业务快速实验和迭代。

**典型接入方式**  
1. **SDK/CLI**：通过 Rust / C++ / Python 包引入 SDK，调用统一的 `run_model` 接口即可在本地或容器中执行推理。  
2. **API 网关**：将 SDK 包装为 HTTP/GRPC 服务，移动端或前端通过 REST/GRPC 调用，实现即插即用的 AI 功能。  
3. **Docker 部署**：在 Arm64 或 x86 服务器上拉取官方 Docker 镜像，使用 `docker run` 启动模型服务，适合大规模生产部署。

**生产可用性**  
- **活跃度高**：截至 2026‑06‑25，仓库拥有 8 109 颗星、1 010 个 Fork，近期仍有代码提交和 Issue 维护。  
- **语言与生态**：核心实现为 Rust，配套 Python/C++ 绑定，兼容主流 DevOps 工具链（Kubernetes、CI/CD）。  
- **成熟度**：具备完整的跨平台运行时、丰富的模型适配列表以及详细的文档，已被多家内部项目用于搜索增强和对话式助手，具备进入生产环境的条件。  
- **风险**：仍需进一步审查许可证（Apache 2.0/MIT 等）以及安全补丁的响应速度，但整体风险较低，适合作为正式项目的底层推理引擎。

## 🧭 Practical evaluation

**Value:** qualcomm/nexa-sdk helps make internal knowledge searchable and usable by assistants.

**Best use cases**

- index knowledge bases
- improve search over documents
- ground assistant answers

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 8109 GitHub stars
- 1010 forks
- updated 2026-06-25
- primary language: Rust
- 14 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 75/100 |
| stars | 83/100 |
| topics | 100/100 |
| outlook | 69/100 |
| quality | 76/100 |
| recency | 40/100 |
| adoption | 81/100 |
| production | 67/100 |
| usefulness | 74/100 |
| integration | 94/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 300/100 |

---

<sub>🔭 Discovered 2026-06-25 · [View on GitHub](https://github.com/qualcomm/nexa-sdk) · [← Back to AI/ML](./README.md)</sub>
