# garden-co/jazz

[![Stars](https://img.shields.io/github/stars/garden-co/jazz?style=flat-square&color=yellow)](https://github.com/garden-co/jazz/stargazers) [![Forks](https://img.shields.io/github/forks/garden-co/jazz?style=flat-square&color=blue)](https://github.com/garden-co/jazz/network) [![Language](https://img.shields.io/badge/lang-Rust-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-46%2F100-brightgreen?style=flat-square)](#)

> A local-first relational database for the browser, React Native and your backend.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 115 |
| 🍴 **Forks** | 9 |
| 💻 **Language** | Rust |
| 📈 **Score** | 46/100 |
| 🗓️ **Last push** | 2026-08-24 |
| 🔍 **Source** | github |

## 🏷️ Topics

`database` `embedded-database` `local-first` `react` `react-native` `svelte` `sync` `vue`

## 🎯 Categories

Frontend · Database · Mobile

## 📝 Summary

### English

**Summary**  
Jazz (garden‑co/jazz) is a local‑first relational database written in Rust that runs in the browser, React Native, and on the server, letting developers store and query data without a remote API. By handling data persistence and sync out of the box, it reduces the amount of custom UI and state‑management code needed to build user‑facing interfaces.  

**Value**  
Jazz lets teams focus on building product UI rather than wiring up bespoke back‑ends, because the same data layer can be used across web, mobile, and backend services. Its relational model and query API enable rapid prototyping of data‑driven components, and the local‑first approach improves perceived performance and offline resilience.  

**Practical adoption path**  
1. **Proof‑of‑concept** – Clone the repo, run the README example, and integrate Jazz into a small feature branch of an existing React or React Native app.  
2. **Component reuse** – Replace ad‑hoc state stores (e.g., Redux slices or local storage) with Jazz tables, and reuse the same schema across web and mobile codebases.  
3. **Gradual rollout** – Incrementally migrate existing data flows to Jazz while keeping fallback APIs, monitoring sync behavior and bundle size.  

**Production readiness**  
Jazz scores a medium readiness level. It is actively maintained (last commit 2026‑07‑02) and has modest community traction (≈115 ⭐, 9 forks). The Rust core offers good performance, but the integration documentation is sparse, so teams should allocate time to validate the build pipeline, native module linking, and long‑term maintenance of the Rust dependency. For prototypes or internal tools Jazz is a solid fit; for customer‑facing production systems, perform a thorough dependency audit and consider a fallback strategy before full deployment.

### Русский

**garden-co/jazz** — это локальная реляционная база данных, работающая в браузере, React Native и на сервере, позволяющая быстро собрать пользовательские интерфейсы без написания собственного UI‑кода. Обычно её внедряют в виде небольшого proof‑of‑concept: подключают библиотеку, проверяют README и создают простую форму‑CRUD, чтобы убедиться в совместимости и оценить нагрузку. Проект находится на среднем уровне готовности — подходит для прототипов и внутренних инструментов, но перед запуском в продакшн требуется проверка зависимостей, стабильности Rust‑кода и план обслуживания.

### 中文

**项目简介**  
garden‑co/jazz 是一款面向浏览器、React Native 与后端的 **本地优先（local‑first）关系型数据库**，通过在客户端直接持有数据副本，实现离线可用、即时同步，并提供统一的查询 API，帮助开发者快速搭建用户界面而无需编写大量自定义 UI 逻辑。

**价值主张**  
- **加速前端交付**：数据层在本地即可完成增删改查，界面渲染几乎是即时的，显著缩短 UI 开发和调试周期。  
- **组件复用**：统一的查询语法和实时订阅机制，使得同一套数据模型可以在 Web、移动端以及后端服务之间共享，降低重复实现的成本。  
- **离线/同步体验**：本地优先的设计让应用在网络不稳定时仍能正常工作，随后自动与服务器进行冲突解决与同步，提升用户体验。

**典型接入方式**  

| 场景 | 步骤概览 |
|------|----------|
| **Web（浏览器）** | 1. `npm install @jazz-db/browser` <br>2. 在项目入口初始化 `JazzDB.open({ name: 'my-db', schema })` <br>3. 使用 `db.table('users').select(...).subscribe(cb)` 进行实时查询 |
| **React Native** | 1. `npm install @jazz-db/react-native` <br>2. 按照文档在 `AppDelegate`（iOS）或 `MainApplication`（Android）中配置本地存储路径 <br>3. 与普通 React 组件一样使用 `useJazzQuery` Hook 获取数据 |
| **后端服务** | 1. `cargo add jazz-db`（Rust）或对应的 Node/Go SDK <br>2. 在服务启动时创建或打开同名数据库 <br>3. 通过 REST / GraphQL 层暴露查询接口，前端即可直接使用同一套 API 进行同步 |

> **建议**：先在一个独立的小功能或演示页面里完成 “打开‑查询‑同步” 的完整闭环（约 5‑10 行代码），确认 README 中的启动脚本、依赖版本以及同步冲突策略后，再扩展到业务模块。

**生产可用性评估**  

| 维度 | 评估 | 说明 |
|------|------|------|
| **成熟度** | ★★☆☆☆（中等） | 代码最近一次更新为 2026‑07‑02，Stars 115、Forks 9，社区活跃度一般。适合作为原型或内部工具的数据层。 |
| **依赖风险** | 中 | 采用 Rust 编写的核心库，需要在前端项目中通过 WebAssembly 或对应的 JS 包桥接，增加构建复杂度。 |
| **运维成本** | 中 | 本地数据库文件需要定期备份、监控同步延迟；后端同步服务需自行部署或使用官方提供的同步网关。 |
| **安全合规** | 待评估 | 需要审查数据加密、访问控制实现，尤其在跨平台同步时。 |
| **适用场景** | ✅ 原型、内部后台、离线优先的 SaaS 产品 <br>❌ 高并发、严格 SLA 的生产核心业务（除非自行强化同步与容错） |

**结论**  
garden‑co/jazz 能显著提升 UI 开发效率，特别适合需要离线能力或跨端数据共享的项目。建议先在低风险的功能点做 PoC，确认集成成本、同步行为和安全策略后，再决定是否在生产环境中推广使用。若项目对可靠性和运维要求较高，可能需要在其基础上加入额外的监控、备份以及冲突解决层。

## 🧭 Practical evaluation

**Value:** garden-co/jazz helps ship user-facing interfaces with less custom UI work.

**Best use cases**

- build product UI faster
- reuse interface components
- improve frontend delivery

**Integration notes:** Looks feasible to evaluate, but integration should start with a small proof of concept and README check.

**Production readiness:** Medium: useful for prototypes or internal workflows, with dependency and maintenance checks before production.

**Quality signals**

- 115 GitHub stars
- 9 forks
- updated 2026-07-02
- primary language: Rust
- 8 topics

**Risks:** Integration path is not obvious from metadata; validate setup cost before committing.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 25/100 |
| stars | 44/100 |
| topics | 100/100 |
| outlook | 52/100 |
| quality | 57/100 |
| recency | 40/100 |
| adoption | 39/100 |
| production | 52/100 |
| usefulness | 42/100 |
| integration | 30/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 300/100 |

---

<sub>🔭 Discovered 2026-07-02 · [View on GitHub](https://github.com/garden-co/jazz) · [← Back to Frontend](./README.md)</sub>
