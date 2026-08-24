# rpcpool/yellowstone-grpc

[![Stars](https://img.shields.io/github/stars/rpcpool/yellowstone-grpc?style=flat-square&color=yellow)](https://github.com/rpcpool/yellowstone-grpc/stargazers) [![Forks](https://img.shields.io/github/forks/rpcpool/yellowstone-grpc?style=flat-square&color=blue)](https://github.com/rpcpool/yellowstone-grpc/network) [![Language](https://img.shields.io/badge/lang-Rust-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-57%2F100-brightgreen?style=flat-square)](#)

> Triton's Dragon's Mouth Yellowstone gRPC service for high-performance Solana streaming

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 972 |
| 🍴 **Forks** | 347 |
| 💻 **Language** | Rust |
| 📈 **Score** | 57/100 |
| 🗓️ **Last push** | 2026-08-24 |
| 🔍 **Source** | github |

## 🏷️ Topics

`dragons-mouth` `grpc` `solana` `yellowstone` `yellowstone-grpc`

## 🎯 Categories

Crypto

## 📝 Summary

### English

**Brief Summary (2‑3 sentences)**  
rpcpool/yellowstone-grpc provides a high‑performance, open‑source gRPC service that streams Solana blockchain data, enabling developers to prototype, inspect, and integrate Web3 workflows such as wallets, DeFi protocols, or analytics pipelines. With over 970 stars, active maintenance, and a Rust codebase, it is positioned as a production‑ready building block for Solana‑centric applications.

**Value**  
- **Deep visibility**: Offers real‑time access to Solana ledger events (blocks, transactions, accounts) without the overhead of running a full validator.  
- **Speed & scalability**: Built in Rust and optimized for low‑latency gRPC streaming, it can handle high‑throughput workloads typical of DeFi and NFT platforms.  
- **Open implementation**: All protocol details are exposed, allowing teams to audit, extend, or customize the data pipeline for bespoke use cases.

**Practical Adoption Path**  
1. **Proof‑of‑Concept**: Clone the repo, run the provided Docker compose or local binary, and follow the README to query a few sample streams (e.g., slot notifications).  
2. **Integration**: Wrap the gRPC client in your service layer (Node.js, Python, or Rust) and replace any ad‑hoc RPC calls with the streaming endpoints.  
3. **Testing & Scaling**: Deploy the service in a staging Kubernetes cluster, monitor latency and resource usage, and tune the number of stream workers as needed.  
4. **Production Roll‑out**: Harden the deployment with TLS, enable authentication, and configure autoscaling based on observed throughput.

**Production Readiness**  
- **Activity & Adoption**: Recent commits (as of 2026‑06‑23), 972 stars, 347 forks, and usage in several open‑source Solana tooling projects indicate strong community momentum.  
- **Reliability**: The Rust implementation and gRPC transport are battle‑tested for low‑latency, high‑concurrency scenarios.  
- **Risks to Address**: Conduct a final review of the MIT/Apache license compatibility, perform a security audit of the service’s exposure surface, and verify that maintainers are responsive to issues before committing to a critical production environment.  

Overall, Yellowstone‑gRPC is a mature OSS component that can be evaluated with a small PoC and, once vetted, promoted to a core data‑ingestion service for production Web3 applications.

### Русский

**rpcpool/yellowstone-grpc** — это высокопроизводительная gRPC‑реализация сервиса Triton’s Dragon’s Mouth Yellowstone, позволяющая быстро прототипировать и отлаживать Web3‑процессы в Solana, а также исследовать детали интеграций блокчейна без закрытого кода. Для внедрения рекомендуется начать с небольшого proof‑of‑concept, следуя инструкциям в README, после чего сервис можно масштабировать до production‑уровня, поскольку проект активно поддерживается (обновления 2026‑06‑23), имеет 972 звезды, 347 форков и хорошую экосистемную совместимость. Несмотря на отсутствие серьёзных метаданных‑рисков, финальная проверка лицензии и безопасности всё‑ещё требуется.

### 中文

**项目简介（2‑3 句）**  
rpcpool/yellowstone-grpc 是 Triton 开发的 “Dragon's Mouth Yellowstone” gRPC 服务，专为 Solana 高吞吐量数据流而设计，提供低延迟、可扩展的区块链实时订阅接口。它以 Rust 实现，开源且保持活跃更新，适合快速原型化和深入审计 Solana 工作流。

**价值**  
- **快速原型**：通过统一的 gRPC 接口即可获取 Solana 的块、交易、账户变更等实时数据，省去自行搭建节点或解析 RPC 响应的时间成本。  
- **透明实现**：全部实现细节公开，开发者可以直接阅读源码，便于调试、定制和安全审计。  
- **高性能**：基于 Rust 与 gRPC 的零拷贝、流式传输特性，能够在毫秒级响应大规模订阅请求，满足 Web3、DeFi、钱包等对实时性的苛刻需求。

**典型接入方式**  
1. **阅读 README**：确认所需的 Rust 版本、依赖库以及 gRPC 代码生成步骤。  
2. **启动服务**：使用提供的 Docker 镜像或直接在本地运行 `cargo run --release`，配置 Solana RPC 节点地址和监听端口。  
3. **生成客户端**：利用 `prost`/`tonic`（或其他语言的 gRPC 插件）从 `proto` 文件生成对应语言的客户端代码。  
4. **小规模 PoC**：在业务代码中创建一个 gRPC 客户端，订阅 `SubscribeBlocks`、`SubscribeTransactions` 等流式接口，验证数据完整性和延迟。  
5. **逐步扩展**：在 PoC 成功后，依据业务需求增加并发订阅、负载均衡或自定义过滤逻辑。

**生产可用性**  
- **活跃度**：截至 2026‑06‑23，项目拥有 972 ★、347 Fork，最近一次提交在同一天，表明维护活跃。  
- **生态兼容**：Rust 主语言、标准 gRPC 接口，易于在多语言微服务体系中集成。  
- **可靠性**：社区已在多个公开项目中使用，具备实战验证；但仍建议在正式环境前完成安全审计、监控告警及容灾演练。  
- **总体评估**：在完成许可证、依赖安全扫描以及维护者确认后，可视为 **高生产就绪度**，适合作为核心链上数据供应层进行正式部署。

## 🧭 Practical evaluation

**Value:** rpcpool/yellowstone-grpc helps prototype or inspect blockchain workflows with open implementation details.

**Best use cases**

- build Web3 workflows
- inspect blockchain integrations
- prototype wallet or DeFi features

**Integration notes:** Looks feasible to evaluate, but integration should start with a small proof of concept and README check.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 972 GitHub stars
- 347 forks
- updated 2026-06-23
- primary language: Rust
- 5 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 64/100 |
| stars | 64/100 |
| topics | 63/100 |
| outlook | 58/100 |
| quality | 63/100 |
| recency | 40/100 |
| adoption | 64/100 |
| production | 56/100 |
| usefulness | 58/100 |
| integration | 46/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 100/100 |

---

<sub>🔭 Discovered 2026-06-23 · [View on GitHub](https://github.com/rpcpool/yellowstone-grpc) · [← Back to Crypto](./README.md)</sub>
