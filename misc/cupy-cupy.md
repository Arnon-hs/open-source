# cupy/cupy

[![Stars](https://img.shields.io/github/stars/cupy/cupy?style=flat-square&color=yellow)](https://github.com/cupy/cupy/stargazers) [![Forks](https://img.shields.io/github/forks/cupy/cupy?style=flat-square&color=blue)](https://github.com/cupy/cupy/network) [![Language](https://img.shields.io/badge/lang-Python-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-65%2F100-brightgreen?style=flat-square)](#)

> NumPy & SciPy for GPU

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 11k |
| 🍴 **Forks** | 1k |
| 💻 **Language** | Python |
| 📈 **Score** | 65/100 |
| 🗓️ **Last push** | 2026-09-05 |
| 🔍 **Source** | github |

## 🏷️ Topics

`cublas` `cuda` `cudnn` `cupy` `curand` `cusolver` `cusparse` `cusparselt` `cutensor` `gpu` `nccl` `numpy`

## 🎯 Categories

Misc

## 📝 Summary

### English

**Summary**  
CuPy is a NumPy‑compatible library that runs array operations on NVIDIA GPUs, offering a drop‑in replacement for many SciPy and NumPy functions. With over 11 k stars, active maintenance, and recent commits, it is mature enough for a serious pilot in GPU‑accelerated workloads.  

**Value**  
CuPy lets existing Python data‑science codebases leverage GPU acceleration with minimal code changes, delivering large speedups for linear‑algebra, FFT, and deep‑learning preprocessing pipelines while preserving the familiar NumPy API.  

**Adoption Path**  
Start with a small proof‑of‑concept: identify a performance‑critical NumPy/SciPy component, replace its imports with `cupy` and run the existing test suite to verify correctness. Validate the README examples, check compatibility with your CUDA version, and progressively expand the substitution to larger modules once benchmarks confirm the expected gains.  

**Production Readiness**  
The project shows high production readiness: recent activity (last commit 2026‑06‑24), a large and active community, extensive documentation, and broad ecosystem adoption (e.g., integration with Dask, RAPIDS, and deep‑learning frameworks). After a final review of the license, security posture, and maintainer responsiveness, CuPy can be safely promoted from pilot to production for GPU‑enabled Python workloads.

### Русский

**Краткое резюме:** CuPy («NumPy & SciPy for GPU») предоставляет почти идентичный API к популярным библиотекам NumPy и SciPy, но ускоряет вычисления за счёт выполнения массивных операций на видеокартах NVIDIA/CUDA. Типичный сценарий внедрения — микросервис или аналитический пайплайн, где уже используется NumPy‑код и требуется порядок‑мagnitude ускорения; начинать стоит с небольшого proof‑of‑concept, проверив совместимость кода и README‑примеров. По готовности к production проект находится на высоком уровне: активные коммиты, более 11 k звёзд, широкое принятие в сообществе и зрелая экосистема, однако перед масштабным запуском следует финально оценить лицензию, безопасность и наличие активных мейнтейнеров.

### 中文

**项目简介**  
CuPy（`cupy/cupy`）是面向 GPU 的 NumPy 与 SciPy 实现，提供与 NumPy 完全兼容的 API，让已有的科学计算、机器学习和深度学习代码几乎不做修改即可在 NVIDIA GPU 上加速运行。

**价值**  
- **即插即用**：只需将 `import numpy as np` 替换为 `import cupy as cp`（或在代码中使用 `cp.asarray`），即可把数组运算迁移到 GPU。  
- **生态兼容**：支持大多数 NumPy、SciPy、Numba、scikit‑learn 等库的接口，方便在现有 Python 科学计算栈中引入 GPU 加速。  
- **高性能**：基于 CUDA 实现，提供 BLAS、FFT、稀疏矩阵等高效算子，显著提升大规模矩阵、向量和信号处理任务的执行速度。

**典型接入方式**  
1. **阅读 README 与示例**：确认项目的 CUDA 版本要求与本地环境匹配。  
2. **小范围 PoC**：在现有工作流中挑选一个计算密集的函数（如矩阵乘法、卷积），用 `cupy` 重写并对比 CPU 与 GPU 的运行时间。  
3. **包装层**：如果代码中混用 NumPy 与 CuPy，可使用 `cupy.asnumpy` / `cupy.asarray` 在 CPU 与 GPU 之间转换数据。  
4. **CI 测试**：在 CI 环境中加入 CUDA 镜像或 GPU 实例，确保依赖、版本和性能基准持续可用。

**生产可用性**  
- **活跃度**：截至 2026‑06‑24，项目仍在积极维护，最近一次提交仅数天前；拥有 11 k+ 星、1 k+ Fork，社区活跃。  
- **成熟度**：已被多家深度学习框架（如 Chainer、PyTorch 的部分后端）以及科研项目采用，具备生产级别的稳定性。  
- **风险**：需进一步审查许可证（BSD‑3‑Clause）兼容性、依赖的 CUDA 版本安全性以及维护者的响应速度，但整体风险较低。  

综上，CuPy 是在已有 Python 科学计算代码上快速实现 GPU 加速的首选方案，适合先做小规模验证，随后在生产环境中逐步推广。

## 🧭 Practical evaluation

**Value:** cupy/cupy may be useful when its README and activity match a concrete workflow.

**Best use cases**

- Not enough metadata yet.

**Integration notes:** Looks feasible to evaluate, but integration should start with a small proof of concept and README check.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 11008 GitHub stars
- 1040 forks
- updated 2026-06-24
- primary language: Python
- 18 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 75/100 |
| stars | 86/100 |
| topics | 100/100 |
| outlook | 77/100 |
| quality | 87/100 |
| recency | 80/100 |
| adoption | 83/100 |
| production | 74/100 |
| usefulness | 42/100 |
| integration | 46/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 0/100 |

---

<sub>🔭 Discovered 2026-06-24 · [View on GitHub](https://github.com/cupy/cupy) · [← Back to Misc](./README.md)</sub>
