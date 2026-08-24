# SRI-CSL/yices2

[![Stars](https://img.shields.io/github/stars/SRI-CSL/yices2?style=flat-square&color=yellow)](https://github.com/SRI-CSL/yices2/stargazers) [![Forks](https://img.shields.io/github/forks/SRI-CSL/yices2?style=flat-square&color=blue)](https://github.com/SRI-CSL/yices2/network) [![Language](https://img.shields.io/badge/lang-SMT-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-47%2F100-brightgreen?style=flat-square)](#)

> SRI Yices SMT Solver

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 465 |
| 🍴 **Forks** | 64 |
| 💻 **Language** | SMT |
| 📈 **Score** | 47/100 |
| 🗓️ **Last push** | 2026-08-24 |
| 🔍 **Source** | github |

## 🏷️ Topics

`sat-solver` `satisfiability` `satisfiability-modulo-theories` `smt-solver` `theorem-prover`

## 🎯 Categories

Misc

## 📝 Summary

### English

**Brief Summary (2‑3 sentences)**  
SRI‑CSL/yices2 is the open‑source implementation of the Yices SMT (Satisfi‑checking Modulo Theories) solver, maintained by the SRI Computer Science Laboratory. With over 460 stars and recent activity, it offers a mature, high‑performance engine for checking logical formulas in a variety of theories (e.g., linear arithmetic, bit‑vectors, arrays). It is most useful when the project’s README and current activity align with a concrete verification or synthesis workflow you need to support.

**Value**  
- Provides a fast, well‑tested SMT backend that can replace commercial solvers in research prototypes, automated theorem proving pipelines, and formal verification tools.  
- The open‑source license removes cost barriers and allows deep integration or custom extensions (e.g., adding new theories or heuristics).  
- A large user community and extensive documentation (README, examples, benchmarks) reduce the learning curve for teams already familiar with SMT solving.

**Practical Adoption Path**  
1. **Proof‑of‑Concept** – Clone the repo, follow the quick‑start instructions in the README, and run the provided benchmark suite to confirm the solver works on your hardware.  
2. **Integration Layer** – Wrap the `yices2` command‑line or C API in a thin adapter that matches your existing toolchain (e.g., a Python front‑end, a CI job, or a custom DSL compiler).  
3. **Validation** – Run a representative subset of your formulas through the adapter, compare results and performance against your current solver, and adjust configuration flags (e.g., theory selection, timeout).  
4. **Iterate** – If needed, contribute small patches or configuration scripts back to the repo to smooth the integration.

**Production Readiness**  
- **Maturity**: Medium. The solver is stable and actively maintained (last update 2026‑07‑05), but it is primarily positioned for research and prototype use.  
- **Dependencies**: Requires a C compiler and optional bindings (Python, OCaml, etc.); these should be vetted for version compatibility with your stack.  
- **Maintenance**: Monitor upstream releases for bug fixes and security patches; consider pinning a specific tag for reproducibility.  
- **Risk Mitigation**: Because the integration path is not fully described in the metadata, allocate a short sprint to confirm build steps, evaluate licensing compliance, and document any custom glue code before committing to production.  

Overall, Yices 2 can be a solid component of internal verification pipelines or prototype tools, provided you perform a small‑scale validation and establish a clear integration wrapper.

### Русский

SRI‑CSL/yices2 — это открытый SMT‑решатель Yices, подходящий для быстрого прототипирования и внутренних верификационных пайплайнов, когда его README и текущая активность соответствуют требуемому рабочему процессу. Рекомендуется начать с небольшого proof‑of‑concept, проверив сборку и базовые примеры, а затем оценить зависимости и частоту обновлений перед выводом в продакшн. Готовность к production — средняя: решение стабильно работает в прототипах, но требует дополнительной проверки интеграции и поддержки в долгосрочной перспективе.

### 中文

**项目简介**  
SRI‑CSL / yices2 是由美国国防高级研究计划局（SRI）计算科学实验室维护的开源 SMT（Satisfiability Modulo Theories）求解器，专注于高效的布尔、线性整数/实数以及非线性算术求解。它在学术界和工业原型中被广泛用于形式化验证、符号执行和约束求解等场景。

**价值**  
- **高性能**：实现了多种专用求解技术（如分层求解、冲突驱动学习），在多数基准上跑分领先。  
- **灵活 API**：提供 C、C++、Python 等语言绑定，便于在现有工具链中直接调用。  
- **活跃维护**：截至 2026‑07‑05 最近一次提交，拥有 465+ stars、64 forks，社区仍在贡献 bugfix 与新特性。  

**典型接入方式**  
1. **源码编译或二进制安装**：`git clone https://github.com/SRI-CSL/yices2.git && ./configure && make && sudo make install`，或使用发行版提供的预编译包（如 Ubuntu 的 `libyices2-dev`）。  
2. **语言绑定**：在 Python 项目中 `pip install yices`（或通过 `pybind11` 手动包装），在 C/C++ 项目中直接 `#include <yices.h>` 并链接 `-lyices2`。  
3. **作为子进程调用**：对已有脚本语言（如 Bash、Make）可通过 `yices-smt2` 命令行工具读取/写入 SMT‑LIB2 格式文件，实现快速原型验证。  

**生产可用性**  
- **成熟度**：中等（Score 56/100），适合作为内部原型或验证流水线的核心求解器。  
- **准备工作**：在正式上线前建议完成以下步骤：  
  1. **阅读 README 与示例**，确认 API 与项目需求匹配。  
  2. **构建小型 PoC**，验证依赖（CMake、GMP、MPFR 等）在目标平台上的兼容性。  
  3. **制定维护策略**：锁定特定 tag 版本，监控 upstream 更新并评估安全补丁。  
- **风险**：文档相对简略，集成路径需自行探索；若对实时性或高并发有严格要求，需进行性能基准测试并可能进行二次封装。  

总体而言，yices2 在需要高效 SMT 求解的内部工具或研究原型中价值突出，只要做好前期的依赖验证与版本管理，即可在生产环境中安全使用。

## 🧭 Practical evaluation

**Value:** SRI-CSL/yices2 may be useful when its README and activity match a concrete workflow.

**Best use cases**

- Not enough metadata yet.

**Integration notes:** Looks feasible to evaluate, but integration should start with a small proof of concept and README check.

**Production readiness:** Medium: useful for prototypes or internal workflows, with dependency and maintenance checks before production.

**Quality signals**

- 465 GitHub stars
- 64 forks
- updated 2026-07-05
- primary language: SMT
- 5 topics

**Risks:** Integration path is not obvious from metadata; validate setup cost before committing.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 45/100 |
| stars | 57/100 |
| topics | 63/100 |
| outlook | 52/100 |
| quality | 58/100 |
| recency | 40/100 |
| adoption | 54/100 |
| production | 52/100 |
| usefulness | 42/100 |
| integration | 30/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 0/100 |

---

<sub>🔭 Discovered 2026-07-05 · [View on GitHub](https://github.com/SRI-CSL/yices2) · [← Back to Misc](./README.md)</sub>
