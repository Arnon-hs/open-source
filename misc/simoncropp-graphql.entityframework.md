# SimonCropp/GraphQL.EntityFramework

[![Stars](https://img.shields.io/github/stars/SimonCropp/GraphQL.EntityFramework?style=flat-square&color=yellow)](https://github.com/SimonCropp/GraphQL.EntityFramework/stargazers) [![Forks](https://img.shields.io/github/forks/SimonCropp/GraphQL.EntityFramework?style=flat-square&color=blue)](https://github.com/SimonCropp/GraphQL.EntityFramework/network) [![Language](https://img.shields.io/badge/lang-C%23-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-54%2F100-brightgreen?style=flat-square)](#)

> Adds EntityFramework Core IQueryable support to GraphQL

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 396 |
| 🍴 **Forks** | 62 |
| 💻 **Language** | C# |
| 📈 **Score** | 54/100 |
| 🗓️ **Last push** | 2026-09-05 |
| 🔍 **Source** | github |

## 🏷️ Topics

_no topics_

## 🎯 Categories

Misc

## 📝 Summary

### English

SimonCropp/GraphQL.EntityFramework adds native IQueryable support from Entity Framework Core to GraphQL queries, letting developers expose EF data sources directly through GraphQL without manual resolvers. Adoption requires reviewing the sparse integration documentation and performing a manual setup check, but the project’s steady activity (≈400 stars, recent 2026 update) indicates it is usable for prototypes or internal tools. For production use, verify dependency compatibility and maintenance practices before committing to ensure medium‑level readiness.

### Русский

GraphQL.EntityFramework добавляет поддержку IQueryable из Entity Framework Core в GraphQL, позволяя напрямую использовать LINQ‑запросы в резолверах и упрощая доступ к данным. Типовой сценарий — подключение пакета к ASP.NET Core‑приложению с EF Core и настройка GraphQL‑схемы так, чтобы поля резолверов возвращали IQueryable, что минимизирует количество обращений к БД. Проект имеет средний уровень готовности к production: подходит для прототипов и внутренних workflows, но перед внедрением в продакшн рекомендуется проверить зависимости, интеграционные детали и поддержать актуальность (последнее обновление — июль 2026).

### 中文

SimonCropp/GraphQL.EntityFramework 为 GraphQL 添加了对 Entity Framework Core IQueryable 的直接支持，使得查询层能够自然地映射到 EF Core 的延迟加载和分页功能，从而简化数据访问代码。典型的接入方式是在 GraphQL schema 中使用其提供的 `GraphQL.EntityFramework` 扩展（如 `AddDbContext`、`UseProjection` 等），将 EF Core 的 `DbContext` 注入到解析器中，直接返回 `IQueryable<T>` 让 GraphQL 自行执行过滤、排序和分页。该项目目前处于中等成熟度，适用于原型或内部工作流；在生产环境使用前建议进行依赖兼容性和维护频率的检查，并手动验证集成成本。

## 🧭 Practical evaluation

**Value:** SimonCropp/GraphQL.EntityFramework may be useful when its README and activity match a concrete workflow.

**Best use cases**

- Not enough metadata yet.

**Integration notes:** Needs manual inspection before adoption because integration signals are sparse in the discovered metadata.

**Production readiness:** Medium: useful for prototypes or internal workflows, with dependency and maintenance checks before production.

**Quality signals**

- 396 GitHub stars
- 62 forks
- updated 2026-07-25
- primary language: C#

**Risks:** Integration path is not obvious from metadata; validate setup cost before committing.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 45/100 |
| stars | 55/100 |
| topics | 0/100 |
| outlook | 63/100 |
| quality | 59/100 |
| recency | 80/100 |
| adoption | 52/100 |
| production | 62/100 |
| usefulness | 58/100 |
| integration | 30/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 0/100 |

---

<sub>🔭 Discovered 2026-07-25 · [View on GitHub](https://github.com/SimonCropp/GraphQL.EntityFramework) · [← Back to Misc](./README.md)</sub>
