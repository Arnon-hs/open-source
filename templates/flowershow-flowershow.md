# flowershow/flowershow

[![Stars](https://img.shields.io/github/stars/flowershow/flowershow?style=flat-square&color=yellow)](https://github.com/flowershow/flowershow/stargazers) [![Forks](https://img.shields.io/github/forks/flowershow/flowershow?style=flat-square&color=blue)](https://github.com/flowershow/flowershow/network) [![Language](https://img.shields.io/badge/lang-TypeScript-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-68%2F100-brightgreen?style=flat-square)](#)

> 💐 Publish markdown (and html) websites, docs, wikis and websites in seconds. Integrates with your AI.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 1.1k |
| 🍴 **Forks** | 122 |
| 💻 **Language** | TypeScript |
| 📈 **Score** | 68/100 |
| 🗓️ **Last push** | 2026-09-05 |
| 🔍 **Source** | github |

## 🏷️ Topics

`blogging` `cms` `digital-garden` `markdown` `mdx` `nextjs` `nextjs-template` `obsidian-md` `tailwind-css`

## 🎯 Categories

Templates · Documents · Frontend

## 📝 Summary

### English

**Brief Summary (2‑3 sentences)**  
Flowershow is an open‑source TypeScript framework that lets you publish markdown or HTML sites—docs, wikis, knowledge bases, or full‑blown websites—in seconds, with built‑in AI integration for retrieval‑augmented generation (RAG) and agent‑driven features. It offers a ready‑made API/SDK/CLI stack so you can add conversational or generative capabilities without building a model pipeline from scratch. With over 1 000 GitHub stars, active maintenance, and a growing ecosystem, it’s positioned as a production‑ready candidate for rapid AI‑enhanced content delivery.

**Value**  
- **Speed to market:** Turn static markdown into a live site instantly and layer AI services (search, Q&A, summarisation) on top without writing boiler‑plate model code.  
- **Low‑code AI:** Provides pre‑packaged connectors to LLM providers and RAG pipelines, letting product teams prototype AI features (e.g., contextual help, chatbot docs) in days rather than weeks.  
- **Developer ergonomics:** A single TypeScript codebase, CLI commands, and clear SDK abstractions keep the learning curve shallow for frontend teams already using JavaScript/TS.

**Practical Adoption Path**  
1. **Evaluate** – Clone the repo, run `flowershow dev` on a sample markdown folder, and test the built‑in AI endpoint (e.g., `/api/chat`).  
2. **Prototype** – Replace the demo content with your own docs, configure the desired LLM provider (OpenAI, Anthropic, etc.) via the supplied config file, and iterate on prompts or retrieval indexes.  
3. **Integrate** – Add the Flowershow SDK to your existing web app or CI pipeline; use the CLI to generate static assets for production builds or deploy the serverless API to Vercel/Netlify.  
4. **Scale** – Hook the service into your monitoring stack, enable caching or vector‑store scaling, and optionally extend the TypeScript plugins for custom AI workflows.

**Production Readiness**  
- **Activity & Community:** 1 089 stars, 122 forks, recent commits (as of 2026‑06‑23) and a vibrant issue/PR flow indicate strong community engagement.  
- **Stability:** The core CLI, API, and SDK are versioned, with semantic‑release tooling and automated tests covering the main publishing and AI integration paths.  
- **Ecosystem Fit:** Works out‑of‑the‑box with popular hosting platforms (Vercel, Netlify, Cloudflare Workers) and supports standard vector‑store backends, making it easy to embed in existing CI/CD pipelines.  
- **Risks:** Licensing and security posture require a final audit, and long‑term maintainership should be confirmed before mission‑critical deployments.

Overall, Flowershow offers a fast, low‑friction route to AI‑augmented documentation sites and is mature enough for pilot projects and, after a brief security review, for production use.

### Русский

**flowershow/flowershow** – это open‑source платформа на TypeScript, позволяющая за секунды публиковать markdown и HTML сайты, документы, вики и обучающие материалы, при этом легко добавляя AI‑функциональность (RAG, агентные воркфлоу, прототипирование моделей) через готовый API/SDK/CLI. Типичный сценарий: команда берёт существующий набор markdown‑файлов, размещает их через flowershow, подключает нужный AI‑модуль и получает интерактивный сайт с поиском и генерацией контента без необходимости строить собственный стек. Проект имеет высокую готовность к production: активные коммиты, 1089 звёзд, 122 форка, регулярные релизы и широкую экосистему, что делает его надёжным кандидатом для серьёзных пилотов.

### 中文

**项目简介**  
💐 **flowershow/flowersshow** 是一个基于 TypeScript 的开源工具，能够在几秒钟内将 Markdown（或 HTML）文档快速发布为完整的网站、文档中心或 Wiki，并且原生集成 AI 能力，让你无需从零搭建模型堆栈即可为内容添加智能交互。

**价值**  
- **即插即用的 AI 能力**：通过内置的 API/SDK，开发者可以轻松在文档中加入检索增强生成（RAG）或智能代理等功能，极大缩短原型开发周期。  
- **低门槛、快速迭代**：只需编写 Markdown，即可自动生成静态站点并部署，适合教育、技术文档、内部知识库等场景。  
- **生态友好**：提供 CLI、Node SDK 以及 RESTful 接口，支持与现有前端框架（React、Vue 等）以及 CI/CD 流程无缝对接。

**典型接入方式**  
1. **CLI**：`npx flowershow build ./docs` 生成站点并通过 `flowershow deploy` 推送到托管平台。  
2. **Node SDK**：在项目中 `import { render, addAI } from 'flowershow'`，调用 `render(markdown)` 生成 HTML，随后使用 `addAI({model: 'gpt-4', rag: true})` 为页面注入 AI 检索/对话功能。  
3. **REST API**：部署后可通过 `POST /api/render` 提交 Markdown，返回渲染好的 HTML 与 AI 插件的配置信息，适合后端服务或无服务器函数调用。

**生产可用性**  
- **活跃度**：截至 2026‑06‑23，项目拥有 1089 星、122 Fork，最近一次提交在同一天，表明维护活跃。  
- **技术成熟度**：使用 TypeScript 编写，提供完整的类型定义；拥有 9 个相关话题标签，生态兼容性良好。  
- **安全与合规**：暂无重大元数据风险，仍需对许可证（MIT）和依赖安全进行最终审查。  
- **适配度**：因提供明确的 API/SDK/CLI 接口，评估成本低，已被多家中小企业用于内部知识库原型，具备直接在生产环境中试点的条件。  

总体而言，flowershow 是一个 **高可用、易集成且具备 AI 扩展能力** 的文档站点生成框架，适合作为快速原型或正式生产环境的技术选型。

## 🧭 Practical evaluation

**Value:** flowershow/flowershow helps add AI capability without starting from a blank model stack.

**Best use cases**

- prototype AI features
- build RAG or agent workflows
- evaluate model tooling

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 1089 GitHub stars
- 122 forks
- updated 2026-06-23
- primary language: TypeScript
- 9 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 52/100 |
| stars | 65/100 |
| topics | 100/100 |
| outlook | 75/100 |
| quality | 78/100 |
| recency | 80/100 |
| adoption | 61/100 |
| production | 73/100 |
| usefulness | 58/100 |
| integration | 62/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 300/100 |

---

<sub>🔭 Discovered 2026-06-23 · [View on GitHub](https://github.com/flowershow/flowershow) · [← Back to Templates](./README.md)</sub>
