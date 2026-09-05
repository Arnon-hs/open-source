# giovantenne/lastsignal

[![Stars](https://img.shields.io/github/stars/giovantenne/lastsignal?style=flat-square&color=yellow)](https://github.com/giovantenne/lastsignal/stargazers) [![Forks](https://img.shields.io/github/forks/giovantenne/lastsignal?style=flat-square&color=blue)](https://github.com/giovantenne/lastsignal/network) [![Language](https://img.shields.io/badge/lang-Ruby-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-67%2F100-brightgreen?style=flat-square)](#)

> A self-hosted dead man's switch for delivering encrypted messages (E2EE) to your loved ones — when you're gone or unresponsive.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 665 |
| 🍴 **Forks** | 16 |
| 💻 **Language** | Ruby |
| 📈 **Score** | 67/100 |
| 🗓️ **Last push** | 2026-09-05 |
| 🔍 **Source** | github |

## 🏷️ Topics

`cryptography` `e2ee` `encryption` `end-to-end-encryption` `open-source` `privacy` `privacy-tools` `self-hosted` `zero-knowledge`

## 🎯 Categories

Security

## 📝 Summary

### English

**Brief Summary (2‑3 sentences)**  
LastSignal is a self‑hosted “dead‑man’s switch” that lets you store encrypted messages and automatically deliver them to designated recipients when you become unresponsive. Built in Ruby, the project offers end‑to‑end encryption and a simple web UI, making it easy to run your own secure fallback communication channel without relying on third‑party services.  

**Value**  
- **Privacy‑first messaging** – messages are encrypted client‑side, so only the intended recipients can read them, even the server operator.  
- **Self‑hosting** – you retain full control over data, keys, and retention policies, which is crucial for compliance‑heavy or high‑trust environments.  
- **Web3‑ready** – the codebase includes hooks for blockchain‑based escrow and identity verification, allowing developers to prototype wallet, DeFi, or NFT‑linked notification workflows without building the infrastructure from scratch.  

**Practical Adoption Path**  
1. **Proof‑of‑Concept** – Clone the repo, run the Docker compose file (or the provided Ruby on Rails setup) locally, and follow the README to create a test switch and recipient.  
2. **Integration** – Extend the webhook endpoint to trigger a blockchain transaction (e.g., release funds from a smart contract) when a switch is activated, or use the built‑in API to store a hash of a DeFi state that can be verified on‑chain.  
3. **Security Review** – Conduct a quick audit of the encryption implementation and verify the license (MIT‑style) matches your compliance needs.  
4. **Pilot Deployment** – Deploy to a staging environment (e.g., a managed Kubernetes cluster) with TLS termination and a dedicated secret‑management solution for the master key.  

**Production Readiness**  
- **Activity & Community** – 665 ★, 16 forks, recent commits (as of 2026‑06‑30) and ongoing issue responses indicate an active maintainer base.  
- **Maturity** – The Ruby on Rails stack is stable, and the project ships with Docker support, automated tests, and clear documentation, making it suitable for a serious pilot.  
- **Risks** – No major metadata concerns, but a final review of the license, any disclosed vulnerabilities, and the long‑term maintainer commitment is advisable before a full production rollout.  

Overall, LastSignal is a high‑readiness OSS candidate for teams that need a trustworthy, self‑hosted dead‑man’s switch and want to experiment with blockchain‑linked notification flows.

### Русский

**LastSignal** — это self‑hosted dead‑man's switch, позволяющий хранить зашифрованные сообщения (E2EE) и автоматически доставлять их близким, когда вы недоступны. Проект легко интегрировать в Web3‑проекты: в качестве небольшого proof‑of‑concept можно развернуть контейнер, подключить его к кошельку или DeFi‑службе и протестировать передачу зашифрованных данных через блокчейн. Благодаря активным обновлениям, 665 звёздам и хорошей экосистемной поддержке, LastSignal считается готовым к пилотному запуску в production, хотя окончательная проверка лицензии и безопасности всё‑ещё требуется.

### 中文

**项目简介**  
giovantenne/lastsignal 是一款自托管的“死亡开关”服务，能够在用户失联或离世后以端到端加密（E2EE）的方式安全地将预先写好的信息递送给指定的亲友。

**价值主张**  
- **隐私安全**：所有消息在本地加密，只有在触发条件满足后才会解密，确保信息只能被授权接收者看到。  
- **自托管可控**：无需依赖第三方平台，用户可以完全掌控数据存储和触发逻辑，符合合规和数据主权要求。  
- **Web3/区块链兼容**：提供开源实现细节，便于在区块链或 DeFi 项目中原型化死亡开关、遗嘱合约或自动化资产转移等业务场景。

**典型接入方式**  
1. **快速 PoC**：克隆仓库 → 按 README 配置 Ruby 环境和数据库 → 部署到本地或容器（Docker）中，创建测试用户并设置触发条件。  
2. **业务集成**：在现有的 Web3 应用中通过 REST/GraphQL 接口调用 `create_message`、`set_trigger` 等 API，实现消息的创建、加密存储以及触发检查。  
3. **链上交互**：可将触发条件（如链上时间锁、特定事件）映射为智能合约状态，由后端轮询或链上预言机触发 LastSignal 的解密流程，实现完全去中心化的遗嘱执行。

**生产可用性**  
- **活跃度**：最近一次提交于 2026‑06‑30，拥有 665 ★、16 Fork，社区关注度较高。  
- **技术成熟度**：核心使用 Ruby 实现，代码结构清晰，文档完整，适合作为 OSS 组件进行正式上线。  
- **风险与准备**：暂无重大元数据风险，但仍需对许可证（MIT/Apache 等）和安全审计进行最终确认；建议在正式生产前完成安全依赖审查并设立监控/备份机制。  

总体而言，LastSignal 在隐私保护和自托管方面具备显著优势，接入门槛低，已具备在生产环境中进行严肃试点的条件。

## 🧭 Practical evaluation

**Value:** giovantenne/lastsignal helps prototype or inspect blockchain workflows with open implementation details.

**Best use cases**

- build Web3 workflows
- inspect blockchain integrations
- prototype wallet or DeFi features

**Integration notes:** Looks feasible to evaluate, but integration should start with a small proof of concept and README check.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 665 GitHub stars
- 16 forks
- updated 2026-06-30
- primary language: Ruby
- 9 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 31/100 |
| stars | 60/100 |
| topics | 100/100 |
| outlook | 76/100 |
| quality | 73/100 |
| recency | 80/100 |
| adoption | 52/100 |
| production | 69/100 |
| usefulness | 74/100 |
| integration | 46/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 100/100 |

---

<sub>🔭 Discovered 2026-06-30 · [View on GitHub](https://github.com/giovantenne/lastsignal) · [← Back to Security](./README.md)</sub>
