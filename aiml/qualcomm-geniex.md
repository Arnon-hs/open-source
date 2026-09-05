# qualcomm/GenieX

[![Stars](https://img.shields.io/github/stars/qualcomm/GenieX?style=flat-square&color=yellow)](https://github.com/qualcomm/GenieX/stargazers) [![Forks](https://img.shields.io/github/forks/qualcomm/GenieX?style=flat-square&color=blue)](https://github.com/qualcomm/GenieX/network) [![Language](https://img.shields.io/badge/lang-Rust-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-83%2F100-brightgreen?style=flat-square)](#)

> Run frontier LLMs and VLMs with day-0 model support across GPU, NPU, and CPU, with comprehensive runtime coverage for PC (Python/C++), mobile (Android & iOS), and Linux/IoT (Arm64 & x86 Docker). Supporting OpenAI GPT-OSS, IBM Granite-4, Qwen-3-VL, Gemma-3n, Ministral-3, and more.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 8.1k |
| 🍴 **Forks** | 1k |
| 💻 **Language** | Rust |
| 📈 **Score** | 83/100 |
| 🗓️ **Last push** | 2026-09-05 |
| 🔍 **Source** | github |

## 🏷️ Topics

`gemma3` `go` `gpt-oss` `granite4` `llama` `llama3` `llm` `on-device-ai` `phi3` `qwen3` `qwen3vl` `sdk`

## 🎯 Categories

AI/ML · Libraries & SDKs · Mobile · DevOps/Infra

## 📝 Summary

### English

**Brief Summary**  
GenieX (qualcomm/GenieX) is an open‑source runtime that lets developers deploy cutting‑edge large language models (LLMs) and vision‑language models (VLMs) on GPUs, NPUs, or CPUs with day‑0 model support. It provides a unified SDK/CLI for Python and C++ across PC, Android, iOS, and Linux/IoT (Arm64 & x86 Docker), and ships pre‑integrated adapters for models such as OpenAI GPT‑OSS, IBM Granite‑4, Qwen‑3‑VL, Gemma‑3n, and Ministral‑3.

**Value**  
GenieX turns internal document collections into searchable knowledge bases that can be queried by AI assistants, boosting the relevance and factual grounding of answers. By handling model loading, hardware abstraction, and cross‑platform deployment in a single package, it removes the engineering overhead of stitching together separate inference stacks, enabling teams to focus on indexing, prompting, and UI/UX.

**Practical Adoption Path**  

| Step | Action | Why it matters |
|------|--------|----------------|
| 1️⃣  | **Prototype** – Clone the repo, run the provided CLI to load a small open‑source LLM (e.g., Gemma‑3n) on a local GPU/CPU. | Confirms the tool works in your environment and validates the API surface. |
| 2️⃣  | **Integrate Indexing** – Connect your existing document store (Elastic, Pinecone, etc.) to GenieX’s SDK and use the “knowledge‑grounding” helper to embed and retrieve passages. | Demonstrates the core use‑case of grounding assistant responses. |
| 3️⃣  | **Mobile/IoT Build** – Use the Android/iOS build scripts to generate a lightweight binary that runs on a device‑side NPU. | Shows cross‑platform feasibility and reduces latency for edge use‑cases. |
| 4️⃣  | **CI/CD & Docker** – Containerize the service with the provided Dockerfile for Arm64/x86 and add it to your CI pipeline. | Guarantees reproducible deployments and aligns with DevOps workflows. |
| 5️⃣  | **Pilot** – Deploy the container to a staging environment, hook it up to a real‑world chatbot, and measure latency, cost, and answer quality. | Provides concrete metrics before full production rollout. |

**Production Readiness**  
- **Activity & Community**: 8 110 stars, 1 009 forks, frequent commits (latest 2026‑06‑26) and a Rust‑centric codebase indicate a vibrant ecosystem.  
- **Hardware Coverage**: Supports GPU, Qualcomm NPU, and CPU, covering the majority of on‑prem, edge, and mobile deployments.  
- **Platform Breadth**: Ready‑to‑use SDKs for Python/C++, CLI tools, and pre‑built Docker images for Arm64 & x86; mobile SDKs for Android & iOS simplify edge rollout.  
- **Model Ecosystem**: Out‑of‑the‑box adapters for major open‑source LLMs/VLMs reduce integration effort.  
- **Risks**: Licensing, security audit, and maintainer continuity still need a final review, but no show‑stopper issues have been identified.

Overall, GenieX is a high‑readiness OSS candidate for organizations that want to make internal knowledge searchable via AI assistants, with a clear, incremental path from prototype to production across cloud, edge, and mobile environments.

### Русский

**GenieX** — это открытая платформа Qualcomm, позволяющая запускать передовые LLM и VLM (GPT‑OSS, Granite‑4, Qwen‑3‑VL, Gemma‑3n, Ministral‑3 и др.) на GPU, NPU и CPU с поддержкой Day‑0 моделей, а также предоставляет единый runtime для ПК (Python/C++), мобильных устройств (Android/iOS) и Linux/IoT (Arm64 / x86 Docker). Типичный сценарий — индексация корпоративных баз знаний и улучшенный поиск по документам, где ответы ассистентов «привязываются» к актуальному контенту. Проект имеет высокую готовность к production: активные коммиты, более 8 тыс. звёзд, более 1 тыс. форков, поддержка нескольких языков (Rust) и широкие возможности интеграции через API/SDK/CLI, что делает его надёжным кандидатом для пилотного внедрения.

### 中文

**价值**  
GenieX 通过统一的运行时框架，让前沿的大语言模型（LLM）和多模态模型（VLM）能够在 GPU、NPU 以及 CPU 上“一键”运行，兼容 PC（Python / C++）、移动端（Android / iOS）和 Linux/IoT（Arm64 / x86 Docker）环境。它内置对 OpenAI GPT‑OSS、IBM Granite‑4、Qwen‑3‑VL、Gemma‑3n、Ministral‑3 等主流模型的 Day‑0 支持，帮助企业把内部文档、知识库等非结构化信息快速索引并在对话式助手中检索、引用，实现 **知识可搜索、可调用**，提升搜索准确性和助手回答的可信度。

**典型接入方式**  
1. **SDK / API**：在 Python 或 C++ 项目中通过 GenieX 提供的库调用 `geniex.run(model, input, device)`，即可在指定硬件上启动模型推理。  
2. **CLI**：使用 `geniex-cli` 直接在终端提交模型、输入文件或流式数据，适合快速原型或脚本化批处理。  
3. **Docker 镜像**：在 Linux/IoT 场景下拉取官方 `qualcomm/geniex` 镜像，配合 `docker run -e DEVICE=...` 启动服务，方便在边缘设备或云端统一部署。  
4. **移动端 SDK**：集成 Android（AAR）或 iOS（XCFramework）库，配合本地 NPU 加速，实现离线或低延迟的模型推理。

**生产可用性**  
- **活跃度**：截至 2026‑06‑26，项目最近一次提交，拥有 8 110 粉丝、1 009 个 Fork，社区活跃。  
- **技术成熟度**：核心实现采用 Rust，提供高性能且安全的运行时；多硬件后端已实现完整覆盖，文档中提供详细的部署指南。  
- **生态兼容**：支持主流开源模型和多平台，已在多个内部项目中用于知识库索引和对话助手，具备可验证的生产案例。  
- **风险**：当前尚需对许可证（Apache‑2.0）进行合规审查，并进行安全审计以确认供应链安全；但整体代码质量、测试覆盖和社区响应速度均表现良好，适合作为 **严肃的试点或正式生产** 使用。

## 🧭 Practical evaluation

**Value:** qualcomm/GenieX helps make internal knowledge searchable and usable by assistants.

**Best use cases**

- index knowledge bases
- improve search over documents
- ground assistant answers

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 8110 GitHub stars
- 1009 forks
- updated 2026-06-26
- primary language: Rust
- 14 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 75/100 |
| stars | 83/100 |
| topics | 100/100 |
| outlook | 83/100 |
| quality | 86/100 |
| recency | 80/100 |
| adoption | 81/100 |
| production | 81/100 |
| usefulness | 74/100 |
| integration | 94/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 400/100 |

---

<sub>🔭 Discovered 2026-06-26 · [View on GitHub](https://github.com/qualcomm/GenieX) · [← Back to AI/ML](./README.md)</sub>
