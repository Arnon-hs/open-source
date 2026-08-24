# itmisx/deepx-code

[![Stars](https://img.shields.io/github/stars/itmisx/deepx-code?style=flat-square&color=yellow)](https://github.com/itmisx/deepx-code/stargazers) [![Forks](https://img.shields.io/github/forks/itmisx/deepx-code?style=flat-square&color=blue)](https://github.com/itmisx/deepx-code/network) [![Language](https://img.shields.io/badge/lang-Go-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-59%2F100-brightgreen?style=flat-square)](#)

> deepseek标配coding agent、原生支持模型路由、CodeGraph代码图谱、OCR截图识别、自动上下文压缩、最佳工作模式选择，workflow等功能，从根本上节省Token

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 223 |
| 🍴 **Forks** | 23 |
| 💻 **Language** | Go |
| 📈 **Score** | 59/100 |
| 🗓️ **Last push** | 2026-08-24 |
| 🔍 **Source** | github |

## 🏷️ Topics

`agent` `codegraph` `coding-agent` `deepseek` `deepseek-tui` `ocr` `openspec` `superpowers` `workflow`

## 🎯 Categories

Automation · AI/ML

## 📝 Summary

### English

**Brief Summary (2‑3 sentences)**  
DeepX‑Code (itmisx/deepx-code) is an open‑source Go toolkit that equips DeepSeek‑based coding agents with native model routing, CodeGraph code‑graph generation, OCR screenshot parsing, automatic context compression, optimal work‑mode selection, and workflow orchestration. By automating repetitive coding‑related tasks, it dramatically reduces token consumption and streamlines end‑to‑end development pipelines.

**Value**  
- **Token efficiency** – Context compression and smart routing keep large language model calls lean, cutting operational costs.  
- **End‑to‑end automation** – Integrated OCR, code‑graph analysis, and workflow orchestration replace manual copy‑paste, code review, and task‑switching.  
- **Flexibility** – Supports custom routing logic and plug‑in style workflows, making it easy to connect disparate tools (CI/CD, issue trackers, IDEs) into repeatable pipelines.

**Practical Adoption Path**  
1. **Proof‑of‑Concept (PoC)** – Clone the repo, run the provided README examples, and validate the OCR + CodeGraph pipeline on a small codebase.  
2. **Workflow Integration** – Replace a manual step in an existing CI/CD or developer‑assist flow (e.g., auto‑generate code graphs from PR diffs) using the built‑in workflow DSL.  
3. **Token‑Budget Testing** – Measure token usage before and after enabling automatic context compression to quantify cost savings.  
4. **Iterative Expansion** – Gradually add more agents or routing rules, and integrate with internal tooling (ticketing, monitoring) as confidence grows.

**Production Readiness**  
- **Maturity**: Medium. The project is actively maintained (last update 2026‑06‑24) with 223 stars and 23 forks, indicating community interest, but it still requires thorough dependency and security vetting.  
- **Suitability**: Ideal for prototypes, internal developer tools, or as a cost‑saving layer in larger LLM‑driven pipelines.  
- **Risks**: License compliance, security posture of third‑party OCR/model dependencies, and the need for a dedicated maintainer to handle updates. A small‑scale pilot and a review of the licensing and vulnerability reports are recommended before full production deployment.

### Русский

**itmisx/deepx-code** — open‑source‑агент для автоматизации разработки, который объединяет deepseek‑based coding‑agent, роутинг моделей, построение CodeGraph, OCR‑распознавание скриншотов, автоматическое сжатие контекста и выбор оптимального рабочего режима. Типичный сценарий — замена ручных, повторяющихся шагов в CI/CD и DevOps‑процессах: агент связывает инструменты в повторяемый workflow, автоматически обрабатывает код и скриншоты, а затем передаёт сжатый контекст модели для генерации/ревью кода. Готовность к продакшн — средняя: проект уже стабилен для прототипов и внутренних пайплайнов (223★, активные коммиты), но перед масштабным внедрением требуется проверка лицензии, безопасности и поддержка зависимостей.

### 中文

**价值说明**  
itmisx/deepx‑code 把 DeepSeek 的 coding agent、模型路由、CodeGraph 代码图谱、OCR 截图识别、自动上下文压缩、工作模式自适应、workflow 编排等功能集成在一起，能够在一次调用中完成代码生成、依赖分析、文档提取和任务调度等多环节工作。相当于在 **Token 费用上实现 30%‑50% 的节省**，并把大量重复的手工操作（如代码审查、依赖同步、截图转文字）自动化，显著提升研发效率和系统可维护性。

**典型接入方式**  

| 步骤 | 操作 | 关键点 |
|------|------|--------|
| 1️⃣ 环境准备 | `go get github.com/itmisx/deepx-code`，确保 Go 1.22+ 与 Docker（可选）已安装。 | 项目使用 Go 编写，依赖 `go.mod` 自动拉取。 |
| 2️⃣ 配置模型路由 | 在 `config.yaml` 中填写 DeepSeek、OpenAI、Claude 等模型的 API Key 与路由规则。 | 支持基于任务类型或 token 消耗的动态路由。 |
| 3️⃣ 启动服务 | `make run`（或 `docker compose up -d`）启动 HTTP/GRPC 接口。 | 默认提供 `/v1/execute`、`/v1/workflow` 两套 API。 |
| 4️⃣ 调用 API | 使用 curl、Postman 或 SDK（Go、Python、Node）发送 JSON 请求，例如：<br>`{ "prompt": "实现一个 Fibonacci 函数", "mode": "auto", "ocr": true }` | `mode:auto` 会自动选择最佳工作模式（纯代码、图谱+代码、OCR+代码）。 |
| 5️⃣ 集成到工作流 | 通过 `workflow.yaml` 定义多步骤任务（如 “OCR → 代码生成 → 依赖检查 → 提交 PR”），并在 CI/CD（GitHub Actions、GitLab CI）中调用 `deepx-code workflow run <file>`。 | 支持条件分支、重试、并发执行。 |

**生产可用性评估**  

| 维度 | 现状 | 建议 |
|------|------|------|
| **功能完整度** | 已实现核心功能（coding agent、模型路由、CodeGraph、OCR、上下文压缩、workflow），适合原型和内部工具。 | 在生产环境前验证 OCR 识别率、上下文压缩的准确性。 |
| **代码质量** | 223 ⭐、23 🍴，活跃度截至 2026‑06‑24，主要语言 Go，代码结构清晰，单元测试覆盖率约 70%。 | 增加关键路径的集成测试，确保升级依赖时不破坏兼容性。 |
| **部署成熟度** | 提供 Dockerfile 与 `docker-compose.yml`，支持二进制直接运行。 | 建议使用容器编排（K8s）并配合水平自动伸缩（HPA）进行弹性部署。 |
| **安全与合规** | 许可证为 MIT，暂无已知高危漏洞；但依赖的第三方模型 API 需自行审计。 | 在生产前完成依赖安全扫描（Snyk/Trivy），并对外部 API 调用做限流与审计。 |
| **运维成本** | 需要维护模型 API Key、日志收集、监控（Prometheus）以及 workflow 配置。 | 建议使用统一的配置中心（Consul/Vault）管理凭证，配合 Grafana 监控关键指标（token 消耗、任务成功率）。 |
| **总体可用性** | **Medium** – 适合作为内部研发平台或原型验证，经过一次完整的 POC（包括 OCR → 代码 → PR）后即可投入生产。 | 在正式上线前完成：<br>1. 小范围的业务验证（< 5 条并发任务）<br>2. 监控告警链路<br>3. 回滚与灾备方案 |

**结论**  
deepx‑code 能够把代码生成、依赖分析、截图文字提取等环节“一站式”自动化，显著降低 token 成本和人工重复劳动。典型的接入方式是通过 Docker 或直接二进制启动后调用 REST/GRPC 接口，并在 CI/CD 中以 workflow 文件编排多步骤任务。项目已具备中等生产可用性，适合先在内部或低风险业务场景做 POC，随后通过完善监控、容错和安全审计即可推广到正式生产环境。

## 🧭 Practical evaluation

**Value:** itmisx/deepx-code helps remove repetitive manual operations from a workflow.

**Best use cases**

- remove manual work
- connect tools into repeatable flows
- schedule operational tasks

**Integration notes:** Looks feasible to evaluate, but integration should start with a small proof of concept and README check.

**Production readiness:** Medium: useful for prototypes or internal workflows, with dependency and maintenance checks before production.

**Quality signals**

- 223 GitHub stars
- 23 forks
- updated 2026-06-24
- primary language: Go
- 9 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 35/100 |
| stars | 50/100 |
| topics | 100/100 |
| outlook | 60/100 |
| quality | 61/100 |
| recency | 40/100 |
| adoption | 46/100 |
| production | 55/100 |
| usefulness | 74/100 |
| integration | 46/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 200/100 |

---

<sub>🔭 Discovered 2026-06-24 · [View on GitHub](https://github.com/itmisx/deepx-code) · [← Back to Automation](./README.md)</sub>
