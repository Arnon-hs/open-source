# antfu/eslint-config

[![Stars](https://img.shields.io/github/stars/antfu/eslint-config?style=flat-square&color=yellow)](https://github.com/antfu/eslint-config/stargazers) [![Forks](https://img.shields.io/github/forks/antfu/eslint-config?style=flat-square&color=blue)](https://github.com/antfu/eslint-config/network) [![Language](https://img.shields.io/badge/lang-JavaScript-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-51%2F100-brightgreen?style=flat-square)](#)

> Anthony's ESLint config preset

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 6.2k |
| 🍴 **Forks** | 576 |
| 💻 **Language** | JavaScript |
| 📈 **Score** | 51/100 |
| 🗓️ **Last push** | 2026-08-24 |
| 🔍 **Source** | github |

## 🏷️ Topics

`eslint` `eslint-config` `eslint-flat-config`

## 🎯 Categories

Templates

## 📝 Summary

### English

**Summary**  
antfu/eslint-config is a community‑maintained ESLint preset created by Anthony Fu that bundles a well‑curated set of rules, plugins, and style guidelines for modern JavaScript/TypeScript projects. With over 6 k stars and regular updates, it aims to cut down the time developers spend on lint‑setup, code reviews, and CI feedback loops. Because the repository provides only the config files and no explicit integration guide, teams should review the rule set and test it in a sandbox before rolling it out.

**Value**  
- **Speed:** A single `npm i -D antfu/eslint-config` brings a comprehensive linting baseline, eliminating the need to hand‑pick plugins and rule sets.  
- **Consistency:** Enforces a shared code style across the codebase, reducing review friction and catching errors early in CI.  
- **Maintainability:** The preset is kept up‑to‑date by its maintainer, so you inherit the latest best‑practice recommendations without extra effort.

**Practical adoption path**  
1. **Prototype:** Add the package to a throw‑away branch or a small internal project and run `eslint . --fix` to see which rules fire.  
2. **Customize:** If needed, extend the preset in your own ESLint config to enable/disable specific rules that clash with existing conventions.  
3. **Validate:** Run the updated linting step locally and in CI for a few builds to confirm that the error budget and build times remain acceptable.  
4. **Roll‑out:** Once satisfied, promote the config to the monorepo’s shared ESLint configuration and document the required `eslint` script for all developers.

**Production readiness**  
The preset is **medium‑ready**: its popularity, recent updates (as of 2026‑06‑26), and active maintenance make it suitable for prototypes, internal tools, and even production services—provided you perform the above validation steps. Before committing to production, verify that the rule set aligns with your organization’s coding standards and that any additional dependencies (e.g., TypeScript parser plugins) are compatible with your build pipeline. Once those checks are done, antfu/eslint-config can be safely used in production environments.

### Русский

**antfu/eslint-config** — готовый набор правил ESLint от Anthony, который ускоряет разработку, автоматизируя проверку кода и улучшая обратную связь в CI. Его обычно подключают в проектах на JavaScript/TypeScript простым расширением конфигурации, однако из‑за скудной документации по интеграции рекомендуется сначала протестировать конфиг в отдельной ветке. При достаточной проверке зависимостей и поддержке он подходит для прототипов и внутренних сервисов, а для продакшн‑окружения требует дополнительного аудита и возможных доработок.

### 中文

**项目简介（2‑3 句话）**  
antfu/eslint-config 是由 Anthony 维护的开箱即用的 ESLint 规则预设，集合了业界最佳实践，帮助团队统一代码风格并捕获潜在错误。只需在项目中引用即可获得一套兼容 TypeScript、Vue、React 等生态的完整 lint 配置，极大降低手动调参的成本。

**价值**  
- **提升开发效率**：统一的规则让新成员快速上手，避免因代码风格不一致导致的重复审查。  
- **加速 CI 反馈**：在 CI 中自动执行 lint，提前发现问题，缩短合并等待时间。  
- **降低维护成本**：维护者会定期更新规则，开发者只需升级依赖即可获益。

**典型接入方式**  
1. **安装依赖**  
   ```bash
   npm i -D eslint @antfu/eslint-config
   # 或者使用 pnpm / yarn
   ```  
2. **创建或修改 ESLint 配置文件**（.eslintrc.cjs / .eslintrc.js）  
   ```js
   // .eslintrc.cjs
   module.exports = {
     extends: ['@antfu'],
   };
   ```  
3. **在 package.json 中添加脚本**（可选）  
   ```json
   "scripts": {
     "lint": "eslint . --ext .js,.ts,.vue"
   }
   ```  
4. **在编辑器中安装 ESLint 插件**，即可获得即时的代码检查与修复提示。

**生产可用性**  
- **成熟度**：GitHub ★6.2k、Fork 576，最近更新于 2026‑06‑26，活跃度高。  
- **适用场景**：非常适合原型、内部工具以及中小型业务的代码质量保障；在大型项目中使用前建议进行一次依赖冲突和规则覆盖的审查。  
- **风险**：项目元数据未提供完整的集成指引，实际接入时可能需要手动排查与已有 ESLint 配置的兼容性。  
- **建议**：在正式生产环境采用前，先在测试分支或内部 CI 中跑一遍完整的 lint，确认规则与团队约定相符，并评估升级成本。  

总体而言，antfu/eslint-config 在保持低接入门槛的同时提供了高质量的 lint 规则，经过适当的验证后即可安全用于生产环境。

## 🧭 Practical evaluation

**Value:** antfu/eslint-config helps engineers save time in daily development and review loops.

**Best use cases**

- speed up developer workflows
- automate local engineering tasks
- improve CI feedback

**Integration notes:** Needs manual inspection before adoption because integration signals are sparse in the discovered metadata.

**Production readiness:** Medium: useful for prototypes or internal workflows, with dependency and maintenance checks before production.

**Quality signals**

- 6213 GitHub stars
- 576 forks
- updated 2026-06-26
- primary language: JavaScript
- 3 topics

**Risks:** Integration path is not obvious from metadata; validate setup cost before committing.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 69/100 |
| stars | 81/100 |
| topics | 38/100 |
| outlook | 56/100 |
| quality | 65/100 |
| recency | 40/100 |
| adoption | 77/100 |
| production | 55/100 |
| usefulness | 42/100 |
| integration | 30/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 100/100 |

---

<sub>🔭 Discovered 2026-06-26 · [View on GitHub](https://github.com/antfu/eslint-config) · [← Back to Templates](./README.md)</sub>
