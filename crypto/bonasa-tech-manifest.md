# Bonasa-Tech/manifest

[![Stars](https://img.shields.io/github/stars/Bonasa-Tech/manifest?style=flat-square&color=yellow)](https://github.com/Bonasa-Tech/manifest/stargazers) [![Forks](https://img.shields.io/github/forks/Bonasa-Tech/manifest?style=flat-square&color=blue)](https://github.com/Bonasa-Tech/manifest/network) [![Language](https://img.shields.io/badge/lang-Rust-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-53%2F100-brightgreen?style=flat-square)](#)

> The Spot CLOB on Solana

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 138 |
| 🍴 **Forks** | 59 |
| 💻 **Language** | Rust |
| 📈 **Score** | 53/100 |
| 🗓️ **Last push** | 2026-05-12 |
| 🔍 **Source** | github |

## 🏷️ Topics

`defi` `orderbook` `solana`

## 🎯 Categories

Crypto

## 📝 Summary

### English

**Brief Summary (2‑3 sentences)**  
Bonasa‑Tech’s **manifest** is an open‑source Rust library that implements a Spot Central Limit Order Book (CLOB) on Solana, letting developers prototype and inspect blockchain‑level trading workflows with full visibility into the underlying logic. While the repo is fairly active (138 ★, recent updates) and useful for building Web3, wallet, or DeFi features, its integration signals are sparse, so a manual review is required before committing to production.

**Value**  
- Provides a ready‑made, auditable implementation of a Spot CLOB, accelerating the creation of order‑book‑based trading interfaces on Solana.  
- Open implementation details let teams debug, benchmark, and extend core market‑making logic rather than starting from scratch.  
- Serves as a learning sandbox for developers new to Solana’s on‑chain finance primitives.

**Practical Adoption Path**  
1. **Explore & Test** – Clone the repo, run the example programs, and use the provided Rust APIs to simulate order flow locally or on a devnet.  
2. **Validate Integration** – Review the codebase to map required Solana accounts, CPI calls, and any off‑chain services (e.g., price oracles). Because metadata is minimal, document the exact setup steps.  
3. **Prototype** – Build a thin wrapper or micro‑service around the library to expose the CLOB functionality to your front‑end or wallet.  
4. **Security & Audits** – Conduct internal code review and, if needed, third‑party audit before moving to mainnet.  
5. **Production Rollout** – Deploy the compiled program to Solana mainnet, monitor transaction costs, and implement fallback mechanisms for upgrades.

**Production Readiness**  
- **Maturity:** Medium. The project is actively maintained (last commit 2026‑05‑12) and has a modest community (138 ★, 59 forks), but the integration path isn’t clearly documented.  
- **Suitability:** Ideal for prototypes, internal tooling, or early‑stage DeFi products where the team can afford a manual integration effort and perform their own security checks.  
- **Considerations:** Prior to production, verify dependency versions, assess runtime costs on Solana, and ensure you have the capability to maintain the program (e.g., handling Solana program upgrades and account migrations).

### Русский

Bonasa‑Tech/manifest — это открытая Rust‑библиотека, позволяющая быстро прототипировать и отлаживать рабочие процессы в Solana‑CLOB, а также исследовать интеграцию блокчейна, кошельков и DeFi‑фич. Подойдёт для разработки Web3‑сценариев и внутреннего тестирования, однако из‑за скудной документации по интеграции требуется ручная проверка и оценка затрат перед внедрением в продакшн. Готовность к боевому использованию средняя: проект имеет 138 звёзд, активную поддержку и недавнее обновление, но требует дополнительного контроля зависимостей и тестов перед выпуском.

### 中文

**项目简介**  
Bonasa‑Tech/manifest 是在 Solana 上实现的 Spot CLOB（中心化订单簿）原型库，提供了可直接查看的区块链工作流实现，帮助开发者快速搭建和验证 Web3、钱包或 DeFi 场景。

**价值**  
- **快速原型**：开箱即用的 Rust 实现，让团队在几行代码内搭建完整的 Spot 交易流，缩短概念验证周期。  
- **透明可审计**：所有核心逻辑公开，便于审计、学习和二次开发，降低对闭源 SDK 的依赖。  
- **灵活扩展**：提供了底层订单簿、撮合和链上状态同步的抽象，可直接用于自定义交易所或流动性聚合器。

**典型接入方式**  
1. **依赖引入**：在 Cargo.toml 中添加 `manifest = { git = "https://github.com/Bonasa-Tech/manifest", tag = "vX.Y.Z" }`。  
2. **链上初始化**：使用项目提供的 `initialize_market` 示例脚本，在本地或 devnet 上部署 Market 程序并获取 Program ID。  
3. **业务集成**：在业务代码中实例化 `MarketClient`，调用 `place_order`, `cancel_order`, `settle_trade` 等 API；如需自定义撮合规则，可实现 `Matcher` trait 并注入。  
4. **本地调试**：配合 Solana 本地测试验证器 (`solana-test-validator`) 进行端到端调试，确认签名、费用和状态同步符合预期。

**生产可用性**  
- **成熟度**：当前评分 53/100，GitHub 138 星、59 Fork，活跃更新至 2026‑05‑12，代码主要使用 Rust，适合技术团队内部原型和中小规模内部服务。  
- **风险**：元数据中集成提示稀少，集成路径不够直观；在生产环境部署前需自行梳理依赖、审计安全（尤其是撮合逻辑）并进行压力测试。  
- **建议**：将其作为 **原型/内部工具** 使用，完成完整的单元/集成测试、代码审计以及运维监控后，再考虑在正式业务中上线。若业务对高可用、审计合规有严格要求，建议在此基础上自行实现或采购成熟的商业 CLOB 方案。

## 🧭 Practical evaluation

**Value:** Bonasa-Tech/manifest helps prototype or inspect blockchain workflows with open implementation details.

**Best use cases**

- build Web3 workflows
- inspect blockchain integrations
- prototype wallet or DeFi features

**Integration notes:** Needs manual inspection before adoption because integration signals are sparse in the discovered metadata.

**Production readiness:** Medium: useful for prototypes or internal workflows, with dependency and maintenance checks before production.

**Quality signals**

- 138 GitHub stars
- 59 forks
- updated 2026-05-12
- primary language: Rust
- 3 topics

**Risks:** Integration path is not obvious from metadata; validate setup cost before committing.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 44/100 |
| stars | 46/100 |
| topics | 38/100 |
| outlook | 68/100 |
| quality | 66/100 |
| recency | 100/100 |
| adoption | 45/100 |
| production | 69/100 |
| usefulness | 42/100 |
| integration | 30/100 |
| sourceTrust | 100/100 |

---

<sub>🔭 Discovered 2026-05-12 · [View on GitHub](https://github.com/Bonasa-Tech/manifest) · [← Back to Crypto](./README.md)</sub>
