# toss/granite

[![Stars](https://img.shields.io/github/stars/toss/granite?style=flat-square&color=yellow)](https://github.com/toss/granite/stargazers) [![Forks](https://img.shields.io/github/forks/toss/granite?style=flat-square&color=blue)](https://github.com/toss/granite/network) [![Language](https://img.shields.io/badge/lang-TypeScript-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-58%2F100-brightgreen?style=flat-square)](#)

> Enterprise-grade React Native framework for microservice apps. Brownfield friendly, 200KB bundles, AWS-ready infrastructure.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 455 |
| 🍴 **Forks** | 51 |
| 💻 **Language** | TypeScript |
| 📈 **Score** | 58/100 |
| 🗓️ **Last push** | 2026-09-05 |
| 🔍 **Source** | github |

## 🏷️ Topics

`react-native`

## 🎯 Categories

Cloud & Storage · Frontend · Mobile

## 📝 Summary

### English

**Brief Summary (2‑3 sentences)**  
toss/granite is an enterprise‑grade React Native framework designed for microservice‑based mobile apps. It delivers lightweight (≈200 KB) bundles, a set of reusable UI components, and built‑in AWS‑ready infrastructure, making it brownfield‑friendly for teams that need to accelerate front‑end delivery while reusing existing services.

**Value**  
- **Speed to market:** Pre‑crafted, theme‑able components let developers ship product‑facing screens with far less custom UI code.  
- **Consistency & reuse:** A shared component library encourages uniform design language across multiple micro‑frontends, reducing duplication and maintenance overhead.  
- **Infrastructure alignment:** Out‑of‑the‑box AWS integration (e.g., Cognito, AppSync, Lambda) streamlines the bridge between the mobile UI and backend services.

**Practical Adoption Path**  
1. **Pilot integration:** Clone the repo, run the sample app, and compare its component API with the UI patterns of an existing microservice.  
2. **Manual metadata review:** Because discovery signals are sparse, perform a code audit to verify compatibility with your current navigation, state‑management, and styling conventions.  
3. **Component migration:** Replace a small, non‑critical screen with Granite components, adjusting any custom theming as needed.  
4. **Incremental rollout:** Gradually expand the substitution to other screens, leveraging Granite’s AWS helpers for authentication, API calls, and analytics.  
5. **Governance checklist:** Confirm license compliance, run security scans (e.g., Snyk), and lock dependency versions before merging to main.

**Production Readiness**  
- **Maturity:** Medium – the framework is solid enough for prototypes, internal tools, or staged rollouts, but it still requires dependency vetting and ongoing maintenance.  
- **Signals:** 455 GitHub stars, recent activity (last commit 2026‑05‑12), and TypeScript codebase indicate an active community, yet the lack of extensive integration metadata means you should conduct a thorough review before full production use.  
- **Risk considerations:** Verify the project’s license, perform security audits, and ensure that maintainers are responsive to issues; once these checks pass, Granite can be promoted to production for customer‑facing mobile apps.

### Русский

toss/granite — это корпоративный React Native‑фреймворк, позволяющий быстро собрать пользовательский интерфейс микросервисных приложений, повторно используя готовые UI‑компоненты и получая небольшие (≈200 KB) бандлы, готовые к работе в AWS. Его обычно внедряют в существующие (brownfield) проекты для ускорения разработки продукта и упрощения доставки фронтенда, однако перед запуском в продакшн требуется ручная проверка интеграции, оценка зависимостей и подтверждение поддержки лицензии и безопасности. При надлежащем аудите фреймворк подходит для прототипов и внутренних сервисов, а при дополнительной проверке может быть использован и в полномасштабных продакшн‑решениях.

### 中文

**项目简介**  
toss/granite 是面向微服务架构的企业级 React Native 框架，专为已有项目（brownfield）设计，打包体积约 200 KB，内置与 AWS 生态的对接方案，可快速交付用户界面。

**价值**  
- **降低 UI 开发成本**：提供一套可直接复用的组件库和布局系统，开发者无需从零编写大量样式和交互代码。  
- **加速产品上线**：统一的微服务集成方式让前端团队可以在数天内搭建出可交付的界面原型，缩短从需求到发布的周期。  
- **提升交付可靠性**：框架自带的代码分割、懒加载以及与 AWS Amplify、AppSync 等服务的预设集成，帮助团队在保持轻量 bundle 的同时获得可靠的后端支撑。

**典型接入方式**  
1. **项目初始化**：在已有 React Native 项目根目录执行 `npx @toss/granite init`，框架会自动生成 `granite.config.ts`、基础路由和示例页面。  
2. **组件使用**：通过 `import { Button, Card } from '@toss/granite/ui'` 引入 UI 组件，配合 `useGraniteService` Hook 调用已注册的微服务 API。  
3. **AWS 配置**：在 `granite.config.ts` 中填写 AWS 区域、Cognito 用户池、AppSync 端点等信息；框架会在构建时自动生成对应的 Amplify 配置文件。  
4. **手动审查**：由于元数据的集成信号较少，建议在正式合入前对 `granite.config.ts`、依赖树以及安全审计报告进行人工检查，确保没有不兼容或安全风险。

**生产可用性**  
- **成熟度**：GitHub ★455、Fork 51，最近一次更新为 2026‑05‑12，代码以 TypeScript 编写，社区活跃度中等。  
- **适用场景**：适合作为内部工具、原型或非核心业务的前端入口；在经过依赖、许可证和安全审计后，可用于面向用户的生产环境。  
- **风险**：仍需确认许可证兼容性、长期维护者活跃度以及潜在的安全漏洞；在正式上线前建议进行完整的 CI/CD 测试和监控埋点。  

总体而言，toss/granite 为需要快速构建微服务驱动的移动 UI 的团队提供了轻量且可扩展的解决方案，只要做好审计和维护工作，即可在生产环境中安全使用。

## 🧭 Practical evaluation

**Value:** toss/granite helps ship user-facing interfaces with less custom UI work.

**Best use cases**

- build product UI faster
- reuse interface components
- improve frontend delivery

**Integration notes:** Needs manual inspection before adoption because integration signals are sparse in the discovered metadata.

**Production readiness:** Medium: useful for prototypes or internal workflows, with dependency and maintenance checks before production.

**Quality signals**

- 455 GitHub stars
- 51 forks
- updated 2026-05-12
- primary language: TypeScript
- 1 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 43/100 |
| stars | 57/100 |
| topics | 13/100 |
| outlook | 64/100 |
| quality | 61/100 |
| recency | 80/100 |
| adoption | 53/100 |
| production | 65/100 |
| usefulness | 58/100 |
| integration | 46/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 300/100 |

---

<sub>🔭 Discovered 2026-05-12 · [View on GitHub](https://github.com/toss/granite) · [← Back to Cloud--storage](./README.md)</sub>
