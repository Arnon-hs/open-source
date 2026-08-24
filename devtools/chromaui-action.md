# chromaui/action

[![Stars](https://img.shields.io/github/stars/chromaui/action?style=flat-square&color=yellow)](https://github.com/chromaui/action/stargazers) [![Forks](https://img.shields.io/github/forks/chromaui/action?style=flat-square&color=blue)](https://github.com/chromaui/action/network) [![Language](https://img.shields.io/badge/lang-JavaScript-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-52%2F100-brightgreen?style=flat-square)](#)

> GitHub Action for publishing your Storybook to Chromatic

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 153 |
| 🍴 **Forks** | 42 |
| 💻 **Language** | JavaScript |
| 📈 **Score** | 52/100 |
| 🗓️ **Last push** | 2026-08-24 |
| 🔍 **Source** | github |

## 🏷️ Topics

`chromatic` `cli` `github-actions` `storybook`

## 🎯 Categories

DevTools

## 📝 Summary

### English

**Summary**  
chromaui/action is a GitHub Action that automates publishing a Storybook build to Chromatic, letting teams ship visual UI components with a single CI step. With 153 ★ and active JavaScript maintenance, it streamlines front‑end delivery by turning visual regression testing and component hosting into a plug‑and‑play CI job.

**Value**  
By embedding the publishing flow directly in the repository’s CI pipeline, the action removes the manual steps of building, uploading, and version‑tracking Storybook assets. This accelerates UI development, encourages component reuse, and gives immediate visual feedback on regressions—key for rapid product iteration and design‑dev collaboration.

**Practical adoption path**  

1. **Add the action** to your workflow (e.g., `.github/workflows/chromatic.yml`) and supply your Chromatic project token.  
2. **Configure** any optional flags (e.g., `storybookBuildDir`, `skip`, `autoAcceptChanges`) to match your build setup.  
3. **Run** the workflow on PRs or merges; the action will build Storybook, upload it to Chromatic, and post a status check with visual diff results.  
4. **Iterate** by reviewing the Chromatic UI for failures and approving changes directly from the PR comment thread.

**Production readiness**  
The project is at a medium readiness level: it’s suitable for prototypes, internal UI libraries, and teams that already use Chromatic for visual testing. The codebase is actively maintained (last update 2026‑06‑24) and has modest community adoption, but before full production rollout you should verify:

* License compatibility and any corporate policy constraints.  
* Security posture of the underlying npm dependencies.  
* Ongoing maintainer activity (e.g., issue response time) to ensure future compatibility with GitHub Actions and Chromatic API changes.

With those checks completed, chromaui/action can be safely integrated into a production CI/CD pipeline for reliable, automated UI publishing.

### Русский

**chromaui/action** — это GitHub Action, позволяющий автоматически публиковать Storybook в Chromatic, что ускоряет доставку пользовательских интерфейсов и упрощает повторное использование компонентов. Типичный сценарий: в CI‑pipeline после сборки UI вызывается действие, которое отправляет Storybook в Chromatic для визуального тестирования и деплоя, тем самым ускоряя разработку и повышая качество фронтенда. Проект имеет средний уровень готовности к production: достаточно зрелый (153 ★, 42 forks, активные обновления), но перед использованием в критических системах рекомендуется проверить лицензию, безопасность зависимостей и наличие активных мейнтейнеров.

### 中文

**项目简介**  
chromaui/action 是一个 GitHub Action，专为将 Storybook 自动发布到 Chromatic 而设计，让前端团队可以在 CI 流程中“一键”完成 UI 预览与视觉回归测试。  

**价值**  
- **加速 UI 交付**：通过自动化发布和视觉测试，开发者无需手动部署 Storybook，能够更快地迭代和验证界面。  
- **提升质量**：Chromatic 的视觉回归检测帮助捕获细微的 UI 变更，降低因界面回滚导致的用户体验风险。  
- **复用组件**：在统一的 Storybook 环境中展示组件库，促进团队内部的组件复用与协作。  

**典型接入方式**  
1. 在仓库根目录创建 `.github/workflows/chromatic.yml`（或其他工作流文件）。  
2. 使用官方提供的步骤：  
   ```yaml
   name: Publish Storybook
   on: [push, pull_request]
   jobs:
     chromatic:
       runs-on: ubuntu-latest
       steps:
         - uses: actions/checkout@v3
         - uses: actions/setup-node@v3
           with:
             node-version: '20'
         - run: npm ci
         - run: npm run build-storybook   # 生成 Storybook 静态文件
         - uses: chromaui/action@v1
           with:
             projectToken: ${{ secrets.CHROMATIC_PROJECT_TOKEN }}
   ```  
3. 在 GitHub Secrets 中添加 `CHROMATIC_PROJECT_TOKEN`（在 Chromatic 项目设置里获取），即可在每次 push 或 PR 时自动发布并运行视觉回归。  

**生产可用性**  
- **成熟度**：已有 153 ⭐、42 🍴，活跃度截至 2026‑06‑24，代码基于 JavaScript，维护相对稳定。  
- **适用场景**：适合原型、内部 UI 流程以及逐步向生产环境迁移的项目；在正式生产前建议评估依赖版本、CI 运行时长以及安全审计（许可证、第三方依赖）。  
- **风险**：暂无重大元数据风险，但仍需确认项目的许可证兼容性、依赖安全（如 npm audit）以及维护者的响应速度。  

综上，chromaui/action 为前端团队提供了“一键”发布与视觉回归的便利，接入成本低，适合作为 CI/CD 流程的一环；在完成安全与维护审查后即可在生产环境中可靠使用。

## 🧭 Practical evaluation

**Value:** chromaui/action helps ship user-facing interfaces with less custom UI work.

**Best use cases**

- build product UI faster
- reuse interface components
- improve frontend delivery

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** Medium: useful for prototypes or internal workflows, with dependency and maintenance checks before production.

**Quality signals**

- 153 GitHub stars
- 42 forks
- updated 2026-06-24
- primary language: JavaScript
- 4 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 41/100 |
| stars | 47/100 |
| topics | 50/100 |
| outlook | 52/100 |
| quality | 53/100 |
| recency | 40/100 |
| adoption | 45/100 |
| production | 52/100 |
| usefulness | 58/100 |
| integration | 46/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 100/100 |

---

<sub>🔭 Discovered 2026-06-24 · [View on GitHub](https://github.com/chromaui/action) · [← Back to DevTools](./README.md)</sub>
