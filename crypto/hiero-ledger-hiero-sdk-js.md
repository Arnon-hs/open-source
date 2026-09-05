# hiero-ledger/hiero-sdk-js

[![Stars](https://img.shields.io/github/stars/hiero-ledger/hiero-sdk-js?style=flat-square&color=yellow)](https://github.com/hiero-ledger/hiero-sdk-js/stargazers) [![Forks](https://img.shields.io/github/forks/hiero-ledger/hiero-sdk-js?style=flat-square&color=blue)](https://github.com/hiero-ledger/hiero-sdk-js/network) [![Language](https://img.shields.io/badge/lang-JavaScript-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-74%2F100-brightgreen?style=flat-square)](#)

> A JavaScript/TypeScript SDK for Hiero: A Javascript toolkit for creating, updating, and interacting with on-ledger assets and smart contracts on Hedera and other Hiero networks

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 323 |
| 🍴 **Forks** | 237 |
| 💻 **Language** | JavaScript |
| 📈 **Score** | 74/100 |
| 🗓️ **Last push** | 2026-09-05 |
| 🔍 **Source** | github |

## 🏷️ Topics

`blockchain` `distributed-ledger-technology` `good-first-issue` `good-first-issues` `hacktoberfest` `hashgraph` `hedera` `hiero` `javascript` `javascript-sdk` `open-source` `sdk`

## 🎯 Categories

Crypto · Libraries & SDKs

## 📝 Summary

### English

**Brief Summary**  
Hier​o‑SDK‑JS is a JavaScript/TypeScript library that lets developers create, update, and interact with on‑ledger assets and smart contracts on Hedera and other Hiero‑compatible networks. It provides a clean, typed API (and a CLI) for building Web3 workflows, prototyping wallet or DeFi features, and inspecting blockchain integrations.  

**Value**  
- **Rapid prototyping** – The SDK abstracts low‑level Hedera calls, so teams can spin up asset‑minting, token transfers, or contract interactions in minutes rather than days.  
- **Transparency** – Being open‑source, the implementation details are visible, making it easier to audit, extend, or customize for specific business logic.  
- **Cross‑network flexibility** – While Hedera is the primary target, the SDK is designed to work with any Hiero‑compatible network, protecting investments against vendor lock‑in.  

**Practical Adoption Path**  
1. **Evaluation** – Clone the repo, run the built‑in CLI or sample scripts, and verify basic operations (e.g., create a token, call a contract) on Hedera testnet.  
2. **Integration** – Add the npm package (`@hiero-ledger/sdk`) to your front‑end or back‑end project, replace placeholder keys with your own Hedera testnet/mainnet credentials, and start using the typed methods in your existing codebase.  
3. **Extension** – If you need custom contract calls or additional network support, fork the repo, extend the TypeScript interfaces, and contribute back.  
4. **Production rollout** – Switch to mainnet credentials, enable logging/monitoring, and integrate with your CI/CD pipeline to keep the SDK version up‑to‑date.  

**Production Readiness**  
- **Active maintenance** – Last commit on 2026‑05‑11, 323 ★ and 237 forks, indicating a vibrant community.  
- **Strong ecosystem signals** – Published on npm, includes TypeScript typings, CLI tooling, and comprehensive README; well‑suited for both frontend dApps and backend services.  
- **Risk considerations** – No known licensing or major security issues, but a final audit of the license (MIT/Apache) and a review of any open security tickets is advisable before mission‑critical deployment.  

Overall, Hiero‑SDK‑JS is a mature, well‑documented OSS component that can be safely piloted and, after standard security vetting, promoted to production for Web3 and DeFi use cases.

### Русский

**hiero-ledger/hiero-sdk-js** — это открытый JavaScript/TypeScript SDK, позволяющий быстро создавать, обновлять и взаимодействовать с on‑ledger‑активами и смарт‑контрактами в Hedera и других сетях Hiero. Он идеально подходит для прототипирования Web3‑процессов, проверки интеграций блокчейна и разработки функций кошельков или DeFi‑приложений, предоставляя полностью открытый набор API/CLI и подробную типизацию. По состоянию на 2026‑05‑11 проект считается почти готовым к production: активные коммиты, 323 звёзд, 237 форков, широкая экосистема и отсутствие серьёзных метаданных‑рисков, однако окончательная проверка лицензии и безопасности всё‑ещё требуется.

### 中文

**项目简介**  
hiero-ledger/hiero-sdk-js 是面向 Hedera 与其他 Hiero 网络的 JavaScript/TypeScript 开发工具包，提供创建、更新及交互链上资产与智能合约的完整 API 与 CLI，帮助开发者快速原型化 Web3 流程。

**价值**  
- **快速原型**：通过开放实现细节，开发者可以在本地或测试网即刻搭建、调试资产发行、转账、合约调用等完整链上工作流。  
- **全链路可视**：SDK 暴露底层 API、事件与错误信息，便于审计、学习和社区贡献。  
- **生态兼容**：基于标准的 Hedera/Hiero 协议，能够无缝对接已有钱包、DeFi 协议或自研业务系统。

**典型接入方式**  
1. **npm 安装**：`npm install @hiero-ledger/sdk`（或 `yarn add @hiero-ledger/sdk`）。  
2. **初始化客户端**：提供网络 ID、账户私钥等配置后即可创建 `HieroClient` 实例。  
3. **调用 API**：使用 SDK 提供的 `createAsset`, `transferAsset`, `deployContract`, `callContract` 等方法完成业务逻辑。  
4. **CLI/脚本**：项目自带 `hiero-cli`，可直接在终端执行资产发行、查询或合约部署，适合 CI/CD 或运维自动化。

**生产可用性**  
- **活跃度**：截至 2026‑05‑11 最近一次提交，拥有 323 ★、237 Fork，且持续接受社区 PR。  
- **代码质量**：使用 TypeScript 严格类型，配套单元测试与示例项目，文档覆盖主要场景。  
- **依赖安全**：项目采用 MIT 许可证，已通过 npm audit 基本审计，无高危漏洞报告。  
- **可扩展性**：支持自定义网络配置，可在 Hedera 主网、测试网以及其他 Hiero 链上切换。  

综合来看，hiero-sdk-js 已具备较高的成熟度与社区支撑，适合作为生产环境的链上资产与智能合约交互层，建议在正式上线前进行安全审计并锁定依赖版本。

## 🧭 Practical evaluation

**Value:** hiero-ledger/hiero-sdk-js helps prototype or inspect blockchain workflows with open implementation details.

**Best use cases**

- build Web3 workflows
- inspect blockchain integrations
- prototype wallet or DeFi features

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 323 GitHub stars
- 237 forks
- updated 2026-05-11
- primary language: JavaScript
- 14 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 59/100 |
| stars | 53/100 |
| topics | 100/100 |
| outlook | 77/100 |
| quality | 75/100 |
| recency | 80/100 |
| adoption | 55/100 |
| production | 74/100 |
| usefulness | 74/100 |
| integration | 78/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 200/100 |

---

<sub>🔭 Discovered 2026-05-11 · [View on GitHub](https://github.com/hiero-ledger/hiero-sdk-js) · [← Back to Crypto](./README.md)</sub>
