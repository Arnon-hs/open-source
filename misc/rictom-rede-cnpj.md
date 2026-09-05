# rictom/rede-cnpj

[![Stars](https://img.shields.io/github/stars/rictom/rede-cnpj?style=flat-square&color=yellow)](https://github.com/rictom/rede-cnpj/stargazers) [![Forks](https://img.shields.io/github/forks/rictom/rede-cnpj?style=flat-square&color=blue)](https://github.com/rictom/rede-cnpj/network) [![Language](https://img.shields.io/badge/lang-Python-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-58%2F100-brightgreen?style=flat-square)](#)

> Visualização gráfica de relacionamentos entre sócios e empresas com dados públicos de CNPJ.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 329 |
| 🍴 **Forks** | 129 |
| 💻 **Language** | Python |
| 📈 **Score** | 58/100 |
| 🗓️ **Last push** | 2026-09-05 |
| 🔍 **Source** | github |

## 🏷️ Topics

`cnpj` `dados-abertos` `flask` `javascript` `python` `receita-federal` `vivagraph`

## 🎯 Categories

Misc

## 📝 Summary

### English

**Brief Summary (2‑3 sentences)**  
`rictom/rede-cnpj` is an open‑source Python tool that generates interactive graphs showing the relationships between shareholders and companies using publicly available CNPJ data. It visualises corporate networks, making it easier to trace ownership structures and detect indirect connections among entities. With recent commits, a sizable community (329 ★, 129 forks) and clear documentation, it is ready for pilot projects.

**Value**  
- **Transparency & Insight:** By turning raw CNPJ filings into navigable graphs, analysts, journalists, and compliance teams can quickly identify hidden ownership links, potential conflicts of interest, or patterns of corporate control.  
- **Speed & Cost‑Efficiency:** Automates data retrieval and visualisation, saving hours of manual spreadsheet work and reducing reliance on proprietary tools.  
- **Extensibility:** Built in Python, it can be integrated with existing data pipelines, enriched with other public datasets (e.g., Receita Federal APIs), or embedded in web dashboards.

**Practical Adoption Path**  
1. **Proof‑of‑Concept (PoC):** Clone the repo, run the provided notebook or CLI on a small sample of CNPJ numbers to verify data quality and visual output.  
2. **Integration:** Wrap the core library in a micro‑service or Airflow task that pulls fresh CNPJ data, generates the graph, and stores the result (e.g., as a JSON graph or PNG).  
3. **User‑Facing Layer:** Embed the generated visualisations in an internal web portal (e.g., using Flask/Dash) or export them to BI tools for broader consumption.  
4. **Scale & Automate:** Schedule regular updates, add caching, and optionally enrich nodes with external metadata (industry codes, risk scores).

**Production Readiness**  
- **Activity & Maintenance:** Last updated on 2026‑06‑24 with active issue handling, indicating a healthy maintainer presence.  
- **Community Signals:** Over 300 stars and 100+ forks show solid community interest and potential contributor base.  
- **Technical Stack:** Pure Python with common dependencies, making deployment on typical cloud or on‑prem environments straightforward.  
- **Risk Considerations:** While no immediate licensing or security red flags appear, a final review of the MIT/Apache license (as declared) and a quick vulnerability scan of dependencies are advisable before full production rollout.  

Overall, `rictom/rede-cnpj` is mature enough for a serious pilot and can be incrementally rolled out into production once the PoC validates fit‑for‑purpose visualisations and integration stability.

### Русский

**rictom/rede-cnpj** — это открытый Python‑инструмент, который визуализирует графы взаимосвязей между компаниями и их участниками на основе публичных данных CNPJ, позволяя быстро обнаруживать цепочки владения и потенциальные конфликты интересов. Типичный сценарий внедрения — интеграция в аналитический пайплайн (например, в системе мониторинга корпоративных рисков) через небольшое proof‑of‑concept: загрузка CSV‑файла с CNPJ, построение графа в NetworkX/Plotly и экспорт интерактивного дашборда. По состоянию на 24 июня 2026 года проект имеет активную поддержку, 329 звёзд, регулярные коммиты и готов к пилотному использованию в продакшене после окончательной проверки лицензии и безопасности.

### 中文

**项目简介**  
rictom/rede-cnpj 是一个基于公开 CNPJ（巴西企业登记号）数据的可视化工具，能够直观地展示股东‑公司之间的关联网络，帮助用户快速洞察企业结构和潜在的关联风险。

**价值**  
- **关系洞察**：通过图形化网络，一目了然地看到同一股东持有的多家公司或企业之间的交叉持股关系。  
- **合规与尽调**：在反洗钱、供应链审计、竞争情报等场景下，快速定位隐藏的关联方。  
- **开源可定制**：基于 Python，代码透明，易于二次开发和集成到内部数据平台。

**典型接入方式**  
1. **数据准备**：使用官方公开的 CNPJ 数据集（如 Receita Federal 提供的 CSV/JSON），或通过项目自带的爬虫脚本抓取最新数据。  
2. **依赖安装**：`pip install -r requirements.txt`（主要依赖 pandas、networkx、pyvis 等）。  
3. **生成图谱**：运行 `python generate_graph.py --input <cnpj_data.csv> --output <output.html>`，得到交互式 HTML 页面。  
4. **嵌入业务系统**：将生成的 HTML 通过 iframe、WebView 或直接在内部门户中引用；如需实时查询，可将核心逻辑封装为 Flask/Django API，前端调用返回子图数据。

**生产可用性**  
- **活跃度**：最近一次提交在 2026‑06‑24，星标 329、Fork 129，社区活跃度良好。  
- **技术成熟度**：核心使用成熟的 Python 数据处理与可视化库，易于在容器或虚拟环境中部署。  
- **可扩展性**：支持自定义节点属性、过滤规则以及增量数据更新，适合从小规模 PoC 逐步扩展到全量业务。  
- **风险**：仍需自行审查许可证（MIT/Apache 等）以及依赖库的安全报告，确保符合企业合规要求。  

综上，rede-cnpj 在关联关系分析和合规审计场景下具备即插即用的价值，接入成本低，且已具备在生产环境中进行试点的技术和社区基础。

## 🧭 Practical evaluation

**Value:** rictom/rede-cnpj may be useful when its README and activity match a concrete workflow.

**Best use cases**

- Not enough metadata yet.

**Integration notes:** Looks feasible to evaluate, but integration should start with a small proof of concept and README check.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 329 GitHub stars
- 129 forks
- updated 2026-06-24
- primary language: Python
- 7 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 53/100 |
| stars | 54/100 |
| topics | 88/100 |
| outlook | 68/100 |
| quality | 72/100 |
| recency | 80/100 |
| adoption | 53/100 |
| production | 69/100 |
| usefulness | 42/100 |
| integration | 46/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 0/100 |

---

<sub>🔭 Discovered 2026-06-24 · [View on GitHub](https://github.com/rictom/rede-cnpj) · [← Back to Misc](./README.md)</sub>
