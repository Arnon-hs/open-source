# metaplex-foundation/mpl-bubblegum

[![Stars](https://img.shields.io/github/stars/metaplex-foundation/mpl-bubblegum?style=flat-square&color=yellow)](https://github.com/metaplex-foundation/mpl-bubblegum/stargazers) [![Forks](https://img.shields.io/github/forks/metaplex-foundation/mpl-bubblegum?style=flat-square&color=blue)](https://github.com/metaplex-foundation/mpl-bubblegum/network) [![Language](https://img.shields.io/badge/lang-Rust-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-42%2F100-brightgreen?style=flat-square)](#)

> Create and manage Metaplex compressed NFTs

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 126 |
| 🍴 **Forks** | 72 |
| 💻 **Language** | Rust |
| 📈 **Score** | 42/100 |
| 🗓️ **Last push** | 2026-08-24 |
| 🔍 **Source** | github |

## 🏷️ Topics

_no topics_

## 🎯 Categories

Misc

## 📝 Summary

### English

**Summary**  
`mpl‑bubblegum` is a Rust library from the Metaplex foundation that implements the on‑chain “bubblegum” protocol for creating, updating and managing compressed NFTs on Solana. It offers low‑cost, high‑throughput NFT minting that stores most data off‑chain while retaining on‑chain proof of ownership, making it useful for prototyping Web3 workflows, wallet integrations, or DeFi use‑cases that need large‑scale NFT handling.

**Value**  
The project gives developers a ready‑made, open‑source implementation of the compressed‑NFT standard, eliminating the need to write low‑level Solana programs from scratch and allowing rapid experimentation with batch minting, lazy minting, and Merkle‑tree proof verification. Because the code is public, teams can inspect the exact on‑chain logic, audit security properties, and extend the protocol to fit custom business rules.

**Practical adoption path**  
1. **Prototype** – Clone the repo, run the provided Cargo examples, and use the Rust SDK to mint a few test compressed NFTs on Solana devnet.  
2. **Integration** – Review the on‑chain instruction definitions and the client‑side helper functions; adapt the SDK calls to your wallet or backend service, adding any required custom metadata.  
3. **Validation** – Deploy the program to a testnet, run integration tests, and verify Merkle‑tree proofs and cost estimates against your expected transaction volume.  
4. **Production rollout** – Once the testnet passes, publish the program to mainnet‑beta, configure your monitoring and key‑management pipelines, and integrate the SDK into your production stack.

**Production readiness**  
The library is moderately mature (126 ★, 72 forks, recent updates) and suitable for internal prototypes or limited‑scale production after a thorough dependency audit and performance testing. However, the integration documentation is sparse, so teams should allocate time to understand the program’s deployment steps, required Solana accounts, and fee structure before committing to a full‑scale launch. With those checks in place, `mpl‑bubblegum` can be a reliable core component for compressed‑NFT workflows in production environments.

### Русский

**metaplex-foundation/mpl-bubblegum** – библиотека на Rust для создания и управления сжатым (compressed) NFT‑контентом Metaplex, позволяющая быстро прототипировать и отлаживать Web3‑процессы, такие как выпуск токенов, интеграцию с кошельками или DeFi‑модулями. Типичный сценарий — разработчик подключает библиотеку к своему Solana‑проекту, генерирует сжатые NFT и проверяет цепочку транзакций, получая полные открытые реализации блокчейн‑логики. Готовность к production — средняя: проект достаточно стабилен (126 звёзд, 72 форка, активные обновления), но интеграционный путь неочевиден, поэтому перед выпуском в продакшн требуется тщательная проверка зависимостей и настройка среды.

### 中文

**项目简介**  
`metaplex-foundation/mpl-bubblegum` 是 Metaplex 官方提供的 Rust 库，用于在 Solana 上创建、管理和查询 **Compressed NFT（压缩 NFT）**。它实现了 Bubblegum 协议的完整接口，帮助开发者在链上高效地铸造、转移和验证大批量 NFT。

**价值**  
- **快速原型**：提供开箱即用的 API，开发者可以在几行代码内完成压缩 NFT 的全链路操作，适合 Web3 工作流、钱包或 DeFi 功能的概念验证。  
- **透明实现**：所有协议细节均在源码中公开，便于审计、学习和二次开发。  
- **成本优势**：压缩 NFT 大幅降低存储和交易费用，适合需要大规模发行的项目（游戏道具、社交徽章等）。

**典型接入方式**  
1. **依赖引入**：在 Cargo.toml 中添加 `mpl-bubblegum = "x.y.z"`（对应的版本号）。  
2. **初始化客户端**：使用 `solana-client` 或 `anchor-client` 创建 `RpcClient`，并加载钱包密钥对。  
3. **调用 SDK**：  
   - `create_tree` → 创建 Merkle 树（压缩 NFT 的根）  
   - `mint_to_collection` → 在指定树中铸造压缩 NFT  
   - `transfer` / `burn` → 转移或销毁 NFT  
   - `verify_proof` → 验证 Merkle 证明，确保链上状态一致  
4. **链上交互**：通过 `solana_program::instruction::Instruction` 将生成的指令发送至 Solana RPC，监控交易回执即可完成操作。  

**生产可用性**  
- **成熟度**：项目已有 126 ★、72 fork，活跃维护至 2026‑06‑26，代码基于稳定的 Rust 生态。  
- **适用场景**：适合内部原型、测试网或中小规模生产环境。  
- **风险与准备**：元数据中未提供完整的集成示例，实际接入前需自行阅读协议文档并进行端到端测试；同时关注依赖的 Solana 版本和 Bubblegum 协议升级。  
- **总体评估**：**中等**（Medium）——在完成必要的依赖审查、性能基准和安全审计后，可在生产环境中使用，尤其是对压缩 NFT 有明确需求的项目。

## 🧭 Practical evaluation

**Value:** metaplex-foundation/mpl-bubblegum helps prototype or inspect blockchain workflows with open implementation details.

**Best use cases**

- build Web3 workflows
- inspect blockchain integrations
- prototype wallet or DeFi features

**Integration notes:** Needs manual inspection before adoption because integration signals are sparse in the discovered metadata.

**Production readiness:** Medium: useful for prototypes or internal workflows, with dependency and maintenance checks before production.

**Quality signals**

- 126 GitHub stars
- 72 forks
- updated 2026-06-26
- primary language: Rust

**Risks:** Integration path is not obvious from metadata; validate setup cost before committing.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 47/100 |
| stars | 45/100 |
| topics | 0/100 |
| outlook | 44/100 |
| quality | 45/100 |
| recency | 40/100 |
| adoption | 45/100 |
| production | 47/100 |
| usefulness | 42/100 |
| integration | 30/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 0/100 |

---

<sub>🔭 Discovered 2026-06-26 · [View on GitHub](https://github.com/metaplex-foundation/mpl-bubblegum) · [← Back to Misc](./README.md)</sub>
