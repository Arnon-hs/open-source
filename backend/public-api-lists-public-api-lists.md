# public-api-lists/public-api-lists

[![Stars](https://img.shields.io/github/stars/public-api-lists/public-api-lists?style=flat-square&color=yellow)](https://github.com/public-api-lists/public-api-lists/stargazers) [![Forks](https://img.shields.io/github/forks/public-api-lists/public-api-lists?style=flat-square&color=blue)](https://github.com/public-api-lists/public-api-lists/network) [![Language](https://img.shields.io/badge/lang-Unknown-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-78%2F100-brightgreen?style=flat-square)](#)

> A curated list of free public APIs across 48 categories — searchable, community-maintained, with a free JSON API.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 15k |
| 🍴 **Forks** | 1.6k |
| 💻 **Language** | Unknown |
| 📈 **Score** | 78/100 |
| 🗓️ **Last push** | 2026-09-05 |
| 🔍 **Source** | github |

## 🏷️ Topics

`api` `api-list` `apis` `awesome` `awesome-list` `beginner-friendly` `collection` `curated-list` `developer-resources` `developer-tools` `free-api` `hacktoberfest`

## 🎯 Categories

Backend · DevTools · Data

## 📝 Summary

### English

**Brief Summary (2‑3 sentences)**  
public‑api‑lists is a community‑maintained, searchable catalogue of free public APIs spanning 48 categories, exposed through a free JSON endpoint. With over 14 k stars and recent activity, it lets developers quickly discover and integrate ready‑made data or AI services without building a model stack from scratch. The project is well‑documented, actively forked, and suitable for a pilot integration or proof‑of‑concept.

**Value**  
- **Speed to market** – Developers can prototype AI‑enhanced features, Retrieval‑Augmented Generation (RAG) pipelines, or autonomous agents by pulling in ready‑made APIs instead of engineering data pipelines or training models.  
- **Breadth of coverage** – 48 curated categories (e.g., finance, health, NLP, geolocation) give a one‑stop source for diverse data and functionality, reducing the time spent searching disparate documentation.  
- **Community‑driven quality** – The list is continuously updated by contributors, ensuring new services appear quickly and stale entries are pruned.  

**Practical Adoption Path**  
1. **Explore the catalogue** – Use the searchable web UI or the public JSON API (`https://public-api-lists.com/api`) to locate APIs that match your use case.  
2. **Proof‑of‑concept** – Clone the repo, run the provided example scripts, and integrate a single API (e.g., a weather or sentiment‑analysis endpoint) into a sandboxed service.  
3. **Validate** – Verify response formats, rate limits, and any required API keys; update your internal API‑wrapper library accordingly.  
4. **Scale** – Add additional endpoints as needed, leveraging the same wrapper pattern; consider caching or fallback logic for reliability.  
5. **Production hardening** – Pin the version of the JSON list you consume (e.g., via a release tag), audit the licenses of the downstream APIs, and implement monitoring for availability and latency.  

**Production Readiness**  
- **Activity & Adoption** – 14 979 stars, 1 591 forks, recent commits (as of 2026‑07‑06), and a rich set of topics indicate a healthy, active community.  
- **Stability** – The JSON API is versioned and the repository includes a clear README, contribution guidelines, and CI checks, making it reliable for automated consumption.  
- **Risk considerations** – While no major metadata or security issues have been identified, a final review of the licenses of individual downstream APIs and a security audit of any API keys used is advisable.  
- **Overall** – The project meets the criteria for a serious pilot: strong community signals, clear documentation, and a low integration barrier, positioning it as a production‑ready OSS component for AI‑enabled applications.

### Русский

Резюме проекта public-api-lists/public-api-lists:

Проект представляет собой обновляемый список бесплатных публичных API по 48 категориям, предоставляемый в формате JSON. Он позволяет добавлять функции AI без создания новой модели стека, что делает его полезным инструментом для прототипирования и внедрения AI-технологий.

Проект готов к serious пилоту, поскольку имеет сильные показатели за последний период времени, включая 14 979 GitHub звезд и 1591 фк. Для внедрения проекта подойдет типовой сценарий: прототипирование AI-функций, создание РАГ или агентских потоков, оценка инструментов для моделирования.

### 中文

**项目简介（2‑3 句）**  
public-api-lists 是一个社区维护的免费公共 API 汇总库，覆盖 48 大类、近 2 万条 API，并提供可搜索的网页与 JSON 接口，帮助开发者快速发现并调用现成的服务。

**价值**  
- **即插即用**：无需自行搭建模型或数据源，直接通过公开 API 为产品添加 AI、数据、后端等功能。  
- **加速原型**：在原型阶段即可检索并调用合适的 API，快速验证 RAG、Agent、数据分析等业务场景。  
- **统一入口**：统一的 JSON 接口和分类标签，让多种 API 的发现、比较与集成变得低成本。

**典型接入方式**  
1. **读取 JSON 列表**：通过 `https://api.publicapis.org/entries`（或项目自带的 JSON 文件）获取完整 API 列表。  
2. **过滤搜索**：在本地或后端根据 `Category`、`Auth`、`HTTPS` 等字段过滤，找到目标 API。  
3. **调用具体 API**：按照对应 API 的文档发送 HTTP 请求，常见的请求库（axios、requests、fetch）均可直接使用。  
4. **示例代码**（Node.js）：

```js
const fetch = require('node-fetch');

async function getApis(category) {
  const res = await fetch('https://api.publicapis.org/entries');
  const data = await res.json();
  return data.entries.filter(e => e.Category === category);
}

// 示例：获取 AI/ML 类 API
getApis('AI/ML').then(console.log);
```

**生产可用性**  
- **活跃度高**：截至 2026‑07‑06，项目拥有 14,979 星、1,591 Fork，最近一次提交在当日，社区活跃。  
- **成熟度**：48 类目、完整的搜索与 JSON 接口，已被多个开源项目和商业原型引用，具备“可直接用于生产”的成熟度。  
- **风险点**：仍需对许可证（MIT/Apache 等）进行确认，审计依赖的第三方 API 的安全与合规性，并确保关键业务不依赖单一外部 API。  
- **推荐做法**：在正式上线前先做小范围 PoC，验证选定 API 的响应时效、错误率和费用（若有），随后在 CI/CD 中加入健康检查与降级方案。  

综上，public-api-lists 具备高可用的社区支持和丰富的资源，是在生产环境中快速集成外部功能的可靠 OSS 候选。

## 🧭 Practical evaluation

**Value:** public-api-lists/public-api-lists helps add AI capability without starting from a blank model stack.

**Best use cases**

- prototype AI features
- build RAG or agent workflows
- evaluate model tooling

**Integration notes:** Looks feasible to evaluate, but integration should start with a small proof of concept and README check.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 14979 GitHub stars
- 1591 forks
- updated 2026-07-06
- 20 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 80/100 |
| stars | 89/100 |
| topics | 100/100 |
| outlook | 84/100 |
| quality | 89/100 |
| recency | 80/100 |
| adoption | 86/100 |
| production | 77/100 |
| usefulness | 74/100 |
| integration | 62/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 300/100 |

---

<sub>🔭 Discovered 2026-07-06 · [View on GitHub](https://github.com/public-api-lists/public-api-lists) · [← Back to Backend](./README.md)</sub>
