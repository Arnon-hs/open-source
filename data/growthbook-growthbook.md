# growthbook/growthbook

[![Stars](https://img.shields.io/github/stars/growthbook/growthbook?style=flat-square&color=yellow)](https://github.com/growthbook/growthbook/stargazers) [![Forks](https://img.shields.io/github/forks/growthbook/growthbook?style=flat-square&color=blue)](https://github.com/growthbook/growthbook/network) [![Language](https://img.shields.io/badge/lang-TypeScript-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-66%2F100-brightgreen?style=flat-square)](#)

> Open Source Feature Flags, Experimentation, and Product Analytics

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 7.9k |
| 🍴 **Forks** | 776 |
| 💻 **Language** | TypeScript |
| 📈 **Score** | 66/100 |
| 🗓️ **Last push** | 2026-08-24 |
| 🔍 **Source** | github |

## 🏷️ Topics

`ab-testing` `abtest` `abtesting` `analytics` `bigquery` `clickhouse` `continuous-delivery` `data-analysis` `data-engineering` `data-science` `databricks` `experimentation`

## 🎯 Categories

Data

## 📝 Summary

### English

**Brief Summary (2‑3 sentences)**  
GrowthBook is an open‑source platform that provides feature‑flag management, A/B testing, and product analytics in a single, TypeScript‑based codebase. It lets engineers toggle functionality, run experiments, and collect usage data without leaving their development workflow, thereby cutting the time spent on manual feature rollouts and post‑deployment validation. With strong community adoption (≈8 k stars, 776 forks) and active maintenance, it is ready for production pilots.

**Value**  
- **Accelerates developer workflows**: Feature flags and experiments can be defined, enabled, and monitored directly from code or the UI, eliminating the need for ad‑hoc scripts or separate analytics tools.  
- **Improves CI feedback loops**: Flags can be toggled per‑branch or per‑pipeline, allowing teams to test new behavior in CI without affecting production, which leads to faster, safer releases.  
- **Unified data**: Built‑in product analytics let you measure the impact of a flag or experiment in real time, reducing the overhead of integrating third‑party analytics solutions.

**Practical Adoption Path**  
1. **Evaluate the SDKs/CLI** – Clone the repo, run the Docker‑compose demo, and try the TypeScript/JavaScript SDK in a sandboxed service.  
2. **Integrate a flag** – Add the GrowthBook SDK to an existing microservice, define a flag in the GrowthBook UI, and gate a feature behind it.  
3. **Add an experiment** – Use the UI to create an A/B test, hook the experiment IDs into the code, and verify results via the built‑in analytics dashboard.  
4. **Roll out to CI** – Configure the CLI or environment variables to enable/disable flags per CI run, allowing automated tests to validate both variants.  
5. **Pilot in production** – Deploy the feature flag service alongside your existing stack, gradually expose the flag to a small user segment, and monitor performance and analytics before a full rollout.

**Production Readiness**  
- **Activity & Ecosystem**: Recent commits (as of 2026‑06‑25), a vibrant community (≈8 k stars, 20 topics), and multiple language SDKs indicate a healthy project.  
- **Stability**: The core is written in TypeScript with strong typing, and the repository includes CI pipelines, Docker images, and Helm charts for easy deployment.  
- **Risk Assessment**: No glaring licensing or security red flags have been identified, though a final review of the open‑source license and maintainer activity is recommended before mission‑critical use.  
Overall, GrowthBook meets the criteria for a serious production pilot and can be adopted incrementally with low friction.

### Русский

Growthbook — это open‑source платформа для feature‑flags, экспериментов и продуктовой аналитики, позволяющая инженерам автоматизировать рутинные задачи, ускорять CI‑feedback и ускорять цикл разработки и ревью. Типичный сценарий: команда подключает SDK/CLI к своему приложению, управляет флагами и A/B‑тестами из единой консоли и получает метрики в реальном времени, что упрощает выпуск новых функций и проверку гипотез. Проект имеет высокий уровень готовности к production: активные коммиты, более 7 тыс. звёзд на GitHub, широкая экосистема SDK, TypeScript‑база и сильные сигналы принятия, хотя лицензия и безопасность требуют окончательной проверки.

### 中文

**项目简介**  
GrowthBook（growthbook/growthbook）是一款开源的 Feature Flag、实验平台和产品分析工具，帮助团队在代码层面快速打开/关闭功能、进行 A/B 测试并实时监控关键业务指标。  

**价值**  
- **提升开发效率**：通过可视化的开关管理和实验框架，工程师可以在本地或 CI 中快速验证新功能，避免频繁的代码回滚和手动配置。  
- **加速评审与发布**：Feature Flag 让功能在代码合并后即可在特定用户或环境中灰度发布，评审过程更流畅，风险更可控。  
- **数据驱动决策**：内置的产品分析仪表盘直接关联实验结果与业务指标，帮助产品团队基于真实数据迭代。  

**典型接入方式**  
1. **SDK 集成**：GrowthBook 为多语言提供官方 SDK（JavaScript/TypeScript、Python、Go、Java、Ruby 等），在代码中调用 `client.isFeatureEnabled('flagKey')` 即可获取开关状态。  
2. **API/CLI**：通过 REST API 或 CLI 可以在 CI/CD 流程中查询或修改标识状态，实现自动化灰度发布和回滚。  
3. **前端插件**：在 React/Vue/Angular 等前端框架中使用对应的 UI 组件库，直接在页面上进行实验变量的切换和结果展示。  

**生产可用性**  
- **活跃度高**：截至 2026‑06‑25，项目拥有 7 924 星、776 Fork，最近一次提交在同日，社区活跃。  
- **技术成熟**：核心代码基于 TypeScript，拥有完整的类型定义和丰富的文档，易于在现有工程中引入。  
- **生态兼容**：提供完整的 API、CLI 与多语言 SDK，支持与常见 CI（GitHub Actions、GitLab CI）以及云平台（AWS、GCP、Azure）集成。  
- **风险可控**：暂无重大许可证或安全漏洞报告，仍需在正式投产前进行一次安全审计和维护者确认。  

综上所述，GrowthBook 具备高生产就绪度，适合作为功能开关与实验平台在企业级项目中快速落地。

## 🧭 Practical evaluation

**Value:** growthbook/growthbook helps engineers save time in daily development and review loops.

**Best use cases**

- speed up developer workflows
- automate local engineering tasks
- improve CI feedback

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 7924 GitHub stars
- 776 forks
- updated 2026-06-25
- primary language: TypeScript
- 20 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 72/100 |
| stars | 83/100 |
| topics | 100/100 |
| outlook | 66/100 |
| quality | 76/100 |
| recency | 40/100 |
| adoption | 80/100 |
| production | 63/100 |
| usefulness | 58/100 |
| integration | 62/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 100/100 |

---

<sub>🔭 Discovered 2026-06-25 · [View on GitHub](https://github.com/growthbook/growthbook) · [← Back to Data](./README.md)</sub>
