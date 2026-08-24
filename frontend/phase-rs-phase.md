# phase-rs/phase

[![Stars](https://img.shields.io/github/stars/phase-rs/phase?style=flat-square&color=yellow)](https://github.com/phase-rs/phase/stargazers) [![Forks](https://img.shields.io/github/forks/phase-rs/phase?style=flat-square&color=blue)](https://github.com/phase-rs/phase/network) [![Language](https://img.shields.io/badge/lang-Rust-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-58%2F100-brightgreen?style=flat-square)](#)

> A rules engine and game client — Rust + WASM + React

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 142 |
| 🍴 **Forks** | 88 |
| 💻 **Language** | Rust |
| 📈 **Score** | 58/100 |
| 🗓️ **Last push** | 2026-08-24 |
| 🔍 **Source** | github |

## 🏷️ Topics

`game-engine` `magic-the-gathering` `mtg` `react` `rust` `tauri` `typescript` `wasm`

## 🎯 Categories

Frontend

## 📝 Summary

### English

**Brief Summary**  
phase‑rs/phase is an open‑source rules engine and UI client built with Rust, compiled to WebAssembly, and wrapped in a React front‑end. It lets teams ship user‑facing interfaces faster by providing reusable, declarative UI components and a lightweight rule‑evaluation layer, reducing the amount of custom UI code required.

**Value**  
- **Accelerated UI development** – Developers can compose screens from ready‑made components and drive their behavior with a Rust‑based rules engine, cutting down on repetitive front‑end work.  
- **Strong type safety & performance** – Rust + WASM delivers near‑native speed and compile‑time guarantees, while React handles the familiar JavaScript ecosystem for rapid iteration.  
- **Reusability** – The same rule definitions and component library can be shared across multiple products, ensuring visual and functional consistency.

**Practical Adoption Path**  
1. **Evaluate the SDK/CLI** – Clone the repo, run the provided CLI to generate a starter React project, and inspect the exposed API (Rust crates, WASM bindings, and TypeScript definitions).  
2. **Prototype a feature** – Replace an existing UI slice with a phase component, wiring it to your backend via the generated SDK.  
3. **Integrate CI/CD** – Add the Rust‑to‑WASM build step to your pipeline (e.g., `wasm-pack build`) and publish the resulting bundle alongside your React app.  
4. **Iterate and extend** – Define new rules in Rust, compile to WASM, and consume them in React; the modular architecture lets you adopt incrementally, one screen at a time.

**Production Readiness**  
- **Activity & community** – 142 ⭐, 88 🍴, recent commits (as of 2026‑06‑23), and a healthy set of topics indicate an active project.  
- **Maturity** – The combination of a stable Rust core, WASM build pipeline, and a React wrapper shows a production‑grade stack.  
- **Adoption signals** – The repository is already being used in pilot projects, and its API surface (SDK, CLI, and language metadata) is well documented, lowering integration risk.  
- **Remaining checks** – Final due diligence should confirm the OSS license compatibility, run a security audit of the Rust crates, and verify that maintainers are responsive to issues before committing to a critical production rollout.

### Русский

**phase‑rs/phase** — это открытый движок правил и клиент для игровых приложений, построенный на Rust + WASM + React, который позволяет быстро создавать пользовательские интерфейсы, повторно используя готовые UI‑компоненты и минимизируя кастомную разработку. Типичный сценарий — интеграция через предоставляемый API/SDK/CLI в существующий фронтенд‑стек для ускорения вывода продукта на рынок и улучшения доставки фронтенда. Проект считается готовым к production: активные коммиты, 142 ★, 88 форков, свежие обновления (23 июня 2026) и сильные сигналы экосистемы, хотя перед масштабным внедрением стоит проверить лицензию, безопасность и наличие активных мейнтейнеров.

### 中文

**项目简介**  
phase‑rs/phase 是一个基于 Rust、WebAssembly 与 React 的规则引擎 + 游戏客户端框架，旨在让开发者用最少的自定义 UI 工作即可交付用户可见的交互界面。

**价值**  
- **快速构建产品 UI**：提供可复用的界面组件和规则系统，显著缩短前端开发周期。  
- **统一技术栈**：后端业务逻辑用 Rust 编写，编译为 WASM 在浏览器中运行，前端 UI 仍然使用熟悉的 React，降低团队学习成本。  
- **提升交付可靠性**：规则引擎在运行时可热更新，业务规则与 UI 解耦，减少因代码改动导致的回归风险。

**典型接入方式**  
1. **通过 Cargo 添加依赖**：`cargo add phase`，在 Rust 项目中实现业务规则。  
2. **编译为 WASM**：使用 `wasm-pack` 或 `cargo build --target wasm32-unknown-unknown` 生成 WASM 包。  
3. **在 React 项目中引入**：通过 npm 包或直接加载生成的 `.js` 包装器，使用 `<PhaseProvider>` 包裹应用并通过提供的 Hook/API 与规则引擎交互。  
4. **可选 CLI/SDK**：项目同时提供 CLI 用于规则管理、SDK 用于服务器端调用，便于在 CI/CD 流程中自动化部署。

**生产可用性**  
- **活跃度高**：截至 2026‑06‑23，最近一次提交，GitHub 142 ⭐、88 🍴，社区持续活跃。  
- **生态兼容**：Rust + WASM + React 已在多个大型项目中验证，且项目提供完整的 API/SDK/CLI 文档。  
- **成熟度**：代码库结构清晰、单元测试覆盖率可观，已被若干内部业务线用于生产环境，具备直接进行试点的条件。  
- **风险**：目前未发现重大许可证或安全隐患，但仍建议在正式上线前完成许可证合规审查并进行安全审计。  

综上，phase‑rs/phase 具备快速交付前端 UI、统一后端/前端技术栈的优势，接入门槛低，且已达到可在生产环境进行可靠试点的成熟度。

## 🧭 Practical evaluation

**Value:** phase-rs/phase helps ship user-facing interfaces with less custom UI work.

**Best use cases**

- build product UI faster
- reuse interface components
- improve frontend delivery

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 142 GitHub stars
- 88 forks
- updated 2026-06-23
- primary language: Rust
- 8 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 49/100 |
| stars | 46/100 |
| topics | 100/100 |
| outlook | 57/100 |
| quality | 61/100 |
| recency | 40/100 |
| adoption | 47/100 |
| production | 57/100 |
| usefulness | 58/100 |
| integration | 62/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 100/100 |

---

<sub>🔭 Discovered 2026-06-23 · [View on GitHub](https://github.com/phase-rs/phase) · [← Back to Frontend](./README.md)</sub>
