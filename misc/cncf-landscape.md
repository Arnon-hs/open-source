# cncf/landscape

[![Stars](https://img.shields.io/github/stars/cncf/landscape?style=flat-square&color=yellow)](https://github.com/cncf/landscape/stargazers) [![Forks](https://img.shields.io/github/forks/cncf/landscape?style=flat-square&color=blue)](https://github.com/cncf/landscape/network) [![Language](https://img.shields.io/badge/lang-Unknown-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-59%2F100-brightgreen?style=flat-square)](#)

> 🌄 The Cloud Native Interactive Landscape filters and sorts hundreds of projects and products, and shows details including GitHub stars, funding, first and last commits, contributor counts and headquarters location.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 9.9k |
| 🍴 **Forks** | 2.2k |
| 💻 **Language** | Unknown |
| 📈 **Score** | 59/100 |
| 🗓️ **Last push** | 2026-08-24 |
| 🔍 **Source** | github |

## 🏷️ Topics

`cloud-native` `cncf` `crunchbase` `landscape` `logo` `serverless` `svg` `wasm`

## 🎯 Categories

Misc

## 📝 Summary

### English

**Summary**  
The CNCF Landscape is an interactive, filterable map of hundreds of cloud‑native projects and products that surfaces key metadata such as GitHub stars, funding, commit history, contributor counts, and HQ location. With ≈10 k stars, recent activity (last updated 2026‑07‑13) and strong ecosystem signals, it is a mature OSS candidate for teams that need to quickly prototype AI‑enhanced features, RAG pipelines, or agent workflows without building a model stack from scratch.  

**Value**  
By aggregating and normalising rich project metadata, the Landscape lets engineers discover, compare, and select AI‑related tools (e.g., vector stores, LLM wrappers, evaluation suites) in a single UI, dramatically cutting the research‑to‑prototype cycle. It also provides a baseline “capability map” that can be programmatically scraped for automated tooling or internal catalogues.  

**Practical adoption path**  
1. **Explore & shortlist** – Use the web UI to filter for AI/ML, backend, or product tags and export the resulting list (CSV/JSON).  
2. **Validate manually** – Review each candidate’s repository, licensing, and security posture (the Landscape’s metadata is sparse on these signals).  
3. **Prototype** – Pull the selected libraries into a sandbox, wire them into a RAG or agent workflow, and run quick proof‑of‑concept tests.  
4. **Integrate** – Once vetted, add the chosen components to your CI/CD pipeline and document them in your internal service catalog.  

**Production readiness**  
The project shows high production readiness: it is actively maintained, has a large contributor base, and is widely adopted across the cloud‑native ecosystem. The main remaining risks are the lack of detailed security/license metadata and the need for a final maintainer review, but these are typical for OSS and can be mitigated with standard due‑diligence checks before a full‑scale rollout.

### Русский

**cncf/landscape** — это интерактивный каталог облачных‑нативных проектов, который автоматически собирает и визуализирует метаданные (звёзды GitHub, финансирование, даты коммитов, количество контрибьюторов, локацию компаний) и позволяет быстро отфильтровать нужные решения. Типичный сценарий — инженеры используют его для прототипирования AI‑фич, построения RAG‑ или агентных воркфлоу и оценки инструментов модели, предварительно проверив детали проекта вручную. По уровню готовности проект считается «high»: активная разработка, широкое принятие (≈10 к звёзд), свежие обновления и сильные экосистемные сигналы делают его подходящим для серьёзных пилотов в продакшн.

### 中文

**项目简介（2‑3 句话）**  
cncf/landscape 是 CNCF 官方维护的交互式云原生生态地图，能够对数百个开源项目和商业产品进行过滤、排序，并展示 GitHub 星标、融资情况、首次/最近提交、贡献者数量、总部位置等关键信息。它帮助用户快速定位并评估适合的 AI/ML、后端或产品解决方案，避免从零搭建模型堆栈。

**价值**  
- **快速发现 AI 能力**：通过可视化的筛选和排序，直接找到已有的 AI/ML 项目或工具，省去自行调研的时间。  
- **数据驱动决策**：提供星标、活跃度、融资、贡献者等多维度指标，帮助评估项目的社区活跃度和商业潜力。  
- **原型加速**：在原型阶段即可挑选合适的模型、RAG 或 agent 工作流组件，快速搭建 PoC。

**典型接入方式**  
1. **手动检索**：在 Landscape UI 中使用关键词、标签或过滤条件（如 “AI/ML”、 “Backend”）定位目标项目。  
2. **元数据导出**：通过项目提供的 JSON/YAML 导出接口，将筛选结果下载到本地。  
3. **二次集成**：在自研平台中解析导出的元数据，结合内部 CI/CD 或治理系统完成依赖声明、许可证合规检查和安全扫描。  
> **注意**：由于发现的元数据中集成信号相对稀疏，建议在正式接入前进行人工审查，确认项目的文档、API、示例代码等是否满足业务需求。

**生产可用性**  
- **成熟度**：近期活跃（2026‑07‑13 更新），拥有 9 936 个 GitHub 星标、2 171 个 Fork，社区活跃度高。  
- **准备度**：在 OSS 候选者中属于高可用级别，可直接用于内部试点或生产前的评估阶段。  
- **风险**：暂无重大元数据风险，但仍需对许可证合规、供应链安全以及维护者活跃度进行最终审查后方可正式上线。  

综上，cncf/landscape 是一个高质量的云原生生态发现工具，适合作为 AI 能力快速原型和生产评估的入口。

## 🧭 Practical evaluation

**Value:** cncf/landscape helps add AI capability without starting from a blank model stack.

**Best use cases**

- prototype AI features
- build RAG or agent workflows
- evaluate model tooling

**Integration notes:** Needs manual inspection before adoption because integration signals are sparse in the discovered metadata.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 9936 GitHub stars
- 2171 forks
- updated 2026-07-13
- 8 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 83/100 |
| stars | 85/100 |
| topics | 100/100 |
| outlook | 64/100 |
| quality | 78/100 |
| recency | 40/100 |
| adoption | 85/100 |
| production | 61/100 |
| usefulness | 42/100 |
| integration | 46/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 0/100 |

---

<sub>🔭 Discovered 2026-07-13 · [View on GitHub](https://github.com/cncf/landscape) · [← Back to Misc](./README.md)</sub>
