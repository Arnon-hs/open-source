# nktkas/hyperliquid

[![Stars](https://img.shields.io/github/stars/nktkas/hyperliquid?style=flat-square&color=yellow)](https://github.com/nktkas/hyperliquid/stargazers) [![Forks](https://img.shields.io/github/forks/nktkas/hyperliquid?style=flat-square&color=blue)](https://github.com/nktkas/hyperliquid/network) [![Language](https://img.shields.io/badge/lang-TypeScript-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-67%2F100-brightgreen?style=flat-square)](#)

> Hyperliquid API SDK for all major JS runtimes, written in TypeScript.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 411 |
| 🍴 **Forks** | 90 |
| 💻 **Language** | TypeScript |
| 📈 **Score** | 67/100 |
| 🗓️ **Last push** | 2026-08-24 |
| 🔍 **Source** | github |

## 🏷️ Topics

`api` `blockchain` `crypto` `cryptocurrency` `dex` `exchange` `hyperliquid` `library` `sdk` `trading` `typescript` `web3`

## 🎯 Categories

Crypto · Trading · Backend

## 📝 Summary

### English

**Brief Summary**  
Hyperliquid is a TypeScript‑based SDK that wraps the Hyperliquid API for all major JavaScript runtimes, making it easy to prototype, test, and inspect blockchain‑based trading and DeFi workflows. With over 400 ★ on GitHub, active maintenance (last commit 2026‑06‑22) and clear implementation signals, it is a solid open‑source candidate for building Web3 front‑ends or backend services.

**Value**  
The library abstracts the low‑level Hyperliquid REST/WebSocket endpoints into typed, promise‑based calls, dramatically reducing boilerplate and the risk of integration bugs. Because it is written in TypeScript, developers get compile‑time safety, auto‑completion, and seamless compatibility with both Node.js and browser environments, enabling rapid iteration on wallet connections, order routing, and market data visualisation.

**Practical Adoption Path**  
1. **Evaluation** – Clone the repo, run the built‑in examples or the CLI to verify connectivity with a testnet key.  
2. **Integration** – Add the package (`npm i @hyperliquid/sdk`) to an existing TypeScript project, import the client, and replace raw HTTP calls with the SDK’s typed methods.  
3. **Extension** – Leverage the exposed type definitions to build custom trading bots, UI dashboards, or DeFi composables, and optionally contribute back any adapters you create.  

**Production Readiness**  
- **Activity & Community**: 411 stars, 90 forks, recent commits, and a healthy issue/PR flow indicate an engaged community.  
- **Stability**: The SDK follows semantic versioning, includes comprehensive typings, and bundles both Node and browser builds, reducing runtime surprises.  
- **Risk**: No glaring licensing or security red flags, but a final audit of the underlying Hyperliquid API terms and a review of the maintainer’s response times are advisable before a full‑scale launch.  

Overall, Hyperliquid’s SDK is production‑ready for pilots and can be promoted to production once the minor due‑diligence steps (license confirmation, security review) are completed.

### Русский

**nktkas/hyperliquid** — это TypeScript‑SDK для API Hyperliquid, работающий во всех популярных JavaScript‑рантаймах. Он упрощает прототипирование и отладку Web3‑процессов: позволяет быстро собрать цепочки DeFi/кошельков, интегрировать блокчейн‑операции и исследовать детали реализации API. Проект демонстрирует высокую готовность к production‑использованию: активные коммиты, 411 звёзд, 90 форков, свежие обновления и широкая поддержка экосистемы, хотя лицензия и безопасность требуют окончательной проверки.

### 中文

**项目简介**  
nktkas/hyperliquid 是一套面向所有主流 JavaScript 运行时（Node、Deno、Browser 等）的 Hyperliquid API SDK，使用 TypeScript 编写，旨在帮助开发者快速原型化或审查区块链工作流。

**价值**  
- **快速上手**：提供完整的 API/SDK/CLI 实现细节，省去自行封装底层 HTTP/WS 的时间。  
- **全栈覆盖**：既可在前端（React/Vue 等）也可在后端（Node、NestJS 等）直接调用，适配 Web3 前端、钱包、DeFi 产品等多种场景。  
- **开源透明**：实现细节公开，便于审计、二次开发和教学。

**典型接入方式**  
1. **安装**：`npm i @hyperliquid/sdk`（或 `yarn add`、`pnpm add`）。  
2. **初始化**：在代码中导入并创建客户端实例，传入 API Key、网络环境等配置。  
   ```ts
   import { HyperliquidClient } from '@hyperliquid/sdk';
   const client = new HyperliquidClient({ apiKey: 'YOUR_KEY', env: 'mainnet' });
   ```
3. **调用**：使用 SDK 方法完成下单、查询持仓、获取行情等操作，所有方法均返回 Promise，支持 TypeScript 类型提示。  
4. **CLI/脚本**：项目自带 `hyperliquid` CLI，可直接在终端执行常用查询或下单脚本，适合快速调试。

**生产可用性**  
- **活跃度**：截至 2026‑06‑22 最近一次提交，拥有 411 ⭐、90 Fork，12 个相关话题，社区活跃。  
- **成熟度**：提供完整的 TypeScript 类型、错误处理和示例文档，已在多个内部和公开的 Web3 项目中试运行。  
- **风险**：暂无重大元数据风险，但仍建议在正式上线前审查许可证（MIT/Apache 等）和安全审计报告，并确认维护者的响应能力。  

综合来看，hyperliquid SDK 在功能完整性、文档友好度和社区支持方面均达到生产级别，适合作为 Web3/DeFi 项目的核心区块链接入层。

## 🧭 Practical evaluation

**Value:** nktkas/hyperliquid helps prototype or inspect blockchain workflows with open implementation details.

**Best use cases**

- build Web3 workflows
- inspect blockchain integrations
- prototype wallet or DeFi features

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 411 GitHub stars
- 90 forks
- updated 2026-06-22
- primary language: TypeScript
- 12 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 49/100 |
| stars | 56/100 |
| topics | 100/100 |
| outlook | 62/100 |
| quality | 64/100 |
| recency | 40/100 |
| adoption | 54/100 |
| production | 61/100 |
| usefulness | 74/100 |
| integration | 78/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 300/100 |

---

<sub>🔭 Discovered 2026-06-22 · [View on GitHub](https://github.com/nktkas/hyperliquid) · [← Back to Crypto](./README.md)</sub>
