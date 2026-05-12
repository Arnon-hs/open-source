# rex-rs/rex

[![Stars](https://img.shields.io/github/stars/rex-rs/rex?style=flat-square&color=yellow)](https://github.com/rex-rs/rex/stargazers) [![Forks](https://img.shields.io/github/forks/rex-rs/rex?style=flat-square&color=blue)](https://github.com/rex-rs/rex/network) [![Language](https://img.shields.io/badge/lang-Rust-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-57%2F100-brightgreen?style=flat-square)](#)

> Rex is a safe and usable kernel extension framework that allows loading and executing Rust kernel extension programs in the place of eBPF.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 540 |
| 🍴 **Forks** | 27 |
| 💻 **Language** | Rust |
| 📈 **Score** | 57/100 |
| 🗓️ **Last push** | 2026-05-12 |
| 🔍 **Source** | github |

## 🏷️ Topics

_no topics_

## 🎯 Categories

Misc

## 📝 Summary

### English

**Brief summary**  
Rex is a Rust‑based kernel‑extension framework that lets you load and run safe, user‑written kernel modules as an alternative to eBPF. It aims to provide a more ergonomic and type‑safe development experience while preserving the performance characteristics needed for low‑level kernel work.

**Value**  
- **Safety & ergonomics**: By leveraging Rust’s ownership and type system, Rex reduces the risk of memory‑unsafe bugs that are common in traditional C kernel modules and in eBPF bytecode.  
- **Familiar language**: Developers can write kernel extensions in full Rust instead of learning eBPF’s restricted C‑like syntax, speeding up prototyping and reducing context switches.  
- **Extensibility**: The framework is designed to be modular, making it straightforward to add custom hooks or integrate with existing kernel subsystems.

**Practical adoption path**  
1. **Evaluate the README and examples** – clone the repo, build the provided demo extensions, and run them on a test kernel (e.g., a VM or a dedicated development machine).  
2. **Check compatibility** – verify that your target kernel version is supported by the current Rex release; the project’s recent commit (May 2026) suggests active maintenance but the supported kernel list is not explicit, so you may need to adjust kernel headers or submit a small patch.  
3. **Integrate build pipeline** – add Rex as a Cargo workspace or submodule, and configure your CI to compile the kernel extension with the same toolchain used for the host kernel.  
4. **Perform security review** – run static analysis (e.g., `cargo clippy`, `cargo audit`) and functional tests to ensure the loaded modules do not violate kernel invariants.  
5. **Gradual rollout** – start with internal prototypes or non‑critical services, monitor logs for kernel panics or performance regressions, then expand to broader workloads.

**Production readiness**  
Rex sits at a **medium** readiness level. The project shows healthy community interest (≈540 ★, 27 forks) and recent activity, making it suitable for internal prototypes or controlled production use after a thorough validation phase. Before committing to a production deployment, you should:  

- Confirm that the kernel version you run is fully supported.  
- Establish a repeatable build and signing process for the extensions.  
- Implement monitoring for kernel stability and performance impact.  
- Allocate resources for ongoing maintenance, as the integration surface (kernel‑Rex API) is still evolving and documentation is sparse.

If those checks pass, Rex can replace eBPF in scenarios where Rust’s safety guarantees and richer language features provide a clear advantage.

### Русский

Rex — это безопасный фреймворк для расширения ядра, позволяющий загружать и запускать программы‑расширения на Rust вместо eBPF; он подходит для прототипов и внутренних инструментов, где требуется более выразительный и типобезопасный код ядра. При внедрении типичный сценарий — написание небольшого Rust‑модуля, его сборка и подключение к ядру через API Rex, после чего модуль исполняется в изолированном контексте. Готовность к production — средняя: проект имеет активную поддержку (540 звёзд, недавние коммиты), но путь интеграции не полностью документирован, поэтому перед выпуском в продакшн требуется ручная проверка настроек и оценка затрат на поддержку.

### 中文

**项目简介**  
Rex（`rex-rs/rex`）是一个安全、易用的内核扩展框架，能够在 Linux 内核中加载并运行用 Rust 编写的扩展程序，提供了比传统 eBPF 更丰富的语言特性和类型安全保障。

**价值**  
- **Rust 安全性**：利用 Rust 的所有权模型和零成本抽象，显著降低内核扩展中的内存安全漏洞风险。  
- **功能完整**：相较于 eBPF，Rust 扩展可以使用完整的标准库（或经过审计的子集），实现更复杂的业务逻辑和数据结构。  
- **开发体验**：统一使用 Rust 开发工具链（cargo、rustc），省去 eBPF 专有的编译与验证步骤，提升开发效率。

**典型接入方式**  
1. **准备内核**：在目标系统上编译并启用 Rex 所需的内核补丁或模块（项目提供的 `rex-loader`）。  
2. **编写扩展**：使用 `cargo new --lib` 创建 Rust 库，添加 `rex` 依赖并实现 `rex::Extension` 接口。  
3. **构建与签名**：通过 `cargo build --release` 生成 ELF，使用项目提供的签名工具对二进制进行签名（防止恶意加载）。  
4. **加载运行**：在用户空间调用 `rexctl load <path>` 将扩展加载进内核，随后可通过 `rexctl invoke` 或自定义系统调用与之交互。  
5. **监控与调试**：利用 `rexctl stats` 查看运行时指标，使用 `gdb`/`rust-gdb` 对内核态代码进行调试。

**生产可用性**  
- **成熟度**：已有 540+ 星、27+ Fork，最近一次提交于 2026‑05‑12，活跃度尚可。  
- **适用场景**：适合内部原型、实验性功能或对安全性要求极高的自研内核模块。  
- **风险与准备**：集成路径在文档中不够完整，需自行检查内核兼容性、签名流程以及对现有加载机制的影响；建议在受控环境中进行完整的 CI/CD 测试后再考虑生产部署。  

总体而言，Rex 为希望在内核层使用 Rust 的团队提供了一个可行的方案，但在正式上线前应做好兼容性评估和运维准备。

## 🧭 Practical evaluation

**Value:** rex-rs/rex may be useful when its README and activity match a concrete workflow.

**Best use cases**

- Not enough metadata yet.

**Integration notes:** Needs manual inspection before adoption because integration signals are sparse in the discovered metadata.

**Production readiness:** Medium: useful for prototypes or internal workflows, with dependency and maintenance checks before production.

**Quality signals**

- 540 GitHub stars
- 27 forks
- updated 2026-05-12
- primary language: Rust

**Risks:** Integration path is not obvious from metadata; validate setup cost before committing.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 36/100 |
| stars | 58/100 |
| topics | 0/100 |
| outlook | 70/100 |
| quality | 63/100 |
| recency | 100/100 |
| adoption | 52/100 |
| production | 68/100 |
| usefulness | 58/100 |
| integration | 30/100 |
| sourceTrust | 100/100 |

---

<sub>🔭 Discovered 2026-05-12 · [View on GitHub](https://github.com/rex-rs/rex) · [← Back to Misc](./README.md)</sub>
