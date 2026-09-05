# google/crubit

[![Stars](https://img.shields.io/github/stars/google/crubit?style=flat-square&color=yellow)](https://github.com/google/crubit/stargazers) [![Forks](https://img.shields.io/github/forks/google/crubit?style=flat-square&color=blue)](https://github.com/google/crubit/network) [![Language](https://img.shields.io/badge/lang-C%2B%2B-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-54%2F100-brightgreen?style=flat-square)](#)

> A bidirectional bindings generator for C++ and Rust.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 1k |
| 🍴 **Forks** | 64 |
| 💻 **Language** | C++ |
| 📈 **Score** | 54/100 |
| 🗓️ **Last push** | 2026-09-05 |
| 🔍 **Source** | github |

## 🏷️ Topics

_no topics_

## 🎯 Categories

Libraries & SDKs

## 📝 Summary

### English

**Brief Summary**  
google/crubit is an open‑source tool that automatically generates bidirectional bindings between C++ and Rust, letting developers call C++ code from Rust and vice‑versa without writing the glue code by hand. With over a thousand stars and recent activity, it can speed up cross‑language prototyping, especially in teams that already use both languages.  

**Value**  
- **Time‑saving**: Generates the boilerplate for FFI, reducing manual `extern "C"` declarations, `#[repr(C)]` structs, and build‑system tweaks.  
- **Consistency**: Guarantees that the generated signatures stay in sync with the source APIs, lowering the risk of mismatched types or calling‑convention bugs.  
- **Bidirectional**: Supports both “Rust‑calls‑C++” and “C++‑calls‑Rust” scenarios, which is rare among FFI generators.  

**Practical Adoption Path**  
1. **Prototype** – Clone the repo, run the provided `crubit` CLI on a small C++ library, and verify the generated Rust bindings compile.  
2. **Code Review** – Manually inspect the generated code for safety‑critical sections (e.g., ownership semantics, `unsafe` blocks) and adjust annotations as needed.  
3. **CI Integration** – Add the `crubit` step to your build pipeline (e.g., as a `cargo` or `bazel` rule) so bindings are regenerated on every change.  
4. **Dependency Check** – Ensure the required toolchain (LLVM/Clang, Rust 1.70+, and any optional `bazel` rules) is available and that the generated code does not introduce unwanted transitive dependencies.  

**Production Readiness**  
- **Maturity**: Medium. The project is actively maintained (last commit 2026‑05‑11) and has a healthy star/fork count, but integration signals are sparse and no formal LTS release exists.  
- **Suitability**: Good for internal tools, prototypes, or services where you control both the C++ and Rust codebases. Before shipping to production, perform a security audit of the generated `unsafe` code, verify the licensing (Apache‑2.0 compatible), and confirm that the maintainers respond to issues relevant to your use case.  
- **Risk Mitigation**: Pin the `crubit` version in your dependency lock file, add regression tests for the generated bindings, and schedule periodic reviews of upstream changes.  

In short, google/crubit can dramatically simplify C++/Rust interop, but it should be introduced behind a review gate and monitored as part of your CI/CD process before being considered production‑grade.

### Русский

**google/crubit** — это генератор двунаправленных биндингов между C++ и Rust, позволяющий автоматически создавать интерфейсы для совместного использования кода на обоих языках. Он подходит для прототипов и внутренних проектов, где требуется быстрый мост между C++‑библиотеками и Rust‑модулями, однако перед выводом в production рекомендуется проверить лицензирование, безопасность и наличие активных поддерживающих разработчиков. При наличии такой проверки проект считается готовым к ограниченному production‑использованию.

### 中文

**项目简介**  
google/crubit 是一个用于 C++ 与 Rust 之间双向绑定的代码生成器，能够自动生成两种语言互相调用所需的桥接层，简化跨语言集成工作。

**价值**  
- **降低跨语言开发成本**：只需编写一次接口定义，即可生成 C++ → Rust 与 Rust → C++ 的绑定代码，避免手写繁琐的 FFI 代码。  
- **保持类型安全**：生成的绑定保留两侧的类型信息，减少手动转换导致的错误。  
- **加速原型与内部工具开发**：在需要快速尝试 Rust 重构或在 C++ 项目中嵌入 Rust 逻辑时，能够迅速搭建可运行的原型。

**典型接入方式**  
1. **在项目根目录添加 `crubit` 配置文件**（如 `crubit.toml`），声明要绑定的 C++ 头文件和对应的 Rust 模块。  
2. **运行 `crubit generate`**，工具会读取配置并在 `out/` 目录生成对应的 Rust FFI 代码与 C++ 包装头文件。  
3. **在 CMake/Makefile 或 Cargo.toml 中引入生成的产物**，完成编译链接。  
4. **手动审查生成的绑定**（尤其是涉及 unsafe 代码的部分），确认符合项目的安全和性能要求后即可投入使用。

**生产可用性**  
- **成熟度**：已有 1007+ 星、64+ Fork，最近一次提交在 2026‑05‑11，活跃度仍在。  
- **适用场景**：适合原型、内部工具或逐步迁移的项目；在正式生产环境使用前，建议进行依赖审计、许可证合规检查以及安全评估。  
- **风险与注意事项**：目前公开的元数据较少，需自行验证生成代码的安全性和性能；同时确认项目维护者的活跃度和长期支持计划。  

总体而言，crubit 在需要 C++ 与 Rust 双向交互的场景下能够显著提升开发效率，适合作为内部或原型阶段的技术选型；在投入生产前应完成必要的审查与测试。

## 🧭 Practical evaluation

**Value:** google/crubit may be useful when its README and activity match a concrete workflow.

**Best use cases**

- Not enough metadata yet.

**Integration notes:** Needs manual inspection before adoption because integration signals are sparse in the discovered metadata.

**Production readiness:** Medium: useful for prototypes or internal workflows, with dependency and maintenance checks before production.

**Quality signals**

- 1007 GitHub stars
- 64 forks
- updated 2026-05-11
- primary language: C++

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 45/100 |
| stars | 64/100 |
| topics | 0/100 |
| outlook | 61/100 |
| quality | 61/100 |
| recency | 80/100 |
| adoption | 59/100 |
| production | 65/100 |
| usefulness | 42/100 |
| integration | 46/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 100/100 |

---

<sub>🔭 Discovered 2026-05-11 · [View on GitHub](https://github.com/google/crubit) · [← Back to Libraries--sdks](./README.md)</sub>
