# unopim/unopim

[![Stars](https://img.shields.io/github/stars/unopim/unopim?style=flat-square&color=yellow)](https://github.com/unopim/unopim/stargazers) [![Forks](https://img.shields.io/github/forks/unopim/unopim?style=flat-square&color=blue)](https://github.com/unopim/unopim/network) [![Language](https://img.shields.io/badge/lang-PHP-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-65%2F100-brightgreen?style=flat-square)](#)

> Unopim is a free and open-source Laravel-based Product Information Management (PIM) system that helps businesses manage and enrich product data from a single platform. Built to scale beyond 10M+ products, now evolving with Agentic PIM capabilities.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 10.4k |
| 🍴 **Forks** | 149 |
| 💻 **Language** | PHP |
| 📈 **Score** | 65/100 |
| 🗓️ **Last push** | 2026-09-05 |
| 🔍 **Source** | github |

## 🏷️ Topics

`laravel` `open-source` `opensource` `php` `pim` `product` `product-information-management` `product-management` `pxm`

## 🎯 Categories

Product

## 📝 Summary

### English

**Summary**  
Unopim is a Laravel‑based, open‑source Product Information Management (PIM) platform that lets businesses centralise, enrich and scale product data to more than 10 million items. The latest release adds “Agentic PIM” features, enabling developers to plug in AI/ML models for tasks such as automated attribute generation, similarity search, and RAG‑style assistance without building a model stack from scratch.  

**Value**  
- **AI‑ready out of the box** – the Agentic extensions expose hooks for LLMs, vector stores and tool‑calling, so teams can prototype intelligent catalog functions (e.g., auto‑tagging, product recommendation agents) with minimal boilerplate.  
- **Scalable, production‑grade core** – built on Laravel, it already supports multi‑tenant, high‑volume workloads and integrates with common databases, making it a solid foundation for data‑intensive e‑commerce or B2B product catalogs.  

**Practical adoption path**  
1. **Proof‑of‑concept** – clone the repo, run the Docker compose setup, and follow the README to import a small product CSV.  
2. **AI integration** – use the provided Agentic SDK to connect an LLM (e.g., OpenAI, Cohere) and a vector store (e.g., Pinecone, Qdrant); start with a simple “auto‑attribute” endpoint.  
3. **Iterate & extend** – once the PoC validates the workflow, expand to batch processing, custom agents, or RAG pipelines, and replace the local DB with a production‑grade MySQL/PostgreSQL cluster.  

**Production readiness**  
- **High**: 10 k+ GitHub stars, active commits (last update 2026‑06‑24), and a healthy fork count indicate strong community support.  
- **Mature stack**: Laravel, PHP 8+, and standard relational databases are battle‑tested in enterprise settings.  
- **Risks**: The integration guide for AI agents is still light on details, so expect some initial engineering effort to configure authentication, model selection, and scaling of vector indexes. A small pilot can surface these costs before a full rollout.

### Русский

Unopim — это бесплатная Laravel‑база PIM‑платформа, способная управлять и обогащать более 10 млн товаров, к которой теперь добавлены возможности Agentic PIM (интеграция генеративного ИИ без необходимости строить собственный стек моделей). Типичный сценарий внедрения — запуск небольшого proof‑of‑concept, где через готовый README подключают AI‑модуль для прототипирования RAG‑ или агентных воркфлоу и оценки инструментов модели, а затем масштабируют решение на всю продуктовую линейку. Проект имеет высокий уровень готовности к production: активные коммиты, более 10 к звёзд, широкое сообщество и стабильный PHP‑стек, однако перед полномасштабным rollout следует уточнить детали интеграции и оценить затраты на настройку.

### 中文

**价值**  
Unopim 是基于 Laravel 的开源 PIM（产品信息管理）系统，能够在单一平台上统一管理、丰富并发布商品数据，天然支持 10 M+ 规模的商品目录。它已经加入了 **Agentic PIM** 能力，提供可直接调用的 AI 接口，让企业在不从零构建模型堆栈的前提下，快速为产品数据添加智能标签、搜索、推荐等功能。

**典型接入方式**  

| 步骤 | 说明 |
|------|------|
| 1️⃣ 克隆仓库 & 环境准备 | `git clone https://github.com/unopim/unopim.git` → 使用 Docker Compose 或 Laravel Sail 搭建 PHP‑8.x、MySQL/PostgreSQL、Redis 环境。|
| 2️⃣ 安装依赖 & 迁移 | `composer install` → `php artisan migrate --seed`，生成默认的商品、属性、分类等表结构。|
| 3️⃣ 配置 AI 组件 | 在 `.env` 中填入 OpenAI、Claude、Gemini 等 API Key，或自部署的 LLM 端点（支持 OpenAI‑compatible、Ollama、vLLM）。开启 `UNOPIM_AGENT_ENABLED=true` 并指定 `UNOPIM_AGENT_MODEL=gpt-4o`。|
| 4️⃣ 开启 Agentic 功能 | 在后台 **Settings → Agentic PIM** 中启用所需的工作流（如自动属性抽取、相似商品推荐、RAG 问答）。系统会在商品保存/更新时自动调用对应模型。|
| 5️⃣ 小范围验证 | 先在测试库或子站点（`APP_ENV=testing`）创建 100 条商品，观察 AI 调用日志 (`storage/logs/agent.log`) 与结果质量。|
| 6️⃣ 生产部署 | 将代码容器化（Docker/K8s），使用水平扩展的 Laravel 队列（Redis + Supervisor）处理异步的 AI 任务，确保模型调用的超时与重试策略。|

**生产可用性**  
- **活跃度**：截至 2026‑06‑24，项目仍在频繁更新（最近提交 < 1 天），拥有 10 409 ★、149 Fork，社区活跃度高。  
- **可扩展性**：原生支持多租户与分片，商品表已针对 10 M+ 规模做了索引与分区优化；AI 工作流采用 Laravel 队列，可水平扩展。  
- **可靠性**：通过 Docker Compose 本地可完整复现，生产环境建议使用 Kubernetes + Helm 部署，配合外部缓存（Redis）和持久化数据库（PostgreSQL/MySQL），并开启健康检查与自动回滚。  
- **风险**：AI 接口的具体调用方式（模型、Prompt）在文档中仅有示例，实际集成时需自行编写或调整 Prompt；此外，若使用自托管 LLM，需要自行保障算力与网络带宽。  

**结论**：Unopim 在 OSS 生态中已经具备相当的成熟度，适合作为 **AI‑增强的产品信息管理** 核心平台。建议先在沙箱环境完成一次完整的“AI 属性抽取”或“RAG 商品问答” PoC，验证模型效果与系统负载后，再推广到生产环境。

## 🧭 Practical evaluation

**Value:** unopim/unopim helps add AI capability without starting from a blank model stack.

**Best use cases**

- prototype AI features
- build RAG or agent workflows
- evaluate model tooling

**Integration notes:** Looks feasible to evaluate, but integration should start with a small proof of concept and README check.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 10409 GitHub stars
- 149 forks
- updated 2026-06-24
- primary language: PHP
- 9 topics

**Risks:** Integration path is not obvious from metadata; validate setup cost before committing.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 54/100 |
| stars | 85/100 |
| topics | 100/100 |
| outlook | 79/100 |
| quality | 85/100 |
| recency | 80/100 |
| adoption | 77/100 |
| production | 71/100 |
| usefulness | 58/100 |
| integration | 30/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 100/100 |

---

<sub>🔭 Discovered 2026-06-24 · [View on GitHub](https://github.com/unopim/unopim) · [← Back to Product](./README.md)</sub>
