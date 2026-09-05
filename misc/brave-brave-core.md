# brave/brave-core

[![Stars](https://img.shields.io/github/stars/brave/brave-core?style=flat-square&color=yellow)](https://github.com/brave/brave-core/stargazers) [![Forks](https://img.shields.io/github/forks/brave/brave-core?style=flat-square&color=blue)](https://github.com/brave/brave-core/network) [![Language](https://img.shields.io/badge/lang-C%2B%2B-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-55%2F100-brightgreen?style=flat-square)](#)

> Core engine for the Brave browser for mobile and desktop. For issues https://github.com/brave/brave-browser/issues

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 3.2k |
| 🍴 **Forks** | 1.2k |
| 💻 **Language** | C++ |
| 📈 **Score** | 55/100 |
| 🗓️ **Last push** | 2026-09-05 |
| 🔍 **Source** | github |

## 🏷️ Topics

_no topics_

## 🎯 Categories

Misc

## 📝 Summary

### English

**Brief Summary**  
brave/brave‑core is the C++‑based engine that powers the Brave web browser on both mobile and desktop platforms. It provides the rendering, networking, and privacy‑focused subsystems that Brave’s UI layer builds on, and is actively maintained (last update 2026‑05‑12) with a sizable community (≈3.2 k stars, 1.2 k forks).

**Value**  
For teams that need a high‑performance, privacy‑oriented web engine without starting from Chromium’s full source tree, brave‑core offers a modular core that can be embedded in custom browsers, hybrid apps, or security‑research tools. Its focus on ad‑blocking, fingerprint‑resistance, and built‑in Tor integration can accelerate development of privacy‑first products.

**Practical Adoption Path**  
1. **Assess Compatibility** – Clone the repository and review the `README.md` and build scripts to understand required dependencies (C++, Ninja, GN, and platform‑specific SDKs).  
2. **Prototype Integration** – Build the core library for your target platform (Linux, macOS, Windows, Android, iOS) using the provided GN args, then link it to a minimal UI shell or existing Chromium‑based UI layer.  
3. **Validate Features** – Run Brave’s test suite and a few real‑world browsing scenarios to confirm that ad‑blocking, HTTPS‑upgrades, and Tor support behave as expected.  
4. **Customize & Harden** – Strip or replace components you don’t need, add your own UI, and audit the code for security and licensing compliance before committing to a longer‑term fork.

**Production Readiness**  
The project is at a **medium** readiness level: it is actively maintained and stable enough for prototypes or internal tools, but the integration surface is not fully documented, and the build process can be complex. Before using brave‑core in production, teams should perform a thorough dependency audit, set up automated builds for their target platforms, and allocate resources for ongoing maintenance and security updates.

### Русский

**Краткое резюме:**  
`brave/brave-core` — это ядро браузера Brave, написанное на C++ и поддерживаемое как для мобильных, так и для настольных платформ. При совпадении требований проекта (например, необходимость собственного движка рендеринга, интеграции рекламных блокировок или кастомных протоколов) репозиторий может стать базой для прототипов или внутренних инструментов, однако перед внедрением требуется ручная проверка сборки и зависимостей, так как в метаданных мало информации о процессе интеграции. Готовность к production — средняя: проект стабилен и активно обновляется (последний коммит 2026‑05‑12), но требует дополнительной валидации и настройки перед использованием в продакшене.

### 中文

**项目简介**  
brave/brave‑core 是 Brave 浏览器在移动端和桌面端使用的核心渲染与网络引擎，基于 C++ 实现并持续维护。它提供了 Chromium‑based 的底层功能，同时加入了 Brave 的隐私保护与广告拦截特性。

**价值**  
- **隐私安全**：内置跟踪防护、广告拦截和安全 DNS，适合需要强隐私的产品。  
- **跨平台**：同一套核心代码可在 Android、iOS、Windows、macOS、Linux 上复用，降低多端开发成本。  
- **活跃社区**：超过 3200 星、1200+ Fork，更新频繁，能够获得社区的 bug 修复和功能改进。

**典型接入方式**  
1. **源码编译**：克隆 `brave/brave-core`，按照官方文档的依赖列表（CMake、Ninja、LLVM 等）编译出 `libbrave_core.so`（或对应平台的库）。  
2. **嵌入到自研浏览器**：在自家 UI 层（Electron、Qt、React Native 等）中加载该库，使用其提供的 `BraveEngine` 接口进行页面加载、网络请求和 UI 渲染。  
3. **功能开关**：通过配置文件或运行时参数打开/关闭 Brave 特有的隐私模块（如 Tracker Blocking、HTTPS‑Only Mode），便于在不同业务场景下灵活定制。  
4. **CI/CD 集成**：将编译产物打包进内部镜像或 SDK，配合自动化测试确保升级不会引入回归。

**生产可用性**  
- **成熟度**：核心代码已在 Brave 浏览器的正式版中大规模使用，稳定性较高。  
- **适配成本**：由于缺少统一的包装层，接入时需要自行处理依赖、构建脚本以及与 UI 框架的对接，建议先在原型或内部测试环境验证。  
- **维护要求**：需定期同步 upstream 更新（包括安全补丁和 Chromium 版本升级），并监控库的二进制兼容性。  

总体而言，brave‑core 适合作为注重隐私的内部浏览器或嵌入式 WebView 的技术基座，具备中等到高的生产可用性，但在正式投产前应完成充分的集成测试和运维准备。

## 🧭 Practical evaluation

**Value:** brave/brave-core may be useful when its README and activity match a concrete workflow.

**Best use cases**

- Not enough metadata yet.

**Integration notes:** Needs manual inspection before adoption because integration signals are sparse in the discovered metadata.

**Production readiness:** Medium: useful for prototypes or internal workflows, with dependency and maintenance checks before production.

**Quality signals**

- 3231 GitHub stars
- 1235 forks
- updated 2026-05-12
- primary language: C++

**Risks:** Integration path is not obvious from metadata; validate setup cost before committing.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 77/100 |
| stars | 75/100 |
| topics | 0/100 |
| outlook | 65/100 |
| quality | 69/100 |
| recency | 80/100 |
| adoption | 75/100 |
| production | 65/100 |
| usefulness | 42/100 |
| integration | 30/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 0/100 |

---

<sub>🔭 Discovered 2026-05-12 · [View on GitHub](https://github.com/brave/brave-core) · [← Back to Misc](./README.md)</sub>
