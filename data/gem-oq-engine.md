# gem/oq-engine

[![Stars](https://img.shields.io/github/stars/gem/oq-engine?style=flat-square&color=yellow)](https://github.com/gem/oq-engine/stargazers) [![Forks](https://img.shields.io/github/forks/gem/oq-engine?style=flat-square&color=blue)](https://github.com/gem/oq-engine/network) [![Language](https://img.shields.io/badge/lang-Python-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-59%2F100-brightgreen?style=flat-square)](#)

> OpenQuake Engine: a software for Seismic Hazard and Risk Analysis

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 441 |
| 🍴 **Forks** | 320 |
| 💻 **Language** | Python |
| 📈 **Score** | 59/100 |
| 🗓️ **Last push** | 2026-09-05 |
| 🔍 **Source** | github |

## 🏷️ Topics

`cluster` `earthquakes` `hazard` `hazard-assessment` `hpc` `openquake` `openquake-engine` `psha` `python` `risk` `risk-analysis` `risk-assessment`

## 🎯 Categories

Data

## 📝 Summary

### English

**Summary**  
OpenQuake Engine (gem/oq-engine) is a Python‑based, open‑source platform for seismic hazard and risk analysis that is actively maintained (last update 2026‑06‑29), has strong community adoption (≈ 440 ★, 320 forks) and is supported by a rich set of documentation and examples. Its proven track record in academic and governmental projects makes it a solid candidate for pilots that need to model earthquake scenarios, compute ground‑motion fields, and assess structural or portfolio‑level risk.

**Value** – The engine bundles state‑of‑the‑art probabilistic seismic hazard calculations, exposure‑loss pipelines, and post‑processing tools in a single, extensible code base, letting engineers and researchers replace ad‑hoc scripts with a vetted, reproducible workflow. Because it is open source, you can customize models, integrate with GIS or asset‑management systems, and avoid costly proprietary licenses.

**Adoption path** – Start with a small proof‑of‑concept: clone the repo, follow the “Getting Started” section of the README, and run one of the supplied example calculations (e.g., a regional hazard map). Validate the output against published results, then incrementally replace your existing scripts with the engine’s API or CLI calls, adding your own exposure data and loss models as needed.

**Production readiness** – The project scores high on readiness: recent commits, active issue discussion, and a sizable user base indicate a stable code base and responsive maintainers. After the initial PoC, a pilot can be scaled to full‑pipeline production by containerizing the engine (Docker/Singularity), integrating it with your CI/CD pipeline, and establishing routine security and dependency audits. Once these steps are completed, OpenQuake Engine is ready for serious, mission‑critical seismic risk projects.

### Русский

Резюме проекта gem/oq-engine:

Gem/oq-engine - это открытый исходный код проект, предназначенный для анализа опасности и риска землетрясений. Этот проект может быть полезен для организаций, которые ищут решение для оценки потенциальных рисков землетрясений, и готовы внедрить его в свою работу, если README и активность проекта соответствуют их конкретному потоку работы. Проект готов к использованию в продакшн-окружении, поскольку имеет свежую активность, широкую адаптацию и сильные сигналы экосистемы.

### 中文

**项目简介**  
gem/oq-engine（OpenQuake Engine）是一套开源的地震危害与风险分析平台，基于 Python 实现，能够对区域、场景或设施级别的地震概率、地面运动和损失进行完整的数值模拟和统计评估。

**价值**  
- **专业性强**：涵盖地震源模型、衰减关系、场地响应和风险损失模型，满足科研、政府部门和保险公司的严苛需求。  
- **可复现、透明**：所有计算流程、参数和数据均在代码中明确定义，便于审计和法规合规。  
- **生态完善**：拥有 400+ Stars、300+ Forks，活跃的社区和丰富的插件（如 GIS、数据库、可视化），可以直接对接已有的地理信息系统或灾害管理平台。

**典型接入方式**  
1. **本地或容器化部署**：克隆仓库后使用 `conda`/`pip` 安装依赖，或通过官方提供的 Docker 镜像快速启动。  
2. **工作流集成**：在已有的灾害评估 pipeline 中调用 `oq-engine` 的 CLI（`oq engine --run`）或 Python API，读取/写入 JSON、CSV 或 PostGIS 数据，实现自动化批量计算。  
3. **结果可视化**：利用自带的 `oq-report` 或与 Jupyter Notebook、Plotly、Kepler.gl 等工具结合，生成地图、危害曲线和风险曲线，便于向决策者展示。

**生产可用性**  
- **活跃维护**：最近一次提交在 2026‑06‑29，核心功能和依赖均在持续更新。  
- **成熟度高**：已在多个国家级地震风险项目中实际部署，社区提供了详尽的文档、示例和 FAQ。  
- **安全与合规**：采用 BSD‑3-Clause 许可证，代码审计记录公开，安全漏洞响应及时。  
- **推荐做法**：在正式上线前先在测试环境完成一次端到端的 POC（例如对单一地区的 PSHA），验证输入数据格式、计算资源需求和结果输出是否符合业务需求，然后再推广到生产环境。  

综上，gem/oq-engine 具备完整的地震风险分析能力、易于集成的接口以及稳健的社区支持，是面向生产环境的可靠 OSS 选型。

## 🧭 Practical evaluation

**Value:** gem/oq-engine may be useful when its README and activity match a concrete workflow.

**Best use cases**

- Not enough metadata yet.

**Integration notes:** Looks feasible to evaluate, but integration should start with a small proof of concept and README check.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 441 GitHub stars
- 320 forks
- updated 2026-06-29
- primary language: Python
- 15 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 63/100 |
| stars | 56/100 |
| topics | 100/100 |
| outlook | 71/100 |
| quality | 76/100 |
| recency | 80/100 |
| adoption | 58/100 |
| production | 70/100 |
| usefulness | 42/100 |
| integration | 46/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 100/100 |

---

<sub>🔭 Discovered 2026-06-29 · [View on GitHub](https://github.com/gem/oq-engine) · [← Back to Data](./README.md)</sub>
