# pgvector/pgvector-python

[![Stars](https://img.shields.io/github/stars/pgvector/pgvector-python?style=flat-square&color=yellow)](https://github.com/pgvector/pgvector-python/stargazers) [![Forks](https://img.shields.io/github/forks/pgvector/pgvector-python?style=flat-square&color=blue)](https://github.com/pgvector/pgvector-python/network) [![Language](https://img.shields.io/badge/lang-Python-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-55%2F100-brightgreen?style=flat-square)](#)

> pgvector support for Python

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 1.5k |
| 🍴 **Forks** | 95 |
| 💻 **Language** | Python |
| 📈 **Score** | 55/100 |
| 🗓️ **Last push** | 2026-09-05 |
| 🔍 **Source** | github |

## 🏷️ Topics

_no topics_

## 🎯 Categories

Misc

## 📝 Summary

### English

**Brief Summary**  
pgvector‑python is the official Python client extension that adds support for the pgvector similarity‑search data type in PostgreSQL. With a solid user base (≈1.5 k stars) and recent activity, it lets Python applications store and query high‑dimensional vectors directly in the database, simplifying AI/ML pipelines that currently rely on separate vector stores.

**Value**  
- **Unified stack** – Eliminates the need for a separate vector database; vectors live alongside relational data, enabling joint filtering, joins, and transactional guarantees.  
- **Familiar API** – Wraps the standard `psycopg2`/`psycopg` connection objects, so existing Python code can be extended with just a few import statements.  
- **Open‑source & community‑backed** – A healthy star/fork count and recent commits indicate community interest and ongoing bug fixes.

**Practical Adoption Path**  
1. **Prototype** – Install via `pip install pgvector` and run the provided migration (`CREATE EXTENSION IF NOT EXISTS vector;`).  
2. **Integrate** – Replace raw SQL for vector columns with the helper classes (`Vector`, `Ivfflat`, etc.) and use `INSERT … VALUES (%s::vector)` or the ORM adapters.  
3. **Validate** – Run a small benchmark against your target PostgreSQL version (≥14) to confirm query latency and index behavior (e.g., `CREATE INDEX ON table USING ivfflat (embedding vector_cosine_ops);`).  
4. **Security & License Review** – Verify the MIT license fits your policy and scan the repository for known vulnerabilities (none reported as of the latest scan).  
5. **Production Hardening** – Pin the library version, add it to your CI pipeline, and monitor the upstream repo for breaking changes.

**Production Readiness**  
- **Maturity**: Medium. The library is stable enough for internal tools and prototypes, but it still requires due‑diligence on dependency updates and compatibility with your PostgreSQL version.  
- **Maintenance**: Recent commits (as of 2026‑06‑26) show active maintenance, yet the core maintainer count is modest; consider contributing back or forking if you need long‑term guarantees.  
- **Risk**: No critical security or licensing red flags, but a final audit of the maintainers’ activity and any upcoming breaking changes is advisable before a full production rollout.  

In short, pgvector‑python offers a low‑friction way to bring vector search into Python‑driven data pipelines; with a brief validation phase and standard open‑source risk checks, it can be safely promoted from prototype to production for many internal use cases.

### Русский

**pgvector/pgvector-python** — это Python‑обёртка для расширения PostgreSQL pgvector, позволяющая хранить и искать векторные представления (например, эмбеддинги) непосредственно в базе. Подойдёт для прототипов и внутренних сервисов, где требуется быстрый поиск похожих объектов (рекомендации, поиск по изображениям, семантический поиск текста) без добавления отдельного векторного движка. Готовность к production — средняя: проект имеет более 1500 звёзд, активные коммиты и актуальную поддержку (обновление 2026‑06‑26), но перед запуском в продакшн следует проверить лицензию, безопасность зависимостей и наличие постоянных мейнтейнеров.

### 中文

**项目简介**  
pgvector/pgvector‑python 为 PostgreSQL 的向量扩展 pgvector 提供 Python 客户端封装，使得在 Python 应用中可以像普通列一样读写向量数据，便于在机器学习、推荐系统、相似度搜索等场景中直接利用数据库进行向量检索。

**价值**  
- **统一存储**：向量与业务数据同库同表，无需额外的向量搜索服务，降低运维复杂度。  
- **零学习成本**：基于 psycopg（或 asyncpg）实现，使用熟悉的 DB‑API 接口即可完成向量的插入、更新和 `SELECT … ORDER BY vector <-> query_vector` 查询。  
- **开源生态**：拥有 1500+ 星、活跃的社区和近期更新，适合作为原型或内部项目的快速实现层。

**典型接入方式**  

| 步骤 | 操作 | 示例代码 |
|------|------|----------|
| 1. 安装 | `pip install pgvector`（或 `pip install pgvector[async]`） |  |
| 2. 创建扩展 | 在 PostgreSQL 中执行 `CREATE EXTENSION IF NOT EXISTS vector;` |  |
| 3. 定义向量列 | `CREATE TABLE items (id serial PRIMARY KEY, embedding vector(1536));` |  |
| 4. 插入向量 | 使用普通的 `INSERT`，Python 端传入 `pgvector.Vector` 实例 | ```python\nfrom pgvector.psycopg import Vector\ncur.execute("INSERT INTO items (embedding) VALUES (%s)", (Vector([0.1, 0.2, …]),))``` |
| 5. 向量检索 | `SELECT * FROM items ORDER BY embedding <-> %s LIMIT 5;` | ```python\ncur.execute("SELECT id FROM items ORDER BY embedding <-> %s LIMIT 5", (Vector(query_vec),))\nresults = cur.fetchall()``` |
| 6. 异步使用（可选） | `from pgvector.asyncpg import Vector` + `asyncpg` 连接池 | 同上，只需在 async 环境下 `await conn.execute(...)` |

**生产可用性**  
- **成熟度**：Medium。代码库已稳定、星数和最近更新表明社区活跃，适合原型、内部服务或对向量检索要求不极端的生产环境。  
- **依赖**：仅依赖 psycopg/asyncpg 与 pgvector 本身，升级成本低。  
- **风险点**：需自行审查许可证（PostgreSQL + BSD‑style），并在部署前进行安全扫描（尤其是数据库访问权限）。建议在正式生产前：  
  1. 验证向量维度、索引（`CREATE INDEX ON items USING ivfflat (embedding vector_cosine_ops);`）的性能。  
  2. 加入 CI 测试，确保兼容项目的 Python 版本与 PostgreSQL 版本。  
  3. 监控查询延迟和磁盘使用，防止向量数据量大幅增长导致性能下降。  

综上，pgvector‑python 能够让 Python 项目快速接入向量检索功能，适合作为原型或内部业务的实现方案；在做好依赖、权限和性能验证后，也可以安全投入到生产环境。

## 🧭 Practical evaluation

**Value:** pgvector/pgvector-python may be useful when its README and activity match a concrete workflow.

**Best use cases**

- Not enough metadata yet.

**Integration notes:** Needs manual inspection before adoption because integration signals are sparse in the discovered metadata.

**Production readiness:** Medium: useful for prototypes or internal workflows, with dependency and maintenance checks before production.

**Quality signals**

- 1503 GitHub stars
- 95 forks
- updated 2026-06-26
- primary language: Python

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 50/100 |
| stars | 68/100 |
| topics | 0/100 |
| outlook | 62/100 |
| quality | 63/100 |
| recency | 80/100 |
| adoption | 63/100 |
| production | 66/100 |
| usefulness | 42/100 |
| integration | 46/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 0/100 |

---

<sub>🔭 Discovered 2026-06-26 · [View on GitHub](https://github.com/pgvector/pgvector-python) · [← Back to Misc](./README.md)</sub>
