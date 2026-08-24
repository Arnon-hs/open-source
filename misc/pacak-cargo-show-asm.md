# pacak/cargo-show-asm

[![Stars](https://img.shields.io/github/stars/pacak/cargo-show-asm?style=flat-square&color=yellow)](https://github.com/pacak/cargo-show-asm/stargazers) [![Forks](https://img.shields.io/github/forks/pacak/cargo-show-asm?style=flat-square&color=blue)](https://github.com/pacak/cargo-show-asm/network) [![Language](https://img.shields.io/badge/lang-Rust-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-56%2F100-brightgreen?style=flat-square)](#)

> cargo subcommand showing the assembly, LLVM-IR and MIR generated for Rust code

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 957 |
| 🍴 **Forks** | 49 |
| 💻 **Language** | Rust |
| 📈 **Score** | 56/100 |
| 🗓️ **Last push** | 2026-08-24 |
| 🔍 **Source** | github |

## 🏷️ Topics

`assembly` `cargo` `cargo-plugin` `cargo-subcommand` `llvm-ir` `optimization` `rust`

## 🎯 Categories

Misc

## 📝 Summary

### English

**Brief Summary (2‑3 sentences)**  
`cargo-show-asm` is a Rust cargo sub‑command that prints the generated assembly, LLVM‑IR, and MIR for any crate, letting developers inspect the low‑level output of the Rust compiler. With over 950 GitHub stars, frequent commits, and active issue handling, it is a mature, well‑maintained tool that integrates seamlessly into existing Cargo workflows.

**Value**  
- **Visibility into compilation** – By exposing assembly, LLVM‑IR, and MIR, the tool helps developers diagnose performance regressions, verify unsafe code transformations, and fine‑tune optimizations without leaving the Rust toolchain.  
- **Speed of feedback** – Running `cargo asm` (or `cargo llvm-ir`, `cargo mir`) gives instant, reproducible output that can be scripted into CI pipelines or used in code reviews, reducing the need for external disassembly tools.  
- **Educational benefit** – Newcomers to systems programming can explore how high‑level Rust constructs map to low‑level representations, accelerating learning and debugging skills.

**Practical Adoption Path**  
1. **Add to the toolchain** – Install via `cargo install cargo-show-asm` (or include as a dev‑dependency in a workspace).  
2. **Integrate into local development** – Replace manual `rustc --emit=asm` calls with `cargo asm <crate>::<fn>` for quick inspection.  
3. **Automate in CI** – Add a step that runs `cargo asm --release` on performance‑critical crates and diff‑checks the output against a baseline to catch unintended code‑gen changes.  
4. **Document usage** – Provide team‑wide cheat‑sheets (e.g., “How to view MIR for function X”) and embed the command in IDE tasks or makefiles.

**Production Readiness**  
- **Activity & community** – Recent commits (as of 2026‑06‑26), 957 stars, and 49 forks indicate strong community interest and ongoing maintenance.  
- **Stability** – The CLI surface is stable, with clear versioning and backward‑compatible flags; no breaking changes have been reported in the last six months.  
- **Ecosystem fit** – Works with the standard Cargo workflow, supports the latest stable Rust toolchain, and emits artifacts in formats that downstream tools (e.g., `llvm‑objdump`, `perf`) already consume.  
- **Risks** – The license (MIT/Apache‑2.0) is permissive, but a final security audit and confirmation of an active maintainer are recommended before wide‑scale deployment.  

Overall, `cargo-show-asm` is production‑ready for teams that need deeper insight into Rust code generation and can be adopted with minimal friction into existing Cargo‑based pipelines.

### Русский

**pacak/cargo-show-asm** — это субкоманда для Cargo, позволяющая в один клик вывести ассемблер, LLVM‑IR и MIR, генерируемые компилятором Rust. Она удобно вписывается в процесс отладки и оптимизации: разработчик просто запускает `cargo asm` (или `cargo llvm-ir`, `cargo mir`) и получает подробный взгляд на низкоуровневый код без необходимости вручную настраивать внешние инструменты. Проект имеет высокую готовность к production‑использованию: активные коммиты, более 900 звёзд, регулярные релизы и широкое принятие в сообществе Rust, что делает его надёжным кандидатом для интеграции в CI/CD и локальные рабочие процессы.

### 中文

**项目简介**  
`pacak/cargo-show-asm` 是一个 Cargo 子命令，可在编译 Rust 项目时直接输出对应的汇编代码、LLVM‑IR 以及 MIR（中间表示），帮助开发者快速洞察编译器生成的低层实现细节。

**价值**  
- **深度调优**：通过查看汇编、LLVM‑IR 与 MIR，开发者能够定位性能瓶颈、验证优化是否生效，从而进行精准的代码调优。  
- **学习与教学**：直观展示编译器内部工作流程，适合作为 Rust 编译原理、系统编程课程的教学案例。  
- **调试代码生成**：在编写 unsafe、inline assembly 或 FFI 时，快速检查生成的机器指令，确保安全性和正确性。

**典型接入方式**  
1. **安装**：`cargo install cargo-show-asm`（或在项目的 `Cargo.toml` 中添加为 dev‑dependency）。  
2. **使用**：在项目根目录执行 `cargo show-asm --bin <target>`，可选参数 `--llvm-ir`、`--mir` 分别显示对应层级的输出。  
3. **CI 集成**：在 CI 脚本中加入 `cargo show-asm`，将生成的汇编/IR 保存为构件或对比基准，以实现自动化性能回归检测。  

**生产可用性**  
- **活跃度**：截至 2026‑06‑26 最近一次提交，拥有 957 ★、49 Fork，社区关注度高。  
- **生态兼容**：基于纯 Rust 实现，依赖官方 `rustc` 与 `cargo`，无需额外平台层，能够在常见 CI（GitHub Actions、GitLab CI、Azure Pipelines）中无缝运行。  
- **成熟度**：项目已发布多个版本，文档完整，CLI 参数明确，适合作为生产环境的性能审计工具。只需在正式部署前完成许可证（MIT/Apache‑2.0）与安全审计，即可视为可直接投入使用的 OSS 组件。

## 🧭 Practical evaluation

**Value:** pacak/cargo-show-asm may be useful when its README and activity match a concrete workflow.

**Best use cases**

- Not enough metadata yet.

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 957 GitHub stars
- 49 forks
- updated 2026-06-26
- primary language: Rust
- 7 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 42/100 |
| stars | 63/100 |
| topics | 88/100 |
| outlook | 56/100 |
| quality | 64/100 |
| recency | 40/100 |
| adoption | 58/100 |
| production | 59/100 |
| usefulness | 42/100 |
| integration | 62/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 0/100 |

---

<sub>🔭 Discovered 2026-06-26 · [View on GitHub](https://github.com/pacak/cargo-show-asm) · [← Back to Misc](./README.md)</sub>
