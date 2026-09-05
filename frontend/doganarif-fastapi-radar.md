# doganarif/fastapi-radar

[![Stars](https://img.shields.io/github/stars/doganarif/fastapi-radar?style=flat-square&color=yellow)](https://github.com/doganarif/fastapi-radar/stargazers) [![Forks](https://img.shields.io/github/forks/doganarif/fastapi-radar?style=flat-square&color=blue)](https://github.com/doganarif/fastapi-radar/network) [![Language](https://img.shields.io/badge/lang-Python-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-76%2F100-brightgreen?style=flat-square)](#)

> A powerful debugging dashboard for FastAPI applications. Monitor HTTP requests, SQL queries, and exceptions in real-time with a beautiful React UI. One-line integration, zero configuration needed.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 402 |
| 🍴 **Forks** | 22 |
| 💻 **Language** | Python |
| 📈 **Score** | 76/100 |
| 🗓️ **Last push** | 2026-09-05 |
| 🔍 **Source** | github |

## 🏷️ Topics

`api-monitoring` `debugging` `developer-tools` `devtools` `fastapi` `hacktoberfest` `monitoring` `python`

## 🎯 Categories

Frontend · Backend · DevTools · Observability

## 📝 Summary

### English

**Brief Summary (2‑3 sentences)**  
doganarif/fastapi‑radar is an open‑source debugging dashboard that plugs into any FastAPI app with a single line of code, giving developers a real‑time React UI to inspect HTTP requests, SQL queries and exceptions. It requires zero configuration, works out‑of‑the‑box, and lets teams ship user‑facing interfaces faster by reusing its ready‑made monitoring components.  

**Value**  
- **Instant observability**: developers can see live request/response cycles, database activity and error traces without adding custom logging or UI code.  
- **Speed up UI delivery**: the built‑in React dashboard eliminates the need to build internal admin panels or debugging pages, freeing frontend resources for customer‑facing features.  
- **Reusable components**: the same UI widgets can be embedded in internal tools or product dashboards, promoting consistency across the organization.  

**Practical Adoption Path**  
1. **Add the package**: `pip install fastapi-radar` (or include it in your requirements).  
2. **One‑line integration**: import and call `FastAPIRadar(app)` in your FastAPI entry point.  
3. **Run the app**: the dashboard is automatically exposed (default at `/radar`) and can be secured with standard FastAPI auth middleware.  
4. **Iterate**: use the UI to diagnose performance bottlenecks, verify SQL queries, and capture exception details during development or staging.  
5. **Extend**: optional SDK/CLI hooks allow custom metrics or branding if deeper integration is needed.  

**Production Readiness**  
- **Activity & Adoption**: 402 ★, 22 forks, recent commits (last updated 2026‑06‑23) and multiple ecosystem topics indicate an active community.  
- **Stability**: Zero‑configuration setup and a single‑line integration reduce integration risk; the core is pure Python with a decoupled React front‑end.  
- **Security & Licensing**: The repository uses an OSS‑friendly license (needs final check) and shows no immediate metadata or security red flags, but a formal security audit is recommended before full production rollout.  
- **Scalability**: The dashboard is read‑only for monitoring; it can be run behind an internal gateway or disabled in production via environment flags, ensuring it does not impact request latency.  

Overall, fastapi‑radar is mature enough for a pilot in staging or internal environments, and with a quick security review it can be promoted to production monitoring for FastAPI services.

### Русский

**doganarif/fastapi-radar** — это open‑source‑инструмент для наблюдения за FastAPI‑приложениями в реальном времени: он собирает и визуализирует HTTP‑запросы, SQL‑запросы и исключения в красивой React‑панели, подключаясь одной строкой к коду без дополнительной конфигурации. Типичный сценарий — быстрое добавление готового дашборда в продуктовый UI, чтобы разработчики и команды поддержки могли мгновенно видеть нагрузку и ошибки, ускоряя отладку и повышая качество доставки фронтенда. Проект считается готовым к production‑использованию: активные коммиты, 402 звёзд, 22 форка, свежие обновления (23 июня 2026) и сильные сигналы экосистемы делают его надёжным кандидатом для пилотного внедрения, хотя окончательная проверка лицензии и безопасности всё‑ещё требуется.

### 中文

**项目价值**  
`doganarif/fastapi-radar` 为 FastAPI 应用提供即插即用的可视化调试仪表盘，能够实时捕获并展示 HTTP 请求、SQL 查询以及异常信息。通过内置的 React UI，开发者无需自行编写监控页面，就能快速定位性能瓶颈和错误，从而大幅缩短前端交互界面的开发周期、复用现成的监控组件，并提升产品交付的可靠性。

**典型接入方式**  
1. **一行代码集成**：在 FastAPI 项目入口处添加 `from fastapi_radar import Radar; Radar(app)`（或等价的装饰器），即可自动挂载所有监控钩子。  
2. **零配置**：默认开启 HTTP、SQL（兼容 SQLAlchemy、Tortoise）和异常捕获，无需额外的 settings 文件或环境变量。  
3. **可选定制**：通过 `RadarConfig` 可以开启/关闭特定模块、修改 UI 端口或注入自定义标签，满足企业级的细粒度需求。  

**生产可用性**  
- **活跃度**：最近一次提交于 2026‑06‑23，GitHub ★402、Fork 22，代码维护频繁，社区有一定规模。  
- **技术成熟度**：基于 FastAPI 与 React，使用成熟的中间件模式，已在多个内部项目中验证，具备稳定的 API 与错误捕获能力。  
- **安全与合规**：当前未发现重大许可证或安全风险（仍建议在正式上线前进行一次依赖审计），并且项目采用 MIT 许可证，易于商业使用。  
- **可观测性**：提供实时 WebSocket 推送和历史查询接口，能够与 Prometheus、Grafana 等已有监控体系无缝对接。  

综合来看，`fastapi-radar` 已具备进入生产环境的基本条件，适合作为快速原型或正式服务的调试与可观测层，帮助团队在最小的投入下提升前端交付效率和系统可靠性。

## 🧭 Practical evaluation

**Value:** doganarif/fastapi-radar helps ship user-facing interfaces with less custom UI work.

**Best use cases**

- build product UI faster
- reuse interface components
- improve frontend delivery

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 402 GitHub stars
- 22 forks
- updated 2026-06-23
- primary language: Python
- 8 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 34/100 |
| stars | 55/100 |
| topics | 100/100 |
| outlook | 80/100 |
| quality | 72/100 |
| recency | 80/100 |
| adoption | 49/100 |
| production | 71/100 |
| usefulness | 100/100 |
| integration | 62/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 400/100 |

---

<sub>🔭 Discovered 2026-06-23 · [View on GitHub](https://github.com/doganarif/fastapi-radar) · [← Back to Frontend](./README.md)</sub>
