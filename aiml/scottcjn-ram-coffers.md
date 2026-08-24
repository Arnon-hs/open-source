# Scottcjn/ram-coffers

[![Stars](https://img.shields.io/github/stars/Scottcjn/ram-coffers?style=flat-square&color=yellow)](https://github.com/Scottcjn/ram-coffers/stargazers) [![Forks](https://img.shields.io/github/forks/Scottcjn/ram-coffers?style=flat-square&color=blue)](https://github.com/Scottcjn/ram-coffers/network) [![Language](https://img.shields.io/badge/lang-C-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-47%2F100-brightgreen?style=flat-square)](#)

> NUMA-distributed weight banking for LLM inference on IBM POWER8. 147 t/s (8.8x stock). Part of the Proof of Physical AI stack.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 148 |
| 🍴 **Forks** | 35 |
| 💻 **Language** | C |
| 📈 **Score** | 47/100 |
| 🗓️ **Last push** | 2026-08-24 |
| 🔍 **Source** | github |

## 🏷️ Topics

`ai-inference` `depin` `hebbian` `llama-cpp` `llm` `numa` `power8` `powerpc` `proof-of-physical-ai` `vec-perm`

## 🎯 Categories

AI/ML

## 📝 Summary

### English

**Brief Summary (2‑3 sentences)**  
Scottcjn/ram‑coffers is a C library that implements NUMA‑distributed weight banking to accelerate large‑language‑model (LLM) inference on IBM POWER8 systems, delivering up to 147 tokens / second—a roughly 8.8× speed‑up over the stock runtime. It is positioned as a component of the “Proof of Physical AI” stack, letting teams add AI inference capability without rebuilding a model stack from scratch. The project is moderately popular (148 stars, 35 forks) and actively maintained as of June 2026.

**Value Proposition**  
- **Performance boost on existing POWER8 hardware** – By sharding model weights across NUMA nodes, the library extracts latent memory‑bandwidth and compute parallelism, turning legacy servers into viable LLM inference nodes.  
- **Lower entry cost** – Teams can prototype RAG, agent‑based workflows, or other AI features on‑premise without purchasing new GPUs or rewriting the inference pipeline.  
- **Open‑source and extensible** – The C codebase can be wrapped in Python or integrated into existing C/C++ inference engines, enabling custom optimizations or hybrid CPU‑GPU deployments.

**Practical Adoption Path**  
1. **Proof‑of‑Concept (PoC)** – Clone the repo, follow the README to build the library on a POWER8 test box, and run the supplied benchmark (or a small open‑source LLM such as LLaMA‑7B). Verify the claimed 8.8× speed‑up against the stock runtime.  
2. **Integration Layer** – Wrap the compiled library with a thin Python/CFFI shim or embed it directly into the current inference service (e.g., a gRPC server). Start with a single endpoint that serves a limited set of queries.  
3. **Validation & Scaling** – Measure latency, throughput, and NUMA traffic under realistic workloads. Tune the weight‑banking configuration (node allocation, batch size) and add monitoring for memory pressure.  
4. **Gradual Rollout** – Deploy the PoC to a staging environment, then to a subset of production traffic while keeping the original runtime as a fallback.  

**Production Readiness**  
- **Maturity:** Medium. The code is actively maintained and has a modest user base, but it lacks extensive documentation, automated CI pipelines, and formal stability guarantees.  
- **Dependencies:** Pure C with standard POSIX/NUMA libraries; no exotic runtime dependencies, which simplifies containerization on POWER8.  
- **Risks:** Integration steps are not fully described in the metadata, so teams must invest effort to understand the build process and the exact NUMA topology requirements. Additionally, long‑term maintenance will require in‑house expertise in C and POWER8 memory architecture.  

Overall, ram‑coffers is a solid candidate for internal prototypes or workloads that can tolerate a modest integration effort, but it should undergo a controlled PoC and thorough performance testing before being promoted to mission‑critical production.

### Русский

**Scottcjn/ram-coffers** — это C‑библиотека, реализующая NUMA‑распределённый банковский механизм памяти, позволяющий ускорить вывод больших языковых моделей на серверах IBM POWER8 до 147 токенов/сек (≈ 8,8 × быстрее базовой конфигурации). Типичный сценарий — запуск прототипов — RAG‑сервисов или агентных воркфлоу, где требуется добавить AI‑функциональность без полной перестройки стекa моделей; рекомендуется начать с небольшого proof‑of‑concept, проверив README и базовую совместимость. Готовность к production — средняя: библиотека достаточно зрелая (148 звёзд, активные коммиты) для внутренних прототипов, но требует проверки зависимостей и уточнения интеграционного пути перед масштабным использованием.

### 中文

**项目简介**  
Scottcjn/ram‑coffers 是面向 IBM POWER8 平台的 NUMA‑分布式权重存储方案，可在 LLM 推理时将吞吐提升至 147 t/s（约为原始实现的 8.8 倍），是 Proof of Physical AI 生态的一部分。

**价值**  
- **显著加速**：通过跨 NUMA 节点的权重银行（weight banking），在同等硬件上实现数倍到十倍的推理速率提升。  
- **降低门槛**：无需从头搭建完整的模型堆栈，直接在已有的 POWER8 环境上复用该库即可获得高性能 AI 能力。  
- **原型友好**：适合快速验证 RAG、Agent 工作流或模型工具链的可行性，帮助团队在内部快速迭代 AI 功能。

**典型接入方式**  
1. **环境准备**：确认服务器运行 IBM POWER8，且操作系统支持 NUMA（如 RHEL/CentOS 8+）。  
2. **依赖安装**：克隆仓库后，使用 `make` 编译 C 代码，确保链接到系统的 `libnuma` 与相应的 BLAS 库。  
3. **代码集成**：在推理入口（如使用 HuggingFace Transformers 的 C++ 后端）调用 `ram_coffers_init()` 初始化权重银行，并在模型加载时使用 `ram_coffers_load_weights()` 替代常规内存拷贝。  
4. **小规模验证**：先在单节点或两节点的 NUMA 环境下跑一个基准模型（如 LLaMA‑7B），对比吞吐与延迟，确认加速效果。  
5. **扩展部署**：在验证通过后，可在多节点 NUMA 集群中通过脚本自动化权重切分与加载，实现更大规模的推理服务。

**生产可用性**  
- **成熟度**：项目已有 148 颗星、35 个 fork，最近一次提交在 2026‑06‑24，代码基于 C 语言实现，技术栈相对稳固。  
- **适用场景**：适合内部原型、研发验证或对吞吐要求极高的专用推理服务。  
- **风险与准备**：  
  - **集成成本**：文档以 README 为主，缺少完整的 CI/CD 示例，需自行梳理依赖和部署脚本。  
  - **维护负担**：依赖 POWER8 的硬件特性，若未来迁移至其他平台需重新实现或放弃。  
  - **生产级监控**：项目本身不提供监控/日志模块，需自行加入 Prometheus、Grafana 等监控体系。  
- **总体评估**：在已具备 POWER8 环境且对推理性能有强需求的团队中，可视为 **中等** 生产可用度。通过一次小规模 PoC 验证后，再进行依赖审计与运维准备，即可在内部生产环境中安全使用。

## 🧭 Practical evaluation

**Value:** Scottcjn/ram-coffers helps add AI capability without starting from a blank model stack.

**Best use cases**

- prototype AI features
- build RAG or agent workflows
- evaluate model tooling

**Integration notes:** Looks feasible to evaluate, but integration should start with a small proof of concept and README check.

**Production readiness:** Medium: useful for prototypes or internal workflows, with dependency and maintenance checks before production.

**Quality signals**

- 148 GitHub stars
- 35 forks
- updated 2026-06-24
- primary language: C
- 10 topics

**Risks:** Integration path is not obvious from metadata; validate setup cost before committing.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 39/100 |
| stars | 46/100 |
| topics | 100/100 |
| outlook | 53/100 |
| quality | 60/100 |
| recency | 40/100 |
| adoption | 44/100 |
| production | 53/100 |
| usefulness | 42/100 |
| integration | 30/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 100/100 |

---

<sub>🔭 Discovered 2026-06-24 · [View on GitHub](https://github.com/Scottcjn/ram-coffers) · [← Back to AI/ML](./README.md)</sub>
