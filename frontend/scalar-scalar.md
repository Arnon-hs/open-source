# scalar/scalar

[![Stars](https://img.shields.io/github/stars/scalar/scalar?style=flat-square&color=yellow)](https://github.com/scalar/scalar/stargazers) [![Forks](https://img.shields.io/github/forks/scalar/scalar?style=flat-square&color=blue)](https://github.com/scalar/scalar/network) [![Language](https://img.shields.io/badge/lang-TypeScript-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-74%2F100-brightgreen?style=flat-square)](#)

> Scalar is an open-source API platform:　　　　　　　　　　　　　　　　　　　　　　　　　　　　　　　　　　　　　　　🌐 Modern REST API Client　　　　　　　　　　　　　　　　　　　　　　　　　　　　　　　　　　　　　　　　📖 Beautiful API References　　　　　　　　　　　　　　　　　　　　　　　　　　　　　　　　　　　　　　　　✨ 1st-Class OpenAPI/Swagger Support

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 15.4k |
| 🍴 **Forks** | 880 |
| 💻 **Language** | TypeScript |
| 📈 **Score** | 74/100 |
| 🗓️ **Last push** | 2026-08-24 |
| 🔍 **Source** | github |

## 🏷️ Topics

`api` `api-client` `docs` `http-client` `openapi` `openapi3` `reference` `rest-api` `swagger` `vue`

## 🎯 Categories

Frontend · Backend

## 📝 Summary

### English

**Brief Summary**  
Scalar is an open‑source API platform that combines a modern REST client, beautifully rendered API reference docs, and first‑class OpenAPI/Swagger support. Built in TypeScript, it lets teams ship user‑facing API interfaces with minimal custom UI work, speeding up product UI development and improving frontend delivery consistency.  

**Value**  
- **Rapid UI creation** – Pre‑styled, interactive API docs and client components replace hand‑crafted UI, cutting development time and reducing design debt.  
- **Consistency & reuse** – Because the same components render both the client console and the reference docs, teams get a single source of truth for API behavior across internal tools and external developer portals.  
- **Developer experience** – Integrated OpenAPI/Swagger handling means developers can import existing specs and instantly get a functional client and documentation site, lowering onboarding friction.  

**Practical Adoption Path**  
1. **Evaluate the spec** – Clone the repo, run the CLI (`npm i @scalar/api-client`) and point it at an existing OpenAPI definition to generate a local preview.  
2. **Prototype** – Embed the `<ScalarApiClient>` React component (or the vanilla JS bundle) into a sandbox or a feature branch of your product UI to test interaction and styling.  
3. **Integrate** – Replace custom API consoles or static docs with Scalar’s components, wiring authentication and request‑mutation hooks to your existing SDK/CLI.  
4. **Deploy** – Publish the built assets as part of your CI/CD pipeline; the package is published to npm and can be version‑locked like any other front‑end dependency.  

**Production Readiness**  
- **Activity & community** – Over 15 k GitHub stars, 880 forks, recent commits (as of 2026‑06‑25), and a vibrant TypeScript ecosystem indicate strong maintenance.  
- **Maturity** – Full OpenAPI/Swagger support, a stable CLI, and multiple integration examples show the project is beyond beta.  
- **Risk considerations** – While no major metadata or security red flags appear, a final review of the MIT‑style license, vulnerability scanning of dependencies, and confirmation of an active maintainer team are recommended before a full‑scale rollout.  

Overall, Scalar offers a high‑confidence, production‑ready foundation for teams that want to deliver polished API UIs quickly and with minimal custom code.

### Русский

Scalar — это открытая платформа API, предоставляющая современный REST‑клиент, красивую генерацию API‑документации и полноценную поддержку OpenAPI/Swagger, что позволяет быстро создавать пользовательские интерфейсы без написания собственного UI‑кода. Типичный сценарий — интеграция в продукт для ускоренного вывода UI‑компонентов и улучшения доставки фронтенда, используя готовый SDK/CLI и метаданные API. Проект имеет высокий уровень готовности к продакшн: активные коммиты, более 15 тыс. звёзд на GitHub, широкое принятие в сообществе и стабильную экосистему, хотя окончательная проверка лицензии и безопасности всё‑ещё требуется.

### 中文

**项目简介**  
Scalar（scalar/scalar）是一个开源的 API 平台，提供 **现代化的 REST API 客户端**、**美观的 API 文档**以及 **一流的 OpenAPI/Swagger 支持**，帮助开发团队快速构建面向用户的交互界面，省去大量自研 UI 工作。

**价值主张**  
- **加速产品 UI 开发**：直接使用内置的 API 客户端与文档组件，无需从头实现请求、错误处理和文档渲染。  
- **组件复用**：提供可嵌入的 React/TSX 组件库，团队可以在多个前端项目中复用同一套交互与展示逻辑。  
- **提升前端交付效率**：统一的 OpenAPI/Swagger 解析与渲染，使前后端约定保持同步，减少沟通成本和运行时错误。

**典型接入方式**  
1. **npm 安装**：`npm i @scalar/api-client @scalar/api-reference`（或使用 Yarn/PNPM）。  
2. **在 React 项目中引入**：  
   ```tsx
   import { ApiClient, ApiReference } from '@scalar/react';

   function App() {
     return (
       <>
         <ApiClient specUrl="https://api.example.com/openapi.json" />
         <ApiReference specUrl="https://api.example.com/openapi.json" />
       </>
     );
   }
   ```
3. **CLI/SDK**：Scalar 同时提供 `scalar-cli` 用于本地生成文档、验证 OpenAPI 文件以及生成 TypeScript SDK，适合 CI/CD 流程中自动化使用。  
4. **自定义主题**：通过 CSS‑in‑JS 或 Tailwind 配置主题变量，轻松匹配企业品牌视觉。

**生产可用性**  
- **活跃度**：截至 2026‑06‑25，仓库拥有 15,354 ⭐、880 🍴，最近一次提交仅几天前，表明项目维护频繁。  
- **技术成熟度**：核心使用 TypeScript 编写，提供完整的类型定义，适配现代前端框架（React、Vue、Svelte）。  
- **社区与生态**：10+ GitHub topics、多个公开案例和社区插件，已在数个 SaaS 产品中实际运行。  
- **风险**：目前未发现重大许可证或安全漏洞，但仍建议在正式投产前完成一次安全审计并确认维护者的响应时间。  

综合来看，Scalar 已具备 **高生产就绪度**，适合作为 UI 层与 OpenAPI 接口的桥梁，在内部或对外的 API 产品中快速落地。

## 🧭 Practical evaluation

**Value:** scalar/scalar helps ship user-facing interfaces with less custom UI work.

**Best use cases**

- build product UI faster
- reuse interface components
- improve frontend delivery

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 15354 GitHub stars
- 880 forks
- updated 2026-06-25
- primary language: TypeScript
- 10 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 74/100 |
| stars | 89/100 |
| topics | 100/100 |
| outlook | 70/100 |
| quality | 78/100 |
| recency | 40/100 |
| adoption | 85/100 |
| production | 66/100 |
| usefulness | 74/100 |
| integration | 78/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 200/100 |

---

<sub>🔭 Discovered 2026-06-25 · [View on GitHub](https://github.com/scalar/scalar) · [← Back to Frontend](./README.md)</sub>
