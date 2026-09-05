# conventional-changelog/commitlint

[![Stars](https://img.shields.io/github/stars/conventional-changelog/commitlint?style=flat-square&color=yellow)](https://github.com/conventional-changelog/commitlint/stargazers) [![Forks](https://img.shields.io/github/forks/conventional-changelog/commitlint?style=flat-square&color=blue)](https://github.com/conventional-changelog/commitlint/network) [![Language](https://img.shields.io/badge/lang-TypeScript-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-63%2F100-brightgreen?style=flat-square)](#)

> 📓 Lint commit messages

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 18.5k |
| 🍴 **Forks** | 965 |
| 💻 **Language** | TypeScript |
| 📈 **Score** | 63/100 |
| 🗓️ **Last push** | 2026-09-05 |
| 🔍 **Source** | github |

## 🏷️ Topics

`commit` `conventions` `git` `lint`

## 🎯 Categories

DevTools

## 📝 Summary

### English

**Brief Summary (2‑3 sentences)**  
conventional‑changelog/commitlint is a TypeScript‑based linter that enforces conventional commit message formats, helping teams keep commit histories clean and machine‑readable. With over 18 k stars and active maintenance, it is a mature OSS component that can be dropped into any JavaScript/TypeScript workflow to automate commit validation locally and in CI.  

**Value**  
- **Consistency & speed** – By catching malformed commit messages at the developer’s workstation, commitlint eliminates noisy PR comments and reduces back‑and‑forth during code review.  
- **Automation friendly** – It integrates with Git hooks (via Husky, lint‑staged, etc.) and CI pipelines, turning a manual best‑practice into a zero‑effort gate that improves traceability and changelog generation.  
- **Ecosystem alignment** – Works out‑of‑the‑box with popular tools such as conventional‑changelog, semantic‑release, and GitHub Actions, enabling end‑to‑end release automation.

**Practical Adoption Path**  
1. **Proof‑of‑concept** – Add `@commitlint/cli` and a minimal `commitlint.config.js` to a sandbox repo; run `npx commitlint --from=HEAD~1 --to=HEAD` to verify rule enforcement.  
2. **Local enforcement** – Wire the CLI into a pre‑commit hook using Husky (`husky add .husky/commit-msg 'npx --no-install commitlint --edit $1'`).  
3. **CI gate** – Add a step in the CI workflow (GitHub Actions, GitLab CI, etc.) that runs `commitlint` against the PR’s commits; fail the job on violations.  
4. **Documentation & onboarding** – Update the project README with the chosen commit style guide and provide a quick‑start script for new contributors.

**Production Readiness**  
- **High** – The project shows strong community adoption (18 k+ stars, ~1 k forks), recent updates (last commit on 2026‑05‑12), and a well‑maintained TypeScript codebase.  
- **Risk profile** – No major licensing or security red flags have been identified; however, a final review of the license (MIT) and a quick dependency audit are advisable before a full‑scale rollout.  
- **Pilot suitability** – Given its stability and low integration friction, commitlint is ready for a serious pilot in any JavaScript/TypeScript codebase, with the expectation that it will quickly pay off in reduced review cycles and more reliable release automation.

### Русский

**conventional-changelog/commitlint** — инструмент для автоматической проверки сообщений коммитов в соответствии с Conventional Commits, позволяющий сократить время на ревью и стандартизировать процесс разработки. Типичный сценарий внедрения: добавить `commitlint` в локальный workflow (pre‑commit hook) и в CI‑pipeline, чтобы сразу получать обратную связь о некорректных сообщениях и поддерживать единый стиль. Проект обладает высокой готовностью к production: активные обновления, более 185 тыс. звёзд, широкое принятие в сообществе и зрелый TypeScript‑код, требующий лишь небольшого пилотного теста и проверки README.

### 中文

**项目简介**  
`conventional-changelog/commitlint` 是一款基于 **Conventional Commits** 规范的提交信息校验工具，帮助团队在本地和 CI 环境中统一、自动化地检查 Git 提交信息的格式，从而提升代码审查效率和发布流程的可靠性。

**价值**  
- **提升开发效率**：在提交阶段即捕获不符合规范的消息，避免后续因不规范提交导致的回滚或额外人工修改。  
- **自动化工作流**：可与 Git hooks、CI（GitHub Actions、GitLab CI、Jenkins 等）以及 monorepo 管理工具（如 Lerna、Nx）无缝集成，实现“提交即校验”。  
- **改进 CI 反馈**：不合规的提交会直接在 CI 中报错，帮助团队快速定位并修正问题，保持主分支的提交历史整洁。

**典型接入方式**  
1. **本地 Git Hook**（推荐）  
   ```bash
   npm i -D @commitlint/{config-conventional,cli}
   echo "module.exports = {extends: ['@commitlint/config-conventional']}" > commitlint.config.js
   npx husky install
   npx husky add .husky/commit-msg 'npx --no-install commitlint --edit "$1"'
   ```
   - 通过 Husky 将 `commitlint` 挂到 `commit-msg` 钩子，实现每次 `git commit` 时自动校验。

2. **CI 中使用**  
   ```yaml
   # GitHub Actions 示例
   name: Lint Commit Messages
   on: [push, pull_request]
   jobs:
     commitlint:
       runs-on: ubuntu-latest
       steps:
         - uses: actions/checkout@v4
         - uses: actions/setup-node@v4
           with:
             node-version: '20'
         - run: npm ci
         - run: npx commitlint --from=${{ github.event.pull_request.base.sha }} --to=HEAD
   ```
   - 在 PR 或 push 触发时检查所有新提交，确保整个分支符合规范。

3. **与其他工具链结合**  
   - 与 **release-it**、**semantic-release**、**changesets** 等发布工具配合，可在生成 changelog 前保证提交信息的可解析性。  
   - 在 monorepo 中使用 `--scope` 参数或自定义配置，实现子包独立校验。

**生产可用性**  
- **活跃度**：截至 2026‑05‑12，项目仍在维护，最近一次提交就在当天；拥有 **18,521** 星、**965** Fork，社区活跃度高。  
- **技术成熟度**：基于 TypeScript 编写，提供完整的类型定义；官方维护的 `@commitlint/config-conventional` 已经是业界事实标准。  
- **生态兼容**：已被多数主流 CI 平台、Git Hook 管理工具（Husky、lefthook）以及发布流水线（semantic-release）所集成，文档清晰、示例丰富。  
- **风险**：目前未发现重大许可证或安全漏洞，但建议在正式投产前完成一次许可证合规审查，并在内部 CI 环境中跑一次完整的安全扫描（如 npm audit、OSSF Scorecard）。  

**结论**  
`conventional-changelog/commitlint` 在规范化提交信息、提升代码审查效率以及支撑自动化发布方面表现出色，具备 **高** 的生产就绪度。建议先在一个小型子项目或单独的 CI 流水线中进行 PoC（Proof‑of‑Concept），验证与现有工作流的兼容性后，再推广至全组织使用。

## 🧭 Practical evaluation

**Value:** conventional-changelog/commitlint helps engineers save time in daily development and review loops.

**Best use cases**

- speed up developer workflows
- automate local engineering tasks
- improve CI feedback

**Integration notes:** Looks feasible to evaluate, but integration should start with a small proof of concept and README check.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 18521 GitHub stars
- 965 forks
- updated 2026-05-12
- primary language: TypeScript
- 4 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 75/100 |
| stars | 91/100 |
| topics | 50/100 |
| outlook | 73/100 |
| quality | 81/100 |
| recency | 80/100 |
| adoption | 86/100 |
| production | 72/100 |
| usefulness | 42/100 |
| integration | 46/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 100/100 |

---

<sub>🔭 Discovered 2026-05-12 · [View on GitHub](https://github.com/conventional-changelog/commitlint) · [← Back to DevTools](./README.md)</sub>
