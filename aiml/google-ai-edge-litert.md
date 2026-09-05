# google-ai-edge/LiteRT

[![Stars](https://img.shields.io/github/stars/google-ai-edge/LiteRT?style=flat-square&color=yellow)](https://github.com/google-ai-edge/LiteRT/stargazers) [![Forks](https://img.shields.io/github/forks/google-ai-edge/LiteRT?style=flat-square&color=blue)](https://github.com/google-ai-edge/LiteRT/network) [![Language](https://img.shields.io/badge/lang-C%2B%2B-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-61%2F100-brightgreen?style=flat-square)](#)

> LiteRT, successor to TensorFlow Lite. is Google's On-device framework for high-performance ML & GenAI deployment on edge platforms, via efficient conversion, runtime, and optimization

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 2.6k |
| 🍴 **Forks** | 349 |
| 💻 **Language** | C++ |
| 📈 **Score** | 61/100 |
| 🗓️ **Last push** | 2026-09-05 |
| 🔍 **Source** | github |

## 🏷️ Topics

_no topics_

## 🎯 Categories

AI/ML

## 📝 Summary

### English

**Brief Summary (2‑3 sentences)**  
LiteRT is Google’s next‑generation on‑device inference framework, designed as the successor to TensorFlow Lite. It provides a streamlined conversion pipeline, a high‑performance C++ runtime, and a suite of edge‑focused optimizations that let developers deploy ML and generative‑AI models on constrained hardware. With over 2.5 k stars and active recent commits, LiteRT aims to accelerate prototype development and internal AI workflows without requiring a ground‑up model stack.

**Value**  
- **Fast edge deployment** – Convert TensorFlow, ONNX, or other supported formats into a lightweight binary that runs efficiently on CPUs, GPUs, and custom accelerators.  
- **Unified tooling** – The same conversion and runtime APIs support classic ML inference as well as generative‑AI (RAG, agents), reducing the need for multiple frameworks.  
- **Performance‑first design** – Low‑latency kernels, memory‑aware scheduling, and optional quantization give better throughput on microcontrollers and edge servers than many generic runtimes.

**Practical Adoption Path**  
1. **Prototype** – Use the LiteRT Python conversion CLI to ingest an existing model, generate a `.lite` artifact, and run a quick C++ or Python inference test on target hardware.  
2. **Validate** – Profile latency, memory, and accuracy; adjust quantization or operator fusion settings provided by LiteRT’s optimizer.  
3. **Integrate** – Wrap the generated runtime library into your application’s build system (CMake/Bazel) and replace the previous TensorFlow Lite calls.  
4. **Audit** – Because metadata and integration documentation are sparse, perform a manual code review, verify licensing (Apache‑2.0), and run security scans on the generated binaries before moving forward.

**Production Readiness**  
- **Maturity**: Medium. The project is actively maintained (last commit 2026‑06‑23) and has a healthy community (≈2.5 k stars, 349 forks), but integration guidance is limited, so extra engineering effort is required.  
- **Dependencies**: Primarily C++ with optional Python tooling; ensure compatibility with your build environment and any hardware‑specific SDKs.  
- **Risk Management**: No critical licensing or security red flags have been identified, but a final review of the maintainers’ activity and any disclosed CVEs is advisable before committing to production.  

Overall, LiteRT is well‑suited for teams that need to prototype edge AI quickly and are willing to invest the modest engineering overhead needed to validate and harden the integration for production use.

### Русский

LiteRT — это открытая on‑device платформа Google‑AI‑Edge, являющаяся преемником TensorFlow Lite и позволяющая быстро добавить возможности машинного обучения и генеративного ИИ на edge‑устройства благодаря эффективному конвертеру, высокопроизводительному рантайму и набору оптимизаций. Она отлично подходит для прототипирования AI‑фич, построения RAG‑ или агентных воркфлоу и оценки инструментов моделей, однако перед внедрением в продакшн требуется ручная проверка интеграции и оценка зависимости/поддержки, так как готовность к масштабному использованию пока находится на среднем уровне.

### 中文

**项目简介**  
LiteRT 是 TensorFlow Lite 的继任者，也是 Google 面向边缘设备的高性能机器学习与生成式 AI 框架。它通过高效的模型转换、轻量级运行时和多层次优化，让 AI 能力在移动端、IoT 以及其他资源受限的硬件上以极低的延迟和功耗运行。

**价值**  
- **快速落地**：无需从零搭建模型堆栈，直接将已有的 TensorFlow、ONNX、PyTorch 等模型转换为 LiteRT 格式，即可在边缘设备上运行。  
- **高性能**：针对 ARM、DSP、GPU 等硬件做了深度优化，能够在资源受限的环境中实现接近服务器级的推理速度。  
- **统一生态**：提供统一的 API 与工具链，支持原型验证、RAG（检索增强生成）以及智能体工作流的快速搭建。

**典型接入方式**  
1. **模型转换**：使用 `lite_rt_converter` 将 TensorFlow、ONNX 或 PyTorch 导出的模型转换为 LiteRT 包（`.lrt`）。  
2. **集成运行时**：在目标设备上通过 C++/Java/Kotlin 接口链接 LiteRT runtime 库，加载 `.lrt` 文件并调用 `Predict` 或 `Generate` 接口。  
3. **性能调优**：利用 LiteRT 提供的硬件调度器（如 `EdgeTPU`、`GPU`、`DSP`）和量化工具，对模型进行后处理以进一步降低延迟和功耗。  

**生产可用性**  
- **成熟度**：目前属于 **Medium** 级别，适合原型开发、内部实验或对性能有严格要求的内部业务。  
- **依赖与维护**：项目主要使用 C++，对编译链和硬件驱动有一定要求；在正式上线前需完成依赖审计、许可证合规以及安全审查。  
- **社区与活跃度**：GitHub ★2583，Fork 349，最近一次更新在 2026‑06‑23，表明项目仍在活跃维护中。  
- **风险点**：缺乏完整的元数据和集成示例，需在接入前进行手动评估；同时需确认许可证（Apache 2.0）与内部合规政策的一致性。  

总体而言，LiteRT 为需要在边缘设备上部署高效 AI 推理的团队提供了一个强大的工具链，适合作为原型验证平台或内部业务的加速器，在完成必要的审计和调优后即可逐步向生产环境迁移。

## 🧭 Practical evaluation

**Value:** google-ai-edge/LiteRT helps add AI capability without starting from a blank model stack.

**Best use cases**

- prototype AI features
- build RAG or agent workflows
- evaluate model tooling

**Integration notes:** Needs manual inspection before adoption because integration signals are sparse in the discovered metadata.

**Production readiness:** Medium: useful for prototypes or internal workflows, with dependency and maintenance checks before production.

**Quality signals**

- 2583 GitHub stars
- 349 forks
- updated 2026-06-23
- primary language: C++

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 64/100 |
| stars | 73/100 |
| topics | 0/100 |
| outlook | 67/100 |
| quality | 67/100 |
| recency | 80/100 |
| adoption | 70/100 |
| production | 67/100 |
| usefulness | 58/100 |
| integration | 46/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 100/100 |

---

<sub>🔭 Discovered 2026-06-23 · [View on GitHub](https://github.com/google-ai-edge/LiteRT) · [← Back to AI/ML](./README.md)</sub>
