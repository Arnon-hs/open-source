# dtolnay/thiserror

[![Stars](https://img.shields.io/github/stars/dtolnay/thiserror?style=flat-square&color=yellow)](https://github.com/dtolnay/thiserror/stargazers) [![Forks](https://img.shields.io/github/forks/dtolnay/thiserror?style=flat-square&color=blue)](https://github.com/dtolnay/thiserror/network) [![Language](https://img.shields.io/badge/lang-Rust-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-54%2F100-brightgreen?style=flat-square)](#)

> derive(Error) for struct and enum error types

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 5.5k |
| 🍴 **Forks** | 210 |
| 💻 **Language** | Rust |
| 📈 **Score** | 54/100 |
| 🗓️ **Last push** | 2026-09-05 |
| 🔍 **Source** | github |

## 🏷️ Topics

_no topics_

## 🎯 Categories

Misc

## 📝 Summary

### English

**Brief Summary**  
`dtolnay/thiserror` is a lightweight Rust crate that provides a `#[derive(Error)]` macro for turning structs and enums into implementations of the standard `std::error::Error` trait. With over 5 400 stars and active maintenance (last updated 2026‑06‑24), it streamlines error handling while keeping the code concise and type‑safe.

**Value**  
- **Zero‑boilerplate error types** – The macro automatically generates `Display` and `source` implementations, letting developers focus on the business logic rather than repetitive error‑handling code.  
- **Strong type safety** – Errors remain distinct Rust types, enabling pattern matching and fine‑grained handling without sacrificing ergonomics.  
- **Ecosystem compatibility** – Works seamlessly with other error‑handling crates (e.g., `anyhow`, `eyre`) and with the standard library, making it a drop‑in improvement for most Rust projects.

**Practical Adoption Path**  
1. **Evaluate the README** – Verify that the macro’s capabilities (custom messages, source chaining, #[from] conversions) align with your project’s error‑design guidelines.  
2. **Add the dependency** – Add `thiserror = "1"` (or the latest version) to `Cargo.toml`.  
3. **Prototype** – Convert a few existing error structs/enums to `#[derive(Error)]` and run the test suite to confirm that `Display` output and source chaining behave as expected.  
4. **Code review** – Ensure the generated code meets your linting and documentation standards; the macro is well‑documented, but a quick manual inspection is advisable.  
5. **Full migration** – Once the prototype passes, replace remaining manual `Error` impls across the codebase.

**Production Readiness**  
- **Maturity**: Medium‑high. The crate is widely adopted (5 459 stars, 210 forks) and receives regular updates, indicating a stable core.  
- **Risk**: The integration surface is small (just a macro), but because the crate does not expose a runtime API, the primary risk is mismatched expectations about features (e.g., custom `source` handling). A brief validation step—compiling a representative module—mitigates this.  
- **Recommendation**: Suitable for prototypes, internal services, and production workloads after the above validation steps; ensure you monitor the crate’s changelog for breaking changes before major version upgrades.

### Русский

**ThisError** — это лёгкая макрос‑библиотека для Rust, позволяющая автоматически генерировать реализации `std::error::Error` для ваших `struct` и `enum` через `#[derive(Error)]`. Она идеальна для быстрого прототипирования и внутренних сервисов, где требуется единый, читаемый тип ошибок без написания boilerplate‑кода; при достаточной проверке зависимостей и тестировании её можно использовать в продакшене, хотя путь интеграции требует ручного анализа из‑за скудной метаданных. С 5 459 звёздами и активным обновлением (2026‑06‑24) проект считается средне‑готовым к production‑использованию.

### 中文

**简短介绍**  
`dtolnay/thiserror` 为 Rust 的结构体和枚举提供了 `#[derive(Error)]` 宏，使得自定义错误类型的实现变得轻量且易读。只需在错误类型上加上 `#[derive(Error)]` 并使用 `#[error("…")]` 注解错误信息，即可自动生成符合 `std::error::Error` 的实现。

**价值**  
- **降低样板代码**：无需手写 `impl Error`、`Display`、`source` 等实现，几行属性即可完成。  
- **提升可读性**：错误信息直接写在属性里，代码与错误描述保持一一对应，便于维护。  
- **兼容生态**：生成的错误实现完全符合 `std::error::Error`，可无缝与 `anyhow`、`thiserror`、`eyre`、`Result` 等常用错误处理库配合使用。  

**典型接入方式**  
1. **在 `Cargo.toml` 添加依赖**  
   ```toml
   [dependencies]
   thiserror = "1.0"
   ```
2. **在代码中使用宏**  
   ```rust
   use thiserror::Error;

   #[derive(Debug, Error)]
   pub enum MyError {
       #[error("网络错误: {0}")]
       Network(#[from] std::io::Error),

       #[error("解析失败: {0}")]
       Parse(String),
   }
   ```
3. **在业务逻辑中直接返回**  
   ```rust
   fn fetch() -> Result<String, MyError> {
       let data = std::fs::read_to_string("config.toml")?;
       // …
       Ok(data)
   }
   ```

**生产可用性**  
- **成熟度**：已有 5 459+ 星、210+ Fork，活跃维护至 2026‑06‑24，社区使用广泛。  
- **稳定性**：遵循语义化版本（SemVer），向后兼容性良好，适合作为内部或对外库的错误基座。  
- **风险**：集成成本主要在于引入宏依赖和确保错误类型的 `#[error]` 信息符合业务需求；没有额外运行时依赖，几乎不影响二进制体积。  
- **建议**：在原型或内部服务中直接使用；在生产环境部署前，进行一次依赖审计（检查兼容的 Rust 版本、审阅宏展开后的代码），即可安全上线。

## 🧭 Practical evaluation

**Value:** dtolnay/thiserror may be useful when its README and activity match a concrete workflow.

**Best use cases**

- Not enough metadata yet.

**Integration notes:** Needs manual inspection before adoption because integration signals are sparse in the discovered metadata.

**Production readiness:** Medium: useful for prototypes or internal workflows, with dependency and maintenance checks before production.

**Quality signals**

- 5459 GitHub stars
- 210 forks
- updated 2026-06-24
- primary language: Rust

**Risks:** Integration path is not obvious from metadata; validate setup cost before committing.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 58/100 |
| stars | 80/100 |
| topics | 0/100 |
| outlook | 65/100 |
| quality | 68/100 |
| recency | 80/100 |
| adoption | 74/100 |
| production | 65/100 |
| usefulness | 42/100 |
| integration | 30/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 0/100 |

---

<sub>🔭 Discovered 2026-06-24 · [View on GitHub](https://github.com/dtolnay/thiserror) · [← Back to Misc](./README.md)</sub>
