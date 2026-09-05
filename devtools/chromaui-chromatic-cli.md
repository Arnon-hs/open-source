# chromaui/chromatic-cli

[![Stars](https://img.shields.io/github/stars/chromaui/chromatic-cli?style=flat-square&color=yellow)](https://github.com/chromaui/chromatic-cli/stargazers) [![Forks](https://img.shields.io/github/forks/chromaui/chromatic-cli?style=flat-square&color=blue)](https://github.com/chromaui/chromatic-cli/network) [![Language](https://img.shields.io/badge/lang-TypeScript-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-62%2F100-brightgreen?style=flat-square)](#)

> Chromatic CLI: `npx chromatic`

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 337 |
| 🍴 **Forks** | 85 |
| 💻 **Language** | TypeScript |
| 📈 **Score** | 62/100 |
| 🗓️ **Last push** | 2026-09-05 |
| 🔍 **Source** | github |

## 🏷️ Topics

`cli` `storybook`

## 🎯 Categories

DevTools

## 📝 Summary

### English

**Summary**  
Chromatic CLI (`npx chromatic`) is a TypeScript‑based dev‑tool that streamlines the delivery of user‑facing interfaces by automating visual testing, component publishing, and UI preview hosting. With 337 GitHub stars and active updates (last seen 2026‑06‑22), it helps teams ship product UIs faster, reuse components safely, and catch regressions before they reach production.

**Value**  
The CLI turns Storybook stories into a CI‑friendly workflow that automatically runs visual diffs, generates shareable URLs, and publishes component libraries, reducing the amount of custom UI scaffolding and QA effort required for front‑end releases.

**Practical adoption path**  
1. **Proof‑of‑concept** – Add the package to a small feature branch, run `npx chromatic` against an existing Storybook, and verify that visual diffs and preview URLs appear as expected.  
2. **Readme & CI integration** – Follow the README to add the CLI step to your CI pipeline (GitHub Actions, CircleCI, etc.) and configure project‑specific thresholds.  
3. **Gradual rollout** – Extend the integration to additional Storybook collections, enforce visual‑test gating, and optionally enable component publishing for internal design systems.

**Production readiness**  
The project is at a medium readiness level: it is suitable for prototypes, internal tooling, and staged production use, but teams should perform a final review of the license, security posture, and maintainer activity before committing to a full production rollout. A small pilot combined with dependency vetting will mitigate the remaining risks.

### Русский

Chromatic CLI (chromaui/chromatic-cli) — инструмент командной строки для автоматизированного тестирования и деплоя UI‑компонентов, позволяющий быстрее выпускать пользовательские интерфейсы за счёт повторного использования готовых компонентов. Рекомендуется начать с небольшого proof‑of‑concept: установить пакет через `npx chromatic`, добавить базовый скрипт в CI и проверить README, а затем оценить зависимости и безопасность перед масштабированием. На текущий момент готовность к production — средняя: проект подходит для прототипов и внутренних процессов, но требует окончательной проверки лицензии, безопасности и активности поддержки.

### 中文

**项目简介**  
Chromatic CLI（`npx chromatic`）是 Chromatic 团队提供的前端可视化回归测试与 UI 部署工具，帮助团队在不编写大量自定义 UI 代码的情况下快速交付用户界面。  

**价值**  
- **加速 UI 开发**：通过自动化的视觉回归测试和组件预览，开发者可以更快地构建、复用和验证界面组件。  
- **提升交付质量**：在每次提交时捕获视觉差异，防止 UI 回归，降低上线风险。  
- **简化工作流**：与 Storybook、CI/CD 体系深度集成，一键发布可共享的 UI 预览链接。  

**典型接入方式**  
1. 在项目根目录安装依赖（或直接使用 npx）：`npx chromatic --project-token <your-token>`。  
2. 在 CI 中添加步骤，例如 GitHub Actions：  
   ```yaml
   - name: Run Chromatic
     run: npx chromatic --project-token ${{ secrets.CHROMATIC_PROJECT_TOKEN }}
   ```  
3. 根据 README 配置 Storybook 输出路径、基准分支等参数，即可在每次构建后自动生成视觉回归报告和预览链接。  

**生产可用性**  
- **成熟度**：已有 337+ 星、85+ Fork，活跃维护，最近一次更新于 2026‑06‑22，代码基于 TypeScript，社区反馈良好。  
- **适用场景**：非常适合原型、内部 UI 工作流以及需要高频视觉回归的产品团队；在正式生产环境使用前建议完成一次小范围的概念验证（PoC），并检查许可证、依赖安全性以及维护者响应速度。  
- **风险**：需自行评估许可证兼容性和潜在的安全依赖；在关键业务系统中使用前，建议进行依赖审计和灾备演练。  

总体而言，Chromatic CLI 在提升 UI 开发效率和交付可靠性方面表现突出，经过适度的前置审查后即可在生产环境中安全使用。

## 🧭 Practical evaluation

**Value:** chromaui/chromatic-cli helps ship user-facing interfaces with less custom UI work.

**Best use cases**

- build product UI faster
- reuse interface components
- improve frontend delivery

**Integration notes:** Looks feasible to evaluate, but integration should start with a small proof of concept and README check.

**Production readiness:** Medium: useful for prototypes or internal workflows, with dependency and maintenance checks before production.

**Quality signals**

- 337 GitHub stars
- 85 forks
- updated 2026-06-22
- primary language: TypeScript
- 2 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 48/100 |
| stars | 54/100 |
| topics | 25/100 |
| outlook | 65/100 |
| quality | 62/100 |
| recency | 80/100 |
| adoption | 52/100 |
| production | 68/100 |
| usefulness | 58/100 |
| integration | 62/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 100/100 |

---

<sub>🔭 Discovered 2026-06-22 · [View on GitHub](https://github.com/chromaui/chromatic-cli) · [← Back to DevTools](./README.md)</sub>
