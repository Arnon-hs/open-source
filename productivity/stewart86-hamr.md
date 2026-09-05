# Stewart86/hamr

[![Stars](https://img.shields.io/github/stars/Stewart86/hamr?style=flat-square&color=yellow)](https://github.com/Stewart86/hamr/stargazers) [![Forks](https://img.shields.io/github/forks/Stewart86/hamr?style=flat-square&color=blue)](https://github.com/Stewart86/hamr/network) [![Language](https://img.shields.io/badge/lang-Rust-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-56%2F100-brightgreen?style=flat-square)](#)

> Hamr is an extensible launcher for Wayland built with rust and gtk layer shell. Extend it with plugins that can be written in any languages.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 336 |
| 🍴 **Forks** | 6 |
| 💻 **Language** | Rust |
| 📈 **Score** | 56/100 |
| 🗓️ **Last push** | 2026-09-05 |
| 🔍 **Source** | github |

## 🏷️ Topics

`gui` `hyprland` `kde` `launcher` `niri` `rust` `sway` `wayland-compositor`

## 🎯 Categories

Productivity

## 📝 Summary

### English

**Brief summary**  
Hamr is an extensible Wayland launcher written in Rust that uses GTK‑Layer‑Shell to render its UI. Its plugin architecture lets developers add functionality in any language, making it easy to assemble custom user‑facing interfaces without building a UI from scratch.  

**Value proposition**  
- **Accelerated UI delivery** – By reusing Hamr’s core launcher and its ready‑made components, teams can focus on business logic rather than low‑level graphics or window‑management code.  
- **Language‑agnostic extensibility** – Plugins can be written in the language that best fits the team (Rust, Python, JavaScript, etc.), enabling gradual migration and reuse of existing libraries.  
- **Consistent Wayland experience** – Leveraging GTK‑Layer‑Shell guarantees proper integration with Wayland compositors, reducing platform‑specific bugs.

**Practical adoption path**  
1. **Prototype** – Clone the repo, run the provided CLI to launch the base UI, and add a simple “Hello‑World” plugin in the preferred language to validate the integration model.  
2. **Component library** – Package frequently used UI pieces (menus, dialogs, notifications) as reusable plugins and publish them in an internal registry.  
3. **CI/CD integration** – Add Hamr as a build artifact in your pipeline, run its test suite, and automate plugin packaging so that new features can be shipped by updating the plugin bundle rather than the core launcher.  
4. **Production rollout** – Deploy the compiled launcher binary alongside the vetted plugin set on target workstations or containers; use the exposed API/SDK to monitor signals and perform graceful updates.

**Production readiness**  
- **Maturity** – With ~336 GitHub stars, recent updates (as of 2026‑05‑12), and a small but active codebase in Rust, Hamr is stable enough for internal tools and prototypes.  
- **Risk considerations** – The project lacks a formal security audit and the long‑term maintainer commitment is unclear; a review of the license (likely MIT/Apache) and a dependency scan is recommended before wide‑scale deployment.  
- **Readiness level** – Medium: suitable for internal workflows, proof‑of‑concepts, and controlled production environments after a brief vetting phase (dependency checks, test coverage, and a fallback UI strategy).

### Русский

Stewart86/hamr — это расширяемый лаунчер для Wayland, написанный на Rust с использованием GTK Layer Shell, который позволяет быстро собрать пользовательский интерфейс, подключая плагины на любом языке. Он удобен для прототипирования и внутренних фронтенд‑процессов, где требуется повторное использование UI‑компонентов и ускорение доставки продукта, однако перед выводом в продакшн стоит проверить лицензирование, безопасность и наличие активных мейнтейнеров. В текущем состоянии проект имеет среднюю готовность к production: достаточно стабилен для тестовых и внутренних решений, но требует дополнительного аудита перед масштабным использованием.

### 中文

**项目简介**  
Hamr 是基于 Rust 与 GTK Layer‑Shell 构建的可扩展 Wayland 启动器，提供插件机制，插件可以用任意语言实现，从而快速组装和定制用户界面。

**价值**  
- **降低前端开发成本**：通过复用 Hamr 提供的 UI 组件和启动器框架，业务方无需从零编写 Wayland UI，即可交付可用的用户界面。  
- **加速产品迭代**：插件化设计让不同团队可以并行开发功能模块，快速验证原型并在内部工作流中使用。  
- **跨语言生态**：插件不局限于 Rust，任何能够生成共享库或通过 IPC 与 Hamr 通信的语言都能加入，方便已有代码资产的迁移与复用。

**典型接入方式**  
1. **依赖引入**：在项目的 `Cargo.toml` 中添加 `hamr` 作为库依赖，或直接克隆仓库编译。  
2. **插件注册**：实现符合 Hamr 插件约定的入口函数（如 `hamr_plugin_entry`），编译为共享库或提供 CLI，放置在 Hamr 配置的插件目录下。  
3. **信号/API 对接**：通过 Hamr 暴露的实现信号（API/SDK/CLI）与主程序交互，利用其语言元数据获取插件能力描述，实现动态加载与运行时配置。  

**生产可用性**  
- **成熟度**：目前在 GitHub 上拥有 336 ★、6 fork，最近一次更新于 2026‑05‑12，代码基于 Rust，具备较好的安全性和性能。  
- **适用场景**：适合内部原型、工具链或面向特定硬件的前端交付；在进入生产环境前建议完成依赖审计、插件安全评估以及维护者活跃度确认。  
- **风险**：需进一步核实许可证兼容性、长期维护者承诺以及潜在的安全漏洞。总体而言，经过上述检查后可在内部或受控生产环境中安全使用。

## 🧭 Practical evaluation

**Value:** Stewart86/hamr helps ship user-facing interfaces with less custom UI work.

**Best use cases**

- build product UI faster
- reuse interface components
- improve frontend delivery

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** Medium: useful for prototypes or internal workflows, with dependency and maintenance checks before production.

**Quality signals**

- 336 GitHub stars
- 6 forks
- updated 2026-05-12
- primary language: Rust
- 8 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 21/100 |
| stars | 54/100 |
| topics | 100/100 |
| outlook | 68/100 |
| quality | 70/100 |
| recency | 80/100 |
| adoption | 45/100 |
| production | 68/100 |
| usefulness | 42/100 |
| integration | 46/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 100/100 |

---

<sub>🔭 Discovered 2026-05-12 · [View on GitHub](https://github.com/Stewart86/hamr) · [← Back to Productivity](./README.md)</sub>
