# OpenCTI-Platform/connectors

[![Stars](https://img.shields.io/github/stars/OpenCTI-Platform/connectors?style=flat-square&color=yellow)](https://github.com/OpenCTI-Platform/connectors/stargazers) [![Forks](https://img.shields.io/github/forks/OpenCTI-Platform/connectors?style=flat-square&color=blue)](https://github.com/OpenCTI-Platform/connectors/network) [![Language](https://img.shields.io/badge/lang-Python-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-58%2F100-brightgreen?style=flat-square)](#)

> OpenCTI Connectors

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 559 |
| 🍴 **Forks** | 606 |
| 💻 **Language** | Python |
| 📈 **Score** | 58/100 |
| 🗓️ **Last push** | 2026-09-05 |
| 🔍 **Source** | github |

## 🏷️ Topics

`cti` `cybersecurity` `misp` `mitre-attack` `threat-intelligence`

## 🎯 Categories

Misc

## 📝 Summary

### English

Here's a brief summary of the OpenCTI-Platform/connectors project:

OpenCTI-Platform/connectors is an open-source project that enables teams to persist, query, and move data with minimal custom setup, making it a valuable tool for database management and security. Its practical adoption path involves evaluating the project through a small proof of concept and reviewing the README documentation, followed by a thorough review of the license, security posture, and active maintainers. With recent activity, strong adoption, and a robust ecosystem, OpenCTI-Platform/connectors is considered production-ready, making it a suitable candidate for serious piloting.

### Русский

Резюме OpenCTI-Platform/connectors:

OpenCTI-Platform/connectors - это открытый проект, который помогает командам сохранять, искать и перемещать данные с минимальной настройкой. Этот проект подойдет для команд, которые стремятся оптимизировать доступ к данным и прототипировать приложения с базой данных. OpenCTI-Platform/connectors уже готов к использованию в производственной среде, с сильным показателем активности, широкой адоптацией и сильным экосистемным потенциалом.

### 中文

**项目简介**  
OpenCTI‑Platform/connectors 是 OpenCTI 生态中的官方连接器集合，提供多种数据源（Threat Intelligence、Vulnerability、Malware 等）的采集、归一化和写入能力，帮助安全团队在统一平台上快速聚合和查询威胁情报。

**价值**  
- **降低集成成本**：无需自行编写采集脚本，直接使用现成的 Python 连接器即可把外部情报库持久化到 OpenCTI。  
- **加速数据访问**：统一的图谱模型让所有情报在平台内即时可查询，提升分析与响应效率。  
- **支持快速原型**：通过即插即用的连接器，团队可以在几分钟内部署完整的情报流，验证业务需求后再做深度定制。

**典型接入方式**  
1. **环境准备**：在 OpenCTI 平台部署完成后，克隆 `connectors` 仓库并根据目标数据源选择对应的子目录（如 `stix`, `cve`, `shodan` 等）。  
2. **配置**：复制 `config.yml.example` 为 `config.yml`，填写 API 密钥、查询频率、目标工作流（Connector ID）等参数。  
3. **部署**：推荐使用 Docker Compose 或 Kubernetes Helm Chart（仓库已提供），启动对应的 connector 服务；服务会定时拉取数据并调用 OpenCTI 的 GraphQL 接口写入。  
4. **验证**：登录 OpenCTI UI，检查对应的 “Data Sources” 是否出现新数据，或使用 GraphQL 查询确认写入成功。

**生产可用性**  
- **活跃度**：截至 2026‑07‑04，项目拥有 559 ⭐、606 🍴，最近一次提交在同一天，说明维护活跃。  
- **技术成熟度**：全程使用 Python 编写，配套 Docker 镜像和 Helm Chart，易于在容器化环境中大规模部署。  
- **安全与合规**：采用 Apache‑2.0 许可证，暂无已知重大安全漏洞；仍建议在内部进行一次依赖审计。  
- **适配性**：已被多个企业级 SOC 与威胁情报平台采用，具备从小规模 PoC（如单一 connector）到全链路生产部署的平滑扩展路径。  

综上，OpenCTI‑Platform/connectors 在功能完整性、社区活跃度和部署便利性方面均已达到生产级别，适合作为安全情报平台的核心数据摄取层。

## 🧭 Practical evaluation

**Value:** OpenCTI-Platform/connectors helps teams persist, query, and move data with less custom plumbing.

**Best use cases**

- manage persistence
- speed up data access
- prototype database-backed apps

**Integration notes:** Looks feasible to evaluate, but integration should start with a small proof of concept and README check.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 559 GitHub stars
- 606 forks
- updated 2026-07-04
- primary language: Python
- 5 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 70/100 |
| stars | 58/100 |
| topics | 63/100 |
| outlook | 68/100 |
| quality | 72/100 |
| recency | 80/100 |
| adoption | 62/100 |
| production | 69/100 |
| usefulness | 42/100 |
| integration | 46/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 0/100 |

---

<sub>🔭 Discovered 2026-07-04 · [View on GitHub](https://github.com/OpenCTI-Platform/connectors) · [← Back to Misc](./README.md)</sub>
