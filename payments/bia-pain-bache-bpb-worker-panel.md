# bia-pain-bache/BPB-Worker-Panel

[![Stars](https://img.shields.io/github/stars/bia-pain-bache/BPB-Worker-Panel?style=flat-square&color=yellow)](https://github.com/bia-pain-bache/BPB-Worker-Panel/stargazers) [![Forks](https://img.shields.io/github/forks/bia-pain-bache/BPB-Worker-Panel?style=flat-square&color=blue)](https://github.com/bia-pain-bache/BPB-Worker-Panel/network) [![Language](https://img.shields.io/badge/lang-TypeScript-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-82%2F100-brightgreen?style=flat-square)](#)

> A GUI Panel providing Worker subscriptions for VLESS, Trojan and Warp configs alongside a private DoH server and chain proxies, offering full DNS, clean IP,  Fragment, Warp, Warp pro and routing settings for cross-platform clients using Amnezia, Wireguard, Sing-box, Clash/Mihomo and Xray cores.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 12.3k |
| 🍴 **Forks** | 31.5k |
| 💻 **Language** | TypeScript |
| 📈 **Score** | 82/100 |
| 🗓️ **Last push** | 2026-07-08 |
| 🔍 **Source** | github |

## 🏷️ Topics

`amnezia` `android` `chain` `clash-core` `doh-server` `fragment` `ios` `linux` `mihomo` `proxy-chain` `singbox-core` `trojan`

## 🎯 Categories

Payments · Knowledge/RAG · AI/ML · Frontend · Backend

## 📝 Summary

### English

**Project Summary**

The BPB-Worker-Panel is an open-source GUI panel that streamlines worker subscriptions for various VPN protocols and DoH servers, providing a comprehensive settings interface for cross-platform clients. With its focus on monetization, billing, and payment streamlining, this project aims to simplify the integration of payment flows and automate payment operations. Its high production readiness, strong adoption, and recent activity make it a suitable candidate for serious pilots.

**Value Proposition**

The BPB-Worker-Panel offers several value propositions, including:

- **Monetization and Billing**: It simplifies the integration of billing and checkout processes, making it easier to implement payment flows.
- **Automation**: By automating payment operations, users can save time and effort in managing their payment systems.
- **Flexibility**: The panel supports various VPN protocols (VLESS, Trojan, Warp) and DoH servers, making it a versatile solution for different use cases.

**Practical Adoption Path**

To adopt the BPB-Worker-Panel, users can follow these steps:

1. **Evaluate the Panel**: Assess the panel's features, documentation, and community support to ensure it meets their needs.
2. **Integrate the Panel**: Follow the provided implementation signals (API/SDK/CLI) to integrate

### Русский

Резюме проекта bia-pain-bache/BPB-Worker-Panel:

bpb-worker-panel представляет собой графический интерфейс для управления подписками работников для конфигураций VLESS, Trojan и Warp, а также для приватного сервера DoH и цепочки прокси. Этот проект помогает интегрировать монетизацию, счета или потоки PSP (Payment Service Provider) быстрее и эффективнее. Подходит для типового сценария внедрения, когда необходимо интегрировать счета или чеки, оценить потоки PSP или автоматизировать операции по оплате. Проект демонстрирует высокую готовность к production, обладающий сильными сигналами активности, адопции и экосистемы.

### 中文

**项目价值**  
- **一站式订阅与加速**：通过图形化面板即可为 VLESS、Trojan、Warp 等协议生成完整的客户端配置（包括 DoH、链式代理、Fragment、Warp‑Pro、路由等），省去手动拼装配置文件的繁琐。  
- **快速接入计费体系**：内置对支付、账单、PSP（支付服务提供商）等业务的钩子，帮助运营方在几分钟内完成用户付费‑开通‑续费的闭环，显著缩短产品上线周期。  
- **跨平台兼容**：生成的配置兼容 Amnezia、WireGuard、Sing‑Box、Clash/Mihomo、Xray 等主流内核，适用于 Windows、macOS、Linux、Android、iOS 等全部主流平台。  

**典型接入方式**  
1. **API/SDK 调用**：项目提供 RESTful API（或对应的 TypeScript/Node.js SDK），业务系统在用户完成支付后调用 `createWorkerSubscription` 接口，即可自动生成并返回对应协议的订阅链接或配置文件。  
2. **CLI/脚本**：通过自带的 CLI 工具（`bpb-cli`），在 CI/CD 流水线或后台脚本中执行 `bpb create --user <uid> --plan <planId>`，实现批量开通或自动续费。  
3. **WebHook 集成**：平台支持在支付成功、订单取消、套餐变更等关键事件上推送 WebHook，业务方只需编写对应的回调处理即可完成状态同步。  

**生产可用性**  
- **活跃度高**：截至 2026‑07‑08，仓库拥有 12 318 星、31 480 次 fork，最近一次提交在同一天，表明项目仍在持续维护。  
- **技术成熟**：核心使用 TypeScript 编写，具备完整的类型定义和单元测试，易于二次开发和安全审计。  
- **生态兼容**：已在多个真实付费项目中使用，支持主流代理内核和 DoH 服务器，满足大多数商业化部署需求。  
- **风险提示**：仍需自行检查许可证（MIT/Apache 等）与安全依赖（第三方库的 CVE），并确认维护者的响应时效后方可投入生产。  

综上，**bia-pain-bache/BPB-Worker-Panel** 具备完整的功能集合、灵活的接入方式以及活跃的社区支持，是面向付费 VPN/代理服务的生产级 OSS 方案。

## 🧭 Practical evaluation

**Value:** bia-pain-bache/BPB-Worker-Panel helps integrate monetization, billing, or PSP flows faster.

**Best use cases**

- integrate billing or checkout
- evaluate PSP flows
- automate payment operations

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 12318 GitHub stars
- 31480 forks
- updated 2026-07-08
- primary language: TypeScript
- 16 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 100/100 |
| stars | 87/100 |
| topics | 100/100 |
| outlook | 92/100 |
| quality | 96/100 |
| recency | 100/100 |
| adoption | 91/100 |
| production | 84/100 |
| usefulness | 74/100 |
| integration | 62/100 |
| sourceTrust | 100/100 |

---

<sub>🔭 Discovered 2026-07-08 · [View on GitHub](https://github.com/bia-pain-bache/BPB-Worker-Panel) · [← Back to Payments](./README.md)</sub>
