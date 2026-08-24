# ashfromsky/acquiremock

[![Stars](https://img.shields.io/github/stars/ashfromsky/acquiremock?style=flat-square&color=yellow)](https://github.com/ashfromsky/acquiremock/stargazers) [![Forks](https://img.shields.io/github/forks/ashfromsky/acquiremock?style=flat-square&color=blue)](https://github.com/ashfromsky/acquiremock/network) [![Language](https://img.shields.io/badge/lang-Python-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-64%2F100-brightgreen?style=flat-square)](#)

> AcquireMock is a full-featured mock payment gateway built for reliable testing of any e-commerce integration. It simulates real payment flows with OTP verification, HMAC-signed webhooks, and a modern user interface.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 76 |
| 🍴 **Forks** | 8 |
| 💻 **Language** | Python |
| 📈 **Score** | 64/100 |
| 🗓️ **Last push** | 2026-08-24 |
| 🔍 **Source** | github |

## 🏷️ Topics

`api-testing` `async` `checkout` `developer-tool` `docker` `e-commerce` `fastapi` `hmac-sha256` `mock-server` `mocking` `otp-verification` `payment-gateway`

## 🎯 Categories

Payments · Automation · Frontend · Backend · DevTools

## 📝 Summary

### English

**Brief Summary**  
AcquireMock is an open‑source, full‑featured mock payment gateway that reproduces real‑world payment flows—including OTP verification, HMAC‑signed webhooks, and a modern UI—so developers can test e‑commerce integrations without touching live PSPs. Written in Python and packaged with an API/SDK/CLI, it speeds up billing‑or checkout‑related development and automated testing.  

**Value**  
- **Accelerated integration** – developers can prototype and validate monetisation, billing, or PSP workflows locally, eliminating the need for costly sandbox accounts or trial transactions.  
- **Realistic behaviour** – OTP, webhook signing, and UI flows mirror production gateways, catching edge‑case bugs early in CI pipelines.  
- **Unified tooling** – a single codebase (Python) offers API, SDK, and CLI entry points, making it easy to embed in backend services, frontend test suites, or DevOps automation.  

**Practical Adoption Path**  
1. **Explore the API/SDK** – clone the repo, run the provided Docker compose or `pip install .` to spin up the mock server locally.  
2. **Replace live credentials** – point your application’s payment client to `http://localhost:8000` (or the configured host) and use the mock’s test keys.  
3. **Integrate in CI** – add a step that starts the mock container before running integration tests; the built‑in CLI can trigger OTP flows and verify webhook signatures automatically.  
4. **Extend as needed** – the Python codebase is modular; you can add custom PSP‑specific endpoints or plug in your own webhook verification logic.  

**Production Readiness**  
- **Maturity**: Medium. The project is actively maintained (last commit 2026‑05‑04), has 76 ⭐ and 8 🍴, and covers both backend and frontend testing needs.  
- **Suitability**: Ideal for prototypes, internal QA environments, and automated test pipelines. For production‑grade payment processing you’ll still need a real PSP, but AcquireMock can safely handle pre‑release validation.  
- **Considerations**: Review the license, perform a brief security audit of the mock server (especially webhook handling), and verify that the dependency tree (Python packages) aligns with your organization’s policies before promoting it to a shared staging environment.

### Русский

AcquireMock — это полнофункциональный open‑source мок‑шлюз для платежей, позволяющий быстро протестировать любые e‑commerce интеграции, имитируя реальные сценарии с OTP‑проверкой, HMAC‑подписанными веб‑хуками и удобным UI. Типичное внедрение — подключение к процессу биллинга или checkout через предоставляемый API/SDK/CLI, что ускоряет оценку PSP‑потоков и автоматизацию платёжных операций. Проект находится на среднем уровне готовности к production: подходит для прототипов и внутренних воркфлоу, но требует проверки лицензии, безопасности и подтверждения активных мейнтейнеров перед масштабным запуском.

### 中文

**项目简介**  
AcquireMock 是一个功能完整的模拟支付网关，能够在本地或 CI 环境中完整复现真实的支付流程，包括 OTP 验证、HMAC 签名的 Webhook 以及现代化的 UI，帮助开发者对电商系统的结算、计费或 PSP 集成进行可靠的自动化测试。

**价值**  
- **加速集成**：无需真实的第三方支付账户，即可在几分钟内搭建完整的支付链路，显著缩短开发和调试周期。  
- **提升可靠性**：通过 OTP、Webhook、错误码等全链路模拟，确保业务逻辑在各种异常场景下也能正确响应。  
- **降低成本**：避免在测试阶段产生真实交易费用或触发风控限制，适合原型、内部工具以及持续集成流水线。

**典型接入方式**  
1. **API/SDK**：项目提供 RESTful API（Swagger 文档）以及 Python SDK，直接在代码中调用 `create_payment`, `confirm_otp` 等接口。  
2. **CLI**：内置 `acquiremock-cli` 可用于快速启动本地模拟服务器或生成测试数据。  
3. **Docker**：官方提供 `docker-compose.yml`，一键启动完整的模拟环境（包括数据库、Web UI、Webhook 服务器）。  
4. **语言元数据**：虽然核心实现是 Python，但通过 OpenAPI 规范，几乎所有主流语言（JavaScript、Java、Go 等）都可以生成对应客户端。

**生产可用性**  
- **成熟度**：GitHub 评分 74/100，拥有 76 ★、8 Fork，最近一次更新于 2026‑05‑04，代码基于 Python，活跃度尚可。  
- **适用场景**：非常适合原型开发、内部测试、CI/CD 自动化以及支付流程的演练。  
- **风险与限制**：当前定位为 **Medium** 级别的生产可用性——在正式线上使用前建议：  
  - 完成安全审计（尤其是 HMAC、OTP 生成逻辑）。  
  - 检查许可证兼容性（项目采用的开源许可证）。  
  - 评估依赖库的维护状态并做好版本锁定。  
  - 如需高可用或大并发，考虑自行部署并进行性能调优。  

总体而言，AcquireMock 能显著提升支付相关功能的开发效率和测试可靠性，适合作为开发、测试环境的首选模拟平台；在经过安全和运维审查后，也可在受控的生产场景（如内部计费系统）中使用。

## 🧭 Practical evaluation

**Value:** ashfromsky/acquiremock helps integrate monetization, billing, or PSP flows faster.

**Best use cases**

- integrate billing or checkout
- evaluate PSP flows
- automate payment operations

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** Medium: useful for prototypes or internal workflows, with dependency and maintenance checks before production.

**Quality signals**

- 76 GitHub stars
- 8 forks
- updated 2026-05-04
- primary language: Python
- 18 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 24/100 |
| stars | 40/100 |
| topics | 100/100 |
| outlook | 54/100 |
| quality | 51/100 |
| recency | 20/100 |
| adoption | 36/100 |
| production | 51/100 |
| usefulness | 90/100 |
| integration | 78/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 500/100 |

---

<sub>🔭 Discovered 2026-05-13 · [View on GitHub](https://github.com/ashfromsky/acquiremock) · [← Back to Payments](./README.md)</sub>
