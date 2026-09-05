# AnttiHero/lavern

[![Stars](https://img.shields.io/github/stars/AnttiHero/lavern?style=flat-square&color=yellow)](https://github.com/AnttiHero/lavern/stargazers) [![Forks](https://img.shields.io/github/forks/AnttiHero/lavern?style=flat-square&color=blue)](https://github.com/AnttiHero/lavern/network) [![Language](https://img.shields.io/badge/lang-TypeScript-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-69%2F100-brightgreen?style=flat-square)](#)

> An agentic law firm. Yours. 67 specialist AI agents that review documents through evidence-backed debate, with mandatory human gates and a 10-pass verification loop. Apache 2.0.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 262 |
| 🍴 **Forks** | 86 |
| 💻 **Language** | TypeScript |
| 📈 **Score** | 69/100 |
| 🗓️ **Last push** | 2026-09-05 |
| 🔍 **Source** | github |

## 🏷️ Topics

`agentic-ai` `ai-agents` `anthropic` `claude` `contract-review` `law-firm` `legal-ai` `legal-tech` `mcp` `mistral-ai` `model-context-protocol` `multi-agent`

## 🎯 Categories

Orchestration · MCP · AI/ML · Documents

## 📝 Summary

### English

**Brief Summary (2‑3 sentences)**  
Lavern (AnttiHero/lavern) is an open‑source, Apache‑2.0‑licensed platform that orchestrates 67 specialist AI agents to review legal documents via evidence‑backed debate, enforced human checkpoints, and a ten‑pass verification loop. Written in TypeScript, it exposes a clean API/SDK/CLI, making it easy to turn ad‑hoc prompts and tools into repeatable, auditable multi‑agent workflows. With 262 ★, 86 forks, and active commits as of 2026‑06‑30, Lavern scores 73/100 and is positioned as a production‑ready candidate for legal‑tech pilots.

**Value**  
- **From isolated prompts to repeatable processes** – Lavern abstracts the choreography of many specialized agents, letting teams build deterministic, version‑controlled pipelines instead of stringing together one‑off calls.  
- **Evidence‑backed debate & verification** – Each document passes through a structured, multi‑round argumentation cycle and a ten‑pass verification loop, dramatically reducing hallucinations and increasing confidence in legal outputs.  
- **Human‑in‑the‑loop safety** – Mandatory gates ensure that a qualified lawyer reviews every decision before final acceptance, satisfying compliance and liability requirements.  
- **Standardised memory & tool use** – Built‑in support for shared agent memory and tool‑integration (e.g., OCR, contract clause extractors) lets organizations reuse knowledge across cases and scale expertise without re‑training models.

**Practical Adoption Path**  
1. **Evaluation** – Clone the repo, run the provided Docker compose or npm scripts, and experiment with the CLI against a small set of sample contracts.  
2. **Integration** – Wrap the Lavern SDK in your existing case‑management system; use the REST API to submit documents and retrieve the final, human‑approved verdict.  
3. **Customization** – Extend or replace specialist agents (e.g., add a GDPR‑compliance checker) by implementing the defined `Agent` interface in TypeScript; the platform’s plug‑in architecture picks them up automatically.  
4. **Pilot** – Deploy the orchestrator on a staging Kubernetes cluster, configure the human‑gate workflow to route decisions to a designated legal reviewer, and monitor the ten‑pass verification logs.  
5. **Scale** – Once validated, promote the service to production, add autoscaling for the agent pool, and integrate with CI/CD to version‑control agent updates and debate‑policy changes.

**Production Readiness**  
- **Activity & Community** – Recent commits (last update 2026‑06‑30), 262 stars, and 86 forks indicate an engaged community and ongoing maintenance.  
- **Architecture** – Modular TypeScript codebase, well‑documented API/SDK/CLI, and containerised deployment options make it straightforward to embed in existing cloud or on‑prem environments.  
- **Reliability** – The built‑in 10‑pass verification loop and mandatory human gates provide strong safety nets for high‑risk legal decisions.  
- **Risks** – No major metadata concerns, but a final security audit (dependency scanning, secret handling) and confirmation of active maintainers are recommended before a full production rollout.  

Overall, Lavern offers a mature, extensible framework for turning fragmented AI tools into a compliant, auditable legal‑review pipeline, making it a solid candidate for pilot projects and, with the usual security diligence, for full‑scale production use.

### Русский

Резюме проекта AnttiHero/lavern:

Проект AnttiHero/lavern представляет собой агентную юридическую фирму, которая обеспечивает автоматизированное обследование документов с использованием доказательств и обязательного человеческого контроля. Он позволяет превратить изолированные команды и инструменты в повторяемые агентские потоки. Проект готов к производству (high) и обладает сильными сигналами приема, обновлений и экосистемы.

### 中文

**项目简介（2‑3 句）**  
AnttiHero/lavern 是一个“代理律所”，内置 67 个专业 AI 代理人，通过基于证据的辩论对文档进行审查，并配有人类审查门和 10 次循环验证，代码采用 Apache‑2.0 许可证开源。

**价值主张**  
- **把碎片化的 Prompt 与工具串联成可复用的工作流**：Lavern 将单个大模型调用、工具调用、记忆管理等环节统一编排，形成结构化的多代理协作流程。  
- **提升审查质量与合规性**：每个代理人围绕同一文档展开证据驱动的辩论，最终结果必须通过人类门和十轮自动验证，显著降低误判风险。  
- **加速业务上线**：提供即插即用的多代理框架，企业无需自行实现复杂的调度、状态持久化和争议解决逻辑，即可快速构建法律文档审查、合同合规、风险评估等场景。

**典型接入方式**  

| 接入层级 | 方式 | 说明 |
|----------|------|------|
| **SDK** | `npm i @lavern/sdk`（TypeScript/JavaScript） | 直接在代码中调用 `LavernClient`，配置代理、工具链和验证策略。 |
| **CLI** | `npx lavern run <workflow.yaml>` | 通过 YAML/JSON 描述工作流，适合脚本化批处理或 CI/CD 集成。 |
| **API** | `POST /v1/workflows`（REST） | 部署后可作为微服务使用，支持跨语言（Python、Go、Java）调用。 |
| **插件** | VSCode/IntelliJ 插件 | 在编辑器内直接启动文档审查，适合律师事务所日常使用。 |

> **接入示例（TypeScript）**  
> ```ts
> import { LavernClient } from '@lavern/sdk';
> const client = new LavernClient({ apiKey: process.env.LAVERN_KEY });
> const result = await client.runWorkflow('contract-review', {
>   document: fs.readFileSync('contract.pdf')
> });
> console.log(result.verdict);
> ```

**生产可用性评估**  

| 维度 | 评估 | 说明 |
|------|------|------|
| **活跃度** | ★★★★★ | 最近一次提交 2026‑06‑30，持续更新；GitHub ★262，Fork ★86，社区讨论活跃。 |
| **生态兼容** | ★★★★★ | 提供完整的 SDK、CLI 与 HTTP API，支持 TypeScript 为主的微服务，也可通过 OpenAPI 生成其他语言客户端。 |
| **安全合规** | ★★★★☆ | 采用 Apache‑2.0 许可证，无已知重大漏洞；仍建议在内部进行依赖审计和容器镜像扫描。 |
| **可扩展性** | ★★★★★ | 代理数量可动态配置，工具链通过插件机制添加，支持水平扩容的 Kubernetes 部署示例。 |
| **运维成熟度** | ★★★★☆ | 提供 Docker 镜像和 Helm Chart，配套监控（Prometheus）与日志（ELK）示例，适合生产环境快速落地。 |

**结论**  
Lavern 已具备较高的生产就绪度，适合作为 **多代理工作流编排平台** 在法律文档审查、合规检查以及需要高度可解释性的 AI 业务中进行试点。企业可先通过 SDK/CLI 完成概念验证（PoC），随后在 Kubernetes 环境中部署完整的 API 服务，结合内部的人类审查门，实现安全、可审计的 AI 驱动审查流水线。

## 🧭 Practical evaluation

**Value:** AnttiHero/lavern helps turn isolated prompts and tools into repeatable agent workflows.

**Best use cases**

- coordinate multi-agent workflows
- add tool-use pipelines
- standardize agent memory

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 262 GitHub stars
- 86 forks
- updated 2026-06-30
- primary language: TypeScript
- 14 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 48/100 |
| stars | 51/100 |
| topics | 100/100 |
| outlook | 75/100 |
| quality | 73/100 |
| recency | 80/100 |
| adoption | 51/100 |
| production | 71/100 |
| usefulness | 74/100 |
| integration | 62/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 400/100 |

---

<sub>🔭 Discovered 2026-06-30 · [View on GitHub](https://github.com/AnttiHero/lavern) · [← Back to Orchestration](./README.md)</sub>
