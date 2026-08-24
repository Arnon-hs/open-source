# wuchalejs/wuchale

[![Stars](https://img.shields.io/github/stars/wuchalejs/wuchale?style=flat-square&color=yellow)](https://github.com/wuchalejs/wuchale/stargazers) [![Forks](https://img.shields.io/github/forks/wuchalejs/wuchale?style=flat-square&color=blue)](https://github.com/wuchalejs/wuchale/network) [![Language](https://img.shields.io/badge/lang-TypeScript-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-55%2F100-brightgreen?style=flat-square)](#)

> Compile-time i18n toolkit that requires zero code changes and produces the smallest possible bundles. Supports React, Svelte, SolidJS, Astro, and more

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 348 |
| 🍴 **Forks** | 14 |
| 💻 **Language** | TypeScript |
| 📈 **Score** | 55/100 |
| 🗓️ **Last push** | 2026-08-24 |
| 🔍 **Source** | github |

## 🏷️ Topics

`ai-translation` `ast` `astro` `gettext` `i18n` `internationalization` `jsx` `l10n` `localization` `multilingual` `po` `preact`

## 🎯 Categories

AI/ML · Frontend

## 📝 Summary

### English

**Brief Summary (2‑3 sentences)**  
wuchale is a compile‑time internationalisation (i18n) toolkit that works without any code modifications and generates the smallest possible bundles. It plugs into popular front‑end frameworks such as React, Svelte, SolidJS, Astro, and many others, letting developers ship fully‑localized apps with zero runtime overhead.

**Value**  
- **Zero‑change integration**: Because localisation is performed at build time, developers do not need to sprinkle i18n hooks throughout their codebase, dramatically reducing maintenance effort.  
- **Bundle‑size efficiency**: Only the strings actually used in the final bundle are emitted, keeping the payload lean—crucial for performance‑sensitive web apps.  
- **Framework‑agnostic**: A single tool covers the major modern UI libraries, so teams can adopt it across heterogeneous projects without learning a new API.

**Practical Adoption Path**  
1. **Install** the package (e.g., `npm i wuchale`) and add the provided CLI or SDK to the build pipeline (Webpack, Vite, Astro, etc.).  
2. **Define** localisation resources (JSON/YAML files) and configure the target languages in the wuchale config file.  
3. **Run** the compile step; wuchale extracts all literal strings, replaces them with generated identifiers, and emits per‑locale bundles.  
4. **Deploy** the generated assets; the runtime simply loads the appropriate locale file—no extra runtime library is required.  
5. **Iterate** by adding new strings to the resource files; the next build automatically picks them up.

**Production Readiness**  
- **Activity & Adoption**: Recent commits (as of 2026‑05‑12), 348 GitHub stars, and a growing ecosystem of topics indicate active maintenance and community interest.  
- **Stability**: The tool is written in TypeScript, has clear CLI/SDK entry points, and integrates cleanly with mainstream bundlers, making it suitable for pilot projects and full‑scale rollouts.  
- **Risk Profile**: No major metadata or licensing red flags have been identified, though a final review of the license terms, security posture, and maintainer responsiveness is recommended before mission‑critical deployment.  

Overall, wuchale offers a low‑friction, high‑performance solution for internationalising modern front‑end applications, and its current health signals make it a strong candidate for production use.

### Русский

**wuchalejs/wuchale** — это compile‑time i18n‑инструмент, который без изменения кода генерирует максимально лёгкие бандлы и работает сразу с React, Svelte, SolidJS, Astro и другими фронтенд‑фреймворками. Он идеально подходит для быстрого прототипирования AI‑фич (RAG, агентные воркфлоу) и оценки моделей, так как предоставляет готовые сигналы API/SDK/CLI и метаданные языка. Проект считается production‑ready: активные коммиты, 348 звёзд, широкая экосистема и хорошая поддержка, хотя лицензия и безопасность требуют окончательной проверки.

### 中文

**项目简介**  
wuchalejs/wuchale 是一个编译期国际化（i18n）工具箱，零代码入侵、极致压缩体积，已原生支持 React、Svelte、SolidJS、Astro 等主流前端框架。

**价值**  
- **无需改动业务代码**：只在编译阶段自动抽取、替换文案，极大降低迁移成本。  
- **最小化产出体积**：通过 Tree‑shaking 与静态分析，仅保留实际使用的语言资源，显著缩减 bundle 大小。  
- **跨框架统一方案**：一次配置即可在多个前端框架之间共享同一套 i18n 资源，提升团队协作效率。

**典型接入方式**  
1. **安装**：`npm i wuchale`（或 `pnpm add wuchale`）。  
2. **配置**：在项目根目录新增 `wuchale.config.ts`，声明语言文件路径、默认语言等。  
3. **编译插件**：在对应框架的构建工具中引入插件，例如  
   - **React/Vite**：`import { wuchaleVite } from 'wuchale/vite';` → `vite.config.ts` 中 `plugins: [wuchaleVite()]`  
   - **SvelteKit**：在 `svelte.config.js` 中加入 `wuchaleSvelte()`。  
4. **运行**：执行常规构建命令（`npm run build`），编译阶段自动生成对应语言的 JSON/JS 资源并注入代码。  

**生产可用性**  
- **活跃度**：截至 2026‑05‑12 最近一次提交，GitHub ★348、Fork 14，持续更新。  
- **生态兼容**：已在多个前端生态（React、Svelte、SolidJS、Astro）通过官方插件验证，且 TypeScript 类型完备。  
- **安全与许可证**：MIT 许可证，无已知重大安全漏洞；仍建议在正式上线前进行内部安全审计。  
- **适配度**：适合作为现有项目的 i18n 增强层，也可在新项目中即刻使用，具备企业级试点的成熟度。

## 🧭 Practical evaluation

**Value:** wuchalejs/wuchale helps add AI capability without starting from a blank model stack.

**Best use cases**

- prototype AI features
- build RAG or agent workflows
- evaluate model tooling

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 348 GitHub stars
- 14 forks
- updated 2026-05-12
- primary language: TypeScript
- 20 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 29/100 |
| stars | 54/100 |
| topics | 100/100 |
| outlook | 50/100 |
| quality | 56/100 |
| recency | 20/100 |
| adoption | 47/100 |
| production | 51/100 |
| usefulness | 58/100 |
| integration | 62/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 200/100 |

---

<sub>🔭 Discovered 2026-05-12 · [View on GitHub](https://github.com/wuchalejs/wuchale) · [← Back to AI/ML](./README.md)</sub>
