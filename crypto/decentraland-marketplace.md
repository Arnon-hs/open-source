# decentraland/marketplace

[![Stars](https://img.shields.io/github/stars/decentraland/marketplace?style=flat-square&color=yellow)](https://github.com/decentraland/marketplace/stargazers) [![Forks](https://img.shields.io/github/forks/decentraland/marketplace?style=flat-square&color=blue)](https://github.com/decentraland/marketplace/network) [![Language](https://img.shields.io/badge/lang-TypeScript-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-51%2F100-brightgreen?style=flat-square)](#)

> 🏛️ Decentraland's NFT Marketplace

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 1.2k |
| 🍴 **Forks** | 691 |
| 💻 **Language** | TypeScript |
| 📈 **Score** | 51/100 |
| 🗓️ **Last push** | 2026-08-24 |
| 🔍 **Source** | github |

## 🏷️ Topics

`dapp`

## 🎯 Categories

Crypto

## 📝 Summary

### English

**Brief Summary**  
Decentraland’s open‑source NFT Marketplace (decentraland/marketplace) is a TypeScript‑based web app that lets users browse, buy, sell, and auction Decentraland parcels, wearables and other NFTs. With 1 195 stars and 691 forks, it provides a concrete reference implementation of Web3 wallet integration, marketplace UI flows, and on‑chain transaction handling, making it a useful starting point for anyone building or prototyping blockchain‑driven e‑commerce or DeFi features.

**Value**  
- **Concrete reference implementation** – The codebase shows end‑to‑end handling of wallet connections, signature requests, ERC‑721/1155 interactions, and marketplace‑specific smart‑contract calls, saving developers time reverse‑engineering these patterns.  
- **Rapid prototyping** – Because the UI and blockchain logic are already wired together, teams can spin up a functional demo of a NFT marketplace or any Web3 checkout flow in days rather than weeks.  
- **Learning resource** – The project’s structure, TypeScript typings, and clear separation of concerns serve as a teaching aid for developers new to decentralized applications.

**Practical Adoption Path**  
1. **Explore & Fork** – Clone the repo and run the development server to understand the existing flow (wallet connect, listing creation, purchase, auction).  
2. **Replace Decentraland contracts** – Swap out the Decentraland‑specific contract addresses and ABIs with those of your own ERC‑721/1155 contracts (or a custom marketplace contract).  
3. **Integrate your wallet/provider** – If you use a different wallet solution (e.g., WalletConnect, Coinbase Wallet), adjust the `src/lib/wallet` module accordingly.  
4. **Customize UI/UX** – Re‑theme the React components, add branding, and modify business rules (fees, royalties, listing limits).  
5. **Test & Audit** – Run unit/integration tests, perform a security audit of any new contract interactions, and verify that the app works on your target networks (mainnet, testnet, or a private chain).  
6. **Deploy** – Deploy the front‑end to a static hosting service (Vercel, Netlify, IPFS) and point it at your production contracts.

**Production Readiness**  
- **Maturity**: Medium. The codebase is actively maintained (last update 2026‑06‑30) and widely used within the Decentraland ecosystem, but it was built primarily as a product rather than a generic library.  
- **Dependencies**: The project relies on several third‑party packages (ethers.js, React, Web3Modal). A review of version compatibility and vulnerability reports is required before production use.  
- **Maintenance**: While the repo has a healthy star/fork count, the core maintainers are focused on Decentraland; you may need to fork and maintain your own version for long‑term stability.  
- **Security & Licensing**: No major metadata risks are flagged, but a formal license verification and security audit of any custom contract integrations are still needed.  

In short, decentraland/marketplace is a solid, production‑grade reference for building NFT marketplaces and other Web3 workflows, best suited for prototyping or internal tools, with a clear upgrade path to a production‑ready solution after thorough dependency, security, and maintenance vetting.

### Русский

Резюме проекта decentraland/marketplace:

Decentraland's NFT Marketplace - это открытый проект, который позволяет прототипировать и отладить блокчейн-работы с прозрачными реализационными деталями. Этот проект особенно полезен для построения Web3-работflows, инспектирования блокчейн-интеграций и прототипирования функций кошелька или DeFi. Проект имеет средний уровень готовности к production, что означает его полезность для прототипирования или внутренних рабочих процессов с необходимостью тщательного проверки зависимостей и сопровождения перед выпуском в production.

### 中文

**项目简介**  
decentraland/marketplace 是 Decentraland 官方的 NFT 交易平台实现，基于 TypeScript 开发，提供完整的智能合约交互、资产展示与交易流程代码，适合作为 Web3 项目原型或区块链工作流的参考实现。

**价值**  
- **快速原型**：开箱即用的 marketplace 代码让开发者能够在几分钟内搭建起 NFT 列表、购买、出价等核心功能，省去从零实现的时间成本。  
- **学习与审计**：所有区块链交互（如钱包连接、合约调用、事件监听）均公开，可直接阅读、调试，帮助团队深入理解 Decentraland 生态及通用的 Web3 工作流。  
- **可复用组件**：项目中封装的 UI 组件、状态管理和链上/链下数据同步逻辑，可直接迁移到其他 NFT、DeFi 或游戏项目中，加速功能迭代。

**典型接入方式**  
1. **代码审查**：克隆仓库后，先检查 `package.json`、`tsconfig.json` 与合约地址配置，确保符合目标链（以太坊/Polygon）和业务需求。  
2. **环境准备**：在本地或 CI 环境中安装依赖 (`npm i`)，并根据 README 配置 `.env`（钱包私钥、Infura/Alchemy RPC、Marketplace 合约地址等）。  
3. **集成到现有前端**：将 `src/components/Marketplace*`、`src/services/blockchain` 等模块按需引入，使用提供的 React Hook（如 `useMarketplace`, `useBuyAsset`）完成 UI 与链上交互。  
4. **测试与部署**：在测试网（Goerli/Polygon Mumbai）运行单元/集成测试，确认钱包签名、交易回执等关键路径后，再部署到主网或内部私链。

**生产可用性**  
- **成熟度**：项目已有 1,195 星、691 次 Fork，活跃度高，最近一次更新在 2026‑06‑30，代码质量和社区活跃度均处于中上水平。  
- **适用场景**：非常适合作为内部原型、演示或限定业务的内部平台；若直接面向公众使用，需要进行以下额外检查：  
  - **安全审计**：确认合约版本、依赖库的安全性，并对关键交易路径做渗透测试。  
  - **许可证合规**：检查项目 LICENSE 与业务兼容性（如 MIT、Apache 等）。  
  - **运维准备**：评估链上费用（gas）监控、故障恢复、日志收集等生产运维需求。  
- **综合评估**：在完成上述安全、合规与运维审查后，可视为 **Medium** 级别的生产可用方案，适合对可靠性要求不极端苛刻的业务；若对高可用、审计合规有更高要求，则建议在此基础上进行二次开发与强化。

## 🧭 Practical evaluation

**Value:** decentraland/marketplace helps prototype or inspect blockchain workflows with open implementation details.

**Best use cases**

- build Web3 workflows
- inspect blockchain integrations
- prototype wallet or DeFi features

**Integration notes:** Needs manual inspection before adoption because integration signals are sparse in the discovered metadata.

**Production readiness:** Medium: useful for prototypes or internal workflows, with dependency and maintenance checks before production.

**Quality signals**

- 1195 GitHub stars
- 691 forks
- updated 2026-06-30
- primary language: TypeScript
- 1 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 71/100 |
| stars | 65/100 |
| topics | 13/100 |
| outlook | 50/100 |
| quality | 57/100 |
| recency | 40/100 |
| adoption | 67/100 |
| production | 54/100 |
| usefulness | 42/100 |
| integration | 46/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 100/100 |

---

<sub>🔭 Discovered 2026-06-30 · [View on GitHub](https://github.com/decentraland/marketplace) · [← Back to Crypto](./README.md)</sub>
