# mozilla/addons-linter

[![Stars](https://img.shields.io/github/stars/mozilla/addons-linter?style=flat-square&color=yellow)](https://github.com/mozilla/addons-linter/stargazers) [![Forks](https://img.shields.io/github/forks/mozilla/addons-linter?style=flat-square&color=blue)](https://github.com/mozilla/addons-linter/network) [![Language](https://img.shields.io/badge/lang-JavaScript-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-62%2F100-brightgreen?style=flat-square)](#)

> 🔍 Firefox Add-ons linter, written in JavaScript. 👁

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 356 |
| 🍴 **Forks** | 157 |
| 💻 **Language** | JavaScript |
| 📈 **Score** | 62/100 |
| 🗓️ **Last push** | 2026-05-11 |
| 🔍 **Source** | github |

## 🏷️ Topics

`cli` `web-extensions`

## 🎯 Categories

DevTools

## 📝 Summary

### English

**Brief Summary (2‑3 sentences)**  
Mozilla’s **addons‑linter** is a JavaScript‑based linter that validates Firefox add‑ons against the latest AMO policies and best‑practice guidelines. It helps engineers catch packaging, manifest, and API‑usage errors early, reducing manual review time and improving CI feedback quality. With a modest star count and recent activity, it is a practical tool for internal prototype pipelines and can be expanded to production with a small proof‑of‑concept rollout.  

**Value**  
- **Time savings:** Automates the repetitive checks that reviewers perform on every submission, cutting down on back‑and‑forth communication.  
- **Consistency:** Enforces a single source of truth for linting rules, ensuring every developer receives the same feedback.  
- **CI integration:** Generates machine‑readable reports that can fail builds, giving developers immediate, actionable results.  

**Practical Adoption Path**  
1. **Proof of concept:** Clone the repo, run the linter locally on a few existing add‑ons, and verify that the output aligns with your team’s review standards.  
2. **README/Docs check:** Confirm the documentation covers the version of the Firefox Add‑on SDK you use; update any missing steps for your environment.  
3. **CI hook:** Add a step to your CI pipeline (e.g., GitHub Actions, Jenkins) that runs `addons-linter` on PRs and fails the job on lint errors.  
4. **Gradual rollout:** Enable the lint step for a single team or a subset of repositories, collect feedback, and iterate on rule configuration.  

**Production Readiness**  
- **Current maturity:** Medium. The project is actively maintained (last commit 2026‑05‑11) and has a modest community (≈350 ★, 150 forks), making it suitable for internal prototypes and early‑stage production.  
- **Dependencies & maintenance:** Verify the transitive JavaScript dependencies for known vulnerabilities and confirm that a maintainer is responsive to security issues.  
- **Risk considerations:** No major licensing or metadata concerns, but a final security audit and a check on long‑term maintainer commitment are advisable before scaling to mission‑critical pipelines.  

Overall, **addons‑linter** offers a clear productivity boost for Firefox add‑on development, and with a controlled proof‑of‑concept and due‑diligence on security/maintenance, it can be safely promoted to production use.

### Русский

**mozilla/addons-linter** — это JavaScript‑линтер для Firefox‑добавок, который ускоряет цикл разработки и ревью, позволяя автоматизировать локальные проверки и получать более быстрый фидбек в CI. Рекомендуется начать интеграцию с небольшого proof‑of‑concept (например, проверив README и запустив линтер на одном‑двух проектах), после чего оценить зависимости и план обслуживания. Уровень готовности — средний: проект подходит для прототипов и внутренних процессов, но перед выводом в продакшн требуется окончательная проверка лицензий, безопасности и активности мейнтейнеров.

### 中文

**项目简介（2‑3 句）**  
mozilla/addons‑linter 是一款用 JavaScript 编写的 Firefox 扩展代码检查工具，能够在本地或 CI 环境中自动发现常见的安全、兼容性和最佳实践问题。它帮助开发者在提交前快速获得高质量的 lint 反馈，从而缩短调试和审查周期。

**价值**  
- **提升开发效率**：在编辑器或 CI 中即时捕获错误，避免因低级 bug 进入审查环节。  
- **统一质量标准**：提供官方维护的规则集，确保所有 Add‑on 代码遵循 Firefox 的安全与兼容性要求。  
- **加速反馈循环**：在 Pull Request 中自动生成检查报告，帮助 reviewer 更专注于业务逻辑。

**典型接入方式**  
1. **本地开发**：在项目根目录 `npm install --save-dev @mozilla/addons-linter`，并在 `package.json` 中添加脚本，例如 `"lint:addons": "addons-linter ./src"`，配合 VSCode 插件或 pre‑commit 钩子使用。  
2. **CI 集成**：在 GitHub Actions、GitLab CI 或 Jenkins 中添加一步执行 `npx addons-linter ./dist`，并将返回的错误码设为构建失败；也可以使用官方提供的 Docker 镜像 `mozilla/addons-linter` 进行无依赖运行。  
3. **Proof‑of‑Concept**：先在 README 或 CI 中跑一次完整检查，确认规则集与项目实际需求匹配，再逐步推广到全部仓库。

**生产可用性**  
- **成熟度**：Medium。已有 356 ⭐、157 🍴，活跃更新至 2026‑05‑11，适合原型、内部工具或对质量要求较高的生产环境。  
- **准备工作**：在正式上线前需完成以下检查  
  - 依赖审计（确保没有已知安全漏洞的子依赖）。  
  - 许可证兼容性确认（MIT/Apache 等）。  
  - 维护者活跃度评估，若长期无人维护则考虑自行 fork。  
- **风险**：暂无重大元数据风险，但仍需对安全姿态和长期维护进行最终评估。  

综上，addons‑linter 能显著提升 Firefox 扩展的开发与审查效率，接入方式灵活，经过适当的依赖与维护审查后即可在生产环境可靠使用。

## 🧭 Practical evaluation

**Value:** mozilla/addons-linter helps engineers save time in daily development and review loops.

**Best use cases**

- speed up developer workflows
- automate local engineering tasks
- improve CI feedback

**Integration notes:** Looks feasible to evaluate, but integration should start with a small proof of concept and README check.

**Production readiness:** Medium: useful for prototypes or internal workflows, with dependency and maintenance checks before production.

**Quality signals**

- 356 GitHub stars
- 157 forks
- updated 2026-05-11
- primary language: JavaScript
- 2 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 55/100 |
| stars | 54/100 |
| topics | 25/100 |
| outlook | 73/100 |
| quality | 68/100 |
| recency | 100/100 |
| adoption | 55/100 |
| production | 72/100 |
| usefulness | 58/100 |
| integration | 46/100 |
| sourceTrust | 100/100 |

---

<sub>🔭 Discovered 2026-05-11 · [View on GitHub](https://github.com/mozilla/addons-linter) · [← Back to DevTools](./README.md)</sub>
