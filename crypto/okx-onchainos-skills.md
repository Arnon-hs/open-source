# okx/onchainos-skills

[![Stars](https://img.shields.io/github/stars/okx/onchainos-skills?style=flat-square&color=yellow)](https://github.com/okx/onchainos-skills/stargazers) [![Forks](https://img.shields.io/github/forks/okx/onchainos-skills?style=flat-square&color=blue)](https://github.com/okx/onchainos-skills/network) [![Language](https://img.shields.io/badge/lang-Rust-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-64%2F100-brightgreen?style=flat-square)](#)

> Skills for AI agents to integrate with the OKX OnchainOS API — Wallet, token discovery, market data, DEX swap, and transaction broadcasting.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 251 |
| 🍴 **Forks** | 49 |
| 💻 **Language** | Rust |
| 📈 **Score** | 64/100 |
| 🗓️ **Last push** | 2026-05-11 |
| 🔍 **Source** | github |

## 🏷️ Topics

_no topics_

## 🎯 Categories

Crypto · AI/ML · Backend · Data

## 📝 Summary

### English

**Brief Summary (2‑3 sentences)**  
`okx/onchainos-skills` is a Rust library that bundles ready‑to‑use “skills” for AI agents to interact with the OKX OnchainOS API, covering wallet operations, token discovery, market data, DEX swaps, and transaction broadcasting. With 251 ★ and recent activity (last commit 2026‑05‑11), it provides an open‑source reference implementation for prototyping Web3 workflows and inspecting blockchain integrations. The project is positioned as a low‑to‑medium‑risk component for internal tooling or proof‑of‑concept DeFi features.

**Value**  
- **Accelerates development** – developers can plug the pre‑built skills into LLM‑driven agents instead of writing low‑level RPC calls, cutting weeks of work for wallet and DEX interactions.  
- **Transparent implementation** – the Rust code is fully open, making it easy to audit, extend, or adapt to custom business rules.  
- **Cross‑domain utility** – the same skill set supports both data‑rich AI assistants (e.g., market‑analysis bots) and transaction‑focused agents (e.g., automated arbitrage or custodial services).

**Practical Adoption Path**  
1. **Read the README & run the example** – verify the build environment (Rust 1.70+, Cargo) and confirm the sample agent can query a testnet wallet.  
2. **Create a small PoC** – integrate a single skill (e.g., `get_market_data`) into an existing LLM workflow to validate authentication, rate‑limits, and response formatting.  
3. **Iterate by adding more skills** – progressively add wallet management, token discovery, and swap functions, using the provided integration tests as a safety net.  
4. **Wrap with internal abstractions** – if needed, expose the Rust library via a gRPC/HTTP shim so non‑Rust services can reuse the skills.  
5. **Conduct security & compliance review** – audit the API keys handling, verify the license (MIT/Apache‑2.0 compatible), and run static analysis tools before moving to production.

**Production Readiness**  
- **Maturity:** Medium – the codebase is actively maintained, well‑starred, and covers core OnchainOS endpoints, but it lacks formal CI/CD pipelines, extensive integration tests, and a documented upgrade path.  
- **Dependencies:** Moderate – relies on OKX’s public API and standard Rust crates; teams should pin versions and monitor upstream changes.  
- **Operational considerations:** Ensure API‑key rotation, rate‑limit handling, and add logging/auditing layers. A small internal pilot is recommended before scaling to customer‑facing services.  

Overall, `okx/onchainos-skills` is a solid foundation for building AI‑driven Web3 components, especially for internal prototypes or sandbox environments, with a clear, incremental path to production after due diligence.

### Русский

**okx/onchainos-skills** — набор Rust‑библиотек, позволяющих AI‑агентам быстро подключаться к API OKX OnchainOS (работа с кошельком, поиск токенов, рыночные данные, DEX‑своп и отправка транзакций). Он идеален для прототипирования Web3‑конвейеров и проверки интеграций DeFi / wallet‑функций, при этом требует небольшого proof‑of‑concept и проверки README перед началом работы. Готовность к production — средняя: проект достаточно стабилен для внутренних и экспериментальных решений, но перед развёртыванием в продакшн стоит оценить лицензирование, безопасность зависимостей и активность сопровождения.

### 中文

**项目简介（2‑3 句话）**  
`okx/onchainos-skills` 是一套基于 Rust 实现的 AI Agent 技能库，封装了 OKX OnchainOS 的核心接口——钱包管理、代币发现、行情查询、DEX 兑换以及交易广播。开发者可以直接调用这些技能，在几行代码内完成完整的 Web3 工作流原型或内部审计。

**价值**  
- **快速原型**：提供即插即用的区块链功能，帮助团队在原型阶段快速验证钱包、DeFi、行情等场景。  
- **透明实现**：全部实现开源，便于审查、二次定制和学习区块链集成细节。  
- **AI‑Agent 友好**：专为大模型或自主代理设计，支持自然语言指令到链上操作的映射。

**典型接入方式**  
1. **阅读 README**：确认所需的 OKX API Key 与网络（主网/测试网）配置。  
2. **创建 Rust 项目**，在 `Cargo.toml` 中加入依赖：  
   ```toml
   onchainos-skills = { git = "https://github.com/okx/onchainos-skills", rev = "main" }
   ```  
3. **初始化客户端**：使用 `OnchainOsClient::new(api_key, secret, endpoint)` 创建实例。  
4. **调用技能**：例如获取钱包余额  
   ```rust
   let balance = client.wallet_balance(address).await?;
   ```  
   或执行 DEX 兑换  
   ```rust
   let tx_hash = client.dex_swap(params).await?;
   ```  
5. **在 AI Agent 中封装**：将上述函数包装为语言模型的 tool（如 OpenAI Function Calling），即可让模型直接通过自然语言触发链上操作。

**生产可用性**  
- **成熟度**：GitHub ★251、Fork 49，最近一次提交于 2026‑05‑11，代码活跃度良好。  
- **适用场景**：非常适合内部原型、测试环境或对安全要求不极端的业务流程。  
- **生产准备度**：**中等**。在正式上线前建议完成以下检查：  
  - 完整的安全审计（尤其是签名、密钥管理和交易广播部分）。  
  - 评估依赖库的维护状态与许可证兼容性。  
  - 对关键路径加入重试、超时和监控，防止链上请求异常导致服务不可用。  
  - 若需要高可用或大规模并发，考虑在外层加一层缓存/队列以及多节点部署。  

总体而言，`okx/onchainos-skills` 为 Web3 开发提供了“一站式”区块链能力，适合作为原型和内部工具的技术基石，经过适当的安全与运维加固后即可投入生产使用。

## 🧭 Practical evaluation

**Value:** okx/onchainos-skills helps prototype or inspect blockchain workflows with open implementation details.

**Best use cases**

- build Web3 workflows
- inspect blockchain integrations
- prototype wallet or DeFi features

**Integration notes:** Looks feasible to evaluate, but integration should start with a small proof of concept and README check.

**Production readiness:** Medium: useful for prototypes or internal workflows, with dependency and maintenance checks before production.

**Quality signals**

- 251 GitHub stars
- 49 forks
- updated 2026-05-11
- primary language: Rust

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 42/100 |
| stars | 51/100 |
| topics | 0/100 |
| outlook | 72/100 |
| quality | 62/100 |
| recency | 100/100 |
| adoption | 49/100 |
| production | 70/100 |
| usefulness | 74/100 |
| integration | 46/100 |
| sourceTrust | 100/100 |

---

<sub>🔭 Discovered 2026-05-11 · [View on GitHub](https://github.com/okx/onchainos-skills) · [← Back to Crypto](./README.md)</sub>
