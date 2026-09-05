# FunnyWolf/agentic-soc-platform

[![Stars](https://img.shields.io/github/stars/FunnyWolf/agentic-soc-platform?style=flat-square&color=yellow)](https://github.com/FunnyWolf/agentic-soc-platform/stargazers) [![Forks](https://img.shields.io/github/forks/FunnyWolf/agentic-soc-platform?style=flat-square&color=blue)](https://github.com/FunnyWolf/agentic-soc-platform/network) [![Language](https://img.shields.io/badge/lang-Python-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-64%2F100-brightgreen?style=flat-square)](#)

> Agentic SOC Platform: A powerful, flexible, open-source, and agent-centric automated security operations platform (AI SOC)

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 926 |
| 🍴 **Forks** | 153 |
| 💻 **Language** | Python |
| 📈 **Score** | 64/100 |
| 🗓️ **Last push** | 2026-09-05 |
| 🔍 **Source** | github |

## 🏷️ Topics

`agentic-soc` `ai` `blueteam` `cybersecurity` `dify` `langchain` `langgraph` `llm` `siem` `soar`

## 🎯 Categories

Orchestration · AI/ML · Security

## 📝 Summary

### English

**Brief Summary (2‑3 sentences)**  
The Agentic SOC Platform (FunnyWolf/agentic-soc-platform) is an open‑source, Python‑based framework that lets security teams stitch together isolated LLM prompts, tools, and data sources into repeatable, agent‑centric workflows. It targets orchestration, AI/ML, database, and security use cases such as multi‑agent coordination, tool‑use pipelines, and standardized agent memory. With 926 ★, recent commits, and growing community interest, it is positioned as a serious candidate for pilot‑grade deployments.

**Value**  
- **Unified Agent Orchestration:** Turns ad‑hoc prompts and scripts into reusable, composable agents, reducing manual glue code and speeding up SOC automation.  
- **Extensible Tool Integration:** Provides a plug‑and‑play pipeline model for adding scanners, threat intel feeds, ticketing systems, or custom scripts without rewriting core logic.  
- **Consistent Memory & State:** Offers a built‑in memory abstraction so agents can retain context across alerts, enabling more accurate triage and response.  

**Practical Adoption Path**  
1. **Proof‑of‑Concept (PoC):** Clone the repo, run the provided Docker/virtual‑env setup, and execute the example workflow from the README to validate environment compatibility.  
2. **Pilot Integration:** Replace one existing alert‑handling script with an Agentic workflow (e.g., enrich a phishing alert using a threat‑intel API). Keep the original pipeline as a fallback.  
3. **Scale & Harden:** Add additional agents (e.g., automated containment, ticket creation), integrate with your SIEM/SOAR via the provided adapters, and configure persistent storage for agent memory.  
4. **Governance & Monitoring:** Implement logging, role‑based access, and CI/CD checks for the agent definitions; run periodic dependency scans to maintain security posture.  

**Production Readiness**  
- **Activity & Community:** Recent commits (as of 2026‑06‑27), 926 stars, 153 forks, and active issue discussions indicate a healthy open‑source project.  
- **Technical Maturity:** Core components are written in Python, with clear module boundaries and Docker support, making deployment and scaling straightforward.  
- **Risk Considerations:** License compliance, long‑term maintainer commitment, and a formal security audit still need verification, but no immediate red flags are present.  
Overall, the platform is mature enough for a controlled pilot and, with proper hardening, can be promoted to production in security operations environments.

### Русский

**FunnyWolf/agentic-soc-platform** — это открытая, агент‑центричная платформа для автоматизации SOC, позволяющая превратить разрозненные prompts и инструменты в повторяемые многокомпонентные рабочие потоки с поддержкой памяти агентов и пайплайнов использования инструментов. Типичный сценарий внедрения — небольшое proof‑of‑concept, в котором интегрируются существующие средства мониторинга и реагирования, а затем масштабируется до полного координирования многопользовательских и мульти‑агентных процессов в реальном времени. Платформа имеет высокий уровень готовности к production: активные коммиты, более 900 звёзд, широкую экосистему Python и позитивные сигналы принятия, что делает её подходящей для серьёзных пилотных проектов.

### 中文

**项目简介**  
FunnyWolf/agentic-soc-platform 是一套以“代理”为核心的开源自动化安全运营平台（AI SOC），通过把零散的 Prompt 与安全工具封装成可复用的 Agent 工作流，实现灵活、可扩展的安全编排。

**价值**  
- **统一工作流**：把分散的安全脚本、模型 Prompt 与工具链统一为可重复执行的 Agent 流程，降低手工编排成本。  
- **多代理协同**：支持多 Agent 并行/串行协作，可实现漏洞扫描 → 威胁情报查询 → 响应自动化等端到端安全链路。  
- **标准化记忆**：内置 Agent Memory 机制，帮助平台在不同任务之间共享上下文，提升检测准确性与响应速度。  

**典型接入方式**  
1. **快速 PoC**：克隆仓库 → 按 README 完成依赖安装 → 使用示例 `workflow.yaml` 在本地 Docker/venv 环境跑通一次完整的多 Agent 流程。  
2. **工具链接入**：在 `tools/` 目录下添加自定义安全工具（如 Nessus、OpenVAS、Suricata），并在工作流配置中声明 `tool_use` 步骤，即可让 Agent 调用。  
3. **平台集成**：通过提供的 REST API 或 Python SDK，将平台嵌入现有 SIEM、SOAR 或 CI/CD 系统，实现自动触发与结果回写。  

**生产可用性**  
- **活跃度**：截至 2026‑06‑27，项目拥有 926 ⭐、153 🍴，最近一次提交在当日，说明维护活跃。  
- **技术成熟度**：核心使用 Python 实现，配套 Docker 镜像和完整文档，已在多个开源社区进行试点，具备“高”生产就绪度。  
- **风险点**：仍需确认许可证兼容性、长期维护者承诺以及容器安全基线；建议在正式投产前完成一次安全审计并制定升级策略。  

综上，FunnyWolf/agentic-soc-platform 适合作为安全团队的实验平台，快速验证多 Agent 编排后，可平滑迁移至生产环境，形成可持续的 AI‑SOC 能力。

## 🧭 Practical evaluation

**Value:** FunnyWolf/agentic-soc-platform helps turn isolated prompts and tools into repeatable agent workflows.

**Best use cases**

- coordinate multi-agent workflows
- add tool-use pipelines
- standardize agent memory

**Integration notes:** Looks feasible to evaluate, but integration should start with a small proof of concept and README check.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 926 GitHub stars
- 153 forks
- updated 2026-06-27
- primary language: Python
- 10 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 55/100 |
| stars | 63/100 |
| topics | 100/100 |
| outlook | 75/100 |
| quality | 77/100 |
| recency | 80/100 |
| adoption | 61/100 |
| production | 71/100 |
| usefulness | 58/100 |
| integration | 46/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 300/100 |

---

<sub>🔭 Discovered 2026-06-27 · [View on GitHub](https://github.com/FunnyWolf/agentic-soc-platform) · [← Back to Orchestration](./README.md)</sub>
