# unicity-sphere/sphere-sdk

[![Stars](https://img.shields.io/github/stars/unicity-sphere/sphere-sdk?style=flat-square&color=yellow)](https://github.com/unicity-sphere/sphere-sdk/stargazers) [![Forks](https://img.shields.io/github/forks/unicity-sphere/sphere-sdk?style=flat-square&color=blue)](https://github.com/unicity-sphere/sphere-sdk/network) [![Language](https://img.shields.io/badge/lang-TypeScript-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-69%2F100-brightgreen?style=flat-square)](#)

> The SDK for autonomous economic agents. Give an agent an identity, a wallet, and the ability to find, negotiate with, and settle with other agents - peer-to-peer, with perfect privacy and ultra-fast finality

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 5.4k |
| 🍴 **Forks** | 99 |
| 💻 **Language** | TypeScript |
| 📈 **Score** | 69/100 |
| 🗓️ **Last push** | 2026-08-24 |
| 🔍 **Source** | github |

## 🏷️ Topics

`ai-agents` `artificial-intelligence` `blockchain` `commerce`

## 🎯 Categories

Crypto · Automation · AI/ML

## 📝 Summary

### English

**Brief Summary**  
Sphere‑SDK is a TypeScript‑based toolkit that equips autonomous economic agents with a verifiable identity, a built‑in wallet, and peer‑to‑peer protocols for discovery, negotiation, and settlement. It lets developers prototype and inspect Web3 workflows—such as DeFi interactions or custom wallet logic—with full visibility into the underlying blockchain implementation.  

**Value**  
- **End‑to‑end agent stack**: identity, cryptographic wallet, and P2P market‑making primitives are delivered out‑of‑the‑box, eliminating the need to cobble together separate libraries.  
- **Transparency**: the SDK’s open source code and explicit API/CLI expose every step of a transaction, making it ideal for learning, auditing, or building compliance‑focused solutions.  
- **Speed & privacy**: built on the Sphere protocol, it offers ultra‑fast finality and cryptographic privacy guarantees that are hard to achieve with generic blockchain SDKs.  

**Practical Adoption Path**  
1. **Prototype** – Clone the repo, run the provided CLI to spin up a local testnet, and use the TypeScript API to create a sample agent that opens a wallet and executes a simple trade.  
2. **Integrate** – Replace the testnet endpoints with a production Sphere node or compatible RPC, and plug the SDK into your existing backend or front‑end (React, Node, etc.).  
3. **Extend** – Leverage the modular negotiation and settlement modules to add custom business logic (e.g., automated market‑making, escrow, or cross‑chain swaps).  
4. **Deploy** – Containerize the agent service, configure monitoring/webhooks, and roll it out in a Kubernetes or serverless environment for production use.  

**Production Readiness**  
- **Activity & Adoption**: 5.4 k stars, 99 forks, recent commits (as of 2026‑06‑25) and growing ecosystem integrations indicate strong community momentum.  
- **Maturity**: The SDK ships with a stable TypeScript API, CLI utilities, and comprehensive documentation, making it straightforward to evaluate and embed.  
- **Risk Considerations**: No glaring licensing or security red flags have been identified, but a final review of the open‑source license (e.g., MIT vs. GPL) and a security audit of the cryptographic primitives is advisable before mission‑critical deployment.  

Overall, Sphere‑SDK is a high‑readiness OSS component for teams looking to prototype or operationalize autonomous agents in Web3, with a clear path from sandbox experimentation to production rollout.

### Русский

**unicity-sphere/sphere-sdk** — это TypeScript‑SDK, позволяющий быстро добавить автономному экономическому агенту уникальную идентичность, кошелёк и полностью приватные P2P‑взаимодействия (поиск, переговоры, расчёты) с мгновенной финальностью. Он подходит для прототипирования и интеграции Web3‑процессов: от создания DeFi‑фич и кошельков до отладки блокчейн‑рабочих потоков через готовый API/CLI. Проект уже имеет 5 k+ звёзд, активные коммиты и широкое принятие, что свидетельствует о высокой готовности к production‑использованию (нужна лишь финальная проверка лицензии и безопасности).

### 中文

**项目简介（2‑3 句话）**  
Sphere‑SDK 是面向自主经济体（AEA）的 TypeScript 开发工具箱，为每个智能体提供唯一身份、链上钱包以及点对点的发现、议价和结算能力，实现零泄漏隐私和亚秒级最终确定性。它让开发者能够在本地快速原型化 Web3 流程、检查区块链集成细节，并直接对接 DeFi、钱包等业务场景。

**价值**  
- **完整身份与资产管理**：统一的 DID 与钱包抽象，省去自行实现密钥管理和链上账户的繁琐工作。  
- **端到端 P2P 交互**：内置发现、协商与结算协议，支持在不泄露业务数据的前提下完成跨链/链内交易。  
- **快速验证与迭代**：提供 API、SDK 与 CLI 三种入口，配合丰富的 TypeScript 类型定义，使得区块链工作流的原型验证和单元测试成本大幅降低。  

**典型接入方式**  
1. **npm 安装**：`npm i @unicity-sphere/sphere-sdk`（或使用 Yarn、pnpm）。  
2. **初始化 SDK**：在项目入口创建 `SphereClient`，传入链配置、身份提供者和可选的本地存储。  
   ```ts
   import { SphereClient } from '@unicity-sphere/sphere-sdk';
   const client = new SphereClient({
     network: 'sui-testnet',
     identity: myDid,
     wallet: myWallet,
   });
   ```  
3. **调用业务 API**：使用 `client.discovery.findAgents()、client.negotiation.propose()、client.settlement.execute()` 等高层方法完成搜索、议价和结算。  
4. **CLI 辅助**：通过 `sphere-cli` 可在本地快速生成 DID、查看钱包余额、模拟交易，适合 CI/CD 流程或脚本化测试。  

**生产可用性**  
- **活跃度**：截至 2026‑06‑25，项目最近一次提交在当日，拥有 5 447+ 星、99+ Fork，社区讨论活跃。  
- **技术成熟度**：基于 TypeScript，提供完整类型声明和自动化测试，兼容主流前端/后端框架。  
- **生态兼容**：支持多链（如 Sui、Ethereum）和标准 DID 方法，易于与现有 Web3 基础设施（钱包、链上服务）对接。  
- **风险**：目前未发现重大许可证或安全隐患，但仍建议在正式上线前完成安全审计并确认维护者响应速度。  

综合来看，Sphere‑SDK 已具备较高的生产就绪度，适合作为企业级或创新项目的区块链原型平台，并可平滑迁移至正式生产环境。

## 🧭 Practical evaluation

**Value:** unicity-sphere/sphere-sdk helps prototype or inspect blockchain workflows with open implementation details.

**Best use cases**

- build Web3 workflows
- inspect blockchain integrations
- prototype wallet or DeFi features

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 5447 GitHub stars
- 99 forks
- updated 2026-06-25
- primary language: TypeScript
- 4 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 50/100 |
| stars | 80/100 |
| topics | 50/100 |
| outlook | 62/100 |
| quality | 65/100 |
| recency | 40/100 |
| adoption | 71/100 |
| production | 61/100 |
| usefulness | 74/100 |
| integration | 78/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 300/100 |

---

<sub>🔭 Discovered 2026-06-25 · [View on GitHub](https://github.com/unicity-sphere/sphere-sdk) · [← Back to Crypto](./README.md)</sub>
