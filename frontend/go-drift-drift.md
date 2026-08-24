# go-drift/drift

[![Stars](https://img.shields.io/github/stars/go-drift/drift?style=flat-square&color=yellow)](https://github.com/go-drift/drift/stargazers) [![Forks](https://img.shields.io/github/forks/go-drift/drift?style=flat-square&color=blue)](https://github.com/go-drift/drift/network) [![Language](https://img.shields.io/badge/lang-Go-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-51%2F100-brightgreen?style=flat-square)](#)

> Cross-platform mobile UI framework for Go

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 309 |
| 🍴 **Forks** | 5 |
| 💻 **Language** | Go |
| 📈 **Score** | 51/100 |
| 🗓️ **Last push** | 2026-08-24 |
| 🔍 **Source** | github |

## 🏷️ Topics

`android` `go` `golang` `ios` `mobile` `mobile-app` `skia` `ui`

## 🎯 Categories

Frontend · Mobile

## 📝 Summary

### English

**Brief Summary (2‑3 sentences)**  
go‑drift/drift is a cross‑platform mobile UI framework written in Go that lets developers build user‑facing interfaces with far less hand‑crafted UI code. By providing reusable components and a Go‑centric API, it speeds up the creation of product UIs and simplifies frontend delivery for teams already using Go on the backend.

**Value**  
- **Accelerated UI development** – Developers can write UI logic in Go, reusing existing Go libraries and avoiding context‑switching to JavaScript, Swift, or Kotlin.  
- **Component reuse** – A library of pre‑built widgets and layout primitives lets teams share UI building blocks across iOS, Android, and desktop builds.  
- **Consistent stack** – Keeping both backend and frontend in the same language reduces cognitive load, onboarding time, and the need for separate UI specialists.

**Practical Adoption Path**  
1. **Proof‑of‑concept** – Clone the repo, run the example app, and verify that the build pipeline (Go 1.22+, gomobile) works on your target platforms.  
2. **Component pilot** – Port a low‑risk internal screen (e.g., a settings page) to Drift, using the README and sample code as a guide.  
3. **Integration checklist** – Review the license, run `go mod tidy`, and scan the dependency tree for known vulnerabilities.  
4. **Iterate & expand** – Gradually replace existing native screens, documenting any platform‑specific quirks and adding missing widgets to the library.

**Production Readiness**  
- **Maturity** – Medium; the project is actively maintained (last update 2026‑05‑11) and has modest community traction (≈ 300 stars).  
- **Fit for production** – Suitable for prototypes, internal tools, or customer‑facing apps where rapid UI delivery outweighs the need for a battle‑tested UI framework. Before full production rollout, perform a security audit, confirm long‑term maintainership, and establish a version‑pinning strategy for its dependencies.

### Русский

**go-drift/drift** — кросс‑платформенный UI‑фреймворк для Go, позволяющий быстро собрать пользовательский интерфейс, переиспользуя готовые компоненты и экономя время на кастомной верстке. Для начала рекомендуется реализовать небольшой proof‑of‑concept, проверив README и базовую сборку, после чего оценить зависимости и стабильность перед выводом в продакшн. Текущий уровень готовности — средний: фреймворк подходит для прототипов и внутренних инструментов, но требует дополнительного аудита лицензий, безопасности и поддержки мейнтейнеров.

### 中文

**项目简介**  
go-drift/drift 是一套基于 Go 语言的跨平台移动 UI 框架，旨在帮助开发者以最少的自定义 UI 工作快速交付面向用户的界面。它提供可复用的组件库和统一的渲染抽象，让前端交付更高效、代码更易维护。

**价值**  
- **加速 UI 开发**：通过现成的组件和统一的布局系统，显著缩短产品 UI 的实现周期。  
- **代码复用**：同一套 Go 代码可在 iOS、Android 甚至桌面平台上运行，降低跨平台维护成本。  
- **提升前端交付效率**：后端开发者可直接使用 Go 编写 UI，减少前后端协作的沟通成本。

**典型接入方式**  
1. **阅读 README**，确认环境要求（Go 1.22+、对应平台的 SDK）。  
2. **创建一个小型 PoC**：在 `main.go` 中引入 `github.com/go-drift/drift`，实现一个简单的页面或按钮，验证编译、运行和 UI 渲染是否正常。  
3. **逐步迁移**：在已有的 Go 项目中逐步替换或包装原有的 UI 逻辑，复用 drift 提供的组件库。  
4. **CI/CD 集成**：将跨平台构建（如 `go build -target=android`）加入流水线，确保每次提交都能成功编译并通过基本 UI 测试。

**生产可用性**  
- **成熟度**：当前评分 63/100，GitHub 具备 300+ 星、近期活跃更新，适合作为原型或内部工具的 UI 层。  
- **风险**：仍需完成许可证合规、依赖安全审计以及维护者活跃度的最终评估。  
- **建议**：在正式生产环境使用前，进行一次完整的安全与依赖审计，并在关键业务模块中进行长时间的稳定性验证；若满足上述条件，可视为中等风险、可投入生产的方案。

## 🧭 Practical evaluation

**Value:** go-drift/drift helps ship user-facing interfaces with less custom UI work.

**Best use cases**

- build product UI faster
- reuse interface components
- improve frontend delivery

**Integration notes:** Looks feasible to evaluate, but integration should start with a small proof of concept and README check.

**Production readiness:** Medium: useful for prototypes or internal workflows, with dependency and maintenance checks before production.

**Quality signals**

- 309 GitHub stars
- 5 forks
- updated 2026-05-11
- primary language: Go
- 8 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 19/100 |
| stars | 53/100 |
| topics | 100/100 |
| outlook | 50/100 |
| quality | 55/100 |
| recency | 20/100 |
| adoption | 44/100 |
| production | 48/100 |
| usefulness | 58/100 |
| integration | 46/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 200/100 |

---

<sub>🔭 Discovered 2026-05-11 · [View on GitHub](https://github.com/go-drift/drift) · [← Back to Frontend](./README.md)</sub>
