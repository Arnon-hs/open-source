# TanStack/query

[![Stars](https://img.shields.io/github/stars/TanStack/query?style=flat-square&color=yellow)](https://github.com/TanStack/query/stargazers) [![Forks](https://img.shields.io/github/forks/TanStack/query?style=flat-square&color=blue)](https://github.com/TanStack/query/network) [![Language](https://img.shields.io/badge/lang-TypeScript-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-59%2F100-brightgreen?style=flat-square)](#)

> 🤖 Powerful asynchronous state management, server-state utilities and data fetching for the web. TS/JS, React Query, Solid Query, Svelte Query and Vue Query.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 49.4k |
| 🍴 **Forks** | 3.8k |
| 💻 **Language** | TypeScript |
| 📈 **Score** | 59/100 |
| 🗓️ **Last push** | 2026-08-24 |
| 🔍 **Source** | github |

## 🏷️ Topics

`async` `cache` `data` `fetch` `graphql` `hooks` `query` `react` `rest` `solid` `stale` `stale-while-revalidate`

## 🎯 Categories

Frontend · Data

## 📝 Summary

### English

**Brief Summary (2‑3 sentences)**  
TanStack Query is a TypeScript‑first library that provides powerful asynchronous state‑management, server‑state utilities, and data‑fetching abstractions for modern web frameworks (React, Solid, Svelte, Vue). With over 49 k stars and active maintenance, it lets teams ship data‑driven UIs faster by handling caching, background refetching, pagination, and optimistic updates out of the box. The project is mature, widely adopted, and ready for production use after a small proof‑of‑concept integration.

**Value**  
- **Accelerated UI development** – developers no longer need to hand‑craft loading, error, caching, or stale‑data logic; TanStack Query supplies a declarative API that covers these concerns automatically.  
- **Consistent experience across frameworks** – the same core concepts work in React, Solid, Svelte, and Vue, enabling reusable patterns and reducing context‑switching for full‑stack teams.  
- **Improved performance & UX** – built‑in cache normalization, background refetching, and optimistic updates keep the UI responsive while minimizing network traffic.  

**Practical Adoption Path**  
1. **Proof of concept** – scaffold a small feature (e.g., a list with pagination) using the framework‑specific package (e.g., `@tanstack/react-query`). Follow the README to set up the `QueryClient` and a provider at the app root.  
2. **Incremental migration** – replace existing fetch‑and‑state code with `useQuery`/`useMutation` hooks, monitoring network calls and UI behavior.  
3. **Team enablement** – create internal wrapper utilities (e.g., a pre‑configured `queryClient`) and documentation that align with your coding standards.  
4. **Full‑scale rollout** – adopt across larger modules, leveraging advanced features like query invalidation, prefetching, and infinite scrolling as needed.  

**Production Readiness**  
- **Activity & community** – recent commits (as of 2026‑05‑12), a large contributor base, and a vibrant ecosystem of plugins and tutorials.  
- **Stability** – high star/fork count, semantic versioning, and extensive type definitions indicate a well‑tested codebase.  
- **Ecosystem fit** – supports major front‑end frameworks and integrates with popular dev tools (React DevTools, VS Code extensions).  
- **Risk profile** – no major licensing or security red flags identified, but a final review of the license (MIT) and any disclosed vulnerabilities is advisable before a production launch.  

Overall, TanStack Query is a battle‑tested, high‑quality OSS candidate that can be safely piloted with a modest proof‑of‑concept and then expanded to become the default data‑fetching layer for your web applications.

### Русский

**TanStack Query** — это кросс‑фреймворковый набор утилит для асинхронного управления серверным состоянием и получения данных (React, Solid, Svelte, Vue) на TypeScript/JavaScript, который позволяет быстро собрать пользовательский интерфейс, минимизируя написание кастомного кода. Рекомендуется начать интеграцию с небольшим proof‑of‑concept, проверив README и базовые запросы, а затем расширять покрытие на остальные части продукта. Проект обладает высокой готовностью к production: активные коммиты, более 49 тыс. звёзд на GitHub, широкое принятие в сообществе и стабильный набор функций, однако перед полномасштабным запуском следует окончательно проверить лицензию, безопасность и наличие активных мейнтейнеров.

### 中文

**项目简介**  
TanStack Query（原 React Query）是一套跨框架的异步状态管理与服务器数据获取库，提供 TypeScript/JavaScript 实现的 React Query、Solid Query、Svelte Query 与 Vue Query。它通过统一的缓存、自动重试、后台刷新等机制，让前端在处理服务器状态时既高效又可靠。

**价值主张**  
- **加速 UI 开发**：统一的查询/变更 API 把数据获取、缓存、同步等繁杂逻辑抽离，开发者只需关注业务 UI，显著缩短产品上线时间。  
- **提升代码复用**：同一套 Query 核心可在 React、Solid、Svelte、Vue 等项目中复用，降低团队学习成本和维护成本。  
- **改善前端交付**：内置的缓存失效、并发请求去重、自动重试等特性提升用户感知性能，减少后端负载。

**典型接入方式**  
1. **阅读官方 README**，确认当前框架（如 React）对应的子包（`@tanstack/react-query`）的安装与基本使用示例。  
2. **在项目根目录创建 QueryClient 并使用 Provider 包裹根组件**，例如 React 中：  
   ```tsx
   import { QueryClient, QueryClientProvider } from '@tanstack/react-query';
   const queryClient = new QueryClient();
   <QueryClientProvider client={queryClient}>
       <App />
   </QueryClientProvider>
   ```  
3. **在业务组件中使用 hooks（`useQuery`、`useMutation` 等）进行数据请求**，并通过 `queryKey` 与 `staleTime` 控制缓存策略。  
4. **先在一个小模块或页面做 PoC**，验证数据流、错误处理和缓存行为是否符合预期，再逐步推广到全局。

**生产可用性**  
- **活跃度高**：截至 2026‑05‑12，GitHub ★49 387、Fork 3 813，最近一次提交在当天，说明项目仍在积极维护。  
- **生态成熟**：官方提供四大框架的实现，配套的 DevTools、React‑Query‑Devtools 等工具已广泛使用。  
- **社区与企业采用**：多家大型互联网公司在生产环境中使用，社区问题响应及时。  
- **风险**：目前未发现重大许可证或安全漏洞，但仍建议在正式上线前完成许可证合规审查、SCA 安全扫描以及核心维护者的最新活跃度确认。

综上，TanStack Query 具备 **高生产就绪度**，适合作为前端数据层的标准化解决方案，建议先在低风险业务模块进行概念验证，验证通过后即可在全站推广。

## 🧭 Practical evaluation

**Value:** TanStack/query helps ship user-facing interfaces with less custom UI work.

**Best use cases**

- build product UI faster
- reuse interface components
- improve frontend delivery

**Integration notes:** Looks feasible to evaluate, but integration should start with a small proof of concept and README check.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 49387 GitHub stars
- 3813 forks
- updated 2026-05-12
- primary language: TypeScript
- 16 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 90/100 |
| stars | 100/100 |
| topics | 100/100 |
| outlook | 60/100 |
| quality | 79/100 |
| recency | 20/100 |
| adoption | 97/100 |
| production | 57/100 |
| usefulness | 42/100 |
| integration | 46/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 200/100 |

---

<sub>🔭 Discovered 2026-05-12 · [View on GitHub](https://github.com/TanStack/query) · [← Back to Frontend](./README.md)</sub>
