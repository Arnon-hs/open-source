# jasmine/jasmine-npm

[![Stars](https://img.shields.io/github/stars/jasmine/jasmine-npm?style=flat-square&color=yellow)](https://github.com/jasmine/jasmine-npm/stargazers) [![Forks](https://img.shields.io/github/forks/jasmine/jasmine-npm?style=flat-square&color=blue)](https://github.com/jasmine/jasmine-npm/network) [![Language](https://img.shields.io/badge/lang-JavaScript-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-44%2F100-brightgreen?style=flat-square)](#)

> A jasmine runner for node projects.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 379 |
| 🍴 **Forks** | 145 |
| 💻 **Language** | JavaScript |
| 📈 **Score** | 44/100 |
| 🗓️ **Last push** | 2026-08-24 |
| 🔍 **Source** | github |

## 🏷️ Topics

_no topics_

## 🎯 Categories

Misc

## 📝 Summary

### English

**Brief summary**  
`jasmine/jasmine-npm` is a Node‑compatible test runner that lets you execute Jasmine specs directly from the command line or as part of an npm script. With a modest star count (379) and recent activity (last updated 2026‑06‑27), it provides a familiar BDD testing experience for JavaScript projects that already rely on Jasmine.

**Value proposition**  
The package bundles the core Jasmine framework with a lightweight CLI, removing the need to set up a separate test harness or integrate Jasmine manually into a build pipeline. For teams that already write Jasmine specs, it offers a drop‑in way to run those tests in CI/CD, npm scripts, or local development without pulling in larger test runners like Jest or Mocha.

**Practical adoption path**  

1. **Evaluate the README** – Verify that the CLI options (`jasmine`, `jasmine init`, etc.) align with your current workflow (e.g., running `npm test`).  
2. **Add as a dev‑dependency**: `npm install --save-dev jasmine@latest`.  
3. **Initialize** the project with `npx jasmine init` to generate the default `spec` folder and configuration.  
4. **Integrate** the test command into your `package.json` scripts, e.g., `"test": "jasmine"`.  
5. **Run a pilot** on a small subset of specs to confirm that reporters, async handling, and any custom matchers work as expected.  

If your codebase already uses Jasmine, the switch is essentially zero‑cost; otherwise, you’ll need to migrate existing tests or adopt Jasmine conventions.

**Production readiness**  
- **Maturity**: Medium – the project is actively maintained (last commit June 2026) and has a healthy community signal (379 ★, 145 forks).  
- **Stability**: Suitable for prototypes, internal tools, or production services where Jasmine is the chosen testing framework, provided you perform a quick dependency audit (check for known vulnerabilities and ensure compatibility with your Node version).  
- **Risks**: The integration documentation is sparse, so you should allocate a brief validation sprint to confirm that custom reporters, coverage tools, or CI integrations (e.g., GitHub Actions) work without extra glue code. Once verified, the runner can be promoted to production with confidence.

### Русский

`jasmine/jasmine-npm` — это готовый к использованию раннер Jasmine для Node‑проекта, позволяющий запускать тесты Jasmine напрямую из npm‑скриптов без дополнительных обёрток. Он подходит для прототипов и внутренних CI‑конвейеров, где требуется простая интеграция тестов в существующий workflow; однако из‑за скудной документации и неочевидного пути настройки рекомендуется протестировать его в небольшом пилоте перед выводом в продакшн. При достаточном контроле зависимостей и проверке поддержки проекта (379 звёзд, активные форки, последнее обновление 2026‑06‑27) уровень готовности можно считать средним.

### 中文

**项目简介（2‑3 句话）**  
`jasmine/jasmine-npm` 是为 Node.js 项目提供的 Jasmine 测试运行器，帮助开发者在服务器端直接使用 Jasmine 编写、执行和报告单元测试。它保持了 Jasmine 的语法风格，同时通过 npm 包的形式便于在 CI/CD 流水线或本地开发环境中快速集成。

**价值**  
- **统一测试框架**：在前端和后端都使用 Jasmine，降低团队学习成本，代码风格保持一致。  
- **即插即用**：作为 npm 包发布，只需在 `package.json` 中添加依赖并在脚本中调用 `jasmine`，即可在 Node 环境下运行所有 spec。  
- **社区认可**：拥有 379 颗星和 145 次 fork，活跃度仍在（截至 2026‑06‑27）说明项目仍在维护，能够满足大多数常规测试需求。

**典型接入方式**  

| 步骤 | 操作 | 说明 |
|------|------|------|
| 1️⃣ 安装 | `npm install --save-dev jasmine`（或 `npm i -D jasmine`） | 将 Jasmine 及其 Node runner 加入开发依赖。 |
| 2️⃣ 初始化 | `npx jasmine init` | 在项目根目录生成 `spec` 目录、`jasmine.json` 配置文件以及示例 spec。 |
| 3️⃣ 编写测试 | 在 `spec/**/*.js` 中编写 `describe/it` 结构的测试代码。 | 与浏览器端 Jasmine 完全兼容。 |
| 4️⃣ 运行 | 在 `package.json` scripts 中加入 `"test": "jasmine"`，随后执行 `npm test`。 | 可配合 CI（GitHub Actions、GitLab CI 等）直接运行。 |
| 5️⃣ 高级配置（可选） | 在 `jasmine.json` 中配置 `helpers`、`spec_dir`、`spec_files`、`random`、`stopSpecOnExpectationFailure` 等。 | 满足自定义报告、覆盖率（配合 nyc/istanbul）等需求。 |

**生产可用性**  

- **成熟度**：Medium。项目已获得一定社区认可，且最近仍有更新（截至 2026‑06‑27），适合作为原型、内部工具或中小型服务的测试框架。  
- **依赖与维护**：依赖仅限 `jasmine-core` 与 Node 环境，无额外原生扩展，升级风险相对低。建议在引入前检查其 `package-lock.json` 中的子依赖是否仍在维护。  
- **集成成本**：元数据中未提供完整的 CI/CD 示例，需自行验证在现有构建流水线（如 Jenkins、GitHub Actions）中的运行方式。  
- **风险点**：  
  1. **集成路径不明确**：官方文档较简洁，若项目需要自定义 reporter、并行执行或与 TypeScript 深度集成，可能需要额外的包装或社区插件。  
  2. **维护频率**：虽然最近有提交，但仍需关注后续的 issue 与 PR 动态，防止出现安全漏洞或不兼容的更新。  

**结论**  
`jasmine/jasmine-npm` 适合作为 Node 项目快速上手的单元测试解决方案，尤其在团队已经使用 Jasmine 前端测试时可实现前后端统一。对于生产环境，建议在正式上线前进行一次完整的 CI 集成验证，并定期审计其依赖和社区活跃度，以确保长期可维护性。

## 🧭 Practical evaluation

**Value:** jasmine/jasmine-npm may be useful when its README and activity match a concrete workflow.

**Best use cases**

- Not enough metadata yet.

**Integration notes:** Needs manual inspection before adoption because integration signals are sparse in the discovered metadata.

**Production readiness:** Medium: useful for prototypes or internal workflows, with dependency and maintenance checks before production.

**Quality signals**

- 379 GitHub stars
- 145 forks
- updated 2026-06-27
- primary language: JavaScript

**Risks:** Integration path is not obvious from metadata; validate setup cost before committing.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 54/100 |
| stars | 55/100 |
| topics | 0/100 |
| outlook | 46/100 |
| quality | 50/100 |
| recency | 40/100 |
| adoption | 55/100 |
| production | 49/100 |
| usefulness | 42/100 |
| integration | 30/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 0/100 |

---

<sub>🔭 Discovered 2026-06-27 · [View on GitHub](https://github.com/jasmine/jasmine-npm) · [← Back to Misc](./README.md)</sub>
