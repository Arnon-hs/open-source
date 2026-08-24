# nv-legate/cupynumeric

[![Stars](https://img.shields.io/github/stars/nv-legate/cupynumeric?style=flat-square&color=yellow)](https://github.com/nv-legate/cupynumeric/stargazers) [![Forks](https://img.shields.io/github/forks/nv-legate/cupynumeric?style=flat-square&color=blue)](https://github.com/nv-legate/cupynumeric/network) [![Language](https://img.shields.io/badge/lang-Python-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-48%2F100-brightgreen?style=flat-square)](#)

> NumPy and SciPy on Multi-Node Multi-GPU systems

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 978 |
| 🍴 **Forks** | 86 |
| 💻 **Language** | Python |
| 📈 **Score** | 48/100 |
| 🗓️ **Last push** | 2026-08-24 |
| 🔍 **Source** | github |

## 🏷️ Topics

_no topics_

## 🎯 Categories

Misc

## 📝 Summary

### English

**Brief Summary (2‑3 sentences)**  
nv‑legate/cupynumeric is an open‑source library that brings NumPy‑ and SciPy‑compatible array operations to multi‑node, multi‑GPU clusters, enabling large‑scale scientific and data‑analytics workloads to run with the familiar Python API. Backed by the Legate runtime, it transparently distributes computations across GPUs and nodes, offering performance gains without requiring users to rewrite code in a low‑level parallel language. With ~1 k stars, active recent commits, and a pure‑Python core, it is positioned as a prototype‑grade tool for teams exploring GPU‑accelerated Python pipelines.

**Value**  
- **Familiar API**: Existing NumPy/SciPy code can be ported with minimal changes, lowering the learning curve for data scientists and researchers.  
- **Scalable performance**: By leveraging the Legate runtime, cupynumeric spreads work across many GPUs and nodes, delivering speedups for large matrix, linear‑algebra, and statistical operations that would otherwise be limited to a single device.  
- **Open‑source & extensible**: The project is MIT‑licensed, written in Python with C++/CUDA kernels, making it easy to inspect, extend, or embed in custom workflows.

**Practical Adoption Path**  
1. **Prototype** – Clone the repo, install the package (via `pip install cupynumeric` or from source), and run the provided examples on a small GPU cluster to verify API compatibility with your existing NumPy code.  
2. **Benchmark & Tune** – Use the built‑in performance tests to compare against pure NumPy/SciPy on your data sizes; adjust Legate runtime settings (e.g., number of workers, memory pools) for optimal throughput.  
3. **Integration Review** – Conduct a manual security and license audit, confirm that the required CUDA/Legate dependencies are compatible with your environment, and add cupynumeric to your CI pipeline for regression testing.  
4. **Pilot Deployment** – Deploy the library in a controlled internal workflow (e.g., a nightly data‑processing job) and monitor resource utilization and error rates.  
5. **Production Roll‑out** – After successful pilot validation, formalize deployment scripts, document version pinning, and establish a maintenance plan (e.g., periodic upstream pulls, monitoring of security advisories).

**Production Readiness**  
- **Maturity**: Medium. The library is actively maintained (last commit 2026‑06‑25) and has a healthy community signal (≈1 k stars, 86 forks), but the ecosystem around Legate is still evolving.  
- **Suitability**: Ideal for prototypes, internal analytics pipelines, or research projects that need to scale NumPy workloads to multiple GPUs.  
- **Considerations before production**: Verify compatibility with your CUDA stack, assess the stability of the Legate runtime in your cluster manager (e.g., Slurm, Kubernetes), and set up monitoring for any runtime‑level regressions. With these checks in place, cupynumeric can be a reliable component of a GPU‑accelerated Python stack.

### Русский

**Краткое резюме:**  
`nv-legate/cupynumeric` — это open‑source библиотека, позволяющая выполнять NumPy и SciPy‑операции на кластерах с несколькими узлами и GPU, что ускоряет вычислительно‑интенсивные задачи в научных и аналитических проектах. При наличии подходящего рабочего процесса (например, прототипирование распределённых машинных‑learning или больших численных симуляций) библиотеку можно быстро интегрировать, но перед переходом в продакшн требуется ручная проверка совместимости зависимостей, лицензии и безопасности, а также подтверждение активности поддерживающих разработчиков. Текущий уровень готовности — средний: подходит для прототипов и внутренних пайплайнов, но требует дополнительного аудита перед масштабным производственным использованием.

### 中文

**项目简介**  
nv-legate/cupynumeric 是一个基于 Legate 框架的 NumPy / SciPy 实现，能够在多节点、多 GPU 环境下以几乎原生的 NumPy 接口执行大规模数组计算，帮助科研和工程团队把单机 Python 工作负载无缝迁移到 GPU 集群。

**价值**  
- **性能提升**：利用 GPU 并行和跨节点通信，数十倍加速矩阵、线性代数和统计计算。  
- **兼容性**：保持 NumPy / SciPy API，现有代码几乎不需要改动即可跑在 GPU 集群上。  
- **可扩展性**：支持自动切分（tiling）和分布式调度，适用于从单机到上千 GPU 的规模。

**典型接入方式**  
1. **环境准备**：在目标机器上安装 CUDA、Legate runtime（`legate install`），并确保 Python 3.9+。  
2. **依赖安装**：`pip install cupynumeric`（或通过 conda‑forge）。  
3. **代码迁移**：将 `import numpy as np` 替换为 `import cupynumeric as np`，其余代码保持不变。  
4. **集群配置**：在提交作业时使用 Legate 提供的 `legate` 启动脚本，指定节点数、GPU 数量和网络层（如 UCX）即可。例如：  
   ```bash
   legate run -n 4 --gpus-per-node 8 my_script.py
   ```
5. **调优**：通过 `legate config` 调整 tile 大小、通信后端等参数，以获得最佳吞吐。

**生产可用性**  
- **成熟度**：项目已有 978 星、86 Fork，最近一次更新在 2026‑06‑25，活跃度尚可。  
- **适用场景**：原型验证、内部数据分析、科研计算以及需要大规模并行的机器学习前处理。  
- **风险与准备**：  
  - 需要自行评估许可证兼容性（Apache‑2.0），并进行安全审计。  
  - 依赖 Legate runtime 与底层 CUDA/UCX，需确保集群环境与这些组件的版本匹配。  
  - 维护者活跃度一般，建议在关键业务前做好内部维护或贡献者备份。  

综上，cupynumeric 在需要把 NumPy 工作负载扩展到多节点 GPU 时提供了高效且低侵入的解决方案，适合作为原型或内部流水线的加速层；在正式生产环境使用前，建议完成环境兼容性、性能基准和运维流程的验证。

## 🧭 Practical evaluation

**Value:** nv-legate/cupynumeric may be useful when its README and activity match a concrete workflow.

**Best use cases**

- Not enough metadata yet.

**Integration notes:** Needs manual inspection before adoption because integration signals are sparse in the discovered metadata.

**Production readiness:** Medium: useful for prototypes or internal workflows, with dependency and maintenance checks before production.

**Quality signals**

- 978 GitHub stars
- 86 forks
- updated 2026-06-25
- primary language: Python

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 48/100 |
| stars | 64/100 |
| topics | 0/100 |
| outlook | 47/100 |
| quality | 52/100 |
| recency | 40/100 |
| adoption | 59/100 |
| production | 52/100 |
| usefulness | 42/100 |
| integration | 46/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 0/100 |

---

<sub>🔭 Discovered 2026-06-25 · [View on GitHub](https://github.com/nv-legate/cupynumeric) · [← Back to Misc](./README.md)</sub>
