# sendaifun/solana-agent-kit

[![Stars](https://img.shields.io/github/stars/sendaifun/solana-agent-kit?style=flat-square&color=yellow)](https://github.com/sendaifun/solana-agent-kit/stargazers) [![Forks](https://img.shields.io/github/forks/sendaifun/solana-agent-kit?style=flat-square&color=blue)](https://github.com/sendaifun/solana-agent-kit/network) [![Language](https://img.shields.io/badge/lang-TypeScript-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-56%2F100-brightgreen?style=flat-square)](#)

> connect any ai agents to solana protocols

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 1.7k |
| 🍴 **Forks** | 862 |
| 💻 **Language** | TypeScript |
| 📈 **Score** | 56/100 |
| 🗓️ **Last push** | 2026-08-24 |
| 🔍 **Source** | github |

## 🏷️ Topics

`ai` `langchain` `langchain-js` `solana` `solana-langchain` `web3js`

## 🎯 Categories

Orchestration · Crypto · AI/ML

## 📝 Summary

### English

**Brief Summary**  
`sendaifun/solana-agent-kit` is an open‑source TypeScript library that lets AI agents interact directly with Solana protocols, making it easy to prototype, test, and inspect Web3 workflows such as wallet actions, DeFi operations, or custom on‑chain logic. With 1.6 k ★ and active maintenance, it provides a concrete, well‑documented bridge between generative AI and the Solana ecosystem.  

**Value**  
The kit abstracts Solana RPC calls, transaction building, and signing into reusable components that AI agents can invoke, turning high‑level natural‑language instructions into real blockchain actions. This accelerates development cycles for teams building AI‑driven Web3 products, reduces the need for hand‑crafted integration code, and offers full visibility into the underlying protocol interactions for audit and debugging.  

**Practical Adoption Path**  
1. **Read the README & run the example** – clone the repo, install dependencies, and execute the provided demo to confirm the environment.  
2. **Proof‑of‑concept (PoC)** – create a minimal agent that performs a single Solana task (e.g., query a token balance or submit a simple transfer) using the kit’s helper functions.  
3. **Iterate & extend** – add more protocol modules (Serum, Raydium, etc.) and integrate the agent with your existing AI stack (LLM prompt templates, LangChain, etc.).  
4. **Security review & testnet deployment** – run the PoC on Solana devnet/testnet, add unit/integration tests, and perform a security audit of any custom signing logic.  

**Production Readiness**  
The project scores high on production readiness: recent commits (as of 2026‑05‑14), strong community signals (1,679 stars, 862 forks), and a clear TypeScript codebase make it suitable for a serious pilot. While the license and security posture still need a final check, the active maintainer community and growing adoption indicate the kit is robust enough to move beyond experimentation into production‑grade Web3 services.

### Русский

**sendaifun/solana-agent-kit** — это открытая TypeScript‑библиотека, позволяющая быстро подключать любые AI‑агенты к протоколам Solana для построения и отладки Web3‑рабочих процессов (например, прототипирование кошельков, DeFi‑операций, мониторинг интеграций). Проект уже имеет активную поддержку (1679 ⭐, 862 форка, последние коммиты — 2026‑05‑14) и демонстрирует высокий уровень готовности к продакшн‑использованию, поэтому рекомендуется начать с небольшого proof‑of‑concept, проверив README и базовые примеры. При дальнейшем внедрении следует уточнить лицензионные и безопасностные детали, но в целом kit готов к серьёзным пилотным проектам.

### 中文

**项目简介（2‑3 句）**  
`sendaifun/solana-agent-kit` 是一个开源工具箱，帮助开发者把任意 AI Agent 与 Solana 上的协议（钱包、DeFi、NFT 等）快速对接，实现区块链工作流的原型化和可视化检查。  

**价值主张**  
- **快速原型**：提供统一的 TypeScript SDK，开发者只需几行代码即可在 Solana 上调用智能合约或查询链上状态，极大缩短 AI‑Web3 场景的验证周期。  
- **透明实现**：所有调用细节、交易构造和签名流程均开源，可直接审计或定制，适合安全敏感的企业内部项目。  
- **生态兼容**：内置对常见 Solana 协议（Serum、Raydium、Metaplex 等）的适配层，支持将 AI 生成的决策直接转化为链上交易或查询。  

**典型接入方式**  
1. **阅读 README 与示例**：项目提供完整的入门指南和多个示例（如 `agent‑to‑wallet.ts`、`agent‑to‑defi.ts`）。  
2. **创建最小化 PoC**：在本地或测试网（devnet）新建一个 Node 项目，`npm i @sendaifun/solana-agent-kit`，按照示例代码实例化 `SolanaAgent`，配置 RPC、钱包私钥等必要参数。  
3. **集成 AI Agent**：将已有的 LLM/Agent 框架（如 LangChain、OpenAI Function Calling）包装成调用 `solanaAgent.execute(action, params)` 的函数，即可让 AI 直接发起链上操作或读取链上数据。  
4. **迭代与部署**：在 PoC 验证后，可将代码迁移到生产环境的 RPC（如 QuickNode、Alchemy）并使用硬件安全模块（HSM）或多签钱包提升安全性。  

**生产可用性**  
- **活跃度**：最近一次提交在 2026‑05‑14，星标 1679、Fork 862，社区活跃，Issue 响应及时。  
- **技术成熟度**：基于 TypeScript，兼容主流前端/后端框架，已实现对多个主流 Solana 协议的适配，具备可直接用于生产的 API。  
- **风险点**：仍需自行审查许可证（MIT/Apache 等）以及依赖的安全审计报告；建议在正式上线前进行代码审计并使用多签或硬件签名来降低密钥泄露风险。  

综上，`sendaifun/solana-agent-kit` 已具备较高的生产就绪度，适合作为 AI‑Web3 项目的底层连接层，从小规模 PoC 起步后即可平滑扩展到正式业务。

## 🧭 Practical evaluation

**Value:** sendaifun/solana-agent-kit helps prototype or inspect blockchain workflows with open implementation details.

**Best use cases**

- build Web3 workflows
- inspect blockchain integrations
- prototype wallet or DeFi features

**Integration notes:** Looks feasible to evaluate, but integration should start with a small proof of concept and README check.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 1679 GitHub stars
- 862 forks
- updated 2026-05-14
- primary language: TypeScript
- 6 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 73/100 |
| stars | 69/100 |
| topics | 75/100 |
| outlook | 54/100 |
| quality | 63/100 |
| recency | 20/100 |
| adoption | 70/100 |
| production | 51/100 |
| usefulness | 58/100 |
| integration | 46/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 300/100 |

---

<sub>🔭 Discovered 2026-05-14 · [View on GitHub](https://github.com/sendaifun/solana-agent-kit) · [← Back to Orchestration](./README.md)</sub>
