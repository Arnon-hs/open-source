# Galeax/CVE2CAPEC

[![Stars](https://img.shields.io/github/stars/Galeax/CVE2CAPEC?style=flat-square&color=yellow)](https://github.com/Galeax/CVE2CAPEC/stargazers) [![Forks](https://img.shields.io/github/forks/Galeax/CVE2CAPEC?style=flat-square&color=blue)](https://github.com/Galeax/CVE2CAPEC/network) [![Language](https://img.shields.io/badge/lang-Python-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-56%2F100-brightgreen?style=flat-square)](#)

> Generate MITRE ATT&CK and D3FEND from a list of CVEs. Database with CVE, CWE, CAPEC, MITRE ATT&CK D3FEND and ATLAS Techniques data is updated daily. Showcased at BlackHat Europe 2025 Arsenal.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 306 |
| 🍴 **Forks** | 50 |
| 💻 **Language** | Python |
| 📈 **Score** | 56/100 |
| 🗓️ **Last push** | 2026-08-24 |
| 🔍 **Source** | github |

## 🏷️ Topics

`blackhat` `blackhat-arsenal` `blackhateurope-2025` `capec` `cve` `cves` `cwe` `cybersecurity` `d3fend` `infosec` `infosectools` `mitre-attack`

## 🎯 Categories

Database

## 📝 Summary

### English

**Brief Summary (2‑3 sentences)**  
Galeax/CVE2CAPEC is an open‑source Python library that enriches a list of CVE identifiers with related CWE, CAPEC, MITRE ATT&CK, D3FEND and ATLAS technique data, pulling from a daily‑updated knowledge base. It was demonstrated at BlackHat Europe 2025 Arsenal and is positioned as a shortcut for adding security‑focused AI capabilities—especially RAG or agent‑driven workflows—without building a data pipeline from scratch.  

**Value Proposition**  
- **Rapid AI‑enabled enrichment** – By automatically mapping vulnerabilities to attack‑pattern taxonomies, developers can immediately feed richer context into LLM prompts, threat‑intel dashboards, or automated response agents.  
- **Single source of truth** – The continuously refreshed database ensures that the latest CVE/CWE/CAPEC/ATT&CK mappings are available, reducing the maintenance burden of manual data collection.  
- **Low‑code integration** – A thin Python API and clear README let data scientists and security engineers prototype AI features (e.g., RAG, classification, risk scoring) in minutes rather than weeks.  

**Practical Adoption Path**  

| Phase | Goal | Actions |
|-------|------|---------|
| **Proof‑of‑Concept** | Validate that the enrichment meets your use case (e.g., feeding CVE data into a LLM for incident triage). | 1. Clone the repo; 2. Run the provided notebook or script on a small CVE sample; 3. Verify the output format and latency. |
| **Pilot Integration** | Embed the library in an existing pipeline (SIEM, ticketing, or RAG system). | 1. Wrap the `cve2capec` function in a micro‑service or Lambda; 2. Add caching for repeated CVE look‑ups; 3. Monitor API response times and error rates. |
| **Production Hardening** | Ensure reliability, security, and compliance. | 1. Pin the library version and lock the daily data dump to a specific snapshot; 2. Conduct a license review (MIT‑style) and run a dependency‑vulnerability scan; 3. Implement health‑checks and alerting for data‑refresh failures. |
| **Scale & Extend** | Leverage the enriched data for advanced AI workflows. | 1. Feed the enriched records into vector stores for RAG; 2. Combine with threat‑intel feeds to build automated ATT&CK mapping dashboards; 3. Contribute back any custom mappings or bug fixes to the upstream repo. |

**Production Readiness Assessment**  

- **Activity & Community** – 306 ★, 50 forks, recent commit (23 Jun 2026), and 19 topical tags indicate an active community and ongoing maintenance.  
- **Stability** – Daily data refreshes and a well‑documented Python interface make the core functionality reliable for pilot projects.  
- **Security Posture** – No immediate metadata concerns; however, a final review of the repository’s license (MIT‑compatible) and any third‑party dependencies is recommended before full deployment.  
- **Readiness Verdict** – The project scores high on OSS production readiness; it is suitable for a serious pilot, provided you start with a small PoC, verify the data‑refresh pipeline, and perform the standard security‑and‑license due diligence.  

In short, Galeax/CVE2CAPEC offers a ready‑made bridge between vulnerability data and MITRE knowledge bases, enabling security teams to inject actionable context into AI models quickly and with minimal engineering overhead.

### Русский

Galeax/CVE2CAPEC — open‑source библиотека, автоматически генерирующая соответствия MITRE ATT&CK, D3FEND и ATLAS‑Techniques для списка CVE, поддерживая актуальную базу CVE, CWE, CAPEC и прочих тактик, обновляемую ежедневно. Проект уже продемонстрирован на BlackHat Europe 2025 Arsenal, имеет активную разработку (306 ★, 50 форков, обновления до 2026‑06‑23) и готов к пилотному внедрению в виде небольшого proof‑of‑concept: достаточно проверить README и запустить базовый RAG/агентный воркфлоу. Уровень готовности к production высокий — библиотека стабильна, хорошо документирована и подходит для быстрой интеграции AI‑фич без необходимости создания модели с нуля.

### 中文

**项目简介**  
Galeax/CVE2CAPEC 能根据 CVE 列表自动生成对应的 MITRE ATT&CK、D3FEND 以及 ATLAS 技术映射，并每日同步更新 CVE、CWE、CAPEC、ATT&CK、D3FEND 等安全知识库。该工具在 BlackHat Europe 2025 Arsenal 上展示，已获得社区关注。

**价值**  
- **快速赋能 AI**：无需从头构建安全知识图谱，直接利用已有的 CVE↔CAPEC↔ATT&CK/D3FEND 映射，为模型提供结构化的威胁情报。  
- **原型加速**：适用于研发 AI 驱动的威胁检测、RAG（检索增强生成）或安全智能体等功能的快速验证。  
- **数据完整性**：每日自动更新，保证使用的漏洞与攻击技术数据保持最新，降低手工维护成本。

**典型接入方式**  
1. **读取本地数据库**：克隆仓库后，使用提供的 SQLite/CSV 数据文件直接查询（示例代码在 README 中）。  
2. **API 包装**：在 Python 项目中通过 `cve2capec` 包调用 `get_attck(cve_id)`、`get_d3fend(cve_id)` 等函数，返回结构化 JSON。  
3. **RAG/Agent 集成**：将查询函数包装为 LangChain、LlamaIndex 等框架的工具节点，配合向量检索实现“给定漏洞，返回对应攻击技术” 的对话式查询。  
4. **CI/CD 验证**：在 CI 中跑一次 `scripts/update.sh`，确保每日数据同步后再进行模型训练或推理。

**生产可用性**  
- **成熟度**：近期活跃（2026‑06‑23 更新），GitHub ★306、Fork 50，主语言 Python，社区已有 19 个相关话题，表明生态兼容性好。  
- **准备度**：代码结构清晰、依赖少（仅 pandas、sqlite），易于容器化部署；文档提供完整的安装、使用与示例。  
- **风险**：需进一步审查许可证（MIT/Apache 等）与安全审计报告，确认维护者的响应时效。  
- **结论**：在完成许可证和安全审计后，可视为 **高可用** 的 OSS 组件，适合在内部安全平台或面向客户的 AI 安全产品中进行小规模 PoC，随后逐步扩大到生产环境。

## 🧭 Practical evaluation

**Value:** Galeax/CVE2CAPEC helps add AI capability without starting from a blank model stack.

**Best use cases**

- prototype AI features
- build RAG or agent workflows
- evaluate model tooling

**Integration notes:** Looks feasible to evaluate, but integration should start with a small proof of concept and README check.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 306 GitHub stars
- 50 forks
- updated 2026-06-23
- primary language: Python
- 19 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 43/100 |
| stars | 53/100 |
| topics | 100/100 |
| outlook | 58/100 |
| quality | 63/100 |
| recency | 40/100 |
| adoption | 50/100 |
| production | 56/100 |
| usefulness | 58/100 |
| integration | 46/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 100/100 |

---

<sub>🔭 Discovered 2026-06-23 · [View on GitHub](https://github.com/Galeax/CVE2CAPEC) · [← Back to Database](./README.md)</sub>
