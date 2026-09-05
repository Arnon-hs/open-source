# bea4dev/ShojiWM

[![Stars](https://img.shields.io/github/stars/bea4dev/ShojiWM?style=flat-square&color=yellow)](https://github.com/bea4dev/ShojiWM/stargazers) [![Forks](https://img.shields.io/github/forks/bea4dev/ShojiWM?style=flat-square&color=blue)](https://github.com/bea4dev/ShojiWM/network) [![Language](https://img.shields.io/badge/lang-Rust-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-55%2F100-brightgreen?style=flat-square)](#)

> The most customizable Wayland compositor with TypeScript(tsx).

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 305 |
| 🍴 **Forks** | 12 |
| 💻 **Language** | Rust |
| 📈 **Score** | 55/100 |
| 🗓️ **Last push** | 2026-09-05 |
| 🔍 **Source** | github |

## 🏷️ Topics

`smithay` `tsx` `typescript` `wayland` `wayland-compositor`

## 🎯 Categories

Misc

## 📝 Summary

### English

**Brief Summary (2‑3 sentences)**  
ShojiWM is an open‑source Wayland compositor written in Rust that lets developers describe the compositor UI with TypeScript (tsx), offering a uniquely high level of customisation. With over 300 GitHub stars and recent activity (last commit 2026‑06‑25), it targets developers who need a programmable, extensible window‑manager for experimental or internal workflows.

**Value**  
- **Programmable UI** – By using TypeScript/tsx, UI logic can be expressed with the same tools and ecosystem that front‑end developers already know, dramatically reducing the learning curve for building custom Wayland experiences.  
- **Fine‑grained extensibility** – The Rust core provides performance and safety, while the TS layer enables rapid iteration, hot‑reloading, and integration with existing JavaScript tooling (linters, formatters, CI pipelines).  
- **Community traction** – 300+ stars and an active commit history indicate a growing user base and enough momentum to find community examples and help.

**Practical Adoption Path**  
1. **Read the README & try the demo** – Verify that the project’s documentation matches your workflow (e.g., building a compositor from a TS entry point).  
2. **Proof‑of‑concept prototype** – Fork the repo, replace the sample UI with a minimal version of your target workflow (e.g., a custom tiling layout or on‑screen keyboard).  
3. **Dependency audit** – Review the Rust crates and npm packages for licensing, security advisories, and maintenance status.  
4. **Integration tests** – Add a CI job that builds the compositor and runs a headless Wayland test suite to ensure stability across updates.  
5. **Iterate and expand** – Once the prototype works, gradually replace more of your window‑manager logic with ShojiWM components.

**Production Readiness**  
ShojiWM sits at a **medium** readiness level. It is suitable for prototypes, internal tools, or niche production environments where the benefits of a TypeScript‑driven compositor outweigh the risks. Before full production deployment, you should:

- Confirm the license (MIT/Apache‑2.0) aligns with your policy.  
- Perform a security audit of both the Rust and JavaScript dependencies.  
- Verify that the maintainers are responsive (e.g., recent pull‑request merges, issue triage).  
- Establish a fallback plan (e.g., pinning to a known good commit or forking) in case upstream activity slows.

With those checks in place, ShojiWM can be adopted incrementally, providing a highly customisable Wayland experience while keeping the development workflow familiar to modern web‑centric teams.

### Русский

ShojiWM — это высоко настраиваемый Wayland‑композитор, написанный на Rust с поддержкой TypeScript/TSX, что делает его удобным для разработки кастомных UI‑решений и быстрых прототипов. Его можно интегрировать в существующий стек, начав с небольшого proof‑of‑concept и проверки README, после чего оценить зависимости и актуальность поддержки; при положительном результате проект подходит для внутренних workflow и прототипов, но требует дополнительного аудита лицензий, безопасности и поддержки перед выводом в продакшн.

### 中文

**项目简介**  
ShojiWM（bea4dev/ShojiWM）是一款基于 Rust 的 Wayland 合成器，使用 TypeScript（tsx）实现高度可定制的窗口管理逻辑。它的插件化架构让开发者可以用熟悉的前端技术快速编写、热加载和调试 UI 组件，从而在 Wayland 环境下实现独特的桌面体验。

**价值**  
- **前端友好**：借助 TypeScript/tsx，前端团队可以直接参与桌面环境的开发，降低学习成本。  
- **高度可定制**：插件系统和配置即代码（Config‑as‑Code）使得几乎所有合成器行为都可以在运行时修改，适合需要特定工作流或实验性功能的团队。  
- **活跃社区**：已有 300+ 星、12 叉，且最近一次提交在 2026‑06‑25，表明项目仍在维护中。

**典型接入方式**  
1. **阅读 README 与示例**：确认项目的构建链（Rust + Cargo + npm/yarn）以及 TypeScript 插件入口。  
2. **创建小型 PoC**：在本地机器上克隆仓库，按照文档编译 `shoji-wm`，并编写一个最简的 tsx 窗口插件（如自定义面板或快捷键）。  
3. **集成到现有工作流**：将编译好的二进制加入启动脚本，或在容器/VM 中以 `ShojiWM` 替代默认的 Wayland 合成器，验证与现有 XWayland、GTK/Qt 应用的兼容性。  
4. **CI/CD 自动化**：利用 Cargo + npm 脚本实现持续构建和插件热更新，确保每次提交都能生成可运行的合成器镜像。

**生产可用性**  
- **成熟度**：中等（Medium）— 适合作为原型、内部工具或特定业务场景的桌面环境；在正式生产环境使用前需完成依赖审计、许可证合规检查以及安全漏洞扫描。  
- **维护成本**：项目主要语言为 Rust，插件使用 TypeScript，团队需要同时具备这两方面的技术栈；若缺乏 Rust 经验，建议引入熟悉系统编程的成员。  
- **风险**：尚未确认长期维护者的活跃度以及许可证（MIT/Apache 等）是否符合企业合规要求；建议在正式投入前与项目维护者沟通或自行 fork 进行内部维护。  

总体而言，ShojiWM 为需要高度可编程桌面环境的团队提供了一个创新且前端友好的选项，只要在引入前完成小规模验证和合规审查，即可在内部生产环境中安全使用。

## 🧭 Practical evaluation

**Value:** bea4dev/ShojiWM may be useful when its README and activity match a concrete workflow.

**Best use cases**

- Not enough metadata yet.

**Integration notes:** Looks feasible to evaluate, but integration should start with a small proof of concept and README check.

**Production readiness:** Medium: useful for prototypes or internal workflows, with dependency and maintenance checks before production.

**Quality signals**

- 305 GitHub stars
- 12 forks
- updated 2026-06-25
- primary language: Rust
- 5 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 28/100 |
| stars | 53/100 |
| topics | 63/100 |
| outlook | 64/100 |
| quality | 65/100 |
| recency | 80/100 |
| adoption | 46/100 |
| production | 66/100 |
| usefulness | 42/100 |
| integration | 46/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 0/100 |

---

<sub>🔭 Discovered 2026-06-25 · [View on GitHub](https://github.com/bea4dev/ShojiWM) · [← Back to Misc](./README.md)</sub>
