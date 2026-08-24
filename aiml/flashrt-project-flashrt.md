# flashrt-project/FlashRT

[![Stars](https://img.shields.io/github/stars/flashrt-project/FlashRT?style=flat-square&color=yellow)](https://github.com/flashrt-project/FlashRT/stargazers) [![Forks](https://img.shields.io/github/forks/flashrt-project/FlashRT?style=flat-square&color=blue)](https://github.com/flashrt-project/FlashRT/network) [![Language](https://img.shields.io/badge/lang-C%2B%2B-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-53%2F100-brightgreen?style=flat-square)](#)

> FlashRT is a high-performance realtime inference engine for small-batch, latency-sensitive AI workloads. The flagship integration is production VLA control for Pi0, Pi0.5, GROOT N1.6, and Pi0-FAST. Also support llm e.g, qwen3.6-27B

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 387 |
| 🍴 **Forks** | 46 |
| 💻 **Language** | C++ |
| 📈 **Score** | 53/100 |
| 🗓️ **Last push** | 2026-08-24 |
| 🔍 **Source** | github |

## 🏷️ Topics

`cuda` `cuda-kernels` `gr00t` `gr00t-n1-6-3b` `jetson` `jetson-orin` `jetson-thor` `motus` `pi` `pi05` `qwen` `qwen3-6`

## 🎯 Categories

AI/ML

## 📝 Summary

### English

**Project Summary:**

FlashRT is an open-source, high-performance real-time inference engine for small-batch, latency-sensitive AI workloads. It enables the addition of AI capabilities without requiring a complete model stack from scratch, making it ideal for prototyping AI features, building RAG or agent workflows, and evaluating model tooling. With its flexible integration capabilities, FlashRT can be used in a variety of use cases, from internal workflows to production environments.

**Value:**

The primary value proposition of FlashRT lies in its ability to add AI capability without requiring a comprehensive model stack. This allows developers to focus on building AI-powered applications without the overhead of designing and implementing a complete AI infrastructure. By leveraging FlashRT, developers can quickly prototype AI features, build RAG or agent workflows, and evaluate model tooling, making it an attractive option for those looking to integrate AI into their applications.

**Practical Adoption Path:**

The practical adoption path for FlashRT involves several steps:

1. **Evaluate and Understand**: Review the FlashRT documentation and README to gain a deeper understanding of its capabilities and limitations.
2. **Small Proof of Concept**: Start with a small proof of concept to validate the setup cost and feasibility of integrating FlashRT into your project.
3. **Integration**: Once the

### Русский

FlashRT — это высокопроизводительный движок для реального времени inference, оптимизированный под небольшие батчи и чувствительные к задержкам задачи ИИ; он позволяет быстро добавить AI‑функциональность (прототипы, RAG‑агенты, оценку моделей) без необходимости строить стек с нуля. Типовое внедрение начинается с небольшого proof‑of‑concept — проверка README и базовой интеграции в существующий пайплайн, после чего можно разворачивать контроль VLA для Pi0/Pi0.5/GROOT N1.6/Pi0‑FAST или использовать LLM (например, qwen3.6‑27B). Готовность к production — средняя: проект подходит для прототипов и внутренних процессов, но требует проверки зависимостей и сопровождения перед масштабным запуском.

### 中文

**项目简介**  
FlashRT 是面向小批量、对时延极为敏感的 AI 推理场景的高性能实时推理引擎。它已在 Pi0、Pi0.5、GROOT N1.6、Pi0‑FAST 等生产级 VLA 控制系统中落地，并且支持大模型（如 Qwen3.6‑27B）等 LLM 场景。

**价值**  
- **快速赋能**：无需从头搭建模型堆栈，直接在现有代码库中加入高效推理能力。  
- **低时延**：针对小批量请求进行深度优化，适合实时控制、交互式问答等对响应速度有严格要求的业务。  
- **多场景适配**：既可用于嵌入式控制系统的 AI 增强，也能支撑 RAG、Agent 工作流等更复杂的 LLM 应用。

**典型接入方式**  
1. **阅读 README & 示例**：项目提供了最小化的 C++ 示例，帮助快速验证环境依赖（CUDA、cuDNN、编译器等）。  
2. **构建库**：使用 CMake 编译生成 `libflashrt.so`，并在目标项目的 CMakeLists 中通过 `target_link_libraries` 引入。  
3. **模型加载**：调用 FlashRT 提供的 API（如 `FlashRT::Engine::loadModel(path)`）加载 ONNX/Transformer 模型。  
4. **推理调用**：在业务代码中创建推理会话，传入小批量输入张量，获取低时延的输出。  
5. **小规模 POC**：先在测试环境跑通一个“单模型‑单任务”的原型，确认性能与兼容性后再扩展到完整工作流。

**生产可用性**  
- **成熟度**：GitHub ★387、Fork 46，活跃更新至 2026‑07‑01，代码以 C++ 为主，社区活跃度中等。  
- **适用范围**：适合作为原型验证、内部工具或对时延要求极高的边缘部署；在正式生产环境使用前，需要完成依赖审计、异常监控和容灾方案。  
- **风险**：项目文档对完整的集成路径描述有限，建议在正式上线前进行一次完整的安装‑验证‑性能基准测试，评估维护成本与升级策略。  

总体而言，FlashRT 为需要低时延 AI 推理的产品提供了即插即用的高性能后端，适合先做小规模验证，再逐步在生产环境中推广。

## 🧭 Practical evaluation

**Value:** flashrt-project/FlashRT helps add AI capability without starting from a blank model stack.

**Best use cases**

- prototype AI features
- build RAG or agent workflows
- evaluate model tooling

**Integration notes:** Looks feasible to evaluate, but integration should start with a small proof of concept and README check.

**Production readiness:** Medium: useful for prototypes or internal workflows, with dependency and maintenance checks before production.

**Quality signals**

- 387 GitHub stars
- 46 forks
- updated 2026-07-01
- primary language: C++
- 19 topics

**Risks:** Integration path is not obvious from metadata; validate setup cost before committing.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 42/100 |
| stars | 55/100 |
| topics | 100/100 |
| outlook | 58/100 |
| quality | 63/100 |
| recency | 40/100 |
| adoption | 51/100 |
| production | 54/100 |
| usefulness | 58/100 |
| integration | 30/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 100/100 |

---

<sub>🔭 Discovered 2026-07-01 · [View on GitHub](https://github.com/flashrt-project/FlashRT) · [← Back to AI/ML](./README.md)</sub>
