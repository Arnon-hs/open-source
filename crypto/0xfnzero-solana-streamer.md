# 0xfnzero/solana-streamer

[![Stars](https://img.shields.io/github/stars/0xfnzero/solana-streamer?style=flat-square&color=yellow)](https://github.com/0xfnzero/solana-streamer/stargazers) [![Forks](https://img.shields.io/github/forks/0xfnzero/solana-streamer?style=flat-square&color=blue)](https://github.com/0xfnzero/solana-streamer/network) [![Language](https://img.shields.io/badge/lang-Rust-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-57%2F100-brightgreen?style=flat-square)](#)

> A lightweight Rust library for real-time event streaming from Solana DEX trading programs. This library provides efficient event parsing and subscription capabilities for PumpFun, PumpSwap, Bonk, and Raydium CPMM protocols.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 170 |
| 🍴 **Forks** | 81 |
| 💻 **Language** | Rust |
| 📈 **Score** | 57/100 |
| 🗓️ **Last push** | 2026-05-14 |
| 🔍 **Source** | github |

## 🏷️ Topics

`0xfnzero` `bonk` `copytrading` `copytradingbot` `fnzero` `grpc` `jito` `letsbonk` `pumpbot` `pumpfun` `pumpswap` `raydium`

## 🎯 Categories

Crypto · Payments · Trading · Automation

## 📝 Summary

### English

**Brief Summary (2‑3 sentences)**  
0xfnzero/solana‑streamer is a lightweight Rust library that lets developers tap into real‑time event streams from popular Solana DEX trading programs such as PumpFun, PumpSwap, Bonk, and Raydium CPMM. It offers fast on‑chain event parsing and subscription APIs, making it easy to prototype, debug, or monitor DeFi workflows on Solana.

**Value**  
- **Transparency & Speed** – By exposing the raw event data and parsing logic, the library lets teams see exactly what’s happening on‑chain, which is invaluable for debugging, audit trails, and building analytics dashboards.  
- **Multi‑protocol support** – One unified API covers several high‑volume DEXs, reducing the need to maintain separate connectors for each protocol.  
- **Open‑source & Community‑backed** – With ~170 stars and active maintenance (last update 2026‑05‑14), the codebase is mature enough to serve as a reference implementation for wallet, trading bot, or DeFi‑automation projects.

**Practical Adoption Path**  
1. **Proof‑of‑Concept** – Clone the repo, run the provided examples, and confirm you can subscribe to a single DEX (e.g., Raydium) in a sandbox or testnet environment.  
2. **Integration Layer** – Wrap the library in a thin service (e.g., a Rust microservice or a language‑binding wrapper) that exposes the event stream via HTTP/WebSocket or a message queue (Kafka, NATS).  
3. **Feature Expansion** – Add the remaining protocol subscriptions, implement filtering/aggregation logic, and integrate with your existing Web3 or analytics stack.  
4. **Testing & Monitoring** – Write integration tests against Solana’s devnet, and set up health checks for the streaming service to catch connectivity or parsing failures early.

**Production Readiness**  
- **Maturity**: Medium. The library is actively maintained and has a decent community footprint, but it is primarily aimed at prototyping and internal tooling.  
- **Dependencies**: Review the crate’s transitive dependencies for security and licensing compliance before shipping to production.  
- **Operational Considerations**: Because the integration path isn’t fully documented, allocate time for initial setup, configuration of RPC endpoints, and handling rate‑limit or node‑failure scenarios.  
- **Recommendation**: Deploy first as a non‑critical service (e.g., for monitoring or internal dashboards). Once the streaming component proves stable under load, you can promote it to production workloads such as automated trading bots or wallet event notifications.

### Русский

**0xfnzero/solana-streamer** — лёгкая библиотека на Rust для получения и парсинга событий в реальном времени из торговых программ Solana (PumpFun, PumpSwap, Bonk, Raydium CPMM). Она позволяет быстро построить прототипы Web3‑воркфлоу, отладить интеграцию DeFi‑протоколов или реализовать базовые функции кошелька/трейдинга, начиная с небольшого proof‑of‑concept и проверки README. Готовность к production — средняя: библиотека стабильно поддерживается (170 ★, 81 fork, обновлена 2026‑05‑14), но требует предварительной проверки зависимостей и уточнения пути интеграции перед масштабным использованием.

### 中文

**项目简介**  
0xfnzero/solana‑streamer 是一个轻量级的 Rust 库，专注于实时读取并解析 Solana 上常见 DEX（PumpFun、PumpSwap、Bonk、Raydium CPMM）的交易事件。它提供高效的事件订阅接口，帮助开发者快速搭建或调试区块链交易工作流。

**价值**  
- **快速原型**：无需自行实现底层 RPC 与日志解析，直接使用库即可获取完整的交易事件流，适合原型开发和概念验证。  
- **透明实现**：开源代码公开了事件解码细节，便于审计、学习和定制。  
- **多协议支持**：一次集成即可覆盖四大主流 Solana DEX，降低维护成本。

**典型接入方式**  
1. **阅读 README**，确认所需的 Solana RPC 节点（如官方或自建）可达。  
2. **在 Cargo.toml** 中加入依赖：  
   ```toml
   solana-streamer = "0.x"
   ```  
3. **创建 `Streamer` 实例**，指定要监听的协议（PumpFun、PumpSwap、Bonk、Raydium）。  
4. **注册回调或使用 async stream**，在业务代码中处理 `Event`（如订单创建、成交、撤单）。  
5. **在小型 PoC** 中验证事件完整性后，逐步迁移到生产服务（可配合 `tokio`、`async‑std` 等运行时）。

**生产可用性**  
- **成熟度**：已有 170+ 星、81 次 fork，近期（2026‑05‑14）仍在维护，代码质量较好。  
- **适用场景**：内部工具、监控系统、DeFi 原型或钱包功能的快速实现。  
- **上线建议**：在正式环境前进行依赖审计（Rust 版本、Solana RPC 稳定性），并做一次完整的集成测试；如需高可用，可自行实现重连、限流和错误恢复逻辑。总体上，库适合作为 **中等** 生产级别的组件，前提是做好运维和安全检查。

## 🧭 Practical evaluation

**Value:** 0xfnzero/solana-streamer helps prototype or inspect blockchain workflows with open implementation details.

**Best use cases**

- build Web3 workflows
- inspect blockchain integrations
- prototype wallet or DeFi features

**Integration notes:** Looks feasible to evaluate, but integration should start with a small proof of concept and README check.

**Production readiness:** Medium: useful for prototypes or internal workflows, with dependency and maintenance checks before production.

**Quality signals**

- 170 GitHub stars
- 81 forks
- updated 2026-05-14
- primary language: Rust
- 19 topics

**Risks:** Integration path is not obvious from metadata; validate setup cost before committing.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 48/100 |
| stars | 48/100 |
| topics | 100/100 |
| outlook | 75/100 |
| quality | 76/100 |
| recency | 100/100 |
| adoption | 48/100 |
| production | 73/100 |
| usefulness | 42/100 |
| integration | 30/100 |
| sourceTrust | 100/100 |

---

<sub>🔭 Discovered 2026-05-14 · [View on GitHub](https://github.com/0xfnzero/solana-streamer) · [← Back to Crypto](./README.md)</sub>
