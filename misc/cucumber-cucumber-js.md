# cucumber/cucumber-js

[![Stars](https://img.shields.io/github/stars/cucumber/cucumber-js?style=flat-square&color=yellow)](https://github.com/cucumber/cucumber-js/stargazers) [![Forks](https://img.shields.io/github/forks/cucumber/cucumber-js?style=flat-square&color=blue)](https://github.com/cucumber/cucumber-js/network) [![Language](https://img.shields.io/badge/lang-TypeScript-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-64%2F100-brightgreen?style=flat-square)](#)

> Cucumber for JavaScript

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 5.3k |
| 🍴 **Forks** | 1.1k |
| 💻 **Language** | TypeScript |
| 📈 **Score** | 64/100 |
| 🗓️ **Last push** | 2026-05-14 |
| 🔍 **Source** | github |

## 🏷️ Topics

`cucumber` `javascript` `typescript`

## 🎯 Categories

Misc

## 📝 Summary

### English

**Summary**  
cucumber/cucumber‑js is the official JavaScript implementation of the Cucumber BDD framework, enabling developers to write executable specifications in Gherkin and run them against JavaScript codebases. With over 5 300 GitHub stars, more than 1 100 forks, recent commits (as of 2026‑05‑14), and a TypeScript codebase, it shows strong community adoption and active maintenance, making it a solid candidate for a production pilot.  

**Value** – It lets teams bridge the gap between business‑level requirements and automated tests, fostering shared understanding across product, QA, and development while reusing existing JavaScript tooling and CI pipelines.  

**Practical adoption path** – Start by reviewing the README and example projects, then spin up a small proof‑of‑concept repository that mirrors an existing feature‑file workflow. Integrate the `cucumber-js` CLI into your test runner (e.g., npm scripts, Jest, or a CI pipeline), map step definitions to your code, and iterate on the test suite while monitoring the project’s issue tracker for any security or licensing concerns.  

**Production readiness** – The project’s high star count, recent activity, and TypeScript foundation indicate maturity and stability; however, a final check of the license (MIT) and a quick security audit of dependencies is still required before full‑scale rollout. Once those checks pass, cucumber‑js can be considered production‑ready for serious BDD adoption.

### Русский

Cucumber‑JS — это официальная реализация BDD‑фреймворка Cucumber для JavaScript/TypeScript, позволяющая писать читаемые сценарии на Gherkin и автоматически выполнять их в тестовых пайплайнах. Он подходит для интеграции в проекты, где требуется связать бизнес‑требования с автотестами (например, UI‑тесты в Selenium/WebdriverIO или API‑тесты в Node.js), и может быть быстро включён в существующий workflow благодаря простому npm‑установочному процессу и поддержке популярных тест‑раннеров. По состоянию на 2026‑05‑14 проект считается готовым к production: активные коммиты, более 5 тыс. звёзд, широкое принятие в сообществе и стабильный TypeScript‑код, хотя перед внедрением следует проверить лицензию и текущие уязвимости.

### 中文

**项目简介（2‑3 句）**  
Cucumber‑JS 是 Cucumber 在 JavaScript/TypeScript 生态中的实现，提供基于 Gherkin 语法的行为驱动开发（BDD）框架，让业务人员和开发者可以用可读的自然语言编写可执行的验收测试。它与 Node.js、浏览器以及常见的测试运行器（如 Jest、Mocha）无缝集成，适用于前端、后端和全栈项目。

**价值**  
- **业务可读性**：使用 Gherkin 编写的特性文件（Feature）让非技术人员也能参与需求确认和验收。  
- **统一测试语言**：前后端团队可共享同一套 BDD 场景，降低沟通成本。  
- **生态兼容**：支持 TypeScript、ESM、CommonJS，且可与 Selenium、Playwright、Puppeteer 等自动化驱动配合，实现端到端 UI 测试。  

**典型接入方式**  
1. **安装**：`npm install @cucumber/cucumber --save-dev`（或 `yarn add -D @cucumber/cucumber`）。  
2. **编写特性文件**：在 `features/` 目录下使用 `.feature` 编写 Gherkin 场景。  
3. **实现 Step Definitions**：在 `step-definitions/` 中使用 TypeScript/JavaScript 编写对应的步骤实现，常配合 `@cucumber/cucumber` 提供的 `Given/When/Then` 接口。  
4. **运行**：在 `package.json` 中添加脚本，例如 `"test:bdd": "cucumber-js"`，或直接在 CI 中执行 `npx cucumber-js`.  
5. **集成 CI/CD**：将上述脚本加入 GitHub Actions、GitLab CI 等流水线，确保每次提交都执行 BDD 测试。  

**生产可用性**  
- **活跃维护**：截至 2026‑05‑14 最近一次提交，社区活跃，拥有 5.3k+ 星、1.1k+ Fork，且主要语言为 TypeScript，代码质量和类型安全都较高。  
- **成熟生态**：已被多个大型项目采用，兼容主流测试框架和浏览器自动化工具，具备完整的插件体系（如报告、并行执行）。  
- **风险**：暂无重大许可证或安全漏洞报告，但在正式落地前仍建议审查项目的 LICENSE（MIT）以及依赖的安全性。  

综上，cucumber/cucumber‑js 在功能完整性、社区活跃度和技术栈兼容性方面均已达到了生产级别，可作为企业级 BDD 测试的首选方案。

## 🧭 Practical evaluation

**Value:** cucumber/cucumber-js may be useful when its README and activity match a concrete workflow.

**Best use cases**

- Not enough metadata yet.

**Integration notes:** Needs manual inspection before adoption because integration signals are sparse in the discovered metadata.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 5321 GitHub stars
- 1107 forks
- updated 2026-05-14
- primary language: TypeScript
- 3 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 76/100 |
| stars | 79/100 |
| topics | 38/100 |
| outlook | 77/100 |
| quality | 81/100 |
| recency | 100/100 |
| adoption | 78/100 |
| production | 77/100 |
| usefulness | 42/100 |
| integration | 46/100 |
| sourceTrust | 100/100 |

---

<sub>🔭 Discovered 2026-05-14 · [View on GitHub](https://github.com/cucumber/cucumber-js) · [← Back to Misc](./README.md)</sub>
