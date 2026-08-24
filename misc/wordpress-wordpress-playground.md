# WordPress/wordpress-playground

[![Stars](https://img.shields.io/github/stars/WordPress/wordpress-playground?style=flat-square&color=yellow)](https://github.com/WordPress/wordpress-playground/stargazers) [![Forks](https://img.shields.io/github/forks/WordPress/wordpress-playground?style=flat-square&color=blue)](https://github.com/WordPress/wordpress-playground/network) [![Language](https://img.shields.io/badge/lang-JavaScript-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-50%2F100-brightgreen?style=flat-square)](#)

> Run WordPress in the browser via WebAssembly PHP

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 2k |
| 🍴 **Forks** | 439 |
| 💻 **Language** | JavaScript |
| 📈 **Score** | 50/100 |
| 🗓️ **Last push** | 2026-08-24 |
| 🔍 **Source** | github |

## 🏷️ Topics

`emscripten` `wasm` `webassembly` `wordpress`

## 🎯 Categories

Misc

## 📝 Summary

### English

**Summary**  
WordPress Playground lets developers run a full WordPress site directly in the browser using WebAssembly‑compiled PHP, enabling fast, sandboxed prototyping without any local server setup. With ~2 k stars and recent activity, it is a mature demo‑oriented project that can be integrated into tooling or documentation workflows after a small proof‑of‑concept test.

**Value**  
- **Instant environment** – spin up a WordPress instance in seconds, perfect for demos, tutorials, UI testing, or evaluating plugins/themes without installing PHP/MySQL locally.  
- **Zero‑install sandbox** – the whole stack runs client‑side, eliminating dependency conflicts and security concerns for external users.  
- **Extensible** – the JavaScript API allows you to preload plugins, themes, or content, making it useful for CI pipelines, onboarding scripts, or interactive docs.

**Practical adoption path**  
1. **Read the README** and run the provided `npm run start` example to confirm the Playground boots in your dev machine.  
2. **Create a minimal proof‑of‑concept** that loads a custom plugin or theme you care about; verify that you can interact with the WP admin UI and that the required assets are reachable.  
3. **Wrap the Playground launch** in a small npm script or Docker container if you need a reproducible CI step, and expose the generated URL to your team.  
4. **Iterate** by adding more plugins, configuring wp-config settings, or integrating with your existing build pipeline.

**Production readiness**  
- **Maturity:** 1956 stars, active maintenance (last commit 2026‑06‑24) and a solid JavaScript codebase indicate a stable core.  
- **Risk level:** Medium – suitable for prototypes, internal tools, documentation, or CI validation, but not yet a drop‑in replacement for a full‑scale production WordPress deployment.  
- **Considerations before production:** evaluate the size of the WASM payload, test long‑running workloads, verify compatibility with any custom PHP extensions you rely on, and set up monitoring for the client‑side resource usage. Once these checks pass, the Playground can be safely used in internal workflows or as a front‑end for low‑traffic, sandboxed WordPress instances.

### Русский

**WordPress/wordpress‑playground** — это open‑source‑проект, позволяющий запускать полную среду WordPress прямо в браузере с помощью WebAssembly‑PHP, что упрощает быстрые прототипы, обучение и демонстрацию без локальной установки. Типичный сценарий — небольшое proof‑of‑concept или внутренний воркфлоу, где требуется быстро проверить плагины, темы или API, интегрировав Playground через README‑описанные примеры. Готовность к production — средняя: проект активно поддерживается (обновления, 2 к+ звёзд), но требует проверки зависимостей и оценки затрат на настройку перед использованием в продакшене.

### 中文

**项目简介**  
WordPress/wordpress‑playground 是一个基于 WebAssembly 的 PHP 运行时，让 WordPress 完全在浏览器中启动、编辑和调试，无需本地服务器或 Docker 环境。

**价值**  
- **即时体验**：开发者、培训师或客户可以直接在网页上打开完整的 WordPress 实例，快速演示主题、插件或 API 用例。  
- **零环境依赖**：省去本地 PHP、MySQL、Web 服务器的安装与配置，降低新手上手门槛和 CI 环境的维护成本。  
- **安全沙箱**：所有代码运行在浏览器的 WASM 沙箱中，天然隔离，适合作为公开的交互式文档或代码实验平台。

**典型接入方式**  
1. **直接嵌入**：在自己的前端页面中通过 `<script src="https://cdn.jsdelivr.net/npm/@wordpress/playground@latest"></script>` 加载库，并使用 `window.wpPlayground` 提供的 API（`loadWordPress`, `runPHP`, `installPlugin` 等）启动实例。  
2. **自定义镜像**：利用项目提供的 `playground-php` Docker 镜像或 `wp-playground` NPM 包，预装特定主题/插件，然后通过 `playground-loader` 将打包好的文件上传至 CDN，页面加载时自动恢复。  
3. **CI / 测试**：在 GitHub Actions 中运行 `npm run playground:start`，对插件的单元测试或回归测试进行 headless 执行（配合 `playwright`），实现“在浏览器中跑单元测试”的工作流。

**生产可用性**  
- **成熟度**：已有 1.9k+ 星、439 个 fork，活跃维护至 2026‑06‑24，核心代码主要是 JavaScript 与 WASM，社区贡献较活跃。  
- **适用场景**：原型开发、内部培训、交互式文档、插件演示以及 CI 中的轻量化功能测试。  
- **限制**：  
  - 仍依赖浏览器的内存和 CPU，处理大规模数据或高并发请求时性能受限。  
  - 持久化只能通过 IndexedDB 或外部 API 实现，生产环境需要自行设计备份/同步方案。  
  - 与传统 WordPress 部署的插件/主题兼容性需逐个验证，部分依赖系统扩展的代码可能无法在 WASM 环境运行。  
- **建议**：在正式生产前，先做一个小范围的 PoC，确认所需插件、主题以及自定义 PHP 扩展能够在 WASM 中正常工作；同时制定监控与回滚策略，避免因浏览器更新导致的兼容性问题。  

总体而言，WordPress/wordpress‑playground 适合作为 **原型/内部工具** 的快速搭建方案，经过适当的验证与补充后，可在受控的生产场景（如内部培训平台、演示站点）中安全使用。

## 🧭 Practical evaluation

**Value:** WordPress/wordpress-playground may be useful when its README and activity match a concrete workflow.

**Best use cases**

- Not enough metadata yet.

**Integration notes:** Looks feasible to evaluate, but integration should start with a small proof of concept and README check.

**Production readiness:** Medium: useful for prototypes or internal workflows, with dependency and maintenance checks before production.

**Quality signals**

- 1956 GitHub stars
- 439 forks
- updated 2026-06-24
- primary language: JavaScript
- 4 topics

**Risks:** Integration path is not obvious from metadata; validate setup cost before committing.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 66/100 |
| stars | 70/100 |
| topics | 50/100 |
| outlook | 55/100 |
| quality | 64/100 |
| recency | 40/100 |
| adoption | 69/100 |
| production | 54/100 |
| usefulness | 42/100 |
| integration | 30/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 0/100 |

---

<sub>🔭 Discovered 2026-06-24 · [View on GitHub](https://github.com/WordPress/wordpress-playground) · [← Back to Misc](./README.md)</sub>
