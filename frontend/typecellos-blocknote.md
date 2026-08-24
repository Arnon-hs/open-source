# TypeCellOS/BlockNote

[![Stars](https://img.shields.io/github/stars/TypeCellOS/BlockNote?style=flat-square&color=yellow)](https://github.com/TypeCellOS/BlockNote/stargazers) [![Forks](https://img.shields.io/github/forks/TypeCellOS/BlockNote?style=flat-square&color=blue)](https://github.com/TypeCellOS/BlockNote/network) [![Language](https://img.shields.io/badge/lang-TypeScript-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-59%2F100-brightgreen?style=flat-square)](#)

> A React Rich Text Editor that's block-based (Notion style) and extensible. Built on top of Prosemirror and Tiptap.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 9.9k |
| 🍴 **Forks** | 749 |
| 💻 **Language** | TypeScript |
| 📈 **Score** | 59/100 |
| 🗓️ **Last push** | 2026-08-24 |
| 🔍 **Source** | github |

## 🏷️ Topics

`block-based` `editor` `javascript` `notion` `notion-editor` `prosemirror` `react` `rich-text-editor` `tiptap` `typescript` `wysiwyg` `yjs`

## 🎯 Categories

Frontend

## 📝 Summary

### English

**Brief Summary**  
TypeCellOS/BlockNote is a block‑based rich‑text editor for React, modeled after Notion’s UI and built on top of ProseMirror and Tiptap. With 9 928 GitHub stars and active maintenance, it offers a highly extensible, TypeScript‑first solution for building user‑facing interfaces with far less custom UI work.  

**Value**  
- **Speed to market:** Developers can drop a ready‑made, drag‑and‑drop‑style editor into any React app and immediately get Notion‑like block editing, saving weeks of UI engineering.  
- **Reusability:** Blocks are composable and can be shared across projects, enabling a library of pre‑built content components (tables, lists, media embeds, etc.).  
- **Extensibility:** Because it sits on ProseMirror/Tiptap, custom node types, commands, and collaborative plugins can be added without rewriting the core editor.  

**Practical Adoption Path**  
1. **Proof‑of‑concept:** Clone the repo, run the example app, and replace a small existing textarea or markdown editor with a `<BlockNoteEditor />` component.  
2. **README & Docs Review:** Follow the quick‑start guide to configure the toolbar, block types, and data serialization.  
3. **Incremental Integration:** Wrap the editor in a feature flag or a sandboxed page, validate data flow (e.g., saving JSON to your backend), and add any needed custom blocks.  
4. **Full‑scale rollout:** Once the POC passes functional and UI tests, replace the legacy editor across the product, leveraging the same block definitions for consistency.  

**Production Readiness**  
- **Activity & Ecosystem:** Recent commits (as of 2026‑07‑06), a vibrant community (≈10 k stars, 749 forks) and a TypeScript codebase indicate strong momentum.  
- **Stability:** The core ProseMirror/Tiptap foundations are battle‑tested; BlockNote adds a thin abstraction layer that has been used in multiple open‑source and commercial projects.  
- **Risks:** No immediate licensing or security red flags, but a final audit of the MIT license compliance, dependency vulnerabilities, and maintainer responsiveness is recommended before a large‑scale deployment.  

Overall, BlockNote is a production‑ready, extensible editor that can accelerate UI development for any React‑based product, provided a small pilot is run to confirm fit and to perform a final security/license review.

### Русский

Резюме TypeCellOS/BlockNote:

TypeCellOS/BlockNote - это высокопроизводительный редактор富ого текста на основе React, который позволяет быстро создавать пользовательские интерфейсы с минимальным вложением усилий в разработку custom UI. Этот проект идеально подходит для случаев, когда необходимо быстро внедрить продукт и использовать готовые компоненты интерфейса. TypeCellOS/BlockNote готов к использованию в production и имеет сильные показатели активности, внедрения и экосистемы, что делает его надежным выбором для серьезных проектов.

### 中文

**项目简介（2‑3 句）**  
TypeCellOS/BlockNote 是基于 ProseMirror 与 Tiptap 实现的块级（Notion 风格）React 富文本编辑器，具备高度可扩展性。它提供了开箱即用的块组件库，帮助开发者快速搭建复杂的用户界面，而无需自行编写大量编辑器 UI 代码。

**价值**  
- **降低前端开发成本**：通过复用 BlockNote 的块组件和编辑器逻辑，产品 UI 可以在数小时内完成原型搭建，显著缩短交付周期。  
- **提升一致性与可维护性**：统一的块模型让不同页面、模块之间的编辑体验保持一致，后期迭代和功能扩展也更简洁。  
- **生态兼容**：基于 TypeScript、React 与 Tiptap，天然兼容现有前端技术栈，易于与业务系统、状态管理库（Redux、Zustand 等）以及后端 API 对接。

**典型接入方式**  
1. **阅读 README 与示例**：项目提供了完整的快速入门指南和 CodeSandbox 示例，先跑通本地开发环境。  
2. **在项目中安装**：`npm i @typecellos/blocknote`（或 `yarn add`），并在需要的页面引入 `BlockNoteEditor` 组件。  
3. **自定义块**：通过 Tiptap 插件机制或 BlockNote 的 `createBlockSpec` API，添加业务专属块（如商品卡片、图表等）。  
4. **小规模 PoC**：在现有业务的一个编辑页面或内部工具中实现一个最小可运行的示例，验证功能、性能和样式兼容性后再逐步推广。  

**生产可用性**  
- **活跃度**：截至 2026‑07‑06，项目仍在持续更新，GitHub 近 10k 星、750+ Fork，社区活跃，具备可靠的维护者。  
- **技术成熟度**：基于业界成熟的 ProseMirror 与 Tiptap，类型安全的 TypeScript 实现，已在多个开源/商业项目中使用。  
- **风险评估**：暂无重大元数据或许可证风险，但建议在正式投产前完成以下检查：  
  - 复审开源许可证（MIT）与公司合规性。  
  - 通过 Snyk / Dependabot 等工具审计依赖安全。  
  - 确认维护者响应速度，必要时可考虑内部 fork 维护关键功能。  

综合来看，BlockNote 已具备 **高** 的生产就绪度，适合作为前端富文本编辑需求的首选 OSS 方案，建议先在小范围 PoC 验证后逐步在产品线上推广。

## 🧭 Practical evaluation

**Value:** TypeCellOS/BlockNote helps ship user-facing interfaces with less custom UI work.

**Best use cases**

- build product UI faster
- reuse interface components
- improve frontend delivery

**Integration notes:** Looks feasible to evaluate, but integration should start with a small proof of concept and README check.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 9928 GitHub stars
- 749 forks
- updated 2026-07-06
- primary language: TypeScript
- 12 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 72/100 |
| stars | 85/100 |
| topics | 100/100 |
| outlook | 63/100 |
| quality | 77/100 |
| recency | 40/100 |
| adoption | 81/100 |
| production | 61/100 |
| usefulness | 42/100 |
| integration | 46/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 100/100 |

---

<sub>🔭 Discovered 2026-07-06 · [View on GitHub](https://github.com/TypeCellOS/BlockNote) · [← Back to Frontend](./README.md)</sub>
