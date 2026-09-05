# rsub122/tabsmith-lint

[![Stars](https://img.shields.io/github/stars/rsub122/tabsmith-lint?style=flat-square&color=yellow)](https://github.com/rsub122/tabsmith-lint/stargazers) [![Forks](https://img.shields.io/github/forks/rsub122/tabsmith-lint?style=flat-square&color=blue)](https://github.com/rsub122/tabsmith-lint/network) [![Language](https://img.shields.io/badge/lang-Unknown-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-38%2F100-brightgreen?style=flat-square)](#)

> Discovered from Hacker News (github-mentions)

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | — |
| 🍴 **Forks** | — |
| 💻 **Language** | Unknown |
| 📈 **Score** | 38/100 |
| 🗓️ **Last push** | 2026-09-05 |
| 🔍 **Source** | hackernews |

## 🏷️ Topics

`hn` `github-mentions`

## 🎯 Categories

Misc

## 📝 Summary

### English

**Summary**  
Tabsmith‑lint is an open‑source linter that scans a Chrome extension’s manifest and source files for the same policy violations that cause Chrome Web Store rejections, letting developers catch problems before they submit. By surfacing these issues locally, it speeds up the development‑review cycle and can be hooked into CI pipelines for automated feedback.  

**Value**  
- **Time savings:** Detects disallowed APIs, missing icons, oversized bundles, and other policy breaches early, preventing costly re‑submission cycles.  
- **Workflow integration:** Works as a command‑line tool that can be run on demand or as part of pre‑commit hooks, CI jobs, or build scripts, giving developers immediate, actionable feedback.  
- **Quality boost:** Reduces the likelihood of store rejections, leading to smoother releases and higher confidence in extension quality.  

**Practical adoption path**  
1. **Evaluate locally:** Clone the repo, run `tabsmith-lint` against an existing extension to see the warnings it produces.  
2. **Add to the toolchain:** Install it as a dev dependency (`npm i -D tabsmith-lint`) and create an npm script (e.g., `"lint:chrome": "tabsmith-lint src/manifest.json"`).  
3. **Automate:** Integrate the script into CI (GitHub Actions, GitLab CI, etc.) and optionally enforce a “lint‑pass” gate before merges.  
4. **Iterate:** Review false positives or missing rules and, if needed, contribute improvements or configure rule overrides.  

**Production readiness**  
- **Maturity:** Rated “Medium”. The tool is functional and recently updated (2026‑06‑26) but has sparse integration metadata, limited documentation, and an unclear release cadence.  
- **Risks:** Verify the license, check the issue tracker for active maintenance, and confirm that the rule set aligns with the latest Chrome Web Store policies before relying on it in production.  
- **Best use:** Ideal for prototypes, internal tooling, or as a gating step in CI where you can monitor its output and supplement it with manual reviews until the project’s maintenance health is confirmed.

### Русский

**Tabsmith‑lint** — утилита, автоматически проверяющая ваш расширенный код на типичные причины отклонения в Chrome Web Store, тем самым экономя время на ручных ревью и ускоряя CI‑feedback. При внедрении её обычно добавляют в локальный набор линтеров и в пайплайн CI, предварительно проверив лицензию, активность репозитория и наличие документации, поскольку метаданные интеграции скудны. Готовность к production — средняя: проект подходит для прототипов и внутренних процессов, но требует дополнительного аудита зависимости и поддержки перед масштабным использованием.

### 中文

**项目简介**  
Tabsmith‑lint 是一款专门用于检测 Chrome Web Store 上架审核会因哪些问题被拒的工具，帮助开发者在提交前提前发现并修复潜在违规，从而节省审稿时间。  

**价值**  
- **提前捕获审查风险**：在本地或 CI 中运行 lint，即可发现违规的 manifest、权限或 CSP 等问题，避免因被 Chrome 审核拒绝而产生的返工。  
- **加速开发与评审**：将审查规则自动化嵌入日常开发流程或 CI，提升 PR 检查效率，缩短上线周期。  
- **降低成本**：减少因审查被拒导致的重复提交和人工沟通，间接节约人力和时间成本。  

**典型接入方式**  
1. **本地使用**：在项目根目录下安装 `tabsmith-lint`（例如 `npm i -D tabsmith-lint`），并在 `package.json` 中添加脚本 `lint:chrome "tabsmith-lint"`，开发时通过 `npm run lint:chrome` 手动检查。  
2. **CI 集成**：在 GitHub Actions、GitLab CI、CircleCI 等流水线中添加一步执行 `tabsmith-lint`，并将其返回的错误码设为 CI 失败条件，确保每次提交都通过审查检查。  
3. **编辑器插件**（可选）：如果社区已有 VS Code/IDE 插件，可在编辑器中实时提示违规项，实现即时反馈。  

**生产可用性**  
- **成熟度**：当前评估为 **Medium**，适合作为原型或内部工作流的自动化工具。  
- **依赖与维护**：项目最近一次更新为 2026‑06‑26，元数据较少，需自行检查许可证、维护频率、issue 处理情况以及发布节奏。  
- **采纳建议**：在正式生产环境使用前，先在内部项目或测试分支进行验证，评估其规则覆盖度与误报率；若满足需求，再逐步推广到全链路 CI。  

综上，Tabsmith‑lint 能显著提升 Chrome 扩展的提交质量与开发效率，但在正式生产环境采用前，建议完成充分的手动评审与依赖审计。

## 🧭 Practical evaluation

**Value:** Tabsmith-lint catches Chrome Web Store rejections before you submit helps engineers save time in daily development and review loops.

**Best use cases**

- speed up developer workflows
- automate local engineering tasks
- improve CI feedback

**Integration notes:** Needs manual inspection before adoption because integration signals are sparse in the discovered metadata.

**Production readiness:** Medium: useful for prototypes or internal workflows, with dependency and maintenance checks before production.

**Quality signals**

- updated 2026-06-26
- 2 topics

**Risks:** Quality signals are limited; verify license, maintenance, docs, issues, and release cadence before using it.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 0/100 |
| stars | 0/100 |
| topics | 25/100 |
| outlook | 47/100 |
| quality | 36/100 |
| recency | 80/100 |
| adoption | 0/100 |
| production | 51/100 |
| usefulness | 42/100 |
| integration | 30/100 |
| sourceTrust | 80/100 |
| categoryMatchCount | 0/100 |

---

<sub>🔭 Discovered 2026-06-26 · [View on GitHub](https://github.com/rsub122/tabsmith-lint) · [← Back to Misc](./README.md)</sub>
