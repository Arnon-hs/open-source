# gramps-project/gramps-web

[![Stars](https://img.shields.io/github/stars/gramps-project/gramps-web?style=flat-square&color=yellow)](https://github.com/gramps-project/gramps-web/stargazers) [![Forks](https://img.shields.io/github/forks/gramps-project/gramps-web?style=flat-square&color=blue)](https://github.com/gramps-project/gramps-web/network) [![Language](https://img.shields.io/badge/lang-JavaScript-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-58%2F100-brightgreen?style=flat-square)](#)

> Open Source Online Genealogy System

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 1.4k |
| 🍴 **Forks** | 218 |
| 💻 **Language** | JavaScript |
| 📈 **Score** | 58/100 |
| 🗓️ **Last push** | 2026-09-05 |
| 🔍 **Source** | github |

## 🏷️ Topics

`family-history` `family-tree` `gedcom` `genealogy` `gramps` `gramps-xml` `hacktoberfest` `javascript` `lit` `web-components`

## 🎯 Categories

Frontend

## 📝 Summary

### English

**Brief Summary (2‑3 sentences)**  
Gramps‑Web is the open‑source, web‑based front‑end for the Gramps genealogy platform, offering a modern JavaScript UI for building and exploring family trees online. Its active community, recent updates, and solid GitHub metrics make it a viable foundation for adding AI‑driven features such as RAG or autonomous agents without having to start from scratch. A small proof‑of‑concept integration can quickly validate the effort required to embed AI tooling.

**Value**  
- **Accelerated AI prototyping:** By leveraging an existing, well‑maintained genealogy stack, developers can focus on layering AI capabilities (e.g., natural‑language search, automated record extraction) instead of recreating core data models and UI components.  
- **Rich domain data:** Gramps already structures person, event, source, and relationship data, providing a high‑quality knowledge base that is ideal for retrieval‑augmented generation (RAG) or agent‑based assistants.  
- **Community & extensibility:** The project’s sizable star/fork count and active issue/PR flow indicate a healthy ecosystem, reducing the risk of “unknown‑unknowns” when extending the platform.

**Practical Adoption Path**  
1. **Proof of concept (PoC):** Fork the repo, run the Docker‑compose setup, and verify the baseline UI works locally.  
2. **AI integration point:** Identify the backend service that serves genealogy data (typically a Python/REST API) and expose a thin wrapper that returns JSON for a given person or family.  
3. **Add AI layer:** Deploy a small LLM service (e.g., OpenAI, Llama‑CPP) and connect it to the wrapper to implement a feature such as “Ask about ancestor’s life” or “Suggest missing records.”  
4. **Iterate & test:** Use the existing unit‑test suite and add integration tests for the new AI endpoints.  
5. **Documentation & hand‑off:** Update the README with the new AI workflow, sample prompts, and deployment instructions.

**Production Readiness**  
- **Code health:** 1,429 stars, 218 forks, recent commit (2026‑05‑13), and a primary JavaScript codebase suggest active maintenance.  
- **Ecosystem fit:** The project already ships Docker images and CI pipelines, simplifying containerized deployment in production environments.  
- **Risk considerations:** The integration path for AI isn’t documented; initial effort will be needed to understand the backend API surface and to provision compute for LLM inference. Once the PoC validates the integration cost, scaling to a full‑featured AI‑enhanced genealogy service is straightforward.  

Overall, Gramps‑Web is a strong OSS candidate for pilots that need a genealogy foundation plus the flexibility to experiment with AI‑driven user experiences.

### Русский

**gr​amps‑project/gramps‑web** — это открытая онлайн‑платформа для генеалогических исследований, которая уже содержит готовую инфраструктуру и может быть быстро расширена AI‑функциями (например, RAG‑поиск по семейным архивам или агентные сценарии). Типичный путь внедрения — запуск небольшого proof‑of‑concept, проверка README и подключение нужных моделей, после чего можно масштабировать в полноценный сервис. Проект считается почти готовым к production: активные коммиты, более 1400 звёзд, широкое сообщество и стабильный JavaScript‑стек, однако детали интеграции требуют предварительной проверки.

### 中文

**项目简介（2‑3 句话）**  
Gramps‑Web 是 Gramps（开源族谱系统）的 Web 前端，实现了在线家谱管理、数据可视化和协作编辑。它基于现代 JavaScript 框架，提供 REST/GraphQL 接口，便于在浏览器和移动端直接使用。

**价值**  
- **快速赋能 AI**：通过已有的族谱数据模型，开发者可以直接在 Gramps‑Web 上实验自然语言查询、RAG（检索增强生成）或智能助手等 AI 功能，而无需从零搭建数据层。  
- **原型迭代成本低**：项目已具备完整的用户管理、树形结构和时间轴展示，适合作为 AI 功能的原型平台，帮助快速验证概念并收集用户反馈。  
- **生态兼容**：拥有 1400+ 星、200+ Fork，活跃的社区和丰富的插件生态，可与现有的 AI 框架（LangChain、LLM‑Ops 等）以及数据存储（PostgreSQL、SQLite）无缝对接。

**典型接入方式**  
1. **本地/容器化部署**：使用官方 Docker 镜像或 `docker‑compose.yml` 快速启动服务，完成数据库初始化后即可访问。  
2. **API 集成**：通过提供的 REST/GraphQL 接口读取族谱实体（人物、事件、关系），在后端接入 LLM（如 OpenAI、Claude）进行自然语言查询或生成族谱报告。  
3. **插件/扩展**：在 `src/plugins` 目录编写自定义插件，注册为前端组件或后端服务，实现 RAG 检索、智能推荐或对话式交互。  
4. **CI/CD 验证**：在 CI 流水线中运行项目自带的单元/集成测试，确保自定义 AI 模块与核心功能兼容。

**生产可用性**  
- **成熟度高**：项目最近一次提交在 2026‑05‑13，活跃度良好，社区响应及时，代码质量符合现代前端最佳实践。  
- **可扩展部署**：支持水平扩容的容器化部署，数据库可选 PostgreSQL（生产推荐）或 SQLite（轻量原型），并提供 Nginx/Traefik 反向代理示例。  
- **安全与合规**：内置用户角色与权限系统，支持 OAuth2/SAML 单点登录，可满足企业内部数据访问控制需求。  
- **风险提示**：官方文档对 AI 功能的集成路径描述有限，建议先在沙盒环境完成小规模 PoC，评估依赖的 LLM SDK、费用及网络延迟后再推进生产化。  

综上，Gramps‑Web 具备稳固的开源基础和丰富的族谱数据模型，是在家谱领域快速试验和落地 AI 功能的理想平台，只要做好前期的集成验证，即可在生产环境中安全、可靠地使用。

## 🧭 Practical evaluation

**Value:** gramps-project/gramps-web helps add AI capability without starting from a blank model stack.

**Best use cases**

- prototype AI features
- build RAG or agent workflows
- evaluate model tooling

**Integration notes:** Looks feasible to evaluate, but integration should start with a small proof of concept and README check.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 1429 GitHub stars
- 218 forks
- updated 2026-05-13
- primary language: JavaScript
- 10 topics

**Risks:** Integration path is not obvious from metadata; validate setup cost before committing.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 59/100 |
| stars | 67/100 |
| topics | 100/100 |
| outlook | 73/100 |
| quality | 79/100 |
| recency | 80/100 |
| adoption | 65/100 |
| production | 69/100 |
| usefulness | 42/100 |
| integration | 30/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 100/100 |

---

<sub>🔭 Discovered 2026-05-13 · [View on GitHub](https://github.com/gramps-project/gramps-web) · [← Back to Frontend](./README.md)</sub>
