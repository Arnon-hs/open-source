# taikoxyz/raiko

[![Stars](https://img.shields.io/github/stars/taikoxyz/raiko?style=flat-square&color=yellow)](https://github.com/taikoxyz/raiko/stargazers) [![Forks](https://img.shields.io/github/forks/taikoxyz/raiko?style=flat-square&color=blue)](https://github.com/taikoxyz/raiko/network) [![Language](https://img.shields.io/badge/lang-Rust-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-43%2F100-brightgreen?style=flat-square)](#)

> Multi-proofs for Taiko. SNARKS, STARKS and Trusted Execution Enclave. Our previous ZK-EVM circuits are deprecated.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 159 |
| 🍴 **Forks** | 134 |
| 💻 **Language** | Rust |
| 📈 **Score** | 43/100 |
| 🗓️ **Last push** | 2026-08-24 |
| 🔍 **Source** | github |

## 🏷️ Topics

_no topics_

## 🎯 Categories

Misc

## 📝 Summary

### English

**Brief Summary**  
Raiko (taikoxyz/raiko) is a Rust‑based framework that lets developers attach zero‑knowledge proof capabilities—SNARKs, STARKs, and Trusted Execution Enclave proofs—to the Taiko blockchain. It replaces the older ZK‑EVM circuits with a more flexible, multi‑proof architecture, making it easier to experiment with privacy‑preserving and integrity‑focused features.

**Value**  
- **Unified proof stack** – One library supports three major proof systems, so teams can choose the most suitable trade‑off (speed, proof size, trust assumptions) without rewriting code.  
- **Rapid prototyping** – The crate exposes high‑level APIs that let engineers add AI‑driven verification or data‑availability checks to smart contracts in minutes, accelerating proof‑of‑concepts and research projects.  
- **Open‑source community** – With ~160 stars and an active fork base, the project benefits from community contributions and transparent auditability, which is valuable for security‑sensitive blockchain applications.

**Practical Adoption Path**  
1. **Evaluate fit** – Clone the repo and run the provided examples; verify that the proof system you need (e.g., SNARK for fast verification) integrates with your existing Taiko node setup.  
2. **Prototype** – Use the high‑level `prove`/`verify` functions to wrap a simple contract or off‑chain AI model inference, iterating locally.  
3. **Manual integration review** – Because metadata on integration points is sparse, inspect the Cargo.toml dependencies, the enclave configuration files, and the proof‑generation pipelines to ensure they align with your build and security policies.  
4. **CI/CD hardening** – Add tests that generate and verify proofs in your pipeline, lock dependency versions, and optionally containerize the enclave runtime for reproducibility.  
5. **Production rollout** – Deploy the hardened library alongside your Taiko validators, monitor proof generation latency, and establish fallback mechanisms (e.g., switch to a different proof system) if performance thresholds are missed.

**Production Readiness**  
- **Maturity**: Medium. The codebase is actively maintained (last update 2026‑06‑29) and has a modest but engaged community, but the integration documentation is limited.  
- **Risk**: The integration path is not fully documented, so teams must allocate time for manual inspection and testing of dependencies, especially the enclave components.  
- **Suitability**: Ideal for internal prototypes, R&D labs, or early‑stage products that need flexible ZK proof capabilities. With proper dependency pinning, security review of the enclave, and performance benchmarking, it can be hardened for production use, but it is not a turnkey solution for mission‑critical deployments without additional engineering effort.

### Русский

Резюме проекта taikoxyz/raiko:

Проект taikoxyz/raiko представляет собой набор инструментов для добавления искусственного интеллекта в существующие системы, позволяя прототипировать и тестировать AI-функции без необходимости создания новой модели. Применяя технологии SNARKS, STARKS и Trusted Execution Enclave, проект обеспечивает безопасность и прозрачность данных. Проект готов для использования в прототипировании и внутренних рабочих процессах, но требует тщательного отбора и проверки перед внедрением в производство.

### 中文

**项目简介（2‑3 句）**  
Taiko Raiko（taikoxyz/raiko）是为 Taiko 区块链提供多种零知识证明（SNARK、STARK）以及可信执行环境（Enclave）实现的库，取代了已废弃的 ZK‑EVM 电路。它以 Rust 编写，旨在让开发者在现有链上快速加入高效、可验证的隐私/可扩展性功能。

**价值**  
- **多证明支持**：一次集成即可在同一框架下切换 SNARK、STARK 或硬件可信执行，满足不同安全/性能需求。  
- **降低研发成本**：提供开箱即用的证明生成、验证和链上提交工具，省去从头实现零知识证明的复杂工作。  
- **生态兼容**：专为 Taiko 设计，能够直接与其 L2 方案对接，帮助项目在保持去中心化的同时提升吞吐和隐私。

**典型接入方式**  
1. **依赖引入**：在 Rust 项目 `Cargo.toml` 中添加 `raiko` 作为依赖。  
2. **选择证明后端**：通过配置文件或环境变量指定使用 `snark`, `stark` 或 `enclave`（如 Intel SGX）实现。  
3. **调用 API**：使用 `RaikoProver::prove(...)` 生成证明，随后用 `RaikoVerifier::verify(...)` 在链上或离线验证。  
4. **链上集成**：将生成的证明打包进 Taiko 的交易/rollup 数据结构，提交到对应的验证合约。  
5. **手动审查**：由于元数据中缺少完整的集成示例，建议在本地先跑完整的端到端测试（包括证明生成、验证、链上提交），确认依赖版本、硬件要求（如 SGX）以及链上合约地址。

**生产可用性**  
- **成熟度**：GitHub 近 160 星、134 叉，最近一次更新在 2026‑06‑29，代码活跃度尚可。  
- **适用场景**：适合原型开发、内部工具或对安全性有明确需求的业务（如隐私交易、跨链桥）。  
- **准备度**：属于 **中等**（Medium）级别——功能可用但集成路径不够透明，需要自行验证依赖兼容性、硬件支持以及升级维护成本后方可在生产环境使用。  
- **风险**：缺少官方的“一键集成”文档或 CI 示例，集成前务必进行手动审查和性能基准测试，以避免意外的部署成本或安全隐患。

## 🧭 Practical evaluation

**Value:** taikoxyz/raiko helps add AI capability without starting from a blank model stack.

**Best use cases**

- prototype AI features
- build RAG or agent workflows
- evaluate model tooling

**Integration notes:** Needs manual inspection before adoption because integration signals are sparse in the discovered metadata.

**Production readiness:** Medium: useful for prototypes or internal workflows, with dependency and maintenance checks before production.

**Quality signals**

- 159 GitHub stars
- 134 forks
- updated 2026-06-29
- primary language: Rust

**Risks:** Integration path is not obvious from metadata; validate setup cost before committing.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 53/100 |
| stars | 47/100 |
| topics | 0/100 |
| outlook | 45/100 |
| quality | 47/100 |
| recency | 40/100 |
| adoption | 49/100 |
| production | 48/100 |
| usefulness | 42/100 |
| integration | 30/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 0/100 |

---

<sub>🔭 Discovered 2026-06-29 · [View on GitHub](https://github.com/taikoxyz/raiko) · [← Back to Misc](./README.md)</sub>
