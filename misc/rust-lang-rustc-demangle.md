# rust-lang/rustc-demangle

[![Stars](https://img.shields.io/github/stars/rust-lang/rustc-demangle?style=flat-square&color=yellow)](https://github.com/rust-lang/rustc-demangle/stargazers) [![Forks](https://img.shields.io/github/forks/rust-lang/rustc-demangle?style=flat-square&color=blue)](https://github.com/rust-lang/rustc-demangle/network) [![Language](https://img.shields.io/badge/lang-Rust-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-52%2F100-brightgreen?style=flat-square)](#)

> Rust symbol demangling

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 310 |
| 🍴 **Forks** | 65 |
| 💻 **Language** | Rust |
| 📈 **Score** | 52/100 |
| 🗓️ **Last push** | 2026-07-08 |
| 🔍 **Source** | github |

## 🏷️ Topics

_no topics_

## 🎯 Categories

Misc

## 📝 Summary

### English

**Project Summary:** 
The rust-lang/rustc-demangle is an open-source Rust library that facilitates demangling of Rust symbols. It may be useful for specific workflows where demangling is required, such as debugging or logging. However, its adoption path may be challenging due to sparse integration signals and a need for manual inspection.

**Value Proposition:** 
The project's value lies in its ability to demangle Rust symbols, making it useful for developers working with Rust code. While its score is relatively low (52/100), its 310 GitHub stars and 65 forks indicate a moderate level of interest and engagement.

**Practical Adoption Path:**
To adopt this project, developers should manually inspect the integration process and validate the setup cost before committing. The project's documentation and activity may not be sufficient to provide a clear adoption path, making it essential to carefully evaluate its suitability for a specific use case.

**Production Readiness:** 
The project is considered medium production-ready, making it suitable for prototypes or internal workflows. However, it's essential to perform dependency and maintenance checks before deploying it in a production environment. The project's sparse integration signals and lack of clear adoption path may make it more challenging to integrate into existing systems.

### Русский

Резюме проекта rust-lang/rustc-demangle:

rust-lang/rustc-demangle - это открытое исходное проект, предназначенное для демангиляции симболов в Rust. Этот проект может быть полезен в определенных рабочих процессах, в которых требуется демангиляция симболов. rust-lang/rustc-demangle имеет средний уровень готовности к production, что означает, что он может быть использован в прототипах или внутренних рабочих процессах, но требует тщательного проверки и оценки перед внедрением в производственную среду.

### 中文

**Rust symbol demangling开源项目简介**

rust-lang/rustc-demangle 是一个用于 Rust 符号解析的开源项目。它可以帮助开发者解析 Rust 的符号名称，例如函数或变量的名称。

**价值**

rust-lang/rustc-demangle 的价值在于，它可以帮助开发者更好地理解和调试 Rust 代码。通过解析符号名称，可以轻松地找到函数或变量的定义和使用位置，提高开发效率和代码质量。

**典型接入方式**

由于 rust-lang/rustc-demangle 是一个 Rust 库，因此可以通过 Cargo (Rust 的包管理器) 来接入。具体步骤如下：

1. 在 Cargo.toml 文件中添加依赖项：`rustc-demangle = "0.26.2"`
2. 在 Rust 代码中导入库：`use rustc_demangle::demangle;`
3. 使用 `demangle` 函数来解析符号名称：`let demangled_name = demangle("foo::bar");`

**生产可用性**

rust-lang/rustc-demangle 的生产可用性为中等。虽然它是一个稳定的

## 🧭 Practical evaluation

**Value:** rust-lang/rustc-demangle may be useful when its README and activity match a concrete workflow.

**Best use cases**

- Not enough metadata yet.

**Integration notes:** Needs manual inspection before adoption because integration signals are sparse in the discovered metadata.

**Production readiness:** Medium: useful for prototypes or internal workflows, with dependency and maintenance checks before production.

**Quality signals**

- 310 GitHub stars
- 65 forks
- updated 2026-07-08
- primary language: Rust

**Risks:** Integration path is not obvious from metadata; validate setup cost before committing.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 45/100 |
| stars | 53/100 |
| topics | 0/100 |
| outlook | 66/100 |
| quality | 63/100 |
| recency | 100/100 |
| adoption | 51/100 |
| production | 68/100 |
| usefulness | 42/100 |
| integration | 30/100 |
| sourceTrust | 100/100 |

---

<sub>🔭 Discovered 2026-07-08 · [View on GitHub](https://github.com/rust-lang/rustc-demangle) · [← Back to Misc](./README.md)</sub>
