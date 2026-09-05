# emilk/egui_plot

[![Stars](https://img.shields.io/github/stars/emilk/egui_plot?style=flat-square&color=yellow)](https://github.com/emilk/egui_plot/stargazers) [![Forks](https://img.shields.io/github/forks/emilk/egui_plot?style=flat-square&color=blue)](https://github.com/emilk/egui_plot/network) [![Language](https://img.shields.io/badge/lang-Rust-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-50%2F100-brightgreen?style=flat-square)](#)

> 2D plotting library in Rust for egui

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 439 |
| 🍴 **Forks** | 103 |
| 💻 **Language** | Rust |
| 📈 **Score** | 50/100 |
| 🗓️ **Last push** | 2026-09-05 |
| 🔍 **Source** | github |

## 🏷️ Topics

_no topics_

## 🎯 Categories

Misc

## 📝 Summary

### English

**Brief Summary**  
`emilk/egui_plot` is a lightweight 2‑D plotting library written in Rust that plugs directly into the `egui` immediate‑mode GUI framework. With a clean API and active maintenance (439 ★, 103 forks, last update 2026‑06‑26), it lets developers add interactive charts to user‑facing interfaces without building custom drawing code.

**Value**  
The crate eliminates the need to hand‑craft SVG/Canvas or embed heavyweight JavaScript charting tools, letting Rust teams ship data‑rich front‑ends faster and keep the entire stack in a single language. Reusing the same `egui`‑based components across internal tools and customer‑facing products also reduces UI debt and improves visual consistency.

**Practical Adoption Path**  
1. Add the crate to your `Cargo.toml` and enable the `egui` feature.  
2. Replace existing custom plot code with `egui_plot::Plot` widgets, following the examples in the repository.  
3. Run the library’s demo to verify rendering on your target platform (desktop, WebAssembly, or native).  
Because the integration signals are sparse, a quick proof‑of‑concept is advisable to confirm that the library’s rendering pipeline meshes with your existing `egui` setup and any custom styling you use.

**Production Readiness**  
The project sits at a medium readiness level: it is stable enough for prototypes, internal dashboards, or MVPs, but teams should audit the dependency tree, check for any unresolved issues, and run a small integration test before committing to a production release. Once those checks are done, `egui_plot` can be considered a reliable component for Rust‑based UI pipelines.

### Русский

**emilk/egui_plot** — это открытая 2‑D библиотека построения графиков на Rust, работающая в рамках UI‑фреймворка egui. Она ускоряет создание пользовательских интерфейсов, позволяя быстро добавить готовые визуальные компоненты (графики, диаграммы) без написания собственного UI‑кода, что особенно ценно для прототипов, внутренних инструментов и ускоренного вывода продукта на рынок. Готовность к production — средняя: проект имеет значительную популярность (439 звёзд, 103 форка) и активное обновление, но путь интеграции не полностью описан, поэтому перед внедрением стоит проверить совместимость и оценить затраты на настройку.

### 中文

**项目简介**  
`emilk/egui_plot` 是一个基于 Rust 的 2D 绘图库，专为 **egui** UI 框架设计，提供即插即用的图表组件，帮助开发者在 Rust 应用中快速构建交互式可视化界面。

**价值**  
- **降低 UI 开发成本**：内置常用折线图、散点图、柱状图等组件，免去手写绘图逻辑。  
- **统一技术栈**：全 Rust 实现，和后端业务代码无缝共享数据结构，避免跨语言桥接。  
- **提升交付速度**：可直接在 egui 窗口中嵌入图表，适合原型、内部工具以及面向用户的产品界面。

**典型接入方式**  
1. **添加依赖**：在 `Cargo.toml` 中加入  
   ```toml
   egui_plot = "0.4"
   ```  
2. **在 egui 渲染函数中使用**：  
   ```rust
   use egui_plot::{Plot, Line};

   egui::CentralPanel::default().show(ctx, |ui| {
       Plot::new("my_plot")
           .view_aspect(2.0)
           .show(ui, |plot_ui| {
               let line = Line::new(vec![(0.0, 0.0), (1.0, 2.0), (2.0, 1.5)]);
               plot_ui.line(line);
           });
   });
   ```  
3. **根据需求自定义样式、交互**：库提供丰富的配置 API（坐标轴、缩放、鼠标悬停提示等），可在 `Plot::new` 链式调用中进行调节。

**生产可用性**  
- **成熟度**：GitHub 近 440 ★、100+ Fork，最近一次提交在 2026‑06‑26，活跃度良好。  
- **适用场景**：非常适合原型、内部工具或对 UI 要求不极端的面向用户的产品。  
- **风险与注意事项**：  
  - 元数据中缺少完整的集成示例，首次接入时需要自行验证与现有 egui 版本的兼容性。  
  - 依赖 `egui` 本身的更新节奏，建议在生产环境使用前锁定兼容的 `egui` 版本并进行回归测试。  
- **结论**：在做好依赖审查和基础集成验证后，`egui_plot` 可在生产环境中稳定使用，特别是需要快速交付可视化功能的 Rust 项目。

## 🧭 Practical evaluation

**Value:** emilk/egui_plot helps ship user-facing interfaces with less custom UI work.

**Best use cases**

- build product UI faster
- reuse interface components
- improve frontend delivery

**Integration notes:** Needs manual inspection before adoption because integration signals are sparse in the discovered metadata.

**Production readiness:** Medium: useful for prototypes or internal workflows, with dependency and maintenance checks before production.

**Quality signals**

- 439 GitHub stars
- 103 forks
- updated 2026-06-26
- primary language: Rust

**Risks:** Integration path is not obvious from metadata; validate setup cost before committing.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 50/100 |
| stars | 56/100 |
| topics | 0/100 |
| outlook | 60/100 |
| quality | 60/100 |
| recency | 80/100 |
| adoption | 55/100 |
| production | 62/100 |
| usefulness | 42/100 |
| integration | 30/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 0/100 |

---

<sub>🔭 Discovered 2026-06-26 · [View on GitHub](https://github.com/emilk/egui_plot) · [← Back to Misc](./README.md)</sub>
