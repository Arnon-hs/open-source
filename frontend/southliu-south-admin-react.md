# southliu/south-admin-react

[![Stars](https://img.shields.io/github/stars/southliu/south-admin-react?style=flat-square&color=yellow)](https://github.com/southliu/south-admin-react/stargazers) [![Forks](https://img.shields.io/github/forks/southliu/south-admin-react?style=flat-square&color=blue)](https://github.com/southliu/south-admin-react/network) [![Language](https://img.shields.io/badge/lang-TypeScript-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-57%2F100-brightgreen?style=flat-square)](#)

> React-Admin后台管理系统模版，React19、Vite7、Antd5、Unocss、Zustand、Keepalive、i18n国际化、动态菜单、适配手机端、虚拟表格组件等。

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 568 |
| 🍴 **Forks** | 104 |
| 💻 **Language** | TypeScript |
| 📈 **Score** | 57/100 |
| 🗓️ **Last push** | 2026-09-05 |
| 🔍 **Source** | github |

## 🏷️ Topics

`admin` `antd` `react` `typescript` `vite`

## 🎯 Categories

Frontend

## 📝 Summary

### English

**Brief Summary (2‑3 sentences)**  
South‑Admin‑React is a modern React‑Admin starter kit built with React 19, Vite 7, Ant Design 5, UnoCSS, Zustand, and a host of productivity features such as keep‑alive routing, i18n, dynamic menus, mobile‑responsive layouts, and a virtualized table component. The template aims to accelerate the creation of feature‑rich back‑office applications by providing a ready‑made, opinionated UI foundation that can be customized with minimal effort.  

**Value**  
- **Speed to market** – All the heavy lifting (routing, state management, theming, internationalization, responsive design, and virtualized data grids) is pre‑configured, letting developers focus on business logic rather than boiler‑plate UI code.  
- **Component reuse** – The library ships a curated set of Ant Design‑based components and utility hooks that can be reused across multiple internal tools or external products, ensuring visual consistency and reducing duplicated effort.  
- **Modern stack** – Leveraging Vite for fast dev server builds, UnoCSS for on‑demand utility‑first styling, and Zustand for lightweight global state keeps the bundle size low and the developer experience smooth.  

**Practical Adoption Path**  
1. **Proof‑of‑Concept (PoC)** – Clone the repo, run the Vite dev server, and replace the demo pages with a small internal feature to validate the build pipeline, theming, and i18n workflow.  
2. **Component Audit** – Review the provided UI components against your design system; extend or replace any that don’t meet brand guidelines.  
3. **Integration Layer** – Connect the built‑in Zustand store to your existing APIs (e.g., authentication, data services) and verify that the keep‑alive routing works with your session handling.  
4. **Gradual Migration** – Incrementally replace legacy admin pages with South‑Admin‑React screens, using the dynamic menu system to control feature toggles.  

**Production Readiness**  
- **Maturity** – With ~568 ★ and 104  forks, the project shows community interest, but it is still at a “medium” readiness level. The codebase is actively updated (last commit 2026‑06‑26) and written in TypeScript, which helps catch bugs early.  
- **Considerations before production**  
  - **License & security review** – Verify the repository’s license (likely MIT) and run a security audit of dependencies (Vite, Antd, UnoCSS, Zustand).  
  - **Maintenance** – Check the activity of core maintainers and the issue backlog; plan for a fork or internal maintenance if community support wanes.  
  - **Performance testing** – Benchmark the virtualized table and keep‑alive routes under realistic data loads for your use case.  
- **Fit** – Ideal for internal tools, prototypes, or new products where rapid UI delivery outweighs the need for a fully battle‑tested enterprise framework. With the above checks, it can be promoted to production for most front‑end workloads.

### Русский

**South‑Admin‑React** — это готовый шаблон админ‑панели на React 19 с Vite 7, Ant‑Design 5 и Unocss, включающий Zustand‑state‑менеджмент, keep‑alive, i18n, динамические меню, мобильную адаптацию и виртуальные таблицы. Он позволяет быстро собрать пользовательский интерфейс продукта, переиспользуя готовые компоненты и минимизируя кастомную UI‑работу; типичный путь внедрения — запуск небольшого proof‑of‑concept, проверка README и настройка меню под свои роуты. По готовности к продакшну проект находится на среднем уровне: подходит для прототипов и внутренних сервисов, но перед масштабным запуском требуется проверка лицензии, безопасности зависимостей и активности мейнтейнеров.

### 中文

**项目简介（2‑3 句）**  
`southliu/south-admin-react` 是基于 React 19、Vite 7、Ant Design 5 的后台管理系统模板，内置 Unocss、Zustand、KeepAlive、i18n 国际化、动态菜单、移动端适配以及虚拟化表格等实用功能，帮助开发者快速搭建功能完整、体验一致的管理后台。

**价值**  
- **加速 UI 开发**：提供开箱即用的页面布局、权限路由、国际化和响应式适配，省去大量重复的 UI 代码。  
- **统一技术栈**：使用最新的 React 19 + Vite 7 组合，配合 TypeScript、Antd5、Zustand 等主流库，便于团队统一规范和维护。  
- **提升可维护性**：组件化、状态管理和 KeepAlive 机制让页面切换更流畅，代码结构清晰，后期迭代成本低。  
- **灵活扩展**：支持自定义插件、动态菜单以及虚拟化表格，能够满足从小型内部工具到中大型企业后台的多种需求。

**典型接入方式**  
1. **克隆仓库或使用模板**：`git clone https://github.com/southliu/south-admin-react.git`，或在 GitHub 上直接点击 “Use this template”。  
2. **安装依赖**：`pnpm install`（推荐）或 `npm i` / `yarn`。  
3. **配置环境**：在根目录创建 `.env`（或 `.env.local`），填写后端 API、语言、主题等项目特有的变量。  
4. **启动开发环境**：`pnpm dev`（Vite 开发服务器默认运行在 `http://localhost:5173`），即可在浏览器中看到完整的后台框架。  
5. **按需裁剪**：在 `src/layouts`, `src/pages` 和 `src/store` 中删除或修改不需要的模块，添加自己的业务页面和接口即可完成一次完整的 PoC。  

**生产可用性**  
- **成熟度**：已有 568 Stars、104 Forks，活跃维护至 2026‑06‑26，代码基于 TypeScript，类型安全可靠。  
- **适用场景**：非常适合作为原型、内部工具或中小型企业后台的快速起步；对大型高并发业务仍需自行评估依赖的安全性、性能（如虚拟表格的分页策略）以及后端接口的容错。  
- **上线准备**：在生产环境中建议进行以下检查：  
  1. **依赖安全审计**：使用 `npm audit` 或 `pnpm audit` 确认无高危漏洞。  
  2. **构建压缩**：`pnpm build` 生成静态资源，配合 CDN 与 HTTP/2/3 加速。  
  3. **环境变量**：确保所有敏感信息（如 API 密钥）通过服务器端注入，避免泄露。  
  4. **监控与日志**：在前端加入错误上报（如 Sentry）和性能监控（如 Lighthouse CI）。  
- **总体评估**：在完成上述安全与性能校验后，项目具备 **中等** 生产可用性，能够支撑内部业务或对外发布的后台系统。  

> **一句话总结**：`south-admin-react` 为 React + Antd 生态提供了一个功能齐全、可直接投入使用的后台模板，帮助团队在几天内完成 UI 搭建并快速进入业务开发阶段，只要做好依赖审计和生产构建，即可安全上线。

## 🧭 Practical evaluation

**Value:** southliu/south-admin-react helps ship user-facing interfaces with less custom UI work.

**Best use cases**

- build product UI faster
- reuse interface components
- improve frontend delivery

**Integration notes:** Looks feasible to evaluate, but integration should start with a small proof of concept and README check.

**Production readiness:** Medium: useful for prototypes or internal workflows, with dependency and maintenance checks before production.

**Quality signals**

- 568 GitHub stars
- 104 forks
- updated 2026-06-26
- primary language: TypeScript
- 5 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 51/100 |
| stars | 59/100 |
| topics | 63/100 |
| outlook | 67/100 |
| quality | 70/100 |
| recency | 80/100 |
| adoption | 56/100 |
| production | 68/100 |
| usefulness | 42/100 |
| integration | 46/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 100/100 |

---

<sub>🔭 Discovered 2026-06-26 · [View on GitHub](https://github.com/southliu/south-admin-react) · [← Back to Frontend](./README.md)</sub>
