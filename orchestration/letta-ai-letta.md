# letta-ai/letta

[![Stars](https://img.shields.io/github/stars/letta-ai/letta?style=flat-square&color=yellow)](https://github.com/letta-ai/letta/stargazers) [![Forks](https://img.shields.io/github/forks/letta-ai/letta?style=flat-square&color=blue)](https://github.com/letta-ai/letta/network) [![Language](https://img.shields.io/badge/lang-Python-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-59%2F100-brightgreen?style=flat-square)](#)

> Letta is the platform for building stateful agents: AI with advanced memory that can learn and self-improve over time.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 22.7k |
| 🍴 **Forks** | 2.4k |
| 💻 **Language** | Python |
| 📈 **Score** | 59/100 |
| 🗓️ **Last push** | 2026-08-24 |
| 🔍 **Source** | github |

## 🏷️ Topics

`ai` `ai-agents` `llm` `llm-agent`

## 🎯 Categories

Orchestration · AI/ML

## 📝 Summary

### English

**Brief summary**  
Letta (letta‑ai/letta) is an open‑source platform that lets developers build stateful AI agents with persistent memory, enabling them to learn, self‑improve, and orchestrate complex multi‑agent workflows. It turns isolated prompts and tool calls into reusable, versioned pipelines, making it easy to add memory‑backed reasoning, tool‑use, and coordination across agents.

**Value**  
- **Advanced memory**: Agents retain context across sessions, allowing cumulative learning and more coherent interactions.  
- **Workflow orchestration**: Provides a unified framework to chain prompts, tools, and multiple agents, turning ad‑hoc scripts into repeatable pipelines.  
- **Standardisation**: Offers a common API for memory storage, tool integration, and agent lifecycle, reducing engineering overhead when scaling AI‑driven products.  

**Practical adoption path**  
1. **Proof‑of‑concept** – Clone the repo, run the provided examples, and verify the README steps on a small task (e.g., a single‑agent Q&A with memory).  
2. **Integration layer** – Wrap existing prompt templates or tool APIs with Letta’s agent interface, using its Python SDK to plug in your data stores or LLM providers.  
3. **Pilot workflow** – Deploy a minimal multi‑agent pipeline (e.g., a planner + executor) in a sandbox environment, instrumenting logs and evaluating memory persistence.  
4. **Scale & customise** – Extend the memory backend, add custom tool adapters, and integrate with your production orchestration (Kubernetes, Airflow, etc.).  

**Production readiness**  
- **Activity & adoption**: 22 k+ GitHub stars, 2.4 k forks, frequent commits (last update 2026‑05‑14) and a growing user community indicate strong momentum.  
- **Technical maturity**: Core written in Python, well‑documented SDK, and clear separation of concerns (orchestration, memory, tool adapters) make it production‑grade.  
- **Risk considerations**: License compatibility, security scanning, and maintainer responsiveness still need a final review, but no major metadata red flags were found. Overall, Letta is a solid OSS candidate for a serious pilot and can be hardened for production with standard code‑review and dependency‑audit processes.

### Русский

**Letta** — это открытая платформа для создания состояний‑ориентированных AI‑агентов с расширенной памятью, позволяющая превращать разрозненные подсказки и инструменты в повторяемые, самосовершенствующиеся рабочие процессы. Типичное внедрение начинается с небольшого proof‑of‑concept: интегрировать Letta в существующий пайплайн, задать базовый сценарий многoагентного взаимодействия и добавить инструменты через готовые коннекторы, после чего масштабировать на более сложные цепочки и долговременную память. Проект считается почти готовым к production: активные коммиты, 22 k★, 2.4 k форков, поддержка Python и стабильный набор функций, однако перед полномасштабным запуском следует проверить лицензию, безопасность и наличие активных мейнтейнеров.

### 中文

**项目简介**  
Letta（letta‑ai/letta）是一个用于构建 **stateful agents** 的平台，提供可持久化、可自我学习的记忆机制，使 AI 能够在多轮交互和长期任务中不断进化。它把零散的 Prompt 与工具链组织成可复用的 Agent 工作流，从而实现多代理协同、工具调用流水线以及统一的记忆管理。

**价值体现**  
- **提升效率**：将分散的 Prompt、工具和数据统一到可编排的工作流中，降低重复开发成本。  
- **增强智能**：内置持久记忆让 Agent 能记住历史上下文，实现更自然的对话和持续学习。  
- **可扩展性**：支持多 Agent 协同、插件式工具调用，适配各种业务场景（教育、客服、数据分析等）。

**典型接入方式**  
1. **快速原型**：克隆仓库，阅读 `README`，按照示例创建一个最小的 Agent 配置文件（YAML/JSON），在本地运行 `letta run` 验证功能。  
2. **代码集成**：在 Python 项目中通过 `pip install letta` 引入 SDK，使用 `Le​ttaAgent` 类实例化并注入自定义工具函数或数据库后端。  
3. **生产化部署**：将 Agent 配置和持久化存储（如 PostgreSQL、Redis）打包为 Docker 镜像，配合 Kubernetes 的 Job/Deployment 进行弹性伸缩；通过 API Gateway 暴露统一的调用入口。

**生产可用性**  
- **活跃度**：截至 2026‑05‑14，项目最近一次提交，拥有 22 716 颗星、2 414 次 fork，社区活跃。  
- **技术成熟度**：核心使用 Python 实现，提供完整的文档、示例和 CI/CD 流水线；可直接对接常见数据库和向量搜索引擎。  
- **风险评估**：暂无重大元数据风险，仍需对许可证（MIT/Apache 等）和安全依赖进行最终审查。总体上，项目已具备 **高** 的生产候选级别，适合先在小范围 PoC 验证后逐步推广至正式环境。

## 🧭 Practical evaluation

**Value:** letta-ai/letta helps turn isolated prompts and tools into repeatable agent workflows.

**Best use cases**

- coordinate multi-agent workflows
- add tool-use pipelines
- standardize agent memory

**Integration notes:** Looks feasible to evaluate, but integration should start with a small proof of concept and README check.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 22716 GitHub stars
- 2414 forks
- updated 2026-05-14
- primary language: Python
- 4 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 85/100 |
| stars | 93/100 |
| topics | 50/100 |
| outlook | 56/100 |
| quality | 68/100 |
| recency | 20/100 |
| adoption | 90/100 |
| production | 53/100 |
| usefulness | 58/100 |
| integration | 46/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 200/100 |

---

<sub>🔭 Discovered 2026-05-14 · [View on GitHub](https://github.com/letta-ai/letta) · [← Back to Orchestration](./README.md)</sub>
