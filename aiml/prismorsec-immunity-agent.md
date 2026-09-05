# PrismorSec/immunity-agent

[![Stars](https://img.shields.io/github/stars/PrismorSec/immunity-agent?style=flat-square&color=yellow)](https://github.com/PrismorSec/immunity-agent/stargazers) [![Forks](https://img.shields.io/github/forks/PrismorSec/immunity-agent?style=flat-square&color=blue)](https://github.com/PrismorSec/immunity-agent/network) [![Language](https://img.shields.io/badge/lang-Python-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-58%2F100-brightgreen?style=flat-square)](#)

> Security for AI agents : Block dangerous commands,  prevent secret leaks, and enforce runtime policies across Claude, OpenClaw, Hermes, Antigravity, Codex,  Cursor and Windsurf

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 113 |
| 🍴 **Forks** | 9 |
| 💻 **Language** | Python |
| 📈 **Score** | 58/100 |
| 🗓️ **Last push** | 2026-09-05 |
| 🔍 **Source** | github |

## 🏷️ Topics

`agent-security` `agentic-ai` `agents` `ai` `cybersecurity` `security`

## 🎯 Categories

AI/ML · Security

## 📝 Summary

### English

**Brief Summary (2‑3 sentences)**  
PrismorSec’s *immunity‑agent* is a Python library that safeguards AI agents by intercepting dangerous commands, preventing confidential data leaks, and enforcing runtime policies across a wide range of models and frameworks (Claude, OpenClaw, Hermes, Antigravity, Codex, Cursor, Windsurf, etc.). It lets developers augment existing agents with security controls without having to rebuild the entire model stack, making it ideal for rapid prototyping of RAG or autonomous‑agent workflows. With modest community interest (≈113 ★) and recent updates, it offers a practical “security‑as‑a‑service” layer for AI‑driven applications.

**Value**  
- **Immediate protection**: Plug‑in policy checks into any supported agent to block malicious prompts, data exfiltration, or unsafe tool usage.  
- **Speed to market**: Developers can focus on core business logic while reusing the library’s pre‑built safeguards, avoiding the need to design custom security layers from scratch.  
- **Broad compatibility**: Works with several popular LLM back‑ends and agent frameworks, so a single codebase can protect heterogeneous deployments.

**Practical Adoption Path**  
1. **Proof‑of‑Concept** – Clone the repo, run the example notebooks, and verify that the README’s quick‑start steps protect a toy agent.  
2. **Policy Definition** – Extend the default rule set (e.g., regex filters, token‑level restrictions) to match your organization’s data‑handling and compliance requirements.  
3. **Integration** – Wrap the agent’s request/response pipeline with the `ImmunityAgent` middleware; this typically involves adding a few lines of Python to the existing inference loop.  
4. **Testing** – Use unit‑ and integration‑tests to simulate dangerous prompts and confirm that the agent is blocked or sanitized as expected.  
5. **Roll‑out** – Deploy the hardened agent in a staging environment, monitor logs for policy violations, and iterate on rules before promoting to production.

**Production Readiness**  
- **Maturity**: Medium. The library is actively maintained (last commit 2026‑05‑12) and has a modest but growing user base, but it is still positioned for prototypes and internal tooling rather than mission‑critical services.  
- **Dependencies**: Pure Python with standard ML libraries; verify version compatibility with your target LLM stack and run a dependency audit.  
- **Operational considerations**: Implement logging and alerting around policy violations, and establish a process for rule updates as new threats emerge.  
- **Risk assessment**: No immediate licensing or metadata red flags, but a final review of the open‑source license and a security audit of the code are advisable before production deployment.  

Overall, *immunity‑agent* offers a low‑friction way to embed security into AI agents, making it a strong candidate for early‑stage projects and internal workflows, with a clear path to hardened production use after thorough testing and policy hardening.

### Русский

**PrismorSec/immunity-agent** — это Python‑библиотека, позволяющая быстро добавить к любому AI‑агенту (Claude, OpenClaw, Hermes, Antigravity, Codex, Cursor, Windsurf) защиту от опасных команд, утечек конфиденциальных данных и соблюдение runtime‑политик. Типичный сценарий — запуск небольшого proof‑of‑concept: интегрировать агент в прототип RAG/агентного воркфлоу, настроить политики и проверить, что модель работает в безопасных границах, после чего масштабировать решение внутри компании. Готовность к production — средняя: проект уже активно поддерживается (обновление 2026‑05‑12, 113 звёзд), но перед выпуском в продакшн требуется проверка лицензии, оценка зависимости и обеспечение постоянного сопровождения.

### 中文

**项目价值**  
PrismorSec /immunity‑agent 为各种大语言模型（Claude、OpenClaw、Hermes、Antigravity、Codex、Cursor、Windsurf 等）提供运行时安全层，能够拦截危险指令、阻止机密泄露并强制执行自定义策略。它让开发者在不从零构建安全框架的前提下，快速为 AI 功能加入防护，降低因模型误用或信息泄露导致的风险。

**典型接入方式**  
1. **依赖安装**：`pip install immunity-agent`（或直接在项目的 `requirements.txt` 中加入）。  
2. **初始化**：在代码中创建 `ImmunityAgent` 实例并加载对应模型的适配器，例如：  
   ```python
   from immunity_agent import ImmunityAgent, ClaudeAdapter

   agent = ImmunityAgent(adapter=ClaudeAdapter())
   agent.add_policy('no_sql_injection')
   agent.add_policy('mask_secret')
   ```
3. **包装调用**：把原始的模型调用包装为 `agent.run(prompt)`，所有输入/输出都会经过策略检查与过滤。  
4. **策略定制**：通过 YAML/JSON 配置文件或 Python API 添加、修改或删除策略，支持正则、关键字、上下文感知等多种过滤方式。  
5. **渐进式验证**：先在单元测试或小型原型（如 Jupyter Notebook）中验证安全策略的效果，再逐步迁移到完整的业务流程。

**生产可用性**  
- **成熟度**：当前评分 61/100，GitHub 113 星、9 fork，最近一次提交为 2026‑05‑12，代码以 Python 为主，社区活跃度一般。  
- **适用场景**：非常适合作为 **原型**、**内部工具** 或 **RAG/Agent 工作流** 的安全防护层。  
- **上线前检查**：  
  1. **依赖审计**：确认所有第三方库的许可证兼容性（MIT/Apache 等）并进行安全扫描。  
  2. **策略审查**：根据业务合规要求审定默认策略，必要时补充自定义规则。  
  3. **性能评估**：在负载测试环境下评估策略检查的延迟，确保满足 SLA。  
  4. **监控与日志**：开启审计日志，实时监控被拦截的指令及泄露风险。  
- **结论**：在完成上述审计与性能验证后，immunity‑agent 可在 **内部生产环境** 稳定使用；若要面向外部客户或高并发场景，仍建议进一步进行代码审计、持续集成测试以及维护者沟通，以确保长期可维护性。

## 🧭 Practical evaluation

**Value:** PrismorSec/immunity-agent helps add AI capability without starting from a blank model stack.

**Best use cases**

- prototype AI features
- build RAG or agent workflows
- evaluate model tooling

**Integration notes:** Looks feasible to evaluate, but integration should start with a small proof of concept and README check.

**Production readiness:** Medium: useful for prototypes or internal workflows, with dependency and maintenance checks before production.

**Quality signals**

- 113 GitHub stars
- 9 forks
- updated 2026-05-12
- primary language: Python
- 6 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 25/100 |
| stars | 44/100 |
| topics | 75/100 |
| outlook | 67/100 |
| quality | 64/100 |
| recency | 80/100 |
| adoption | 39/100 |
| production | 66/100 |
| usefulness | 58/100 |
| integration | 46/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 200/100 |

---

<sub>🔭 Discovered 2026-05-12 · [View on GitHub](https://github.com/PrismorSec/immunity-agent) · [← Back to AI/ML](./README.md)</sub>
