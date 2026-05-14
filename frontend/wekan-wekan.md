# wekan/wekan

[![Stars](https://img.shields.io/github/stars/wekan/wekan?style=flat-square&color=yellow)](https://github.com/wekan/wekan/stargazers) [![Forks](https://img.shields.io/github/forks/wekan/wekan?style=flat-square&color=blue)](https://github.com/wekan/wekan/network) [![Language](https://img.shields.io/badge/lang-JavaScript-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-70%2F100-brightgreen?style=flat-square)](#)

> The Open Source kanban, built with Meteor. GitHub issues/PRs are only for FLOSS Developers, not for support, support is at https://wekan.fi/commercial-support/ . New English strings for new features at imports/i18n/data/en.i18n.json . Non-English translations at https://app.transifex.com/wekan/wekan only.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 20.9k |
| 🍴 **Forks** | 3k |
| 💻 **Language** | JavaScript |
| 📈 **Score** | 70/100 |
| 🗓️ **Last push** | 2026-05-13 |
| 🔍 **Source** | github |

## 🏷️ Topics

`docker-image` `foss` `javascript` `kanban` `meteor` `real-time` `sandstorm` `snapcraft` `wekan`

## 🎯 Categories

Frontend · DevTools · Data · Database · DevOps/Infra

## 📝 Summary

### English

**Brief Summary**  
Wekan is an open‑source Kanban board built with Meteor that lets teams create, organize, and track work items without writing custom UI code. It offers a ready‑made, component‑driven frontend, multilingual support via Transifex, and an extensible API/SDK for integration into larger products. The project is actively maintained (≈21 k stars, 3 k forks) and positioned for commercial support through the Wekan team.

**Value**  
- **Accelerated UI delivery** – By reusing Wekan’s pre‑built board, cards, and drag‑and‑drop components, developers can ship user‑facing interfaces far faster than building them from scratch.  
- **Component reuse** – The Meteor‑based codebase and exposed API/CLI let you embed the board in existing applications or extend it with custom widgets, reducing duplicated effort across products.  
- **Multilingual out‑of‑the‑box** – New English strings live in `imports/i18n/data/en.i18n.json`, while community translations are managed on Transifex, simplifying internationalization.

**Practical Adoption Path**  
1. **Evaluate** – Clone the repo, run the Meteor dev server, and explore the API/SDK documentation to confirm the required integration points (REST API, Webhooks, or direct component import).  
2. **Prototype** – Embed a Wekan board in a sandboxed feature branch of your product, replace default data sources with your own backend, and test multilingual UI using the provided i18n files.  
3. **Secure** – Conduct a quick security audit (dependency scanning, license check) and, if needed, engage the commercial support channel for a formal SLA.  
4. **Deploy** – Package the Meteor app with Docker or your preferred PaaS, configure persistence (MongoDB) and SSL, then roll out to a staging environment before production.

**Production Readiness**  
Wekan scores high on readiness: it has recent commits (as of 2026‑05‑13), a large and active community, and strong ecosystem signals (issues/PRs limited to FLOSS contributors, commercial support available). The codebase is mature (JavaScript/Meteor), well‑documented, and already used in many production deployments. While final checks on licensing compliance and security posture are still required, the project is considered a solid candidate for a serious pilot or full production rollout.

### Русский

Wekan — это открытая kanban‑платформа на Meteor, позволяющая быстро собрать пользовательский интерфейс без написания собственного UI‑кода, используя готовые компоненты и API/SDK для интеграции. Она подходит для команд, которым нужно ускорить вывод продукта на рынок, переиспользовать визуальные элементы и упростить доставку фронтенда. Проект имеет высокий уровень готовности к продакшн: активные коммиты, более 20 тыс. звёзд на GitHub, широкую экосистему и коммерческую поддержку, что делает его надёжным выбором для пилотных внедрений.

### 中文

**项目简介**  
Wekan 是一款基于 Meteor 的开源看板工具，提供类似 Trello 的可视化任务管理界面。它的代码完全开放，社区负责功能开发，商业支持则通过 https://wekan.fi/commercial-support/ 提供。

**价值**  
- **快速交付前端 UI**：内置完整的看板、卡片、拖拽等交互组件，开发者无需从零实现，可直接嵌入或二次定制。  
- **复用成熟界面**：通过 API/SDK 可以在自有系统中复用 Wekan 的界面和业务逻辑，加速产品 UI 的迭代。  
- **多语言支持**：默认提供英文字符串，社区翻译覆盖多语言，便于国际化项目快速上线。

**典型接入方式**  
1. **作为独立服务部署**：使用 Docker 镜像或源码自行部署，提供完整的 REST/GraphQL API，前端通过 HTTP 调用即可。  
2. **嵌入式组件**：利用公开的 JavaScript SDK，将看板 UI 直接嵌入已有的单页应用，配合自定义插件实现业务特化。  
3. **CLI/脚本集成**：通过提供的 CLI 工具进行数据导入/导出、自动化迁移等 DevOps 场景。

**生产可用性**  
- **活跃度高**：20922 星、2972 叉，最近一次提交在 2026‑05‑13，社区活跃，问题响应及时。  
- **技术成熟**：基于 Meteor 的全栈框架，提供完整的后端 API 与前端组件，已有多家企业在生产环境使用。  
- **风险可控**：目前未发现重大许可证或安全漏洞，仍建议在正式上线前进行一次安全审计并确认维护者的响应能力。  

综合来看，Wekan 具备较高的生产就绪度，适合作为内部工具或对外产品的看板模块快速落地。

## 🧭 Practical evaluation

**Value:** wekan/wekan helps ship user-facing interfaces with less custom UI work.

**Best use cases**

- build product UI faster
- reuse interface components
- improve frontend delivery

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 20922 GitHub stars
- 2972 forks
- updated 2026-05-13
- primary language: JavaScript
- 9 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 87/100 |
| stars | 92/100 |
| topics | 100/100 |
| outlook | 86/100 |
| quality | 96/100 |
| recency | 100/100 |
| adoption | 91/100 |
| production | 82/100 |
| usefulness | 42/100 |
| integration | 46/100 |
| sourceTrust | 100/100 |

---

<sub>🔭 Discovered 2026-05-13 · [View on GitHub](https://github.com/wekan/wekan) · [← Back to Frontend](./README.md)</sub>
