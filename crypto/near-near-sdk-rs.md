# near/near-sdk-rs

[![Stars](https://img.shields.io/github/stars/near/near-sdk-rs?style=flat-square&color=yellow)](https://github.com/near/near-sdk-rs/stargazers) [![Forks](https://img.shields.io/github/forks/near/near-sdk-rs?style=flat-square&color=blue)](https://github.com/near/near-sdk-rs/network) [![Language](https://img.shields.io/badge/lang-Rust-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-62%2F100-brightgreen?style=flat-square)](#)

> Rust library for writing NEAR smart contracts

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 509 |
| 🍴 **Forks** | 279 |
| 💻 **Language** | Rust |
| 📈 **Score** | 62/100 |
| 🗓️ **Last push** | 2026-09-05 |
| 🔍 **Source** | github |

## 🏷️ Topics

`blockchain` `nearprotocol` `rust` `sdk` `wasm`

## 🎯 Categories

Crypto · Libraries & SDKs

## 📝 Summary

### English

**Brief Summary**  
near‑sdk‑rs is an open‑source Rust crate that provides the core APIs, macros, and tooling for writing, testing, and deploying smart contracts on the NEAR blockchain. It lets developers prototype Web3, wallet, or DeFi workflows with full visibility into the underlying implementation, making it a handy bridge between Rust‑based back‑ends and NEAR’s runtime.  

**Value**  
- **Transparent blockchain integration** – By exposing the SDK’s API surface, data types, and CLI helpers, developers can inspect exactly how contract logic interacts with NEAR’s state machine, which is useful for learning, auditing, or building custom tooling.  
- **Rapid prototyping** – The crate’s ergonomic macros and built‑in testing utilities let teams spin up functional contracts quickly, accelerating proof‑of‑concepts for DeFi, NFT, or wallet features.  
- **Community‑backed ecosystem** – With >500 stars, a growing fork base, and active Rust contributions, the library benefits from community‑driven improvements and examples that can be reused in production projects.  

**Practical Adoption Path**  
1. **Evaluate** – Clone the repo, run the built‑in unit tests, and experiment with the sample contracts to verify that the SDK meets your functional requirements.  
2. **Integrate** – Add `near-sdk = "X.Y.Z"` to your Cargo.toml, replace placeholder macros (`#[near_bindgen]`, `env::log`, etc.) with your business logic, and use the provided CLI (`near-cli`) for local simulation.  
3. **Test & Audit** – Leverage the SDK’s test harness (simulated blockchain environment) and run static analysis tools (e.g., cargo-audit, cargo-deny) to catch dependency vulnerabilities.  
4. **Deploy** – After passing internal QA, deploy to NEAR testnet, then to mainnet once you have confirmed gas costs, storage requirements, and upgrade procedures.  

**Production Readiness**  
- **Maturity**: Medium. The library is actively maintained (last update 2026‑06‑26) and widely used in the NEAR community, but it still requires a thorough security review and dependency vetting before mission‑critical deployment.  
- **Stability**: The core API is relatively stable, but breaking changes can appear in major version bumps; pinning a specific version in Cargo.toml mitigates this risk.  
- **Operational considerations**: Ensure you have a process for monitoring SDK releases, applying security patches, and managing Rust toolchain compatibility.  

In short, near‑sdk‑rs is a solid foundation for Rust‑based NEAR contracts, ideal for prototyping and internal tooling, and can be hardened for production with standard security and dependency‑management practices.

### Русский

near/near-sdk-rs — это открытая библиотека на Rust, позволяющая быстро писать и отлаживать смарт‑контракты для блокчейна NEAR, предоставляя полностью открытый API, CLI и метаданные языка. Она идеальна для прототипирования Web3‑функционала (кошельков, DeFi‑модулей) и анализа интеграций с блокчейном, при этом имеет умеренную готовность к продакшну: достаточно зрелая (≈ 500 звёзд, активные форки) для внутренних и пилотных проектов, но требует проверки лицензии, безопасности и поддержки перед масштабным внедрением.

### 中文

**项目简介**  
near/near-sdk-rs 是一个基于 Rust 的开发套件，专门用于编写、编译和部署在 NEAR 区块链上的智能合约。它提供了完整的 API、宏和 CLI 工具，使开发者能够以安全、高效的方式在 Rust 中实现 Web3 业务逻辑。

**价值**  
- **快速原型**：通过 Rust 的零成本抽象和强类型检查，能够在几行代码内搭建完整的 DeFi、钱包或其他链上业务原型。  
- **透明实现**：开源实现让开发者可以直接审查合约底层逻辑、序列化方案和跨合约调用细节，降低信任成本。  
- **生态兼容**：与 NEAR 官方节点、钱包 SDK 以及常见的前端框架（如 near-api-js）无缝对接，适合构建完整的 Web3 工作流。

**典型接入方式**  
1. **依赖引入**：在 Cargo.toml 中添加 `near-sdk = "X.Y.Z"`（或直接引用仓库），即可使用宏 `#[near_bindgen]`、存储模型等核心功能。  
2. **本地编译&测试**：使用 `cargo test` 运行单元测试，或通过 `near-sdk-sim` 进行链上模拟。  
3. **部署**：利用官方 `near-cli`（或 `near-api-rs`）将编译好的 `.wasm` 合约上传至 NEAR 测试网/主网。  
4. **CI/CD 集成**：在 CI 流程中加入 `cargo fmt`、`cargo clippy` 与 `cargo audit`，确保代码风格、质量和安全依赖。

**生产可用性**  
- **成熟度**：项目已有 500+ 星、近 300 次 fork，活跃度高，最近一次提交在 2026‑06‑26，代码质量和文档相对完善。  
- **适用场景**：非常适合内部原型、功能验证以及中小规模的生产合约；大规模高并发场景仍需自行评估依赖的安全审计和运行时性能。  
- **风险与准备**：在正式上线前建议完成以下工作：  
  1. **许可证审查**：确认 MIT/Apache 双许可证符合企业合规要求。  
  2. **安全审计**：使用 `cargo audit` 检查依赖漏洞，并对关键合约逻辑进行第三方审计。  
  3. **运维监控**：结合 NEAR 官方监控工具或自建日志系统，监控合约调用延迟、gas 消耗等关键指标。  

总体而言，near/near-sdk-rs 在功能完整性和开发便利性上已具备中等到较高的生产可用性，只要完成常规的安全与运维审查，即可在实际业务中安全使用。

## 🧭 Practical evaluation

**Value:** near/near-sdk-rs helps prototype or inspect blockchain workflows with open implementation details.

**Best use cases**

- build Web3 workflows
- inspect blockchain integrations
- prototype wallet or DeFi features

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** Medium: useful for prototypes or internal workflows, with dependency and maintenance checks before production.

**Quality signals**

- 509 GitHub stars
- 279 forks
- updated 2026-06-26
- primary language: Rust
- 5 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 61/100 |
| stars | 58/100 |
| topics | 63/100 |
| outlook | 71/100 |
| quality | 71/100 |
| recency | 80/100 |
| adoption | 59/100 |
| production | 68/100 |
| usefulness | 58/100 |
| integration | 46/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 200/100 |

---

<sub>🔭 Discovered 2026-06-26 · [View on GitHub](https://github.com/near/near-sdk-rs) · [← Back to Crypto](./README.md)</sub>
