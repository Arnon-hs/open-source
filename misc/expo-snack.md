# expo/snack

[![Stars](https://img.shields.io/github/stars/expo/snack?style=flat-square&color=yellow)](https://github.com/expo/snack/stargazers) [![Forks](https://img.shields.io/github/forks/expo/snack?style=flat-square&color=blue)](https://github.com/expo/snack/network) [![Language](https://img.shields.io/badge/lang-TypeScript-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-49%2F100-brightgreen?style=flat-square)](#)

> Expo Snack lets you run Expo in the browser.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 510 |
| 🍴 **Forks** | 180 |
| 💻 **Language** | TypeScript |
| 📈 **Score** | 49/100 |
| 🗓️ **Last push** | 2026-08-24 |
| 🔍 **Source** | github |

## 🏷️ Topics

`expo` `expo-snack`

## 🎯 Categories

Misc

## 📝 Summary

### English

**Brief Summary (2‑3 sentences)**  
Expo Snack is an open‑source web‑based playground that lets developers write, preview, and share Expo React‑Native projects directly in the browser, without any local setup. With a modest 58 / 100 health score, it’s a handy tool for rapid prototyping, demos, and internal experimentation, especially when its README and recent activity align with your workflow.  

**Value**  
- **Zero‑install development** – developers can start coding instantly from any machine, which speeds up onboarding, hack‑days, and UI/UX proof‑of‑concepts.  
- **Live sharing** – generated URLs let teammates or stakeholders view and interact with the app in real time, simplifying feedback loops.  
- **Close alignment with the Expo ecosystem** – projects built in Snack can be exported to a full Expo CLI project, making the transition to production straightforward.  

**Practical Adoption Path**  
1. **Evaluate the README and demo** – confirm that the supported Expo SDK version matches your target.  
2. **Run a pilot** – create a small prototype in Snack, export it, and import it into a local Expo CLI repo to verify that the code and dependencies translate cleanly.  
3. **Security & licensing review** – check the MIT‑style license, scan the generated bundle for known vulnerabilities, and confirm that the maintainer’s recent commits (last update 2026‑06‑25) address any critical issues.  
4. **Integrate into workflow** – embed Snack URLs in issue tickets, design reviews, or CI pipelines for quick visual validation before committing code.  

**Production Readiness**  
- **Maturity**: Medium. The project is actively maintained (latest commit within days) and has a respectable community footprint (≈ 510 ★, 180 forks).  
- **Risks**: Sparse integration metadata means you’ll need manual checks for compatibility with your dependency stack and for any hidden security concerns.  
- **Recommendation**: Suitable for prototypes, internal tools, and as a front‑end sandbox; for production‑grade apps, use Snack for early iteration and then migrate the exported code to a fully version‑controlled Expo project where you can apply stricter testing, linting, and dependency management.

### Русский

**expo/snack** – это open‑source инструмент, позволяющий запускать проекты Expo прямо в браузере, что упрощает быстрые прототипы и внутренние демо без необходимости локальной установки. Его типичное внедрение — интеграция в CI/CD или воркфлоу разработки UI‑компонентов, где разработчики могут мгновенно проверять изменения и делиться ссылками на работающие примеры. Проект имеет средний уровень готовности к production: достаточный набор звёзд и форков, активные коммиты и поддержка TypeScript, но перед использованием в продакшене рекомендуется проверить лицензию, безопасность зависимостей и наличие активных мейнтейнеров.

### 中文

**项目简介（2‑3 句）**  
Expo Snack 是一个基于浏览器的在线编辑器，能够在无需本地环境的情况下直接运行和预览 Expo 应用。它让开发者只需打开网页即可编写、调试、分享 React Native 代码，特别适合快速原型、教学演示和协作讨论。

**价值**  
- **即开即用**：不需要安装 Xcode、Android Studio 或本地 Node 环境，打开页面即可编码并实时预览。  
- **低门槛协作**：生成的链接可直接分享，团队成员或学生可以在任何设备上查看和编辑同一个项目。  
- **快速原型**：适合验证 UI、交互或库兼容性，省去完整项目搭建的时间成本。

**典型接入方式**  
1. **直接使用官方页面**：访问 https://snack.expo.dev，创建或导入项目即可。  
2. **嵌入到自有平台**：通过 `@expo/snack-sdk`（或对应的 iframe）将 Snack 编辑器嵌入内部文档、教学系统或产品原型工具中。  
3. **CI/CD 与自动化**：利用 Snack 提供的 API（如 `snack-runtime`）在 CI 中运行单元测试或生成预览截图，实现“代码‑即‑预览”的工作流。  

**生产可用性**  
- **成熟度**：GitHub ★510、Fork ★180，最近一次更新在 2026‑06‑25，代码基于 TypeScript，社区活跃度中等。  
- **适用场景**：非常适合作为原型、内部工具或教学平台的前端编辑器；在正式产品中直接使用需评估以下因素：  
  - **依赖与维护**：检查 Snack 运行时依赖的 Expo 版本是否与项目的生产依赖保持一致。  
  - **安全与合规**：确认许可证（MIT）符合公司政策，并对运行在浏览器的代码进行 CSP、输入校验等安全加固。  
  - **可用性保障**：由于服务托管在 Expo 官方，需评估其 SLA 与故障恢复机制，或考虑自行部署私有化实例（目前官方未提供完整自托管方案）。  
- **结论**：在原型、内部协作或教学环境中可直接投入使用；若要在面向客户的生产系统中使用，建议在正式上线前进行安全审计、依赖锁定以及容错方案设计。

## 🧭 Practical evaluation

**Value:** expo/snack may be useful when its README and activity match a concrete workflow.

**Best use cases**

- Not enough metadata yet.

**Integration notes:** Needs manual inspection before adoption because integration signals are sparse in the discovered metadata.

**Production readiness:** Medium: useful for prototypes or internal workflows, with dependency and maintenance checks before production.

**Quality signals**

- 510 GitHub stars
- 180 forks
- updated 2026-06-25
- primary language: TypeScript
- 2 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 56/100 |
| stars | 58/100 |
| topics | 25/100 |
| outlook | 49/100 |
| quality | 55/100 |
| recency | 40/100 |
| adoption | 57/100 |
| production | 53/100 |
| usefulness | 42/100 |
| integration | 46/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 0/100 |

---

<sub>🔭 Discovered 2026-06-25 · [View on GitHub](https://github.com/expo/snack) · [← Back to Misc](./README.md)</sub>
