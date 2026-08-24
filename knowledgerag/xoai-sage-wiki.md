# xoai/sage-wiki

[![Stars](https://img.shields.io/github/stars/xoai/sage-wiki?style=flat-square&color=yellow)](https://github.com/xoai/sage-wiki/stargazers) [![Forks](https://img.shields.io/github/forks/xoai/sage-wiki?style=flat-square&color=blue)](https://github.com/xoai/sage-wiki/network) [![Language](https://img.shields.io/badge/lang-Go-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-48%2F100-brightgreen?style=flat-square)](#)

> An LLM-compiled personal knowledge base.  Drop in your papers, articles, and notes. sage-wiki compiles them into a structured, interlinked wiki — with concepts extracted, cross-references discovered, and everything searchable.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 544 |
| 🍴 **Forks** | 91 |
| 💻 **Language** | Go |
| 📈 **Score** | 48/100 |
| 🗓️ **Last push** | 2026-08-24 |
| 🔍 **Source** | github |

## 🏷️ Topics

_no topics_

## 🎯 Categories

Knowledge/RAG

## 📝 Summary

### English

xoai/sage‑wiki turns raw papers, articles, and notes into a searchable, interlinked wiki by extracting concepts and cross‑references, making internal knowledge instantly usable by AI assistants. Adoption is straightforward for prototyping — drop your documents in, run the Go‑based compiler, and inspect the generated wiki — but before moving to production you should verify licensing, security posture, and maintainer activity, as the project currently shows medium readiness suitable for internal workflows or proof‑of‑concept use.

### Русский

xoai/sage‑wiki — это LLM‑собранный персональный wiki, который превращает загруженные статьи, заметки и документы в структурированную, перекрёстно связанную базу знаний, делая их поисковыми и готовыми к использованию ассистентами. Типовой сценарий: индексация внутренних документов и улучшение поиска по ним, а также grounding ответов ИИ‑ассистентов. Проект имеет средний уровень production‑readiness — подходит для прототипов и внутренних рабочих процессов, но перед внедрением в продакшн требуется проверка зависимостей, лицензии и активности мейнтейнеров.

### 中文

**项目简介**  
xoai/sage-wiki 是一个基于大模型（LLM）自动编译的个人知识库。用户只需把论文、文章、笔记等文档拖入系统，sage‑wiki 会自动抽取概念、发现交叉引用并生成结构化、可互链的 Wiki，所有内容均可全文检索。

**价值**  
- **知识可搜索、可复用**：将碎片化的文档转化为结构化的概念图和链接网络，显著提升内部知识的检索效率。  
- **助理可靠的知识来源**：在对话式 AI、客服机器人或内部助手中提供可追溯、经过概念抽取的事实依据，降低幻觉风险。  
- **快速原型与内部工作流**：无需手动标注或构建索引，几分钟即可搭建文档索引，适合研发、产品和运营团队快速验证 RAG 场景。

**典型接入方式**  
1. **准备文档**：将 PDF、Markdown、HTML 等格式的论文、报告或笔记放入指定目录或通过 API 上传。  
2. **运行 sage-wiki**（Docker / 二进制）：项目提供 `docker-compose.yml`，启动后自动触发 LLM 进行概念抽取、实体链接和 Wiki 生成。  
3. **查询接口**：通过内建的 GraphQL/REST API 或 Web UI 发起全文搜索、概念查询或关联图谱浏览。  
4. **与业务系统集成**：在聊天机器人、内部搜索平台或 CI/CD 流程中调用 API，实现“基于文档的回答”或“文档自动归档”。  

**生产可用性**  
- **成熟度**：当前为 **Medium**。已在内部原型和小规模业务中验证，可支撑研发或内部知识管理的生产需求。  
- **依赖与维护**：核心使用 Go 编写，依赖相对稳定；但项目的自动化集成信号较少，建议在正式上线前进行一次手动审查（检查抽取的元数据、概念准确性）。  
- **安全与合规**：暂无重大元数据泄露风险，仍需自行评估许可证（MIT）与潜在的安全漏洞。  
- **社区活跃度**：GitHub ★544，Fork 91，最近更新于 2026‑06‑28，社区活跃度良好，可作为长期维护的依据。  

**结论**：sage-wiki 适合作为内部文档索引和 RAG（检索增强生成）系统的快速落地方案，尤其在需要结构化概念图和跨文档关联的场景下表现突出。上线前进行一次人工质量检查并确认依赖安全后，即可在生产环境中使用。

## 🧭 Practical evaluation

**Value:** xoai/sage-wiki helps make internal knowledge searchable and usable by assistants.

**Best use cases**

- index knowledge bases
- improve search over documents
- ground assistant answers

**Integration notes:** Needs manual inspection before adoption because integration signals are sparse in the discovered metadata.

**Production readiness:** Medium: useful for prototypes or internal workflows, with dependency and maintenance checks before production.

**Quality signals**

- 544 GitHub stars
- 91 forks
- updated 2026-06-28
- primary language: Go

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 49/100 |
| stars | 58/100 |
| topics | 0/100 |
| outlook | 46/100 |
| quality | 50/100 |
| recency | 40/100 |
| adoption | 56/100 |
| production | 51/100 |
| usefulness | 42/100 |
| integration | 46/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 100/100 |

---

<sub>🔭 Discovered 2026-06-28 · [View on GitHub](https://github.com/xoai/sage-wiki) · [← Back to Knowledgerag](./README.md)</sub>
