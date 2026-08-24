# cardano-foundation/cardano-wallet

[![Stars](https://img.shields.io/github/stars/cardano-foundation/cardano-wallet?style=flat-square&color=yellow)](https://github.com/cardano-foundation/cardano-wallet/stargazers) [![Forks](https://img.shields.io/github/forks/cardano-foundation/cardano-wallet?style=flat-square&color=blue)](https://github.com/cardano-foundation/cardano-wallet/network) [![Language](https://img.shields.io/badge/lang-Haskell-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-46%2F100-brightgreen?style=flat-square)](#)

> HTTP server & command-line for managing UTxOs and HD wallets in Cardano.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 819 |
| 🍴 **Forks** | 232 |
| 💻 **Language** | Haskell |
| 📈 **Score** | 46/100 |
| 🗓️ **Last push** | 2026-08-24 |
| 🔍 **Source** | github |

## 🏷️ Topics

_no topics_

## 🎯 Categories

Crypto

## 📝 Summary

### English

**Summary**  
cardano-foundation/cardano‑wallet is an open‑source Haskell implementation of a HTTP API and CLI for creating, managing, and querying HD wallets and UTxOs on the Cardano blockchain. It provides a ready‑to‑run server that can be used to prototype Web3 workflows, test DeFi integrations, or inspect on‑chain data without building a wallet from scratch.  

**Value**  
The project gives developers a concrete reference implementation of Cardano’s wallet layer, exposing low‑level UTxO operations and high‑level HD wallet functions through a clean REST interface. This makes it easy to experiment with transaction construction, address derivation, and balance monitoring, accelerating the development of wallet‑centric applications, blockchain explorers, or DeFi prototypes.  

**Practical adoption path**  
1. **Evaluate** – Clone the repo, run the provided Docker image or build from source, and point the server at a testnet node to verify basic wallet creation and UTxO queries.  
2. **Integrate** – Wrap the HTTP endpoints in your service layer (e.g., via OpenAPI client libraries) and replace the testnet node with your target mainnet node or a custom relay.  
3. **Validate** – Conduct a security review of the Haskell code and the underlying Cardano libraries, and perform end‑to‑end tests for the specific wallet features you need (e.g., multi‑asset handling, transaction signing).  

**Production readiness**  
The wallet scores a moderate 55/100. Its strong community signals—819 ★, 232 forks, recent updates (June 2026)—show active maintenance, but the integration documentation is sparse, and the API surface may require custom glue code. It is well‑suited for prototypes, internal tooling, or as a reference implementation, but moving to production demands:  

* a thorough dependency audit (ensure compatible Cardano node versions),  
* performance testing under expected load,  
* security hardening (e.g., key storage, rate limiting), and  
* possibly extending the API to cover missing workflow steps.  

With those checks in place, the wallet can serve as a reliable backbone for production‑grade Cardano applications.

### Русский

**cardano-foundation/cardano-wallet** — это HTTP‑сервер и CLI‑утилита на Haskell для управления UTxO‑и HD‑кошельками Cardano, позволяющая быстро прототипировать и отлаживать Web3‑процессы, проверять интеграцию с блокчейном и экспериментировать с функциями DeFi. Проект уже имеет 819 звёзд, активные форки и регулярные обновления (последний — 2026‑06‑26), что делает его пригодным для внутренних прототипов и небольших сервисов, однако из‑за скудной документации по интеграции требуется ручная проверка и настройка перед использованием в продакшене. В целом готовность к production — средняя: подходит для быстрых экспериментов, но требует дополнительного аудита зависимостей и стабильности перед масштабным запуском.

### 中文

**项目简介（2‑3 句）**  
`cardano-foundation/cardano-wallet` 是一个基于 Haskell 实现的 HTTP 服务和 CLI 工具，用于管理 Cardano 的 UTxO 与分层确定性（HD）钱包。它提供完整的 REST API，方便开发者在本地或测试网快速创建、查询、发送交易以及检查钱包状态。

**价值**  
- **快速原型**：开放实现细节，让团队能够在几行代码内搭建 Web3 工作流、模拟 DeFi 场景或验证链上集成。  
- **可视化调试**：通过 HTTP 接口和命令行，轻松检查 UTxO 分布、余额变化和交易构造过程，帮助定位链上问题。  
- **社区与生态**：拥有 800+ 星、200+ Fork，得到 Cardano 基金会官方维护，社区贡献活跃，文档和示例较为完善。

**典型接入方式**  
1. **本地或容器化部署**：直接运行 `cardano-wallet serve`（或使用官方 Docker 镜像），连接到本地区块节点或公共测试网。  
2. **API 调用**：在后端服务或前端应用中通过 HTTP/JSON 与钱包交互（如创建钱包、查询余额、构造并提交交易）。  
3. **CLI 集成**：在 CI/CD 脚本或运维工具中使用 `cardano-wallet` 命令行，实现自动化钱包管理或批量交易。  
4. **SDK 包装**：可自行封装成 Go、Python、JavaScript 等语言的轻量 SDK，内部调用其 REST 接口。

**生产可用性**  
- **成熟度**：中等（Medium）。项目活跃，近期仍在更新，代码质量和社区支持都不错，但元数据中缺少明确的生产级集成指南。  
- **使用建议**：适合作为内部原型、测试网实验或对链上行为进行深度审计的工具；在正式生产环境部署前，需要进行依赖审计、容错与监控方案的额外实现（如健康检查、日志聚合、备份恢复）。  
- **风险点**：集成路径不够透明，需自行评估钱包节点的运维成本、与 Cardano 节点的同步延迟以及安全加固（密钥管理、访问控制）。在确认满足安全与可靠性要求后方可投入业务关键流程。

## 🧭 Practical evaluation

**Value:** cardano-foundation/cardano-wallet helps prototype or inspect blockchain workflows with open implementation details.

**Best use cases**

- build Web3 workflows
- inspect blockchain integrations
- prototype wallet or DeFi features

**Integration notes:** Needs manual inspection before adoption because integration signals are sparse in the discovered metadata.

**Production readiness:** Medium: useful for prototypes or internal workflows, with dependency and maintenance checks before production.

**Quality signals**

- 819 GitHub stars
- 232 forks
- updated 2026-06-26
- primary language: Haskell

**Risks:** Integration path is not obvious from metadata; validate setup cost before committing.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 59/100 |
| stars | 62/100 |
| topics | 0/100 |
| outlook | 48/100 |
| quality | 53/100 |
| recency | 40/100 |
| adoption | 61/100 |
| production | 50/100 |
| usefulness | 42/100 |
| integration | 30/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 100/100 |

---

<sub>🔭 Discovered 2026-06-26 · [View on GitHub](https://github.com/cardano-foundation/cardano-wallet) · [← Back to Crypto](./README.md)</sub>
