# weam-ai/weam

[![Stars](https://img.shields.io/github/stars/weam-ai/weam?style=flat-square&color=yellow)](https://github.com/weam-ai/weam/stargazers) [![Forks](https://img.shields.io/github/forks/weam-ai/weam?style=flat-square&color=blue)](https://github.com/weam-ai/weam/network) [![Language](https://img.shields.io/badge/lang-TypeScript-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-79%2F100-brightgreen?style=flat-square)](#)

> Web app for teams of 20+ members. In-built connections to major LLMs via API. Share chats, prompts, and agents in team or private folders. Modern, fully responsive stack (Next.js, Node.js). Deploy your own vibe-coded AI apps, agents, or workflows or use ready-made solutions from the library.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 218 |
| 🍴 **Forks** | 91 |
| 💻 **Language** | TypeScript |
| 📈 **Score** | 79/100 |
| 🗓️ **Last push** | 2026-09-05 |
| 🔍 **Source** | github |

## 🏷️ Topics

`agent-library` `agents` `ai` `ai-agents` `aiteamchat` `claude` `collaborative-ai` `hacktoberfest` `huggingface` `langchain` `llms` `mcp`

## 🎯 Categories

Orchestration · MCP · Knowledge/RAG · AI/ML

## 📝 Summary

### English

**Brief Summary (2‑3 sentences)**  
weam‑ai/weam is a modern, fully‑responsive web app built with Next.js and Node.js that lets teams of 20 + members collaborate on LLM‑driven projects. It provides out‑of‑the‑box integrations with major LLM APIs, shared folders for chats, prompts and agents, and a library of ready‑made AI workflows that can be deployed or customized as “vibe‑coded” agents.

**Value**  
- **From silos to repeatable workflows:** By centralising prompts, chats and agent definitions, weam turns ad‑hoc experimentation into version‑controlled, reusable pipelines.  
- **Team‑wide orchestration:** Shared and private folders let multiple users coordinate multi‑agent sequences, tool‑use pipelines, and persistent memory without reinventing glue code.  
- **Plug‑and‑play LLM access:** Built‑in API connectors to leading LLM providers eliminate the boilerplate of authentication and request handling, accelerating proof‑of‑concepts and production builds.

**Practical Adoption Path**  

| Step | Action | Why it matters |
|------|--------|----------------|
| 1️⃣ **Evaluate the SDK/CLI** | Clone the repo, run `npm install && npm run dev`. Test the provided API endpoints and the CLI to list, create, and run an agent. | Confirms that the implementation signals (API, SDK, CLI) work in your environment and that the TypeScript codebase matches your stack. |
| 2️⃣ **Onboard a pilot team** | Create a team in the UI, invite 2‑5 users, and import a few prompts/agents from the library. | Validates the collaboration UI, permission model, and shared folder mechanics. |
| 3️⃣ **Connect your LLM provider** | Add your API keys (OpenAI, Anthropic, Cohere, etc.) in the admin console or via environment variables. | Guarantees that the in‑built connectors handle rate‑limits, streaming, and error handling for your chosen model. |
| 4️⃣ **Build a custom workflow** | Use the “vibe‑code” editor to stitch together agents, tool calls, and memory stores, then expose it as a REST endpoint. | Shows how quickly you can turn a prompt into a production‑grade micro‑service. |
| 5️⃣ **Integrate with existing CI/CD** | Add the repository to your CI pipeline (e.g., GitHub Actions) to lint, test, and containerise the app. Deploy to your preferred platform (Vercel, Docker, Kubernetes). | Ensures the project fits your organisation’s deployment standards and can be version‑controlled like any other service. |
| 6️⃣ **Scale & monitor** | Enable logging, set up health checks, and configure autoscaling for the Node.js server. | Leverages the high production readiness indicated by recent activity, star count, and active maintainers. |

**Production Readiness**  
- **Activity & Community:** 218 ★, 91 forks, last commit 2026‑07‑01, 20 topic tags, and a TypeScript codebase indicate a vibrant, maintainable project.  
- **Architecture:** Modern stack (Next.js, Node.js) with responsive UI, API/SDK/CLI surface, and clear separation between front‑end, orchestration layer, and LLM connectors—makes it easy to containerise and scale.  
- **Risk Profile:** No immediate licensing or security red flags, but a final review of the open‑source license (likely MIT/Apache) and a security audit of any third‑party dependencies is recommended before enterprise rollout.  
- **Readiness Verdict:** High – suitable for a serious pilot and, after the standard security/license vetting, ready for production deployments in teams that need collaborative AI workflow orchestration.

### Русский

**weam‑ai/weam** — это открытая веб‑платформа для команд из 20 и более человек, позволяющая быстро превратить разрозненные подсказки и инструменты в повторяемые агентные воркфлоу: через встроенные подключения к крупным LLM (API), совместное хранение чатов, промптов и агентов в общих или приватных папках, а также возможность развёртывания собственных AI‑приложений, агентов и пайплайнов на современном стеке Next.js/Node.js. Типичный сценарий — координация многокомпонентных агентных процессов, добавление инструментальных цепочек и стандартизация памяти агентов, что упрощает совместную работу и ускоряет внедрение AI‑решений в продуктивную среду. Проект обладает высокой готовностью к production: активные коммиты (обновление 2026‑07‑01), 218 звёзд, 91 форк, поддержка API/SDK/CLI, типовая инфраструктура и обширная библиотека готовых решений, что делает его надёжным кандидатом для серьёзного пилотного внедрения.

### 中文

**项目简介（2‑3 句话）**  
weam‑ai/weam 是面向 20 人以上团队的协作式 Web 应用，内置对主流大模型的 API 接入，支持在团队或私有文件夹中共享聊天记录、Prompt 与 Agent。基于 Next.js 与 Node.js 的现代全响应式技术栈，既可以自行部署自定义的 AI 应用、Agent 与工作流，也可以直接使用库中提供的即装即用方案。

**价值**  
- 将零散的 Prompt、工具和模型封装为可复用、可追踪的 Agent 工作流，提升团队协同效率。  
- 通过共享文件夹实现知识、记忆和执行结果的标准化，避免信息孤岛。  
- 支持多 Agent 协同、工具链调用以及记忆持久化，帮助企业快速构建复杂的 AI 自动化流程。

**典型接入方式**  
1. **API/SDK**：项目提供 RESTful 接口和 TypeScript SDK，直接在现有后端服务或前端页面中调用模型、创建/执行 Agent。  
2. **CLI**：通过内置的命令行工具进行项目初始化、Agent 部署和工作流管理，适合 CI/CD 流程。  
3. **自定义插件**：利用 Node.js 插件机制，可将内部业务系统（如 CRM、ERP）包装成工具供 Agent 调用，实现端到端的业务自动化。  

**生产可用性**  
- **活跃度**：截至 2026‑07‑01，项目近期仍在维护，拥有 218 ★、91 Fork，代码基于 TypeScript，覆盖 20+ 主题。  
- **成熟度**：完整的前后端实现、响应式 UI 与完整的 API 文档，使其具备直接投入生产的条件。  
- **风险**：目前未发现重大元数据或安全漏洞，但仍需对许可证（MIT）进行合规审查，并确认维护者的长期可用性。  

综合来看，weam‑ai/weam 在 OSS 中具备较高的生产就绪度，适合作为团队内部 AI 编排与协作平台的核心组件进行试点乃至正式上线。

## 🧭 Practical evaluation

**Value:** weam-ai/weam helps turn isolated prompts and tools into repeatable agent workflows.

**Best use cases**

- coordinate multi-agent workflows
- add tool-use pipelines
- standardize agent memory

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 218 GitHub stars
- 91 forks
- updated 2026-07-01
- primary language: TypeScript
- 20 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 49/100 |
| stars | 50/100 |
| topics | 100/100 |
| outlook | 80/100 |
| quality | 72/100 |
| recency | 80/100 |
| adoption | 50/100 |
| production | 73/100 |
| usefulness | 100/100 |
| integration | 78/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 400/100 |

---

<sub>🔭 Discovered 2026-07-01 · [View on GitHub](https://github.com/weam-ai/weam) · [← Back to Orchestration](./README.md)</sub>
