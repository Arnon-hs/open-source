# uxlfoundation/oneDNN

[![Stars](https://img.shields.io/github/stars/uxlfoundation/oneDNN?style=flat-square&color=yellow)](https://github.com/uxlfoundation/oneDNN/stargazers) [![Forks](https://img.shields.io/github/forks/uxlfoundation/oneDNN?style=flat-square&color=blue)](https://github.com/uxlfoundation/oneDNN/network) [![Language](https://img.shields.io/badge/lang-C%2B%2B-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-68%2F100-brightgreen?style=flat-square)](#)

> oneAPI Deep Neural Network Library (oneDNN)

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 4k |
| 🍴 **Forks** | 1.1k |
| 💻 **Language** | C++ |
| 📈 **Score** | 68/100 |
| 🗓️ **Last push** | 2026-09-05 |
| 🔍 **Source** | github |

## 🏷️ Topics

`aarch64` `amx` `avx512` `bfloat16` `cpp` `deep-learning` `deep-neural-networks` `library` `oneapi` `onednn` `openmp` `performance`

## 🎯 Categories

AI/ML

## 📝 Summary

### English

**Summary**  
oneDNN (oneAPI Deep Neural Network Library) is an open‑source C++ library that provides highly‑optimized primitives for deep‑learning workloads across CPUs, GPUs and accelerators. With over 4 000 GitHub stars, active maintenance (last commit 2026‑06‑25) and a large fork base, it lets teams reuse proven backend infrastructure—API/SDK/CLI interfaces and language metadata—rather than rebuilding common neural‑network kernels from scratch. This accelerates the delivery of API services, standardizes service patterns, and reduces engineering overhead.

**Value**  
By abstracting low‑level performance optimizations into a single, well‑documented library, oneDNN lets developers focus on business logic while benefiting from Intel’s extensive hardware‑specific tuning. The library’s broad hardware support and stable API enable consistent performance across heterogeneous environments, lowering total cost of ownership for AI‑centric backends.

**Practical adoption path**  
1. **Evaluation** – Clone the repo, run the provided CMake/CLI examples, and benchmark the primitives against existing workloads.  
2. **Integration** – Replace custom kernels with oneDNN calls via its C++ API or the language bindings (Python, Java) that wrap the core library.  
3. **Testing & CI** – Add oneDNN’s unit‑test suite to your CI pipeline to verify compatibility with your target hardware and OS.  
4. **Roll‑out** – Deploy the updated services behind feature flags, monitor latency/throughput, and gradually expand usage to other micro‑services.

**Production readiness**  
The project scores high on production readiness: recent commits, a vibrant contributor community, extensive adoption in major frameworks (e.g., TensorFlow, PyTorch), and strong ecosystem signals (1148 forks, 18 topical tags). While the license (Apache 2.0) and security posture appear clean, a final review of maintainers’ responsiveness and any disclosed CVEs is advisable before committing to a large‑scale pilot.

### Русский

**oneDNN** — это высокопроизводительная open‑source библиотека для ускорения нейронных сетей, предоставляющая готовые реализации API/SDK/CLI и метаданные, которые позволяют командам быстро переиспользовать общую инфраструктуру бэкенда вместо её собственного построения. Типичный сценарий — ускоренная доставка API‑сервисов: подключаете библиотеку, берёте проверенные паттерны и стандарты сервисов и сразу получаете стабильную, оптимизированную вычислительную основу. Проект имеет высокий уровень готовности к продакшн: активные коммиты, широкое принятие (4010 звёзд, 1148 форков), поддержка C++ и обширный набор тем, однако перед масштабным внедрением рекомендуется окончательная проверка лицензии, безопасности и активности мейнтейнеров.

### 中文

**项目简介**  
oneDNN（oneAPI Deep Neural Network Library）是由 uxlfoundation 维护的高性能深度学习算子库，提供 C++、C 和 Python 接口，帮助开发者在 CPU、GPU、加速器等多种硬件上实现高效的神经网络推理和训练。  

**价值**  
- **复用后端能力**：将常用的计算、内存管理、调度等基础设施封装为统一的 API，团队无需重复实现底层加速逻辑。  
- **加速交付**：通过标准化的算子实现和跨硬件优化，能够显著缩短 API 服务和模型部署的开发周期。  
- **统一模式**：提供统一的编程模型和性能基准，便于在不同项目间保持后端实现的一致性。  

**典型接入方式**  
1. **作为库依赖**：在 CMake 或 Bazel 项目中直接引用 `oneDNN`，链接对应的静态/动态库。  
2. **通过 Python 包**：`pip install onednn`（或 `pip install intel‑one‑dnn`）后即可在脚本或 Flask/Django 等服务中调用 `onednn` 接口。  
3. **CLI/SDK**：使用官方提供的 `onednn-cli` 检查硬件支持、生成算子配置文件，或通过 SDK 完成自定义算子注册。  

**生产可用性**  
- **活跃度高**：截至 2026‑06‑25，项目拥有 4 010+ Stars、1 148+ Forks，最近一次提交在 2026‑06‑25，说明仍在积极维护。  
- **生态成熟**：被多家主流框架（如 TensorFlow、PyTorch）以及 Intel 的 oneAPI 生态所采纳，具备完整的 CI/CD、自动化测试和安全审计流程。  
- **部署准备**：提供多平台二进制（Linux、Windows、macOS）和容器镜像，支持静态链接，便于在容器化或裸机环境中直接上线。  

总体来看，oneDNN 已具备高水平的社区认可、代码质量和跨硬件性能保证，是在后端服务中复用深度学习基础设施、加速模型上线的可靠 OSS 选型。

## 🧭 Practical evaluation

**Value:** uxlfoundation/oneDNN helps teams reuse service infrastructure instead of rebuilding common backend pieces.

**Best use cases**

- ship API services faster
- reuse backend infrastructure
- standardize service patterns

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 4010 GitHub stars
- 1148 forks
- updated 2026-06-25
- primary language: C++
- 18 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 77/100 |
| stars | 77/100 |
| topics | 100/100 |
| outlook | 79/100 |
| quality | 84/100 |
| recency | 80/100 |
| adoption | 77/100 |
| production | 73/100 |
| usefulness | 58/100 |
| integration | 46/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 100/100 |

---

<sub>🔭 Discovered 2026-06-25 · [View on GitHub](https://github.com/uxlfoundation/oneDNN) · [← Back to AI/ML](./README.md)</sub>
