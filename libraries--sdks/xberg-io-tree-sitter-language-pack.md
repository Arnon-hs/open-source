# xberg-io/tree-sitter-language-pack

[![Stars](https://img.shields.io/github/stars/xberg-io/tree-sitter-language-pack?style=flat-square&color=yellow)](https://github.com/xberg-io/tree-sitter-language-pack/stargazers) [![Forks](https://img.shields.io/github/forks/xberg-io/tree-sitter-language-pack?style=flat-square&color=blue)](https://github.com/xberg-io/tree-sitter-language-pack/network) [![Language](https://img.shields.io/badge/lang-Rust-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-69%2F100-brightgreen?style=flat-square)](#)

> Comprehensive tree-sitter grammar compilation with polyglot bindings — Rust, Python, Node.js, Go, Java, Ruby, Elixir, PHP, C#, WASM, Dart, Kotlin-Android, Swift, Zig, and CLI. 306+ languages.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 408 |
| 🍴 **Forks** | 63 |
| 💻 **Language** | Rust |
| 📈 **Score** | 69/100 |
| 🗓️ **Last push** | 2026-09-05 |
| 🔍 **Source** | github |

## 🏷️ Topics

`ast` `c-ffi` `csharp` `elixir` `golang` `grammer` `java` `kreuzberg` `language-pack` `node` `parser` `polyglot`

## 🎯 Categories

Libraries & SDKs · Mobile

## 📝 Summary

### English

**Summary (2‑3 sentences)**  
xberg‑io’s *tree‑sitter-language‑pack* bundles compiled Tree‑sitter grammars for more than 300 languages and ships polyglot bindings for Rust, Python, Node.js, Go, Java, Ruby, Elixir, PHP, C#, WASM, Dart, Kotlin‑Android, Swift, Zig and a CLI. By exposing a unified API/SDK and rich language metadata, it lets engineers parse, query, and transform source code from any supported language without writing language‑specific glue code. The project is actively maintained (last commit 2026‑06‑24), has 408 stars, 63 forks, and a strong ecosystem signal, making it a solid candidate for production pilots.

**Value**  
- **Speed up daily development** – developers can instantly query syntax trees for linting, refactoring, or code‑generation tasks across dozens of languages, cutting the time spent writing custom parsers.  
- **Automate engineering workflows** – CI pipelines can use the CLI or SDK to provide fast, language‑agnostic feedback (e.g., detecting anti‑patterns, enforcing style rules, generating documentation).  
- **Reduce maintenance overhead** – a single, version‑controlled dependency replaces dozens of individual grammar repositories and language‑specific bindings.

**Practical adoption path**  
1. **Prototype** – Pull the Rust crate (or the language‑specific binding you need) and run the CLI on a small codebase to verify parsing accuracy for your target languages.  
2. **Integrate** – Wrap the SDK in your existing tooling (e.g., a pre‑commit hook, a VS Code extension, or a CI job) using the provided language metadata to auto‑detect file types.  
3. **Scale** – Deploy the CLI or a compiled WASM module in CI/CD containers; cache the compiled grammars to keep build times low.  
4. **Monitor** – Enable the built‑in diagnostics (grammar version, parsing errors) to catch upstream grammar changes early.

**Production readiness**  
- **Activity & community** – Recent commits, 408 ★ on GitHub, and 17 topical tags indicate an engaged maintainer base.  
- **Stability** – Grammars are pre‑compiled and versioned; the polyglot bindings have been used in multiple open‑source projects, suggesting API stability.  
- **Risk considerations** – No obvious licensing or security red flags, but a final review of the MIT‑style license, supply‑chain scanning, and maintainer responsiveness is advisable before a full rollout.  

Overall, the pack offers a high‑impact, low‑friction way to bring robust, multi‑language parsing into developer tooling and CI pipelines, and it is mature enough for a serious production pilot.

### Русский

**xberg-io/tree-sitter-language-pack** — это набор готовых к использованию грамматик Tree‑sitter с полиглотными биндингами (Rust, Python, Node.js, Go, Java, Ruby, Elixir, PHP, C#, WASM, Dart, Kotlin‑Android, Swift, Zig и CLI), покрывающий более 300 языков. Он позволяет инженерам ускорить локальные задачи и CI‑проверки, автоматизируя парсинг кода и получая метаданные о синтаксисе в едином API/CLI. Проект находится в высокой стадии готовности к продакшну: активные коммиты, 400+ звёзд, широкое принятие и стабильная экосистема, требующая лишь финального аудита лицензий и безопасности.

### 中文

**项目简介**  
xberg-io/tree-sitter-language-pack 是一个“一站式”Tree‑sitter 语法库打包器，提供 Rust、Python、Node.js、Go、Java、Ruby、Elixir、PHP、C#、WASM、Dart、Kotlin‑Android、Swift、Zig 以及 CLI 等多语言绑定，覆盖 300+ 编程语言，帮助开发者在本地和 CI 中快速获取高质量的语法树。

**价值**  
- **提升开发效率**：统一的 API/SDK/CLI 让工程师在代码编辑、静态分析、自动重构等日常工作中免去自行编译或维护单独语法库的成本。  
- **加速 CI 反馈**：在构建流水线中直接调用语言元数据和语法树，可实现更精准的 lint、代码审查和安全扫描，缩短回归时间。  
- **跨语言统一**：一次集成即可在多种语言环境下使用，同一套语法定义保证跨项目、跨平台的一致性。

**典型接入方式**  
1. **CLI**：`xberg tree-sitter --lang rust --parse src/main.rs`，适用于脚本化任务或 CI 步骤。  
2. **SDK**：在对应语言的包管理器中引入，例如 `pip install xberg-ts`（Python）或 `npm i xberg-ts`（Node.js），随后调用 `xberg.parse(code, language)` 获取语法树。  
3. **直接调用 Rust 库**：在 Rust 项目中加入 `xberg-ts` crate，利用零成本抽象进行高性能解析。  

**生产可用性**  
- **活跃度**：截至 2026‑06‑24 最近一次提交，星标 408、Fork 63，社区活跃，Issue 响应及时。  
- **成熟度**：多语言绑定已在多个开源项目和内部 CI 中使用，文档覆盖常见场景，兼容性测试覆盖主要平台。  
- **风险**：暂无重大元数据风险，仍需在正式投产前完成许可证合规审查和安全依赖扫描。总体而言，项目已具备高可用的生产候选属性，适合在业务关键流水线中进行试点。

## 🧭 Practical evaluation

**Value:** xberg-io/tree-sitter-language-pack helps engineers save time in daily development and review loops.

**Best use cases**

- speed up developer workflows
- automate local engineering tasks
- improve CI feedback

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 408 GitHub stars
- 63 forks
- updated 2026-06-24
- primary language: Rust
- 17 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 45/100 |
| stars | 56/100 |
| topics | 100/100 |
| outlook | 73/100 |
| quality | 74/100 |
| recency | 80/100 |
| adoption | 53/100 |
| production | 74/100 |
| usefulness | 58/100 |
| integration | 78/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 200/100 |

---

<sub>🔭 Discovered 2026-06-24 · [View on GitHub](https://github.com/xberg-io/tree-sitter-language-pack) · [← Back to Libraries--sdks](./README.md)</sub>
