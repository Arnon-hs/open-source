# semantic-release/release-notes-generator

[![Stars](https://img.shields.io/github/stars/semantic-release/release-notes-generator?style=flat-square&color=yellow)](https://github.com/semantic-release/release-notes-generator/stargazers) [![Forks](https://img.shields.io/github/forks/semantic-release/release-notes-generator?style=flat-square&color=blue)](https://github.com/semantic-release/release-notes-generator/network) [![Language](https://img.shields.io/badge/lang-JavaScript-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-68%2F100-brightgreen?style=flat-square)](#)

> :clipboard: semantic-release plugin to generate changelog content with conventional-changelog

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 362 |
| 🍴 **Forks** | 51 |
| 💻 **Language** | JavaScript |
| 📈 **Score** | 68/100 |
| 🗓️ **Last push** | 2026-05-11 |
| 🔍 **Source** | github |

## 🏷️ Topics

`changelog` `conventional-changelog` `conventional-commits` `github` `publish` `release` `semantic-release`

## 🎯 Categories

DevTools

## 📝 Summary

### English

**Brief Summary**  
semantic‑release/release‑notes‑generator is a JavaScript plugin for semantic‑release that automatically creates conventional‑changelog style release notes. By extracting commit messages, it builds a ready‑to‑publish changelog, cutting the manual effort required for every version bump.

**Value**  
The plugin turns a repetitive, error‑prone step—writing release notes—into an automated, consistent process. Teams gain faster feedback in CI pipelines, cleaner pull‑request histories, and a single source of truth for what changed between releases, which speeds up review cycles and reduces the cognitive load on engineers.

**Practical Adoption Path**  
1. **Add the package** – `npm i -D @semantic-release/release-notes-generator`.  
2. **Configure semantic‑release** – add the plugin to the `plugins` array in `.releaserc` (or `release.config.js`).  
3. **Adopt Conventional Commits** – ensure developers follow the conventional‑commit format (e.g., via commit‑lint or a commit‑msg template).  
4. **Run in CI** – let the existing semantic‑release workflow invoke the generator; the generated notes are automatically attached to the GitHub release and can be consumed by downstream tools (changelog files, Slack notifications, etc.).  

**Production Readiness**  
- **Activity & Adoption** – 362 ★, 51 forks, recent commits (as of 2026‑05‑11) and wide usage across many CI pipelines indicate a healthy, actively maintained project.  
- **Stability** – The plugin is a core part of the semantic‑release ecosystem, with clear versioning, extensive test coverage, and compatibility with the latest Node.js releases.  
- **Risk Profile** – No major licensing or security red flags have been identified; the remaining due‑diligence steps are confirming maintainer responsiveness and reviewing any disclosed vulnerabilities.  

Overall, the release‑notes‑generator is production‑ready for pilots and can be rolled out to all projects that already use semantic‑release or are looking to adopt automated versioning.

### Русский

**semantic-release/release-notes-generator** — это плагин для semantic‑release, автоматически формирующий содержимое changelog‑а на основе conventional‑changelog. Он позволяет инженерам экономить время на ручном составлении релиз‑нот, ускоряя рабочие циклы и улучшая обратную связь в CI, а также легко интегрируется через API/CLI в существующие пайплайны. Проект имеет высокую готовность к production: активная поддержка, свежие коммиты (обновлён 2026‑05‑11), 362 ★ на GitHub и широкое принятие в сообществе.

### 中文

**项目简介**  
semantic-release/release-notes-generator 是一个基于 conventional‑changelog 的 semantic‑release 插件，用于自动生成符合约定的发布说明（changelog）。它通过解析提交信息，实时产出结构化的变更日志，帮助团队保持发布记录的一致性与可读性。

**价值**  
- **节省时间**：自动化生成发布说明，免去手动编写和审校的繁琐工作。  
- **提升效率**：在 CI/CD 流程中即刻提供变更概览，加速代码审查和发布决策。  
- **统一规范**：强制使用 conventional‑commit 规范，确保日志格式统一，便于后续追踪和审计。

**典型接入方式**  
1. **作为 semantic‑release 插件**：在项目根目录的 `release.config.js`（或 `package.json`）中添加  
   ```js
   module.exports = {
     plugins: [
       ['@semantic-release/commit-analyzer'],
       ['@semantic-release/release-notes-generator'],
       // 其他插件如 npm、github 等
     ]
   };
   ```  
2. **CLI 使用**：在本地或 CI 环境直接运行 `semantic-release`，插件会在发布阶段自动调用生成发布说明。  
3. **自定义配置**：可通过插件选项覆盖默认的 `conventional-changelog` 预设，例如指定 `preset: 'angular'` 或自定义 `writerOpts`。

**生产可用性**  
- **活跃度高**：截至 2026‑05‑11 最近一次提交，拥有 362 Stars、51 Forks，且持续接受 PR 与 Issue。  
- **语言与生态**：使用 JavaScript 编写，兼容 Node.js 环境，已被多个大型开源项目和企业 CI 流水线采用。  
- **风险评估**：暂无重大许可证或安全漏洞报告，仍需在正式投产前完成许可证合规与安全审计。  
- **总体评估**：在满足合规审查后，可视为 **生产就绪** 的 OSS 组件，适合在任何需要自动化发布说明的项目中直接使用。

## 🧭 Practical evaluation

**Value:** semantic-release/release-notes-generator helps engineers save time in daily development and review loops.

**Best use cases**

- speed up developer workflows
- automate local engineering tasks
- improve CI feedback

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 362 GitHub stars
- 51 forks
- updated 2026-05-11
- primary language: JavaScript
- 7 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 43/100 |
| stars | 54/100 |
| topics | 88/100 |
| outlook | 78/100 |
| quality | 76/100 |
| recency | 100/100 |
| adoption | 51/100 |
| production | 77/100 |
| usefulness | 58/100 |
| integration | 62/100 |
| sourceTrust | 100/100 |

---

<sub>🔭 Discovered 2026-05-11 · [View on GitHub](https://github.com/semantic-release/release-notes-generator) · [← Back to DevTools](./README.md)</sub>
