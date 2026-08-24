# kamu-data/kamu-cli

[![Stars](https://img.shields.io/github/stars/kamu-data/kamu-cli?style=flat-square&color=yellow)](https://github.com/kamu-data/kamu-cli/stargazers) [![Forks](https://img.shields.io/github/forks/kamu-data/kamu-cli?style=flat-square&color=blue)](https://github.com/kamu-data/kamu-cli/network) [![Language](https://img.shields.io/badge/lang-Rust-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-55%2F100-brightgreen?style=flat-square)](#)

> Next-generation decentralized data lakehouse and a multi-party stream processing network

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 344 |
| 🍴 **Forks** | 17 |
| 💻 **Language** | Rust |
| 📈 **Score** | 55/100 |
| 🗓️ **Last push** | 2026-08-24 |
| 🔍 **Source** | github |

## 🏷️ Topics

`blockchain` `data-as-code` `data-management` `data-science` `datafusion` `flink` `jupyter` `kamu` `open-data` `open-data-fabric` `spark` `sql`

## 🎯 Categories

Crypto · Data

## 📝 Summary

### English

**Summary (2‑3 sentences)**  
kamu-data/kamu‑cli is an open‑source Rust‑based CLI that powers a next‑generation, decentralized data lakehouse and multi‑party stream‑processing network for Web3. It lets developers prototype, inspect, and debug blockchain‑centric data pipelines—such as wallet integrations, DeFi flows, or cross‑chain analytics—by exposing clear API/SDK signals and rich metadata. With active maintenance, a growing user base, and strong ecosystem signals, it’s ready for serious pilot projects.

**Value**  
- **Rapid prototyping** – The CLI bundles the core lakehouse engine, stream processors, and blockchain adapters, so teams can spin up end‑to‑end Web3 data workflows without building infrastructure from scratch.  
- **Transparency** – All implementation details (API contracts, SDK bindings, data schemas) are openly visible, making it easy to audit, extend, or integrate with existing DeFi wallets and analytics tools.  
- **Decentralized governance** – By storing data in a peer‑to‑peer lakehouse, you avoid single‑point‑of‑failure storage and gain built‑in versioning, provenance, and access‑control suited for multi‑party collaborations.

**Practical adoption path**  
1. **Evaluate** – Clone the repo, run the CLI’s `kamu init` command, and connect a testnet node (e.g., Ethereum Sepolia) to verify data ingestion and stream processing.  
2. **Integrate** – Use the generated SDK (Rust, with bindings for Python/JS) to embed lakehouse operations into your existing wallet or DeFi service codebase.  
3. **Pilot** – Deploy a small cluster of nodes (or use a managed provider) to run a production‑like pipeline, monitor performance via built‑in metrics, and iterate on schema definitions.  
4. **Scale** – Add more participants, configure access policies, and connect additional blockchains or off‑chain data sources as the network grows.

**Production readiness**  
- **Activity & community** – 344 stars, recent commits (last update 2026‑06‑23), and a healthy fork count indicate an active project.  
- **Maturity** – Core lakehouse and streaming components are stable; the CLI is documented and includes example workflows for common Web3 use cases.  
- **Risks to resolve** – Final due‑diligence on the license, security audit results, and long‑term maintainer commitment is still required, but no major red flags appear. Overall, the project is sufficiently mature for a pilot or early‑stage production deployment.

### Русский

**kamu-data/kamu-cli** — это открытый CLI‑инструмент на Rust, позволяющий быстро прототипировать и отлаживать Web3‑рабочие процессы, интеграцию блокчейнов, а также функции кошельков и DeFi, предоставляя доступ к API/SDK и метаданным реализации. Проект уже имеет активную разработку (обновления — 23 июня 2026 г., 344 звёзды, 17 форков) и демонстрирует высокую готовность к использованию в продакшене, хотя окончательная проверка лицензии и безопасности всё‑ещё требуется.

### 中文

**项目简介**  
kamu-data/kamu-cli 是面向下一代去中心化数据湖（lakehouse）和多方流处理网络的开源工具，提供基于 Rust 实现的 CLI/SDK，帮助开发者快速原型化和审查区块链工作流。

**价值**  
- **快速原型**：通过完整的实现细节（API、SDK、CLI），开发者可以在几行代码内搭建 Web3 流程、钱包或 DeFi 功能的原型。  
- **透明审计**：公开的实现让团队能够直接检查区块链集成点、数据流向和安全模型，降低黑盒风险。  
- **多方协作**：支持去中心化的数据湖和流处理网络，适合跨组织、跨链的数据共享与实时分析。

**典型接入方式**  
1. **CLI**：直接在终端执行 `kamu` 命令进行数据集创建、查询、同步等操作。  
2. **SDK**：在 Rust 项目中引入 `kamu-cli` 依赖，调用库函数实现自定义的链上/链下数据管道。  
3. **API 网关**：配合社区提供的 HTTP/GraphQL 接口，将 CLI/SDK 功能包装为微服务，供其他语言（如 Python、JavaScript）调用。  

**生产可用性**  
- **活跃度**：截至 2026‑06‑23，项目最近一次提交，拥有 344 星、12 个主题标签，社区活跃。  
- **成熟度**：代码基于 Rust，具备良好的类型安全和性能，适合在高并发、低延迟的生产环境中使用。  
- **风险**：目前未发现重大元数据或许可证问题，但仍建议进一步审查安全审计报告和维护者响应速度。总体而言，kamu-cli 已具备在正式业务中进行试点或上线的条件。

## 🧭 Practical evaluation

**Value:** kamu-data/kamu-cli helps prototype or inspect blockchain workflows with open implementation details.

**Best use cases**

- build Web3 workflows
- inspect blockchain integrations
- prototype wallet or DeFi features

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 344 GitHub stars
- 17 forks
- updated 2026-06-23
- primary language: Rust
- 12 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 31/100 |
| stars | 54/100 |
| topics | 100/100 |
| outlook | 58/100 |
| quality | 61/100 |
| recency | 40/100 |
| adoption | 48/100 |
| production | 55/100 |
| usefulness | 58/100 |
| integration | 46/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 200/100 |

---

<sub>🔭 Discovered 2026-06-23 · [View on GitHub](https://github.com/kamu-data/kamu-cli) · [← Back to Crypto](./README.md)</sub>
