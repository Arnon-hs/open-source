# NG-ZORRO/ng-zorro-antd

[![Stars](https://img.shields.io/github/stars/NG-ZORRO/ng-zorro-antd?style=flat-square&color=yellow)](https://github.com/NG-ZORRO/ng-zorro-antd/stargazers) [![Forks](https://img.shields.io/github/forks/NG-ZORRO/ng-zorro-antd?style=flat-square&color=blue)](https://github.com/NG-ZORRO/ng-zorro-antd/network) [![Language](https://img.shields.io/badge/lang-TypeScript-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-66%2F100-brightgreen?style=flat-square)](#)

> Angular UI Component Library based on Ant Design

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 9.2k |
| 🍴 **Forks** | 4.1k |
| 💻 **Language** | TypeScript |
| 📈 **Score** | 66/100 |
| 🗓️ **Last push** | 2026-09-05 |
| 🔍 **Source** | github |

## 🏷️ Topics

`angular` `angular-components` `angular-directives` `angular-ui-components` `ant` `ant-design` `antd` `enterprise` `frontend` `ivy` `ng-zorro` `ngx`

## 🎯 Categories

Frontend · Design

## 📝 Summary

### English

**Summary**  
NG‑ZORRO (ng-zorro-antd) is a mature Angular UI component library that implements Ant Design’s visual language, letting teams assemble polished, responsive interfaces with minimal custom CSS or JavaScript. With over 9 k stars, active maintenance, and a rich set of ready‑to‑use components, it is positioned as a high‑readiness OSS candidate for production use.

**Value**  
By providing a comprehensive catalog of pre‑styled, accessible components (tables, forms, charts, navigation, etc.), NG‑ZORRO dramatically cuts the time and effort required to build consistent user‑facing screens, reduces UI bugs, and enforces a unified design system across the product. This accelerates delivery, lowers frontend technical debt, and frees developers to focus on business logic rather than low‑level styling.

**Practical Adoption Path**  
1. **Proof of concept** – Scaffold a small feature or internal tool using NG‑ZORRO, following the README and example projects to validate compatibility with your Angular version and build pipeline.  
2. **Component audit** – Map the library’s components to your existing UI requirements, identify any gaps, and decide whether to extend or override styles.  
3. **Gradual migration** – Replace legacy UI pieces incrementally, starting with low‑risk modules, while keeping a fallback to custom components if needed.  
4. **CI/CD integration** – Add linting and version‑pinning (e.g., via package‑json lockfile) and monitor upstream releases for security patches.

**Production Readiness**  
NG‑ZORRO scores high on production readiness: recent commits (as of 2026‑06‑25), a large and active community, extensive TypeScript typings, and strong adoption in enterprise Angular projects. While the license (MIT) and security posture appear clean, a final review of any transitive dependencies and a routine vulnerability scan are recommended before committing to a full‑scale rollout.

### Русский

NG‑ZORRO (ng-zorro-antd) — это готовая к использованию библиотека UI‑компонентов для Angular, построенная на дизайне Ant Design, которая позволяет быстро создавать пользовательские интерфейсы без написания собственного кода стилей и компонентов. Для внедрения рекомендуется начать с небольшого proof‑of‑concept проекта, следуя README, чтобы оценить совместимость и настроить стили, а затем масштабировать использование компонентов в основных продуктах. Библиотека обладает высокой готовностью к production: активная поддержка, частые обновления, более 9 000 звёзд на GitHub и широкое принятие в сообществе, что делает её надёжным выбором для ускорения фронтенд‑доставки.

### 中文

**项目简介（2‑3 句）**  
NG‑ZORRO（ng-zorro-antd）是基于 Ant Design 规范的 Angular UI 组件库，提供 100+ 高质量、主题统一的前端组件。它通过遵循 Ant Design 的设计语言，让开发者在 Angular 项目中快速构建专业的企业级界面，极大减少自研 UI 的工作量。

**价值**  
- **提升开发效率**：可直接复用成熟的按钮、表单、表格、布局等组件，省去从零实现的时间。  
- **统一视觉体验**：所有组件遵循 Ant Design 视觉规范，保证产品 UI 风格一致。  
- **生态兼容**：基于 TypeScript 与 Angular 官方最佳实践，易于与 Angular CLI、RxJS、NgRx 等生态工具结合。

**典型接入方式**  
1. **安装**：`npm install ng-zorro-antd@latest`（或 `yarn add ng-zorro-antd`）。  
2. **全局引入**：在根模块 `AppModule` 中导入 `NgZorroAntdModule`（或按需导入单个组件模块），并在 `styles.css` 中加入 Ant Design 主题样式 `@import "~ng-zorro-antd/ng-zorro-antd.min.css";`。  
3. **按需加载**：配合 `ng-zorro-antd` 官方的 `ng-zorro-antd/cli` 或 `babel-plugin-import` 实现按需引入，减少打包体积。  
4. **配置国际化**：在根模块提供 `NZ_I18N`（如 `zh_CN`）以支持中文本地化。  

**生产可用性**  
- **活跃度高**：截至 2026‑06‑25，项目拥有 9,154+ 星、4,055+ Fork，最近一次提交在当天，说明维护活跃。  
- **成熟度**：已在多个大型企业内部和开源项目中使用，社区文档完整，提供完整的示例和迁移指南。  
- **风险**：暂无重大元数据风险，但仍需对许可证（MIT）和安全审计进行最终确认。总体而言，NG‑ZORRO 具备高生产就绪度，适合作为 Angular 前端项目的 UI 基础库进行试点或正式上线。

## 🧭 Practical evaluation

**Value:** NG-ZORRO/ng-zorro-antd helps ship user-facing interfaces with less custom UI work.

**Best use cases**

- build product UI faster
- reuse interface components
- improve frontend delivery

**Integration notes:** Looks feasible to evaluate, but integration should start with a small proof of concept and README check.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 9154 GitHub stars
- 4055 forks
- updated 2026-06-25
- primary language: TypeScript
- 14 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 90/100 |
| stars | 84/100 |
| topics | 100/100 |
| outlook | 78/100 |
| quality | 89/100 |
| recency | 80/100 |
| adoption | 86/100 |
| production | 75/100 |
| usefulness | 42/100 |
| integration | 46/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 200/100 |

---

<sub>🔭 Discovered 2026-06-25 · [View on GitHub](https://github.com/NG-ZORRO/ng-zorro-antd) · [← Back to Frontend](./README.md)</sub>
