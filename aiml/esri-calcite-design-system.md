# Esri/calcite-design-system

[![Stars](https://img.shields.io/github/stars/Esri/calcite-design-system?style=flat-square&color=yellow)](https://github.com/Esri/calcite-design-system/stargazers) [![Forks](https://img.shields.io/github/forks/Esri/calcite-design-system?style=flat-square&color=blue)](https://github.com/Esri/calcite-design-system/network) [![Language](https://img.shields.io/badge/lang-TypeScript-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-61%2F100-brightgreen?style=flat-square)](#)

> A monorepo containing the packages for Esri's Calcite Design System

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 361 |
| 🍴 **Forks** | 89 |
| 💻 **Language** | TypeScript |
| 📈 **Score** | 61/100 |
| 🗓️ **Last push** | 2026-05-12 |
| 🔍 **Source** | github |

## 🏷️ Topics

`accessibility` `arcgis-online` `calcite` `calcite-components` `component-library` `custom-elements` `design-system` `esri` `hacktoberfest` `i18n` `stenciljs` `typescript`

## 🎯 Categories

AI/ML · Frontend · Design

## 📝 Summary

### English

**Brief Summary (2‑3 sentences)**  
Esri’s **Calcite Design System** is a TypeScript‑based monorepo that bundles a collection of UI components, styles, and tooling for building consistent, accessible web applications that follow Esri’s design language. The repository is actively maintained (last commit 2026‑05‑12), has strong community traction (361 ⭐, 89 🍴), and is positioned as a solid foundation for adding AI‑enhanced front‑end features without having to start from scratch.  

**Value Proposition**  
- **Accelerated UI development** – Provides ready‑made, themeable components (buttons, dialogs, maps, etc.) that integrate seamlessly with Esri’s mapping libraries, letting teams focus on AI logic rather than UI boilerplate.  
- **AI‑ready extensibility** – The design system’s component architecture makes it easy to embed AI‑driven widgets (e.g., chat assistants, RAG result panels) while preserving a unified look‑and‑feel across the application.  

**Practical Adoption Path**  
1. **Proof‑of‑concept** – Clone the repo, run the `README`‑guided starter app, and replace a sample component with a simple AI widget (e.g., a text‑completion field).  
2. **Component integration** – Import the needed Calcite components via the monorepo’s package manager (npm/yarn) into your existing TypeScript front‑end, customizing themes through the provided design tokens.  
3. **Iterative rollout** – Gradually replace custom UI pieces with Calcite equivalents, leveraging its built‑in accessibility and responsiveness, while wiring AI services (LLMs, RAG pipelines) into the new components.  

**Production Readiness**  
- **High**: Recent commits, active issue triage, and a growing user base indicate a mature, well‑maintained codebase.  
- **Signals**: Strong GitHub metrics (361 stars, 89 forks), multiple topics, and TypeScript typing ensure stability and ease of integration.  
- **Remaining checks**: Conduct a final review of the MIT/Apache license compliance, run a security audit of dependencies, and confirm that core maintainers are responsive before a full‑scale production deployment.

### Русский

**Esri/calcite-design-system** — это открытый набор компонентов и стилей на TypeScript, позволяющий быстро внедрять в веб‑приложения готовый дизайн‑систему Esri и, при этом, добавить AI‑функциональность без необходимости строить стек с нуля. Типичный сценарий — создание прототипа AI‑фич (например, RAG‑агентов или интерактивных визуализаций) в небольшом proof‑of‑concept, используя готовую документацию и примеры из README, а затем масштабирование в полноценный продукт. Проект считается почти готовым к production: активные коммиты (обновление 2026‑05‑12), широкое принятие (361 ★, 89 forks), сильные сигналы экосистемы и поддержка TypeScript делают его надёжным кандидатом для серьёзных пилотных внедрений.

### 中文

**项目简介**  
Esri 的 Calcite Design System 是一个 monorepo，统一维护了构建 Esri UI 组件库所需的所有 npm 包，提供一致、可定制的前端设计规范与实现。  

**价值**  
- **提升开发效率**：直接复用成熟的 UI 组件和主题体系，无需从零搭建样式系统或交互规范。  
- **统一品牌体验**：所有组件遵循 Esri 的视觉与交互准则，确保产品在不同项目间保持一致的品牌形象。  
- **可扩展的 AI 集成**：组件已做好与 AI 功能（如聊天机器人、RAG 界面）的嵌入准备，帮助快速原型化 AI 特性。  

**典型接入方式**  
1. **阅读 README 与文档**，确认所需的 package（如 `@esri/calcite-components`、`@esri/calcite-react`）。  
2. **在项目中安装**：`npm i @esri/calcite-components`（或对应的框架适配包）。  
3. **在代码中引入并使用**：  
   ```tsx
   import { CalciteButton } from "@esri/calcite-components-react";
   <CalciteButton appearance="solid">提交</CalciteButton>
   ```  
4. **按需自定义主题**：通过 CSS custom properties 或主题 JSON 覆盖默认配色、字号等。  
5. **小范围 PoC**：先在一个独立的页面或组件库中实验，验证样式兼容性与打包体积后再推广到全局。  

**生产可用性**  
- **活跃度高**：截至 2026‑05‑12 最近一次提交，拥有 361 ★、89 🍴，且持续接受 PR 与 Issue。  
- **技术成熟**：使用 TypeScript 编写，提供完整的类型声明，兼容主流前端框架（React、Vue、Angular）。  
- **社区与生态**：在 Esri 生态体系中被广泛采用，已有多款官方产品基于 Calcite 上线。  
- **风险**：需进一步审查许可证（Apache‑2.0）与安全依赖，但整体安全姿态良好，适合作为正式生产环境的 UI 基础设施。  

综上，Calcite Design System 可作为前端 UI 的即插即用解决方案，快速实现统一视觉、加速 AI 功能原型，并具备足够的成熟度支撑生产级部署。

## 🧭 Practical evaluation

**Value:** Esri/calcite-design-system helps add AI capability without starting from a blank model stack.

**Best use cases**

- prototype AI features
- build RAG or agent workflows
- evaluate model tooling

**Integration notes:** Looks feasible to evaluate, but integration should start with a small proof of concept and README check.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 361 GitHub stars
- 89 forks
- updated 2026-05-12
- primary language: TypeScript
- 14 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 49/100 |
| stars | 54/100 |
| topics | 100/100 |
| outlook | 77/100 |
| quality | 79/100 |
| recency | 100/100 |
| adoption | 53/100 |
| production | 76/100 |
| usefulness | 42/100 |
| integration | 46/100 |
| sourceTrust | 100/100 |

---

<sub>🔭 Discovered 2026-05-13 · [View on GitHub](https://github.com/Esri/calcite-design-system) · [← Back to AI/ML](./README.md)</sub>
