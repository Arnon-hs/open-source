# posva/mande

[![Stars](https://img.shields.io/github/stars/posva/mande?style=flat-square&color=yellow)](https://github.com/posva/mande/stargazers) [![Forks](https://img.shields.io/github/forks/posva/mande?style=flat-square&color=blue)](https://github.com/posva/mande/network) [![Language](https://img.shields.io/badge/lang-TypeScript-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-73%2F100-brightgreen?style=flat-square)](#)

> 800 bytes modern wrapper around fetch with smart defaults

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 1.3k |
| 🍴 **Forks** | 44 |
| 💻 **Language** | TypeScript |
| 📈 **Score** | 73/100 |
| 🗓️ **Last push** | 2026-09-05 |
| 🔍 **Source** | github |

## 🏷️ Topics

`api` `browser` `esm` `fetch` `http-client` `typescript`

## 🎯 Categories

Networking · Backend

## 📝 Summary

### English

**Brief Summary (2‑3 sentences)**  
`posva/mande` is a lightweight (≈800 bytes) TypeScript wrapper around the native `fetch` API that ships with sensible defaults for headers, error handling, and request/response parsing. It lets teams standardize how they call internal services, reducing duplicated boiler‑plate and accelerating API‑service delivery. With strong community adoption (1.3 k ★, active maintenance) it’s ready for serious pilot use.

**Value**  
- **Reuse of infrastructure** – By encapsulating common concerns (JSON handling, timeout, auth headers, retry logic) in a single, well‑tested module, teams avoid re‑implementing the same fetch boiler‑plate across micro‑services.  
- **Consistency & standards** – All services that import `mande` inherit the same request conventions, making debugging, logging, and security policies (e.g., CSP, auth tokens) uniform across the codebase.  
- **Speed to market** – New API endpoints can be added with a one‑liner (`mande.get('/users')`) rather than wiring up a custom client, shrinking development cycles.

**Practical Adoption Path**  
1. **Evaluation** – Clone the repo, run the test suite, and try the provided CLI examples to confirm behavior matches your internal policies (e.g., header injection, error shapes).  
2. **Pilot** – Replace a single low‑risk service’s `fetch` calls with `mande` in a feature branch; monitor request/response logs for any regressions.  
3. **Roll‑out** – Once the pilot validates, create an internal wrapper (e.g., `src/lib/apiClient.ts`) that re‑exports `mande` with organization‑specific defaults (auth token provider, base URL).  
4. **Standardize** – Add the wrapper to your shared libraries monorepo, enforce its use via lint rules or code‑review checklists, and deprecate direct `fetch` usage.

**Production Readiness**  
- **Activity & community** – Updated as of 2026‑06‑29, 1.3 k ★, 44 forks, and active issue discussion indicate a healthy maintainer presence.  
- **Quality** – Written in TypeScript with built‑in type safety, modest bundle size, and no heavy runtime dependencies, making it easy to audit and bundle.  
- **Risk considerations** – No immediate licensing or critical security flags, but a final review of the MIT license compliance, any transitive dependencies, and a brief security audit is recommended before full production deployment.  

Overall, `posva/mande` offers a mature, low‑overhead solution for standardizing HTTP calls in TypeScript back‑ends and is suitable for a production pilot after the standard OSS due‑diligence steps.

### Русский

Проект posva/mande представляет собой современную обертку вокруг fetch с умными настройками по умолчанию, позволяющую командам повторно использовать инфраструктуру сервисов вместо того, чтобы заново создавать общие фрагменты бэкенда. Типовой сценарий использования posva/mande включает в себя быструю доставку API-сервисов, повторное использование инфраструктуры бэкенда и стандартизацию шаблонов сервисов. Проект имеет высокий уровень готовности к production, подтвержденный недавней активностью, широким внедрением и сильными сигналами экосистемы, что делает его достойным кандидатом для серьезного пилотного проекта.

### 中文

**项目简介**  
posva/mande 是一个仅 800 bytes 的现代化 fetch 包装库，提供智能默认配置，让前端/后端代码在调用 HTTP 接口时既简洁又可靠。它以 TypeScript 编写，保持极小体积的同时，内置错误处理、超时、重试等常用功能，帮助团队避免重复实现底层网络请求逻辑。

**价值**  
- **复用基础设施**：统一的请求层封装，使团队能够在多个服务之间共享同一套网络策略（如统一的 header、错误码处理、日志上报），减少重复代码。  
- **加速 API 开发**：开箱即用的默认配置让开发者专注业务逻辑，显著缩短后端 API 服务的交付周期。  
- **标准化服务模式**：通过统一的请求库，团队可以在代码审查、监控和安全审计时保持一致的实现规范。

**典型接入方式**  
```bash
npm i mande
```
```ts
import mande from 'mande';

const api = mande('/api/users');

api.get({ id: 123 })          // GET /api/users?id=123
   .then(data => console.log(data))
   .catch(err => console.error(err));
```
- 直接在前端项目或 Node.js 服务中 `import` 使用。  
- 支持自定义 `fetch` 实现、拦截器、超时、重试等选项，满足复杂业务需求。  
- 可配合 CI/CD、代码生成工具或自研 SDK 统一调用方式。

**生产可用性**  
- **活跃度**：截至 2026‑06‑29 最近一次提交，拥有 1 332 Stars、44 Forks，社区活跃。  
- **技术成熟度**：使用 TypeScript 编写，提供完整类型声明，易于在大型代码库中集成。  
- **安全与维护**：暂无已知重大安全漏洞，许可证为 MIT，适合商业使用；仍需在正式上线前确认维护者响应速度和依赖链安全。  
- **总体评估**：在 OSS 候选中属于高可用级别，适合作为内部或对外 API 的底层请求层进行试点或直接生产部署。

## 🧭 Practical evaluation

**Value:** posva/mande helps teams reuse service infrastructure instead of rebuilding common backend pieces.

**Best use cases**

- ship API services faster
- reuse backend infrastructure
- standardize service patterns

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 1332 GitHub stars
- 44 forks
- updated 2026-06-29
- primary language: TypeScript
- 6 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 41/100 |
| stars | 67/100 |
| topics | 75/100 |
| outlook | 75/100 |
| quality | 73/100 |
| recency | 80/100 |
| adoption | 59/100 |
| production | 74/100 |
| usefulness | 74/100 |
| integration | 78/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 200/100 |

---

<sub>🔭 Discovered 2026-06-29 · [View on GitHub](https://github.com/posva/mande) · [← Back to Networking](./README.md)</sub>
