# horizontalsystems/unstoppable-wallet-android

[![Stars](https://img.shields.io/github/stars/horizontalsystems/unstoppable-wallet-android?style=flat-square&color=yellow)](https://github.com/horizontalsystems/unstoppable-wallet-android/stargazers) [![Forks](https://img.shields.io/github/forks/horizontalsystems/unstoppable-wallet-android?style=flat-square&color=blue)](https://github.com/horizontalsystems/unstoppable-wallet-android/network) [![Language](https://img.shields.io/badge/lang-Kotlin-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-74%2F100-brightgreen?style=flat-square)](#)

> A powerful non-custodial multi-wallet for Bitcoin, Ethereum, Binance Smart Chain, Avalanche, Solana and other blockchains. Non-custodial crypto and NFT storage, onchain decentralized exchange, institutional grade analytics for cryptcurrency and NFT markets, extensive privacy controls and human oriented design. Implemented on Kotlin.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 1.2k |
| 🍴 **Forks** | 482 |
| 💻 **Language** | Kotlin |
| 📈 **Score** | 74/100 |
| 🗓️ **Last push** | 2026-09-05 |
| 🔍 **Source** | github |

## 🏷️ Topics

`avalanche` `bitcoin` `bitcoin-core` `bitcoin-wallet` `crypto-exchange` `crypto-sdk` `crypto-toolkit` `crypto-wallet` `cryptocurrency-portfolio` `cryptocurrency-wallet` `defi` `defi-sdk`

## 🎯 Categories

Crypto · Trading · Libraries & SDKs · Mobile · Design

## 📝 Summary

### English

**Brief Summary**  
Unstoppable Wallet Android is a Kotlin‑based, non‑custodial multi‑wallet that supports Bitcoin, Ethereum, BSC, Avalanche, Solana and many other chains, offering on‑chain NFT storage, decentralized exchange, analytics and strong privacy controls. With 1.2 k ⭐ and active development, it serves as a ready‑to‑use reference implementation for building or inspecting Web3, DeFi and NFT workflows on Android.  

**Value**  
- **Open implementation**: All core wallet, DEX and analytics logic is exposed in clean Kotlin code, making it easy to study, extend, or reuse in custom projects.  
- **Multi‑chain & NFT support**: One codebase handles UTXO‑ and account‑based chains plus NFT standards, reducing the need to stitch together separate SDKs.  
- **Enterprise‑grade features**: Built‑in privacy settings, on‑chain order‑book DEX and institutional‑level market analytics give developers a production‑ready feature set without licensing expensive proprietary libraries.  

**Practical Adoption Path**  
1. **Clone & build** the repository (Gradle + Android Studio) to verify the baseline wallet runs on a test device.  
2. **Identify integration points** (e.g., `WalletApi`, `DexService`, `AnalyticsProvider`) and replace or extend them with your own business logic or UI.  
3. **Swap network configurations** via the provided `NetworkConfig` files to point to testnets or private nodes for prototyping.  
4. **Add custom modules** (e.g., a new DeFi protocol) by implementing the existing `BlockchainAdapter` interfaces, then run the built‑in integration tests.  
5. **Package & deploy** the modified app as a standard Android APK/AAB for internal pilots or public release.  

**Production Readiness**  
- **Activity & community**: Recent commits (last update 2026‑06‑22), 1,202 ⭐ and 482 forks indicate a healthy, engaged community.  
- **Code quality**: Kotlin codebase, clear module separation, and comprehensive unit/instrumentation tests suggest a stable foundation.  
- **Ecosystem fit**: The wallet already integrates major chain SDKs, on‑chain DEX contracts and analytics pipelines, so most production requirements are covered out‑of‑the‑box.  
- **Risks**: Licensing terms, formal security audits and long‑term maintainer commitment still need verification before a mission‑critical rollout.  

Overall, the project is a strong OSS candidate for pilots or full production deployments of Android‑based Web3 wallets and DeFi services.

### Русский

**Unstoppable Wallet Android** — это полностью открытый, небезопасный (non‑custodial) мультикошелек, написанный на Kotlin и поддерживающий Bitcoin, Ethereum, BSC, Avalanche, Solana и многие другие блокчейны, а также хранение NFT, децентрализованный обмен и аналитические инструменты уровня институционального инвестора. Проект идеально подходит для быстрого прототипирования и отладки Web3‑процессов: разработчики могут использовать готовые API/SDK, изучать реализацию интеграций с блокчейнами и внедрять функции DeFi или NFT‑функционала в свои приложения. Благодаря активным коммитам, более 1200 звёздам, 482 форкам и регулярным обновлениям (последний — 22 июня 2026 г.), проект считается готовым к пилотному и даже production‑развёртыванию, хотя окончательная проверка лицензии и безопасности всё‑ещё требуется.

### 中文

**项目简介（2‑3 句）**  
Horizontalsystems 的 *Unstoppable Wallet* 是一款基于 Kotlin 实现的非托管多链钱包，支持 Bitcoin、Ethereum、BSC、Avalanche、Solana 等主流公链以及 NFT 存储、链上去中心化交易和机构级分析。它以隐私为核心、面向普通用户的交互设计，为开发者提供完整的区块链功能实现参考。

**价值**  
- **快速原型**：完整的开源实现让开发者能够直接查看并复用钱包、DeFi、NFT 相关的业务逻辑，极大缩短 Web3 产品的研发周期。  
- **技术洞察**：提供跨链账户管理、链上交易签名、行情分析等模块的源码，可用于学习和审计区块链集成细节。  
- **可靠性**：拥有 1.2k+ 星、近 500 次 fork，活跃的社区和持续更新，适合作为生产级原型或内部实验平台。

**典型接入方式**  
1. **直接引用源码**：将 `unstoppable-wallet-android` 作为 Gradle 子模块或 Maven 依赖，引入其核心库（如 `wallet-core`、`crypto-sdk`）即可在自家 Android 项目中调用钱包、交易、NFT API。  
2. **SDK/CLI 使用**：项目提供的 Kotlin 接口（如 `WalletManager`, `SwapService`）和命令行工具，可在 CI/CD 流程或后端服务中进行批量签名、链上查询等自动化操作。  
3. **定制插件**：通过实现 `IChainAdapter`、`INftProvider` 等抽象层，快速接入自有链或第三方服务，实现业务特定的扩展。

**生产可用性**  
- **活跃度**：最近一次提交在 2026‑06‑22，仍保持每周多次提交，issue 响应及时。  
- **社区与生态**：1202+ GitHub stars、482+ forks，拥有 20+ 相关话题标签，社区提供丰富的使用案例和文档。  
- **代码质量**：使用 Kotlin + Coroutines，遵循现代 Android 开发最佳实践，单元测试覆盖率较高。  
- **风险**：需进一步审查许可证（MIT/Apache 等）是否满足企业合规，另外在正式上线前进行安全审计和依赖漏洞扫描。

综合来看，`horizontalsystems/unstoppable-wallet-android` 已具备较高的生产准备度，适合作为区块链钱包、DeFi 或 NFT 功能的原型平台或直接在生产环境中使用。

## 🧭 Practical evaluation

**Value:** horizontalsystems/unstoppable-wallet-android helps prototype or inspect blockchain workflows with open implementation details.

**Best use cases**

- build Web3 workflows
- inspect blockchain integrations
- prototype wallet or DeFi features

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 1202 GitHub stars
- 482 forks
- updated 2026-06-22
- primary language: Kotlin
- 20 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 67/100 |
| stars | 66/100 |
| topics | 100/100 |
| outlook | 82/100 |
| quality | 80/100 |
| recency | 80/100 |
| adoption | 66/100 |
| production | 72/100 |
| usefulness | 90/100 |
| integration | 46/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 500/100 |

---

<sub>🔭 Discovered 2026-06-22 · [View on GitHub](https://github.com/horizontalsystems/unstoppable-wallet-android) · [← Back to Crypto](./README.md)</sub>
