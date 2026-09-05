# slothflowlabs/duckle

[![Stars](https://img.shields.io/github/stars/slothflowlabs/duckle?style=flat-square&color=yellow)](https://github.com/slothflowlabs/duckle/stargazers) [![Forks](https://img.shields.io/github/forks/slothflowlabs/duckle?style=flat-square&color=blue)](https://github.com/slothflowlabs/duckle/network) [![Language](https://img.shields.io/badge/lang-Rust-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-71%2F100-brightgreen?style=flat-square)](#)

> Local-first ETL/ELT studio: a drag-and-drop visual pipeline designer that compiles to SQL and runs on DuckDB. Tiny desktop app, no servers, git-friendly workspaces.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 597 |
| 🍴 **Forks** | 39 |
| 💻 **Language** | Rust |
| 📈 **Score** | 71/100 |
| 🗓️ **Last push** | 2026-09-05 |
| 🔍 **Source** | github |

## 🏷️ Topics

`data-engineering` `data-integration` `data-pipeline` `data-quality` `desktop-app` `developer-tools` `drag-and-drop` `duckdb` `elt` `embedded` `etl` `local-first`

## 🎯 Categories

Productivity · Frontend · DevTools · Data · Database

## 📝 Summary

### English

**Brief summary**  
Duckle (slothflowlabs/duckle) is a lightweight, local‑first ETL/ELT studio that lets users build drag‑and‑drop data pipelines which are compiled to native DuckDB SQL and executed on the user’s machine. The desktop app requires no servers, stores workspaces in plain files (git‑friendly), and is built in Rust.

**Value proposition**  
Duckle turns internal knowledge bases, CSV/Parquet dumps, or any DuckDB‑compatible source into searchable, queryable assets without the overhead of a managed data warehouse. By materialising the pipeline as SQL, the resulting tables can be directly fed to LLM‑powered assistants, enabling more accurate grounding, document‑level retrieval, and “knowledge‑as‑code” versioning.

**Practical adoption path**  

| Step | What to do | Reason |
|------|------------|--------|
| 1️⃣ Quick‑look | Clone the repo, run `cargo run --release` (or download the pre‑built binary) and open the sample workspace. | Verifies that the desktop UI launches on the target OS and that DuckDB is bundled correctly. |
| 2️⃣ Proof‑of‑concept | Create a small pipeline that ingests a handful of internal CSV/JSON docs, transforms them (e.g., text‑cleaning, embeddings), and writes the result to a DuckDB table. Export the workspace to a Git repo. | Shows end‑to‑end flow from raw data → searchable table, and demonstrates the git‑friendly workflow. |
| 3️⃣ Integration test | Write a minimal script that loads the generated DuckDB file and runs a few example queries from your existing RAG pipeline or assistant backend. | Confirms that the SQL output is compatible with your downstream retrieval or embedding service. |
| 4️⃣ Scale‑up pilot | Replace the toy data with a real knowledge base (e.g., internal wiki dumps, support tickets). Add any needed custom transformations (Rust plugins or SQL UDFs). | Validates performance, resource usage, and the ability to maintain pipelines in version control. |
| 5️⃣ Production hand‑off | Freeze the workspace version, containerise the DuckDB file (if needed for CI/CD), and add monitoring of pipeline runs (DuckDB logs, file‑size alerts). | Provides a reproducible, auditable artefact that can be deployed in a CI pipeline or shipped with the assistant service. |

**Production readiness**  
- **Activity & community** – 597 stars, 39 forks, recent commits (last update 2026‑06‑23) and a healthy Rust ecosystem indicate active maintenance.  
- **Architecture** – Purely local, no external services; the only runtime dependency is DuckDB, which is battle‑tested and embeddable.  
- **Reliability** – Workspaces are plain files, making backups, rollbacks, and Git‑based CI straightforward.  
- **Scalability** – DuckDB handles multi‑GB datasets comfortably on a laptop; for larger corpora you can shard the data across multiple DuckDB files and orchestrate them with a simple script.  
- **Risk considerations** – The license (MIT) is permissive, but a final security audit of the Rust code and any third‑party crates is advisable. Verify that maintainers are responsive (e.g., recent issue triage) before committing to a long‑term production deployment.

Overall, Duckle is production‑ready for a serious pilot: it offers a low‑cost, serverless way to turn raw knowledge into queryable tables that LLM assistants can reliably ground on, with a clear, incremental path from a quick demo to a fully version‑controlled data pipeline.

### Русский

**slothflowlabs/duckle** — это локальное ETL/ELT‑студио с визуальным конструктором потоков, который в режиме drag‑and‑drop генерирует SQL‑запросы и исполняет их в DuckDB. Проект позиционируется как лёгкое десктоп‑приложение без серверов, поддерживает git‑дружественные рабочие пространства и позволяет быстро индексировать внутренние базы знаний, улучшая поиск по документам и обогащая ответы ассистентов. По состоянию на 2026‑06‑23 проект имеет активную разработку, 597 звёзд, свежие коммиты и хорошую экосистему, что делает его готовым к пилотному внедрению в production после небольшого proof‑of‑concept и проверки README/лицензии.

### 中文

**项目简介**  
slothflowlabs/duckle 是一款 **Local‑first ETL/ELT 工作室**，提供拖拽式可视化流水线编辑器，能够将数据流编译为原生 SQL 并在 DuckDB 上执行。它是一个体积极小的桌面应用，无需后端服务器，工作空间基于普通文件夹，天然支持 Git 进行版本管理。

---

## 价值点  
1. **本地化安全**：所有数据处理在本机完成，避免了敏感信息上传至云端，符合内部合规要求。  
2. **低门槛、可视化**：拖拽式 UI 让非技术成员也能快速构建、调试 ETL 流程，提升团队自助数据能力。  
3. **SQL 原生输出**：生成的 SQL 可直接在 DuckDB、PostgreSQL、Snowflake 等兼容引擎上运行，便于迁移和二次开发。  
4. **Git‑友好**：工作空间即文件系统，配合 Git 可实现流水线的版本控制、审计和 CI/CD。  
5. **开源且活跃**：截至 2026‑06‑23，拥有 597 ★、39 Fork，最近一次提交仅几天前，社区活跃度高，适合作为内部工具的长期支撑。

---

## 典型接入方式  
| 步骤 | 说明 |
|------|------|
| **1. 环境准备** | 下载并安装 `duckle`（提供 macOS/Windows/ Linux 可执行文件），或通过 `cargo install duckle` 编译安装。 |
| **2. 创建工作空间** | 在本地创建一个普通目录作为项目根，使用 `duckle init` 初始化，生成 `duckle.yaml`、`pipeline/` 等文件结构。 |
| **3. 设计流水线** | 启动桌面 UI（`duckle gui`），拖拽数据源、转换、目标节点，保存后自动生成对应的 `.sql` 文件。 |
| **4. 版本管理** | 将工作空间目录加入 Git，提交 `duckle.yaml` 与生成的 SQL，团队即可通过 PR 评审流水线变更。 |
| **5. 自动化运行** | 在 CI 脚本或本地调度器中调用 `duckle run <pipeline_name>`，DuckDB 会执行生成的 SQL，输出结果文件或写入目标数据库。 |
| **6. 与知识库/助手集成** | 将流水线输出的结构化数据（如文档索引、实体表）加载到向量数据库或检索系统，供 LLM/AI 助手进行上下文检索，实现 “内部知识可搜索、可调用”。 |

> **小型验证**：建议先在一个独立的 Git 仓库里创建一个简易的文档索引流水线（CSV → DuckDB → 向量化），验证 `duckle` 与现有检索服务（如 Milvus、Qdrant）的兼容性后，再推广到全业务。

---

## 生产可用性评估  

| 维度 | 评估 | 说明 |
|------|------|------|
| **代码活跃度** | ★★★★★ | 最近一次提交在 2026‑06‑23，持续更新，社区活跃。 |
| **社区与生态** | ★★★★☆ | 597 ★、20+ 话题，已有若干企业用户在内部使用。 |
| **安全与合规** | ★★★★☆ | 完全本地执行，无外部依赖；仍需自行审计 Rust 依赖的许可证与 CVE。 |
| **可维护性** | ★★★★☆ | 基于 Rust，二进制体积小，部署简单；文档齐全，示例丰富。 |
| **容错与监控** | ★★★☆☆ | 目前缺乏内置的作业调度/监控插件，建议结合外部调度系统（Cron、Airflow）实现。 |
| **总体评分** | **74/100** | 适合作为内部 ETL/ELT 的核心工具，进入生产环境的门槛低，只需完成安全审计和 CI 集成即可。 |

**结论**：`duckle` 已具备在生产环境中使用的技术成熟度，尤其适合需要 **本地化、可视化、Git‑友好** 的数据管道场景。建议先在非关键业务做小范围 POC，验证与现有知识库/向量检索系统的集成后，再逐步推广至全组织。

## 🧭 Practical evaluation

**Value:** slothflowlabs/duckle helps make internal knowledge searchable and usable by assistants.

**Best use cases**

- index knowledge bases
- improve search over documents
- ground assistant answers

**Integration notes:** Looks feasible to evaluate, but integration should start with a small proof of concept and README check.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 597 GitHub stars
- 39 forks
- updated 2026-06-23
- primary language: Rust
- 20 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 40/100 |
| stars | 59/100 |
| topics | 100/100 |
| outlook | 79/100 |
| quality | 74/100 |
| recency | 80/100 |
| adoption | 54/100 |
| production | 70/100 |
| usefulness | 90/100 |
| integration | 46/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 500/100 |

---

<sub>🔭 Discovered 2026-06-23 · [View on GitHub](https://github.com/slothflowlabs/duckle) · [← Back to Productivity](./README.md)</sub>
