# sumup/sumup-ios-sdk

[![Stars](https://img.shields.io/github/stars/sumup/sumup-ios-sdk?style=flat-square&color=yellow)](https://github.com/sumup/sumup-ios-sdk/stargazers) [![Forks](https://img.shields.io/github/forks/sumup/sumup-ios-sdk?style=flat-square&color=blue)](https://github.com/sumup/sumup-ios-sdk/network) [![Language](https://img.shields.io/badge/lang-Swift-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-57%2F100-brightgreen?style=flat-square)](#)

> SumUp iOS SDK.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 61 |
| 🍴 **Forks** | 33 |
| 💻 **Language** | Swift |
| 📈 **Score** | 57/100 |
| 🗓️ **Last push** | 2026-09-05 |
| 🔍 **Source** | github |

## 🏷️ Topics

`ios` `payments` `sdk` `sumup`

## 🎯 Categories

Payments · Libraries & SDKs · Mobile

## 📝 Summary

### English

**Brief Summary**  
SumUp iOS SDK is an open‑source Swift library that lets iOS developers embed SumUp’s payment processing (checkout, billing, and other PSP flows) directly into their apps. With a clean, signal‑based API it speeds up the integration of monetisation features while keeping the codebase native to iOS.  

**Value**  
- **Accelerated time‑to‑market** – the SDK abstracts the low‑level HTTP calls and security handling required for card‑present and card‑not‑present transactions, letting teams focus on UI/UX and business logic.  
- **Consistent experience** – using SumUp’s UI components and SDK‑driven error handling ensures a uniform checkout flow across devices, reducing testing overhead.  
- **Flexibility** – the library exposes raw API signals for custom workflows (e.g., subscription billing, split‑payments) while also offering high‑level convenience methods for quick prototypes.  

**Practical Adoption Path**  
1. **Evaluate** – clone the repo, run the sample app, and inspect the Swift API surface to confirm it meets the required payment scenarios.  
2. **Prototype** – add the SDK via Swift Package Manager or CocoaPods, configure the sandbox credentials, and implement a basic checkout flow using the provided UI components.  
3. **Customize & Test** – extend the SDK’s callbacks (e.g., `onTransactionSuccess`, `onError`) to integrate with your backend, run end‑to‑end tests in SumUp’s sandbox, and perform security reviews (PCI‑DSS considerations).  
4. **Productionize** – switch to live credentials, add monitoring for SDK events, and lock dependency versions; optionally contribute any missing edge‑case handling back to the project.  

**Production Readiness**  
The SDK is **moderately ready** for production: it is actively maintained (last update 2026‑05‑12), written in Swift, and has a modest community (≈ 60 stars, 33 forks). It is suitable for internal tools, pilots, or customer‑facing apps after a brief dependency audit and security review. Before a full rollout, verify the licensing terms, confirm that SumUp’s merchant account and compliance requirements are satisfied, and establish a process for monitoring SDK updates and potential breaking changes.

### Русский

SumUp iOS SDK (sumup/sumup-ios-sdk) позволяет быстро добавить в iOS‑приложения функции монетизации — интеграцию платежей, биллинга и проверку PSP‑сценариев, используя готовый Swift‑интерфейс. SDK удобно внедрять в прототипы и внутренние сервисы: достаточно подключить библиотеку и вызвать предоставленные API для оформления чека или автоматизации платёжных операций. Готовность к production — средняя: проект имеет активные коммиты, 61 звезду и 33 форка, но перед запуском в продакшн стоит проверить лицензию, безопасность и наличие поддерживающих мейнтейнеров.

### 中文

**项目简介（2‑3 句）**  
SumUp iOS SDK 是一套面向 iOS 平台的 Swift 开源库，帮助开发者在移动应用中快速接入 SumUp 的支付、结算与计费功能。通过统一的 API，开发者可以在几行代码内完成支付授权、交易创建和结果回调，从而简化 PSP（支付服务提供商）流程的实现。

**价值**  
- **加速货币化**：提供即插即用的支付 UI 与后端交互封装，显著缩短从原型到可用产品的开发周期。  
- **统一结算**：支持多种支付方式（卡片、Apple Pay 等），统一账单与对账逻辑，降低业务系统的复杂度。  
- **可评估的 PSP 流程**：通过 SDK 暴露的事件与回调，便于在内部或 A/B 测试中快速评估不同支付方案的转化率与用户体验。

**典型接入方式**  
1. **依赖管理**：使用 Swift Package Manager（推荐）或 CocoaPods 将 `sumup-ios-sdk` 添加到项目中。  
2. **初始化**：在 App 启动时使用商户提供的 API Key 调用 `Sumup.shared.initialize(...)` 完成 SDK 配置。  
3. **调用支付**：在需要结账的页面创建 `SumupPaymentRequest`，传入金额、货币、订单号等必填信息，随后调用 `Sumup.shared.startPayment(request, from: viewController)`。  
4. **结果处理**：实现 `SumupPaymentDelegate`，在 `paymentDidSucceed`、`paymentDidFail`、`paymentDidCancel` 等回调中处理成功、失败或用户取消的业务逻辑。  

**生产可用性**  
- **成熟度**：项目已有 60+ Stars、30+ Fork，最近一次提交在 2026‑05‑12，活跃度尚可。  
- **适用场景**：适合原型、内部工具以及对支付流程有明确控制需求的业务；在正式生产环境使用前建议完成以下检查：  
  - **许可证审查**：确认项目使用的开源许可证与公司合规要求匹配。  
  - **安全评估**：审查 SDK 中的网络请求、数据加密以及依赖的第三方库是否符合 PCI‑DSS 等支付安全标准。  
  - **维护性**：评估维护者响应速度，必要时可考虑自行 fork 并维持关键 bug 修复。  

总体而言，`sumup/sumup-ios-sdk` 能在中等风险可接受范围内快速实现 iOS 应用的支付功能，适合作为内部或面向小规模用户的生产方案，前提是完成上述合规与安全审查后再投入大规模上线。

## 🧭 Practical evaluation

**Value:** sumup/sumup-ios-sdk helps integrate monetization, billing, or PSP flows faster.

**Best use cases**

- integrate billing or checkout
- evaluate PSP flows
- automate payment operations

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** Medium: useful for prototypes or internal workflows, with dependency and maintenance checks before production.

**Quality signals**

- 61 GitHub stars
- 33 forks
- updated 2026-05-12
- primary language: Swift
- 4 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 38/100 |
| stars | 38/100 |
| topics | 50/100 |
| outlook | 64/100 |
| quality | 60/100 |
| recency | 80/100 |
| adoption | 38/100 |
| production | 64/100 |
| usefulness | 58/100 |
| integration | 46/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 300/100 |

---

<sub>🔭 Discovered 2026-05-12 · [View on GitHub](https://github.com/sumup/sumup-ios-sdk) · [← Back to Payments](./README.md)</sub>
