# rust-lang/compiler-builtins

[![Stars](https://img.shields.io/github/stars/rust-lang/compiler-builtins?style=flat-square&color=yellow)](https://github.com/rust-lang/compiler-builtins/stargazers) [![Forks](https://img.shields.io/github/forks/rust-lang/compiler-builtins?style=flat-square&color=blue)](https://github.com/rust-lang/compiler-builtins/network) [![Language](https://img.shields.io/badge/lang-Rust-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-45%2F100-brightgreen?style=flat-square)](#)

> Rust implementations of compiler-rt and libm

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 498 |
| 🍴 **Forks** | 276 |
| 💻 **Language** | Rust |
| 📈 **Score** | 45/100 |
| 🗓️ **Last push** | 2026-08-24 |
| 🔍 **Source** | github |

## 🏷️ Topics

_no topics_

## 🎯 Categories

Misc

## 📝 Summary

### English

**Brief summary**  
`rust-lang/compiler-builtins` provides Rust implementations of the low‑level runtime libraries — compiler‑rt and libm — that are normally linked in by the compiler. By exposing these primitives as a reusable crate, it lets projects avoid custom C‑based shims and ship mathematically‑correct functions and intrinsics directly from Rust.

**Value**  
The crate frees developers from maintaining their own copies of compiler‑rt or libm, reducing duplication and the risk of ABI mismatches. It also enables faster iteration on performance‑critical code because the built‑ins are written in safe/idiomatic Rust and are kept in sync with the Rust compiler itself.

**Practical adoption path**  
1. **Evaluate the API** – add the crate as a dev‑dependency and experiment with a few intrinsics (e.g., `sqrtf64`, `memcpy`) in a sandbox project.  
2. **Check compatibility** – ensure the target platform(s) you ship to are supported by the crate’s feature flags (e.g., `x86_64`, `aarch64`).  
3. **Integrate** – replace existing C‑based runtime calls with the Rust equivalents, adjusting build scripts to link only this crate.  
4. **Validate** – run the project's test suite and benchmark critical paths to confirm functional and performance parity.

**Production readiness**  
The project is at a **medium** readiness level. It has a healthy community signal (≈ 500 ★, 276 forks) and is actively maintained (last update 2026‑06‑23), making it suitable for prototypes, internal tools, or services where low‑level math/runtime correctness is needed. However, the integration documentation is sparse, so teams should allocate time for a manual inspection of build scripts and platform support before committing to production use, and plan for ongoing dependency monitoring.

### Русский

**rust-lang/compiler-builtins** — это набор Rust‑реализаций библиотек compiler‑rt и libm, позволяющий быстро добавить низкоуровневые математические и системные функции без написания собственного кода. Он полезен, когда нужно ускорить разработку пользовательского интерфейса, переиспользуя готовые компоненты и снижая количество кастомных зависимостей, однако путь интеграции не очевиден и требует ручного анализа текущей инфраструктуры. Проект имеет средний уровень готовности к production: подходит для прототипов и внутренних сервисов, но перед выпуском в продакшн следует проверить совместимость, нагрузку и затраты на настройку.

### 中文

**项目简介（2‑3 句）**  
`rust-lang/compiler-builtins` 是 Rust 语言对 LLVM compiler‑rt 与 libm 的实现，提供底层运行时函数（如整数溢出检查、浮点数学运算等）的纯 Rust 替代。它让在 `no_std` 环境或自定义目标平台上编译 Rust 程序时，无需依赖外部 C 库即可获得完整的运行时支持。

**价值**  
- **统一语言栈**：全部用 Rust 编写，避免了跨语言链接和二进制兼容性问题，提升代码安全性和可审计性。  
- **适配裸金属/嵌入式**：在没有标准库或操作系统的环境中仍能提供必需的数学与运行时函数，极大降低了移植成本。  
- **可复用性**：作为官方维护的基库，其他 Rust 项目（如 `core`, `alloc`）直接依赖，减少了重复实现的工作量。

**典型接入方式**  
1. 在 `Cargo.toml` 中添加依赖：  
   ```toml
   [dependencies]
   compiler_builtins = { git = "https://github.com/rust-lang/compiler-builtins", rev = "v0.1.73" }
   ```  
2. 对于 `no_std` 项目，启用对应特性（如 `compiler_builtins/mem`、`compiler_builtins/mul` 等），并在 crate 根部声明 `#![no_std]`。  
3. 在目标平台的 `target.json` 中加入 `compiler-builtins` 的链接指示，或在 `rustc` 编译时使用 `-C link-arg=-lcompiler_builtins`。  
4. 若使用自定义链接器或裸机启动代码，需手动在链接脚本中导入 `compiler_builtins` 提供的符号。

**生产可用性**  
- **成熟度**：项目已有 500+ 星、200+ Fork，活跃维护，最近一次提交在 2026‑06‑23，代码质量和安全审计水平较高。  
- **适用场景**：非常适合 **原型、内部工具、嵌入式固件、WebAssembly** 等需要 `no_std` 支持的场景。  
- **风险与准备**：集成路径并非全部自动化，需手动检查目标平台的链接配置以及特性开启情况；在大型生产系统中使用前，建议在 CI 中加入 `compiler_builtins` 的编译与单元测试，确认没有未实现的符号。总体而言，经过适当的依赖和维护审查后，可在生产环境中稳定使用。

## 🧭 Practical evaluation

**Value:** rust-lang/compiler-builtins helps ship user-facing interfaces with less custom UI work.

**Best use cases**

- build product UI faster
- reuse interface components
- improve frontend delivery

**Integration notes:** Needs manual inspection before adoption because integration signals are sparse in the discovered metadata.

**Production readiness:** Medium: useful for prototypes or internal workflows, with dependency and maintenance checks before production.

**Quality signals**

- 498 GitHub stars
- 276 forks
- updated 2026-06-23
- primary language: Rust

**Risks:** Integration path is not obvious from metadata; validate setup cost before committing.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 61/100 |
| stars | 57/100 |
| topics | 0/100 |
| outlook | 47/100 |
| quality | 51/100 |
| recency | 40/100 |
| adoption | 58/100 |
| production | 49/100 |
| usefulness | 42/100 |
| integration | 30/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 0/100 |

---

<sub>🔭 Discovered 2026-06-23 · [View on GitHub](https://github.com/rust-lang/compiler-builtins) · [← Back to Misc](./README.md)</sub>
