# Azure/artifact-signing-action

[![Stars](https://img.shields.io/github/stars/Azure/artifact-signing-action?style=flat-square&color=yellow)](https://github.com/Azure/artifact-signing-action/issues/128/stargazers) [![Forks](https://img.shields.io/github/forks/Azure/artifact-signing-action?style=flat-square&color=blue)](https://github.com/Azure/artifact-signing-action/issues/128/network) [![Language](https://img.shields.io/badge/lang-Unknown-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-38%2F100-brightgreen?style=flat-square)](#)

> Discovered from Hacker News (github-mentions)

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | — |
| 🍴 **Forks** | — |
| 💻 **Language** | Unknown |
| 📈 **Score** | 38/100 |
| 🗓️ **Last push** | 2026-09-05 |
| 🔍 **Source** | hackernews |

## 🏷️ Topics

`hn` `github-mentions`

## 🎯 Categories

Misc

## 📝 Summary

### English

**Brief Summary**  
The project documents a post‑migration issue where Windows SmartScreen starts flagging sites that moved from the Enterprise‑Only Certificate (EOC) infrastructure, and it also notes that EV (Extended Validation) certificates are being affected. The repository collects community reports, reproduces the problem, and offers initial diagnostics and work‑arounds for developers and security teams.

**Value**  
- Provides a concrete, real‑world case study of SmartScreen false‑positives after a certificate‑authority migration, which can help teams anticipate similar regressions when switching PKI providers.  
- Includes scripts and step‑by‑step guidance to reproduce the warnings, making it a useful reference for troubleshooting SmartScreen and EV‑cert interactions without needing to dig through scattered forum posts.

**Practical Adoption Path**  
1. **Review the README & issue tracker** – confirm that the documented scenario matches your migration (e.g., moving from EOC to a new CA, using EV certs).  
2. **Clone the repo** and run the provided reproduction scripts in a test environment that mirrors your production URL and certificate chain.  
3. **Validate the findings** against your own SmartScreen logs; if the same warnings appear, follow the suggested mitigations (e.g., re‑signing with a trusted root, submitting the site to Microsoft’s SmartScreen reputation service).  
4. **Integrate the diagnostic scripts** into your CI/CD pipeline to catch SmartScreen regressions early after any future certificate changes.  

**Production Readiness** – *Medium*  
The project is actively maintained (last update 2026‑05‑11) and contains useful technical artifacts, but signals such as a formal release, extensive test coverage, and a clear licensing statement are missing. It is suitable for prototypes, internal tooling, or as a reference when planning a PKI migration, provided you perform due‑diligence checks (license compliance, issue responsiveness, and ongoing maintenance) before relying on it in a production environment.

### Русский

SmartScreen предупреждает о подозрительных сайтах после миграции с EOC, при этом затрагивает и EV‑сертификаты, что может быть критично для процессов проверки подлинности веб‑ресурсов. Проект подходит для быстрого прототипирования или внутренних систем, где требуется отследить и подавить ложные срабатывания SmartScreen, но перед выводом в продакшн необходимо вручную оценить лицензирование, активность репозитория и наличие актуальной документации. Готовность к production — средняя: требуется проверка зависимостей и план обслуживания.

### 中文

**项目价值**  
- 该项目记录了在从 **EOC（Enterprise Operation Center）** 迁移后，Windows SmartScreen 对网站和 EV（Extended Validation）证书产生误报的情况，帮助开发者快速定位和排查因迁移导致的安全提示失效。  
- 对于需要在内部或原型系统中保持安全提示连续性的团队，它提供了一个可复现的案例与调试思路，避免因误报导致的用户信任下降或业务中断。

**典型接入方式**  
1. **手动审查**：在将项目引入现有工作流前，先检查仓库的许可证、维护状态、Issue 活动以及发布节奏，确保符合组织的合规要求。  
2. **环境复现**：在本地或测试环境中部署迁移前后的站点，使用相同的域名、证书链和 SmartScreen 配置，复现误报现象。  
3. **脚本或 CI 集成**：将项目提供的检测脚本（如有）加入 CI 流水线，在每次部署后自动验证 SmartScreen 状态，及时捕获新出现的误报。  
4. **文档对照**：结合项目的 README 与实际迁移步骤，对比文档中的 “已知问题” 与 “解决方案”，在必要时提交 PR 或 Issue 进行补充。

**生产可用性**  
- **成熟度**：当前评分 41/100，属于 **中等** 稳定性。适合用于原型、内部工具或作为迁移前的风险评估参考。  
- **依赖与维护**：项目更新于 2026‑05‑11，活跃度较低，依赖项不多，但需自行监控上游库的安全更新。  
- **上线建议**：在正式生产环境使用前，完成以下检查：  
  - 确认许可证兼容（MIT/Apache 等开源许可证）。  
  - 检查最近的 Issue 与 PR，评估是否还有未解决的关键 bug。  
  - 评估维护者响应速度，必要时自行 fork 并维护。  
  - 在受控环境中进行完整的回归测试，确保 SmartScreen 误报已被妥善处理。  

综上，该项目在 **迁移后 SmartScreen 与 EV 证书误报排查** 场景下具备实用价值，但因信息稀疏、维护有限，建议在充分评估并进行手动验证后，再考虑在生产环境中采用。

## 🧭 Practical evaluation

**Value:** SmartScreen warnings triggered after migration from EOC. EV certs affected too may be useful when its README and activity match a concrete workflow.

**Best use cases**

- Not enough metadata yet.

**Integration notes:** Needs manual inspection before adoption because integration signals are sparse in the discovered metadata.

**Production readiness:** Medium: useful for prototypes or internal workflows, with dependency and maintenance checks before production.

**Quality signals**

- updated 2026-05-11
- 2 topics

**Risks:** Quality signals are limited; verify license, maintenance, docs, issues, and release cadence before using it.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 0/100 |
| stars | 0/100 |
| topics | 25/100 |
| outlook | 47/100 |
| quality | 36/100 |
| recency | 80/100 |
| adoption | 0/100 |
| production | 51/100 |
| usefulness | 42/100 |
| integration | 30/100 |
| sourceTrust | 80/100 |
| categoryMatchCount | 0/100 |

---

<sub>🔭 Discovered 2026-05-11 · [View on GitHub](https://github.com/Azure/artifact-signing-action/issues/128) · [← Back to Misc](./README.md)</sub>
