# carbon-design-system/sveld

[![Stars](https://img.shields.io/github/stars/carbon-design-system/sveld?style=flat-square&color=yellow)](https://github.com/carbon-design-system/sveld/stargazers) [![Forks](https://img.shields.io/github/forks/carbon-design-system/sveld?style=flat-square&color=blue)](https://github.com/carbon-design-system/sveld/network) [![Language](https://img.shields.io/badge/lang-TypeScript-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-56%2F100-brightgreen?style=flat-square)](#)

> Generate TypeScript definitions and component documentation for your Svelte components

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 444 |
| 🍴 **Forks** | 24 |
| 💻 **Language** | TypeScript |
| 📈 **Score** | 56/100 |
| 🗓️ **Last push** | 2026-09-05 |
| 🔍 **Source** | github |

## 🏷️ Topics

`docgen` `documentation` `jsdoc` `svelte` `svelte-component` `typescript-definitions`

## 🎯 Categories

Frontend · Design

## 📝 Summary

### English

**Summary:** carbon-design-system/sveld is an open-source project that generates TypeScript definitions and component documentation for Svelte components, primarily used for building Web3 workflows, inspecting blockchain integrations, and prototyping wallet or DeFi features. This project offers a valuable tool for developers to streamline their workflow and improve code maintainability. With its medium production readiness, sveld can be used in prototypes or internal workflows after thorough dependency and maintenance checks.

**Value:** The value proposition of carbon-design-system/sveld lies in its ability to simplify the development process for blockchain-based projects. By generating TypeScript definitions and component documentation, developers can focus on building complex Web3 workflows without worrying about the underlying implementation details.

**Practical Adoption Path:** To adopt sveld in a production environment, developers should first evaluate its feasibility through a small proof of concept and review the README documentation. This will help identify potential integration challenges and ensure that the project meets the specific needs of the project. Once the proof of concept is successful, developers can integrate sveld into their workflow, perform thorough dependency and maintenance checks, and gradually scale up its usage.

**Production Readiness:** The production readiness of carbon-design-system/sveld is classified as medium. While it offers a valuable tool for developers, its production readiness is contingent

### Русский

Carbon‑design‑system/sveld автоматически создаёт TypeScript‑определения и документацию для Svelte‑компонентов, ускоряя разработку и отладку Web3‑решений. Он особенно полезен для прототипирования и инспекции блокчейн‑воркфлоу (кошельков, DeFi‑интеграций) и позволяет быстро оценить интеграцию перед более глубоким погружением. Проект имеет средний уровень готовности к production: подходит для внутренних прототипов и экспериментов, но перед выводом в продакшн рекомендуется проверить зависимости, поддерживаемость и лицензи

### 中文

**项目简介**  
`carbon-design-system/sveld` 是一个面向 Svelte 组件的工具，能够自动生成 TypeScript 类型定义和完整的组件文档，从而提升代码可维护性并加速 UI 开发。

**价值**  
- **统一类型安全**：为每个 Svelte 组件输出精准的 `.d.ts`，在 TypeScript 项目中实现完整的类型检查。  
- **文档即代码**：基于组件源码自动生成 Markdown/HTML 文档，省去手动编写 API 手册的时间。  
- **加速原型与审查**：在区块链/Web3 场景下，可快速搭建钱包、DeFi、链上交互等 UI 原型，并通过生成的文档让团队成员快速了解组件的属性、事件和插槽，帮助审查链路实现细节。

**典型接入方式**  
1. **安装**：`npm i -D @carbon-design-system/sveld`（或 `pnpm add -D`）。  
2. **配置**：在项目根目录新建 `sveld.config.js`，指定组件入口、输出目录以及需要的文档格式，例如：  
   ```js
   module.exports = {
     components: 'src/lib/**/*.svelte',
     outDir: 'docs/components',
     typesDir: 'src/types',
     markdown: true,
   };
   ```
3. **运行**：在 `package.json` 中添加脚本 `"gen:docs": "sveld"`，执行 `npm run gen:docs` 即可生成 TypeScript 定义文件和文档。  
4. **CI 集成**：将上述脚本加入 CI 流程（如 GitHub Actions），确保每次提交后文档和类型保持同步。

**生产可用性**  
- **成熟度**：已有 444 ★、24 Fork，最近一次更新在 2026‑06‑27，活跃度尚可。  
- **适用场景**：非常适合作为内部原型、组件库的文档生成以及 Web3 前端的快速迭代工具。  
- **上线准备**：在生产环境使用前建议完成以下检查：  
  1. **依赖审计**：确认 `sveld` 及其依赖的许可证兼容性并通过安全扫描。  
  2. **维护者确认**：检查最近的 Issue/PR 活动，确保项目仍有活跃维护者。  
  3. **回归测试**：在小型 POC 中验证生成的 `.d.ts` 与实际运行时行为一致，避免类型不匹配导致的运行错误。  
- **风险等级**：中等。对原型和内部工具非常可靠，若用于面向外部用户的生产系统，需要额外的依赖管理和持续维护措施。

## 🧭 Practical evaluation

**Value:** carbon-design-system/sveld helps prototype or inspect blockchain workflows with open implementation details.

**Best use cases**

- build Web3 workflows
- inspect blockchain integrations
- prototype wallet or DeFi features

**Integration notes:** Looks feasible to evaluate, but integration should start with a small proof of concept and README check.

**Production readiness:** Medium: useful for prototypes or internal workflows, with dependency and maintenance checks before production.

**Quality signals**

- 444 GitHub stars
- 24 forks
- updated 2026-06-27
- primary language: TypeScript
- 6 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 35/100 |
| stars | 56/100 |
| topics | 75/100 |
| outlook | 66/100 |
| quality | 69/100 |
| recency | 80/100 |
| adoption | 50/100 |
| production | 68/100 |
| usefulness | 42/100 |
| integration | 46/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 200/100 |

---

<sub>🔭 Discovered 2026-06-27 · [View on GitHub](https://github.com/carbon-design-system/sveld) · [← Back to Frontend](./README.md)</sub>
