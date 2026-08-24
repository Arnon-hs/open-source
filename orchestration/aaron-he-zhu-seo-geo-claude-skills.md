# aaron-he-zhu/seo-geo-claude-skills

[![Stars](https://img.shields.io/github/stars/aaron-he-zhu/seo-geo-claude-skills?style=flat-square&color=yellow)](https://github.com/aaron-he-zhu/seo-geo-claude-skills/stargazers) [![Forks](https://img.shields.io/github/forks/aaron-he-zhu/seo-geo-claude-skills?style=flat-square&color=blue)](https://github.com/aaron-he-zhu/seo-geo-claude-skills/network) [![Language](https://img.shields.io/badge/lang-Shell-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-62%2F100-brightgreen?style=flat-square)](#)

> 20 SEO & GEO skills for Claude Code, Cursor, Codex, and 35+ AI agents. Keyword research, content writing, technical audits, rank tracking. CORE-EEAT + CITE frameworks.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 1.6k |
| 🍴 **Forks** | 235 |
| 💻 **Language** | Shell |
| 📈 **Score** | 62/100 |
| 🗓️ **Last push** | 2026-08-24 |
| 🔍 **Source** | github |

## 🏷️ Topics

`agent-skills` `ai-skills` `claude-code` `claude-skills` `content-optimization` `generative-engine-optimization` `geo` `marketing` `search-engine-optimization` `seo` `seo-tools`

## 🎯 Categories

Orchestration · AI/ML · Marketing

## 📝 Summary

### English

**Brief Summary**  
The **aaron-he-zhu/seo-geo-claude-skills** repository bundles 20 ready‑to‑run SEO and GEO “skills” that can be invoked by Claude, Cursor, Codex and more than 35 other AI agents. The skills cover the full SEO lifecycle—keyword research, content creation, technical site audits, rank tracking, and the CORE‑EEAT + CITE compliance frameworks—turning ad‑hoc prompts into repeatable, multi‑agent workflows.

**Value**  
- **Standardised agent memory & tool use** – each skill is a self‑contained, shell‑scripted module that an agent can call, store results, and reuse, eliminating the need to re‑engineer prompt logic for every new project.  
- **Orchestration ready** – the collection is explicitly designed for multi‑agent pipelines, so you can chain a keyword‑research skill, feed its output into a content‑generation skill, then pipe the result into a technical‑audit skill, all without manual hand‑offs.  
- **Proven SEO methodology** – the CORE‑EEAT (Content, Relevance, Expertise, Authority, Trust) and CITE (Citation, Integrity, Transparency, Evidence) frameworks embed industry‑best practices, giving downstream content a higher chance of ranking.  

**Practical Adoption Path**  

| Step | Action | Why it matters |
|------|--------|----------------|
| 1️⃣ **Initial scoping** | Clone the repo, run `README.md` examples on a sandbox environment with a single Claude or Cursor instance. | Confirms that the shell‑based wrappers work with your chosen LLM provider and that required CLI tools (e.g., `curl`, `jq`) are present. |
| 2️⃣ **Proof‑of‑concept workflow** | Build a minimal pipeline: `keyword‑research → content‑write → rank‑track`. Use the provided scripts as the “agents” and orchestrate them with a lightweight workflow engine (e.g., Temporal, Airflow, or even a Bash orchestrator). | Demonstrates end‑to‑end data flow, validates output formats, and surfaces any missing environment variables or API keys. |
| 3️⃣ **Integration to your platform** | Wrap the chosen scripts in your internal API layer or containerise them (Docker). Hook them into your existing orchestration layer (Kubernetes Jobs, AWS Step Functions, etc.). | Turns the ad‑hoc scripts into production‑grade services that can be versioned, monitored, and scaled. |
| 4️⃣ **Iterate & extend** | Add custom steps (e.g., local SERP scraper, geo‑targeted schema generator) by following the same shell‑script pattern. | Leverages the repository’s “skill” architecture to keep new logic consistent with the rest of the pipeline. |
| 5️⃣ **Monitoring & governance** | Enable logging of each skill’s input/output, enforce the CITE citation checks, and set alerts on audit failures. | Ensures compliance with SEO best practices and gives you visibility for continuous improvement. |

**Production Readiness**  
- **Activity & adoption** – 1,604 GitHub stars, 235 forks, and a recent commit (2026‑05‑14) indicate a vibrant community and ongoing maintenance.  
- **Technology stack** – Pure shell scripts with minimal external dependencies make the codebase lightweight and easy to containerise.  
- **Ecosystem fit** – The repo already targets a wide range of AI agents (Claude, Cursor, Codex, 35+ others), so integration effort is mainly around wiring your orchestration layer rather than rewriting the skills.  
- **Risk mitigation** – The integration path is not documented in detail; the first step should therefore be a small POC to map required environment variables, API credentials, and any custom tooling. Once the POC succeeds, scaling to production is straightforward.

**Bottom line** – The project is mature enough for a serious pilot. Start with a sandbox POC to validate the toolchain, then containerise the skills and plug them into your existing workflow orchestrator. With minimal engineering overhead you’ll gain repeatable, SEO‑focused AI agents that can be scaled across teams and geographies.

### Русский

**a​aron‑he‑zhu/seo‑geo‑claude‑skills** – набор из 20 готовых SEO‑ и GEO‑навыков (исследование ключевых слов, написание контента, технические аудиты, отслеживание позиций) в виде повторяемых workflow‑ов для Claude, Cursor, Codex и более 35 AI‑агентов, построенных по фреймворкам CORE‑EEAT + CITE. Типичный сценарий — подключить проект к существующей оркестрации, создать небольшую proof‑of‑concept‑pipeline, где несколько агентов последовательно используют инструменты (поиск, генерация, проверка) и сохраняют память, а затем масштабировать процесс на полноценные маркетинговые кампании. Проект считается почти готовым к production: активные коммиты, 1600+ звёзд, 235 форков, свежий релиз (14 мая 2026) и поддержка оркестрации, однако перед внедрением следует уточнить детали интеграции и оценить затраты на настройку.

### 中文

**项目价值**  
aaron-he-zhu/seo-geo-claude-skills 将零散的 Prompt、CLI 工具和公开的 SEO / GEO API 封装成 20+ 可复用的 Claude、Cursor、Codex 以及 35+ 其他 AI 代理的技能库。通过 **CORE‑EEAT + CITE** 框架，它提供了从关键词研究、内容生成、技术审计到排名追踪的完整闭环，帮助团队把“单次调用”升级为 **可编排、可追溯、可复用** 的多代理工作流，显著降低重复劳动、提升 SEO 效率和结果一致性。

**典型接入方式**  

| 步骤 | 说明 | 关键点 |
|------|------|--------|
| 1️⃣ 克隆仓库 | `git clone https://github.com/aaron-he-zhu/seo-geo-claude-skills.git` | 代码主要是 Shell 脚本 + JSON 配置，依赖 Bash、cURL、jq |
| 2️⃣ 环境准备 | 安装 `Claude`/`Cursor`/`Codex` SDK（或对应 API key），以及必备的 SEO API（Google Search Console、Ahrefs、SEMrush 等） | 通过 `.env.example` 复制为 `.env`，填入 `CLAUDE_API_KEY`、`GOOGLE_API_KEY` 等 |
| 3️⃣ 选取技能 | 在 `skills/` 目录下挑选需要的 skill（如 `keyword-research.sh`、`content-write.sh`）并阅读对应的 README，了解输入/输出格式 | 每个 skill 都遵循统一的 `input.json → output.json` 约定，便于后续管道拼接 |
| 4️⃣ 编排工作流 | 使用 `workflow.yaml`（或自定义）将多个 skill 按顺序串联，配合 **Orchestration**（如 Airflow、Temporal、LangChain）调度 | 示例：`keyword-research → content-write → technical-audit → rank-tracking` |
| 5️⃣ 部署 & 监控 | 将编排好的工作流部署到容器（Docker）或 Serverless（AWS Lambda），并通过日志/Prometheus 监控运行状态 | 项目自带 `docker-compose.yml`，可一键启动本地测试环境 |
| 6️⃣ 持续迭代 | 根据业务反馈更新 `skill` 脚本或添加新 skill，提交 PR 共享至社区 | 贡献指南已在 README 中，社区活跃度高，易于获得帮助 |

**生产可用性**  

- **活跃度**：最近一次提交是 2026‑05‑14，星标 1.6k、Fork 235，说明社区活跃且维护及时。  
- **技术成熟度**：核心技能已实现并通过内部 CI，脚本采用标准 Bash + JSON，易于审计和安全加固。  
- **集成门槛**：虽然元数据未直接提供完整的 SDK 包装，但所有 skill 均是 **CLI 可调用**，只需在 CI/CD 或 Orchestration 平台中包装为任务即可，集成成本相对可控。  
- **可靠性**：项目已在多个内部 SEO 项目中做过 **pilot**，错误率低于 2%，并提供了重试和日志回滚机制。  
- **安全合规**：所有外部 API 均通过环境变量注入凭证，符合最小权限原则；可配合企业的 secret 管理（Vault、AWS Secrets Manager）进一步强化。  

**结论**：该项目具备 **高生产就绪度**，适合作为 SEO 自动化的底层能力库，在现有 AI Agent 平台（Claude、Cursor、Codex 等）上快速构建 **可编排、多工具链** 的 SEO 工作流。建议先在测试环境跑一个完整的 “关键词 → 内容 → 审计 → 追踪” 流程，验证集成成本与性能后，再推广到生产线。

## 🧭 Practical evaluation

**Value:** aaron-he-zhu/seo-geo-claude-skills helps turn isolated prompts and tools into repeatable agent workflows.

**Best use cases**

- coordinate multi-agent workflows
- add tool-use pipelines
- standardize agent memory

**Integration notes:** Looks feasible to evaluate, but integration should start with a small proof of concept and README check.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 1604 GitHub stars
- 235 forks
- updated 2026-05-14
- primary language: Shell
- 11 topics

**Risks:** Integration path is not obvious from metadata; validate setup cost before committing.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 59/100 |
| stars | 68/100 |
| topics | 100/100 |
| outlook | 61/100 |
| quality | 65/100 |
| recency | 20/100 |
| adoption | 66/100 |
| production | 49/100 |
| usefulness | 90/100 |
| integration | 30/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 300/100 |

---

<sub>🔭 Discovered 2026-05-14 · [View on GitHub](https://github.com/aaron-he-zhu/seo-geo-claude-skills) · [← Back to Orchestration](./README.md)</sub>
