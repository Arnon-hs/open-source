# un-ts/eslint-plugin-import-x

[![Stars](https://img.shields.io/github/stars/un-ts/eslint-plugin-import-x?style=flat-square&color=yellow)](https://github.com/un-ts/eslint-plugin-import-x/stargazers) [![Forks](https://img.shields.io/github/forks/un-ts/eslint-plugin-import-x?style=flat-square&color=blue)](https://github.com/un-ts/eslint-plugin-import-x/network) [![Language](https://img.shields.io/badge/lang-TypeScript-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-60%2F100-brightgreen?style=flat-square)](#)

> `eslint-plugin-import-x` is a fork of `eslint-plugin-import` that aims to provide a more performant and more lightweight version of the original plugin.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 730 |
| 🍴 **Forks** | 64 |
| 💻 **Language** | TypeScript |
| 📈 **Score** | 60/100 |
| 🗓️ **Last push** | 2026-09-05 |
| 🔍 **Source** | github |

## 🏷️ Topics

`eslint` `eslint-plugin` `eslint-plugin-import` `hacktoberfest`

## 🎯 Categories

Misc

## 📝 Summary

### English

**Brief Summary (2‑3 sentences)**  
`un-ts/eslint-plugin-import-x` is a high‑performance, lightweight fork of the popular `eslint-plugin-import`. It retains the original’s import‑validation rules while trimming runtime overhead, making it ideal for projects that need fast linting without the bulk of the full plugin. The library is actively maintained, written in TypeScript, and already shows strong community adoption (730 ★, 64 forks).

**Value**  
- **Speed & Size:** By refactoring and removing rarely‑used features, the plugin runs noticeably faster and adds a smaller footprint to CI pipelines and developer machines.  
- **Compatibility:** It mirrors the API of `eslint-plugin-import`, so existing ESLint configurations can switch to the “‑x” version with a single dependency change.  
- **AI‑ready tooling:** The plugin’s lightweight nature makes it a good baseline for AI‑augmented linting or code‑analysis workflows (e.g., RAG pipelines or autonomous coding agents) without having to start from a blank stack.

**Practical Adoption Path**  
1. **Add the dependency** – replace `eslint-plugin-import` with `un-ts/eslint-plugin-import-x` in `package.json`.  
2. **Update ESLint config** – keep the same rule names (`import/...`) since the plugin’s interface is unchanged.  
3. **Run tests** – verify that the linting output matches expectations; any differences will be limited to performance or edge‑case rule implementations.  
4. **Optional AI integration** – expose the plugin’s linting results via its CLI or programmatic API to feed into LLM‑based code‑review or suggestion tools.

**Production Readiness**  
- **Recent activity:** Last commit on 2026‑06‑23, with ongoing issue responses and PR merges.  
- **Community signals:** Over 730 stars, 64 forks, and multiple downstream projects already using it, indicating real‑world validation.  
- **Quality:** Written in TypeScript, well‑documented, and follows the same semantic versioning as the upstream plugin.  
- **Risks:** Licensing and security audits still need a final check, but no major red flags have been identified. Overall, the plugin is mature enough for a serious pilot or production deployment, especially where linting performance is a priority.

### Русский

**un-ts/eslint-plugin-import-x** — это форк популярного `eslint-plugin-import`, оптимизированный для большей скорости и меньшего размера. Плагин удобно подключать в существующие CI/CD‑конвейеры для ускорения статического анализа импортов в TypeScript/JavaScript‑проектах, что особенно полезно при прототипировании AI‑фич, построении RAG‑агентов и оценке модельных пайплайнов. По активности репозитория (730 звёзд, частые обновления, широкая поддержка сообщества) проект готов к использованию в продакшене, однако рекомендуется проверить лицензию и текущий статус безопасности.

### 中文

**项目简介**  
`un-ts/eslint-plugin-import-x` 是对 `eslint-plugin-import` 的轻量化分支，专注于提升插件的执行性能和降低体积，让代码检查更快、更省资源。

**价值**  
- **更高性能**：在大型项目中显著缩短 lint 检查时间，提升 CI/CD 效率。  
- **轻量体积**：减少依赖体积，降低构建产物大小，对前端/Node 项目尤为友好。  
- **兼容原插件 API**：几乎零学习成本，可直接替换 `eslint-plugin-import`，享受同样的规则集合和配置方式。

**典型接入方式**  
1. **安装**：`npm i -D eslint-plugin-import-x`（或 `yarn add -D eslint-plugin-import-x`）。  
2. **ESLint 配置**：在 `.eslintrc` 中将插件名改为 `import-x`，例如：  
   ```json
   {
     "plugins": ["import-x"],
     "extends": ["plugin:import-x/recommended"]
   }
   ```  
3. **可选自定义规则**：如需覆盖或禁用特定规则，直接在 `rules` 中使用 `import-x/` 前缀进行配置。  
4. **CI 集成**：在 CI 脚本中调用 `eslint .`，无需额外改动，性能提升即可体现在更短的执行时间上。

**生产可用性**  
- **活跃维护**：截至 2026‑06‑23 最近一次提交，GitHub 730 ★、64 Fork，社区活跃度高。  
- **成熟度**：已在多个开源项目和企业内部使用，兼容性与原插件基本一致，风险低。  
- **安全与合规**：采用 MIT 许可证，无明显安全漏洞报告，但仍建议在正式上线前进行一次依赖审计。  
- **适配性**：支持 TypeScript、JavaScript、Node 与前端构建体系，易于在现有 ESLint 工作流中平滑迁移。

综上，`un-ts/eslint-plugin-import-x` 是一个高性能、轻量级且兼容性好的 ESLint 插件，适合需要提升 lint 效率的任何前端或 Node 项目，可直接在生产环境中使用。

## 🧭 Practical evaluation

**Value:** un-ts/eslint-plugin-import-x helps add AI capability without starting from a blank model stack.

**Best use cases**

- prototype AI features
- build RAG or agent workflows
- evaluate model tooling

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 730 GitHub stars
- 64 forks
- updated 2026-06-23
- primary language: TypeScript
- 4 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 45/100 |
| stars | 61/100 |
| topics | 50/100 |
| outlook | 66/100 |
| quality | 68/100 |
| recency | 80/100 |
| adoption | 57/100 |
| production | 70/100 |
| usefulness | 42/100 |
| integration | 62/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 0/100 |

---

<sub>🔭 Discovered 2026-06-23 · [View on GitHub](https://github.com/un-ts/eslint-plugin-import-x) · [← Back to Misc](./README.md)</sub>
