# fancyboi999/open-tag

[![Stars](https://img.shields.io/github/stars/fancyboi999/open-tag?style=flat-square&color=yellow)](https://github.com/fancyboi999/open-tag/stargazers) [![Forks](https://img.shields.io/github/forks/fancyboi999/open-tag?style=flat-square&color=blue)](https://github.com/fancyboi999/open-tag/network) [![Language](https://img.shields.io/badge/lang-TypeScript-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-60%2F100-brightgreen?style=flat-square)](#)

> Open-source, self-hostable alternative to Claude Tag — a Slack-style workspace where your team and its AI agents (Claude Code, Codex, GitHub Copilot, and more) work as teammates in channels, threads, DMs, and shared tasks. Your data stays on your machines.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 43 |
| 🍴 **Forks** | 7 |
| 💻 **Language** | TypeScript |
| 📈 **Score** | 60/100 |
| 🗓️ **Last push** | 2026-08-24 |
| 🔍 **Source** | github |

## 🏷️ Topics

`agentic-workflows` `agents` `ai-agents` `chatops` `claude-code` `claude-tag` `codex` `collaboration` `llm` `local-first` `loop-engineering` `multi-agent`

## 🎯 Categories

Orchestration · AI/ML

## 📝 Summary

### English

**Project Summary:**

fancyboi999/open-tag is an open-source, self-hostable platform that enables teams to collaborate with AI agents, such as Claude Code, Codex, and GitHub Copilot, in a Slack-style workspace. By integrating these agents into workflows, teams can streamline tasks and improve productivity. This platform keeps data on local machines, ensuring data security and control.

**Value:**

The value proposition of fancyboi999/open-tag lies in its ability to turn isolated prompts and tools into repeatable agent workflows. This allows teams to standardize agent memory, add tool-use pipelines, and coordinate multi-agent workflows, ultimately improving team collaboration and productivity.

**Practical Adoption Path:**

To adopt fancyboi999/open-tag, teams can start by evaluating the project through a small proof of concept and README check. This will help identify potential integration challenges and dependencies. Once the feasibility is established, teams can begin to integrate the platform into their workflows, starting with internal prototypes or small-scale production environments. Before scaling up to larger production environments, teams should conduct thorough dependency and maintenance checks.

**Production Readiness:**

The production readiness of fancyboi999/open-tag is considered medium. While the project has shown some promise, with 43 GitHub stars and 7 forks,

### Русский

**fancyboi999/open-tag** — это открытая, самохостимая альтернатива Claude Tag, позволяющая собрать в едином Slack‑подобном пространстве команду людей и AI‑агентов (Claude Code, Codex, GitHub Copilot и др.) для совместной работы в каналах, ветках, личных сообщениях и общих задачах, при этом все данные остаются на ваших серверах. Типичный сценарий внедрения — запуск небольшого proof‑of‑concept, где в канал интегрируются несколько агентов для автоматизации цепочек инструментов (например, генерация кода → проверка → деплой), после чего workflow масштабируется в продуктивную среду после проверки зависимостей и безопасности. Готовность к production — средняя: проект пригоден для прототипов и внутренних процессов, но требует дополнительного аудита лицензий, безопасности и поддержки перед широким развертыванием.

### 中文

**项目简介**  
fancyboi999/open-tag 是一个开源、可自托管的 “Claude Tag” 替代品——类似 Slack 的协作工作区，团队成员和 AI 代理（Claude Code、Codex、GitHub Copilot 等）可以在频道、线程、私聊和共享任务中并肩工作，所有数据都保存在本地机器上。

**价值主张**  
- **把孤立的 Prompt 与工具串联成可复用的工作流**，让多代理协同、工具链调用和记忆管理变得标准化、可追踪。  
- **数据完全自控**：无需将业务信息上传至云服务，符合隐私合规和安全要求。  
- **灵活的插件式架构**：支持自定义 Agent、工具以及任务模板，适配不同业务场景（如代码审查、自动化报告、营销内容生成等）。

**典型接入方式**  
1. **快速 PoC**：克隆仓库 → 按 README 安装依赖（Node.js ≥ 18、Docker 可选） → 配置本地 `.env`（API Key、数据库路径） → 启动 `npm run dev`，在浏览器访问默认 UI。  
2. **业务集成**：在现有系统中通过 REST/WebSocket API 与 open‑tag 交互，或使用提供的 SDK（TypeScript）在代码中创建、调度、监听 Agent 任务。  
3. **CI/CD 与自动化**：将工作流定义保存为 JSON/YAML，配合 GitOps 在容器化环境（K8s、Docker‑Compose）中部署，实现持续交付与版本化管理。

**生产可用性评估**  
- **成熟度**：GitHub Stars ≈ 43、Forks ≈ 7，最近一次提交在 2026‑07‑01，代码基于 TypeScript，具备基本的单元测试和 CI。  
- **适用场景**：非常适合作为原型平台或内部工具，帮助团队快速验证多 Agent 协同流程。  
- **风险与准备工作**  
  - 需自行审查许可证（MIT/Apache 等）以及依赖的安全漏洞。  
  - 检查第三方 AI 服务的访问凭证和配额，防止生产环境突发费用。  
  - 对关键业务建议进行容器化部署并加入监控、日志、备份等运维措施。  
- **结论**：在完成依赖安全审计、完善 CI/CD 与运维监控后，open‑tag 可在内部生产环境中稳定运行；对外部高可用、弹性伸缩需求则需要进一步的架构强化（如水平扩容、数据库复制等）。

## 🧭 Practical evaluation

**Value:** fancyboi999/open-tag helps turn isolated prompts and tools into repeatable agent workflows.

**Best use cases**

- coordinate multi-agent workflows
- add tool-use pipelines
- standardize agent memory

**Integration notes:** Looks feasible to evaluate, but integration should start with a small proof of concept and README check.

**Production readiness:** Medium: useful for prototypes or internal workflows, with dependency and maintenance checks before production.

**Quality signals**

- 43 GitHub stars
- 7 forks
- updated 2026-07-01
- primary language: TypeScript
- 17 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 23/100 |
| stars | 35/100 |
| topics | 100/100 |
| outlook | 60/100 |
| quality | 54/100 |
| recency | 40/100 |
| adoption | 32/100 |
| production | 53/100 |
| usefulness | 90/100 |
| integration | 46/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 200/100 |

---

<sub>🔭 Discovered 2026-07-01 · [View on GitHub](https://github.com/fancyboi999/open-tag) · [← Back to Orchestration](./README.md)</sub>
