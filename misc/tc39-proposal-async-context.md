# tc39/proposal-async-context

[![Stars](https://img.shields.io/github/stars/tc39/proposal-async-context?style=flat-square&color=yellow)](https://github.com/tc39/proposal-async-context/stargazers) [![Forks](https://img.shields.io/github/forks/tc39/proposal-async-context?style=flat-square&color=blue)](https://github.com/tc39/proposal-async-context/network) [![Language](https://img.shields.io/badge/lang-Unknown-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-36%2F100-brightgreen?style=flat-square)](#)

> Discovered from Lobsters: proposal-async-context: Async Context for JavaScript

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | — |
| 🍴 **Forks** | — |
| 💻 **Language** | Unknown |
| 📈 **Score** | 36/100 |
| 🗓️ **Last push** | 2026-09-05 |
| 🔍 **Source** | lobsters |

## 🏷️ Topics

`lobsters`

## 🎯 Categories

Misc

## 📝 Summary

### English

**Brief Summary**  
`proposal-async-context` is an open‑source library that brings an “async‑local storage”‑style API to JavaScript, allowing developers to attach and retrieve contextual data across asynchronous call chains without manually threading it through function arguments. Although still a proposal‑stage implementation, the project is actively maintained (last update 2026‑07‑02) and may be handy for prototypes or internal tooling that need request‑scoped state (e.g., tracing, logging, or feature flags).

**Value**  
- **Cleaner code** – eliminates boilerplate for passing context objects through callbacks, promises, and async/await flows.  
- **Consistent tracing** – enables request‑level identifiers to be automatically available in any async task, which is useful for logging, metrics, and distributed tracing.  
- **Low‑overhead API** – mirrors the familiar Node.js `AsyncLocalStorage` interface, so existing code can adopt it with minimal changes.

**Practical Adoption Path**  
1. **Evaluate Fit** – Review the README, license, and issue tracker to confirm the API meets your use case (e.g., request‑scoped data, correlation IDs).  
2. **Prototype** – Add the package to a sandbox or a non‑critical micro‑service, wrap a few entry points with `AsyncContext.run()` and verify that context propagates through your async code (promises, `setTimeout`, event emitters, etc.).  
3. **Testing & Linting** – Write unit tests that assert context is preserved across typical async patterns; integrate with your CI pipeline to catch regressions.  
4. **Safety Checks** – Ensure the library’s dependencies are actively maintained, the license is compatible with your project, and there are no open security issues.  
5. **Gradual Rollout** – If the prototype succeeds, enable the library in a staged deployment (e.g., canary or feature flag) before rolling it out to the full production fleet.

**Production Readiness**  
- **Maturity**: Medium. The codebase is recent and appears maintained, but as a proposal‑level library it lacks the long‑term stability guarantees of a finalized ECMAScript feature.  
- **Risk**: Limited quality signals (few topics, sparse documentation, and unknown release cadence) mean you should perform due‑diligence on licensing, security, and community activity.  
- **Recommendation**: Suitable for internal services, prototypes, or as a stepping stone until a native async‑context API lands in the JavaScript runtime. For critical production systems, pair it with robust monitoring and be prepared to replace it if the proposal evolves or is abandoned.

### Русский

Резюме проекта "proposal-async-context: Async Context for JavaScript":

"Проект proposal-async-context предлагает решение для работы с асинхронным контекстом в JavaScript, что может быть полезно в определенных сценариях, когда требуется интеграция с конкретным workflow. Внедрение проекта возможно в прототипах или внутренних рабочих процессах, но требует тщательного осмотра и проверки лицензии, поддержки, документации, проблем и графика выпусков. Проект расчитан на средний уровень готовности к production."

### 中文

**项目简介**  
`proposal-async-context` 为 JavaScript 提供了一个实验性的 **异步上下文（Async Context）** API，旨在让开发者能够在跨异步边界（如 `Promise`、`async/await`、事件回调）之间安全、透明地传递状态或元数据。该提案目前仍在讨论阶段，代码仓库更新至 2026‑07‑02，社区关注度不高，仅有 1 条主题讨论。

---

### 价值点
1. **跨异步链路的上下文传播**：无需手动把对象作为参数层层传递，类似于 Node.js 的 `AsyncLocalStorage`，但目标是成为跨平台、标准化的语言特性。  
2. **简化日志、追踪、事务等场景**：在微服务或前端复杂交互中，可统一在同一 async context 中记录请求 ID、用户信息等元数据，提升调试和监控效率。  
3. **原型与内部工具快速实现**：对需要实验性异步上下文的原型或内部脚本，直接引入该库可省去自行实现类似机制的工作量。

### 典型接入方式
1. **安装**（若已发布 npm 包）  
   ```bash
   npm install proposal-async-context
   ```
2. **在代码中创建并使用 Context**  
   ```js
   import { AsyncContext } from 'proposal-async-context';

   const ctx = new AsyncContext();

   async function handler(req) {
     // 在当前异步链路里设置上下文值
     ctx.run({ requestId: req.id }, async () => {
       await doSomething();          // 任何后续的 async 调用都能读取到 requestId
     });
   }

   // 读取上下文
   function log(msg) {
     const { requestId } = ctx.get();
     console.log(`[${requestId}] ${msg}`);
   }
   ```
3. **与已有框架结合**  
   - **Node.js**：可在 Express/Koa 中间件里 `ctx.run(...)`，后续的业务代码无需显式传递 `req`。  
   - **前端**：在 React、Vue 等框架的根组件或页面入口处创建 context，子组件的异步请求自动共享同一上下文。  

> **注意**：如果项目尚未发布正式 npm 包，可能需要直接克隆仓库并通过 `npm link` 或本地路径引用。

### 生产可用性评估
- **成熟度**：提案仍处于 **Stage 2/3**（取决于最新进度），未进入正式 ECMAScript 标准。社区实现仅有单一仓库，活跃度低。  
- **风险**：  
  - API 可能在后续提案阶段发生破坏性变更。  
  - 兼容性依赖运行时（Node、浏览器）实现情况，部分旧版环境可能不支持。  
  - 文档、issue 及发布节奏有限，需自行评估维护成本。  
- **适用场景**：  
  - **原型开发、内部工具**：快速验证异步上下文概念。  
  - **受控的微服务或前端子系统**：在明确的技术栈和 Node 版本（≥14）下使用，并配合版本锁定。  
- **不建议直接用于关键生产系统**，除非能够接受潜在的 API 变更并自行承担兼容层的实现工作。

**结论**：`proposal-async-context` 为跨异步链路传递状态提供了便利的抽象，适合作为概念验证或内部项目的实验性依赖。若计划在生产环境使用，建议先在内部环境进行充分测试，并做好未来迁移到标准化实现（如 Node.js 原生 `AsyncLocalStorage`）的预案。

## 🧭 Practical evaluation

**Value:** proposal-async-context: Async Context for JavaScript may be useful when its README and activity match a concrete workflow.

**Best use cases**

- Not enough metadata yet.

**Integration notes:** Needs manual inspection before adoption because integration signals are sparse in the discovered metadata.

**Production readiness:** Medium: useful for prototypes or internal workflows, with dependency and maintenance checks before production.

**Quality signals**

- updated 2026-07-02
- 1 topics

**Risks:** Quality signals are limited; verify license, maintenance, docs, issues, and release cadence before using it.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 0/100 |
| stars | 0/100 |
| topics | 13/100 |
| outlook | 45/100 |
| quality | 32/100 |
| recency | 80/100 |
| adoption | 0/100 |
| production | 49/100 |
| usefulness | 42/100 |
| integration | 30/100 |
| sourceTrust | 70/100 |
| categoryMatchCount | 0/100 |

---

<sub>🔭 Discovered 2026-07-03 · [View on GitHub](https://github.com/tc39/proposal-async-context) · [← Back to Misc](./README.md)</sub>
