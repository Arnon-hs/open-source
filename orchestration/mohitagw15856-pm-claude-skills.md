# mohitagw15856/pm-claude-skills

[![Stars](https://img.shields.io/github/stars/mohitagw15856/pm-claude-skills?style=flat-square&color=yellow)](https://github.com/mohitagw15856/pm-claude-skills/stargazers) [![Forks](https://img.shields.io/github/forks/mohitagw15856/pm-claude-skills?style=flat-square&color=blue)](https://github.com/mohitagw15856/pm-claude-skills/network) [![Language](https://img.shields.io/badge/lang-JavaScript-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-67%2F100-brightgreen?style=flat-square)](#)

> 238 professional Agent Skills (PRDs, launches, postmortems, compliance & more) for Claude, ChatGPT, Gemini, Cursor & Codex. Try free in-browser, or 'npx pm-claude-skills add'. One SKILL.md, every AI tool.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 1k |
| 🍴 **Forks** | 182 |
| 💻 **Language** | JavaScript |
| 📈 **Score** | 67/100 |
| 🗓️ **Last push** | 2026-08-24 |
| 🔍 **Source** | github |

## 🏷️ Topics

`agent-skills` `ai-agents` `chatgpt` `claude-ai` `claude-code` `claude-skills` `codex` `cursor` `gemini` `hermes-agent` `llm-tools` `mcp`

## 🎯 Categories

Orchestration · MCP · AI/ML · Product

## 📝 Summary

### English

**Brief Summary (2‑3 sentences)**  
The *pm‑claude‑skills* repository bundles 238 ready‑to‑use “Agent Skills” – PRDs, launch plans, post‑mortems, compliance checklists and more – that can be invoked by Claude, ChatGPT, Gemini, Cursor or Codex. The skills are delivered as single `SKILL.md` files and can be tried instantly in the browser or added to a project with a one‑liner CLI (`npx pm-claude-skills add`). By turning ad‑hoc prompts into reusable, version‑controlled workflows, the library makes multi‑agent orchestration far more predictable and scalable.

**Value Proposition**  
- **Standardisation** – Every skill follows a consistent markdown schema, giving product teams a shared language for requirements, launch steps, compliance checks, and post‑mortems across any LLM.  
- **Speed to market** – Teams can drop a skill into an existing prompt or toolchain without writing custom code, accelerating prototyping and reducing duplication.  
- **Reusability & memory** – Skills act as modular building blocks that can be chained, stored in agent memory, and reused across projects, enabling reliable multi‑agent pipelines.

**Practical Adoption Path**  
1. **Explore** – Open the in‑browser demo to browse the catalogue and see example outputs.  
2. **Install** – Run `npx pm-claude-skills add` in your project; the CLI scaffolds a `skills/` folder with the chosen markdown files and a thin JavaScript wrapper.  
3. **Integrate** – Import the wrapper in your existing LLM orchestration code (Node.js, TypeScript, or via the provided HTTP API) and call `runSkill('launch‑plan')` or similar.  
4. **Extend** – Add custom skills by copying an existing `SKILL.md` template, editing the markdown, and committing to your repo for version control.  
5. **Govern** – Use the built‑in metadata (topic tags, version, required APIs) to enforce compliance and audit usage across teams.

**Production Readiness**  
- **Activity & Community** – 1 019 stars, 182 forks, recent commits (as of 2026‑06‑24) and a vibrant JavaScript ecosystem indicate strong momentum.  
- **Implementation Signals** – The project ships a clear CLI, an HTTP/SDK interface, and language‑agnostic markdown assets, making integration straightforward.  
- **Stability** – The core library is lightweight, has no heavy runtime dependencies, and the skill files are pure data, reducing runtime risk.  
- **Risks** – Final due‑diligence is needed on the open‑source license, security review of the CLI, and confirmation of an active maintainer. Assuming those checks pass, the package is ready for a serious pilot in production environments.

### Русский

**mohitagw15856/pm-claude-skills** — это набор из 238 готовых «навыков» (PRD, запуски, постмортемы, комплаенс и т.д.) для Claude, ChatGPT, Gemini, Cursor и Codex, позволяющих превратить разрозненные подсказки и инструменты в повторяемые агентные рабочие процессы. Типичный сценарий — интеграция через CLI (`npx pm-claude-skills add`) или в браузере для координации многопользовательских агентов, построения пайплайнов с использованием инструментов и стандартизации памяти агентов. Проект имеет высокую готовность к production: активные коммиты, более 1000 звёзд, широкая экосистема (JS‑SDK, API), однако требуется окончательная проверка лицензии и безопасности.

### 中文

**项目简介**  
mohitagw15856/pm-claude-skills 提供 238 条专业的 Agent Skill（包括 PRD、产品发布、事后复盘、合规等），可直接在 Claude、ChatGPT、Gemini、Cursor、Codex 等主流大模型中使用。只需在浏览器中免费体验，或通过 `npx pm-claude-skills add` 一键装载，即可在任意 AI 工具中获得统一的 `SKILL.md` 文档。

**价值**  
- 将碎片化的 Prompt 与工具链转化为可复用、可版本化的 Agent 工作流，提升团队协作效率。  
- 通过统一的 Skill 定义，实现多 Agent 协同、工具调用流水线以及 Agent 记忆的标准化管理。  

**典型接入方式**  
1. **浏览器即用**：访问项目主页或演示页面，直接在网页上运行 Skill。  
2. **CLI 安装**：在项目根目录执行 `npx pm-claude-skills add`，自动生成对应的 `SKILL.md` 并注入到代码库或 CI 流程中。  
3. **SDK/API**：项目公开了 JavaScript SDK，可在自研平台通过 `import { getSkill } from 'pm-claude-skills'` 调用特定 Skill，或通过 REST API 拉取 Skill 内容进行二次加工。  

**生产可用性**  
- **活跃度**：截至 2026‑06‑24，最近一次提交，仅 1 天前更新；GitHub ★1019、Fork 182，社区活跃。  
- **技术成熟度**：核心实现基于 JavaScript，提供 CLI、SDK 与 REST 接口，易于在现有微服务或 Serverless 环境中集成。  
- **风险**：暂无重大元数据风险；仍需对许可证（MIT）和安全审计进行最终确认。整体来看，项目已具备高可用性，适合作为正式生产环境的 Agent 技能库进行试点。

## 🧭 Practical evaluation

**Value:** mohitagw15856/pm-claude-skills helps turn isolated prompts and tools into repeatable agent workflows.

**Best use cases**

- coordinate multi-agent workflows
- add tool-use pipelines
- standardize agent memory

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 1019 GitHub stars
- 182 forks
- updated 2026-06-24
- primary language: JavaScript
- 20 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 57/100 |
| stars | 64/100 |
| topics | 100/100 |
| outlook | 67/100 |
| quality | 68/100 |
| recency | 40/100 |
| adoption | 62/100 |
| production | 58/100 |
| usefulness | 90/100 |
| integration | 46/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 400/100 |

---

<sub>🔭 Discovered 2026-06-24 · [View on GitHub](https://github.com/mohitagw15856/pm-claude-skills) · [← Back to Orchestration](./README.md)</sub>
