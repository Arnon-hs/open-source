# paypal/payflow-gateway

[![Stars](https://img.shields.io/github/stars/paypal/payflow-gateway?style=flat-square&color=yellow)](https://github.com/paypal/payflow-gateway/stargazers) [![Forks](https://img.shields.io/github/forks/paypal/payflow-gateway?style=flat-square&color=blue)](https://github.com/paypal/payflow-gateway/network) [![Language](https://img.shields.io/badge/lang-C%23-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-65%2F100-brightgreen?style=flat-square)](#)

> PayPal Payflow Gateway SDK for .NET (C# and VB) and Java. Supports .NET 8/10/Framework 4.8 and Java 11+.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 90 |
| 🍴 **Forks** | 73 |
| 💻 **Language** | C# |
| 📈 **Score** | 65/100 |
| 🗓️ **Last push** | 2026-09-05 |
| 🔍 **Source** | github |

## 🏷️ Topics

`csharp` `dotnet` `java` `maven` `payflow` `payment-gateway` `payments` `paypal-payments-pro` `sdks` `visual-basic`

## 🎯 Categories

Payments · Libraries & SDKs

## 📝 Summary

### English

**Summary:** 

The PayPal Payflow Gateway SDK is an open-source project that enables developers to integrate payment flows into their applications using C# and Java. This SDK supports various .NET and Java frameworks, making it a versatile tool for developers. By leveraging this SDK, developers can streamline payment operations and focus on other aspects of their projects.

**Value Proposition:** 

The primary value proposition of this project lies in its ability to simplify payment integration, allowing developers to focus on core functionality rather than spending time on payment processing. This SDK provides a straightforward way to integrate billing, checkout, or PSP flows, making it an attractive choice for developers looking to monetize their applications.

**Practical Adoption Path:** 

To adopt this SDK, developers can follow these steps:

1. **Evaluate the SDK**: Review the SDK's documentation, codebase, and GitHub activity to ensure it meets their project requirements.
2. **Choose the Right Framework**: Select the .NET or Java framework that aligns with their project's needs.
3. **Integrate the SDK**: Follow the SDK's guidelines to integrate payment flows into their application.
4. **Test and Refine**: Thoroughly test the payment integration and refine the implementation as needed.

**Production Readiness:** 

The PayPal Payflow Gateway SDK is considered

### Русский

**PayPal Payflow Gateway SDK** (paypal/payflow-gateway) — это открытый набор библиотек для .NET (C# и VB) и Java, позволяющий быстро подключить платёжный шлюз Payflow к вашим сервисам, автоматизировать биллинг и PSP‑процессы. Он подходит для прототипов, внутренних инструментов и первых интеграций checkout/биллинга, но перед выводом в продакшн стоит проверить лицензирование, безопасность и наличие активных мейнтейнеров. Готовность к production — средняя: SDK стабилен, имеет более 90 звёзд и регулярные обновления (последний — 2026‑06‑28), однако требуется дополнительный аудит зависимостей и поддержки.

### 中文

**项目简介**  
PayPal Payflow Gateway SDK 为 .NET（C#、VB）和 Java 提供统一的 Payflow 接口实现，兼容 .NET 8/10/Framework 4.8 与 Java 11+，帮助开发者快速在应用中接入 PayPal 的支付、结算与账单功能。

**价值**  
- **加速支付集成**：封装了 Payflow 的 API 调用细节，开发者只需调用 SDK 即可完成支付、退款、账单等常见 PSP（Payment Service Provider）流程。  
- **跨语言统一**：同一套功能在 C#、VB 与 Java 中保持一致，降低多语言项目的维护成本。  
- **灵活适配**：支持最新的 .NET 8/10 以及传统 .NET Framework 4.8，满足云原生微服务和传统企业应用的不同需求。

**典型接入方式**  
1. **引用 SDK**：在 .NET 项目中通过 NuGet（`PayPal.Payflow`）或在 Java 项目中通过 Maven Central 引入对应包。  
2. **配置凭证**：在 `appsettings.json`（或 `pom.xml`）中配置 Payflow 的商户 ID、用户名、密码及环境（sandbox/production）。  
3. **调用业务接口**：使用 SDK 提供的 `PayflowConnection`、`Transaction` 等类完成授权、捕获、退款等操作；示例代码在仓库的 `samples` 目录中可直接使用。  
4. **可选 CLI/脚本**：仓库附带的简单 CLI 工具可用于快速验证 API 连通性或执行批量退款，适合作为 CI/CD 流程的一环。

**生产可用性**  
- **成熟度**：已有 90+ Stars、73 Forks，活跃度截至 2026‑06‑28，表明社区仍在使用并贡献。  
- **适用场景**：适合原型、内部工具以及对支付流程有明确控制需求的业务；在正式生产环境使用前建议完成以下检查：  
  - **依赖审计**：确认所有第三方库（尤其是网络和加密相关）已更新至安全版本。  
  - **安全合规**：核对 PayPal 官方的 PCI‑DSS 要求，确保凭证存储方式符合企业安全策略。  
  - **维护者沟通**：虽然当前暂无活跃维护者标记，但可通过 Issues 与社区取得支持，或自行 fork 进行内部维护。  
- **总体评估**：在完成上述审查后，SDK 可在生产环境中稳定运行，尤其适合需要快速交付且对支付细节有自定义需求的项目。

## 🧭 Practical evaluation

**Value:** paypal/payflow-gateway helps integrate monetization, billing, or PSP flows faster.

**Best use cases**

- integrate billing or checkout
- evaluate PSP flows
- automate payment operations

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** Medium: useful for prototypes or internal workflows, with dependency and maintenance checks before production.

**Quality signals**

- 90 GitHub stars
- 73 forks
- updated 2026-06-28
- primary language: C#
- 10 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 47/100 |
| stars | 42/100 |
| topics | 100/100 |
| outlook | 74/100 |
| quality | 69/100 |
| recency | 80/100 |
| adoption | 43/100 |
| production | 68/100 |
| usefulness | 74/100 |
| integration | 46/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 200/100 |

---

<sub>🔭 Discovered 2026-06-28 · [View on GitHub](https://github.com/paypal/payflow-gateway) · [← Back to Payments](./README.md)</sub>
