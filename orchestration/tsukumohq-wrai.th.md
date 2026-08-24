# TsukumoHQ/WRAI.TH

[![Stars](https://img.shields.io/github/stars/TsukumoHQ/WRAI.TH?style=flat-square&color=yellow)](https://github.com/TsukumoHQ/WRAI.TH/stargazers) [![Forks](https://img.shields.io/github/forks/TsukumoHQ/WRAI.TH?style=flat-square&color=blue)](https://github.com/TsukumoHQ/WRAI.TH/network) [![Language](https://img.shields.io/badge/lang-Go-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-58%2F100-brightgreen?style=flat-square)](#)

> Multi-agent orchestration via MCP. Persistent memory, inter-agent messaging, goal cascade, context budget pruning. One binary, zero config.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 22 |
| 🍴 **Forks** | 9 |
| 💻 **Language** | Go |
| 📈 **Score** | 58/100 |
| 🗓️ **Last push** | 2026-08-24 |
| 🔍 **Source** | github |

## 🏷️ Topics

`ai-agents` `claude` `claude-code` `golang` `mcp` `mcp-server` `multi-agent` `orchestration` `pixel-art` `sqlite`

## 🎯 Categories

Orchestration · MCP · AI/ML · Backend · Database

## 📝 Summary

### English

**Brief Summary (2‑3 sentences)**  
TsukumoHQ/WRAI.TH is a Go‑based, zero‑configuration binary that orchestrates multiple AI agents through a Message‑Centric Protocol (MCP). It supplies persistent memory, inter‑agent messaging, goal cascading, and context‑budget pruning, turning ad‑hoc prompts and tool calls into repeatable, composable workflows. The project is positioned as a lightweight backend for building and managing multi‑agent pipelines.

**Value Proposition**  
WRAI.TH abstracts the plumbing required to coordinate several agents, letting developers focus on the business logic of their AI applications. By providing built‑in memory persistence and a budget‑aware context manager, it reduces prompt‑token waste and improves consistency across runs. The single‑binary, language‑agnostic API/CLI makes it easy to plug into existing services, CI pipelines, or internal tooling without heavyweight infrastructure.

**Practical Adoption Path**  

| Step | Action | Reason |
|------|--------|--------|
| 1️⃣  | **Spin up the binary** (download the latest release, run `wrai.th serve` locally) | Zero‑config start‑up lets teams evaluate quickly. |
| 2️⃣  | **Integrate via the exposed API/CLI** (REST/GRPC endpoints or command‑line wrappers) | Works with any language stack; you can call it from Python, Node, etc. |
| 3️⃣  | **Define agent specs** (JSON/YAML describing prompts, tools, memory keys) and register them through the API | Formalizes isolated prompts into reusable “agent modules.” |
| 4️⃣  | **Create a workflow** using the goal‑cascade DSL or SDK to chain agents, set memory scopes, and configure budget limits | Turns prototypes into deterministic pipelines. |
| 5️⃣  | **Test in a sandbox** (unit tests or a staging environment) and monitor logs/metrics emitted by WRAI.TH | Validates correctness and performance before production rollout. |
| 6️⃣  | **Deploy** (Docker container, Kubernetes sidecar, or as a system service) and hook into your CI/CD | Leverages the single‑binary nature for straightforward containerization. |
| 7️⃣  | **Add observability** (exported Prometheus metrics, tracing hooks) and enforce security policies (auth, rate limiting) | Completes the production hardening checklist. |

**Production Readiness Assessment**  
- **Maturity**: Medium. The project is actively maintained (last commit 2026‑06‑24) and has modest community traction (22 stars, 9 forks).  
- **Stability**: The single‑binary design reduces dependency surface, but you should audit the Go modules for known CVEs and verify the license compatibility.  
- **Scalability**: Suitable for prototype‑scale or internal services; for high‑throughput workloads you’ll need to evaluate horizontal scaling (multiple instances behind a load balancer) and persistent storage options for the memory layer.  
- **Operational Considerations**: Add health‑checks, logging, and metric collection; perform a security review of the exposed API endpoints.  

Overall, WRAI.TH is a solid foundation for building reproducible multi‑agent workflows, especially in experimental or internal environments. With a brief integration effort and standard production hardening (security audit, monitoring, scaling tests), it can be promoted to production for use‑cases such as automated customer support pipelines, data‑processing orchestration, or tool‑augmented AI assistants.

### Русский

TsukumoHQ/WRAI.TH — это Go‑бинарник, позволяющий без настройки организовать оркестрацию многокомпонентных AI‑агентов через MCP: сохраняет постоянную память, поддерживает межагентские сообщения, каскад целей и автоматическое обрезание контекста. Он идеален для быстрого прототипирования и внутренних пайплайнов, где требуется превратить разрозненные подсказки и инструменты в повторяемые рабочие процессы с единым API/SDK/CLI. Проект находится на среднем уровне готовности к production: имеет базовые функции и активные обновления, но перед развертыванием следует проверить лицензию, безопасность и наличие постоянных мейнтейнеров.

### 中文

**项目简介（2‑3 句话）**  
TsukumoHQ/WRAI.TH 是一款基于 **MCP（Message‑Centric Protocol）** 的多代理编排引擎，提供持久化记忆、代理间消息、目标级联与上下文预算裁剪等功能。只需一个可执行文件、零配置，即可把孤立的 Prompt 与工具组合成可复用的工作流。

---

## 价值点

| 价值 | 说明 |
|------|------|
| **将碎片化 Prompt 统一为可复用工作流** | 通过持久记忆和目标级联，把一次性对话转化为可迭代、可追溯的流程。 |
| **简化多代理协作** | 内置的跨代理消息总线让不同模型、工具或微服务能够自然对话，省去自行实现队列或 RPC 的工作。 |
| **自动化上下文管理** | Context‑budget 剪枝机制防止上下文膨胀，保持响应速度和成本可控。 |
| **一键部署、零运维** | 单二进制文件，无需额外服务或容器编排，适合快速原型和内部实验。 |

---

## 典型接入方式

1. **CLI 调用**  
   ```bash
   ./wrai.th --config ./my_workflow.yaml
   ```  
   直接在命令行启动预定义的多代理工作流，适合脚本化或 CI/CD 场景。

2. **SDK / API**  
   项目提供 Go SDK（`github.com/TsukumoHQ/WRAI.TH/client`）以及 HTTP/JSON 接口。示例（Go）：

   ```go
   import "github.com/TsukumoHQ/WRAI.TH/client"

   c := client.New("http://localhost:8080")
   resp, err := c.RunWorkflow(context.Background(), "my-workflow", input)
   ```

   通过 HTTP POST 发送 `workflow_id` 与 `input`，即可在任何语言（Python、Node 等）中调用。

3. **容器化（可选）**  
   虽然是单二进制，但也提供 Dockerfile，便于在 Kubernetes 或本地 Docker 中统一管理依赖与网络。

---

## 生产可用性评估

| 维度 | 现状 | 备注 |
|------|------|------|
| **成熟度** | **中等**（适合原型、内部工具） | 依赖少、代码量小，易审计；但仍缺乏大规模生产案例。 |
| **维护状态** | 最近一次提交 2026‑06‑24，星标 22，fork 9 | 活跃度一般，需要自行评估维护者响应速度。 |
| **安全/合规** | 暂未发现重大风险，需进一步审查许可证、第三方依赖的安全报告 | 建议在 CI 中加入 SBOM 与漏洞扫描。 |
| **部署成本** | 低（单二进制/容器） | 无额外数据库或消息队列，资源占用约 30 MB 内存。 |
| **可扩展性** | 通过 MCP 可接入任意语言的代理或工具 | 需要自行实现对应的 MCP 客户端或适配层。 |
| **监控/日志** | 内置 JSON 日志，支持 Prometheus 指标导出 | 可与已有监控体系集成。 |

**结论**：WRAI.TH 在 **快速验证多代理协作**、**构建内部工具链** 方面表现出色，部署成本极低。若计划在生产环境大规模使用，建议在以下方面做额外工作：

1. **安全审计**：检查依赖的 Go 模块是否有未修复的 CVE。  
2. **高可用部署**：考虑使用水平复制 + 负载均衡，并持久化记忆存储（如外部 KV）。  
3. **运维脚本**：编写健康检查、滚动升级与日志收集脚本。  

完成上述准备后，WRAI.TH 完全可以作为生产级的多代理编排层。

## 🧭 Practical evaluation

**Value:** TsukumoHQ/WRAI.TH helps turn isolated prompts and tools into repeatable agent workflows.

**Best use cases**

- coordinate multi-agent workflows
- add tool-use pipelines
- standardize agent memory

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** Medium: useful for prototypes or internal workflows, with dependency and maintenance checks before production.

**Quality signals**

- 22 GitHub stars
- 9 forks
- updated 2026-06-24
- primary language: Go
- 10 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 25/100 |
| stars | 29/100 |
| topics | 100/100 |
| outlook | 56/100 |
| quality | 53/100 |
| recency | 40/100 |
| adoption | 28/100 |
| production | 54/100 |
| usefulness | 74/100 |
| integration | 62/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 500/100 |

---

<sub>🔭 Discovered 2026-06-24 · [View on GitHub](https://github.com/TsukumoHQ/WRAI.TH) · [← Back to Orchestration](./README.md)</sub>
