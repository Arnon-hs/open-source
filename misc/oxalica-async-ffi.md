# oxalica/async-ffi

[![Stars](https://img.shields.io/github/stars/oxalica/async-ffi?style=flat-square&color=yellow)](https://github.com/oxalica/async-ffi/stargazers) [![Forks](https://img.shields.io/github/forks/oxalica/async-ffi?style=flat-square&color=blue)](https://github.com/oxalica/async-ffi/network) [![Language](https://img.shields.io/badge/lang-Rust-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-43%2F100-brightgreen?style=flat-square)](#)

> FFI-compatible futures

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 180 |
| 🍴 **Forks** | 18 |
| 💻 **Language** | Rust |
| 📈 **Score** | 43/100 |
| 🗓️ **Last push** | 2026-08-24 |
| 🔍 **Source** | github |

## 🏷️ Topics

`async` `ffi` `rust`

## 🎯 Categories

Misc

## 📝 Summary

### English

oxalica/async-ffi provides FFI‑compatible Rust futures, enabling seamless asynchronous interop between Rust code and foreign language runtimes. Its value lies in letting developers embed async Rust components into C/C++, Python, or other environments without rewriting concurrency logic, provided they follow the documented usage patterns and perform a manual integration check. While the project shows healthy activity (180 ★, recent 2026 update) and is suitable for prototypes or internal tools, production adoption should include dependency vetting, maintenance review, and validation of the integration cost before committing to a stable release.

### Русский

oxalica/async-ffi предоставляет FFI‑совместимые будущие (futures) на Rust, позволяя легко интегрировать асинхронный код с внешними библиотеками и языками. Типовой сценарий — подключение к существующим C/C++‑проектам или другим средам, где требуется обмен асинхронными задачами через FFI, после ручной проверки настроек и зависимостей. Проект имеет средний уровень готовности к production: подходит для прототипов и внутренних workflows, но перед внедрением в продакшн рекомендуется провести аудит интеграции и оценить затраты на поддержку.

### 中文

oxalica/async-ffi 提供了 FFI 兼容的 futures，使得在 Rust 与其他语言之间进行异步交互变得更加直接。通过在项目中引入该 crate，并按照其示例进行手动绑定（如使用 bindgen 或手动声明外部函数），即

## 🧭 Practical evaluation

**Value:** oxalica/async-ffi may be useful when its README and activity match a concrete workflow.

**Best use cases**

- Not enough metadata yet.

**Integration notes:** Needs manual inspection before adoption because integration signals are sparse in the discovered metadata.

**Production readiness:** Medium: useful for prototypes or internal workflows, with dependency and maintenance checks before production.

**Quality signals**

- 180 GitHub stars
- 18 forks
- updated 2026-07-24
- primary language: Rust
- 3 topics

**Risks:** Integration path is not obvious from metadata; validate setup cost before committing.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 32/100 |
| stars | 48/100 |
| topics | 38/100 |
| outlook | 47/100 |
| quality | 50/100 |
| recency | 40/100 |
| adoption | 44/100 |
| production | 49/100 |
| usefulness | 42/100 |
| integration | 30/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 0/100 |

---

<sub>🔭 Discovered 2026-07-24 · [View on GitHub](https://github.com/oxalica/async-ffi) · [← Back to Misc](./README.md)</sub>
