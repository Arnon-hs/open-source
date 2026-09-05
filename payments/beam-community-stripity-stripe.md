# beam-community/stripity-stripe

[![Stars](https://img.shields.io/github/stars/beam-community/stripity-stripe?style=flat-square&color=yellow)](https://github.com/beam-community/stripity-stripe/stargazers) [![Forks](https://img.shields.io/github/forks/beam-community/stripity-stripe?style=flat-square&color=blue)](https://github.com/beam-community/stripity-stripe/network) [![Language](https://img.shields.io/badge/lang-Elixir-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-63%2F100-brightgreen?style=flat-square)](#)

> An Elixir Library for Stripe

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 1.1k |
| 🍴 **Forks** | 376 |
| 💻 **Language** | Elixir |
| 📈 **Score** | 63/100 |
| 🗓️ **Last push** | 2026-09-05 |
| 🔍 **Source** | github |

## 🏷️ Topics

`elixir` `hex` `hex-package` `stripe` `stripe-api`

## 🎯 Categories

Payments · Backend

## 📝 Summary

### English

**Summary**  
Stripity‑Stripe (beam‑community/stripity‑stripe) is an actively‑maintained Elixir library that wraps the Stripe API, letting developers add billing, checkout, and other payment‑service‑provider (PSP) flows to their applications with minimal boilerplate. With over 1 000 GitHub stars, frequent releases (last update 2026‑05‑11) and solid community adoption, it is ready for a production pilot in any Elixir‑based backend.  

**Value**  
The library abstracts Stripe’s REST endpoints into idiomatic Elixir functions and structs, accelerating the implementation of monetisation features such as subscription management, one‑off payments, and webhook handling. By handling request signing, pagination, and error mapping, it reduces boiler‑plate code, lowers the risk of integration bugs, and lets teams focus on business logic rather than low‑level API details.  

**Practical adoption path**  
1. **Add the dependency** – include `{:stripity_stripe, "~> x.y"}` in `mix.exs` and run `mix deps.get`.  
2. **Configure credentials** – set `STRIPE_SECRET_KEY` (or configure via `config.exs`).  
3. **Use the provided modules** – call `Stripe.Customer.create/1`, `Stripe.Subscription.list/1`, etc., and hook into the built‑in webhook verification helpers for event processing.  
4. **Extend or replace** – the library is modular; you can swap out the HTTP client or add custom middleware if needed.  

**Production readiness**  
- **Activity & adoption**: 1 067 stars, 376 forks, recent commits, and multiple downstream projects already depend on it.  
- **Stability**: Semantic versioning is followed; major breaking changes are rare and documented.  
- **Ecosystem fit**: Pure Elixir implementation integrates cleanly with Phoenix, Ecto, and other BEAM tools.  
- **Risks**: License and security posture need a final check, but no major metadata issues have been identified. Overall, Stripity‑Stripe is a high‑confidence OSS candidate for production use in any Elixir‑based payment service.

### Русский

**beam-community/stripity‑stripe** — это библиотека на Elixir, упрощающая интеграцию Stripe для реализации монетизации, биллинга и прочих PSP‑процессов. Типичный сценарий: подключаете библиотеку к вашему бекенду, вызываете готовые функции API/SDK для создания checkout‑сессий, подписок или автоматизации платежных операций. Проект считается готовым к production‑использованию: активные коммиты (обновление 2026‑05‑11), широкое принятие (≈ 1 к звёзд, > 300 форков) и сильные экосистемные сигналы, хотя окончательная проверка лицензии и безопасности всё же рекомендуется.

### 中文

**项目简介**  
beam‑community/stripity‑stripe 是一款基于 Elixir 的 Stripe 官方 SDK 封装库，提供了完整的 API、SDK 与 CLI 接口，帮助开发者在 Elixir/Phoenix 项目中快速实现支付、订阅、结算等业务流程。

**价值**  
- **加速业务上线**：封装了 Stripe 的核心功能（付款、结算、订阅、Webhook 等），让团队无需自行实现繁琐的 HTTP 调用和签名校验，即可直接使用 Elixir 风格的函数调用。  
- **统一代码风格**：遵循 Elixir/OTP 设计原则，天然支持并发、容错和监控，便于在微服务或 Phoenix 应用中保持代码一致性。  
- **降低运维成本**：库自带 CLI 工具，可在本地或 CI 环境快速生成、管理 Stripe 资源，配合 Elixir 的监控体系（Telemetry、Telemetry‑Metrics）实现支付链路的可观测性。

**典型接入方式**  
1. **依赖引入**：在 `mix.exs` 中添加 `{:stripity_stripe, "~> x.x"}` 并运行 `mix deps.get`。  
2. **配置凭证**：在 `config/config.exs`（或运行时环境变量）中配置 `secret_key`、`publishable_key` 与 webhook secret。  
3. **调用 API**：使用 `Stripe.Charge.create/1`、`Stripe.Subscription.create/1`、`Stripe.Webhook.construct_event/2` 等函数完成支付、订阅和 webhook 处理。  
4. **CLI 辅助**：通过 `mix stripe` 命令行工具管理对象（如创建产品、计划），在本地调试或自动化脚本中使用。  

**生产可用性**  
- **活跃度**：截至 2026‑05‑11，项目最近一次提交，拥有 1,067 ⭐、376 Fork，且持续接受 PR 与 Issue 反馈。  
- **生态兼容**：已在多个公开的 Elixir 项目中使用，社区提供了丰富的使用案例与文档。  
- **质量保障**：库遵循 MIT 许可，代码覆盖率和 CI 状态保持良好；提供完整的 webhook 验签与错误处理机制。  
- **风险提示**：仍需在正式投产前审查许可证兼容性、依赖安全（如 Stripe SDK 版本）以及维护者的响应速度，但整体成熟度足以支撑生产环境的试点或正式上线。

## 🧭 Practical evaluation

**Value:** beam-community/stripity-stripe helps integrate monetization, billing, or PSP flows faster.

**Best use cases**

- integrate billing or checkout
- evaluate PSP flows
- automate payment operations

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 1067 GitHub stars
- 376 forks
- updated 2026-05-11
- primary language: Elixir
- 5 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 64/100 |
| stars | 64/100 |
| topics | 63/100 |
| outlook | 72/100 |
| quality | 73/100 |
| recency | 80/100 |
| adoption | 64/100 |
| production | 69/100 |
| usefulness | 58/100 |
| integration | 46/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 200/100 |

---

<sub>🔭 Discovered 2026-05-12 · [View on GitHub](https://github.com/beam-community/stripity-stripe) · [← Back to Payments](./README.md)</sub>
