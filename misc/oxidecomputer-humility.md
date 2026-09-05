# oxidecomputer/humility

[![Stars](https://img.shields.io/github/stars/oxidecomputer/humility?style=flat-square&color=yellow)](https://github.com/oxidecomputer/humility/stargazers) [![Forks](https://img.shields.io/github/forks/oxidecomputer/humility?style=flat-square&color=blue)](https://github.com/oxidecomputer/humility/network) [![Language](https://img.shields.io/badge/lang-Rust-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-50%2F100-brightgreen?style=flat-square)](#)

> Debugger for Hubris

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 575 |
| 🍴 **Forks** | 62 |
| 💻 **Language** | Rust |
| 📈 **Score** | 50/100 |
| 🗓️ **Last push** | 2026-09-05 |
| 🔍 **Source** | github |

## 🏷️ Topics

_no topics_

## 🎯 Categories

Misc

## 📝 Summary

### English

**Summary**  
Humility is an open‑source Rust debugger for the Hubris microkernel, offering low‑level inspection and crash‑analysis tools that can speed up development of embedded firmware. With ~575 ★ and recent activity (last commit 2026‑05‑14), it is mature enough for prototypes but still requires manual vetting to confirm it fits a specific workflow.

**Value** – Humility provides the only dedicated debugging interface for Hubris, letting developers step through kernel code, view task state, and extract diagnostics without needing expensive hardware debuggers. This can dramatically reduce iteration time for teams building safety‑critical or IoT firmware on Oxide’s hardware stack.

**Practical adoption path** –  
1. Clone the repository and run the provided Cargo build to verify the tool compiles on your target platform.  
2. Follow the README examples to attach Humility to a running Hubris instance (usually via a serial or JTAG link).  
3. Integrate the command‑line invocations into your CI/CD or local test harness, and script common queries (e.g., `humility dump`, `humility stack`) to make the debugger part of routine regression testing.  

Because the integration details are sparse in the metadata, teams should allocate a short “evaluation sprint” to confirm that the required transport (serial/JTAG) and Rust toolchain versions are compatible with their existing build environment.

**Production readiness** – Rated medium: the debugger is stable enough for internal tooling and prototype validation, but production use should include a dependency audit (Rust version, Cargo lockfile, and any native libraries) and a fallback plan if the tool’s integration surface proves insufficient for automated pipelines. Once the initial validation succeeds, Humility can be locked into a versioned internal package and used safely for ongoing firmware development.

### Русский

**OxideComputer/humility** — это отладчик для операционной системы Hubris, написанный на Rust. Он подходит для прототипов и внутренних процессов, где требуется интерактивный контроль над задачами Hubris, но перед внедрением следует вручную проверить совместимость и оценить затраты на настройку, так как интеграционные сигналы в метаданных ограничены. Готовность к production — средняя: проект имеет активное развитие (575★, 62 fork, обновлён 2026‑05‑14), но требует проверки зависимостей и поддержки перед использованием в продакшене.

### 中文

**项目简介**  
OxideComputer 的 **humility** 是一款面向 Hubris（Oxide 生态系统中的微内核） 的调试工具，使用 Rust 编写，提供对任务、内存、寄存器等底层状态的实时检查与可视化，帮助开发者快速定位和排查固件问题。

**价值**  
- **深度可观测性**：能够在不破坏目标系统的前提下，读取并展示 Hubris 内核的内部状态，极大提升故障定位效率。  
- **Rust 生态兼容**：基于安全的 Rust 实现，避免了常见的 C/C++ 调试器的内存安全风险。  
- **社区认可**：已有 575+ Stars、62+ Forks，活跃的开源社区提供了不少使用案例和改进建议。

**典型接入方式**  
1. **源码编译**：克隆仓库后，使用 `cargo build --release` 生成 `humility` 可执行文件。  
2. **硬件连接**：通过 JTAG/SWD 或串口将调试主机与运行 Hubris 的目标板相连，确保目标板开启调试接口。  
3. **命令行调用**：在调试主机上运行 `humility <subcommand> [options]`，常用子命令包括 `dump`, `read-reg`, `trace` 等。  
4. **脚本化集成**：可将 `humility` 命令封装进 CI/CD 或内部测试脚本，实现自动化固件回归检查。

**生产可用性**  
- **成熟度**：项目已在 2026-05-14 最近一次更新，代码基于 Rust，具备较好的安全性和可维护性。  
- **适用场景**：适合原型验证、内部研发调试以及在生产前的固件验证阶段使用。  
- **风险与准备**：元数据中缺乏完整的集成文档，接入前需要手动确认硬件接口、依赖的 JTAG/SWD 适配器以及目标板的调试配置；同时建议在受控环境中进行一次完整的功能验证后，再考虑在更大规模的流水线中使用。  

总体而言，**humility** 在提供 Hubris 深度调试能力方面表现突出，适合作为内部研发或原型阶段的核心调试工具；在正式生产环境使用前，需要完成集成验证和运维流程的梳理。

## 🧭 Practical evaluation

**Value:** oxidecomputer/humility may be useful when its README and activity match a concrete workflow.

**Best use cases**

- Not enough metadata yet.

**Integration notes:** Needs manual inspection before adoption because integration signals are sparse in the discovered metadata.

**Production readiness:** Medium: useful for prototypes or internal workflows, with dependency and maintenance checks before production.

**Quality signals**

- 575 GitHub stars
- 62 forks
- updated 2026-05-14
- primary language: Rust

**Risks:** Integration path is not obvious from metadata; validate setup cost before committing.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 45/100 |
| stars | 59/100 |
| topics | 0/100 |
| outlook | 60/100 |
| quality | 60/100 |
| recency | 80/100 |
| adoption | 55/100 |
| production | 62/100 |
| usefulness | 42/100 |
| integration | 30/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 0/100 |

---

<sub>🔭 Discovered 2026-05-14 · [View on GitHub](https://github.com/oxidecomputer/humility) · [← Back to Misc](./README.md)</sub>
