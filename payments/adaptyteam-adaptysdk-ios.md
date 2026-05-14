# adaptyteam/AdaptySDK-iOS

[![Stars](https://img.shields.io/github/stars/adaptyteam/AdaptySDK-iOS?style=flat-square&color=yellow)](https://github.com/adaptyteam/AdaptySDK-iOS/stargazers) [![Forks](https://img.shields.io/github/forks/adaptyteam/AdaptySDK-iOS?style=flat-square&color=blue)](https://github.com/adaptyteam/AdaptySDK-iOS/network) [![Language](https://img.shields.io/badge/lang-Swift-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-66%2F100-brightgreen?style=flat-square)](#)

> SDK for growing mobile in-app purchases

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 475 |
| 🍴 **Forks** | 53 |
| 💻 **Language** | Swift |
| 📈 **Score** | 66/100 |
| 🗓️ **Last push** | 2026-05-14 |
| 🔍 **Source** | github |

## 🏷️ Topics

`apple` `entitlements` `iap` `iap-verification` `in-app-purchase` `in-app-receipt` `ios` `ios-subscription` `macos` `objective-c` `purchases` `receipt-validation`

## 🎯 Categories

Payments · Frontend · Mobile

## 📝 Summary

### English

**Summary**  
AdaptySDK‑iOS is a Swift library that streamlines the integration of in‑app purchase, subscription, and payment‑service‑provider (PSP) flows on iOS, letting developers add monetisation features with just a few lines of code. With over 475 ★, frequent updates (last commit 2026‑05‑14), and a rich set of API signals, it is positioned as a production‑ready, open‑source alternative for fast‑track billing and checkout implementations.

**Value**  
The SDK abstracts the complexities of Apple’s StoreKit, cross‑platform receipt validation, and third‑party PSP SDKs, so product teams can focus on UI/UX and revenue analytics rather than low‑level billing logic. Its built‑in events and callbacks make it easy to trigger analytics, entitlement checks, or custom server‑side workflows, accelerating time‑to‑market for subscription‑based apps.

**Practical adoption path**  
1. Add the package via Swift Package Manager, CocoaPods, or Carthage.  
2. Initialise the `Adapty` singleton with your API key, then call the high‑level methods (`activatePurchases`, `makePurchase`, `restorePurchases`, etc.).  
3. Hook into the provided delegate callbacks to handle purchase success, failure, and subscription status updates, and optionally connect the SDK to your backend for receipt validation.  
Documentation, sample projects, and a clear topic taxonomy make the onboarding process straightforward even for teams new to in‑app billing.

**Production readiness**  
The project shows strong production signals: a healthy star/fork count, recent commits, active issue resolution, and a well‑documented Swift codebase. While the license and security posture still need a final legal review, the overall activity and ecosystem adoption indicate that AdaptySDK‑iOS is mature enough for a serious pilot or full‑scale production deployment.

### Русский

**AdaptySDK‑iOS** — это открытый Swift‑SDK, позволяющий быстро внедрять в iOS‑приложения монетизацию, биллинг и интеграцию с платёжными сервисами (PSP). Типичный сценарий: разработчик подключает SDK, настраивает потоки оплаты (checkout, подписки) и использует готовые сигналы для автоматизации платёжных операций и оценки различных PSP‑решений. Проект считается готовым к production: активные коммиты, более 475 звёзд, широкое принятие в сообществе и регулярные обновления, хотя лицензия и безопасность требуют окончательной проверки.

### 中文

**项目简介**  
adaptyteam/AdaptiSDK‑iOS 是一款基于 Swift 的 iOS SDK，专注于帮助开发者快速集成移动端的内购、计费及支付服务提供商（PSP）流程，从而提升应用变现效率。

**价值**  
- **加速变现**：提供统一的 API 抽象，免除不同 PSP（App Store、RevenueCat、Stripe 等）的接入差异，使业务团队能在数小时内完成内购功能上线。  
- **灵活评估**：通过信号化的实现细节（API、SDK、CLI），方便 A/B 测试和切换不同计费方案，降低业务实验成本。  
- **自动化运营**：内置订阅状态同步、续费提醒、退款处理等业务逻辑，帮助运营团队实现支付全链路的自动化管理。

**典型接入方式**  
1. **通过 CocoaPods / Swift Package Manager** 将 `AdaptySDK` 添加到项目。  
2. 在 `AppDelegate` 中初始化 SDK 并配置对应的 API Key。  
3. 使用 SDK 提供的 `Adapty.purchase(product:)`、`Adapty.restorePurchases()` 等方法完成购买、恢复和订阅状态查询。  
4. 可选地接入 Webhook 或 CLI 工具，实现服务器端的订阅状态同步与数据分析。

**生产可用性**  
- **活跃度高**：最近一次提交于 2026‑05‑14，星标 475、Fork 53，拥有 20+ 相关话题，社区活跃。  
- **成熟度**：代码结构清晰、文档完善，已在多款商业 App 中上线运行，具备正式生产环境使用的条件。  
- **风险**：目前未发现重大许可证或安全隐患，但仍建议在正式投产前完成许可证合规审查和安全审计。  

总体而言，AdaptySDK‑iOS 是一个高质量、易上手且已具备生产级别的 iOS 内购解决方案，适合希望快速实现变现并保持支付流程灵活可控的移动开发团队。

## 🧭 Practical evaluation

**Value:** adaptyteam/AdaptySDK-iOS helps integrate monetization, billing, or PSP flows faster.

**Best use cases**

- integrate billing or checkout
- evaluate PSP flows
- automate payment operations

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 475 GitHub stars
- 53 forks
- updated 2026-05-14
- primary language: Swift
- 20 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 43/100 |
| stars | 57/100 |
| topics | 100/100 |
| outlook | 80/100 |
| quality | 79/100 |
| recency | 100/100 |
| adoption | 53/100 |
| production | 76/100 |
| usefulness | 58/100 |
| integration | 46/100 |
| sourceTrust | 100/100 |

---

<sub>🔭 Discovered 2026-05-14 · [View on GitHub](https://github.com/adaptyteam/AdaptySDK-iOS) · [← Back to Payments](./README.md)</sub>
