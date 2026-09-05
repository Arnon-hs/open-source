# TanStack/table

[![Stars](https://img.shields.io/github/stars/TanStack/table?style=flat-square&color=yellow)](https://github.com/TanStack/table/stargazers) [![Forks](https://img.shields.io/github/forks/TanStack/table?style=flat-square&color=blue)](https://github.com/TanStack/table/network) [![Language](https://img.shields.io/badge/lang-TypeScript-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-67%2F100-brightgreen?style=flat-square)](#)

> 🤖 Headless UI for building powerful tables & datagrids for TS/JS -  React-Table, Vue-Table, Solid-Table, Svelte-Table

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 28.2k |
| 🍴 **Forks** | 3.5k |
| 💻 **Language** | TypeScript |
| 📈 **Score** | 67/100 |
| 🗓️ **Last push** | 2026-09-05 |
| 🔍 **Source** | github |

## 🏷️ Topics

`datagrid` `datagrids` `datatable` `filtering` `grid` `grouping` `hooks` `javascript` `pagination` `react` `reactjs` `solid`

## 🎯 Categories

Frontend

## 📝 Summary

### English

**Summary**  
TanStack /table is a headless, framework‑agnostic UI library that lets you compose powerful, type‑safe tables and data‑grids in React, Vue, Solid, Svelte, or plain TypeScript/JavaScript. With over 28 k GitHub stars and a very active maintainer community, it provides the core table logic (sorting, filtering, pagination, virtualization, etc.) while leaving the visual layer completely up to you, dramatically cutting the amount of custom UI code needed for data‑intensive front‑ends.  

**Value**  
- **Accelerates UI delivery** – developers can focus on styling and business logic instead of reinventing sorting, grouping, or virtual scrolling.  
- **Reusable across frameworks** – the same core engine powers tables in multiple front‑end stacks, enabling component libraries to share a single, battle‑tested data layer.  
- **Strong TypeScript support** – compile‑time safety reduces runtime bugs and improves developer productivity.  

**Practical adoption path**  
1. **Proof‑of‑concept** – scaffold a small feature (e.g., an admin list) using the README examples; verify that the headless API integrates cleanly with your existing component library.  
2. **Component wrapper** – create a thin wrapper that applies your design system (CSS, theming, accessibility) around the TanStack core.  
3. **Gradual migration** – replace legacy table implementations incrementally, starting with low‑risk pages, and expand to more complex grids as confidence grows.  

**Production readiness**  
- **High** – recent commits (as of 2026‑07‑12), a large contributor base, and widespread adoption in commercial projects signal stability.  
- **Quality signals** – 28 k stars, 3.5 k forks, active issue triage, and a well‑documented API.  
- **Remaining checks** – perform a final review of the MIT license, run a security audit of transitive dependencies, and confirm that the core maintainers are still responsive before committing to a full‑scale rollout.

### Русский

**TanStack/table** — это headless‑библиотека на TypeScript, позволяющая быстро создавать мощные таблицы и датагриды в React, Vue, Solid и Svelte без написания собственного UI‑кода. Для внедрения рекомендуется начать с небольшого proof‑of‑concept, следуя README, чтобы оценить интеграцию и адаптировать стили под ваш дизайн‑систем. Проект имеет высокий уровень готовности к production: активные коммиты, более 28 тыс. звёзд на GitHub, широкое распространение и зрелую экосистему, хотя финальную проверку лицензии и безопасности следует провести.

### 中文

**项目简介（2‑3 句话）**  
TanStack /table 是一个 **headless** 表格/数据网格库，提供框架无关的核心逻辑，支持 React、Vue、Solid、Svelte 等前端框架。它通过纯 TypeScript 实现强大的排序、过滤、分页、分组等功能，让开发者只需专注 UI 样式即可快速构建高性能的数据表格。

**价值**  
- **降低 UI 开发成本**：表格的交互、状态管理、数据处理等复杂逻辑已封装好，前端只需编写展示层，显著缩短产品 UI 开发周期。  
- **高度可复用**：同一套业务逻辑可以在多个框架（React、Vue、Solid、Svelte）之间共享，提升团队代码复用率。  
- **提升交付质量**：成熟的开源社区和丰富的功能特性（虚拟化、服务器端渲染、行/列冻结等）帮助团队交付更流畅、响应更快的前端体验。

**典型接入方式**  
1. **阅读官方 README**，选择对应框架的适配包（如 `@tanstack/react-table`、`@tanstack/vue-table` 等）。  
2. **在项目中安装**：`npm i @tanstack/react-table`（或对应框架的包）。  
3. **创建表格实例**：使用 `createTable` 定义列、数据源及所需插件（排序、过滤、分页、虚拟化等）。  
4. **在 UI 组件中渲染**：将表格实例的状态（`getHeaderGroups`、`getRowModel` 等）绑定到自定义的 JSX/Template 中，即可得到完整的表格 UI。  
5. **小范围 PoC**：先在一个独立页面或功能模块实现一个简易表格，验证 API、样式集成以及性能表现，再逐步推广到全局。

**生产可用性**  
- **活跃度高**：截至 2026‑07‑12，GitHub ★28.1k、Fork 3.5k，最近一次提交在当日，社区活跃且维护频繁。  
- **技术成熟**：全 TypeScript 编写，提供完整类型定义，兼容现代前端生态（React 18+、Vue 3+ 等）。  
- **生态支持**：拥有丰富的插件体系（虚拟化、服务器端渲染、树形结构等），并被多家大型产品在生产环境中使用。  
- **风险**：目前未发现重大许可证或安全隐患，但仍建议在正式上线前进行一次安全审计，并确认维护者响应速度符合内部 SLA。  

综上，TanStack/table 在功能完整性、社区活跃度和技术成熟度上均达到生产级别，适合作为前端数据表格的核心库，先通过小型 PoC 验证后即可在项目中大规模推广。

## 🧭 Practical evaluation

**Value:** TanStack/table helps ship user-facing interfaces with less custom UI work.

**Best use cases**

- build product UI faster
- reuse interface components
- improve frontend delivery

**Integration notes:** Looks feasible to evaluate, but integration should start with a small proof of concept and README check.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 28176 GitHub stars
- 3539 forks
- updated 2026-07-12
- primary language: TypeScript
- 19 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 89/100 |
| stars | 95/100 |
| topics | 100/100 |
| outlook | 80/100 |
| quality | 92/100 |
| recency | 80/100 |
| adoption | 93/100 |
| production | 76/100 |
| usefulness | 42/100 |
| integration | 46/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 100/100 |

---

<sub>🔭 Discovered 2026-07-12 · [View on GitHub](https://github.com/TanStack/table) · [← Back to Frontend](./README.md)</sub>
