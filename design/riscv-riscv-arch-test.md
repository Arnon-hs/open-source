# riscv/riscv-arch-test

[![Stars](https://img.shields.io/github/stars/riscv/riscv-arch-test?style=flat-square&color=yellow)](https://github.com/riscv/riscv-arch-test/stargazers) [![Forks](https://img.shields.io/github/forks/riscv/riscv-arch-test?style=flat-square&color=blue)](https://github.com/riscv/riscv-arch-test/network) [![Language](https://img.shields.io/badge/lang-Assembly-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-52%2F100-brightgreen?style=flat-square)](#)

> The RISC-V Architectural Certification Tests (ACTs) are a set of assembly language tests designed to certify that a design faithfully implements the RISC-V specification.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 734 |
| 🍴 **Forks** | 325 |
| 💻 **Language** | Assembly |
| 📈 **Score** | 52/100 |
| 🗓️ **Last push** | 2026-09-05 |
| 🔍 **Source** | github |

## 🏷️ Topics

_no topics_

## 🎯 Categories

Design

## 📝 Summary

### English

**Brief Summary (2‑3 sentences)**  
The *riscv/riscv-arch-test* repository provides a comprehensive suite of assembly‑level tests that verify whether a hardware design fully complies with the RISC‑V ISA specification. While the tests themselves are not AI‑centric, they can be leveraged as a reliable baseline for building and validating AI‑enabled tooling—such as RAG pipelines or autonomous agents—that need to reason about or generate RISC‑V code. The project is actively maintained (last update 2026‑06‑26) and enjoys a solid community presence (≈734 ⭐, 325 🍴).

**Value**  
- **Certification Backbone** – Guarantees that any RISC‑V core used in AI‑accelerators or edge devices meets the official ISA, reducing costly post‑silicon bugs.  
- **Reusable Test Assets** – The assembly tests can be fed into AI models (e.g., code‑generation or verification agents) as ground‑truth data, accelerating prototype development of AI‑driven hardware verification tools.  
- **Open‑Source Community** – A mature contributor base ensures ongoing updates and bug fixes, making the suite a trustworthy reference point for both hardware and AI teams.

**Practical Adoption Path**  
1. **Environment Setup** – Clone the repo and install the required toolchain (e.g., GNU RISC‑V toolchain, Spike or QEMU).  
2. **Run Baseline Tests** – Execute the provided makefiles to confirm that your target core passes the baseline ACTs.  
3. **Integrate with AI Workflows** – Export test cases (source, expected results, logs) as structured data (JSON/CSV) and feed them into your AI pipeline for tasks such as:  
   - Training a model to generate correct RISC‑V assembly.  
   - Building a RAG system that answers “why does this instruction fail?” queries.  
   - Automating regression testing via AI‑driven test‑case selection.  
4. **Manual Validation** – Because metadata on integration points is sparse, perform a small pilot run to verify that the AI tooling correctly consumes the test artifacts and that the feedback loop works.  
5. **Scale Up** – Once the pilot succeeds, embed the test suite into CI/CD pipelines for continuous hardware‑AI co‑verification.

**Production Readiness**  
- **Maturity**: Medium. The test suite is production‑grade for hardware certification, but the AI‑integration layer is still experimental and requires custom glue code.  
- **Dependencies**: Relies on external RISC‑V simulators and toolchains; ensure version compatibility and maintain them as part of your release process.  
- **Maintenance**: Monitor upstream updates (new ISA extensions, bug fixes) and plan periodic syncs.  
- **Risk Mitigation**: Conduct a cost‑benefit analysis of the integration effort, and establish a fallback to the raw test suite if AI components under‑perform.  

Overall, *riscv-arch-test* offers a solid, community‑validated foundation for any project that needs to certify RISC‑V hardware and can serve as high‑quality training/validation data for AI systems that interact with low‑level code. With a modest integration effort and proper validation, it can be safely used in production‑grade verification pipelines.

### Русский

**riscv/riscv-arch-test** — набор ассемблерных тестов для подтверждения полной совместимости реализации процессора с спецификацией RISC‑V. Он удобен для быстрого прототипирования и верификации AI‑ориентированных решений (например, RAG‑агентов), однако требует ручного аудита и настройки перед внедрением, так как автоматические интеграционные сигналы ограничены. Проект находится на среднем уровне готовности к production: подходит для внутренних и экспериментальных пайплайнов после проверки зависимостей и поддержки.

### 中文

**价值**  
riscv‑arch‑test 为 RISC‑V 处理器实现提供了官方的体系结构认证套件，能够在最底层（汇编）层面验证指令集、异常处理、特权模式等是否严格符合 RISC‑V 规范。通过这些测试，硬件团队可以在 silicon 交付前快速发现实现偏差，降低后期返工和验证成本；同时，软件/仿真平台也能借助它确保兼容性，从而提升整个生态的可靠性。

**典型接入方式**  

| 步骤 | 说明 |
|------|------|
| 1️⃣ 克隆仓库 | `git clone https://github.com/riscv/riscv-arch-test.git` |
| 2️⃣ 选择目标子集 | 根据需要的特权级别或指令集（RV32/64, M/A/F/D 等）挑选对应的 `rv32ui`, `rv64mi` 等子目录。 |
| 3️⃣ 配置编译工具链 | 使用 RISC‑V GNU Toolchain（或对应的 LLVM‑based 工具链）设置 `CROSS_COMPILE=riscv64-unknown-elf-`，并确保 `make` 能找到 `as`、`ld`。 |
| 4️⃣ 生成可执行映像 | 在测试目录下运行 `make`（或 `make RISCV_TOOLCHAIN=/path/to/toolchain`），会得到 `.elf`/`.bin` 文件。 |
| 5️⃣ 运行在仿真器或硬件上 | - **仿真器**：Spike、QEMU、Renode 等直接加载生成的映像。<br>- **实际硬件**：通过 JTAG/Flash 烧录后复位执行，或使用 OpenOCD/Debug Probe 读取退出状态。 |
| 6️⃣ 收集并解析结果 | 测试结束后会在 `log/` 生成 `*.log`，其中包含 PASS/FAIL、异常码等信息。可使用社区提供的 Python 脚本 `parse_results.py` 自动汇总统计。 |
| 7️⃣ （可选）CI 集成 | 将上述步骤写成 GitHub Actions、GitLab CI 或 Jenkins pipeline，实现每次提交后自动跑回归测试，确保任何代码改动都不破坏已认证的行为。 |

**生产可用性**  

- **成熟度**：项目已有 734 ⭐、325 🍴，活跃维护至 2026‑06‑26，社区贡献和 Issue 反馈较多，属于 **中等成熟度**。  
- **适用场景**：  
  - **原型验证**：快速检查新指令或特权扩展的实现是否符合规范。  
  - **内部 CI/CD**：在芯片设计流水线或仿真平台中作为回归套件。  
  - **生态兼容性**：发行版、OS、编译器等需要保证对 RISC‑V 基础指令的兼容时使用。  
- **上线注意事项**：  
  1. **依赖明确**：需要一套兼容的 RISC‑V 编译工具链和目标仿真器/硬件环境；不同平台的启动/退出约定可能略有差异，需要在 CI 脚本中统一。  
  2. **手动审查**：测试报告仅给出 PASS/FAIL，若出现失败需人工检查对应的汇编代码和硬件异常日志，因元数据中缺乏自动定位信息。  
  3. **维护成本**：当 RISC‑V ISA 版本升级（如加入新扩展）时，需要同步更新测试子集或自行添加扩展测试。  
- **生产级别评估**：在 **内部或受控环境**（原型验证、内部回归）可直接使用；若要在面向客户的生产流水线中作为唯一合规依据，建议配合更高层次的系统级验证（软件堆栈、性能基准）并做好 **依赖锁定** 与 **版本审计**。  

综上，riscv‑arch‑test 是 RISC‑V 生态中验证实现正确性的关键工具，接入成本适中，适合原型与内部 CI；在生产环境使用时需要做好依赖管理、结果审查和与更高层次验证的组合，以确保整体系统的可靠交付。

## 🧭 Practical evaluation

**Value:** riscv/riscv-arch-test helps add AI capability without starting from a blank model stack.

**Best use cases**

- prototype AI features
- build RAG or agent workflows
- evaluate model tooling

**Integration notes:** Needs manual inspection before adoption because integration signals are sparse in the discovered metadata.

**Production readiness:** Medium: useful for prototypes or internal workflows, with dependency and maintenance checks before production.

**Quality signals**

- 734 GitHub stars
- 325 forks
- updated 2026-06-26
- primary language: Assembly

**Risks:** Integration path is not obvious from metadata; validate setup cost before committing.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 63/100 |
| stars | 61/100 |
| topics | 0/100 |
| outlook | 62/100 |
| quality | 63/100 |
| recency | 80/100 |
| adoption | 62/100 |
| production | 63/100 |
| usefulness | 42/100 |
| integration | 30/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 100/100 |

---

<sub>🔭 Discovered 2026-06-26 · [View on GitHub](https://github.com/riscv/riscv-arch-test) · [← Back to Design](./README.md)</sub>
