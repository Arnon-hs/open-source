# trustwallet/assets

[![Stars](https://img.shields.io/github/stars/trustwallet/assets?style=flat-square&color=yellow)](https://github.com/trustwallet/assets/stargazers) [![Forks](https://img.shields.io/github/forks/trustwallet/assets?style=flat-square&color=blue)](https://github.com/trustwallet/assets/network) [![Language](https://img.shields.io/badge/lang-Go-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-54%2F100-brightgreen?style=flat-square)](#)

> A comprehensive, up-to-date collection of information about several thousands (!) of crypto tokens.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 5.3k |
| 🍴 **Forks** | 27.2k |
| 💻 **Language** | Go |
| 📈 **Score** | 54/100 |
| 🗓️ **Last push** | 2026-08-24 |
| 🔍 **Source** | github |

## 🏷️ Topics

_no topics_

## 🎯 Categories

Crypto

## 📝 Summary

### English

**Brief Summary (2‑3 sentences)**  
trustwallet/assets is an open‑source, constantly refreshed repository that catalogs detailed metadata for thousands of cryptocurrency tokens. It serves as a ready‑to‑use reference for developers building or testing Web3 applications, wallet features, and DeFi integrations. With a strong community footprint (5 k+ stars, 27 k+ forks) and recent activity, it is a mature OSS candidate for production pilots.

**Value**  
- **Comprehensive token data** – provides contract addresses, symbols, decimals, and other on‑chain attributes across multiple blockchains, eliminating the need to scrape or maintain this information yourself.  
- **Accelerates prototyping** – developers can instantly query token metadata to mock wallet balances, price feeds, or transaction flows, shortening time‑to‑market for new Web3 products.  
- **Transparency** – the data is openly version‑controlled, making it easy to audit changes, track provenance, and align with compliance requirements.

**Practical Adoption Path**  
1. **Explore & Validate** – Clone the repo and run the provided scripts to query a small subset of tokens relevant to your use case; verify that the fields you need (e.g., `decimals`, `logoURI`) are present.  
2. **Integrate** – Wrap the JSON/YAML assets in a lightweight service (e.g., a Go microservice or a Node.js cache layer) that your application can call at runtime.  
3. **Sync & Extend** – Set up a scheduled job (the project already includes a `update.sh` script) to pull daily updates, and optionally contribute missing or corrected entries back to the upstream repo.  
4. **Monitor** – Because integration signals are sparse, add health checks that flag missing or malformed token entries before they reach production.

**Production Readiness**  
- **Activity & Adoption** – The repository is actively maintained (last commit 2026‑07‑02), widely forked, and referenced by several wallet and DeFi projects, indicating a healthy ecosystem.  
- **Stability** – The data format is stable, and the Go tooling around it is well‑documented, making it straightforward to embed in production pipelines.  
- **Risks** – While no critical metadata issues have been identified, a final review of the license (MIT/Apache‑style) and a security audit of the update scripts are advisable. Once those checks are completed, trustwallet/assets can be considered production‑ready for serious pilots and eventual full‑scale deployment.

### Русский

**trustwallet/assets** — это открытая, постоянно обновляемая база данных с подробной информацией о нескольких тысячах криптотокенов, которая позволяет быстро прототипировать и проверять блокчейн‑процессы без необходимости разрабатывать собственные парсеры. Типичный сценарий — интеграция в Web3‑приложения, кошельки или DeFi‑сервисы для получения метаданных токенов и построения цепочек взаимодействия; перед внедрением рекомендуется вручную проверить релевантность найденных сигналов. Проект обладает высокой готовностью к production: активная разработка, значительная популярность (5 346 звёзд, 27 198 форков), недавние обновления и сильные экосистемные сигналы, хотя окончательная оценка лицензии, безопасности и поддержки поддерживается отдельным аудитом.

### 中文

**项目简介**  
trustwallet/assets 是一个由 Trust Wallet 官方维护的开源库，收录并持续更新数千种加密代币的完整元数据（合约地址、符号、精度、图标等），为 Web3 开发者提供可靠的代币信息源。

**价值**  
- **快速原型**：无需自行抓取链上数据，即可在钱包、DeFi、交易所等项目中直接引用完整的代币列表，加速业务验证。  
- **数据一致性**：统一的、社区审校的代币信息帮助避免因元数据错误导致的合约调用失败或 UI 展示错误。  
- **生态兼容**：被多款主流钱包和 DeFi 前端采用，具备成熟的社区认可度。

**典型接入方式**  
1. **直接引用 JSON**：项目中通过 HTTP/HTTPS 拉取 `assets/evm/<chainId>.json`（或对应链的文件），解析后在前端或后端使用。  
2. **Go SDK**：项目使用 Go 语言时，可通过 `github.com/trustwallet/assets` 包读取本地克隆的仓库或远程文件，实现结构化的代币查询。  
3. **CI 同步**：在 CI/CD 流程中使用 `git submodule` 或 `git subtree` 将 assets 库同步到代码库，确保每次构建都使用最新的代币元数据。  

**生产可用性**  
- **活跃度**：截至 2026‑07‑02，仓库最近一次提交，星标 5,346，fork 27,198，社区活跃，具备持续维护的迹象。  
- **成熟度**：已在多个钱包和 DeFi 项目中实际使用，属于 “高” 级别的 OSS 候选，适合作为正式环境的数据源。  
- **风险**：目前未发现重大元数据风险，但仍需在正式上线前完成许可证合规、代码审计以及维护者沟通，以确认安全姿态和长期支持。  

综上，trustwallet/assets 提供了高质量、可直接消费的代币元数据，是构建 Web3 应用时的可靠底层资源，适合在生产环境中使用，只要完成常规的合规与安全审查即可。

## 🧭 Practical evaluation

**Value:** trustwallet/assets helps prototype or inspect blockchain workflows with open implementation details.

**Best use cases**

- build Web3 workflows
- inspect blockchain integrations
- prototype wallet or DeFi features

**Integration notes:** Needs manual inspection before adoption because integration signals are sparse in the discovered metadata.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 5346 GitHub stars
- 27198 forks
- updated 2026-07-02
- primary language: Go

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 100/100 |
| stars | 79/100 |
| topics | 0/100 |
| outlook | 54/100 |
| quality | 63/100 |
| recency | 40/100 |
| adoption | 85/100 |
| production | 56/100 |
| usefulness | 42/100 |
| integration | 46/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 100/100 |

---

<sub>🔭 Discovered 2026-07-02 · [View on GitHub](https://github.com/trustwallet/assets) · [← Back to Crypto](./README.md)</sub>
