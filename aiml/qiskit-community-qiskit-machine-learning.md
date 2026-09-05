# qiskit-community/qiskit-machine-learning

[![Stars](https://img.shields.io/github/stars/qiskit-community/qiskit-machine-learning?style=flat-square&color=yellow)](https://github.com/qiskit-community/qiskit-machine-learning/stargazers) [![Forks](https://img.shields.io/github/forks/qiskit-community/qiskit-machine-learning?style=flat-square&color=blue)](https://github.com/qiskit-community/qiskit-machine-learning/network) [![Language](https://img.shields.io/badge/lang-Python-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-58%2F100-brightgreen?style=flat-square)](#)

> An open-source library built on Qiskit for quantum machine learning tasks at scale on quantum hardware and classical simulators

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 1.1k |
| 🍴 **Forks** | 439 |
| 💻 **Language** | Python |
| 📈 **Score** | 58/100 |
| 🗓️ **Last push** | 2026-09-05 |
| 🔍 **Source** | github |

## 🏷️ Topics

`machine-learning` `qiskit` `quantum-computing`

## 🎯 Categories

AI/ML

## 📝 Summary

### English

qiskit-community/qiskit-machine‑learning is an open‑source Python library that extends Qiskit for scalable quantum‑machine‑learning experiments on both quantum hardware and classical simulators and real quantum devices and classical simulators, enabling researchers to prototype and automate market‑related workflows such as strategy backtesting and monitoring. Adoption is straightforward for prototyping or internal use—just install the package, integrate it into existing Qiskit‑based pipelines, and run experiments—but teams should perform manual inspection, dependency checks, and a final review of licensing, security, and maintainer activity before moving to production. The project shows moderate production readiness (useful for prototypes) with healthy community signals (≈1 k stars, 400+ forks) but requires due‑diligence for security and maintenance before full‑scale deployment.

### Русский

qiskit-community/qiskit-machine-learning — это открытая библиотека на Python, расширяющая Qiskit инструментами для квантового машинного обучения, позволяющая исследовать и автоматизировать торговые стратегии как на реальном квантовом оборудовании, так и в классических симуляторах. Типичное внедрение включает прототипирование и внутреннее тестирование торговых моделей (back‑test, мониторинг рыночных потоков) с последующей ручной проверкой интеграции, поскольку готовые сигналы о совместимости ограничены. Готовность к production оценивается как средняя: библиотека подходит для экспериментальных и прототипных решений, но требует проверки зависимостей, лицензии и безопасности перед запуском в продакшн.

### 中文

**项目简介**  
qiskit‑community/qiskit‑machine‑learning 是基于 Qiskit 的开源库，提供在真实量子硬件和经典模拟器上进行量子机器学习的统一接口，适用于大规模实验与原型开发。

**价值**  
- **科研加速**：封装了量子特征映射、量子模型训练与评估等常用流程，帮助量子计算研究者快速实现和验证新算法。  
- **交易系统原型**：可将量子机器学习模型嵌入量化交易框架，用于探索量子优势在因子提取、策略生成或风险预测等场景。  
- **跨平台复用**：同一套代码既能在本地模拟器上跑快速迭代，又能无缝切换到 IBM Quantum 实机进行真实测算，降低了实验成本。

**典型接入方式**  
1. **环境准备**：在 Python 项目中 `pip install qiskit-machine-learning`，并确保已安装 Qiskit（`qiskit[all]`）以及对应的 IBM Quantum 账户令牌。  
2. **模型构建**：使用库提供的 `QuantumKernel`, `VQC`（Variational Quantum Classifier）等类，配合 Scikit‑Learn 接口完成特征映射与模型训练。  
3. **后端选择**：通过 `AerSimulator`（本地）或 `IBMQBackend`（云端）在 `QuantumInstance` 中指定运行后端，实现一次代码即可在模拟器和真实硬件之间切换。  
4. **与交易系统集成**：将训练好的量子模型包装为 REST API（如 FastAPI）或直接在策略脚本中调用，输出预测信号供回测或实时决策使用。

**生产可用性**  
- **成熟度**：GitHub 近 1.1k 星、439 Fork，活跃度仍在（最近更新于 2026‑06‑26），适合作为 **原型/内部实验** 平台。  
- **依赖管理**：核心依赖为 Qiskit 与 SciKit‑Learn，需定期检查兼容性和安全漏洞。  
- **上线前检查**：  
  - 评估量子后端排队时间与成本（真实硬件受限）。  
  - 对模型输出进行充分的离线回测，确保在模拟器上表现稳定后再迁移至实机。  
  - 完成许可证（Apache‑2.0）合规审查及安全审计。  
- **结论**：在 **中等** 生产准备度下，适合用于 **内部研发、概念验证** 或 **低频交易策略的探索**；若要在高频、低延迟的生产环境中使用，还需额外的容错、监控和性能优化层。

## 🧭 Practical evaluation

**Value:** qiskit-community/qiskit-machine-learning helps research and automate market workflows.

**Best use cases**

- research trading systems
- backtest strategies
- monitor market workflows

**Integration notes:** Needs manual inspection before adoption because integration signals are sparse in the discovered metadata.

**Production readiness:** Medium: useful for prototypes or internal workflows, with dependency and maintenance checks before production.

**Quality signals**

- 1074 GitHub stars
- 439 forks
- updated 2026-06-26
- primary language: Python
- 3 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 66/100 |
| stars | 65/100 |
| topics | 38/100 |
| outlook | 66/100 |
| quality | 70/100 |
| recency | 80/100 |
| adoption | 65/100 |
| production | 68/100 |
| usefulness | 42/100 |
| integration | 46/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 100/100 |

---

<sub>🔭 Discovered 2026-06-26 · [View on GitHub](https://github.com/qiskit-community/qiskit-machine-learning) · [← Back to AI/ML](./README.md)</sub>
