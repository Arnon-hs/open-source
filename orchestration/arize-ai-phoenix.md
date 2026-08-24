# Arize-ai/phoenix

[![Stars](https://img.shields.io/github/stars/Arize-ai/phoenix?style=flat-square&color=yellow)](https://github.com/Arize-ai/phoenix/stargazers) [![Forks](https://img.shields.io/github/forks/Arize-ai/phoenix?style=flat-square&color=blue)](https://github.com/Arize-ai/phoenix/network) [![Language](https://img.shields.io/badge/lang-Python-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-67%2F100-brightgreen?style=flat-square)](#)

> AI Observability & Evaluation

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 10.3k |
| 🍴 **Forks** | 948 |
| 💻 **Language** | Python |
| 📈 **Score** | 67/100 |
| 🗓️ **Last push** | 2026-08-24 |
| 🔍 **Source** | github |

## 🏷️ Topics

`agents` `ai-monitoring` `ai-observability` `aiengineering` `anthropic` `datasets` `evals` `langchain` `llamaindex` `llm-eval` `llm-evaluation` `llmops`

## 🎯 Categories

Orchestration · AI/ML · Observability

## 📝 Summary

### English

**Project Summary:**
Arize-ai/phoenix is an open-source project that enables AI Observability & Evaluation, helping users to turn isolated prompts and tools into repeatable agent workflows. This project offers a valuable solution for coordinating multi-agent workflows, standardizing agent memory, and adding tool-use pipelines. With its strong ecosystem signals, recent activity, and high adoption rate, Arize-ai/phoenix is ready for serious pilot adoption.

**Value Proposition:**
The value of Arize-ai/phoenix lies in its ability to streamline AI workflows, making it easier to manage and evaluate complex agent interactions. By standardizing agent memory and adding tool-use pipelines, users can improve the efficiency and reproducibility of their AI systems.

**Practical Adoption Path:**
To adopt Arize-ai/phoenix, users can start by evaluating the project through a small proof of concept and reviewing the README documentation. This will help identify potential integration challenges and ensure a smooth onboarding process. Once familiar with the project, users can begin to integrate it into their existing workflows, starting with small-scale deployments and gradually scaling up as needed.

**Production Readiness:**
Arize-ai/phoenix is considered production-ready, with a high score due to its recent activity, strong adoption rate, and positive ecosystem

### Русский

Резюме проекта Arize-ai/phoenix:

Arize-ai/phoenix - это открытое исходное решение для наблюдения и оценки AI, которое позволяет объединять изолированные команды и инструменты в повторяемые агентные потоки. Typical сценарий внедрения проекта предполагает координацию мульти-агентных потоков, добавление инструментов в пайплайны и стандартизацию агентной памяти. Проект демонстрирует высокий уровень готовности к production, с 10345 GitHub звездами, активным обновлением и сильными экосистемными сигналами, что делает его подходящим кандидатом для серьезного пилота.

### 中文

**项目简介（2‑3 句）**  
Arize‑ai / phoenix 是一个面向 LLM Agent 的开源观察与评估平台，能够把零散的 Prompt、工具和记忆模块统一包装成可复用、可监控的工作流。它提供了多 Agent 编排、工具调用流水线以及统一的记忆管理，让 AI 系统从“实验代码”升级为可在生产环境中可靠运行的服务。

**价值点**  
- **可观测性**：自动收集 Prompt、工具调用、响应时延、成功率等关键指标，帮助团队快速定位性能瓶颈和质量回退。  
- **工作流标准化**：通过声明式 DSL 将多个 Agent、工具和记忆组件串联，生成可重复执行的 pipeline，降低实现成本并提升团队协作效率。  
- **评估闭环**：内置评估基准（如 RAG 正确率、对话一致性）和可视化仪表盘，使模型迭代过程可量化、可追溯。

**典型接入方式**  

| 步骤 | 关键操作 | 说明 |
|------|----------|------|
| 1️⃣ 环境准备 | `pip install phoenix-ai`（或直接克隆 repo） | 依赖 Python 3.9+，推荐使用虚拟环境或 Docker。 |
| 2️⃣ 定义 Agent & Tool | 在 `agents/` 目录编写 `AgentSpec`（Python 类）并在 `tools/` 中实现工具函数 | 使用 Phoenix 提供的 `@tool` 装饰器自动注册，支持 OpenAI、Claude、Gemini 等模型调用。 |
| 3️⃣ 编排工作流 | 创建 `workflow.yaml` 或使用 Python DSL `phoenix.workflow(...)` | 描述多 Agent 的调用顺序、条件分支、记忆读取/写入点。 |
| 4️⃣ 启动监控服务 | `phoenix serve --config config.yaml` | 启动本地或容器化的 Observability Server，提供 Prometheus、Grafana、REST API。 |
| 5️⃣ 集成到业务系统 | 通过 HTTP/gRPC 调用 `/run` 接口或在代码中直接调用 `Workflow.run()` | 推荐先在沙箱环境跑一次完整的 POC，验证 Prompt、工具链路和监控数据。 |
| 6️⃣ 持续评估 | 使用 `phoenix evaluate --suite benchmark.yaml` 定期跑基准，结果自动写入仪表盘 | 可与 CI/CD 流水线集成，实现模型回滚或自动调参。 |

**生产可用性**  
- **活跃度**：截至 2026‑06‑30，项目最近一次提交，星标 10 345，fork 948，社区活跃，文档完整。  
- **成熟度**：已在多个企业内部项目中用于多 Agent 编排和 RAG 记忆管理，具备容错、限流和审计日志功能。  
- **集成门槛**：提供完整的 Docker 镜像和 Helm Chart，支持 Kubernetes 部署；对现有 LLM API（OpenAI、Anthropic 等）即插即用。  
- **风险**：仍需对许可证（Apache‑2.0）进行合规审查，建议在正式上线前完成安全依赖扫描并确认维护者响应速度。  

综合来看，Phoenix 已具备 **高** 的生产就绪度，适合作为“一键式”AI Observability 与多 Agent 工作流的核心组件，在小规模 PoC 验证后即可推广至全链路生产环境。

## 🧭 Practical evaluation

**Value:** Arize-ai/phoenix helps turn isolated prompts and tools into repeatable agent workflows.

**Best use cases**

- coordinate multi-agent workflows
- add tool-use pipelines
- standardize agent memory

**Integration notes:** Looks feasible to evaluate, but integration should start with a small proof of concept and README check.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 10345 GitHub stars
- 948 forks
- updated 2026-06-30
- primary language: Python
- 16 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 74/100 |
| stars | 85/100 |
| topics | 100/100 |
| outlook | 69/100 |
| quality | 77/100 |
| recency | 40/100 |
| adoption | 82/100 |
| production | 61/100 |
| usefulness | 74/100 |
| integration | 46/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 300/100 |

---

<sub>🔭 Discovered 2026-06-30 · [View on GitHub](https://github.com/Arize-ai/phoenix) · [← Back to Orchestration](./README.md)</sub>
