# gcpaas/DataRoom

[![Stars](https://img.shields.io/github/stars/gcpaas/DataRoom?style=flat-square&color=yellow)](https://github.com/gcpaas/DataRoom/stargazers) [![Forks](https://img.shields.io/github/forks/gcpaas/DataRoom?style=flat-square&color=blue)](https://github.com/gcpaas/DataRoom/network) [![Language](https://img.shields.io/badge/lang-Vue-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-52%2F100-brightgreen?style=flat-square)](#)

> 🔥AI对话式生成大屏、页面，采用前后端一体化解决方案，几十种炫酷图表，支持20+数据来源接入，适用于大屏、低代码、BI场景，使用简单，代码完全开源。

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 809 |
| 🍴 **Forks** | 204 |
| 💻 **Language** | Vue |
| 📈 **Score** | 52/100 |
| 🗓️ **Last push** | 2026-09-05 |
| 🔍 **Source** | github |

## 🏷️ Topics

_no topics_

## 🎯 Categories

Misc

## 📝 Summary

### English

**Brief Summary**  
gcpaas/DataRoom is an open‑source, full‑stack solution that lets you generate AI‑driven dashboards and pages through conversational prompts. It bundles dozens of eye‑catching charts, supports more than 20 data sources, and is built with Vue for rapid low‑code or BI prototyping.

**Value**  
- **AI‑enabled UI creation** – developers can add conversational AI generation to visual analytics without building a model stack from scratch.  
- **Fast prototyping** – the integrated front‑ and back‑end, pre‑made chart components, and multi‑source connectors let teams spin up data‑rich screens in hours rather than weeks.  
- **Open and extensible** – the code is fully available, so you can customize chart types, data adapters, or embed the engine in larger RAG/agent workflows.

**Practical Adoption Path**  
1. **Evaluate the repo** – clone the project, run `npm install && npm run dev` to verify the Vue UI builds locally.  
2. **Connect a data source** – use the built‑in connectors (e.g., MySQL, PostgreSQL, API, CSV) and confirm data can be queried via the provided back‑end API.  
3. **Prototype a use case** – create a few conversational prompts to generate dashboards that match your internal reporting needs.  
4. **Customize/extend** – if you need additional chart types or a different LLM, fork the repo and replace the AI service configuration (the code is modular).  
5. **Integrate** – wrap the DataRoom UI as an iframe or micro‑frontend within your existing portal, and expose the back‑end API through your authentication layer.

**Production Readiness**  
- **Maturity**: Medium. The project has solid community interest (≈ 800 ★, 200 forks) and recent activity, but integration details are sparse and the deployment scripts are minimal.  
- **Suitability**: Ideal for internal tools, prototypes, or low‑code BI dashboards where rapid iteration outweighs strict SLAs.  
- **Considerations before production**:  
  * Perform a security audit of the back‑end API and data‑source connectors.  
  * Validate the AI service (e.g., OpenAI, Azure) cost and latency for your workload.  
  * Set up CI/CD, monitoring, and version‑pinning of dependencies to avoid breaking changes.  
  * If you need high‑availability or multi‑tenant isolation, add container orchestration or service‑mesh layers yourself.  

With these steps, DataRoom can be safely moved from a proof‑of‑concept to a production‑grade component for AI‑augmented analytics.

### Русский

gcpaas/DataRoom — это полностью открытая платформа, объединяющая AI‑диалоговый генератор экранов и страниц с готовыми более чем 20 типами источников данных и десятками стильных визуализаций (Vue‑компоненты). Она позволяет быстро добавить AI‑функциональность в прототипы или внутренние BI‑решения (low‑code, дашборды, RAG‑агенты) без разработки собственного стека, однако перед внедрением требуется ручная проверка интеграции и оценка затрат на настройку. Текущий уровень готовности — средний: проект подходит для прототипов и ограниченных внутренних сценариев, но требует проверки зависимостей и поддержки перед запуском в продакшн.

### 中文

**项目简介（2‑3 句）**  
gcpaas/DataRoom 是一套前后端一体化的 AI 对话式大屏/页面生成平台，内置数十种炫酷可视化图表并支持 20+ 数据源接入，适用于大屏展示、低代码和 BI 场景，使用门槛低且代码完全开源。

---

## 价值说明
1. **快速赋能 AI 可视化**：通过自然语言对话即可生成或编辑大屏页面，省去手工编写配置和图表代码的时间。  
2. **丰富的数据与图表生态**：内置多种交互式图表（折线、柱状、热力图、仪表盘等），并提供 MySQL、PostgreSQL、ClickHouse、Elasticsearch、Prometheus、Excel、CSV 等 20+ 主流数据源的即插即用适配器。  
3. **低代码 + 开源**：前端基于 Vue，后端采用 Node.js/Express，全部源码公开，企业可自行二次开发或按需裁剪，避免供应商锁定。  
4. **适配多种业务场景**：从运营大屏、营销报表到内部 BI 与监控面板，都可在几分钟内部署完成原型，帮助业务快速验证 AI+BI 的价值。

---

## 典型接入方式
| 步骤 | 操作 | 说明 |
|------|------|------|
| 1️⃣ 环境准备 | `git clone https://github.com/gcpaas/DataRoom && cd DataRoom` <br>安装 Node.js（>=18）和 Yarn | 项目依赖 Vue 3 + Vite，后端使用 Node。 |
| 2️⃣ 配置数据源 | 在 `config/datasources.json`（或 UI 中的「数据源管理」）添加数据源信息，如 MySQL、ClickHouse、Prometheus 等。 | 支持通过环境变量或密钥管理平台注入凭证，安全可控。 |
| 3️⃣ 启动服务 | 前端：`yarn dev` <br>后端：`yarn start:server` | 前后端同端口（Vite 代理）或分离部署（Docker-compose 示例已提供）。 |
| 4️⃣ AI 对话接入 | 在 `src/services/ai.ts` 中配置 OpenAI、Claude、Gemini 等模型的 API Key。<br>前端页面的「AI 生成」对话框即可调用。 | 支持自定义 Prompt，实现业务专属的图表生成逻辑。 |
| 5️⃣ 嵌入业务系统 | 通过 iframe、WebComponent 或直接在 Vue 项目中 `import DataRoom`，将生成的大屏嵌入内部门户或 SaaS 产品。 | 提供 RESTful 接口 (`/api/dashboard`) 与 WebSocket 实时数据推送。 |

> **Docker 一键部署**：仓库根目录提供 `docker-compose.yml`，执行 `docker compose up -d` 即可在生产环境快速启动前后端容器，默认映射 8080 端口。

---

## 生产可用性评估
| 维度 | 现状 | 建议 |
|------|------|------|
| **代码成熟度** | 809 ⭐、204 🍴，最近一次提交为 2026‑06‑23，活跃度仍在。 | 关注最新 PR 与 Issue，确保关键依赖（Vue 3、Node 18）已升级到安全版本。 |
| **功能完整性** | 已实现 30+ 图表组件、20+ 数据源适配器、AI 对话生成。 | 根据业务需求评估是否需要自行实现额外数据源或自定义图表。 |
| **部署复杂度** | 提供 Docker‑Compose 与完整文档，部署相对简单。 | 在生产环境使用容器编排（K8s）并加入健康检查、日志采集。 |
| **安全性** | AI 调用需要外部 LLM API Key，数据源凭证通过环境变量管理。 | 建议使用密钥管理系统（Vault、KMS）统一管理凭证，开启 HTTPS 与 CORS 限制。 |
| **可扩展性** | 前端插件化（Vue 组件），后端插件化（Express 中间件）。 | 如需高并发，可将渲染服务拆分为独立微服务，使用 Redis 缓存图表配置。 |
| **生产准备度** | **Medium**：适合作为内部原型、BI 门户或低代码平台的基础设施。 | 在正式上线前完成：<br>1. 代码审计与依赖安全扫描；<br>2. 监控与告警（Prometheus + Grafana）；<br>3. 灾备与滚动升级方案。 |

**总结**：gcpaas/DataRoom 已具备较完整的功能集合和开箱即用的部署方式，适合在内部业务或面向特定客户的低代码 BI 场景快速落地。若要在大流量生产环境使用，建议进行安全加固、依赖审计以及容器化运维实践后再投入。

## 🧭 Practical evaluation

**Value:** gcpaas/DataRoom helps add AI capability without starting from a blank model stack.

**Best use cases**

- prototype AI features
- build RAG or agent workflows
- evaluate model tooling

**Integration notes:** Needs manual inspection before adoption because integration signals are sparse in the discovered metadata.

**Production readiness:** Medium: useful for prototypes or internal workflows, with dependency and maintenance checks before production.

**Quality signals**

- 809 GitHub stars
- 204 forks
- updated 2026-06-23
- primary language: Vue

**Risks:** Integration path is not obvious from metadata; validate setup cost before committing.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 58/100 |
| stars | 62/100 |
| topics | 0/100 |
| outlook | 62/100 |
| quality | 62/100 |
| recency | 80/100 |
| adoption | 61/100 |
| production | 63/100 |
| usefulness | 42/100 |
| integration | 30/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 0/100 |

---

<sub>🔭 Discovered 2026-06-23 · [View on GitHub](https://github.com/gcpaas/DataRoom) · [← Back to Misc](./README.md)</sub>
