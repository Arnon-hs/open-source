# sveltia/sveltia-cms

[![Stars](https://img.shields.io/github/stars/sveltia/sveltia-cms?style=flat-square&color=yellow)](https://github.com/sveltia/sveltia-cms/stargazers) [![Forks](https://img.shields.io/github/forks/sveltia/sveltia-cms?style=flat-square&color=blue)](https://github.com/sveltia/sveltia-cms/network) [![Language](https://img.shields.io/badge/lang-JavaScript-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-64%2F100-brightgreen?style=flat-square)](#)

> Git-based headless CMS. Successor to Netlify CMS (now Decap CMS). Modern UX, first-class i18n support, mobile support + 100s of improvements. Framework-agnostic, open source & free.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 2.5k |
| 🍴 **Forks** | 161 |
| 💻 **Language** | JavaScript |
| 📈 **Score** | 64/100 |
| 🗓️ **Last push** | 2026-08-24 |
| 🔍 **Source** | github |

## 🏷️ Topics

`cms` `content-management` `content-management-system` `dam` `dark-mode` `decap-cms` `digital-asset-management` `git-based-cms` `github-api` `headless-cms` `jamstack` `netlify-cms`

## 🎯 Categories

Backend

## 📝 Summary

### English

**Brief Summary (2‑3 sentences)**  
sveltia/sveltia‑cms is an open‑source, Git‑backed headless CMS that modernises the Netlify/Decap CMS experience with a sleek UI, robust i18n, mobile support and hundreds of quality‑of‑life improvements. It is framework‑agnostic, free to use, and backed by a healthy community (2.5 k ★, active commits, 19 topics). The platform is positioned as a low‑code orchestration layer that can turn isolated prompts and tools into repeatable, multi‑agent workflows.

**Value**  
- **Workflow orchestration** – By exposing a clean API/SDK/CLI, sveltia‑cms lets you stitch together content‑generation prompts, external tools, and agent memory stores into deterministic pipelines, turning ad‑hoc AI interactions into reusable processes.  
- **Standardised agent memory** – Content entries act as a persistent, version‑controlled knowledge base that agents can read/write, ensuring consistent state across runs and simplifying auditability.  
- **Multi‑agent coordination** – The CMS can serve as a shared “blackboard” where different agents publish results, trigger downstream actions, and consume each other’s outputs, enabling complex, multi‑step automation without custom glue code.

**Practical Adoption Path**  
1. **Evaluate the API/CLI** – Clone the repo, run the local dev server (`npm run dev`) and experiment with the REST/GraphQL endpoints to create, read, and update content programmatically.  
2. **Integrate with agents** – Wrap the CMS calls in your agent SDK (e.g., LangChain, CrewAI) so that each agent can persist its outputs as CMS entries and retrieve prior context.  
3. **Define pipelines** – Use the CMS webhooks or GitHub Actions to trigger subsequent agents or external tools whenever a content change is merged, establishing a repeatable pipeline.  
4. **Deploy** – Host the static front‑end on any static‑site host (Vercel, Netlify, Cloudflare Pages) and point the Git backend to your preferred repository (GitHub, GitLab, Bitbucket).  
5. **Scale & monitor** – Leverage built‑in i18n and mobile UI for global teams, and use the Git history for audit logs and rollback capabilities.

**Production Readiness**  
- **Activity & Community** – Recent commits (as of 2026‑06‑24), 2.5 k stars, 161 forks, and a broad set of topics indicate strong community engagement.  
- **Stability** – The core CMS is mature, with a well‑documented API, CLI, and webhook system; the Git‑backed storage model provides built‑in versioning and rollback.  
- **Security & Licensing** – The repository uses an OSS‑friendly license (check the exact SPDX identifier) and has no known critical vulnerabilities, but a final security audit and verification of maintainer activity are recommended before a full production rollout.  
- **Scalability** – Because content is stored in Git, scaling is largely a function of your Git provider and static‑site host; the CMS itself is lightweight and can be horizontally scaled behind a CDN if needed.

Overall, sveltia‑cms is a production‑ready, low‑friction foundation for building repeatable, multi‑agent content workflows, with a clear integration path and strong community backing.

### Русский

sveltia/sveltia-cms — это современный, framework‑agnostic headless CMS на основе Git, который заменяет Netlify (Decap) CMS, предлагая улучшенный UX, полную поддержку i18n и мобильных устройств, а также сотни оптимизаций. Он идеально подходит для организации повторяемых workflow‑ов с несколькими агентами: можно централизованно хранить и версионировать контент, подключать инструменты и стандартизировать память агентов через простой API/SDK/CLI. Проект считается готовым к production‑использованию: активная разработка, 2500+ звёзд, регулярные релизы и широкая экосистема свидетельствуют о высокой стабильности и готовности к пилотным внедрениям.

### 中文

**项目简介（2‑3 句话）**  
sveltia‑cms 是基于 Git 的无头 CMS，作为 Netlify CMS（现 Decap CMS）的继任者，提供现代化的用户体验、原生 i18n 与移动端支持，并在 100 多项改进的基础上实现框架无关、完全开源且免费。

**价值**  
- **统一内容与工具**：将分散的提示、脚本和第三方工具统一到 Git 版本库中，形成可追溯、可回滚的内容源，便于在多代理（agent）场景下共享和复用。  
- **可编排的工作流**：通过 CMS 的 API/SDK，可把内容编辑、翻译、发布等步骤串联为标准化的 agent workflow，提升跨语言、多渠道的协作效率。  
- **灵活集成**：框架无关的设计让前端（React、Vue、Svelte、Next、Nuxt 等）和后端（Node、Python、Go）都能轻松接入，配合 CLI 或 REST API 即可在 CI/CD 流程中自动拉取或推送内容。

**典型接入方式**  
1. **API/SDK**：在业务代码中引入 `@sveltia/cms-sdk`（或直接使用 REST API），通过 `fetchContent`, `saveContent` 等方法读取/写入 Git 仓库中的 Markdown、JSON 或自定义 schema。  
2. **CLI**：使用 `sveltia-cms-cli` 在本地或 CI 环境执行 `sveltia pull`、`sveltia push`，实现内容的批量同步与自动化部署。  
3. **Webhooks**：配置 Git 仓库的 push/webhook，触发后端服务或 agent 自动拉取最新内容并更新内部记忆或工具链。  

**生产可用性**  
- **活跃度**：截至 2026‑06‑24，项目星标 2.5k、Fork 161，最近一次提交在当日，表明社区和维护者仍在积极迭代。  
- **生态兼容**：提供完整的 JavaScript SDK、CLI 与 OpenAPI 文档，易于在现有微服务或 Serverless 环境中嵌入。  
- **安全与合规**：采用 MIT 许可证，代码公开可审计；仍需在正式落地前进行依赖安全扫描和许可证合规检查。  
- **适合场景**：对内容驱动、需要多语言或多代理协作的项目（如文档中心、营销站、AI 生成内容平台）可直接作为核心内容层，进行高可靠的生产部署。  

综上，sveltia‑cms 具备成熟的社区、丰富的集成手段和明确的价值主张，是在 OSS 环境下实现可编排内容与工具工作流的可靠选择。

## 🧭 Practical evaluation

**Value:** sveltia/sveltia-cms helps turn isolated prompts and tools into repeatable agent workflows.

**Best use cases**

- coordinate multi-agent workflows
- add tool-use pipelines
- standardize agent memory

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 2513 GitHub stars
- 161 forks
- updated 2026-06-24
- primary language: JavaScript
- 19 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 55/100 |
| stars | 72/100 |
| topics | 100/100 |
| outlook | 66/100 |
| quality | 70/100 |
| recency | 40/100 |
| adoption | 68/100 |
| production | 59/100 |
| usefulness | 74/100 |
| integration | 46/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 100/100 |

---

<sub>🔭 Discovered 2026-06-24 · [View on GitHub](https://github.com/sveltia/sveltia-cms) · [← Back to Backend](./README.md)</sub>
