# MetaMask/eth-phishing-detect

[![Stars](https://img.shields.io/github/stars/MetaMask/eth-phishing-detect?style=flat-square&color=yellow)](https://github.com/MetaMask/eth-phishing-detect/stargazers) [![Forks](https://img.shields.io/github/forks/MetaMask/eth-phishing-detect?style=flat-square&color=blue)](https://github.com/MetaMask/eth-phishing-detect/network) [![Language](https://img.shields.io/badge/lang-TypeScript-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-57%2F100-brightgreen?style=flat-square)](#)

> Utility for detecting phishing domains targeting Web3 users

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 1.3k |
| 🍴 **Forks** | 1.1k |
| 💻 **Language** | TypeScript |
| 📈 **Score** | 57/100 |
| 🗓️ **Last push** | 2026-09-05 |
| 🔍 **Source** | github |

## 🏷️ Topics

_no topics_

## 🎯 Categories

Crypto

## 📝 Summary

### English

**Brief Summary (2‑3 sentences)**  
MetaMask’s eth‑phishing‑detect is an open‑source TypeScript library that flags known phishing domains targeting Web3 users, helping developers safeguard wallet and DeFi integrations. With over 1 200 GitHub stars and recent updates, it offers a ready‑to‑use detection list and utility functions for rapid prototyping of secure blockchain workflows.  

**Value**  
- **Security baseline:** Provides a curated, community‑maintained list of malicious domains and a simple API to check URLs, reducing the risk of phishing attacks in dApps, wallets, and DeFi front‑ends.  
- **Speed to market:** By plugging the library into existing TypeScript/JavaScript codebases, teams can add phishing protection without building their own threat intelligence pipeline.  
- **Transparency:** Open implementation and data sources let auditors verify detection logic and adapt the list to specific threat models.

**Practical Adoption Path**  
1. **Prototype:** Import the package, run the built‑in `detect` function on user‑entered URLs, and observe false‑positive/negative rates in a sandbox environment.  
2. **Manual review:** Because detection signals are sparse, supplement the library with a secondary verification step (e.g., domain reputation API or manual whitelist/blacklist).  
3. **Integration:** Wrap the check in a middleware layer for wallet connections, transaction signing, or DeFi UI components; add logging and alerting for any flagged domains.  
4. **Governance:** Periodically sync the upstream phishing list, contribute any missed domains, and monitor the repository for security patches.

**Production Readiness**  
- **Readiness level:** Medium. The library is mature enough for internal tools and prototype‑level products, but production deployments should include additional safeguards (rate‑limiting, fallback checks) and a formal security review.  
- **Dependencies & maintenance:** The project is actively maintained (last commit 2026‑06‑23) and has a healthy fork/star count, yet a final audit of licensing, vulnerability disclosures, and maintainer activity is recommended before wide‑scale rollout.  
- **Risk mitigation:** Implement a layered defense (library + secondary threat intel) and establish a process for updating the phishing list to keep pace with emerging attacks.

### Русский

**MetaMask/eth‑phishing‑detect** — это открытый TypeScript‑инструмент, автоматически выявляющий фишинговые домены, нацеленные на Web3‑пользователей, что позволяет быстро прототипировать и проверять безопасные блокчейн‑воркфлоу (кошельки, DeFi‑интеграции). Его типичное применение — интеграция в процесс разработки или внутренний аудит, где результаты требуют ручного подтверждения из‑за ограниченной полноты метаданных. Проект имеет умеренную готовность к production: достаточную популярность (≈1,3 к звёзд, 1 к форков) и актуальное обновление, но перед выпуском в продакшн рекомендуется проверить лицензию, безопасность зависимостей и наличие активных мейнтейнеров.

### 中文

**项目简介**  
MetaMask/eth‑phishing‑detect 是一套基于 TypeScript 的开源工具，用于检测针对 Web3 用户的钓鱼域名。它通过分析以太坊相关的元数据（如 ENS、智能合约交互日志等）来识别潜在的恶意站点，帮助开发者在构建钱包、DeFi 前端或其他区块链应用时提前拦截风险。

**价值**  
- **安全防护**：在用户输入或点击链接前实时判别是否为已知或可疑的钓鱼域名，降低资产被盗风险。  
- **快速原型**：提供即插即用的检测库，开发者无需自行实现复杂的威胁情报模型，即可在原型或内部测试环境中验证安全性。  
- **社区可信**：拥有超过 1.2k 星、1k+ Fork，活跃的开源社区持续贡献规则和更新。

**典型接入方式**  
1. **依赖安装**：`npm install @metamask/eth-phishing-detect`。  
2. **加载规则**：在应用启动时调用 `loadPhishingDetection()`，获取最新的钓鱼域名列表（默认从 MetaMask 官方 CDN 拉取）。  
3. **检测调用**：在用户提交 URL、输入 ENS 名称或发起交易前，使用 `detectPhishing(urlOrDomain)` 返回 `true/false` 或更详细的风险报告。  
4. **手动审查**：由于检测信号相对稀疏，建议在检测结果为“可疑”时加入二次人工审核或结合其它威胁情报源。

**生产可用性**  
- **成熟度**：中等（Medium）。代码库活跃，最近一次更新在 2026‑06‑23，适合原型、内部工具或对安全要求不极端的生产环境。  
- **依赖与维护**：需要自行监控库的更新频率、审计其许可证（MIT）以及潜在的安全漏洞。  
- **上线建议**：在正式上线前进行以下步骤：  
  1. 将规则文件镜像到自有 CDN，确保可靠性。  
  2. 实施自动化安全扫描（如 Snyk、OSS‑Review）以捕获潜在依赖漏洞。  
  3. 加入人工复核流程，处理检测结果为 “可疑” 的情况。  

综上，MetaMask/eth‑phishing‑detect 适合作为 Web3 应用的安全加固层，尤其在快速迭代的原型阶段价值突出；在生产环境使用时需做好规则同步、依赖审计和人工复核等补强措施。

## 🧭 Practical evaluation

**Value:** MetaMask/eth-phishing-detect helps prototype or inspect blockchain workflows with open implementation details.

**Best use cases**

- build Web3 workflows
- inspect blockchain integrations
- prototype wallet or DeFi features

**Integration notes:** Needs manual inspection before adoption because integration signals are sparse in the discovered metadata.

**Production readiness:** Medium: useful for prototypes or internal workflows, with dependency and maintenance checks before production.

**Quality signals**

- 1293 GitHub stars
- 1080 forks
- updated 2026-06-23
- primary language: TypeScript

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 76/100 |
| stars | 66/100 |
| topics | 0/100 |
| outlook | 64/100 |
| quality | 66/100 |
| recency | 80/100 |
| adoption | 69/100 |
| production | 67/100 |
| usefulness | 42/100 |
| integration | 46/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 100/100 |

---

<sub>🔭 Discovered 2026-06-23 · [View on GitHub](https://github.com/MetaMask/eth-phishing-detect) · [← Back to Crypto](./README.md)</sub>
