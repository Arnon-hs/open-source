# filecoin-project/lotus

[![Stars](https://img.shields.io/github/stars/filecoin-project/lotus?style=flat-square&color=yellow)](https://github.com/filecoin-project/lotus/stargazers) [![Forks](https://img.shields.io/github/forks/filecoin-project/lotus?style=flat-square&color=blue)](https://github.com/filecoin-project/lotus/network) [![Language](https://img.shields.io/badge/lang-Go-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-52%2F100-brightgreen?style=flat-square)](#)

> Reference implementation of the Filecoin protocol, written in Go

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 3k |
| 🍴 **Forks** | 1.4k |
| 💻 **Language** | Go |
| 📈 **Score** | 52/100 |
| 🗓️ **Last push** | 2026-08-24 |
| 🔍 **Source** | github |

## 🏷️ Topics

`blockchain` `filecoin` `golang` `ipfs`

## 🎯 Categories

Crypto

## 📝 Summary

### English

**Brief Summary (2‑3 sentences)**  
The Lotus repository is the reference Go implementation of the Filecoin protocol, providing a full node, miner, and client stack for interacting with the decentralized storage network. With over 2,900 stars, active maintenance, and recent releases, it serves as a practical foundation for building, testing, and inspecting Web3 storage workflows, wallets, and DeFi integrations. Its open‑source nature makes it a solid candidate for prototyping and early‑stage production pilots.

**Value**  
- **Transparency & Control:** By exposing the complete protocol logic, developers can audit, customize, and extend core Filecoin functionality without relying on closed‑source services.  
- **Rapid Prototyping:** Ready‑made APIs and command‑line tools let teams spin up local or testnet nodes in minutes, accelerating the development of storage‑centric dApps, wallet features, or cross‑chain DeFi primitives.  
- **Ecosystem Leverage:** Lotus is the de‑facto reference client, meaning most tooling, documentation, and community support revolve around it, reducing integration friction.

**Practical Adoption Path**  
1. **Proof‑of‑Concept (PoC):** Clone the repo, follow the README to launch a local devnet or connect to the Filecoin testnet; use the provided Go SDK to perform simple storage deals or query chain state.  
2. **Feature Validation:** Extend the client or miner modules to implement the specific workflow (e.g., custom escrow logic, wallet UI, or analytics). Run integration tests against the testnet to verify correctness and performance.  
3. **Pilot Deployment:** Deploy a hardened Lotus node in a controlled cloud environment, enable TLS, and configure monitoring/metrics. Integrate with your existing services via the RPC API or Go client libraries.  
4. **Production Roll‑out:** Harden the node (firewall, secrets management), enable persistent storage, and join the Filecoin mainnet. Leverage the active maintainer community for security patches and upgrades.

**Production Readiness**  
- **Activity & Adoption:** Recent commits (as of 2026‑05‑11), a large star/fork count, and widespread use in the Filecoin ecosystem indicate strong momentum.  
- **Stability:** The codebase is mature, with comprehensive test coverage and documented upgrade paths for protocol changes.  
- **Risk Considerations:** While no major metadata or licensing issues are apparent, a final security audit, review of the Apache‑2.0 license compliance, and confirmation of active maintainers are advisable before mission‑critical deployment.  

Overall, Lotus is highly production‑ready for pilots and can be scaled to full‑scale deployments with standard DevOps hardening practices.

### Русский

**filecoin-project/lotus** — это референс‑реализация протокола Filecoin на Go, позволяющая быстро прототипировать и исследовать блокчейн‑процессы благодаря полностью открытой кодовой базе. Типичный сценарий внедрения — построение Web3‑воркфлоу, проверка интеграций с Filecoin, а также разработка кошельков или DeFi‑фич в небольшом proof‑of‑concept, после чего проект готов к масштабированию в продакшн. Репозиторий демонстрирует высокий уровень готовности: активные коммиты, более 2 900 звёзд, широкое принятие в экосистеме и стабильную поддержку, что делает его надёжным кандидатом для серьёзных пилотных запусков.

### 中文

**项目简介**  
filecoin-project/lotus 是 Filecoin 协议的官方实现，使用 Go 语言编写，提供完整的节点、矿工、钱包等功能，是探索和验证 Filecoin 区块链工作流的首选开源代码库。

**价值**  
- **透明可查**：完整的协议实现让开发者能够直接阅读、调试和改进区块链逻辑。  
- **快速原型**：提供丰富的 API 与 CLI，帮助在 Web3、DeFi、钱包等场景下快速搭建原型或进行集成测试。  
- **生态支撑**：拥有数千星标、活跃的社区和多家项目的实际采用，降低了自行实现协议的成本和风险。

**典型接入方式**  
1. **本地部署**：克隆仓库后按照 README 中的步骤运行 `lotus daemon` 启动全节点或 `lotus miner` 启动矿工节点。  
2. **API 调用**：通过 JSON‑RPC 或 gRPC 接口（如 `lotus client`、`lotus wallet`）在业务系统中调用存储、检索、支付等功能。  
3. **容器化**：官方提供 Docker 镜像，可在 Kubernetes 或 Docker Compose 中快速拉起测试网络，适合作为 CI/CD 流水线的区块链环境。  
4. **SDK/库**：在 Go 项目中直接引用 `github.com/filecoin-project/lotus` 包，利用其内部库实现自定义链上交互。

**生产可用性**  
- **成熟度高**：截至 2026‑05‑11，项目活跃度强，近期有多次代码更新，社区贡献者众多。  
- **稳定性**：已在多个公共和企业级 Filecoin 主网/测试网中运行，具备生产级别的容错和监控方案。  
- **准备度**：适合作为正式业务的底层设施，建议先在小规模 PoC 中验证部署脚本和安全配置（如密钥管理、访问控制），随后逐步扩展至全链路生产环境。  

总体而言，Lotus 具备高可靠性和丰富的集成手段，是在 Filecoin 生态中实现区块链功能的首选开源实现。

## 🧭 Practical evaluation

**Value:** filecoin-project/lotus helps prototype or inspect blockchain workflows with open implementation details.

**Best use cases**

- build Web3 workflows
- inspect blockchain integrations
- prototype wallet or DeFi features

**Integration notes:** Looks feasible to evaluate, but integration should start with a small proof of concept and README check.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 2990 GitHub stars
- 1364 forks
- updated 2026-05-11
- primary language: Go
- 4 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 78/100 |
| stars | 74/100 |
| topics | 50/100 |
| outlook | 49/100 |
| quality | 61/100 |
| recency | 20/100 |
| adoption | 75/100 |
| production | 51/100 |
| usefulness | 42/100 |
| integration | 46/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 100/100 |

---

<sub>🔭 Discovered 2026-05-11 · [View on GitHub](https://github.com/filecoin-project/lotus) · [← Back to Crypto](./README.md)</sub>
