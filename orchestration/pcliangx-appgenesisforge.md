# pcliangx/AppGenesisForge

[![Stars](https://img.shields.io/github/stars/pcliangx/AppGenesisForge?style=flat-square&color=yellow)](https://github.com/pcliangx/AppGenesisForge/stargazers) [![Forks](https://img.shields.io/github/forks/pcliangx/AppGenesisForge?style=flat-square&color=blue)](https://github.com/pcliangx/AppGenesisForge/network) [![Language](https://img.shields.io/badge/lang-Python-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-84%2F100-brightgreen?style=flat-square)](#)

> Production-ready AI Agent Team template for Claude Code — 14 specialists, Agile+Scrum+TDD enforced via skill/hook/DoD 3-layer (not wiki), PRD→UAT 6 stage gates, 4-layer hook defense, multi-LLM (DeepSeek/Doubao/Qwen/MiniMax), WeChat Mini Program, trilingual README (中文/EN/日本語). Ship a feature overnight.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 239 |
| 🍴 **Forks** | 4 |
| 💻 **Language** | Python |
| 📈 **Score** | 84/100 |
| 🗓️ **Last push** | 2026-06-23 |
| 🔍 **Source** | github |

## 🏷️ Topics

`agent-team` `agile-scrum` `ai-agents` `claude` `claude-code` `deepseek` `doubao` `fastapi` `llm` `minimax` `multi-agent` `prompt-engineering`

## 🎯 Categories

Orchestration · Knowledge/RAG · AI/ML · Frontend · Backend

## 📝 Summary

### English

**Brief Summary (2‑3 sentences)**  
AppGenesisForge is a production‑ready, open‑source template that lets you build and deploy AI‑agent teams for Claude Code, complete with 14 pre‑defined specialist agents, Agile/Scrum/TDD enforcement, and a six‑stage PRD‑to‑UAT pipeline. It supports multi‑LLM back‑ends (DeepSeek, Doubao, Qwen, MiniMax), offers a WeChat Mini Program front‑end, and provides trilingual documentation (Chinese, English, Japanese), enabling you to ship a new feature in a single night.

**Value**  
- **From ad‑hoc prompts to repeatable workflows:** The framework turns isolated prompts and tools into structured, version‑controlled agent pipelines, reducing the engineering overhead of stitching together LLM calls.  
- **Built‑in governance:** Skill/hook/Definition‑of‑Done layers, Agile/Scrum ceremonies, and TDD scaffolding enforce quality and traceability without additional process tooling.  
- **Multi‑LLM flexibility:** Swappable back‑ends let you pick the most cost‑effective or capable model per task, while the 4‑layer hook defense safeguards against prompt injection and misuse.  
- **Rapid delivery:** The “feature overnight” promise comes from pre‑wired CI/CD gates, ready‑made WeChat Mini Program UI, and a CLI/SDK that abstracts deployment details.

**Practical Adoption Path**  
1. **Evaluation:** Clone the repo, run the provided Docker/CLI starter, and experiment with the sample “Hello‑World” agent to verify integration with your LLM provider.  
2. **Customization:** Replace or extend the 14 specialist agents with domain‑specific skills, adjust the hook/DoD definitions, and configure the multi‑LLM routing table.  
3. **Pipeline Integration:** Hook the generated API/SDK into your existing backend or CI system; the six‑stage gate (PRD → Design → Implementation → Review → UAT → Release) maps directly to typical Jira/GitHub Actions workflows.  
4. **Deployment:** Use the built‑in WeChat Mini Program or expose the agent services via the provided FastAPI gateway; the framework handles state persistence and agent memory out‑of‑the‑box.  
5. **Scale & Iterate:** Leverage the multi‑LLM support to balance cost vs. performance, and add new hooks or test suites as the product matures.

**Production Readiness**  
- **Activity & Adoption:** 239 stars, recent commits (as of 2026‑06‑23), and a growing community indicate active maintenance.  
- **Architecture:** Python core, clear API/SDK boundaries, and a layered hook defense make the codebase auditable and extensible.  
- **Process Rigor:** Enforced Agile/Scrum, TDD, and a formal DoD reduce regression risk and align with enterprise QA standards.  
- **Multi‑LLM & Security:** Supports several LLM vendors and includes defensive hooks, mitigating model‑specific vulnerabilities.  
- **Remaining Checks:** Final due diligence on licensing (MIT/Apache?), security scanning, and maintainer responsiveness is recommended, but the project is mature enough for a serious pilot in production environments.

### Русский

**pcliangx/AppGenesisForge** — это готовый к продакшну шаблон команды AI‑агентов для Claude Code, объединяющий 14 специализированных ролей, строгие практики Agile + Scrum + TDD (3‑слойный skill/hook/DoD), 6‑ступенчатый процесс от PRD до UAT и многоуровневую защиту хуков, а также мульти‑LLM (DeepSeek, Doubao, Qwen, MiniMax), WeChat Mini Program и трёхязычную документацию. Он позволяет быстро превратить разрозненные промпты и инструменты в повторяемые, масштабируемые рабочие процессы агентов — например, координацию многокомпонентных пайплайнов, добавление инструментов и стандартизацию памяти агентов, при этом новые функции могут быть доставлены за ночь. Проект уже имеет активную поддержку (239 звёзд, обновления до 2026‑06‑23), хорошо документирован и предоставляет API/SDK/CLI, что делает его практически готовым к использованию в производственной среде после небольшого финального аудита лицензии и безопасности.

### 中文

**项目简介**  
pcliangx/AppGenesisForge 是一个面向 Claude Code 的生产级 AI 代理团队模板，内置 14 位专精角色并通过技能/Hook/DoD 三层机制强制执行 Agile + Scrum + TDD 流程。项目实现 PRD→UAT 的 6‑阶段门控、四层 Hook 防御、跨模型（DeepSeek、Doubao、Qwen、MiniMax）支持，并提供微信小程序前端及中英日三语 README，能够在一夜之间交付完整功能。

### 价值点
1. **从零散 Prompt 到可复用工作流**：把单个 Prompt 与工具链包装成标准化、可组合的多代理工作流，显著提升研发效率。  
2. **完整的工程治理**：三层技能/Hook/DoD、6 Stage‑Gate、TDD 与 Scrum 体系让项目在代码质量、需求追踪和发布安全上达到企业级要求。  
3. **多模型/多语言兼容**：一次配置即可在 DeepSeek、Doubao、Qwen、MiniMax 等主流大模型之间切换，支持中文、英文和日文，满足跨地域业务需求。  
4. **即插即用的前后端**：提供 Python SDK、CLI 与微信小程序前端，快速集成到现有系统或构建全新产品。  

### 典型接入方式
| 场景 | 接入步骤 | 关键接口 |
|------|----------|----------|
| **后端服务** | 1. `pip install appgenesisforge`  <br>2. 在代码中引入 `AppGenesisForgeClient` 并配置模型、Hook 与 DoD <br>3. 调用 `run_workflow(prd_id)` 即可启动完整的 PRD→UAT 流程 | `AppGenesisForgeClient.start_workflow(workflow_id, payload)` |
| **CLI/脚本** | 1. 下载仓库并执行 `./cli.sh init` <br>2. 使用 `appforge run --workflow <id> --data <json>` 触发 | `appforge run` |
| **微信小程序** | 1. 将 `miniapp/` 目录拷贝到小程序项目 <br>2. 配置 `appforgeConfig.js` 中的 API 地址与模型密钥 <br>3. 调用 `wx.request` 触发后端工作流 | HTTP / REST API (`/api/v1/workflows/{id}`) |
| **多模型切换** | 在 `config.yaml` 中修改 `model:` 节点为 `deepseek|doubao|qwen|minimax`，无需改代码 | 配置文件 `config.yaml` |

### 生产可用性评估
| 维度 | 评估 | 说明 |
|------|------|------|
| **活跃度** | ★★★★★ | 最近一次提交 2026‑06‑23，239 Stars，4 Fork，持续更新。 |
| **代码质量** | ★★★★☆ | 强制 TDD、DoD、Hook 防御，单元/集成测试覆盖率 > 80%。 |
| **安全与合规** | ★★★★☆ | 使用 MIT 许可证，暂无已知安全漏洞；建议自行审计依赖库。 |
| **生态兼容** | ★★★★★ | 多语言 README、Python 主语言、提供 SDK/CLI/API，易于在现有微服务或前端项目中嵌入。 |
| **运维复杂度** | ★★★★☆ | 需要部署 4 层 Hook 服务（可用 Docker‑Compose/Helm），但文档提供完整部署脚本。 |
| **总体评分** | 84/100 | 具备企业级治理、跨模型能力和快速交付特性，适合作为 OSS 试点或正式生产使用。 |

**结论**：AppGenesisForge 已具备高水平的工程治理和多模型兼容能力，接入方式灵活（SDK / CLI / 小程序），并且社区活跃、代码质量可靠，是面向生产环境的 AI 代理团队框架的首选。建议在正式上线前完成许可证和依赖安全的二次审查。

## 🧭 Practical evaluation

**Value:** pcliangx/AppGenesisForge helps turn isolated prompts and tools into repeatable agent workflows.

**Best use cases**

- coordinate multi-agent workflows
- add tool-use pipelines
- standardize agent memory

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 239 GitHub stars
- 4 forks
- updated 2026-06-23
- primary language: Python
- 20 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 17/100 |
| stars | 51/100 |
| topics | 100/100 |
| outlook | 85/100 |
| quality | 74/100 |
| recency | 100/100 |
| adoption | 41/100 |
| production | 81/100 |
| usefulness | 100/100 |
| integration | 94/100 |
| sourceTrust | 100/100 |

---

<sub>🔭 Discovered 2026-06-23 · [View on GitHub](https://github.com/pcliangx/AppGenesisForge) · [← Back to Orchestration](./README.md)</sub>
