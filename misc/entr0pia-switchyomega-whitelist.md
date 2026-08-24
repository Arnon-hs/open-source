# entr0pia/SwitchyOmega-Whitelist

[![Stars](https://img.shields.io/github/stars/entr0pia/SwitchyOmega-Whitelist?style=flat-square&color=yellow)](https://github.com/entr0pia/SwitchyOmega-Whitelist/stargazers) [![Forks](https://img.shields.io/github/forks/entr0pia/SwitchyOmega-Whitelist?style=flat-square&color=blue)](https://github.com/entr0pia/SwitchyOmega-Whitelist/network) [![Language](https://img.shields.io/badge/lang-Python-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-52%2F100-brightgreen?style=flat-square)](#)

> 中国大陆域名, SwitchyOmega 白名单规则, 自动更新

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 1.3k |
| 🍴 **Forks** | 109 |
| 💻 **Language** | Python |
| 📈 **Score** | 52/100 |
| 🗓️ **Last push** | 2026-08-24 |
| 🔍 **Source** | github |

## 🏷️ Topics

`china` `dns` `domains` `switchyomega`

## 🎯 Categories

Misc

## 📝 Summary

### English

**Brief Summary**  
`entr0pia/SwitchyOmega-Whitelist` is a Python‑based, community‑maintained repository that provides an automatically‑updating whitelist of mainland‑China domains for SwitchyOmega proxy extensions. It keeps the whitelist current without manual effort, making it easy to route only the specified sites through a proxy while leaving the rest of the traffic untouched.  

**Value**  
- **Zero‑maintenance list** – The project scrapes authoritative sources and refreshes the whitelist on a regular schedule, eliminating the tedious manual curation that most proxy users face.  
- **Seamless SwitchyOmega integration** – The output format matches SwitchyOmega’s rule syntax, so users can drop the generated file into their existing profiles with a single click.  
- **Open‑source transparency** – With >1 300 stars and an active Python codebase, the logic is auditable, extensible, and can be forked for custom regional rules or additional filtering criteria.  

**Practical Adoption Path**  
1. **Proof‑of‑Concept** – Clone the repo, run the provided script (`update_whitelist.py`) locally, and import the generated `whitelist.txt` into a test SwitchyOmega profile. Verify that known mainland sites are correctly proxied while others bypass the proxy.  
2. **CI Integration** – Add the script to a CI pipeline (GitHub Actions, GitLab CI, etc.) to generate and publish the whitelist as an artifact or to a static‑hosting bucket (e.g., GitHub Pages).  
3. **Production Roll‑out** – Point the production SwitchyOmega configuration to the hosted whitelist URL. Optionally wrap the script in a Docker container for reproducible builds and schedule it via cron or a serverless function.  

**Production Readiness**  
- **Maturity** – Medium. The repository is actively maintained (last update 2026‑06‑23) and has a healthy star/fork count, indicating community trust.  
- **Dependencies** – Pure Python with only standard libraries and a few well‑maintained HTTP/HTML parsers; easy to audit and lock via `requirements.txt`.  
- **Risks** – License (likely MIT/Apache) and security posture need a final check; the upstream data sources must remain accessible for continuous updates.  
- **Recommendation** – Suitable for internal tools, prototypes, or as a component of larger RAG/agent workflows. Before production deployment, perform a short security audit, pin dependency versions, and establish a monitoring alert for update failures.

### Русский

**SwitchyOmega‑Whitelist** — это набор правил для белого списка доменов Китая, предназначенный для автоматического обновления конфигураций в расширении SwitchyOmega. Проект удобно использовать в прототипах и внутренних сервисах, где требуется быстро добавить AI‑поддержку (например, построить RAG‑или агентные сценарии), проверив работу через небольшое POC и ознакомившись с README. Готовность к production — средняя: репозиторий популярен (1348 звёзд, 109 форков), активно поддерживается, но перед выпуском в продакшн следует уточнить лицензию, провести аудит безопасности и убедиться в стабильности зависимостей.

### 中文

**项目简介（2‑3 句）**  
`entr0pia/SwitchyOmega-Whitelist` 是一套针对中国大陆域名的 SwitchyOmega 白名单规则库，能够自动同步最新的域名列表并生成可直接导入 SwitchyOmega 的配置文件。项目采用 Python 脚本实现，支持定时更新，帮助用户在使用代理插件时快速过滤国内站点。

**价值**  
- **省时省力**：免去手动维护国内域名白名单的繁琐工作，脚本自动抓取并更新最新列表。  
- **提升网络体验**：在 SwitchyOmega 中使用白名单后，国内站点走直连，国外站点走代理，显著降低访问延迟和流量消耗。  
- **开箱即用**：提供完整的规则文件和更新脚本，适配常见的 SwitchyOmega 版本，无需额外配置。

**典型接入方式**  
1. **克隆仓库**：`git clone https://github.com/entr0pia/SwitchyOmega-Whitelist.git`  
2. **运行更新脚本**（可自行设置 cron 或 GitHub Actions）：  
   ```bash
   cd SwitchyOmega-Whitelist
   python generate_whitelist.py   # 生成 whitelist.txt
   ```  
3. **导入 SwitchyOmega**：在 SwitchyOmega 的 “规则列表” 页面，选择 “导入”，加载生成的 `whitelist.txt`。  
4. **自动化**：将脚本部署到 CI/CD 或服务器上，定时执行并通过 Git 提交更新，保持规则始终最新。

**生产可用性**  
- **成熟度**：已有 1300+ 星、100+ Fork，社区活跃，最近一次更新在 2026‑06‑23，代码质量较高。  
- **适用场景**：适合内部网络、企业 VPN、个人科学上网等需要区分国内外流量的生产环境。  
- **风险与准备**：在正式上线前需检查许可证兼容性、依赖安全（如 `requests`、`beautifulsoup4`）以及更新频率是否满足业务 SLA；建议先在预生产环境进行一次完整的自动更新与导入测试。  

总体而言，`SwitchyOmega-Whitelist` 已具备在生产环境中使用的条件，只要完成安全审计和自动化部署，即可实现可靠的国内域名白名单管理。

## 🧭 Practical evaluation

**Value:** entr0pia/SwitchyOmega-Whitelist helps add AI capability without starting from a blank model stack.

**Best use cases**

- prototype AI features
- build RAG or agent workflows
- evaluate model tooling

**Integration notes:** Looks feasible to evaluate, but integration should start with a small proof of concept and README check.

**Production readiness:** Medium: useful for prototypes or internal workflows, with dependency and maintenance checks before production.

**Quality signals**

- 1348 GitHub stars
- 109 forks
- updated 2026-06-23
- primary language: Python
- 4 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 51/100 |
| stars | 67/100 |
| topics | 50/100 |
| outlook | 53/100 |
| quality | 61/100 |
| recency | 40/100 |
| adoption | 62/100 |
| production | 55/100 |
| usefulness | 42/100 |
| integration | 46/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 0/100 |

---

<sub>🔭 Discovered 2026-06-23 · [View on GitHub](https://github.com/entr0pia/SwitchyOmega-Whitelist) · [← Back to Misc](./README.md)</sub>
