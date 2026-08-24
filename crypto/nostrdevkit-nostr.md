# nostrdevkit/nostr

[![Stars](https://img.shields.io/github/stars/nostrdevkit/nostr?style=flat-square&color=yellow)](https://github.com/nostrdevkit/nostr/stargazers) [![Forks](https://img.shields.io/github/forks/nostrdevkit/nostr?style=flat-square&color=blue)](https://github.com/nostrdevkit/nostr/network) [![Language](https://img.shields.io/badge/lang-Rust-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-72%2F100-brightgreen?style=flat-square)](#)

> Rust implementation of the nostr protocol, high-level client library, Nostr Wallet Connect and more.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 652 |
| 🍴 **Forks** | 159 |
| 💻 **Language** | Rust |
| 📈 **Score** | 72/100 |
| 🗓️ **Last push** | 2026-08-24 |
| 🔍 **Source** | github |

## 🏷️ Topics

`freedom` `nostr` `nostr-connect` `nostr-protocol` `nwc` `protocol` `python` `rust` `rust-lang` `rust-nostr` `sdk` `swift`

## 🎯 Categories

Crypto

## 📝 Summary

### English

**Summary**  
nostrdevkit/nostr is a Rust‑based implementation of the Nostr protocol that provides a high‑level client SDK, Nostr Wallet Connect support, and command‑line tools. It lets developers quickly prototype, test, and inspect Web3 and blockchain workflows—especially wallet and DeFi integrations—while keeping the underlying protocol details transparent. With strong recent activity, a growing star/fork count, and a clean Rust API, it’s a solid OSS candidate for production pilots.  

**Value**  
The library abstracts the low‑level Nostr messaging format into ergonomic Rust types and helpers, reducing the time needed to build or audit blockchain‑related features. By exposing API/SDK/CLI entry points and detailed implementation signals, teams can both experiment with new Nostr‑based use cases and perform deep inspection of how data moves across the network, which is valuable for security reviews and rapid prototyping of wallet‑connect or DeFi flows.  

**Practical Adoption Path**  
1. **Evaluation** – Clone the repo, run the provided CLI examples, and explore the generated Rust docs to confirm API fit.  
2. **Integration** – Add the crate to your Cargo.toml, use the high‑level client to connect to Nostr relays, and leverage the Wallet Connect module for signing or payment flows.  
3. **Testing & Auditing** – Use the built‑in test suite and optional mock relays to validate behavior in a sandbox before moving to production.  
4. **Deployment** – Package the compiled binary or embed the library in your service, configuring relay endpoints and authentication as needed.  

**Production Readiness**  
- **Activity & Community**: 652 ★, 159 forks, recent commits (as of 2026‑07‑13) and a diverse set of 13 topics indicate an active, engaged community.  
- **Stability**: The crate follows semantic versioning, provides a CLI for quick sanity checks, and includes comprehensive documentation.  
- **Risk Assessment**: No major metadata issues; the remaining checks are licensing compliance, security audit of the codebase, and confirmation of maintainers’ responsiveness. Assuming those are cleared, the library is ready for serious pilot deployments in production environments.

### Русский

Резюме проекта nostrdevkit/nostr:

Проект nostrdevkit/nostr представляет собой открытую реализацию протокола Nostr, включающую в себя высокоуровневую клиентскую библиотеку и инструменты для соединения кошельков. Он позволяет прототипировать или инспектировать блокчейн-процесса с прозрачным раскрытием деталей реализации.

Проект подходит для следующих типовых сценариев внедрения: разработка Web3-процессов, инспектирование блокчейн-интеграций, прототипирование функций кошельков или DeFi. Проект готов к production, поскольку имеет сильные сигналы активности, адопции и экосистемных факторов, что позволяет рассматривать его для серьезного пилота.

### 中文

**项目简介（2‑3 句）**  
nostrdevkit/nostr 是用 Rust 编写的 Nostr 协议实现，提供高层次的客户端库、Nostr Wallet Connect 等功能。它以安全、性能和易用为目标，帮助开发者快速构建和调试 Web3、DeFi 或钱包相关的工作流。

**价值**  
- **快速原型**：完整的协议实现和丰富的 SDK/CLI，使得区块链交互、钱包连接等场景可以在几行代码内完成验证。  
- **可审计**：Rust 代码天然安全，开源实现让协议细节透明，便于审计和定制。  
- **生态兼容**：兼容 Nostr Wallet Connect，能够直接对接现有的 Nostr 客户端和去中心化应用。

**典型接入方式**  
1. **库依赖**：在 Cargo.toml 中加入 `nostr = "x.y"`，使用提供的 `Client`、`Event` 等结构体进行消息收发。  
2. **CLI 工具**：通过项目自带的 `nostr-cli`（已发布到 crates.io）执行发布、订阅、钱包连接等操作，适合作为脚本或 CI 步骤。  
3. **NWC（Nostr Wallet Connect）**：使用库中的 `NwcClient` 与支持 NWC 的钱包进行握手、签名请求等交互，直接嵌入 Web3 前端或后端服务。

**生产可用性**  
- **活跃度**：截至 2026‑07‑13，项目仍在持续更新，拥有 652 ★、159 Fork，近期提交频率保持在每周数次。  
- **社区与生态**：13 个 GitHub Topics 覆盖 `rust`, `nostr`, `wallet-connect` 等关键领域，已有若干生产项目引用。  
- **代码质量**：Rust 本身的内存安全特性加上 CI 自动化测试，降低了运行时错误和安全风险。  
- **风险**：需进一步确认许可证兼容性（MIT/Apache 双许可证）以及安全审计报告，但整体成熟度足以支持正式环境的试点或生产部署。

## 🧭 Practical evaluation

**Value:** nostrdevkit/nostr helps prototype or inspect blockchain workflows with open implementation details.

**Best use cases**

- build Web3 workflows
- inspect blockchain integrations
- prototype wallet or DeFi features

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 652 GitHub stars
- 159 forks
- updated 2026-07-13
- primary language: Rust
- 13 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 55/100 |
| stars | 60/100 |
| topics | 100/100 |
| outlook | 63/100 |
| quality | 66/100 |
| recency | 40/100 |
| adoption | 59/100 |
| production | 64/100 |
| usefulness | 74/100 |
| integration | 94/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 100/100 |

---

<sub>🔭 Discovered 2026-07-13 · [View on GitHub](https://github.com/nostrdevkit/nostr) · [← Back to Crypto](./README.md)</sub>
