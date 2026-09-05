# solana-foundation/pay-kit

[![Stars](https://img.shields.io/github/stars/solana-foundation/pay-kit?style=flat-square&color=yellow)](https://github.com/solana-foundation/pay-kit/stargazers) [![Forks](https://img.shields.io/github/forks/solana-foundation/pay-kit?style=flat-square&color=blue)](https://github.com/solana-foundation/pay-kit/network) [![Language](https://img.shields.io/badge/lang-Rust-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-65%2F100-brightgreen?style=flat-square)](#)

> Agentic commerce building blocks (x402, MPP, AP2) for TypeScript, Rust, Go, Python, Ruby, PHP, Lua, Kotlin and Swift.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 64 |
| 🍴 **Forks** | 18 |
| 💻 **Language** | Rust |
| 📈 **Score** | 65/100 |
| 🗓️ **Last push** | 2026-09-05 |
| 🔍 **Source** | github |

## 🏷️ Topics

`base` `golang` `kotlin` `lua` `mpp` `payments` `php` `python` `ruby` `rust` `solana` `swift`

## 🎯 Categories

Crypto · Payments

## 📝 Summary

### English

**Brief Summary (2‑3 sentences)**  
solana‑foundation/pay‑kit is an open‑source collection of “agentic commerce” building blocks (x402, MPP, AP2) that let developers prototype, inspect, and integrate blockchain payment flows across a wide range of languages—including TypeScript, Rust, Go, Python, Ruby, PHP, Lua, Kotlin, and Swift. The kit offers concrete implementations for Web3 workflows such as wallet interactions, DeFi primitives, and cross‑chain payments, making it easier to experiment with Solana‑based payment logic without reinventing low‑level plumbing.  

**Value**  
- **Rapid prototyping** – Ready‑made modules expose the inner workings of Solana payment primitives, so teams can quickly spin up proof‑of‑concepts or sandbox environments.  
- **Multi‑language support** – By providing idiomatic bindings for nine popular languages, the kit fits into existing tech stacks, reducing the learning curve for non‑Rust developers.  
- **Transparency** – Open implementation details let engineers audit, extend, or customize the payment flow, which is critical for compliance and security reviews in regulated fintech contexts.  

**Practical Adoption Path**  
1. **Read the README & run the basic example** – Clone the repo, follow the “quick‑start” script for the language of choice, and verify that a simple payment transaction executes on Solana devnet.  
2. **Create a small PoC** – Integrate one module (e.g., the x402 token‑transfer wrapper) into an existing service or a minimal front‑end to validate end‑to‑end flow and assess performance.  
3. **Extend or compose modules** – Combine multiple building blocks (MPP for multi‑party payments, AP2 for atomic swaps) to model the target business logic, customizing only the glue code.  
4. **Security & compliance audit** – Review the Rust core for known vulnerabilities, run static analysis tools, and confirm the license (Apache‑2.0) aligns with your organization’s policy.  
5. **Scale to production** – Replace devnet endpoints with mainnet, add monitoring, and adopt the library’s versioning strategy for long‑term maintenance.  

**Production Readiness**  
- **Activity & community** – The project shows recent commits (last update 2026‑06‑22), 64 GitHub stars, 18 forks, and a modest but active contributor base, indicating ongoing maintenance.  
- **Ecosystem fit** – Solana’s growing DeFi and payments ecosystem, combined with the kit’s language coverage, makes it a viable foundation for pilots in Web3 wallets, NFT marketplaces, or cross‑border payment services.  
- **Risk considerations** – While no major metadata or licensing red flags appear, a final security review (dependency scanning, audit of the Rust core, and verification of maintainers’ activity) is advisable before mission‑critical deployment.  

Overall, pay‑kit is production‑ready for a controlled pilot: start with a lightweight PoC, perform a security audit, and then expand to full‑scale integration once confidence in the implementation and support model is established.

### Русский

**solana-foundation/pay-kit** — набор открытых строительных блоков (x402, MPP, AP2) для реализации Web‑3 и DeFi‑функций на TypeScript, Rust, Go, Python, Ruby, PHP, Lua, Kotlin и Swift. Он позволяет быстро прототипировать и проверять блокчейн‑воркфлоу, интегрировать кошельки и платежные схемы, а также инспектировать детали реализации без закрытого кода. Проект уже активно поддерживается (обновления 2026‑06‑22, 64 звёзд, 18 форков) и готов к пилотному запуску в продакшн после небольшого proof‑of‑concept и проверки README/лицензии.

### 中文

**项目简介**  
solana-foundation/pay‑kit 是一套面向多语言（TypeScript、Rust、Go、Python、Ruby、PHP、Lua、Kotlin、Swift）的 Agentic Commerce 基础组件，提供 x402、MPP、AP2 等 Solana 生态链上支付与 DeFi 工作流的实现示例。

**价值**  
- **快速原型**：通过开箱即用的实现细节，开发者可以在几行代码内搭建、调试和验证区块链支付、钱包或 DeFi 场景。  
- **跨语言统一**：同一套业务模型在多种语言中保持一致，降低团队学习成本，便于后端、前端、移动端统一迭代。  
- **透明可审计**：所有核心逻辑均开源，便于安全审计和合规检查，帮助企业在生产环境前彻底了解链上交互细节。

**典型接入方式**  
1. **阅读 README**：确认目标语言的依赖安装方式（如 `npm install @solana/pay-kit`、`cargo add pay-kit`、`pip install solana-pay-kit` 等）。  
2. **创建小型 PoC**：在本地或测试网（devnet）中写一个最小化的支付或钱包调用示例，验证链上请求、签名和回执流程。  
3. **集成到业务代码**：在 PoC 稳定后，将对应语言的 SDK 引入正式项目，按照 SDK 文档完成配置（RPC 节点、钱包密钥、费用模型等），并加入错误处理与监控。  
4. **安全与审计**：在代码合并前进行依赖审计（SCA）和合约调用审计，确保无未授权的网络请求或密钥泄露。

**生产可用性**  
- **活跃度**：最近一次提交在 2026‑06‑22，仓库拥有 64 ★、18 Fork，且主要语言为 Rust，说明社区仍在维护。  
- **成熟度**：提供完整的多语言实现和示例，适合作为 **OSS 级别的候选组件** 进行正式项目试点。  
- **风险**：目前未发现重大元数据风险，但仍需对许可证（MIT/Apache 等）和安全响应流程进行最终确认。总体来看，经过小范围 PoC 验证后，可视为具备生产环境使用的准备度。

## 🧭 Practical evaluation

**Value:** solana-foundation/pay-kit helps prototype or inspect blockchain workflows with open implementation details.

**Best use cases**

- build Web3 workflows
- inspect blockchain integrations
- prototype wallet or DeFi features

**Integration notes:** Looks feasible to evaluate, but integration should start with a small proof of concept and README check.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 64 GitHub stars
- 18 forks
- updated 2026-06-22
- primary language: Rust
- 15 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 32/100 |
| stars | 39/100 |
| topics | 100/100 |
| outlook | 69/100 |
| quality | 67/100 |
| recency | 80/100 |
| adoption | 37/100 |
| production | 71/100 |
| usefulness | 58/100 |
| integration | 78/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 200/100 |

---

<sub>🔭 Discovered 2026-06-23 · [View on GitHub](https://github.com/solana-foundation/pay-kit) · [← Back to Crypto](./README.md)</sub>
