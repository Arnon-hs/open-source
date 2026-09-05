# TanStack/tanstack.com

[![Stars](https://img.shields.io/github/stars/TanStack/tanstack.com?style=flat-square&color=yellow)](https://github.com/TanStack/tanstack.com/stargazers) [![Forks](https://img.shields.io/github/forks/TanStack/tanstack.com?style=flat-square&color=blue)](https://github.com/TanStack/tanstack.com/network) [![Language](https://img.shields.io/badge/lang-TypeScript-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-56%2F100-brightgreen?style=flat-square)](#)

> The marketing and docs site for all TanStack projects

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 1k |
| 🍴 **Forks** | 367 |
| 💻 **Language** | TypeScript |
| 📈 **Score** | 56/100 |
| 🗓️ **Last push** | 2026-09-05 |
| 🔍 **Source** | github |

## 🏷️ Topics

_no topics_

## 🎯 Categories

Marketing

## 📝 Summary

### English

Here's a brief summary of the TanStack/tanstack.com project:

TanStack/tanstack.com is an open-source marketing and documentation site for various TanStack projects, offering a valuable resource for developers looking for information on these projects. To adopt this project, developers should manually inspect the integration before use, as the integration signals are sparse in the metadata. In terms of production readiness, TanStack/tanstack.com is suitable for prototypes or internal workflows but requires further dependency and maintenance checks before deployment in a production environment.

### Русский

**Краткое резюме**  
TanStack/tanstack.com — это открытый маркетинговый и документационный сайт, объединяющий все проекты TanStack. Он подходит для быстрой развертки внутренней или клиентской портальной страницы, где требуется единый стиль и автогенерация документации для React‑Query, TanStack Table и др.; при этом требуется ручная проверка совместимости и настройка CI/CD, так как автоматических интеграционных сигналов мало. Готовность к production — средний уровень: проект достаточно популярен (1026⭐, 367 форков) и активно поддерживается, но перед выпуском в продакшн следует оценить лицензию, безопасность зависимостей и наличие ответственных мейнтейнеров.

### 中文

**项目简介**  
TanStack /tanstack.com 是 TanStack 系列库（React‑Query、React‑Table、React‑Location 等）的官方营销与文档站点，使用 TypeScript + Vite/Next.js 构建，负责统一展示产品特性、使用指南和案例。

**价值**  
- **统一入口**：为所有 TanStack 项目提供统一的品牌形象和文档入口，降低用户查找成本。  
- **即时更新**：文档与代码同步发布，确保新特性、API 变更能够第一时间在站点上呈现。  
- **SEO 与营销**：通过静态站点生成和优化的 meta 信息提升搜索可见度，帮助社区增长和生态推广。

**典型接入方式**  
1. **源码引用**：在内部项目的文档系统中直接 fork 仓库，按需修改站点主题或导航结构。  
2. **API 数据**：利用站点提供的公开 JSON/MDX 文档（如 `docs/**/*.mdx`），通过自建文档生成脚本或组件库进行二次渲染。  
3. **CI/CD 集成**：在 CI 流程中运行 `npm run build && npm run export`，将生成的静态文件部署到 Vercel、Netlify 或自建 CDN，实现自动化发布。  

**生产可用性**  
- **成熟度**：已有 1 k+ ★、近 400 fork，且最近一次提交在 2026‑06‑29，活跃度良好。  
- **适用场景**：适合作为内部或面向社区的文档门户、营销站点，亦可在原型阶段快速搭建展示页面。  
- **风险与注意事项**：  
  - 需自行审查许可证（MIT）与依赖的安全性，尤其是构建工具链（Vite/Next.js）和第三方插件。  
  - 站点本身不提供后端服务，若需要搜索、评论等交互功能，需要自行集成相应 SaaS 或自建服务。  
  - 维护成本主要在主题自定义和文档同步上，建议在生产环境使用前进行一次完整的 CI/CD 与安全审计。  

总体而言，tanstack.com 具备中等到高的生产可用性，适合作为文档/营销站点的基础框架，只要在接入前完成依赖检查和安全审计即可投入正式使用。

## 🧭 Practical evaluation

**Value:** TanStack/tanstack.com may be useful when its README and activity match a concrete workflow.

**Best use cases**

- Not enough metadata yet.

**Integration notes:** Needs manual inspection before adoption because integration signals are sparse in the discovered metadata.

**Production readiness:** Medium: useful for prototypes or internal workflows, with dependency and maintenance checks before production.

**Quality signals**

- 1026 GitHub stars
- 367 forks
- updated 2026-06-29
- primary language: TypeScript

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 64/100 |
| stars | 64/100 |
| topics | 0/100 |
| outlook | 62/100 |
| quality | 64/100 |
| recency | 80/100 |
| adoption | 64/100 |
| production | 66/100 |
| usefulness | 42/100 |
| integration | 46/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 100/100 |

---

<sub>🔭 Discovered 2026-06-29 · [View on GitHub](https://github.com/TanStack/tanstack.com) · [← Back to Marketing](./README.md)</sub>
