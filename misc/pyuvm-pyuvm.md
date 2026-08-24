# pyuvm/pyuvm

[![Stars](https://img.shields.io/github/stars/pyuvm/pyuvm?style=flat-square&color=yellow)](https://github.com/pyuvm/pyuvm/stargazers) [![Forks](https://img.shields.io/github/forks/pyuvm/pyuvm?style=flat-square&color=blue)](https://github.com/pyuvm/pyuvm/network) [![Language](https://img.shields.io/badge/lang-Python-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-48%2F100-brightgreen?style=flat-square)](#)

> The UVM written in Python

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 556 |
| 🍴 **Forks** | 105 |
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

**Project Summary**

pyuvm/pyuvm is an open-source project that provides a Python implementation of the Universal Verification Methodology (UVM), a widely-used verification framework in the electronics industry. Despite its relatively low score, the project has a moderate level of production readiness, making it suitable for prototype development or internal workflows with proper dependency and maintenance checks. However, a manual inspection is recommended before adoption due to sparse integration signals.

**Value Proposition**

The primary value proposition of pyuvm/pyuvm lies in its potential to streamline verification workflows, particularly for those already familiar with the UVM framework. By providing a Python-based implementation, the project may appeal to developers who prefer a more flexible and dynamic language for verification tasks.

**Practical Adoption Path**

To adopt pyuvm/pyuvm in a practical setting, follow these steps:

1. **Manual Inspection**: Carefully review the project's README, documentation, and codebase to ensure it aligns with your specific verification needs and workflow.
2. **Integration Testing**: Perform thorough integration testing to validate the project's compatibility with your existing tools and frameworks.
3. **Dependency and Maintenance Checks**: Verify the project's dependencies and maintenance status to ensure it can be sustained in the long term.
4. **Pilot Project**: Choose

### Русский

**pyuvm/pyuvm** — это открытая реализация методологии UVM на Python, позволяющая писать и запускать верификационные тест‑бенчі в привычной для разработчиков Python среде. Проект подходит для прототипирования и внутренних верификационных пайплайнов, когда требуется быстро интегрировать UVM‑подобный подход без перехода на SystemVerilog; перед вводом в продакшн рекомендуется проверить совместимость зависимостей, актуальность лицензии и наличие активных мейнтейнеров. По текущим метрикам (556 звёзд, 105 форков, недавнее обновление) готовность к использованию в production оценивается как «средняя» – подходит для экспериментальных и внутренних задач после небольшого аудита.

### 中文

**项目简介（2‑3 句话）**  
pyuvm 是用 Python 实现的 UVM（Universal Verification Methodology）框架，旨在为硬件验证提供与 SystemVerilog UVM 类似的面向对象、可复用的验证组件。它保留了 UVM 的核心概念（如 sequencer、driver、monitor、agent、environment），但利用 Python 的生态和易用性，让验证工程师能够更快编写、调试和维护测试基准。

---

## 价值

1. **降低学习成本**：Python 语法简洁，开发者无需掌握 SystemVerilog 即可使用 UVM 思想进行验证，适合软件背景的验证工程师或快速原型验证。  
2. **生态互通**：可以直接调用 Python 科学计算、机器学习、数据分析等库（NumPy、Pandas、TensorFlow 等），方便在验证过程中进行统计、自动化报告或 AI‑驱动的生成式测试。  
3. **脚本化与自动化**：Python 天生适合写脚本，配合 CI/CD 流水线可以实现全自动回归、覆盖率收集与报告生成。  
4. **开源社区**：已有 556+ stars、105+ forks，社区提供了多个示例和插件，能够快速上手并在项目中进行二次扩展。

---

## 典型接入方式

| 步骤 | 操作 | 说明 |
|------|------|------|
| 1️⃣ | **环境准备** | `python -m venv venv && source venv/bin/activate` <br> `pip install pyuvm`（或从源码 `git clone https://github.com/pyuvm/pyuvm.git && pip install -e .`） |
| 2️⃣ | **引入框架** | 在验证代码中 `from uvm import *`，即可使用 `uvm_component`, `uvm_test`, `uvm_env` 等基类。 |
| 3️⃣ | **搭建验证环境** | 按 UVM 结构创建 `agent → driver / monitor / sequencer`，编写 `sequence` 与 `test`，并在 `main.py` 中实例化 `uvm_root().run_test()`。 |
| 4️⃣ | **与 DUT 交互** | - **Co‑simulation**：使用 cocotb、Verilator、VCS 等仿真器通过 DPI/PLI 与 Python 进程通信。<br>- **纯 Python DUT**：若 DUT 已经用 MyHDL、nmigen 等 Python‑HDL 描述，可直接在同一进程内调用。 |
| 5️⃣ | **CI 集成** | 在 Jenkins/GitHub Actions 中添加 `pytest` 或自定义脚本，执行 `python -m pytest`、收集覆盖率报告并上传至 Codecov。 |
| 6️⃣ | **报告与调试** | 利用 `uvm_report_server` 输出日志，配合 `logging`、`pdb`、`ipdb` 或 Jupyter Notebook 进行交互式调试。 |

> **小贴士**：如果已有 SystemVerilog UVM 环境，可通过 cocotb‑uvm 桥接层把已有的 SV‑UVM 组件迁移到 pyuvm，保持验证资产的可复用性。

---

## 生产可用性评估

| 维度 | 评估 | 说明 |
|------|------|------|
| **成熟度** | ★★☆☆☆（中等） | 项目活跃度仍在，最近一次提交在 2026‑06‑28，星标/分叉数量表明已有一定社区使用。但相较于成熟的 SystemVerilog UVM，生态、文档和第三方插件仍在成长中。 |
| **依赖管理** | 中等 | 仅依赖标准 Python 包，安装简单。但在与仿真器（Verilator、VCS、NC‑Sim）或 cocotb 结合时，需要自行确保对应版本的兼容性。 |
| **安全/许可证** | 待确认 | 项目采用 BSD‑3‑Clause（需在源码中确认），在引入前应审查许可证与内部合规要求。 |
| **维护者活跃度** | 中等 | 最近有提交记录，但核心维护者人数有限。建议在生产环境中指定内部维护者负责关键 bug 的跟踪与补丁。 |
| **适用场景** | ✅ 原型验证、内部验证平台、教学/科研、AI‑驱动验证 | ❌ 对于需要严格行业认证、长期维护的大规模 ASIC 项目，仍建议保留 SystemVerilog UVM 作为主力。 |
| **推荐使用方式** | **先行试点** → 在内部验证框架或实验室项目中使用，评估与现有仿真流的兼容性 → 若验证效果满意且维护成本可接受，再逐步推广到更大规模的项目。 |

**结论**：pyuvm 为希望在 Python 环境中复用 UVM 思想的团队提供了一个低门槛、易集成的方案，适合原型验证、内部研发或教学实验。若在生产环境使用，需做好依赖、许可证与维护者支持的审查，并建议在关键路径上保留传统 SystemVerilog UVM 作为备份。

## 🧭 Practical evaluation

**Value:** pyuvm/pyuvm may be useful when its README and activity match a concrete workflow.

**Best use cases**

- Not enough metadata yet.

**Integration notes:** Needs manual inspection before adoption because integration signals are sparse in the discovered metadata.

**Production readiness:** Medium: useful for prototypes or internal workflows, with dependency and maintenance checks before production.

**Quality signals**

- 556 GitHub stars
- 105 forks
- updated 2026-06-28
- primary language: Python

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 51/100 |
| stars | 58/100 |
| topics | 0/100 |
| outlook | 46/100 |
| quality | 50/100 |
| recency | 40/100 |
| adoption | 56/100 |
| production | 51/100 |
| usefulness | 42/100 |
| integration | 46/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 0/100 |

---

<sub>🔭 Discovered 2026-06-28 · [View on GitHub](https://github.com/pyuvm/pyuvm) · [← Back to Misc](./README.md)</sub>
