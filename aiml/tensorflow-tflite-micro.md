# tensorflow/tflite-micro

[![Stars](https://img.shields.io/github/stars/tensorflow/tflite-micro?style=flat-square&color=yellow)](https://github.com/tensorflow/tflite-micro/stargazers) [![Forks](https://img.shields.io/github/forks/tensorflow/tflite-micro?style=flat-square&color=blue)](https://github.com/tensorflow/tflite-micro/network) [![Language](https://img.shields.io/badge/lang-C%2B%2B-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-55%2F100-brightgreen?style=flat-square)](#)

> Infrastructure to enable deployment of ML models to low-power resource-constrained embedded targets (including microcontrollers and digital signal processors).

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 3k |
| 🍴 **Forks** | 1.1k |
| 💻 **Language** | C++ |
| 📈 **Score** | 55/100 |
| 🗓️ **Last push** | 2026-09-05 |
| 🔍 **Source** | github |

## 🏷️ Topics

_no topics_

## 🎯 Categories

AI/ML

## 📝 Summary

### English

**Brief Summary (2‑3 sentences)**  
TensorFlow Lite Micro (tensorflow/tflite‑micro) provides a lightweight runtime that lets you run TensorFlow‑Lite models on ultra‑low‑power embedded devices such as microcontrollers and DSPs. By abstracting the hardware‑specific details, it enables developers to add AI capabilities to constrained targets without building a custom inference stack from scratch. The project is actively maintained in C++, with a sizable community (≈3 k stars) and frequent updates.

**Value**  
- **Fast AI enablement** – You can take an existing TensorFlow model, convert it to the TFLite format, and deploy it to devices that have only a few hundred kilobytes of RAM and flash, dramatically shortening time‑to‑value for edge AI use cases.  
- **Unified tooling** – The same TensorFlow ecosystem (training, quantization, profiling) is reused, so teams avoid learning a new inference engine for each hardware platform.  
- **Portability** – A single code base supports a wide range of MCUs, development boards, and DSPs, making it easier to prototype across multiple form factors.

**Practical Adoption Path**  
1. **Model preparation** – Train in TensorFlow, then use the TFLite converter (with post‑training quantization) to generate a `.tflite` file.  
2. **Select a target** – Choose a supported microcontroller/DSP (e.g., ARM Cortex‑M, ESP32, STM32, or NXP i.MX RT). The repository includes example Makefiles and platform‑specific glue code.  
3. **Integrate the runtime** – Add `tflite-micro` as a submodule or via a package manager, compile the runtime with the appropriate micro‑kernel (CMSIS‑NN, XNNPACK, etc.), and link your model’s generated C array.  
4. **Validate** – Run the provided test harness on the target hardware, profile memory/latency, and adjust quantization or kernel selection as needed.  
5. **Deploy** – Flash the binary to the device; optionally wrap the inference call in an API that your application can invoke (e.g., sensor‑to‑action loop, RAG/agent trigger).

Because the metadata does not expose a high‑level “plug‑and‑play” integration, a manual review of the target’s build system and required kernel back‑ends is recommended before committing to the stack.

**Production Readiness**  
- **Maturity**: Medium. The project is stable for prototyping and internal pipelines, with active maintenance and a large contributor base, but it lacks formal SLAs or certified compliance kits for safety‑critical domains.  
- **Dependencies**: Relies on the TensorFlow Lite converter, CMSIS‑NN/XNNPACK kernels, and target‑specific SDKs; these must be version‑pinned and tested in CI.  
- **Operational considerations**: Verify memory footprints, real‑time latency, and power consumption on the target hardware; incorporate regression tests for model updates.  
- **Risk mitigation**: Conduct a pilot integration to assess setup cost, confirm that the required kernel implementations exist for your MCU/DSP, and establish a process for updating the runtime as TensorFlow releases evolve.  

In short, tflite‑micro is a solid foundation for adding AI to embedded products, best suited for prototypes or controlled production deployments where the integration effort can be validated early in the development cycle.

### Русский

TensorFlow Lite Micro (tflite‑micro) — это инфраструктура для развёртывания моделей машинного обучения на микроконтроллерах и DSP с ограниченными ресурсами, позволяющая добавить AI‑функциональность без создания собственного стекa с нуля. Типичный сценарий — быстрая прототипизация AI‑фич, построение RAG‑агентов или оценка новых моделей в рамках внутренних workflow, после чего проводится ручная проверка интеграции, так как автоматические сигналы о совместимости скудны. Готовность к production — средняя: проект подходит для прототипов и ограниченных внутренних задач, но требует проверки зависимостей и обслуживания перед масштабным внедрением.

### 中文

**TensorFlow Lite Micro 简介**

TensorFlow Lite Micro 是一个开源项目，用于在低功耗、资源有限的嵌入式目标（包括微控制器和数字信号处理器）上部署机器学习模型。它提供了一个基础设施，使开发者能够轻松添加 AI 能力。

**价值**

TensorFlow Lite Micro 的价值在于它可以帮助开发者快速添加 AI 能力，而无需从头开始构建模型栈。它适用于以下场景：

* prototype AI 功能
* 构建 RAG 或代理工作流
* 评估模型工具

**典型接入方式**

由于 TensorFlow Lite Micro 的集成信号在元数据中较为稀疏，因此需要进行手动检查和验证。接入方式包括：

1. 检查元数据并手动检查集成信号
2. 验证设置成本和依赖关系
3. 在内部工作流或原型中使用 TensorFlow Lite Micro

**生产可用性**

TensorFlow Lite Micro 的生产可用性为中等（Medium）。它适用于以下场景：

* 原型开发
* 内部工作流
* 需要

## 🧭 Practical evaluation

**Value:** tensorflow/tflite-micro helps add AI capability without starting from a blank model stack.

**Best use cases**

- prototype AI features
- build RAG or agent workflows
- evaluate model tooling

**Integration notes:** Needs manual inspection before adoption because integration signals are sparse in the discovered metadata.

**Production readiness:** Medium: useful for prototypes or internal workflows, with dependency and maintenance checks before production.

**Quality signals**

- 2997 GitHub stars
- 1060 forks
- updated 2026-07-13
- primary language: C++

**Risks:** Integration path is not obvious from metadata; validate setup cost before committing.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 76/100 |
| stars | 74/100 |
| topics | 0/100 |
| outlook | 65/100 |
| quality | 69/100 |
| recency | 80/100 |
| adoption | 74/100 |
| production | 65/100 |
| usefulness | 42/100 |
| integration | 30/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 100/100 |

---

<sub>🔭 Discovered 2026-07-13 · [View on GitHub](https://github.com/tensorflow/tflite-micro) · [← Back to AI/ML](./README.md)</sub>
