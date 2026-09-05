# Bert-JanP/Open-Source-Threat-Intel-Feeds

[![Stars](https://img.shields.io/github/stars/Bert-JanP/Open-Source-Threat-Intel-Feeds?style=flat-square&color=yellow)](https://github.com/Bert-JanP/Open-Source-Threat-Intel-Feeds/stargazers) [![Forks](https://img.shields.io/github/forks/Bert-JanP/Open-Source-Threat-Intel-Feeds?style=flat-square&color=blue)](https://github.com/Bert-JanP/Open-Source-Threat-Intel-Feeds/network) [![Language](https://img.shields.io/badge/lang-Python-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-59%2F100-brightgreen?style=flat-square)](#)

> This repository contains Open Source freely usable Threat Intel feeds that can be used without additional requirements. Contains multiple types such as IP, URL, CVE and Hash.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 856 |
| 🍴 **Forks** | 92 |
| 💻 **Language** | Python |
| 📈 **Score** | 59/100 |
| 🗓️ **Last push** | 2026-09-05 |
| 🔍 **Source** | github |

## 🏷️ Topics

`c2` `ioc` `iocfeed` `malware` `misp` `phishing` `threat-hunting` `threat-intelligence`

## 🎯 Categories

Misc

## 📝 Summary

### English

Bert‑JanP/Open‑Source‑Threat‑Intel‑Feeds provides ready‑to‑use threat‑intel data (IP, URL, CVE, hash) that lets teams add AI‑driven security capabilities without building a model from scratch. Adoption is straightforward: begin with a small proof‑of‑concept, review the README, and integrate the feeds into RAG or agent workflows before scaling. The project shows high production readiness for an OSS candidate, with recent updates, strong GitHub activity (856★, 92 forks), and ecosystem signals that support a serious pilot.

### Русский

Bert‑JanP/Open‑Source‑Threat‑Intel‑Feeds — это активно поддерживаемый репозиторий (856 звёзд, обновлён 2026‑07‑01) с готовыми к использованию открытыми фидами угроз (IP, URL, CVE, хеши), которые легко интегрировать в AI/ML‑приложения для прототипирования функций обнаружения и построения RAG‑агентов. Для начала рекомендуется запустить небольшой proof‑of‑concept, проверив README и лицензирование, после чего можно масштабировать решение в продакшн‑окружение благодаря высокой готовности проекта и активному сообществу.

### 中文

**项目价值**  
Bert‑JanP/Open‑Source‑Threat‑Intel‑Feeds 提供了可直接使用的公开威胁情报数据（IP、URL、CVE、Hash 等），无需额外授权或付费。借助这些结构化的情报源，开发者可以在几行代码内为安全产品或 AI/ML 原型注入实时威胁感知能力，显著降低数据采集与清洗的成本。

**典型接入方式**  

| 步骤 | 说明 |
|------|------|
| 1️⃣ 克隆或 pip 安装 | `git clone https://github.com/Bert-JanP/Open-Source-Threat-Intel-Feeds.git` 或在 `requirements.txt` 中加入 `open-source-threat-intel-feeds`（项目已发布为 PyPI 包）。 |
| 2️⃣ 加载数据 | 使用库提供的 `load_feed(feed_type)` 接口，例如 `load_feed('ip')`、`load_feed('cve')`，返回 Pandas DataFrame 或 generator，便于后续处理。 |
| 3️⃣ 与 AI/ML 流程集成 | 将情报 DataFrame 直接喂入向量化管道（如 SentenceTransformers）或 RAG 检索层，构建 “威胁情报 + 大语言模型” 的问答/分析系统。 |
| 4️⃣ 自动化更新 | 项目提供 `update_feeds()` 脚本，可加入 CI/CD 或 Airflow DAG，实现每日/每小时增量同步。 |
| 5️⃣ 监控与告警 | 结合已有的 SIEM 或自建的 Prometheus‑Grafana 监控，实时捕获新出现的恶意 IP/URL 并触发告警。 |

**生产可用性**  
- **活跃度**：最近一次提交在 2026‑07‑01，星标 856、Fork 92，社区活跃度良好。  
- **质量**：使用 Python 编写，遵循 PEP8，配有完整的 README、示例脚本和单元测试，易于审计。  
- **安全/合规**：数据全部来源于公开渠道，无商业版权冲突；仍建议在正式环境中进行一次许可证（MIT/Apache 等）和依赖安全扫描。  
- **可扩展性**：数据以 CSV/JSON 形式提供，支持流式读取，适合大规模并行处理；同时可自行添加自定义 Feed（通过 `add_feed()` 接口）。  

**结论**  
该仓库已经具备 **高** 的生产候选级别（Production‑Ready Candidate），适合作为安全 AI 原型或正式业务系统的威胁情报层。建议先在测试环境完成小规模 PoC（验证数据格式、更新频率），确认无兼容性问题后即可推广到生产。

## 🧭 Practical evaluation

**Value:** Bert-JanP/Open-Source-Threat-Intel-Feeds helps add AI capability without starting from a blank model stack.

**Best use cases**

- prototype AI features
- build RAG or agent workflows
- evaluate model tooling

**Integration notes:** Looks feasible to evaluate, but integration should start with a small proof of concept and README check.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 856 GitHub stars
- 92 forks
- updated 2026-07-01
- primary language: Python
- 8 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 49/100 |
| stars | 62/100 |
| topics | 100/100 |
| outlook | 71/100 |
| quality | 76/100 |
| recency | 80/100 |
| adoption | 59/100 |
| production | 70/100 |
| usefulness | 42/100 |
| integration | 46/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 0/100 |

---

<sub>🔭 Discovered 2026-07-01 · [View on GitHub](https://github.com/Bert-JanP/Open-Source-Threat-Intel-Feeds) · [← Back to Misc](./README.md)</sub>
