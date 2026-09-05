# pact-foundation/pact-js

[![Stars](https://img.shields.io/github/stars/pact-foundation/pact-js?style=flat-square&color=yellow)](https://github.com/pact-foundation/pact-js/stargazers) [![Forks](https://img.shields.io/github/forks/pact-foundation/pact-js?style=flat-square&color=blue)](https://github.com/pact-foundation/pact-js/network) [![Language](https://img.shields.io/badge/lang-TypeScript-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-73%2F100-brightgreen?style=flat-square)](#)

> JS version of Pact. Pact is a contract testing framework for HTTP APIs and non-HTTP asynchronous messaging systems.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 1.8k |
| 🍴 **Forks** | 355 |
| 💻 **Language** | TypeScript |
| 📈 **Score** | 73/100 |
| 🗓️ **Last push** | 2026-09-05 |
| 🔍 **Source** | github |

## 🏷️ Topics

`consumer-driven-contracts` `hacktoberfest` `mocha` `pact` `pact-js` `smartbear-supported` `test-framework`

## 🎯 Categories

Communication · DevTools

## 📝 Summary

### English

**Brief Summary**  
pact-foundation/pact‑js is the JavaScript implementation of the Pact contract‑testing framework, enabling teams to verify HTTP APIs and asynchronous messaging contracts directly from Node.js/TypeScript code. With over 1.7 k stars, active maintenance, and a rich ecosystem of CLI, SDK and language‑specific metadata, it is ready for serious pilot projects.  

**Value**  
- **Infrastructure reuse** – By defining consumer‑driven contracts once, teams avoid rebuilding request/response validation, mock servers, and stubbing logic across services.  
- **Speed to market** – Contract tests catch integration bugs early, letting API teams ship features faster and with higher confidence.  
- **Standardization** – A single, well‑documented contract format and test runner enforces consistent service patterns across micro‑services and messaging systems.  

**Practical Adoption Path**  
1. **Evaluate the API/CLI** – Install the npm package, run the built‑in CLI to generate a sample contract, and integrate the Pact‑JS SDK into existing test suites (Jest, Mocha, etc.).  
2. **Create consumer contracts** – Write Pact files in the consumer codebase; these become the source of truth for provider verification.  
3. **Set up provider verification** – Add a verification step to the provider CI pipeline using the Pact‑JS verifier, optionally publishing contracts to a Pact broker for cross‑team sharing.  
4. **Iterate and automate** – Promote contracts through staging environments, then gate production deployments on successful verification.  

**Production Readiness**  
- **Activity & Adoption** – Recent commits (as of 2026‑06‑25), 1 781 stars, 355 forks, and usage in multiple open‑source and enterprise projects indicate a healthy, active community.  
- **Maturity** – The TypeScript codebase, comprehensive CLI, and support for both HTTP and asynchronous messaging make it suitable for production pipelines.  
- **Risks** – No major licensing or security red flags have been identified, but a final review of the license (Apache‑2.0) and a security audit of dependencies is recommended before full rollout.  

Overall, pact‑js offers a robust, production‑grade contract‑testing solution that can be adopted quickly with minimal friction and delivers tangible speed and reliability gains for API‑centric teams.

### Русский

**pact-foundation/pact-js** — это TypeScript‑реализация популярного фреймворка Pact для контрактного тестирования HTTP‑API и асинхронных сообщений. Он позволяет командам быстро запускать новые сервисы, переиспользуя уже проверенную инфраструктуру тестов и стандартизируя паттерны взаимодействия между микросервисами. Проект имеет высокий уровень готовности к продакшн: активные коммиты, более 1700 звёзд, широкое принятие в сообществе и стабильный набор API/CLI, требующий лишь финальной проверки лицензии и безопасности.

### 中文

**项目简介**  
pact-foundation/pact-js 是 Pact 的 JavaScript 实现，提供基于合同的测试框架，支持 HTTP API 以及非 HTTP 的异步消息系统。它帮助团队在已有的服务基础设施上复用公共后端模块，避免重复搭建，从而加速 API 服务的交付。

**价值点**  
- **复用后端设施**：通过共享契约文件，前后端可以在同一套接口定义上协同开发，减少重复实现。  
- **提升交付速度**：在消费方编写消费者契约后，提供者只需验证契约即可上线，缩短集成与回归测试周期。  
- **统一服务模式**：契约即文档，团队能够统一 API 规范、错误码、消息格式等，提升系统可维护性。

**典型接入方式**  
1. **作为开发依赖**：`npm install @pact-foundation/pact`（或 `yarn add @pact-foundation/pact`），在项目中引入 Pact SDK。  
2. **编写消费者契约**：使用提供的 DSL（如 `pact.withProvider`、`pact.addInteraction`）描述期望的请求/响应或消息。  
3. **生成契约文件**：运行测试后自动生成 `pact` JSON 文件，供提供者验证。  
4. **提供者验证**：在提供者项目中使用 Pact CLI 或 SDK 加载契约文件，执行验证脚本，确保实现符合约定。  
5. **CI/CD 集成**：将 Pact 验证步骤加入 CI 流程，利用 Pact Broker 进行契约发布、版本管理与兼容性检查。

**生产可用性**  
- **活跃度高**：截至 2026‑06‑25，项目最近有提交，拥有 1.8k+ 星、355+ Fork，社区活跃。  
- **技术成熟**：基于 TypeScript，提供完整的 API、CLI 与 Pact Broker 集成，已在多家大型企业生产环境中使用。  
- **风险可控**：暂无重大许可证或安全隐患，仍需在正式投产前完成许可证合规与安全审计。  

综上，pact-js 具备高可用性和明确的价值主张，是在微服务或消息驱动架构中实现契约测试的可靠 OSS 选型。

## 🧭 Practical evaluation

**Value:** pact-foundation/pact-js helps teams reuse service infrastructure instead of rebuilding common backend pieces.

**Best use cases**

- ship API services faster
- reuse backend infrastructure
- standardize service patterns

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 1781 GitHub stars
- 355 forks
- updated 2026-06-25
- primary language: TypeScript
- 7 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 64/100 |
| stars | 69/100 |
| topics | 88/100 |
| outlook | 78/100 |
| quality | 79/100 |
| recency | 80/100 |
| adoption | 68/100 |
| production | 73/100 |
| usefulness | 74/100 |
| integration | 62/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 200/100 |

---

<sub>🔭 Discovered 2026-06-25 · [View on GitHub](https://github.com/pact-foundation/pact-js) · [← Back to Communication](./README.md)</sub>
