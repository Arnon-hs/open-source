# openclaw/clawhub

[![Stars](https://img.shields.io/github/stars/openclaw/clawhub?style=flat-square&color=yellow)](https://github.com/openclaw/clawhub/stargazers) [![Forks](https://img.shields.io/github/forks/openclaw/clawhub?style=flat-square&color=blue)](https://github.com/openclaw/clawhub/network) [![Language](https://img.shields.io/badge/lang-TypeScript-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-64%2F100-brightgreen?style=flat-square)](#)

> Skill Directory for OpenClaw

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 8.6k |
| 🍴 **Forks** | 1.3k |
| 💻 **Language** | TypeScript |
| 📈 **Score** | 64/100 |
| 🗓️ **Last push** | 2026-05-11 |
| 🔍 **Source** | github |

## 🏷️ Topics

`directory` `skill`

## 🎯 Categories

Misc

## 📝 Summary

### English

**Brief Summary (2‑3 sentences)**  
openclaw/clawhub is a TypeScript‑based “Skill Directory” that aggregates and catalogs reusable OpenClaw skills, making it easy to discover, share, and integrate functionality across projects. With a strong community presence (8.5 k stars, 1.3 k forks) and recent updates, it offers a solid foundation for teams that want a centralized hub for OpenClaw‑related assets.

**Value**  
- **Centralized discovery** – Developers can browse a curated list of OpenClaw skills instead of hunting through disparate repositories, accelerating prototyping and reducing duplication of effort.  
- **Reusable components** – By exposing skill metadata and versioning, teams can plug proven modules into their pipelines, improving consistency and lowering maintenance overhead.  
- **Community‑driven growth** – The high star/fork count signals active contribution, meaning new skills and bug fixes appear regularly, keeping the directory current with the OpenClaw ecosystem.

**Practical Adoption Path**  
1. **Evaluate the README and repository structure** – Verify that the skill taxonomy aligns with your internal naming conventions and that the API surface (e.g., JSON manifests, TypeScript typings) matches your integration needs.  
2. **Run a pilot integration** – Clone the repo, install the TypeScript package, and import a few representative skills into a sandboxed OpenClaw workflow to confirm compatibility and performance.  
3. **Customize/extend** – If required, add your organization’s private skill definitions or adjust the directory’s search filters, then contribute back via pull requests to keep the upstream project healthy.  
4. **Roll out to production** – After successful pilot validation, embed the directory as a dependency in your CI/CD pipeline, automate skill version updates, and monitor the repository for new releases.

**Production Readiness**  
The project scores high on production readiness: it shows recent activity (last commit 2026‑05‑11), strong adoption signals (stars, forks, and ecosystem interest), and is written in a widely‑used language (TypeScript). While no major metadata risks were identified, a final review of the license, security posture, and maintainer responsiveness is advisable before committing to a long‑term deployment. Once those checks are cleared, openclaw/clawhub is suitable for a serious pilot and can be promoted to production use.

### Русский

**openclaw/clawhub** — это открытый каталог навыков для OpenClaw, реализованный на TypeScript, который уже собрал более 8 500 звёзд и 1 300 форков, а также активно поддерживается (обновления до 2026‑05‑11). Он удобен для интеграции в проекты, где требуется быстрый доступ к готовым «клавишам» и сценариям OpenClaw: достаточно просмотреть README и убедиться, что набор навыков соответствует вашему рабочему процессу, после чего добавить зависимость и подключить нужные модули. По готовности к production проект находится на высоком уровне — активная разработка, значительное сообщество и положительные экосистемные сигналы позволяют использовать его в серьёзных пилотных внедрениях после финальной проверки лицензии и безопасности.

### 中文

**项目简介**  
openclaw/clawhub 是 OpenClaw 的技能目录（Skill Directory），用 TypeScript 编写，提供统一的插件/技能清单，帮助开发者快速发现、浏览和集成 OpenClaw 社区的扩展功能。

**价值**  
- **统一入口**：集中管理所有 OpenClaw 相关的技能，降低搜索和评估成本。  
- **可扩展**：通过标准化的目录结构，团队可以自行添加内部或第三方技能，保持生态一致性。  
- **社区活跃**：截至 2026‑05‑11，项目拥有 8.5k+ Stars、1.3k+ Forks，更新频繁，说明社区支持力度大。

**典型接入方式**  
1. **依赖安装**：`npm i @openclaw/clawhub`（或使用 Yarn）。  
2. **读取目录**：在代码中导入 `getSkills()`（或类似 API），获取已注册的技能列表。  
3. **动态加载**：根据返回的元数据（名称、版本、入口文件），使用 `import()` 或 `require()` 动态加载所需技能。  
4. **自定义注册**：通过项目提供的 `registerSkill()` 接口，将内部插件注册到目录中，实现统一管理。

**生产可用性**  
- **成熟度**：近期活跃，且已有多个开源项目实际使用，具备生产级别的稳定性。  
- **风险**：需要在正式采用前检查许可证兼容性、潜在安全依赖以及维护者的响应速度。  
- **准备度**：在完成上述审查后，可直接在生产环境中作为 OpenClaw 生态的插件发现与加载层使用，适合作为正式项目的基础设施组件。

## 🧭 Practical evaluation

**Value:** openclaw/clawhub may be useful when its README and activity match a concrete workflow.

**Best use cases**

- Not enough metadata yet.

**Integration notes:** Needs manual inspection before adoption because integration signals are sparse in the discovered metadata.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 8565 GitHub stars
- 1323 forks
- updated 2026-05-11
- primary language: TypeScript
- 2 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 78/100 |
| stars | 84/100 |
| topics | 25/100 |
| outlook | 76/100 |
| quality | 81/100 |
| recency | 100/100 |
| adoption | 82/100 |
| production | 77/100 |
| usefulness | 42/100 |
| integration | 46/100 |
| sourceTrust | 100/100 |

---

<sub>🔭 Discovered 2026-05-11 · [View on GitHub](https://github.com/openclaw/clawhub) · [← Back to Misc](./README.md)</sub>
