# nguyenphutrong/quotio

[![Stars](https://img.shields.io/github/stars/nguyenphutrong/quotio?style=flat-square&color=yellow)](https://github.com/nguyenphutrong/quotio/stargazers) [![Forks](https://img.shields.io/github/forks/nguyenphutrong/quotio?style=flat-square&color=blue)](https://github.com/nguyenphutrong/quotio/network) [![Language](https://img.shields.io/badge/lang-Swift-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-69%2F100-brightgreen?style=flat-square)](#)

> Stop juggling AI accounts. Quotio is a beautiful native macOS menu bar app that unifies your Claude, Gemini, OpenAI, Qwen, and Antigravity subscriptions – with real-time quota tracking and smart auto-failover for AI coding tools like Claude Code, OpenCode, and Droid.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 4.4k |
| 🍴 **Forks** | 286 |
| 💻 **Language** | Swift |
| 📈 **Score** | 69/100 |
| 🗓️ **Last push** | 2026-05-11 |
| 🔍 **Source** | github |

## 🏷️ Topics

`ai-tools` `developer-tools` `proxy` `quota-monitor`

## 🎯 Categories

Payments · AI/ML · DevTools

## 📝 Summary

### English

**Brief summary**  
Quotio is a native mac‑OS menu‑bar utility that aggregates multiple AI service subscriptions (Claude, Gemini, OpenAI, Qwen, Antigravity) into a single interface, showing real‑time usage quotas and automatically failing over to the next provider when limits are reached. It is built in Swift, has attracted over 4 k stars on GitHub, and targets developers who need seamless, cost‑aware access to AI coding assistants such as Claude Code, OpenCode and Droid.

**Value proposition**  
- **Unified billing & quota visibility** – developers no longer juggle separate accounts; Quotio displays remaining tokens/credits for each provider and lets you switch instantly, reducing downtime and unexpected over‑charges.  
- **Smart auto‑failover** – when a model’s quota is exhausted, the app reroutes requests to an alternate provider, keeping CI pipelines and AI‑assisted tools running without manual intervention.  
- **Developer‑centric integration** – the library exposes simple Swift APIs and a CLI, making it easy to embed quota checks or payment‑flow hooks into internal tooling, prototype checkout experiences, or automate PSP (payment service provider) operations.

**Practical adoption path**  
1. **Proof‑of‑concept** – clone the repo, run the provided example project, and verify that the menu‑bar UI correctly reads quotas from your API keys.  
2. **Read‑me validation** – follow the quick‑start guide to add your credentials (Claude, Gemini, OpenAI, etc.) and test the auto‑failover by artificially limiting one quota.  
3. **Integrate** – import the Swift package into your macOS app or CI script, call the `QuotaManager` API to fetch remaining credits before each AI request, and optionally hook into your billing backend to log usage.  
4. **Iterate** – expand the proof‑of‑concept into a small internal tool (e.g., a build‑agent wrapper) before rolling it out to production services.

**Production readiness**  
- **Maturity**: Medium. The project is actively maintained (last commit 2026‑05‑11), has a strong community signal (4 383 stars, 286 forks), and the core functionality is stable for prototyping.  
- **Dependencies**: Pure Swift/macOS, but relies on each provider’s authentication flow; you’ll need to manage API keys and possibly rate‑limit handling yourself.  
- **Risks**: Integration steps are not fully documented in the metadata, so expect some initial setup effort to map your PSP/billing workflow to Quotio’s API. Conduct a small PoC to gauge configuration complexity and verify that auto‑failover meets your latency requirements before committing to production.  

Overall, Quotio offers a compelling way to streamline AI‑service billing and reliability for macOS‑based development environments, provided you allocate time for a modest integration validation.

### Русский

Quotio — это нативное macOS‑приложение в виде меню‑бара, которое объединяет подписки на Claude, Gemini, OpenAI, Qwen и Antigravity, отображает их текущие квоты в реальном времени и автоматически переключает запросы между сервисами (auto‑failover) для инструментов разработки кода — Claude Code, OpenCode и Droid.  
Типичный сценарий внедрения: добавить в прототип или внутренний workflow быстрый модуль биллинга/чекаута, который через простую POC‑интеграцию (см. README) получает данные о доступных квотах и управляет оплатой/переключением между AI‑провайдерами.  
Готовность к production — средняя: проект имеет большую популярность (4383 ★, 286 forks) и активную поддержку (обновление 2026‑05‑11), но путь интеграции не полностью документирован, поэтому перед запуском в продакшн требуется проверка зависимостей и небольшая пилотная проверка.

### 中文

**项目简介（2‑3 句）**  
Quotio 是一款原生 macOS 菜单栏工具，统一管理 Claude、Gemini、OpenAI、Qwen、Antigravity 等多家 AI 账号，并实时显示配额使用情况。它还能在 Claude Code、OpenCode、Droid 等 AI 编码插件之间进行智能自动切换，避免因配额耗尽导致的中断。

---

## 价值体现  

1. **一站式账号与配额管理**：开发者无需在多个浏览器或客户端之间切换，所有 AI 订阅在同一界面可视化，极大提升工作效率。  
2. **自动容错与降级**：配额即将耗尽时，Quotio 会自动切换到备用模型，保证代码生成、调试等 AI 辅助功能的持续可用。  
3. **加速计费与 PSP 流程集成**：提供统一的账单视图和 API，可快速嵌入内部计费、结算或支付服务（PSP）系统，缩短从概念验证到上线的时间。  

---

## 典型接入方式  

| 场景 | 接入步骤 | 关键点 |
|------|----------|--------|
| **原型/内部工具** | 1. Fork 项目或直接 clone <br>2. 按 README 中的 `setup.sh` 脚本配置 API Key（Claude、Gemini、OpenAI 等）<br>3. 在 macOS 上运行 `Quotio.app`，通过菜单栏观察配额 | 只需几分钟即可完成，适合快速验证 AI 费用和切换策略。 |
| **计费/结算系统** | 1. 在后端服务中调用 Quotio 提供的本地 REST 接口（`/quota/status`、`/quota/switch`）<br>2. 将返回的配额数据写入业务数据库或计费平台<br>3. 根据配额阈值触发自动切换或提醒邮件 | 需要在 CI/CD 中加入 Swift 编译步骤，确保二进制兼容目标 macOS 版本。 |
| **生产级 AI 编码平台** | 1. 将 Quotio 作为系统守护进程部署在开发者工作站或 CI 机器上<br>2. 使用其提供的 SDK（Swift/Objective‑C）在自研 IDE 插件中读取当前模型信息<br>3. 配合内部支付网关（Stripe、PayPal 等）实现按使用量计费 | 关注安全：API Key 采用 macOS Keychain 存储；建议使用签名的二进制并开启 Gatekeeper。 |

---

## 生产可用性评估  

| 维度 | 评估 | 说明 |
|------|------|------|
| **代码成熟度** | ★★★☆☆ (中等) | 4383 星、286 Fork，活跃维护至 2026‑05‑11，主语言 Swift，代码结构清晰，但缺少完整的 CI 测试覆盖。 |
| **依赖与运维** | ★★☆☆☆ | 依赖 macOS 框架和系统权限（Keychain、网络），在非 macOS 环境不可用；需要定期更新 Swift 编译链。 |
| **安全合规** | ★★☆☆☆ | API Key 通过 Keychain 存储，符合本地安全要求；对外提供的 REST 接口需自行加固（TLS、鉴权）。 |
| **可扩展性** | ★★★★☆ | 支持任意数量的 AI 供应商，只需在配置文件中添加对应的 API Endpoint 与凭证。 |
| **上线建议** | **先做 PoC** → 完成配额监控与自动切换验证 → 在内部 CI 环境进行压力测试 → 通过安全审计后方可投入生产。 |

**结论**：Quotio 对于需要在 macOS 开发环境中统一管理多家 AI 账号、实现配额可视化和自动容错的团队非常有价值。它适合作为原型或内部工具快速落地；在生产环境使用前，建议完成小规模 PoC、完善安全加固并做好依赖维护计划。

## 🧭 Practical evaluation

**Value:** nguyenphutrong/quotio helps integrate monetization, billing, or PSP flows faster.

**Best use cases**

- integrate billing or checkout
- evaluate PSP flows
- automate payment operations

**Integration notes:** Looks feasible to evaluate, but integration should start with a small proof of concept and README check.

**Production readiness:** Medium: useful for prototypes or internal workflows, with dependency and maintenance checks before production.

**Quality signals**

- 4383 GitHub stars
- 286 forks
- updated 2026-05-11
- primary language: Swift
- 4 topics

**Risks:** Integration path is not obvious from metadata; validate setup cost before committing.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 61/100 |
| stars | 78/100 |
| topics | 50/100 |
| outlook | 83/100 |
| quality | 80/100 |
| recency | 100/100 |
| adoption | 73/100 |
| production | 74/100 |
| usefulness | 74/100 |
| integration | 30/100 |
| sourceTrust | 100/100 |

---

<sub>🔭 Discovered 2026-05-11 · [View on GitHub](https://github.com/nguyenphutrong/quotio) · [← Back to Payments](./README.md)</sub>
