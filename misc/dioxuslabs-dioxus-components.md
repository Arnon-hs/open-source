# DioxusLabs/dioxus-components

[![Stars](https://img.shields.io/github/stars/DioxusLabs/dioxus-components?style=flat-square&color=yellow)](https://github.com/DioxusLabs/dioxus-components/stargazers) [![Forks](https://img.shields.io/github/forks/DioxusLabs/dioxus-components?style=flat-square&color=blue)](https://github.com/DioxusLabs/dioxus-components/network) [![Language](https://img.shields.io/badge/lang-Rust-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-51%2F100-brightgreen?style=flat-square)](#)

> Accessible, unstyled, foundational components for Dioxus.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 298 |
| 🍴 **Forks** | 63 |
| 💻 **Language** | Rust |
| 📈 **Score** | 51/100 |
| 🗓️ **Last push** | 2026-09-05 |
| 🔍 **Source** | github |

## 🏷️ Topics

`components` `dioxus` `rust`

## 🎯 Categories

Misc

## 📝 Summary

### English

**Brief Summary**  
Dioxus‑components is an open‑source library that provides a small set of accessible, unstyled “building‑block” UI components for the Dioxus Rust framework. The components are deliberately minimal so they can be styled or extended to fit any design system, making them a good starting point for prototypes or internal tools that need accessibility out of the box.

**Value**  
- **Accessibility first** – each component follows WAI‑ARIA best practices, saving you the effort of retro‑fitting accessibility later.  
- **Unstyled** – no opinionated CSS or design system is imposed, so you can apply your own styling or integrate with existing design tokens without fighting default styles.  
- **Rust‑native** – written in pure Rust and tightly coupled to Dioxus, it avoids the overhead of bridging to JavaScript or external UI libraries.  
- **Lightweight** – with only a few dozen components, the crate adds minimal compile‑time and binary size overhead.

**Practical Adoption Path**  

| Step | Action | Why it matters |
|------|--------|----------------|
| 1️⃣  | **Review the README & examples** – clone the repo, run `cargo run --example <example_name>` to see the components in action. | Confirms that the API matches your intended UI patterns and that the docs are sufficient for your team. |
| 2️⃣  | **Add the crate** – add `dioxus-components = "0.?"` (use the latest tag) to your `Cargo.toml`. | Straightforward dependency addition; the crate has no heavy external dependencies. |
| 3️⃣  | **Prototype a screen** – replace any ad‑hoc Dioxus markup with the library’s components (e.g., `<Button>`, `<Modal>`, `<Checkbox>`). | Gives you a concrete sense of the ergonomics, type‑safety, and how easy it is to apply custom styling. |
| 4️⃣  | **Run the accessibility audit** – use tools like axe‑core (via `dioxus-cli` or browser extensions) on the rendered output. | Verifies the promised accessibility guarantees in your actual usage context. |
| 5️⃣  | **Integrate with your styling pipeline** – apply CSS‑in‑Rust solutions (e.g., `dioxus‑styled`, Tailwind via `dioxus‑tailwind`) or inline style props. | Ensures the unstyled components can be themed consistently with the rest of your product. |
| 6️⃣  | **Lock the version & add CI checks** – pin the crate version, add a CI job that builds the project and runs `cargo test` + an accessibility lint. | Reduces risk of future breaking changes and guarantees ongoing compliance. |

**Production Readiness**  
- **Maturity** – 298 ★ on GitHub, 63 forks, and recent activity (last commit 2026‑05‑12) indicate a healthy, actively maintained project.  
- **Stability** – The library follows semantic versioning, but because it is still relatively small (few components) and the API surface can evolve, treat it as **medium‑risk** for mission‑critical production.  
- **Suitable Use Cases** – Ideal for internal tools, prototypes, or as a base layer for a custom design system that you will style yourself. For large‑scale consumer‑facing products, perform a short‑term pilot, lock the version, and monitor the repo for breaking changes.  

**Bottom Line**  
If you need accessible, framework‑native UI primitives for Dioxus and are comfortable styling them yourself, `dioxus‑components` offers a lightweight, well‑maintained starting point. Adopt it by first prototyping a few screens, confirming the accessibility and styling workflow, and then freezing the dependency version before rolling it out to production.

### Русский

**DioxusLabs/dioxus-components** — это набор доступных, без стилизации базовых компонентов для фреймворка Dioxus, позволяющий быстро собрать пользовательский UI, не привязываясь к конкретному дизайну. Их обычно подключают в прототипы или внутренние инструменты, где требуется гибкая и полностью контролируемая разметка, после чего стили добавляются отдельно. Проект имеет умеренную готовность к продакшену (много звёзд, активные обновления, но интеграция требует ручного анализа и проверки совместимости с текущей сборкой).

### 中文

**项目简介**  
Dioxus‑Labs 的 **dioxus-components** 是一套为 Dioxus 框架提供的可访问（ARIA‑compliant）、无样式、基础 UI 组件库。它只实现最小化的行为与结构，留给使用者自行决定样式和主题，从而在保持可访问性的前提下，灵活地构建任意前端界面。

**价值**  
- **可访问性即插即用**：所有组件均已内置符合 WCAG/ARIA 的实现，省去自行编写可访问性代码的工作量。  
- **极简且可组合**：仅提供结构和交互，不带任何 CSS，方便与现有的设计系统、Tailwind、styled‑components 等方案无缝对接。  
- **与 Dioxus 原生兼容**：基于 Rust 与 Dioxus 的虚拟 DOM，使用时无需额外桥接层，保持编译期安全与高性能。

**典型接入方式**  
1. **在 Cargo.toml 中添加依赖**  
   ```toml
   [dependencies]
   dioxus-components = "0.2"   # 具体版本请参考仓库的 Release
   ```
2. **在代码中引入并使用**  
   ```rust
   use dioxus::prelude::*;
   use dioxus_components::button::Button;

   fn app(cx: Scope) -> Element {
       cx.render(rsx! {
           Button {
               // 组件本身不提供样式，只负责可访问性与交互
               onclick: move |_| println!("Clicked!"),
               "点击我"
           }
       })
   }
   ```
3. **自行添加样式**（可选）  
   - 通过全局 CSS、Tailwind、或 `style` 属性为组件提供视觉样式。  
   - 也可以封装自己的包装组件，复用统一的主题。

**生产可用性**  
- **成熟度**：已有 298 ⭐、63 🍴，最近一次提交在 2026‑05‑12，活跃度尚可。  
- **适用场景**：非常适合原型、内部工具或需要快速保证可访问性的项目；对外部产品也可使用，只要在上线前完成样式统一和充分的测试。  
- **风险与注意事项**  
  - 组件本身不提供 UI，需自行维护样式层，可能增加前端设计工作量。  
  - 依赖 Dioxus 生态，若项目使用其他前端框架则不适用。  
  - 在生产环境部署前，请检查库的兼容性（Rust 版本、Dioxus 版本）以及是否有活跃的维护者响应 issue。  

综上，`dioxus-components` 为 Dioxus 项目提供了“一键可访问、零样式”的基础组件，接入成本低，适合对可访问性有要求且愿意自行管理 UI 样式的团队，在做好依赖审查和样式统一后，可安全用于生产环境。

## 🧭 Practical evaluation

**Value:** DioxusLabs/dioxus-components may be useful when its README and activity match a concrete workflow.

**Best use cases**

- Not enough metadata yet.

**Integration notes:** Needs manual inspection before adoption because integration signals are sparse in the discovered metadata.

**Production readiness:** Medium: useful for prototypes or internal workflows, with dependency and maintenance checks before production.

**Quality signals**

- 298 GitHub stars
- 63 forks
- updated 2026-05-12
- primary language: Rust
- 3 topics

**Risks:** Integration path is not obvious from metadata; validate setup cost before committing.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 45/100 |
| stars | 53/100 |
| topics | 38/100 |
| outlook | 63/100 |
| quality | 63/100 |
| recency | 80/100 |
| adoption | 51/100 |
| production | 63/100 |
| usefulness | 42/100 |
| integration | 30/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 0/100 |

---

<sub>🔭 Discovered 2026-05-12 · [View on GitHub](https://github.com/DioxusLabs/dioxus-components) · [← Back to Misc](./README.md)</sub>
