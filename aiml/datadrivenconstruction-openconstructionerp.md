# datadrivenconstruction/OpenConstructionERP

[![Stars](https://img.shields.io/github/stars/datadrivenconstruction/OpenConstructionERP?style=flat-square&color=yellow)](https://github.com/datadrivenconstruction/OpenConstructionERP/stargazers) [![Forks](https://img.shields.io/github/forks/datadrivenconstruction/OpenConstructionERP?style=flat-square&color=blue)](https://github.com/datadrivenconstruction/OpenConstructionERP/network) [![Language](https://img.shields.io/badge/lang-TypeScript-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-60%2F100-brightgreen?style=flat-square)](#)

> Open-source construction ERP - BOQ, PDF/CAD/BIM takeoff, AI cost matching. 42 regional catalogues, 21 languages, 71 modules. AGPL-3.0. v3.0 - pip install openconstructionerp

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 385 |
| 🍴 **Forks** | 125 |
| 💻 **Language** | TypeScript |
| 📈 **Score** | 60/100 |
| 🗓️ **Last push** | 2026-08-24 |
| 🔍 **Source** | github |

## 🏷️ Topics

`4d` `5d` `ai` `autocad` `bill-of-quantities` `bim` `boq` `cad` `calculation` `construction` `cost-estimation` `erp`

## 🎯 Categories

AI/ML

## 📝 Summary

### English

**Brief Summary**  
OpenConstructionERP is an AGPL‑3.0‑licensed, TypeScript‑based ERP for the construction industry. It covers the full estimate‑to‑invoice cycle—BOQ creation, PDF/CAD/BIM take‑off, AI‑driven cost matching, and integrates 42 regional catalogues in 21 languages across 71 functional modules. The project can be installed with a single `pip install openconstructionerp` command (v3.0) and is actively maintained (last update 2026‑06‑23).

**Value Proposition**  
- **End‑to‑end automation**: By digitising take‑off, costing, and procurement, the platform reduces manual spreadsheet work and accelerates bid preparation.  
- **AI‑enhanced cost matching**: Machine‑learning models suggest the most appropriate price items from a massive, region‑specific catalogue, improving estimate accuracy.  
- **Global reach**: 42 regional catalogues and 21 language packs let multinational contractors reuse the same system across sites, ensuring data consistency and compliance.  
- **Extensible architecture**: 71 modular services (e.g., inventory, payroll, project scheduling) can be enabled or replaced, making the ERP adaptable to niche workflows or integration with existing tools.

**Practical Adoption Path**  
1. **Pilot Installation** – Deploy the Docker‑compose or Helm chart in a sandbox environment; the `pip install openconstructionerp` command pulls the core services.  
2. **Data Onboarding** – Import existing BOQ, CAD/BIM files, and map them to the appropriate regional catalogue using the built‑in import wizard or the REST API.  
3. **AI Model Tuning** – Run the provided cost‑matching notebooks on historic project data to fine‑tune the AI models for your market segment.  
4. **User Training & Role Configuration** – Leverage the role‑based UI to grant estimators, site managers, and accountants the right permissions; the multilingual UI eases adoption across teams.  
5. **Production Roll‑out** – Migrate the sandbox to a high‑availability Kubernetes cluster, enable monitoring (Prometheus/Grafana) and backup pipelines, and integrate with existing ERP/CRM systems via the open REST/GraphQL API or the provided SDK.

**Production Readiness**  
- **Activity & Community**: 385 ★, 125 forks, frequent commits, and a healthy issue‑response cycle indicate an engaged maintainer base.  
- **Technical Maturity**: 71 well‑documented modules, TypeScript codebase, CI/CD pipelines, and containerised deployments demonstrate production‑grade engineering practices.  
- **Ecosystem Fit**: Exposes clear integration points (REST/GraphQL API, CLI, SDK), making it straightforward to embed in existing construction‑tech stacks or to build custom analytics pipelines.  
- **Risks to Address**: Verify the AGPL‑3.0 compliance impact for your organization, conduct a security audit of third‑party dependencies, and confirm that maintainers have a documented on‑call process for critical incidents.

Overall, OpenConstructionERP shows strong signals for a serious pilot or full‑scale deployment in construction firms seeking to modernise estimating, cost control, and project‑wide data workflows.

### Русский

OpenConstructionERP — это полностью открытая ERP‑система для строительного сектора, позволяющая автоматически формировать сметные расчёты (BOQ) из PDF/CAD/BIM, сопоставлять их с затратами с помощью ИИ и работать с 42 региональными каталогами на 21 языке через 71 модуль. Типичный сценарий внедрения: интеграция через API/CLI в существующие процессы планирования и контроля проектов, где система берёт чертежи, генерирует сметы и сразу же сравнивает их с актуальными ценами, ускоряя оценку и снижение расходов. Проект имеет высокий уровень готовности к продакшн: активные коммиты, 385 звёзд, 125 форков, поддержка TypeScript, AGPL‑3.0 и готовый пакет `pip install openconstructionerp` позволяют быстро развернуть и масштабировать решение.

### 中文

**项目简介**  
datadrivenconstruction/OpenConstructionERP 是一套开源建筑行业 ERP 系统，涵盖 BOQ、PDF/CAD/BIM 计量、AI 成本匹配等功能，内置 42 个地区目录、21 种语言和 71 个业务模块，采用 AGPL‑3.0 许可证，最新版本可通过 `pip install openconstructionerp` 快速获取。

**价值**  
- **全流程数字化**：从图纸提量到成本核算全链路自动化，显著降低人工计量和核算错误。  
- **多语言、多地区**：一次部署即可支持全球不同地区和语言的项目，适合跨国施工企业。  
- **AI 辅助**：利用 AI 模型实现成本匹配和预测，帮助企业更精准地编制预算和控制成本。

**典型接入方式**  
1. **Python 包**：`pip install openconstructionerp` 后直接在脚本或 Jupyter Notebook 中调用 API。  
2. **REST/GraphQL 接口**：系统自带的 API 服务可通过 HTTP 请求与现有业务系统（如 CRM、财务系统）对接。  
3. **CLI 工具**：提供命令行工具用于批量导入/导出图纸、生成报表，适合 DevOps 自动化流程。  
4. **SDK**：官方 TypeScript SDK 支持前端或 Node.js 应用快速集成。

**生产可用性**  
- **活跃度高**：截至 2026‑06‑23 最近一次提交，GitHub ★385、Fork 125，社区活跃。  
- **模块化设计**：71 个可插拔模块，易于按需裁剪和扩展。  
- **成熟生态**：支持多语言、多地区目录，已在多个项目中实战验证。  
- **安全合规**：采用 AGPL‑3.0 开源许可证，代码审计和依赖检查工具已集成，适合企业内部审计。  

综合来看，OpenConstructionERP 已具备进入生产环境的技术成熟度，适合作为建筑企业数字化转型的核心平台进行试点或全量部署。

## 🧭 Practical evaluation

**Value:** datadrivenconstruction/OpenConstructionERP helps research and automate market workflows.

**Best use cases**

- research trading systems
- backtest strategies
- monitor market workflows

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 385 GitHub stars
- 125 forks
- updated 2026-06-23
- primary language: TypeScript
- 20 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 53/100 |
| stars | 55/100 |
| topics | 100/100 |
| outlook | 59/100 |
| quality | 64/100 |
| recency | 40/100 |
| adoption | 54/100 |
| production | 59/100 |
| usefulness | 58/100 |
| integration | 62/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 100/100 |

---

<sub>🔭 Discovered 2026-06-23 · [View on GitHub](https://github.com/datadrivenconstruction/OpenConstructionERP) · [← Back to AI/ML](./README.md)</sub>
