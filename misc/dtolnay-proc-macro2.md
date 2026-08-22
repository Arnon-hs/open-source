# dtolnay/proc-macro2

[![Stars](https://img.shields.io/github/stars/dtolnay/proc-macro2?style=flat-square&color=yellow)](https://github.com/dtolnay/proc-macro2/stargazers) [![Forks](https://img.shields.io/github/forks/dtolnay/proc-macro2?style=flat-square&color=blue)](https://github.com/dtolnay/proc-macro2/network) [![Language](https://img.shields.io/badge/lang-Rust-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-52%2F100-brightgreen?style=flat-square)](#)

> _No description provided._

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 931 |
| 🍴 **Forks** | 136 |
| 💻 **Language** | Rust |
| 📈 **Score** | 52/100 |
| 🗓️ **Last push** | 2026-08-22 |
| 🔍 **Source** | github |

## 🏷️ Topics

_no topics_

## 🎯 Categories

Misc

## 📝 Summary

### English

dtolnay/proc-macro2 provides a stable, reusable abstraction over Rust’s procedural‑macro APIs, making it easier to write macros that work across different compiler versions. Adoption requires manually reviewing the README and integrating the crate into your build, as the project’s metadata offers limited automated integration signals. While the crate is actively maintained (931★, 136 forks, last updated 2026‑08‑22) and suitable for prototypes or internal tools, you should verify dependency compatibility and maintenance practices before using it in production‑critical code.

### Русский

We need to produce a brief summary (2-3 sentences) in Russian explaining benefit, typical integration scenario, and production readiness level. Use given info: dtolnay/proc-macro2, Score 52/100, categories Misc, value proposition: may be useful when README and activity match a concrete workflow. Use cases not given. Integration notes: needs manual inspection because integration signals sparse. Production readiness: Medium: useful for prototypes or internal workflows, with dependency and maintenance checks before production. Quality signals: 931 stars, 136 forks, updated 2026-08-22, primary language Rust. Risks: integration path not obvious; validate setup cost.

Thus summary: dtolnay/proc-macro2 — это библиотека Rust для работы с процедурными макросами, предоставляющая абстракцию над proc_macro crate, упрощающая написание и тестирование макросов. Типовой сценарий — интеграция в crates, где требуется кросс‑версионная совместимость макросов (например, в crates‑использующих syn/quote), после ручной проверки зависимостей и

### 中文

dtolnay/proc‑macro2 提供了一个与编译器版本解耦的稳定 TokenStream API，使得编写过程宏时能够独立于特定的 Rust 编译器实现，因而被众多宏库（如 syn、quote）广泛依赖。在项目中只需在 Cargo.toml 中加入 `proc-macro2 = "1"`，然后使用 `proc_macro2::TokenStream` 等类型进行宏的实现和测试。该 crate 被评估为中等生产就绪度，

## 🧭 Practical evaluation

**Value:** dtolnay/proc-macro2 may be useful when its README and activity match a concrete workflow.

**Best use cases**

- Not enough metadata yet.

**Integration notes:** Needs manual inspection before adoption because integration signals are sparse in the discovered metadata.

**Production readiness:** Medium: useful for prototypes or internal workflows, with dependency and maintenance checks before production.

**Quality signals**

- 931 GitHub stars
- 136 forks
- updated 2026-08-22
- primary language: Rust

**Risks:** Integration path is not obvious from metadata; validate setup cost before committing.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 53/100 |
| stars | 63/100 |
| topics | 0/100 |
| outlook | 69/100 |
| quality | 67/100 |
| recency | 100/100 |
| adoption | 60/100 |
| production | 68/100 |
| usefulness | 42/100 |
| integration | 18/100 |
| sourceTrust | 100/100 |

---

<sub>🔭 Discovered 2026-08-22 · [View on GitHub](https://github.com/dtolnay/proc-macro2) · [← Back to Misc](./README.md)</sub>
