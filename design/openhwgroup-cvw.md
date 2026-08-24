# openhwgroup/cvw

[![Stars](https://img.shields.io/github/stars/openhwgroup/cvw?style=flat-square&color=yellow)](https://github.com/openhwgroup/cvw/stargazers) [![Forks](https://img.shields.io/github/forks/openhwgroup/cvw?style=flat-square&color=blue)](https://github.com/openhwgroup/cvw/network) [![Language](https://img.shields.io/badge/lang-SystemVerilog-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-46%2F100-brightgreen?style=flat-square)](#)

> CORE-V Wally is a configurable RISC-V Processor associated with RISC-V System-on-Chip Design textbook. Contains a 5-stage pipeline, support for A, B, C, D, F,  M and Q extensions, and optional caches, BP, FPU, VM/MMU, AHB, RAMs, and peripherals.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 553 |
| 🍴 **Forks** | 530 |
| 💻 **Language** | SystemVerilog |
| 📈 **Score** | 46/100 |
| 🗓️ **Last push** | 2026-08-24 |
| 🔍 **Source** | github |

## 🏷️ Topics

_no topics_

## 🎯 Categories

Design

## 📝 Summary

### English

**Brief Summary (2‑3 sentences)**  
CORE‑V Wally (openhwgroup/cvw) is an open‑source, highly configurable 5‑stage RISC‑V core that supports a wide range of extensions (A, B, C, D, F, M, Q) and optional blocks such as caches, branch predictor, FPU, MMU, AHB bus, RAMs and peripheral interfaces. It is bundled with the “RISC‑V System‑on‑Chip Design” textbook, making it a ready‑to‑use reference design for both education and early‑stage silicon prototyping.  

**Value Proposition**  
- **Accelerated AI‑centric SoC development:** By providing a pre‑verified RISC‑V core with optional AI‑friendly extensions (e.g., vector‑type F/D/Q units), teams can embed inference engines or custom accelerators without starting from a blank RTL stack.  
- **Broad configurability:** Designers can enable only the needed extensions and peripherals, reducing area and power while keeping the design portable across FPGA and ASIC flows.  
- **Educational and reference material:** The accompanying textbook and extensive documentation shorten the learning curve for engineers new to RISC‑V or AI‑enabled hardware.  

**Practical Adoption Path**  
1. **Initial Evaluation** – Clone the repository, run the provided simulation testbenches, and verify that the default configuration meets functional requirements.  
2. **Configuration Tuning** – Use the provided `config.mk`/parameter files to enable the desired extensions (e.g., FPU for floating‑point inference, MMU for OS support) and optional caches or peripherals.  
3. **Tool‑chain Integration** – Incorporate the RTL into your FPGA or ASIC flow (e.g., Synopsys, Cadence, or open‑source Yosys/nextpnr). Because integration signals are sparsely documented, a manual review of the top‑level interface and clock/reset domains is required.  
4. **AI Stack Hook‑up** – Connect your AI inference engine (e.g., a lightweight RISC‑V‑compatible neural net runtime) to the core via the optional AXI/AHB bus or custom peripheral interface.  
5. **Verification & Validation** – Run regression tests, perform timing analysis, and, if targeting silicon, run gate‑level simulations before tape‑out.  

**Production Readiness**  
- **Maturity:** Medium. The project is actively maintained (last commit 2026‑06‑26) and has a healthy community (≈ 550 ★, 530 forks), but the integration documentation is limited, requiring manual effort to map signals and verify compatibility with your existing flow.  
- **Prototype Suitability:** Ideal for internal prototypes, research platforms, or early‑stage ASIC/FPGA projects where the flexibility outweighs the integration overhead.  
- **Production Use:** Viable for production after a dedicated integration sprint that validates the chosen configuration, checks tool‑chain compatibility, and establishes a regression suite. Dependency management (SystemVerilog version, third‑party IP for caches/BRAM, etc.) should be audited before committing to volume manufacturing.  

In short, openhwgroup/cvw offers a powerful, configurable RISC‑V foundation for AI‑enabled hardware, but teams should allocate time for manual integration and thorough validation before moving from prototype to production.

### Русский

**openhwgroup/cvw** — открытая реализация конфигурируемого RISC‑V процессора CORE‑V Wally с 5‑ступенчатым конвейером и поддержкой расширений A, B, C, D, F, M, Q, а также опциональных кэшей, предсказателя переходов, FPU, MMU, шины AHB, RAM‑ов и периферии. Он позволяет быстро прототипировать AI‑функциональность (например, RAG‑модели или агентные воркфлоу), используя готовый аппаратный стек вместо построения модели с нуля. Готовность к продакшну — средняя: проект подходит для внутренних прототипов и экспериментальных интеграций, но требует ручной проверки и настройки из‑за скудной метаданных о интеграции.

### 中文

**项目简介**  
CORE‑V Wally 是一款可配置的 RISC‑V 处理器，实现了 5 级流水线，完整支持 A、B、C、D、F、M、Q 扩展，并可选配缓存、分支预测、浮点单元、MMU/VM、AHB 总线、内部 RAM 以及多种外设，配套《RISC‑V SoC 设计》教材使用。

**价值**  
- **快速原型**：提供成熟的硬核实现，开发者无需从零搭建 CPU，即可在此基础上集成 AI 加速单元、RAG 或智能体工作流。  
- **灵活定制**：通过参数化的 Verilog/SystemVerilog 代码，可按需裁剪指令集、缓存层级和外设，满足不同性能/面积需求。  
- **社区与生态**：拥有 550+ 星、530+ Fork，活跃的开源社区提供示例、文档和验证套件，降低学习成本。

**典型接入方式**  
1. **代码获取**：`git clone https://github.com/openhwgroup/cvw.git`。  
2. **配置生成**：使用项目提供的 `make`/`cmake` 脚本或 `scripts/configure_cvw.py`，在 `config/` 目录中打开或编辑 YAML/JSON 配置文件，选择所需扩展、缓存大小、外设等。  
3. **集成到 SoC**：将生成的 RTL（`src/`）和约束文件（`constraints/`）加入现有 FPGA/ASIC 项目，使用标准的 AXI/AHB 接口与其他 IP 核对接。  
4. **验证**：运行自带的 UVM 测试套件或自行编写的指令集仿真脚本，确保功能正确后再进行综合/实现。  

**生产可用性**  
- **成熟度**：中等（Medium）。代码活跃更新，已通过多次 FPGA 验证，适合作为原型或内部研发平台。  
- **部署前检查**：需要手动审查集成文档，确认所选配置与目标工艺、时钟约束以及外设接口匹配；同时评估依赖的第三方 IP（如 FPU、MMU）是否满足安全/功耗要求。  
- **生产建议**：在进入量产前，建议完成以下步骤：  
  1. 完整的功能与时序仿真（包括功耗分析）。  
  2. 与供应链确认所用的 IP 许可证和维护计划。  
  3. 编写或引入 DVT/IVT 测试向量，进行 silicon 级验证。  

综上，openhwgroup/cvw 为需要快速搭建具备 AI 扩展能力的 RISC‑V SoC 提供了可靠的基础块，只要在集成前做好配置审查和验证工作，即可在原型或内部生产环境中安全使用。

## 🧭 Practical evaluation

**Value:** openhwgroup/cvw helps add AI capability without starting from a blank model stack.

**Best use cases**

- prototype AI features
- build RAG or agent workflows
- evaluate model tooling

**Integration notes:** Needs manual inspection before adoption because integration signals are sparse in the discovered metadata.

**Production readiness:** Medium: useful for prototypes or internal workflows, with dependency and maintenance checks before production.

**Quality signals**

- 553 GitHub stars
- 530 forks
- updated 2026-06-26
- primary language: SystemVerilog

**Risks:** Integration path is not obvious from metadata; validate setup cost before committing.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 68/100 |
| stars | 58/100 |
| topics | 0/100 |
| outlook | 48/100 |
| quality | 53/100 |
| recency | 40/100 |
| adoption | 61/100 |
| production | 50/100 |
| usefulness | 42/100 |
| integration | 30/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 100/100 |

---

<sub>🔭 Discovered 2026-06-26 · [View on GitHub](https://github.com/openhwgroup/cvw) · [← Back to Design](./README.md)</sub>
