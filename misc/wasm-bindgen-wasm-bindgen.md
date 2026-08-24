# wasm-bindgen/wasm-bindgen

[![Stars](https://img.shields.io/github/stars/wasm-bindgen/wasm-bindgen?style=flat-square&color=yellow)](https://github.com/wasm-bindgen/wasm-bindgen/stargazers) [![Forks](https://img.shields.io/github/forks/wasm-bindgen/wasm-bindgen?style=flat-square&color=blue)](https://github.com/wasm-bindgen/wasm-bindgen/network) [![Language](https://img.shields.io/badge/lang-Rust-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-50%2F100-brightgreen?style=flat-square)](#)

> Facilitating high-level interactions between Wasm modules and JavaScript

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 9k |
| 🍴 **Forks** | 1.2k |
| 💻 **Language** | Rust |
| 📈 **Score** | 50/100 |
| 🗓️ **Last push** | 2026-08-24 |
| 🔍 **Source** | github |

## 🏷️ Topics

`binding-generator` `javascript` `rust` `rust-wasm` `wasm`

## 🎯 Categories

Misc

## 📝 Summary

### English

**Summary**  
wasm‑bindgen is a Rust library that generates the glue code needed for seamless, high‑level communication between WebAssembly modules and JavaScript. It automates the export of Rust functions, structs, and enums to JavaScript and the import of JavaScript APIs into Rust, dramatically reducing the boilerplate and type‑mismatch errors that normally accompany Wasm‑JS interop.

**Value**  
By handling the low‑level details of memory layout, type conversion, and JS‑to‑Wasm calling conventions, wasm‑bindgen lets developers write idiomatic Rust code while still exposing a clean, type‑safe JavaScript API. This accelerates feature development, improves maintainability, and enables Rust‑centric teams to leverage the existing JavaScript ecosystem (DOM, npm packages, etc.) without writing manual bindings.

**Practical adoption path**  
1. **Proof‑of‑concept** – Scaffold a small Rust crate with `wasm-pack new` and add `wasm-bindgen` as a dependency. Follow the README to compile to Wasm (`wasm-pack build`) and import the generated JS module in a minimal web page.  
2. **Iterative expansion** – Incrementally expose additional Rust functions/structs via the `#[wasm_bindgen]` attribute, verifying that the generated TypeScript definitions match your expectations.  
3. **CI integration** – Add the `wasm-pack` build step to your CI pipeline, and optionally publish the generated npm package for consumption by the rest of your front‑end codebase.  
4. **Full‑scale migration** – Replace hand‑written JS glue with wasm‑bindgen bindings across the codebase, using the library’s support for async, closures, and DOM APIs as needed.

**Production readiness**  
The project is highly mature: over 8 900 stars, 1 200 forks, continuous commits (last updated today), and broad adoption in the Rust‑WebAssembly ecosystem (e.g., Yew, Seed, and Trunk). Its active maintainers, extensive documentation, and proven use in production‑grade applications make it a safe candidate for a serious pilot, provided the initial integration effort (tooling setup, build pipeline) is validated with a small proof‑of‑concept first.

### Русский

wasm-bindgen — это библиотека, позволяющая легко связывать WebAssembly‑модули, написанные на Rust, с JavaScript‑кодом, автоматически генерируя типобезопасные обёртки и упрощая передачу данных и вызов функций между двумя средами. Типичный сценарий внедрения — добавить небольшую proof‑of‑concept в существующее веб‑приложение, проверить генерацию биндов через `wasm-bindgen-cli` и затем интегрировать полученные JS‑модули в сборку. Проект имеет высокую готовность к production: активная поддержка, более 8 000 звёзд, регулярные обновления и широкое принятие в экосистеме Rust/Wasm.

### 中文

**项目简介（2‑3 句）**  
wasm‑bindgen 是 Rust 官方提供的工具链，帮助开发者在 WebAssembly 模块与 JavaScript 之间进行高级、类型安全的交互。它自动生成绑定代码，使得 Rust 编写的业务逻辑可以像普通 JS 库一样直接在浏览器或 Node.js 中调用。

**价值**  
- **零成本的类型映射**：在 Rust 与 JavaScript 之间自动完成结构体、枚举、函数等的序列化/反序列化，避免手写繁琐的 glue 代码。  
- **提升开发效率**：通过宏和生成的 `*.js` 包装器，开发者可以在 Rust 中使用原生的 `async/await`、`Promise` 等 JS 特性，反之亦然。  
- **生态兼容**：与 `wasm-pack`、`cargo`、`npm` 完全集成，生成的包可以直接发布到 npm，供前端团队使用。

**典型接入方式**  

| 步骤 | 操作 | 说明 |
|------|------|------|
| 1️⃣ 初始化项目 | `cargo new --lib my_wasm` | 创建 Rust 库项目。 |
| 2️⃣ 添加依赖 | `cargo add wasm-bindgen` | 引入 `wasm-bindgen` crate。 |
| 3️⃣ 编写绑定代码 | ```rust<br>use wasm_bindgen::prelude::*;<br>#[wasm_bindgen] pub fn add(a: i32, b: i32) -> i32 { a + b }<br>``` | 使用 `#[wasm_bindgen]` 宏标记要导出的函数/结构体。 |
| 4️⃣ 编译为 Wasm | `wasm-pack build --target web`（或 `nodejs`） | `wasm-pack` 会调用 `wasm-bindgen`，生成 `.wasm`、`js` 包装文件和 `package.json`。 |
| 5️⃣ 前端使用 | ```js<br>import init, { add } from './my_wasm_pkg';<br>await init();<br>console.log(add(2,3));<br>``` | 在 Web/Node 项目中通过 npm 安装生成的包，即可调用 Rust 实现的函数。 |
| 6️⃣ CI/CD 集成 | 在 CI 中加入 `wasm-pack test --headless --chrome` 等命令，确保编译和单元测试通过。 | 自动化验证兼容性和性能。 |

**生产可用性**  
- **活跃度**：截至 2026‑05‑13，项目仍在持续更新，拥有近 9k ⭐、1.2k 🍴，社区活跃。  
- **生态成熟度**：已被大量开源库（如 `yew`, `seed`, `wasm-bindgen-futures`）和企业项目采用，具备完善的文档、示例和常见问题解答。  
- **稳定性**：`wasm-bindgen` 版本遵循语义化版本号，向后兼容性良好；配套的 `wasm-pack`、`cargo` 插件均为官方维护。  
- **风险评估**：主要风险在于首次集成的学习成本和构建环境（需要 Rust、wasm‑target、Node/npm）。建议先在一个小型功能（如纯计算函数）做 PoC，验证编译、加载时的体积和性能，再逐步迁移更复杂的业务逻辑。  

**结论**：基于其强大的类型绑定能力、活跃的社区和成熟的工具链，wasm‑bindgen 完全可以在生产环境中使用，适合作为 Rust‑to‑JS 交互的首选桥梁。只要做好前期的构建脚本和 CI 配置，即可平滑引入现有前端项目。

## 🧭 Practical evaluation

**Value:** wasm-bindgen/wasm-bindgen may be useful when its README and activity match a concrete workflow.

**Best use cases**

- Not enough metadata yet.

**Integration notes:** Looks feasible to evaluate, but integration should start with a small proof of concept and README check.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 8989 GitHub stars
- 1211 forks
- updated 2026-05-13
- primary language: Rust
- 5 topics

**Risks:** Integration path is not obvious from metadata; validate setup cost before committing.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 77/100 |
| stars | 84/100 |
| topics | 63/100 |
| outlook | 52/100 |
| quality | 66/100 |
| recency | 20/100 |
| adoption | 82/100 |
| production | 50/100 |
| usefulness | 42/100 |
| integration | 30/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 0/100 |

---

<sub>🔭 Discovered 2026-05-13 · [View on GitHub](https://github.com/wasm-bindgen/wasm-bindgen) · [← Back to Misc](./README.md)</sub>
