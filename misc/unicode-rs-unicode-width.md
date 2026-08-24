# unicode-rs/unicode-width

[![Stars](https://img.shields.io/github/stars/unicode-rs/unicode-width?style=flat-square&color=yellow)](https://github.com/unicode-rs/unicode-width/stargazers) [![Forks](https://img.shields.io/github/forks/unicode-rs/unicode-width?style=flat-square&color=blue)](https://github.com/unicode-rs/unicode-width/network) [![Language](https://img.shields.io/badge/lang-Rust-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-43%2F100-brightgreen?style=flat-square)](#)

> Displayed width of Unicode characters and strings according to UAX#11 rules.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 302 |
| 🍴 **Forks** | 37 |
| 💻 **Language** | Rust |
| 📈 **Score** | 43/100 |
| 🗓️ **Last push** | 2026-08-24 |
| 🔍 **Source** | github |

## 🏷️ Topics

_no topics_

## 🎯 Categories

Misc

## 📝 Summary

### English

**Brief summary**  
unicode‑rs/unicode‑width is a small Rust library that computes the displayed column width of Unicode code points and strings following the Unicode Standard Annex #11 (UAX‑11) East‑Asian Width rules. It is useful for terminal‑based UI, text layout, and any situation where accurate visual alignment of mixed‑script text is required.

**Value proposition**  
The crate abstracts the complex width‑lookup tables and edge‑case handling (combining marks, ambiguous characters, etc.) into a simple API (`UnicodeWidthChar`, `UnicodeWidthStr`). This saves developers from re‑implementing the UAX‑11 logic and reduces bugs in command‑line tools, log formatters, and text editors that need precise column calculations.

**Practical adoption path**  
1. **Evaluate the API** – add the crate as a dev‑dependency and call `char.width()` or `str.width()` on a few representative strings in a sandbox project.  
2. **Check compatibility** – ensure the crate’s supported Rust edition (2021) aligns with your codebase and that no conflicting transitive dependencies exist.  
3. **Run the test suite** – the library ships with comprehensive tests; running them locally confirms that the build works in your environment.  
4. **Integrate** – replace any ad‑hoc width calculations with the library calls, and add unit tests around the new code paths.

**Production readiness**  
- **Maturity**: 302 stars, 37 forks, and recent activity (last commit 2026‑07‑02) indicate an active, community‑maintained project.  
- **Stability**: The API is stable and well‑documented; no major breaking changes have been announced.  
- **Risk**: The integration path is not explicitly described in the metadata, so a brief manual review is needed to confirm build and licensing compatibility.  
- **Recommendation**: Suitable for prototypes, internal tools, and production services after a short validation phase (run the library’s tests, confirm no hidden dependencies, and perform a performance sanity check). With those checks in place, it can be considered medium‑risk ready for production use.

### Русский

`unicode-rs/unicode-width` — небольшая Rust‑библиотека, вычисляющая отображаемую ширину Unicode‑символов и строк по правилам UAX #11, что позволяет корректно выравнивать текст в терминалах, таблицах и UI‑компонентах. Она подходит для прототипов и внутренних сервисов, где требуется точный расчёт ширины символов (например, при построении консольных таблиц или логов), но перед использованием в продакшене следует проверить совместимость со сборкой и убедиться, что её API удобно интегрировать в ваш код. По текущим метрикам проект имеет умеренную популярность (302 ★, 37 форков), активен (обновление 2026‑07‑02) и находится на среднем уровне готовности: пригоден для production после небольшого аудита зависимости и тестов.

### 中文

**unicode-rs/unicode-width 介绍**

unicode-rs/unicode-width 是一个用于计算 Unicode 字符和字符串显示宽度的 Rust 库，遵循 UAX#11 规则。它可以用于各种场景中，例如文本处理和界面设计。

**价值**

unicode-rs/unicode-width 的价值在于，它可以帮助开发者准确计算 Unicode 文本的显示宽度，从而提高软件的用户体验。它特别适用于需要处理国际化文本的应用。

**典型接入方式**

由于该库的文档和活动信息有限，因此需要手动检查和测试才能确定其接入方式。一般来说，可以通过以下步骤接入该库：

1. 添加依赖：在 Rust 项目中添加 `unicode-width` 依赖。
2. 导入库：导入 `unicode-width` 库并使用其 API。
3. 调用函数：调用 `unicode_width` 或 `unicode_width_char` 函数计算 Unicode 文本的显示宽度。

**生产可用性**

unicode-rs/unicode-width 的生产可用性为中等。它可以用于 prototyping 或内部工作流，但需要在生产环境中

## 🧭 Practical evaluation

**Value:** unicode-rs/unicode-width may be useful when its README and activity match a concrete workflow.

**Best use cases**

- Not enough metadata yet.

**Integration notes:** Needs manual inspection before adoption because integration signals are sparse in the discovered metadata.

**Production readiness:** Medium: useful for prototypes or internal workflows, with dependency and maintenance checks before production.

**Quality signals**

- 302 GitHub stars
- 37 forks
- updated 2026-07-02
- primary language: Rust

**Risks:** Integration path is not obvious from metadata; validate setup cost before committing.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 39/100 |
| stars | 53/100 |
| topics | 0/100 |
| outlook | 45/100 |
| quality | 47/100 |
| recency | 40/100 |
| adoption | 49/100 |
| production | 48/100 |
| usefulness | 42/100 |
| integration | 30/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 0/100 |

---

<sub>🔭 Discovered 2026-07-02 · [View on GitHub](https://github.com/unicode-rs/unicode-width) · [← Back to Misc](./README.md)</sub>
