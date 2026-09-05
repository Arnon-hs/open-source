# Firma-AI/openfirma

[![Stars](https://img.shields.io/github/stars/Firma-AI/openfirma?style=flat-square&color=yellow)](https://github.com/Firma-AI/openfirma/stargazers) [![Forks](https://img.shields.io/github/forks/Firma-AI/openfirma?style=flat-square&color=blue)](https://github.com/Firma-AI/openfirma/network) [![Language](https://img.shields.io/badge/lang-Rust-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-58%2F100-brightgreen?style=flat-square)](#)

> Runtime enforcement boundary for AI agents: a local sidecar that gates every outbound call against Cedar policies you own. Deterministic, call-level, no model on the hot path

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 95 |
| 🍴 **Forks** | 3 |
| 💻 **Language** | Rust |
| 📈 **Score** | 58/100 |
| 🗓️ **Last push** | 2026-09-05 |
| 🔍 **Source** | github |

## 🏷️ Topics

`access-control` `agentic-ai` `ai-agents` `ai-governance` `ai-safety` `authorization` `cedar` `cedar-policy` `guardrails` `policy-engine` `runtime-security` `rust`

## 🎯 Categories

AI/ML · Security

## 📝 Summary

### English

**Brief summary (2‑3 sentences)**  
Firma‑AI’s **openfirma** is a Rust‑based sidecar that sits between your AI agent and any external service, intercepting every outbound request and evaluating it against Cedar policies you define. It provides deterministic, call‑level enforcement without inserting a model into the hot path, making it a lightweight way to add policy‑driven safety to prototype or internal AI workflows.

**Value**  
- **Policy‑first safety**: By gating every outbound call with Cedar policies, you can enforce data‑privacy, usage‑limits, or compliance rules even before a model generates a response.  
- **Zero‑impact runtime**: Enforcement happens in a separate sidecar, so the model’s inference latency remains unchanged.  
- **Rapid prototyping**: Developers can plug in existing AI stacks (RAG pipelines, autonomous agents, etc.) and immediately gain fine‑grained control without rebuilding a model stack from scratch.

**Practical adoption path**  
1. **Proof‑of‑concept** – Clone the repo, run the provided Docker compose or local binary, and point a simple AI client (e.g., a LangChain chain) at the sidecar.  
2. **Policy authoring** – Write Cedar policies for the specific outbound calls you need to guard (e.g., “no request to external APIs containing PII”).  
3. **Integration** – Replace direct HTTP calls in your agent code with the sidecar’s endpoint; the sidecar forwards allowed requests and returns denials.  
4. **Testing & iteration** – Use the built‑in logging and deterministic policy evaluation to tune rules before scaling.

**Production readiness**  
- **Maturity**: Medium. The project has recent activity (updated 2026‑06‑24), a modest star count (95) and a small number of forks, indicating early‑stage but functional code.  
- **Stability**: Deterministic enforcement and a clear separation of concerns make it suitable for internal prototypes or low‑risk production services.  
- **Considerations before production**:  
  - Verify the license and ensure it aligns with your organization’s policy.  
  - Conduct a security audit of the sidecar (network exposure, dependency hygiene).  
  - Establish monitoring for policy denials and sidecar health.  
  - Plan for maintainers: if the core team is small, you may need to fork and commit to long‑term upkeep.

In short, openfirma offers a pragmatic way to add policy‑driven guardrails to AI agents with minimal performance impact; start with a small PoC, solidify Cedar policies, and perform the usual security and maintenance checks before promoting it to production.

### Русский

**Firma‑AI/openfirma** — это локальный sidecar‑модуль, который перехватывает каждый исходящий запрос от AI‑агента и проверяет его в режиме реального времени по вашим политикам Cedar, обеспечивая детерминированный контроль доступа без участия модели в «горячем» пути. Его типичное применение — быстрый прототипинг функций ИИ, построение RAG‑или агентных воркфлоу и оценка инструментов моделей, где достаточно небольшого proof‑of‑concept и проверки README перед интеграцией. Готовность к продакшену — средняя: проект стабилен для внутренних и экспериментальных сценариев, но требует проверки лицензии, безопасности и поддержки перед масштабным внедрением.

### 中文

**项目简介（2‑3 句）**  
Firma‑AI/openfirma 是一个运行时强制执行边界（runtime enforcement boundary），通过本地 sidecar 在每一次对外调用前检查您自定义的 Cedar 策略，实现对 AI 代理的细粒度、确定性的访问控制。它在调用层面拦截请求，且不在热路径上加载模型，保持低延迟和高安全性。

**价值**  
- **安全合规**：所有出站请求都必须通过可审计的策略检查，防止模型泄露、违规调用或不当数据流出。  
- **快速落地 AI 能力**：无需从零搭建模型栈，只需把已有模型或 RAG/Agent 工作流接入 sidecar，即可获得安全保障的 AI 功能。  
- **确定性与可调试**：策略在编译时即确定，调用结果可预测，便于调试和审计。

**典型接入方式**  
1. **本地 sidecar 部署**：使用 Docker 或直接在宿主机上运行 Rust 编译的二进制。  
2. **代理配置**：将现有的模型服务（如 OpenAI、Claude、本地 LLM）或 RAG/Agent 工作流的 HTTP/HTTPS 入口指向 sidecar 的监听端口。  
3. **策略编写**：使用 Cedar 语言编写组织内部的访问控制策略（如限流、模型调用权限、数据脱敏等），并通过 sidecar 的 API 加载。  
4. **验证**：先在小范围（例如单个微服务或 CI/CD 流水线）进行 PoC，确认策略生效后逐步推广。

**生产可用性**  
- **成熟度**：当前评分 61/100，GitHub 95 星、3 个 Fork，活跃维护至 2026‑06‑24，代码基于 Rust，具备较好的性能和安全特性。  
- **适用场景**：非常适合作为原型或内部工作流的安全网，亦可在对合规要求较高的生产环境中使用，但需完成以下检查后方可正式上线：  
  - 完整审计许可证和依赖链的安全性；  
  - 对 sidecar 的高可用部署（如 Kubernetes DaemonSet）进行压力测试；  
  - 建立策略更新、回滚和审计日志的运维流程。  
- **总体评估**：在完成依赖安全审查和运维准备后，可视为 **中等生产可用性**，适合在内部或受控的生产环境中逐步推广。

## 🧭 Practical evaluation

**Value:** Firma-AI/openfirma helps add AI capability without starting from a blank model stack.

**Best use cases**

- prototype AI features
- build RAG or agent workflows
- evaluate model tooling

**Integration notes:** Looks feasible to evaluate, but integration should start with a small proof of concept and README check.

**Production readiness:** Medium: useful for prototypes or internal workflows, with dependency and maintenance checks before production.

**Quality signals**

- 95 GitHub stars
- 3 forks
- updated 2026-06-24
- primary language: Rust
- 13 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 15/100 |
| stars | 42/100 |
| topics | 100/100 |
| outlook | 68/100 |
| quality | 66/100 |
| recency | 80/100 |
| adoption | 35/100 |
| production | 66/100 |
| usefulness | 58/100 |
| integration | 46/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 200/100 |

---

<sub>🔭 Discovered 2026-06-24 · [View on GitHub](https://github.com/Firma-AI/openfirma) · [← Back to AI/ML](./README.md)</sub>
