# festoney8/bilibili-cleaner

[![Stars](https://img.shields.io/github/stars/festoney8/bilibili-cleaner?style=flat-square&color=yellow)](https://github.com/festoney8/bilibili-cleaner/stargazers) [![Forks](https://img.shields.io/github/forks/festoney8/bilibili-cleaner?style=flat-square&color=blue)](https://github.com/festoney8/bilibili-cleaner/network) [![Language](https://img.shields.io/badge/lang-TypeScript-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-60%2F100-brightgreen?style=flat-square)](#)

> bilibili 页面净化大师，深度净化 B 站，优化功能，过滤视频 / 评论 / 动态

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 848 |
| 🍴 **Forks** | 24 |
| 💻 **Language** | TypeScript |
| 📈 **Score** | 60/100 |
| 🗓️ **Last push** | 2026-05-11 |
| 🔍 **Source** | github |

## 🏷️ Topics

`bilibili` `greasemonkey` `greasyfork` `tampermonkey` `userscript` `violentmonkey`

## 🎯 Categories

Misc

## 📝 Summary

### English

**Brief Summary (2‑3 sentences)**  
Bilibili‑Cleaner is a TypeScript‑based browser extension that deeply sanitises B‑Station (bilibili) pages by filtering out unwanted videos, comments, and dynamic content, providing a cleaner, faster user experience. With over 800 GitHub stars and recent updates, it offers a ready‑made solution for anyone looking to declutter the bilibili UI without writing custom scripts.

**Value**  
- **User‑focused UX improvement** – removes noisy or irrelevant elements (ads, spam comments, repetitive recommendations) directly in the browser, making content consumption more efficient.  
- **Open‑source & extensible** – the codebase can be forked or customized to fit specific moderation policies or corporate branding guidelines.  
- **Low‑cost adoption** – no server‑side components are required; deployment is as simple as installing the extension or bundling it into an internal browser image.

**Practical Adoption Path**  
1. **Proof‑of‑Concept** – Clone the repo, run the TypeScript build, and test the extension in a local Chrome/Edge profile to verify that the filtering rules align with your workflow.  
2. **Readme & Config Review** – Confirm the documented configuration options (e.g., whitelist/blacklist patterns) and adjust them for your use case.  
3. **Pilot Deployment** – Package the built extension and distribute it to a small user group (e.g., a team of QA engineers) via your organisation’s extension management platform.  
4. **Feedback Loop** – Collect user feedback, tweak filters, and optionally contribute improvements back to the upstream project.  
5. **Scale‑out** – Once stable, roll the extension out to all relevant workstations or embed it in a custom Chromium build used internally.

**Production Readiness**  
- **Maturity**: Medium. The project is actively maintained (last commit 2026‑05‑11) and has a solid community signal (848 ★, 24 forks), but it lacks formal release tagging and extensive automated testing.  
- **Dependencies**: Pure TypeScript/JS with standard browser APIs, so integration risk is low; however, verify that any third‑party libraries used are up‑to‑date and have compatible licenses.  
- **Operational Considerations**: Since it runs client‑side, there are no server‑side scalability concerns, but you should monitor for breaking changes in bilibili’s DOM that could disable the filters.  
- **Security & Governance**: Perform a quick audit of the source for any external script injections or unsafe permissions, and confirm the license (MIT/Apache‑style) aligns with your policy.

Overall, Bilibili‑Cleaner is a practical, low‑overhead tool for internal prototypes or user‑facing deployments, provided you run a small validation phase and keep an eye on upstream updates.

### Русский

**bilibili-cleaner** – это open‑source расширение на TypeScript, которое глубоко «очищает» страницы B‑站, убирая рекламные блоки, нежелательные комментарии и лишние элементы ленты, тем самым ускоряя загрузку и улучшая пользовательский опыт. Типичный сценарий внедрения — подключить скрипт в виде пользовательского расширения или в рамках внутреннего веб‑инструмента, протестировать на небольшом наборе страниц и убедиться, что фильтры работают согласно требованиям. Уровень готовности — средний: проект активно поддерживается (обновление 2026‑05‑11, 848 звёзд), но перед запуском в продакшн рекомендуется проверить лицензию, провести аудит безопасности и обеспечить сопровождение зависимостей.

### 中文

**项目简介**  
`festoney8/bilibili-cleaner` 是一款基于 TypeScript 的 B 站页面净化插件，能够深度过滤视频、评论、动态等噪声信息，提升观看和交互体验。

**价值**  
- **去噪提升**：自动屏蔽广告、推荐垃圾、低质量评论等，让页面更干净、信息更聚焦。  
- **功能扩展**：提供可自定义的过滤规则和快捷键，支持一键开启/关闭，适配多种使用场景。  
- **社区认可**：已有 848+ ⭐、24+ 🍴，活跃度高，说明在 B 站用户群体中已有一定口碑。

**典型接入方式**  
1. **浏览器插件**：将仓库代码打包为 Chrome/Edge 扩展，直接在浏览器中加载。  
2. **脚本注入**：使用 Tampermonkey/Greasemonkey 脚本，将 `dist` 产物以用户脚本形式运行。  
3. **自建前端项目**：在自己的前端页面中通过 npm 安装 `bilibili-cleaner`，在页面加载后调用 `initCleaner()` 即可生效。  

**生产可用性**  
- **成熟度**：项目已更新至 2026‑05‑11，代码基于 TypeScript，类型安全，易于二次开发。  
- **依赖与维护**：依赖较少（主要是 DOM 操作库），但仍需自行审查许可证（MIT/Apache）以及潜在的安全漏洞。  
- **上线建议**：在内部或原型环境先进行小范围验证（如在测试账号上开启），确认过滤规则不影响核心功能后，再推广到正式环境。整体上属于 **中等成熟度**，适合作为内部工具或面向特定用户的产品功能实现。

## 🧭 Practical evaluation

**Value:** festoney8/bilibili-cleaner may be useful when its README and activity match a concrete workflow.

**Best use cases**

- Not enough metadata yet.

**Integration notes:** Looks feasible to evaluate, but integration should start with a small proof of concept and README check.

**Production readiness:** Medium: useful for prototypes or internal workflows, with dependency and maintenance checks before production.

**Quality signals**

- 848 GitHub stars
- 24 forks
- updated 2026-05-11
- primary language: TypeScript
- 6 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 35/100 |
| stars | 62/100 |
| topics | 75/100 |
| outlook | 75/100 |
| quality | 76/100 |
| recency | 100/100 |
| adoption | 55/100 |
| production | 75/100 |
| usefulness | 42/100 |
| integration | 46/100 |
| sourceTrust | 100/100 |

---

<sub>🔭 Discovered 2026-05-11 · [View on GitHub](https://github.com/festoney8/bilibili-cleaner) · [← Back to Misc](./README.md)</sub>
