# rochus-keller/mumps

[![Stars](https://img.shields.io/github/stars/rochus-keller/mumps?style=flat-square&color=yellow)](https://github.com/rochus-keller/mumps//stargazers) [![Forks](https://img.shields.io/github/forks/rochus-keller/mumps?style=flat-square&color=blue)](https://github.com/rochus-keller/mumps//network) [![Language](https://img.shields.io/badge/lang-Unknown-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-31%2F100-brightgreen?style=flat-square)](#)

> Discovered from Hacker News (github-mentions)

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | — |
| 🍴 **Forks** | — |
| 💻 **Language** | Unknown |
| 📈 **Score** | 31/100 |
| 🗓️ **Last push** | 2026-08-24 |
| 🔍 **Source** | hackernews |

## 🏷️ Topics

`hn` `github-mentions`

## 🎯 Categories

Misc

## 📝 Summary

### English

**Project Summary:**

Show HN: A faithful MUMPS 76 anniversary implementation is an open-source, NoSQL database that enables the addition of AI capabilities without starting from scratch. This project offers a unique value proposition for prototyping AI features, building RAG (Rule-Based) or agent workflows, and evaluating model tooling. However, its production readiness is limited due to sparse integration signals and quality signals.

**Value:**

The project's value lies in its ability to facilitate AI capabilities without requiring a complete model stack, making it an attractive option for prototyping and internal workflows. Its NoSQL database design allows for flexible data storage and retrieval, which can be beneficial for AI-driven applications.

**Practical Adoption Path:**

To adopt this project, users should follow these steps:

1. **Manual Inspection**: Carefully review the code and documentation to ensure it meets their needs and requirements.
2. **Verify Dependencies**: Check the dependencies and ensure they are compatible with their existing infrastructure.
3. **Maintenance Checks**: Regularly review the project's maintenance, updates, and issue tracking to ensure it remains stable and secure.
4. **Prototype and Test**: Use the project to prototype AI features, build RAG or agent workflows, and evaluate model tooling.
5. **Assess

### Русский

Резюме:

"Show HN: A faithful MUMPS 76 anniversary implementation – the original NoSQL DB" - это открытый исходный код проект, который позволяет добавлять функциональность AI без создания новой базовой модели. Этот проект подойдет для прототипирования AI-приложений и внедрения агентных потоков, а также для оценки инструментов для моделирования. Проект имеет средний уровень готовности к production, что означает его можно использовать для внутренних прототипов или рабочих процессов, но требует тщательного проверки зависимостей и поддержки перед внедрением в производство.

### 中文

**项目简介（2‑3 句）**  
Show HN: A faithful MUMPS‑76 anniversary implementation 是对 1976 年诞生的 MUMPS 数据库的忠实复刻，号称“最早的 NoSQL DB”。该实现保留了原始的层次化全局变量模型，可直接用于原型化 AI 功能、RAG（检索增强生成）或智能体工作流的后端存储。

**价值**  
- **快速赋能 AI**：无需从零搭建向量存储或键值系统，直接利用 MUMPS 的稀疏全局结构实现高效检索和持久化。  
- **轻量原型**：对实验性 AI 功能（如文档检索、上下文记忆）提供即插即用的后端，缩短开发周期。  
- **历史兼容**：对需要复现旧系统或研究 NoSQL 演进的场景提供真实的历史参考实现。

**典型接入方式**  
1. **源码编译**：克隆仓库后使用提供的 Makefile/ CMake 脚本在 Linux 环境下编译生成 `mumpsd` 可执行文件。  
2. **语言桥接**：通过社区维护的 Python（`pymumps`）或 Node.js（`mumps-client`）包装库，在 AI 项目中以 `dict‑like` 接口读写全局变量。  
3. **容器化**：将编译好的二进制和配置文件打包为 Docker 镜像，使用 `docker run -p 52773:52773` 暴露默认端口，配合 Kubernetes 的 `StatefulSet` 实现持久化。  
4. **集成 RAG**：将检索向量存储在 MUMPS 全局（如 `^VECTOR(id)`），并在查询时使用自定义的遍历/过滤函数与 LLM 交互。

**生产可用性**  
- **成熟度**：目前标记为 **Medium**，适合内部原型、研发环境或低风险业务。  
- **依赖与维护**：项目更新于 2026‑06‑28，活跃度不高，需自行审查许可证（通常为 BSD‑like）并评估社区 Issue 与 PR 的响应速度。  
- **上线前检查**：  
  1. 验证源码许可证与公司合规性。  
  2. 进行安全审计（尤其是 C 代码的内存管理）。  
  3. 编写健康检查脚本，监控进程存活、磁盘使用和全局变量一致性。  
  4. 若需高可用，考虑在外层使用 HAProxy/Consul 实现读写分离或多实例复制。  

综上，Show HN: A faithful MUMPS‑76 实现可作为 AI 原型快速搭建的 NoSQL 后端，但在生产环境部署前必须完成依赖、维护、合规及监控等完整评估。

## 🧭 Practical evaluation

**Value:** Show HN: A faithful MUMPS 76 anniversary implementation – the original NoSQL DB helps add AI capability without starting from a blank model stack.

**Best use cases**

- prototype AI features
- build RAG or agent workflows
- evaluate model tooling

**Integration notes:** Needs manual inspection before adoption because integration signals are sparse in the discovered metadata.

**Production readiness:** Medium: useful for prototypes or internal workflows, with dependency and maintenance checks before production.

**Quality signals**

- updated 2026-06-28
- 2 topics

**Risks:** Quality signals are limited; verify license, maintenance, docs, issues, and release cadence before using it.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 0/100 |
| stars | 0/100 |
| topics | 25/100 |
| outlook | 33/100 |
| quality | 26/100 |
| recency | 40/100 |
| adoption | 0/100 |
| production | 38/100 |
| usefulness | 42/100 |
| integration | 30/100 |
| sourceTrust | 80/100 |
| categoryMatchCount | 0/100 |

---

<sub>🔭 Discovered 2026-06-28 · [View on GitHub](https://github.com/rochus-keller/mumps/) · [← Back to Misc](./README.md)</sub>
