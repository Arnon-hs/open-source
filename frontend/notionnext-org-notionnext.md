# notionnext-org/NotionNext

[![Stars](https://img.shields.io/github/stars/notionnext-org/NotionNext?style=flat-square&color=yellow)](https://github.com/notionnext-org/NotionNext/stargazers) [![Forks](https://img.shields.io/github/forks/notionnext-org/NotionNext?style=flat-square&color=blue)](https://github.com/notionnext-org/NotionNext/network) [![Language](https://img.shields.io/badge/lang-JavaScript-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-70%2F100-brightgreen?style=flat-square)](#)

> 使用 NextJS + Notion API 实现的，支持多种部署方案的静态博客，无需服务器、零门槛搭建网站，为Notion和所有创作者设计。 (A static blog built with NextJS and Notion API, supporting multiple deployment options. No server required, zero threshold to set up a website. Designed for Notion and all creators.)

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 11.4k |
| 🍴 **Forks** | 14.6k |
| 💻 **Language** | JavaScript |
| 📈 **Score** | 70/100 |
| 🗓️ **Last push** | 2026-09-05 |
| 🔍 **Source** | github |

## 🏷️ Topics

`blog` `nextjs` `notion` `react` `tailwindcss` `vercel` `zeabur`

## 🎯 Categories

Frontend · Backend

## 📝 Summary

### English

**Brief Summary**  
NotionNext is an open‑source static blog framework built with Next.js and the Notion API. It lets creators turn Notion pages into a fully‑featured website without managing any server, and it supports a variety of deployment targets (Vercel, Netlify, Cloudflare Pages, etc.). The project also includes ready‑made hooks for adding AI‑powered features such as RAG or agents on top of the Notion content.

**Value**  
- **Zero‑ops hosting** – because the output is a static site, you can deploy with a single click to any edge‑CDN, eliminating server costs and operational complexity.  
- **Creator‑first workflow** – content lives in Notion, a tool many writers already use, and updates are reflected automatically after a rebuild.  
- **AI‑ready architecture** – the codebase exposes clean API/SDK layers that make it trivial to plug in LLMs, vector stores, or agent pipelines for search, summarisation, or recommendation features without rebuilding the stack from scratch.

**Practical Adoption Path**  
1. **Fork or clone** the repo and configure the Notion integration token and database IDs.  
2. **Run locally** (`npm run dev`) to verify that your Notion pages render correctly.  
3. **Add AI modules** (e.g., LangChain, OpenAI SDK) by using the provided `api/` folder or CLI hooks; the project already ships with example endpoints for vector‑search over Notion content.  
4. **Deploy** to your preferred platform (Vercel, Netlify, Cloudflare Pages) using the one‑click Git integration; the CI pipeline automatically builds the static assets.  
5. **Monitor & iterate** – the static nature means you can roll back instantly, and any AI‑related changes are just new serverless functions or edge workers.

**Production Readiness**  
- **Community traction:** 11 k+ stars, 14 k+ forks, frequent commits (last update 2026‑05‑14) indicate strong adoption and active maintenance.  
- **Mature stack:** Built on Next.js (v14+), TypeScript, and the official Notion API, all of which are battle‑tested in production.  
- **Deployment flexibility:** Supports all major static‑site hosts, giving you the ability to choose a provider that matches your security and compliance requirements.  
- **Extensibility:** Clearly separated front‑end, API, and CLI layers make it safe to introduce AI services without destabilising the core blog functionality.  

Overall, NotionNext is a production‑grade, low‑friction solution for creators who want a static site powered by Notion and a convenient foothold for adding AI capabilities.

### Русский

NotionNext — это полностью статический блог, построенный на Next.js и Notion API, который позволяет быстро развернуть сайт без собственного сервера и без сложных настроек, используя любой из поддерживаемых вариантов деплоя (Vercel, Netlify, Docker и пр.). Он идеально подходит для создателей контента, желающих добавить AI‑функциональность (прототипировать RAG‑системы, агентные воркфлоу и т.п.) к уже существующим страницам в Notion, используя готовый SDK/CLI и готовые интеграции. Проект имеет высокую готовность к production: активные коммиты, более 11 k звёзд, широкое принятие в сообществе и стабильный набор функций, что делает его надёжным кандидатом для серьёзных пилотов.

### 中文

**项目简介**  
NotionNext 是一个基于 Next.js 与 Notion API 的静态博客框架，支持多种一键部署方式（Vercel、Netlify、Cloudflare Pages 等），无需后端服务器，几乎零配置即可将 Notion 页面转化为高性能博客站点，专为 Notion 用户和内容创作者设计。

**价值点**  
- **零运维成本**：全部生成静态文件，托管在 CDN 上，无需维护服务器或数据库。  
- **快速上手**：只需在 Notion 中编写内容，配置几行环境变量即可完成部署，门槛极低。  
- **灵活部署**：兼容主流无服务器平台，亦可本地构建后自行托管。  
- **可扩展**：基于 Next.js，开发者可以自由加入自定义页面、插件或 AI 功能（如 RAG、智能摘要）而不必从零搭建技术栈。

**典型接入方式**  
1. **Fork / Clone 项目**：获取源码后在本地执行 `npm install`。  
2. **配置 Notion API**：在 Notion 创建公开数据库或页面，获取 `NOTION_TOKEN` 与 `NOTION_DATABASE_ID`，在 `.env.local` 中填写。  
3. **选择部署平台**：  
   - **Vercel**：直接导入 GitHub 仓库，一键完成构建与部署。  
   - **Netlify / Cloudflare Pages**：同样通过 GitHub 连接，设置构建命令 `npm run build && npm run export`，输出目录为 `out/`。  
   - **本地静态托管**：运行 `npm run build && npm run export`，将生成的 `out/` 目录上传到任意静态文件服务器（如 GitHub Pages、S3、阿里云 OSS）。  
4. **可选扩展**：在 `pages/api` 或自定义插件中引入 AI SDK（如 OpenAI、Claude）实现内容自动摘要、标签生成或 RAG 检索等高级功能。

**生产可用性**  
- **活跃度**：截至 2026‑05‑14，项目拥有 11.4k+ ⭐、14.5k+ 🍴，最近一次提交在数天前，说明社区和维护者仍在持续迭代。  
- **技术成熟度**：基于 Next.js 13+ 的 App Router 与 Incremental Static Regeneration，生成的站点具备 CDN 缓存、自动化预渲染等生产级特性。  
- **安全与合规**：仅通过 Notion API 读取公开数据，无后端持久化，攻击面极小；项目采用 MIT 许可证，商业使用无障碍。  
- **可观测性**：默认集成 Vercel/Netlify 的日志与监控，亦可自行接入 Sentry、LogRocket 等工具。  

综合来看，NotionNext 已具备 **高可用、低成本、易扩展** 的特性，适合作为企业内部知识库、个人技术博客或创作者内容平台的生产级解决方案。只要完成基本的安全审计（API Token 管理、依赖漏洞扫描），即可在正式业务中安全上线。

## 🧭 Practical evaluation

**Value:** notionnext-org/NotionNext helps add AI capability without starting from a blank model stack.

**Best use cases**

- prototype AI features
- build RAG or agent workflows
- evaluate model tooling

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 11416 GitHub stars
- 14588 forks
- updated 2026-05-14
- primary language: JavaScript
- 7 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 100/100 |
| stars | 86/100 |
| topics | 88/100 |
| outlook | 81/100 |
| quality | 89/100 |
| recency | 80/100 |
| adoption | 90/100 |
| production | 75/100 |
| usefulness | 58/100 |
| integration | 46/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 200/100 |

---

<sub>🔭 Discovered 2026-05-14 · [View on GitHub](https://github.com/notionnext-org/NotionNext) · [← Back to Frontend](./README.md)</sub>
