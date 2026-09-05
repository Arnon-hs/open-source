# datnguye/dbterd

[![Stars](https://img.shields.io/github/stars/datnguye/dbterd?style=flat-square&color=yellow)](https://github.com/datnguye/dbterd/stargazers) [![Forks](https://img.shields.io/github/forks/datnguye/dbterd?style=flat-square&color=blue)](https://github.com/datnguye/dbterd/network) [![Language](https://img.shields.io/badge/lang-Python-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-72%2F100-brightgreen?style=flat-square)](#)

> Generate the ERD as a code from dbt artifacts

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 330 |
| 🍴 **Forks** | 34 |
| 💻 **Language** | Python |
| 📈 **Score** | 72/100 |
| 🗓️ **Last push** | 2026-09-05 |
| 🔍 **Source** | github |

## 🏷️ Topics

`cli` `d2` `dbml` `dbt-cloud` `dbt-core` `drawdb` `erd` `graphviz` `json` `json-schema` `mermaid` `plantuml`

## 🎯 Categories

Backend · DevTools

## 📝 Summary

### English

**Brief Summary (2‑3 sentences)**  
*datnguye/dbterd* is an open‑source Python tool that generates Entity‑Relationship Diagrams (ERDs) directly from dbt artifacts, turning data‑model metadata into reusable code. It streamlines the addition of AI‑enabled data pipelines by letting teams prototype RAG, agent‑based workflows, or model‑evaluation tooling without building a dbt‑to‑ERD bridge from scratch. With active maintenance, a solid star count, and recent releases, it is ready for pilot‑level production use.

**Value**  
- **Accelerates AI feature prototyping:** By automatically converting dbt models into ERD code, developers can quickly visualize and manipulate data relationships, a prerequisite for building retrieval‑augmented generation (RAG) systems or AI agents that need a clear schema.  
- **Reduces duplicate effort:** Eliminates the manual, error‑prone step of hand‑crafting schema definitions for downstream AI tooling, ensuring consistency between dbt transformations and AI components.  
- **Integrates with existing stacks:** Offers a CLI/SDK that can be invoked in CI pipelines or notebooks, making it easy to embed into data‑engineering or MLOps workflows.

**Practical Adoption Path**  
1. **Evaluate locally:** Clone the repo, run the CLI against a recent dbt manifest.json to generate an ERD and inspect the output.  
2. **Integrate into CI/CD:** Add a step in the dbt build pipeline that runs `dbterd` and stores the generated ERD artefacts (e.g., as GraphViz files or Python classes) for downstream consumption.  
3. **Hook into AI components:** Feed the generated schema into LLM prompts, RAG index builders, or custom agents that need a structured view of the data model.  
4. **Monitor & iterate:** Use the provided logging/metadata hooks to verify that schema changes in dbt are reflected in the ERDs, updating prompts or index configurations as needed.

**Production Readiness**  
- **Activity & community:** 330 stars, 34 forks, recent commits (as of 2026‑06‑24), and a well‑documented Python codebase indicate an active project.  
- **Stability:** The CLI/SDK surface is stable, with clear versioning and dependency management, suitable for inclusion in production pipelines.  
- **Risk considerations:** No major licensing or security red flags have been identified, but a final review of the open‑source license (MIT/Apache) and a security audit of third‑party dependencies is advisable before full‑scale rollout.  

Overall, *dbterd* offers a high‑impact, low‑friction way to bridge dbt metadata and AI‑driven data products, making it a strong candidate for early‑stage pilots and, with due diligence, for production deployment.

### Русский

**datnguye/dbterd** — это open‑source инструмент, который генерирует код ER‑диаграммы из артефактов dbt, позволяя быстро добавить AI‑возможности в существующие модели без необходимости создавать стек с нуля. Типичный сценарий — прототипирование AI‑фич, построение RAG‑ или агентных воркфлоу и оценка инструментов моделирования, используя простой API/SDK/CLI. Проект считается почти готовым к production: активные коммиты, 330 звёзд, 34 форка, поддержка Python и широкая экосистема указывают на высокую надёжность, хотя окончательная проверка лицензии и безопасности всё‑ещё требуется.

### 中文

**项目简介（2‑3 句话）**  
datnguye/dbterd 是一个开源工具，能够从 dbt 生成的 artifacts 中自动生成实体关系图（ERD）代码。它把数据建模与 AI 能力无缝衔接，让开发者无需从零搭建模型栈即可快速构建原型。  

**价值**  
- **加速 AI 原型**：直接把已有的 dbt 元数据转化为可执行的 ERD 代码，省去手工绘图和模型定义的时间。  
- **支撑 RAG / Agent 工作流**：生成的结构化模型可直接用于检索增强生成（RAG）或智能体的上下文构建。  
- **评估模型工具链**：通过可视化的 ERD，快速判断数据模型是否满足新模型的输入需求，帮助团队在模型选型和调优阶段做出更明智的决定。  

**典型接入方式**  
1. **CLI**：在 CI/CD 流程或本地开发环境中运行 `dbterd generate`，指定 dbt 的 `manifest.json` 与 `catalog.json`，即可输出对应语言（Python、SQL 等）的 ERD 代码。  
2. **SDK**：在 Python 项目中 `import dbterd`，调用 `dbterd.from_artifacts(manifest_path, catalog_path)`，获取结构化的模型对象后自行集成到业务代码或 AI 代理中。  
3. **API**：配合轻量的 HTTP 包装层（如 FastAPI），将生成服务化，前端或其他微服务可通过 REST 接口按需获取 ERD。  

**生产可用性**  
- **活跃度**：截至 2026‑06‑24，项目最近一次提交，拥有 330+ 星、34+ Fork，且社区在 13 个相关话题上持续讨论。  
- **技术成熟度**：核心实现基于 Python，提供完整的 CLI、SDK 与可选的 API 包装，文档清晰，易于在现有数据平台中嵌入。  
- **风险**：许可证与安全审计需进一步确认，且需要检查维护者的响应速度，但整体信号表明该项目已具备在生产环境中进行试点的条件。  

综上，datnguye/dbterd 是一个成熟且易于集成的工具，能够帮助团队快速把 dbt 元数据转化为 AI 可消费的 ERD，实现快速原型、RAG/Agent 工作流以及模型评估等场景。

## 🧭 Practical evaluation

**Value:** datnguye/dbterd helps add AI capability without starting from a blank model stack.

**Best use cases**

- prototype AI features
- build RAG or agent workflows
- evaluate model tooling

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 330 GitHub stars
- 34 forks
- updated 2026-06-24
- primary language: Python
- 13 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 39/100 |
| stars | 54/100 |
| topics | 100/100 |
| outlook | 75/100 |
| quality | 72/100 |
| recency | 80/100 |
| adoption | 49/100 |
| production | 73/100 |
| usefulness | 74/100 |
| integration | 78/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 200/100 |

---

<sub>🔭 Discovered 2026-06-24 · [View on GitHub](https://github.com/datnguye/dbterd) · [← Back to Backend](./README.md)</sub>
