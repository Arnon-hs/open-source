# picoe/Eto

[![Stars](https://img.shields.io/github/stars/picoe/Eto?style=flat-square&color=yellow)](https://github.com/picoe/Eto/stargazers) [![Forks](https://img.shields.io/github/forks/picoe/Eto?style=flat-square&color=blue)](https://github.com/picoe/Eto/network) [![Language](https://img.shields.io/badge/lang-C%23-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-52%2F100-brightgreen?style=flat-square)](#)

> Cross platform GUI framework for desktop and mobile applications in .NET

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 3.9k |
| 🍴 **Forks** | 344 |
| 💻 **Language** | C# |
| 📈 **Score** | 52/100 |
| 🗓️ **Last push** | 2026-08-24 |
| 🔍 **Source** | github |

## 🏷️ Topics

_no topics_

## 🎯 Categories

Misc

## 📝 Summary

### English

**Project Summary:**
picoe/Eto is an open-source, cross-platform GUI framework for building desktop and mobile applications in .NET, allowing developers to create user-facing interfaces with less custom UI work. This framework enables faster product UI development, reusability of interface components, and improved frontend delivery. With its medium production readiness, picoe/Eto is suitable for prototypes or internal workflows, but requires manual inspection and dependency checks before production.

**Value Proposition:**
The primary value of picoe/Eto lies in its ability to streamline the development process by reducing the amount of custom UI work required. This is achieved through its reusable interface components, which can be easily integrated into applications, saving time and resources.

**Practical Adoption Path:**
To adopt picoe/Eto, developers should first manually inspect the integration signals to ensure a smooth transition. This involves validating the setup cost and dependencies before committing to the framework. Once the integration path is clear, developers can start building their applications using picoe/Eto's cross-platform capabilities.

**Production Readiness:**
picoe/Eto has a medium production readiness score, indicating that it is suitable for prototypes or internal workflows. While it has a significant user base (3944 GitHub stars) and is actively maintained,

### Русский

Резюме проекта picoe/Eto:

Представляем picoe/Eto - кроссплатформенное фреймворк GUI для создания десктопных и мобильных приложений на .NET. Это мощный инструмент, позволяющий сократить объем ручной работы по созданию пользовательских интерфейсов и ускорить процесс разработки. picoe/Eto подходит для внутренних прототипов или рабочих процессов, но требует тщательного проверки и оценки перед выпуском в производство.

### 中文

**项目价值**  
picoe/Eto 是基于 .NET 的跨平台 GUI 框架，能够一次编写代码即可在 Windows、macOS、Linux 以及移动端（iOS、Android）上生成原生界面。它提供了丰富的控件抽象和统一的布局系统，帮助开发者大幅减少手写 UI 的工作量，实现界面组件的复用，从而加速产品 UI 的交付。

**典型接入方式**  
1. **引用 NuGet 包**：在 .NET 项目（.NET 6/7/8）中通过 `dotnet add package Eto.Forms` 添加依赖。  
2. **创建 Eto 应用入口**：在 `Program.cs` 中调用 `Eto.Forms.Application` 并指定平台实现（如 `Eto.WinForms`, `Eto.Mac`, `Eto.GtkSharp`, `Eto.Xamarin.Android`, `Eto.Xamarin.iOS`）。  
3. **编写跨平台 UI**：使用 Eto 的控件（`Button`, `Label`, `GridView` 等）和布局（`DynamicLayout`, `StackLayout`）编写一次代码，框架会在运行时映射到对应平台的原生控件。  
4. **平台特定定制**：如有必要，可通过 `#if` 条件编译或 `Platform.Is*` 检查，在特定平台上加入微调代码。  
5. **构建与发布**：使用 .NET 的多目标项目（`<TargetFrameworks>net6.0-windows;net6.0-macos;net6.0-android;net6.0-ios</TargetFrameworks>`）一次构建即可生成各平台的可执行文件或 App 包。

**生产可用性**  
- **成熟度**：GitHub ★3944、Fork ★344，最近一次提交于 2026‑07‑06，活跃度良好。  
- **适用场景**：非常适合内部工具、原型系统以及对 UI 响应速度要求不极端的面向用户的桌面/移动应用。  
- **风险与注意事项**：  
  - 项目元数据中缺乏完整的集成指南，建议在正式采用前进行一次手动评估，确认依赖（如 Gtk、Xamarin、WinForms）在目标环境中的可用性。  
  - 对于高并发、严格性能或高度自定义的 UI（如复杂动画、游戏级渲染），可能需要额外的原生实现或替代方案。  
- **推荐使用策略**：先在小型内部项目或原型中验证集成成本和维护成本；若满足功能与性能需求，再逐步推广到生产环境，并配合持续的依赖安全审计（NuGet 包版本更新、平台 SDK 兼容性检查）。  

综上，Eto 为 .NET 开发者提供了一条“一次编写、跨平台运行”的 UI 解决方案，适合希望快速交付桌面/移动前端的团队，但在正式上线前应进行充分的集成验证和维护评估。

## 🧭 Practical evaluation

**Value:** picoe/Eto helps ship user-facing interfaces with less custom UI work.

**Best use cases**

- build product UI faster
- reuse interface components
- improve frontend delivery

**Integration notes:** Needs manual inspection before adoption because integration signals are sparse in the discovered metadata.

**Production readiness:** Medium: useful for prototypes or internal workflows, with dependency and maintenance checks before production.

**Quality signals**

- 3944 GitHub stars
- 344 forks
- updated 2026-07-06
- primary language: C#

**Risks:** Integration path is not obvious from metadata; validate setup cost before committing.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 63/100 |
| stars | 77/100 |
| topics | 0/100 |
| outlook | 54/100 |
| quality | 58/100 |
| recency | 40/100 |
| adoption | 73/100 |
| production | 52/100 |
| usefulness | 58/100 |
| integration | 30/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 0/100 |

---

<sub>🔭 Discovered 2026-07-06 · [View on GitHub](https://github.com/picoe/Eto) · [← Back to Misc](./README.md)</sub>
