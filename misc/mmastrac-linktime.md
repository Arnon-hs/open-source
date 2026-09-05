# mmastrac/linktime

[![Stars](https://img.shields.io/github/stars/mmastrac/linktime?style=flat-square&color=yellow)](https://github.com/mmastrac/linktime/stargazers) [![Forks](https://img.shields.io/github/forks/mmastrac/linktime?style=flat-square&color=blue)](https://github.com/mmastrac/linktime/network) [![Language](https://img.shields.io/badge/lang-Rust-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-47%2F100-brightgreen?style=flat-square)](#)

> Link-time initialization, destruction, scattered data collection macros for Rust

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 988 |
| 🍴 **Forks** | 72 |
| 💻 **Language** | Rust |
| 📈 **Score** | 47/100 |
| 🗓️ **Last push** | 2026-09-05 |
| 🔍 **Source** | github |

## 🏷️ Topics

`constructor` `ctor` `dtor` `dylib` `link-section` `linktime` `macros` `rust`

## 🎯 Categories

Misc

## 📝 Summary

### English

mmastrac/linktime is a lightweight Rust library that provides macros for safe link‑time initialization and destruction of static data, as well as utilities for gathering scattered data across compilation units. By leveraging linker sections, it enables zero‑cost, compile‑time registration of callbacks, resources, or configuration tables without runtime overhead, making it ideal for embedded, plugin, or low‑level systems programming.

### Русский

`mmastrac/linktime` — это набор макросов для Rust, упрощающих работу с инициализацией и деструкцией данных во время линковки, а также сбором «разбросанных» (scattered) данных. Он позволяет объявлять и автоматически управлять глобальными ресурсами, гарантируя их корректный порядок создания и освобождения без необходимости писать boilerplate‑код. Проект полезен в системном и низкоуровневом программировании, где важен контроль над временем жизни статических объектов.

### 中文

mmastrac/linktime：mmastrac/linktime may be useful when its README and activity match a concrete workflow.。适合用于Misc。Early or unclear: treat as research material until maintenance, releases, docs, and issue activity are verified.

## 🧭 Practical evaluation

**Value:** mmastrac/linktime may be useful when its README and activity match a concrete workflow.

**Best use cases**

- Not enough metadata yet.

**Integration notes:** Looks feasible to evaluate, but integration should start with a small proof of concept and README check.

**Production readiness:** Early or unclear: treat as research material until maintenance, releases, docs, and issue activity are verified.

**Quality signals**

- 988 GitHub stars
- 72 forks
- updated 2026-05-08
- primary language: Rust
- 8 topics

**Risks:** Integration path is not obvious from metadata; validate setup cost before committing.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 47/100 |
| stars | 64/100 |
| topics | 100/100 |
| outlook | 50/100 |
| quality | 62/100 |
| recency | 20/100 |
| adoption | 59/100 |
| production | 48/100 |
| usefulness | 42/100 |
| integration | 30/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 0/100 |

---

<sub>🔭 Discovered 2026-05-08 · [View on GitHub](https://github.com/mmastrac/linktime) · [← Back to Misc](./README.md)</sub>
