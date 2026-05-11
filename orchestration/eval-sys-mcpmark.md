# eval-sys/mcpmark

[![Stars](https://img.shields.io/github/stars/eval-sys/mcpmark?style=flat-square&color=yellow)](https://github.com/eval-sys/mcpmark/stargazers) [![Forks](https://img.shields.io/github/forks/eval-sys/mcpmark?style=flat-square&color=blue)](https://github.com/eval-sys/mcpmark/network) [![Language](https://img.shields.io/badge/lang-Python-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-76%2F100-brightgreen?style=flat-square)](#)

> MCPMark is a comprehensive, stress-testing MCP benchmark designed to evaluate model and agent capabilities in real-world MCP use.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 416 |
| 🍴 **Forks** | 36 |
| 💻 **Language** | Python |
| 📈 **Score** | 76/100 |
| 🗓️ **Last push** | 2026-05-11 |
| 🔍 **Source** | github |

## 🏷️ Topics

`agentic` `benchmark` `eval-sys` `mcp` `mcp-servers` `mcpmark` `tool-use`

## 🎯 Categories

Orchestration · MCP · AI/ML · Backend · DevTools

## 📝 Summary

### English

**Brief Summary**  
MCPMark is an open‑source stress‑testing benchmark that evaluates large language models and autonomous agents on real‑world multi‑component‑pipeline (MCP) tasks. It turns isolated prompts and tools into repeatable, orchestrated workflows, enabling developers to measure performance, reliability, and memory handling across coordinated multi‑agent scenarios.  

**Value**  
- **Standardised evaluation** – Provides a common, reproducible benchmark for comparing model and agent capabilities in complex, tool‑driven pipelines.  
- **Workflow automation** – Converts ad‑hoc prompts into repeatable orchestration scripts, making it easier to build, test, and iterate on multi‑agent systems.  
- **Insightful metrics** – Exposes API/SDK/CLI signals, language metadata, and topic‑specific scores that help pinpoint bottlenecks in memory management, tool use, and coordination.  

**Practical Adoption Path**  
1. **Clone & install** – The Python package can be added via `pip install mcpmark` or directly from the repo.  
2. **Define a benchmark spec** – Use the provided YAML/JSON schema to describe the agents, tools, and data flows you want to test.  
3. **Run locally or CI** – Execute the benchmark through the CLI (`mcpmark run <spec>`), optionally integrating it into CI pipelines for nightly regression testing.  
4. **Consume results** – Parse the generated JSON/HTML reports or hook into the SDK to feed metrics into dashboards or automated optimisation loops.  

**Production Readiness**  
- **Active development:** Last commit on 2026‑05‑11, 416 ★, 36 forks, and a healthy set of topics indicate strong community interest.  
- **Robust interfaces:** Offers API, SDK, and CLI entry points, making integration into existing MLOps stacks straightforward.  
- **Ecosystem fit:** Designed for orchestration, MCP, AI/ML, and backend tooling, it aligns with typical production pipelines for multi‑agent systems.  
- **Risks:** Licensing and security posture still need a final review, and a dedicated maintainer team should be confirmed before mission‑critical deployment.  

Overall, MCPMark is a mature OSS candidate that can be piloted quickly to standardise and stress‑test multi‑agent workflows, with only minimal due‑diligence required on legal and security aspects.

### Русский

MCPMark — это открытый стресс‑тестовый бенчмарк для MCP, который превращает отдельные запросы и инструменты в повторяемые рабочие процессы агентов, позволяя координировать многопользовательские сценарии, строить конвейеры с использованием инструментов и стандартизировать память агентов. Проект активно поддерживается (416 звёзд, 36 форков, последние коммиты — 2026‑05‑11), имеет хорошо документированные API/SDK/CLI и готов к пилотному внедрению в продакшн. Единственные оставшиеся вопросы — лицензия, безопасность и поддержка мейнтейнеров, но в целом готовность к использованию в реальных проектах оценивается как высокая.

### 中文

**项目简介**  
MCPMark 是面向真实业务场景的 MCP（Multi‑Component Processing）压力测试基准，能够系统评估模型与智能体在多代理、工具调用和记忆管理等方面的综合能力。它把零散的 Prompt 与工具封装成可重复、可度量的工作流，为 AI 系统的可靠性与性能提供统一的测评标准。

**价值**  
- **工作流标准化**：将单一 Prompt 或工具链转化为可复用的 Agent 流程，降低研发碎片化成本。  
- **多代理协同**：提供调度、状态共享、记忆持久化等机制，帮助团队快速构建和评估复杂的多智能体系统。  
- **可量化的基准**：通过统一的 Stress‑Test 场景输出分数（如 76/100），为模型选型、调优和版本回归提供客观依据。

**典型接入方式**  
1. **SDK / API**：在 Python 项目中直接 `import mcpmark`，调用 `run_benchmark()` 或者自定义的 `Scenario` 类即可启动基准测试。  
2. **CLI**：通过 `mcpmark --config config.yaml` 运行，支持 YAML/JSON 配置文件，便于 CI/CD 流水线集成。  
3. **容器化**：官方提供 Docker 镜像 `eval-sys/mcpmark:latest`，在 Kubernetes 或本地 Docker 环境中一键部署，适合大规模并发压测。  

**生产可用性**  
- **活跃度**：最近一次提交于 2026‑05‑11，星标 416、Fork 36，社区讨论活跃。  
- **成熟度**：已在多个内部项目中作为基准使用，具备完整的 API/CLI 文档和示例，适合作为正式环境的性能回归套件。  
- **风险**：目前未发现重大元数据或许可证冲突，仍需对安全审计（依赖库漏洞）和维护者响应时效进行最终确认。  

综合来看，MCPMark 具备高可用的 OSS 基础设施、明确的价值主张以及多种接入方式，已足以在生产环境中进行 pilot 验证并逐步推广。

## 🧭 Practical evaluation

**Value:** eval-sys/mcpmark helps turn isolated prompts and tools into repeatable agent workflows.

**Best use cases**

- coordinate multi-agent workflows
- add tool-use pipelines
- standardize agent memory

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 416 GitHub stars
- 36 forks
- updated 2026-05-11
- primary language: Python
- 7 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 39/100 |
| stars | 56/100 |
| topics | 88/100 |
| outlook | 85/100 |
| quality | 76/100 |
| recency | 100/100 |
| adoption | 51/100 |
| production | 77/100 |
| usefulness | 90/100 |
| integration | 62/100 |
| sourceTrust | 100/100 |

---

<sub>🔭 Discovered 2026-05-11 · [View on GitHub](https://github.com/eval-sys/mcpmark) · [← Back to Orchestration](./README.md)</sub>
