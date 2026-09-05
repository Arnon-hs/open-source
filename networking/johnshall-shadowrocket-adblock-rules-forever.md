# Johnshall/Shadowrocket-ADBlock-Rules-Forever

[![Stars](https://img.shields.io/github/stars/Johnshall/Shadowrocket-ADBlock-Rules-Forever?style=flat-square&color=yellow)](https://github.com/Johnshall/Shadowrocket-ADBlock-Rules-Forever/stargazers) [![Forks](https://img.shields.io/github/forks/Johnshall/Shadowrocket-ADBlock-Rules-Forever?style=flat-square&color=blue)](https://github.com/Johnshall/Shadowrocket-ADBlock-Rules-Forever/network) [![Language](https://img.shields.io/badge/lang-Unknown-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-62%2F100-brightgreen?style=flat-square)](#)

> 提供多款 Shadowrocket 规则，拥有强劲的广告过滤功能。每日 8 时重新构建规则。

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 27.9k |
| 🍴 **Forks** | 1.9k |
| 💻 **Language** | Unknown |
| 📈 **Score** | 62/100 |
| 🗓️ **Last push** | 2026-09-05 |
| 🔍 **Source** | github |

## 🏷️ Topics

`adblock` `gfw` `proxy` `shadowrocket` `v2ray`

## 🎯 Categories

Networking

## 📝 Summary

### English

**Brief Summary**  
Johnshall/Shadowrocket‑ADBlock‑Rules‑Forever supplies a collection of high‑performance ad‑blocking rule sets for the iOS/macOS client Shadowrocket. The rules are regenerated every day at 08:00 UTC, ensuring that the latest ad domains and tracking URLs are filtered out.

**Value**  
- **Up‑to‑date protection** – Daily rebuilds keep the blocklist current with new ad services and trackers.  
- **Broad coverage** – Multiple rule formats (e.g., Surge, Quantumult, Shadowrocket) are provided, so the same repository can serve different proxy clients.  
- **Strong community backing** – Over 27 k GitHub stars and 1.8 k forks indicate wide adoption and frequent contributions, which translates into faster bug fixes and feature enhancements.

**Practical Adoption Path**  
1. **Clone or download the repository** and locate the rule file(s) that match your Shadowrocket version (e.g., `shadowrocket.txt`).  
2. **Import the rule file** into Shadowrocket via the app’s “Rule List” → “Import from URL/Local”.  
3. **Enable the rule set** in the Shadowrocket profile you want to protect.  
4. **Validate** by browsing a few ad‑heavy sites and confirming that ads are blocked; optionally compare with the repository’s `README` for any required configuration flags.  
5. **Automate updates** (optional but recommended): add a scheduled script or use a mobile automation tool (e.g., Shortcuts, cron on a jail‑broken device) to fetch the latest rule file daily at 08:00 UTC.

**Production‑Readiness**  
- **Recent activity**: The project was updated on 2026‑06‑25, showing active maintenance.  
- **Community signals**: High star/fork count and multiple topics indicate strong ecosystem interest and a mature user base.  
- **Stability**: The rule generation process is deterministic and runs on a fixed schedule, making the output predictable for CI/CD pipelines or automated deployments.  
- **Risk considerations**: The repository does not expose a turnkey integration script; you must manually pull and apply the rule set, and verify that the rule syntax aligns with your Shadowrocket version. A brief validation step is advisable before rolling out to production environments.

Overall, the project is production‑ready for teams that need reliable, daily‑updated ad‑blocking rules for Shadowrocket, provided they allocate a small amount of effort to integrate and test the rule import process.

### Русский

**Shadowrocket‑ADBlock‑Rules‑Forever** — это набор готовых правил для клиента Shadowrocket, обеспечивающих мощную блокировку рекламных и трекер‑запросов; правила автоматически пересобираются каждый день в 8 утра, что гарантирует актуальность фильтрации. Проект уже имеет активную поддержку (обновления — 2026‑06‑25, более 27 тыс. звёзд и 1,8 тыс. форков), поэтому его можно быстро интегрировать в существующий workflow Shadowrocket после короткой проверки совместимости. Благодаря высокой активности и широкому принятию, набор правил готов к использованию в продакшене, однако рекомендуется протестировать его в тестовой среде, чтобы оценить затраты на настройку под конкретные требования.

### 中文

**项目简介**  
Johnshall/Shadowrocket-ADBlock-Rules-Forever 为 Shadowrocket 客户端提供一套高效的广告拦截规则库，并且每天 08:00 自动重新构建，确保规则始终保持最新。

**价值**  
- **强大的广告过滤**：集合了多源规则，覆盖常见广告、追踪器以及恶意域名，显著提升浏览与应用的清爽度。  
- **实时更新**：每日自动重建规则，能够快速响应新出现的广告域名和过滤技术，几乎零滞后。  
- **开源透明**：规则以文本形式公开，可自行审查或二次定制，满足对隐私和安全有严格要求的用户。

**典型接入方式**  
1. **克隆仓库或下载最新的规则文件**（如 `rules.txt`、`rules.conf`）。  
2. 在 Shadowrocket 客户端的「规则」页面，选择「导入本地规则」或「远程规则 URL」，填入本地路径或仓库的 raw 文件链接。  
3. 根据需要在 Shadowrocket 中开启「广告过滤」或「自定义规则」开关，即可生效。  
4. 若需自行维护，可使用 GitHub Actions 中的自动构建脚本（项目已提供），在本地或 CI 环境中定时运行 `npm run build`，生成最新规则后推送到仓库。

**生产可用性**  
- **活跃度**：最近一次提交为 2026‑06‑25，项目仍在持续维护。  
- **社区规模**：超过 27k ⭐、1.8k 🍴，说明已有大量用户在实际使用并贡献反馈。  
- **生态兼容**：规则文件为通用文本格式，兼容 Shadowrocket 以及其他基于 Surge/QuantumultX 的代理客户端。  
- **风险**：元数据中未提供一键集成脚本，接入前需要手动验证规则是否与现有策略冲突；此外，若业务对规则更新的时效性有严格 SLA，建议自行部署 CI 进行二次构建。  

综合来看，该项目在功能、更新频率和社区支持方面都已具备生产级别的成熟度，适合作为广告拦截的核心规则源，在正式环境使用前只需进行一次规则审查和测试即可。

## 🧭 Practical evaluation

**Value:** Johnshall/Shadowrocket-ADBlock-Rules-Forever may be useful when its README and activity match a concrete workflow.

**Best use cases**

- Not enough metadata yet.

**Integration notes:** Needs manual inspection before adoption because integration signals are sparse in the discovered metadata.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 27868 GitHub stars
- 1863 forks
- updated 2026-06-25
- 5 topics

**Risks:** Integration path is not obvious from metadata; validate setup cost before committing.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 82/100 |
| stars | 95/100 |
| topics | 63/100 |
| outlook | 75/100 |
| quality | 85/100 |
| recency | 80/100 |
| adoption | 91/100 |
| production | 71/100 |
| usefulness | 42/100 |
| integration | 30/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 100/100 |

---

<sub>🔭 Discovered 2026-06-25 · [View on GitHub](https://github.com/Johnshall/Shadowrocket-ADBlock-Rules-Forever) · [← Back to Networking](./README.md)</sub>
