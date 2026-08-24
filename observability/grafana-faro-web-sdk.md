# grafana/faro-web-sdk

[![Stars](https://img.shields.io/github/stars/grafana/faro-web-sdk?style=flat-square&color=yellow)](https://github.com/grafana/faro-web-sdk/stargazers) [![Forks](https://img.shields.io/github/forks/grafana/faro-web-sdk?style=flat-square&color=blue)](https://github.com/grafana/faro-web-sdk/network) [![Language](https://img.shields.io/badge/lang-TypeScript-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-57%2F100-brightgreen?style=flat-square)](#)

> The Grafana Faro Web SDK, part of the Grafana Faro project, is a highly configurable web SDK for real user monitoring (RUM) that instruments browser frontend applications to capture observability signals. Frontend telemetry can then be correlated with backend and infrastructure data for full-stack observability.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 1.1k |
| 🍴 **Forks** | 113 |
| 💻 **Language** | TypeScript |
| 📈 **Score** | 57/100 |
| 🗓️ **Last push** | 2026-08-24 |
| 🔍 **Source** | github |

## 🏷️ Topics

_no topics_

## 🎯 Categories

Observability

## 📝 Summary

### English

**Brief Summary (2‑3 sentences)**  
The Grafana Faro Web SDK is a TypeScript‑based, highly configurable library that adds real‑user‑monitoring (RUM) to browser‑side applications, sending frontend telemetry that can be correlated with Grafana’s backend and infrastructure metrics for full‑stack observability. With over a thousand GitHub stars and active recent commits, it lets teams ship UI‑heavy features faster by handling the heavy lifting of instrumentation, leaving developers free to focus on product logic.

**Value Proposition**  
- **Instant observability**: Out‑of‑the‑box hooks capture page loads, navigation, errors, and custom user events without writing bespoke tracking code.  
- **Unified data**: Frontend signals are sent to the same Grafana backend used for backend and infra metrics, enabling end‑to‑end tracing and root‑cause analysis.  
- **Reduced UI overhead**: By providing a ready‑made SDK, teams spend less time building custom monitoring layers and can iterate on UI components more quickly.

**Practical Adoption Path**  

| Step | Action | Why |
|------|--------|-----|
| 1️⃣  | **Proof‑of‑concept** – scaffold a minimal app (e.g., Create‑React‑App or Vite) and follow the README to install `@grafana/faro-web-sdk`. Verify that a heartbeat event appears in your Grafana instance. | Confirms compatibility and validates the data pipeline with minimal risk. |
| 2️⃣  | **Configuration tuning** – enable only the needed instruments (e.g., navigation, fetch, custom events) and set the appropriate `apiKey`/`collectorUrl`. | Keeps payload size low and aligns telemetry with your observability goals. |
| 3️⃣  | **Gradual rollout** – wrap the SDK initialization in a feature flag and enable it for a subset of users or environments (staging → canary → production). | Allows monitoring of performance impact and early detection of mis‑configurations. |
| 4️⃣  | **Integration with existing Grafana dashboards** – map Faro‑generated traces to existing dashboards or create new panels that surface UI latency, error rates, and user journeys. | Turns raw data into actionable insights for developers and SREs. |
| 5️⃣  | **Governance & maintenance** – lock the SDK version in `package.json`, add a security‑scan step (e.g., `npm audit`), and monitor the repository for releases or breaking changes. | Ensures long‑term stability and reduces supply‑chain risk. |

**Production Readiness Assessment**  

| Dimension | Rating | Rationale |
|-----------|--------|-----------|
| **Stability** | ★★★☆☆ (Medium) | The SDK is actively maintained (last commit 2026‑05‑11) and has a healthy star/fork count, but it is still relatively new for mission‑critical workloads. |
| **Feature completeness** | ★★★★☆ | Core RUM capabilities (page view, navigation, errors, custom events) are present; advanced features (session replay, AI‑assisted anomaly detection) are not yet built‑in. |
| **Integration effort** | ★★☆☆☆ (Low‑moderate) | Simple npm install and a few config lines; however, aligning collector endpoints and authentication may require coordination with your Grafana stack. |
| **Operational risk** | ★★☆☆☆ | No known licensing or major security issues, but a formal security audit and a review of the maintainers’ activity are advisable before full production rollout. |
| **Overall** | **Medium** – suitable for prototypes, internal tools, or phased production releases after a controlled pilot. |

**Bottom line** – Grafana Faro Web SDK can accelerate UI development by offloading observability concerns to a proven, open‑source library. Start with a small proof‑of‑concept, validate data flow, then expand the rollout behind feature flags while establishing version lock‑down and security checks. After these steps, the SDK is ready for production use in most non‑mission‑critical front‑end services.

### Русский

**Grafana Faro Web SDK** — это гибко настраиваемый TypeScript‑SDK для реального мониторинга пользовательского опыта (RUM), который встраивает в браузерные фронтенды сбор телеметрии и позволяет связывать её с данными бекенда и инфраструктуры для полноценной full‑stack наблюдаемости. Типичный сценарий — добавить несколько строк кода в небольшое proof‑of‑concept проекта, проверить работу через README, а затем масштабировать SDK на все UI‑компоненты, ускоряя разработку и повышая качество доставки клиентской части. Уровень готовности — средний: SDK достаточно зрелый (≈1 k звёзд, активные коммиты) для прототипов и внутренних сервисов, но перед запуском в продакшн требуется проверка лицензии, безопасности и поддерживаемости зависимостей.

### 中文

**项目简介**  
Grafana Faro Web SDK 是 Grafana Faro 系列中的前端监控工具，提供高度可配置的 Real‑User‑Monitoring（RUM）能力。它能够在浏览器端自动埋点，收集页面加载、交互、错误等可观测信号，并与后端、基础设施数据关联，实现全栈可观测性。

**价值**  
- **降低前端监控门槛**：无需自行编写复杂的埋点代码，即可获取完整的用户行为与性能数据。  
- **加速 UI 开发**：通过统一的监控 SDK，团队可以更专注于业务功能和界面复用，缩短产品交付周期。  
- **提升可观测性**：前端遥测与 Grafana 后端数据天然兼容，帮助运维和开发快速定位性能瓶颈和异常。

**典型接入方式**  
1. **安装**：`npm install @grafana/faro-web-sdk`（或使用 Yarn、pnpm）。  
2. **初始化**：在入口文件（如 `index.tsx`、`main.js`）中引入并调用 `initializeFaro`，传入 Grafana Faro Collector 的 URL 与项目 ID 等必需配置。  
   ```ts
   import { initializeFaro } from '@grafana/faro-web-sdk';

   initializeFaro({
     url: 'https://faro-collector.example.com',
     apiKey: 'YOUR_PROJECT_API_KEY',
     // 可选：开启页面加载、错误、用户交互等插件
     plugins: [/* @grafana/faro-web-sdk-plugin-* */],
   });
   ```
3. **自定义埋点（可选）**：使用 `faro.api.pushEvent`、`faro.api.setUser` 等 API 手动上报业务事件或用户信息。  
4. **验证**：启动项目后打开浏览器开发者工具的 Network 面板，确认向 Collector 发送的 `POST /collect` 请求；也可在 Grafana Faro UI 中查看实时数据。

**生产可用性**  
- **成熟度**：GitHub ★1062、Fork 113，活跃维护，最近一次提交在 2026‑05‑11，代码基于 TypeScript，适合现代前端框架。  
- **适用场景**：非常适合作为原型、内部工具或逐步迁移到生产环境的监控方案。  
- **风险与准备**：在正式上线前建议完成以下检查  
  - 评估许可证（Apache‑2.0）与公司合规性。  
  - 通过安全审计（SCA）确认依赖无已知漏洞。  
  - 在小范围（如单个业务线或功能）进行 PoC，验证数据上报、隐私合规和对现有前端性能的影响。  
- **结论**：在完成上述验证后，Faro Web SDK 可进入生产使用，提供可靠的前端可观测性并与 Grafana 生态无缝集成。

## 🧭 Practical evaluation

**Value:** grafana/faro-web-sdk helps ship user-facing interfaces with less custom UI work.

**Best use cases**

- build product UI faster
- reuse interface components
- improve frontend delivery

**Integration notes:** Looks feasible to evaluate, but integration should start with a small proof of concept and README check.

**Production readiness:** Medium: useful for prototypes or internal workflows, with dependency and maintenance checks before production.

**Quality signals**

- 1062 GitHub stars
- 113 forks
- updated 2026-05-11
- primary language: TypeScript

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 51/100 |
| stars | 64/100 |
| topics | 0/100 |
| outlook | 47/100 |
| quality | 47/100 |
| recency | 20/100 |
| adoption | 61/100 |
| production | 48/100 |
| usefulness | 74/100 |
| integration | 62/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 100/100 |

---

<sub>🔭 Discovered 2026-05-11 · [View on GitHub](https://github.com/grafana/faro-web-sdk) · [← Back to Observability](./README.md)</sub>
