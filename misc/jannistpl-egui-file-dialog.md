# jannistpl/egui-file-dialog

[![Stars](https://img.shields.io/github/stars/jannistpl/egui-file-dialog?style=flat-square&color=yellow)](https://github.com/jannistpl/egui-file-dialog/stargazers) [![Forks](https://img.shields.io/github/forks/jannistpl/egui-file-dialog?style=flat-square&color=blue)](https://github.com/jannistpl/egui-file-dialog/network) [![Language](https://img.shields.io/badge/lang-Rust-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-42%2F100-brightgreen?style=flat-square)](#)

> Full featured and customizable file dialog for egui

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 162 |
| 🍴 **Forks** | 29 |
| 💻 **Language** | Rust |
| 📈 **Score** | 42/100 |
| 🗓️ **Last push** | 2026-08-24 |
| 🔍 **Source** | github |

## 🏷️ Topics

_no topics_

## 🎯 Categories

Misc

## 📝 Summary

### English

**Summary**  
jannistpl/egui‑file‑dialog is a Rust library that adds a full‑featured, highly customizable file‑selection dialog to applications built with the egui immediate‑mode GUI framework. With 162 GitHub stars and recent activity (last updated 2026‑06‑26), it lets developers ship user‑facing interfaces faster by reusing a ready‑made component instead of crafting their own file picker from scratch.  

**Value**  
The crate eliminates the need for bespoke UI work around file handling, reducing development time and UI inconsistencies across projects that already use egui. Its configurability (filters, multi‑selection, custom styling) makes it suitable for a wide range of desktop and web‑based front‑ends, helping teams deliver polished product UIs more quickly and with fewer bugs.  

**Practical adoption path**  
1. **Add the dependency** – include `egui-file-dialog` in your `Cargo.toml`.  
2. **Prototype** – instantiate the dialog in a sandbox egui app to confirm the API matches your workflow (e.g., filter syntax, async handling).  
3. **Integrate** – replace any ad‑hoc file‑picker code with the library’s `FileDialog::new(...).show(&mut ui)` calls, adjusting styling via the provided builder methods.  
4. **Validate** – run the full test suite of your application to ensure the dialog’s event handling plays nicely with your existing egui state management.  

**Production readiness**  
The project sits at a **medium** readiness level: it is stable enough for prototypes, internal tools, or non‑mission‑critical features, but the integration path is not fully documented, and metadata provides limited guidance on version compatibility or build scripts. Before committing to production, perform a small‑scale integration test, verify that the crate’s dependencies (egui version, optional features) align with your stack, and assess maintenance risk (e.g., activity frequency, open issues). With those checks in place, the library can be safely promoted to production for most frontend workloads.

### Русский

**jannistpl/egui-file-dialog** — это полнофункциональный и настраиваемый файловый диалог для библиотеки egui, позволяющий быстро добавить пользовательский интерфейс без написания собственного UI‑кода. Его обычно внедряют в прототипы или внутренние инструменты, где требуется быстрое построение UI‑компонентов, а затем, после проверки зависимостей и тестов, могут использовать в продуктивных приложениях среднего уровня готовности. Несмотря на хорошие метрики (162 ★, 29 forks, активные обновления), путь интеграции не полностью документирован, поэтому перед переходом в продакшн рекомендуется провести ручную проверку и оценить затраты на настройку.

### 中文

**项目价值**  
`jannistpl/egui-file-dialog` 为 Rust 的 GUI 框架 **egui** 提供了功能完整、可高度定制的文件选择对话框。使用它可以直接复用成熟的文件浏览 UI，省去自行实现文件树、过滤、预览等繁琐工作，从而加速产品界面开发、提升前端交付效率。

**典型接入方式**  
1. **添加依赖**：在 `Cargo.toml` 中加入  
   ```toml
   egui-file-dialog = { git = "https://github.com/jannistpl/egui-file-dialog.git" }
   ```  
   （或使用 crates.io 上的发布版本）。  
2. **在 egui 应用中创建对话框**：在 `egui::CentralPanel` 或自定义窗口的 `ui` 回调里实例化 `FileDialog::new()`，配置过滤、起始路径、回调等参数后调用 `show(&mut ctx)`。  
3. **处理返回**：对话框关闭后会返回 `Option<PathBuf>`，业务代码根据返回值执行打开、保存或错误处理。  
4. **可选自定义**：利用提供的主题、图标、列宽等属性，配合 egui 的样式系统进一步美化 UI，满足品牌或交互需求。

**生产可用性评估**  
- **成熟度**：项目已有 162 ⭐、29 🍴，最近一次提交在 2026‑06‑26，活跃度尚可。  
- **适用场景**：非常适合原型、内部工具或对 UI 完整度要求不极端的产品界面；对需要快速交付且不想自行实现文件浏览的团队尤为有价值。  
- **风险与准备**：  
  - 元数据中缺少详细的集成指南，首次接入时需要手动阅读源码或示例代码确认 API 用法。  
  - 依赖于 egui 的版本兼容性，建议在引入前确认项目的 egui 版本与库的 `Cargo.toml` 中声明的范围一致。  
  - 生产环境使用前应进行一次完整的功能回归（打开/保存、过滤、错误处理等），并评估维护成本（如后续 egui 升级是否需要同步更新）。  

**结论**：在对文件对话框有基本需求且希望快速交付的 Rust/egui 项目中，`egui-file-dialog` 是一个“中等成熟度、可直接使用”的组件。只要在正式上线前进行一次集成验证和兼容性检查，即可在生产环境中安全使用。

## 🧭 Practical evaluation

**Value:** jannistpl/egui-file-dialog helps ship user-facing interfaces with less custom UI work.

**Best use cases**

- build product UI faster
- reuse interface components
- improve frontend delivery

**Integration notes:** Needs manual inspection before adoption because integration signals are sparse in the discovered metadata.

**Production readiness:** Medium: useful for prototypes or internal workflows, with dependency and maintenance checks before production.

**Quality signals**

- 162 GitHub stars
- 29 forks
- updated 2026-06-26
- primary language: Rust

**Risks:** Integration path is not obvious from metadata; validate setup cost before committing.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 37/100 |
| stars | 47/100 |
| topics | 0/100 |
| outlook | 43/100 |
| quality | 45/100 |
| recency | 40/100 |
| adoption | 44/100 |
| production | 47/100 |
| usefulness | 42/100 |
| integration | 30/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 0/100 |

---

<sub>🔭 Discovered 2026-06-26 · [View on GitHub](https://github.com/jannistpl/egui-file-dialog) · [← Back to Misc](./README.md)</sub>
