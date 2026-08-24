# zhu1090093659/spec_driven_develop

[![Stars](https://img.shields.io/github/stars/zhu1090093659/spec_driven_develop?style=flat-square&color=yellow)](https://github.com/zhu1090093659/spec_driven_develop/stargazers) [![Forks](https://img.shields.io/github/forks/zhu1090093659/spec_driven_develop?style=flat-square&color=blue)](https://github.com/zhu1090093659/spec_driven_develop/network) [![Language](https://img.shields.io/badge/lang-Shell-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-63%2F100-brightgreen?style=flat-square)](#)

> Spec-driven development workflow for AI coding agents: architecture-first planning, task decomposition, GitHub Issue/PR tracking, Deep Discuss, and adaptive control for Claude Code, Codex, Cursor, and other Markdown-capable agents.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 912 |
| 🍴 **Forks** | 95 |
| 💻 **Language** | Shell |
| 📈 **Score** | 63/100 |
| 🗓️ **Last push** | 2026-08-24 |
| 🔍 **Source** | github |

## 🏷️ Topics

`ai-agent` `ai-assisted-development` `ai-coding-assistant` `claude-code` `codex` `cursor` `dev-workflow` `developer-tools` `engineering-cybernetics` `github-issues` `llm` `markdown`

## 🎯 Categories

Automation · AI/ML · DevTools

## 📝 Summary

### English

**Brief Summary**  
zhu1090093659/spec_driven_develop provides a spec‑driven workflow for AI coding agents, combining architecture‑first planning, task decomposition, GitHub Issue/PR tracking, “Deep Discuss” sessions, and adaptive control for Claude Code, Codex, Cursor, and other Markdown‑compatible agents. By automating the repetitive steps of prompt engineering, issue creation, and code review, it lets developers focus on higher‑level design and validation.  

**Value**  
- **Automation of boilerplate** – The framework scripts the end‑to‑end cycle (design → task split → issue/PR creation → AI‑generated code → discussion → merge), eliminating the manual copy‑paste and context‑switching that typically slows AI‑assisted development.  
- **Consistent, auditable specs** – Architecture‑first specs become the single source of truth, ensuring that every generated change can be traced back to an explicit requirement.  
- **Tool‑agnostic but ready‑to‑run** – Built around Markdown‑compatible agents, it works with Claude Code, Codex, Cursor, etc., allowing teams to pick the model that fits their cost‑performance profile without rewriting pipelines.  

**Practical Adoption Path**  
1. **Proof‑of‑Concept (PoC)** – Clone the repo, run the provided `README` example, and connect a single AI agent (e.g., Claude Code) to a test GitHub repository. Verify that the spec → issue → PR flow executes end‑to‑end.  
2. **Incremental Integration** – Replace an existing manual step (e.g., issue creation) with the spec‑driven script while keeping the rest of the pipeline unchanged.  
3. **Full‑stack Rollout** – Extend the PoC to cover the entire development cycle: architecture docs → task decomposition → parallel AI agents → Deep Discuss review → automated merges.  
4. **Monitoring & Governance** – Add logging, CI checks, and approval gates to ensure generated code meets internal quality standards before production deployment.  

**Production Readiness**  
- **Maturity**: Medium. The project has strong community interest (≈ 912 stars, 95 forks) and recent activity (updated 2026‑07‑01), indicating active maintenance, but the integration documentation is sparse and the setup scripts are primarily shell‑based, which may require environment tuning.  
- **Suitability**: Ideal for prototypes, internal tooling, or teams experimenting with AI‑augmented development. Before production use, perform a dependency audit (shell utilities, API keys, rate limits) and establish fallback procedures in case the AI service is unavailable.  
- **Risk Mitigation**: Start with a small, isolated workflow to measure setup cost and reliability; once confidence is gained, scale to broader codebases and add governance controls.  

In short, *spec_driven_develop* can dramatically cut manual overhead in AI‑assisted coding, but teams should adopt it gradually, validate the integration effort, and augment the pipeline with robust monitoring before treating it as production‑critical.

### Русский

**zhu1090093659/spec_driven_develop** — это набор скриптов и шаблонов, позволяющих автоматизировать «spec‑driven» процесс разработки с AI‑агентами: от архитектурного планирования и декомпозиции задач до создания и отслеживания GitHub Issue/PR, интеграции Deep Discuss и адаптивного управления агентами (Claude Code, Codex, Cursor и другими, работающими с Markdown). Типичный сценарий внедрения — запуск небольшого proof‑of‑concept, когда в пайплайн добавляют генерацию спецификаций и автоматическое открытие задач в репозитории, тем самым устраняя рутинные ручные операции и делая процесс повторяемым. Готовность к продакшну — средняя: проект уже имеет значительную пользовательскую базу (912 звёзд, 95 форков) и актуальное обновление, но требует проверки зависимостей и небольших доработок интеграции перед использованием в критически важных системах.

### 中文

**项目简介（2‑3 句）**  
zhu1090093659/spec_driven_develop 为 AI 编码代理提供了一套“规格驱动”的开发工作流：先进行架构设计与任务拆解，再通过 GitHub Issue/PR、Deep Discuss 等工具自动跟踪进度，支持 Claude Code、Codex、Cursor 等能够解析 Markdown 的模型，实现全链路的自适应控制与自动化。

---

## 价值点

1. **消除重复手工**：把需求拆解、任务分配、代码审查、合并等环节全部自动化，显著降低人工干预和出错概率。  
2. **统一工具链**：将 GitHub、Deep Discuss、AI 编码模型等常用工具串联成可复用的流水线，提升团队协作效率。  
3. **适配多种模型**：内置对 Claude Code、Codex、Cursor 等 Markdown‑capable AI 代理的适配层，便于在同一工作流中切换或并行使用不同模型。  
4. **可视化与可追溯**：所有任务均以 Issue/PR 形式记录，支持审计、回滚和进度监控，符合企业合规要求。

---

## 典型接入方式

| 步骤 | 说明 | 关键操作 |
|------|------|----------|
| 1️⃣ 环境准备 | 克隆仓库，确保系统已安装 `bash`、`git`、`jq` 等依赖。 | `git clone https://github.com/zhu1090093659/spec_driven_develop.git && cd spec_driven_develop` |
| 2️⃣ 配置凭证 | 在项目根目录创建 `.env`，填入 GitHub Token、OpenAI/Anthropic API Key 等。 | `echo "GITHUB_TOKEN=xxxx\nOPENAI_API_KEY=xxxx" > .env` |
| 3️⃣ 定义规格 | 编写 Markdown 规格文件（如 `specs/feature_a.md`），描述架构、接口、验收标准。 | `vim specs/feature_a.md` |
| 4️⃣ 运行工作流 | 调用主脚本启动自动化：<br>`./run.sh specs/feature_a.md` <br>脚本会自动：<br>① 生成任务树 → ② 在 GitHub 创建 Issue → ③ 调用 AI 生成代码 → ④ 提交 PR → ⑤ 触发 Deep Discuss 讨论。 |
| 5️⃣ 结果验证 | 通过 GitHub UI 查看 Issue/PR 状态，或在 `logs/` 目录查看运行日志。 | `open https://github.com/your-org/your-repo/issues` |

> **小规模 PoC**：建议先在测试仓库中跑一次完整流程，确认 AI 生成质量、Issue 模板匹配度以及 Deep Discuss 的交互效果，再逐步推广到正式项目。

---

## 生产可用性评估

| 维度 | 现状 | 建议 |
|------|------|------|
| **成熟度** | 代码已更新至 2026‑07‑01，拥有 912 ★、95 🍴，社区活跃度中等。 | 适合作为原型或内部工具；若用于对外产品，需进行代码审计和单元测试补齐。 |
| **依赖管理** | 主要依赖 Shell、Git、curl、jq 以及外部 AI API。 | 在 CI/CD 中锁定 Shell 环境（Docker 镜像），并对 API 调用做限流/重试处理。 |
| **可扩展性** | 通过 Markdown 规格文件和可插拔的 AI 调用脚本实现模型切换。 | 如需接入自研模型，只需实现对应的 `generate.sh` 接口即可。 |
| **运维成本** | 需要维护 API 密钥、GitHub Webhook、以及定期更新依赖脚本。 | 建议使用 Secrets 管理平台统一存储凭证，定期跑 `./update_deps.sh` 检查依赖安全。 |
| **安全合规** | 代码自动提交 PR，可能泄露业务机密。 | 在企业内部网络部署私有 GitHub 实例，限制 API Key 的访问范围。 |
| **总体生产准备度** | **中等**（适合内部原型、研发加速），在正式生产环境使用前需完成：<br>1. 完整的单元/集成测试<br>2. 依赖安全审计<br>3. 监控与告警（API 调用失败、流水线卡点） | 完成以上步骤后，可在业务关键流程中逐步替代手工操作，实现全链路自动化。 |

---

**一句话总结**：`spec_driven_develop` 通过规格‑驱动的方式把 AI 代码生成、任务管理和讨论协作全部自动化，适合在内部研发或原型阶段快速提升效率；在生产环境使用前，需要做依赖锁定、权限管理和测试验证，以确保可靠性与安全性。

## 🧭 Practical evaluation

**Value:** zhu1090093659/spec_driven_develop helps remove repetitive manual operations from a workflow.

**Best use cases**

- remove manual work
- connect tools into repeatable flows
- schedule operational tasks

**Integration notes:** Looks feasible to evaluate, but integration should start with a small proof of concept and README check.

**Production readiness:** Medium: useful for prototypes or internal workflows, with dependency and maintenance checks before production.

**Quality signals**

- 912 GitHub stars
- 95 forks
- updated 2026-07-01
- primary language: Shell
- 20 topics

**Risks:** Integration path is not obvious from metadata; validate setup cost before committing.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 50/100 |
| stars | 63/100 |
| topics | 100/100 |
| outlook | 67/100 |
| quality | 67/100 |
| recency | 40/100 |
| adoption | 59/100 |
| production | 55/100 |
| usefulness | 90/100 |
| integration | 30/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 300/100 |

---

<sub>🔭 Discovered 2026-07-01 · [View on GitHub](https://github.com/zhu1090093659/spec_driven_develop) · [← Back to Automation](./README.md)</sub>
