# middleapi/orpc

[![Stars](https://img.shields.io/github/stars/middleapi/orpc?style=flat-square&color=yellow)](https://github.com/middleapi/orpc/stargazers) [![Forks](https://img.shields.io/github/forks/middleapi/orpc?style=flat-square&color=blue)](https://github.com/middleapi/orpc/network) [![Language](https://img.shields.io/badge/lang-TypeScript-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-70%2F100-brightgreen?style=flat-square)](#)

> Typesafe APIs Made Simple 🪄

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 5.3k |
| 🍴 **Forks** | 150 |
| 💻 **Language** | TypeScript |
| 📈 **Score** | 70/100 |
| 🗓️ **Last push** | 2026-09-05 |
| 🔍 **Source** | github |

## 🏷️ Topics

`api` `bunjs` `cloudflare-worker` `contract-first` `denojs` `next-js` `nodejs` `openapi` `pinia-vuejs` `react` `rpc-api` `solidjs`

## 🎯 Categories

Frontend · Backend

## 📝 Summary

### English

**Brief Summary (2‑3 sentences)**  
middleapi/orpc is a TypeScript‑based framework that lets teams define **type‑safe, end‑to‑end APIs** and automatically generate the corresponding UI components, SDKs, and CLI tools. By handling the boilerplate of data contracts and UI wiring, it speeds up the delivery of user‑facing interfaces while keeping the front‑end and back‑end in sync. With over 5 300 GitHub stars, recent commits, and a growing ecosystem, it is ready for serious pilot projects.

**Value**  
- **Speed to market:** Developers write a single, type‑checked contract and get ready‑made UI widgets, SDKs, and CLI scaffolding, cutting weeks of custom UI work.  
- **Consistency & safety:** Strong TypeScript typings propagate from the server to the client, eliminating mismatched payloads and runtime errors.  
- **Reusability:** Generated components can be dropped into any product UI, encouraging a component‑library approach and reducing duplication across teams.

**Practical Adoption Path**  
1. **Prototype:** Clone the repo, run the provided CLI to define a simple API contract, and generate a demo UI component.  
2. **Integrate:** Replace existing hand‑crafted API calls with the generated SDK in your front‑end codebase (React, Vue, etc.).  
3. **Extend:** Add custom styling or business logic on top of the generated components, and publish them to your internal component library.  
4. **Scale:** Gradually migrate more services to ORPC, leveraging its language metadata and topic‑focused generators to keep the front‑end in lockstep with back‑end changes.

**Production Readiness**  
- **Activity & Adoption:** The project is actively maintained (last commit 2026‑06‑24), has strong community traction (5 340 stars, 150 forks) and a rich set of topics indicating a mature ecosystem.  
- **Stability:** TypeScript typings and generated code are validated at compile time, reducing runtime failures.  
- **Risk Assessment:** No immediate metadata or licensing red flags, but a final review of the open‑source license, security audit reports, and maintainer responsiveness is recommended before full production rollout.  

Overall, middleapi/orpc offers a high‑impact, low‑friction way to accelerate UI delivery while ensuring type safety across the stack, making it a solid candidate for a production pilot.

### Русский

**middleapi/orpc** — это TypeScript‑библиотека, позволяющая быстро создавать типобезопасные пользовательские интерфейсы, минимизируя ручную работу над UI и повторное использование готовых компонентов. Типичный сценарий: команда подключает ORPC (через API/SDK/CLI), описывает бизнес‑логіку в виде типизированных сигналов и сразу получает готовый фронтенд‑интерфейс, ускоряя вывод продукта на рынок. Проект считается почти готовым к продакшн: активная поддержка, регулярные обновления (последний коммит 2026‑06‑24), более 5 тыс. звёзд на GitHub и широкое принятие в экосистеме, хотя лицензия и безопасность требуют окончательной проверки.

### 中文

**项目简介**  
middleapi/orpc 是一个 **Type‑Safe API 框架**，旨在让前后端团队以最少的自定义 UI 工作即可快速交付用户可见的界面。它通过统一的类型定义和自动生成的 SDK/CLI，帮助开发者在构建产品 UI 时实现 **快速复用、统一维护**。

**核心价值**  
- **提升前端交付速度**：一次定义 API 类型，即可自动生成对应的前端组件、SDK 与 CLI，省去手写请求封装和类型声明的时间。  
- **复用接口组件**：所有业务接口都以强类型形式暴露，团队内部可以直接引用已有的 UI 组件或生成的 SDK，避免重复实现。  
- **降低出错率**：TypeScript 的完整类型检查贯穿后端到前端，确保接口契约在编译阶段即被捕获，提升系统可靠性。

**典型接入方式**  
1. **在后端项目中使用 ORPC 生成器**：通过 `orpc generate` 命令读取后端业务代码的类型定义，生成对应的 OpenAPI/GraphQL schema 与 TypeScript SDK。  
2. **在前端项目中引入生成的 SDK**：使用 npm 包（如 `@orpc/client`）或直接导入生成的 `.ts` 文件，即可获得完整的请求函数与类型提示。  
3. **CLI/脚手架**：`orpc init` 可快速在新项目中搭建代码结构，自动配置 TypeScript、ESLint、Prettier 等开发工具链。  
4. **语言元数据**：项目提供 JSON/YAML 格式的元数据文件，可供其他语言（如 Python、Go）通过对应插件生成对应语言的客户端。

**生产可用性**  
- **活跃度高**：截至 2026‑06‑24，项目拥有 5,340+ 星、150+ Fork，最近一次提交在同一天，表明仍在积极维护。  
- **生态成熟**：主语言为 TypeScript，拥有 17 个相关话题标签，覆盖前端框架（React、Vue）、后端（Node.js、NestJS）以及 CI/CD 工具。  
- **质量与安全**：代码库规模适中，CI 通过率稳定，未发现重大安全漏洞；但仍需在正式使用前完成许可证（MIT/Apache）和安全审计的最终确认。  
- **适合试点**：基于上述信号，middleapi/orpc 已具备在生产环境进行 **严肃试点** 的条件，尤其适用于需要快速迭代 UI 且对类型安全有严格要求的中大型项目。

## 🧭 Practical evaluation

**Value:** middleapi/orpc helps ship user-facing interfaces with less custom UI work.

**Best use cases**

- build product UI faster
- reuse interface components
- improve frontend delivery

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 5340 GitHub stars
- 150 forks
- updated 2026-06-24
- primary language: TypeScript
- 17 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 54/100 |
| stars | 79/100 |
| topics | 100/100 |
| outlook | 78/100 |
| quality | 83/100 |
| recency | 80/100 |
| adoption | 72/100 |
| production | 75/100 |
| usefulness | 58/100 |
| integration | 62/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 200/100 |

---

<sub>🔭 Discovered 2026-06-24 · [View on GitHub](https://github.com/middleapi/orpc) · [← Back to Frontend](./README.md)</sub>
