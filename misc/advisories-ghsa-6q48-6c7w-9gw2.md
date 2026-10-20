# advisories/GHSA-6q48-6c7w-9gw2

[![Stars](https://img.shields.io/github/stars/advisories/GHSA-6q48-6c7w-9gw2?style=flat-square&color=yellow)](https://github.com/advisories/GHSA-6q48-6c7w-9gw2/stargazers) [![Forks](https://img.shields.io/github/forks/advisories/GHSA-6q48-6c7w-9gw2?style=flat-square&color=blue)](https://github.com/advisories/GHSA-6q48-6c7w-9gw2/network) [![Language](https://img.shields.io/badge/lang-Unknown-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-41%2F100-brightgreen?style=flat-square)](#)

> Discovered from Hacker News (github-mentions)

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | — |
| 🍴 **Forks** | — |
| 💻 **Language** | Unknown |
| 📈 **Score** | 41/100 |
| 🗓️ **Last push** | 2026-10-20 |
| 🔍 **Source** | hackernews |

## 🏷️ Topics

`hn` `github-mentions`

## 🎯 Categories

Misc

## 📝 Summary

### English

Certifi bundles emSign root CAs but includes compromised intermediate keys, making it suitable only for prototypes and internal workflows. Adopt it by first verifying compatibility with your systems, updating dependencies, and integrating into a test environment. For production use, conduct a thorough security audit and maintain regular update checks.

### Русский

Certifi объединяет корневые сертификаты emSign, но содержит уязвимые промежуточные ключи, что делает его пригодным только для прототипов и внутренних процессов. Для внедрения сначала проверьте совместимость с вашими системами и обновите зависимости, а затем интегрируйте в тестовую среду. При продакшене требуется тщательный аудит безопасности и регулярные проверки обновлений.

### 中文

Certifi 将 emSign 根证书打包，但包含已泄露的中间密钥，仅适用于原型和内部流程。采用时先验证与系统的兼容性，更新依赖并集成到测试环境。生产环境需进行彻底的安全审计并保持定期更新检查。

## 🧭 Practical evaluation

**Value:** Certifi bundles emSign root CAs with compromised intermediate CA keys may be useful when its README and activity match a concrete workflow.

**Best use cases**

- Not enough metadata yet.

**Integration notes:** Needs manual inspection before adoption because integration signals are sparse in the discovered metadata.

**Production readiness:** Medium: useful for prototypes or internal workflows, with dependency and maintenance checks before production.

**Quality signals**

- updated 2026-10-20
- 2 topics

**Risks:** Quality signals are limited; verify license, maintenance, docs, issues, and release cadence before using it.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 0/100 |
| stars | 0/100 |
| topics | 25/100 |
| outlook | 54/100 |
| quality | 41/100 |
| recency | 100/100 |
| adoption | 0/100 |
| production | 58/100 |
| usefulness | 42/100 |
| integration | 30/100 |
| sourceTrust | 80/100 |
| categoryMatchCount | 0/100 |

---

<sub>🔭 Discovered 2026-10-20 · [View on GitHub](https://github.com/advisories/GHSA-6q48-6c7w-9gw2) · [← Back to Misc](./README.md)</sub>
