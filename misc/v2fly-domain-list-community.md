# v2fly/domain-list-community

[![Stars](https://img.shields.io/github/stars/v2fly/domain-list-community?style=flat-square&color=yellow)](https://github.com/v2fly/domain-list-community/stargazers) [![Forks](https://img.shields.io/github/forks/v2fly/domain-list-community?style=flat-square&color=blue)](https://github.com/v2fly/domain-list-community/network) [![Language](https://img.shields.io/badge/lang-Go-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-55%2F100-brightgreen?style=flat-square)](#)

> Community managed domain list. Generate geosite.dat for V2Ray.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 9k |
| 🍴 **Forks** | 1.4k |
| 💻 **Language** | Go |
| 📈 **Score** | 55/100 |
| 🗓️ **Last push** | 2026-08-24 |
| 🔍 **Source** | github |

## 🏷️ Topics

`geosite` `v2ray`

## 🎯 Categories

Misc

## 📝 Summary

### English

**Brief Summary (2‑3 sentences)**  
v2fly/domain‑list‑community is a crowd‑sourced repository that maintains a curated list of domain rules used to generate the `geosite.dat` file for V2Ray, a popular proxy platform. The project is actively maintained in Go, with over 8,900 stars and 1,300 forks, making it a reliable source for up‑to‑date geolocation‑based routing rules. Its community‑driven approach ensures the list stays current with emerging domains and regional blocks.

**Value**  
- **Accelerates AI‑enabled networking** – By providing ready‑made, high‑quality domain lists, developers can quickly add AI‑driven routing, RAG, or agent‑based decision logic to V2Ray without building a dataset from scratch.  
- **Reduces operational overhead** – The list is continuously updated by contributors, eliminating the need for manual maintenance of domain blocklists or allowlists.  
- **Broad ecosystem compatibility** – The generated `geosite.dat` is the standard input for V2Ray and many downstream tools, enabling seamless integration into existing proxy, firewall, or AI‑augmented traffic‑analysis pipelines.

**Practical Adoption Path**  
1. **Clone the repository** and run the provided generation script (`make geosite.dat` or the Go CLI) to produce the binary `geosite.dat`.  
2. **Validate** the output against your own policy (e.g., spot‑check critical domains) – the project recommends a brief manual inspection because metadata signals are sparse.  
3. **Deploy** the `geosite.dat` file to your V2Ray configuration (`routing.rules.geoSite`) or feed it into any AI workflow that consumes domain lists (e.g., prompt‑enhanced RAG pipelines).  
4. **Automate updates** by scheduling a CI job that pulls the latest repository, regenerates the file, and redeploys it, ensuring you stay in sync with community changes.

**Production Readiness**  
- **Activity & Adoption** – The repo shows recent commits (last update 2026‑06‑27), a large star count, and many forks, indicating strong community interest and ongoing maintenance.  
- **Stability** – The core generation tool is written in Go, a compiled language with a proven track record for reliability in production environments.  
- **Risk Considerations** – While no major metadata or licensing issues have been identified, a final review of the project’s license (MIT‑style) and its security posture (e.g., dependency scanning) is advisable before large‑scale rollout.  
Overall, v2fly/domain‑list‑community is a mature OSS component suitable for a serious pilot or production deployment, provided the standard due‑diligence steps (license check, security audit, and a brief manual validation) are completed.

### Русский

**v2fly/domain-list-community** — это открытый репозиторий, поддерживаемый сообществом, который собирает и поддерживает актуальный список доменов, а также генерирует файл `geosite.dat` для V2Ray, облегчая внедрение AI‑функций без необходимости создавать собственный набор данных. Типичный сценарий — автоматическое обновление списка запрещённых/разрешённых доменов в прокси‑решениях, интеграция в RAG‑ или агентные рабочие процессы и быстрый прототипинг AI‑сервисов. Проект имеет высокий уровень готовности к production: активные коммиты, более 8 тыс. звёзд, активная пользовательская база и стабильный стек на Go, однако перед развертыванием рекомендуется проверить лицензию, безопасность и наличие поддерживающих мейнтейнеров.

### 中文

**项目简介**  
v2fly/domain-list-community 是由社区维护的域名列表仓库，可直接生成 V2Ray 使用的 `geosite.dat` 文件，帮助用户快速构建基于 V2Ray 的分流与访问控制规则。

**价值**  
- **开箱即用**：无需自行收集、分类域名，项目已提供完整、持续更新的社区域名库。  
- **提升 AI 场景效率**：在需要对网络流量进行语义识别、RAG（检索增强生成）或智能代理的 AI 原型中，直接使用生成的 `geosite.dat` 即可实现精准的域名过滤与路由，省去手动维护的工作量。  
- **社区活跃、质量可靠**：近 9k ⭐、1.3k 🍴、近期频繁更新，具备成熟的生态和广泛的实际使用案例。

**典型接入方式**  
1. **获取最新数据**：`git clone https://github.com/v2fly/domain-list-community.git` 或下载发行版的 `geosite.dat`。  
2. **生成 geosite.dat**（如需自定义）  
   ```bash
   go run ./cmd/convert -i ./list -o ./geosite.dat
   ```  
3. **在 V2Ray 配置中引用**  
   ```json
   {
     "routing": {
       "domainStrategy": "IPIfNonMatch",
       "rules": [
         {
           "type": "field",
           "domain": ["geosite:category-ads"],
           "outboundTag": "blocked"
         }
       ]
     }
   }
   ```  
4. **在 AI 工作流中使用**：将生成的 `geosite.dat` 交给流量监控或代理层，配合模型（如 LLM）进行实时域名分类、策略决策或安全审计。

**生产可用性**  
- **成熟度**：项目活跃度高，最近一次提交在 2026‑06‑27，且已有大量实际部署案例，具备生产级别的可靠性。  
- **风险**：目前未发现重大许可证或安全漏洞，但仍建议在正式上线前进行一次代码审计和依赖安全扫描。  
- **适配性**：基于 Go 实现，易于在容器、K8s 或裸机环境中部署，兼容 V2Ray 主流版本。

综上，v2fly/domain-list-community 是一个高质量、易集成的域名列表解决方案，适合作为 AI 驱动的网络分流、访问控制或安全审计的基础组件，在生产环境中具备足够的稳定性与可维护性。

## 🧭 Practical evaluation

**Value:** v2fly/domain-list-community helps add AI capability without starting from a blank model stack.

**Best use cases**

- prototype AI features
- build RAG or agent workflows
- evaluate model tooling

**Integration notes:** Needs manual inspection before adoption because integration signals are sparse in the discovered metadata.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 8981 GitHub stars
- 1368 forks
- updated 2026-06-27
- primary language: Go
- 2 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 78/100 |
| stars | 84/100 |
| topics | 25/100 |
| outlook | 56/100 |
| quality | 66/100 |
| recency | 40/100 |
| adoption | 83/100 |
| production | 57/100 |
| usefulness | 42/100 |
| integration | 46/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 0/100 |

---

<sub>🔭 Discovered 2026-06-27 · [View on GitHub](https://github.com/v2fly/domain-list-community) · [← Back to Misc](./README.md)</sub>
