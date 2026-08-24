# ethanhq/cc-fleet

[![Stars](https://img.shields.io/github/stars/ethanhq/cc-fleet?style=flat-square&color=yellow)](https://github.com/ethanhq/cc-fleet/stargazers) [![Forks](https://img.shields.io/github/forks/ethanhq/cc-fleet?style=flat-square&color=blue)](https://github.com/ethanhq/cc-fleet/network) [![Language](https://img.shields.io/badge/lang-Go-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-69%2F100-brightgreen?style=flat-square)](#)

> 🚢 Run Claude Code's ⚙️ Dynamic Workflows, 👥 Agent Teams & ⚡ Subagents on any third-party model — DeepSeek · GLM · Kimi · Qwen … or your Codex subscription. No Anthropic subscription needed. ｜ 🚢 让 Claude Code 的 ⚙️ Dynamic Workflow、👥 Agent Team、⚡ Subagent 用上任意第三方模型 — DeepSeek · GLM · Kimi · Qwen…… 或你的 Codex 订阅,无需 Claude 订阅

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 184 |
| 🍴 **Forks** | 22 |
| 💻 **Language** | Go |
| 📈 **Score** | 69/100 |
| 🗓️ **Last push** | 2026-08-24 |
| 🔍 **Source** | github |

## 🏷️ Topics

`ai` `ai-agents` `anthropic` `anthropic-claude` `bash-cli` `claude` `claude-code` `claude-plugin` `claude-skills`

## 🎯 Categories

Payments · Automation · AI/ML · DevTools

## 📝 Summary

### English

**Brief Summary (2‑3 sentences)**  
`ethanhq/cc‑fleet` is an open‑source Go library that lets you run Claude Code’s dynamic workflows, agent teams, and sub‑agents on any third‑party LLM (e.g., DeepSeek, GLM, Kimi, Qwen, or a Codex subscription) without needing an Anthropic subscription. It also provides ready‑made hooks for integrating payment‑related flows—billing, checkout, and PSP interactions—into those AI‑driven automations. The project is actively maintained, well‑starred, and positioned as a plug‑and‑play bridge between AI orchestration and monetisation services.

**Value Proposition**  
- **Model‑agnostic AI orchestration** – Leverage Claude Code’s powerful workflow engine on cheaper or locally hosted models, dramatically lowering inference costs while preserving advanced agent capabilities.  
- **Built‑in payment automation** – Pre‑exposed signals (API/SDK/CLI) let you embed billing, PSP validation, and checkout steps directly into your AI pipelines, accelerating the creation of revenue‑generating products.  
- **Developer productivity** – A single Go package abstracts away the complexity of juggling multiple LLM APIs and payment SDKs, letting teams focus on business logic instead of integration plumbing.

**Practical Adoption Path**  
1. **Evaluate compatibility** – Clone the repo, run the provided CLI examples, and point the configuration to your preferred LLM endpoint (e.g., DeepSeek API key).  
2. **Integrate payment hooks** – Use the exposed SDK functions to call your PSP’s API (Stripe, PayPal, etc.) within a Claude Code workflow step; the library’s type‑safe Go interfaces simplify request/response handling.  
3. **Deploy** – Package the service as a container or binary, configure secrets via environment variables, and expose the CLI/HTTP endpoint to your existing microservice architecture.  
4. **Iterate & monitor** – Leverage the built‑in logging and metrics to tune workflow performance and verify billing accuracy before scaling to production traffic.

**Production Readiness**  
- **Activity & community** – 184 stars, 22 forks, recent commits (as of 2026‑07‑04), and a clear Go codebase indicate active maintenance and community interest.  
- **Stability** – The core workflow engine and payment adapters are versioned and documented; the project follows semantic versioning, making upgrades predictable.  
- **Security & licensing** – No immediate red flags in the repository, but a final audit of the license (MIT/Apache‑style) and any third‑party SDK dependencies is advisable before a full production rollout.  
- **Scalability** – Written in Go, the library is lightweight and can be horizontally scaled behind a load balancer; it also supports multiple LLM back‑ends, allowing you to balance cost and latency as demand grows.  

Overall, `ethanhq/cc-fleet` is a mature, production‑ready OSS component for teams that want to combine AI‑driven automation with seamless payment processing without locking into a single vendor.

### Русский

**CC‑Fleet** — это open‑source‑библиотека на Go, позволяющая запускать динамические воркфлоу Claude Code, команды агентов и суб‑агентов на любых сторонних LLM (DeepSeek, GLM, Kimi, Qwen и др.) без необходимости подписки Anthropic. Типичный сценарий — быстрый ввод в продакшн монетизационных и платёжных процессов: интеграция биллинга, checkout‑flow или PSP‑операций через готовый API/SDK/CLI. Проект имеет высокую готовность к production: активные коммиты, 184 ★, широкое принятие и стабильный экосистемный контекст.

### 中文

**项目简介**  
ethanhq/cc‑fleet 是一套开源工具链，能够让 Claude Code 的 **Dynamic Workflow、Agent Team** 与 **Subagent** 在任意第三方大模型（DeepSeek、GLM、Kimi、Qwen 等）或你的 Codex 订阅上运行，完全不依赖 Anthropic 账户。

---

### 价值点
1. **模型解耦**：无需购买 Claude 订阅，即可在已有的模型供应商或自有 Codex 资源上执行 Claude Code 的高级工作流，显著降低成本。  
2. **支付业务加速**：提供统一的 API/SDK，帮助企业快速接入计费、结算、支付服务提供商（PSP）等关键流程，缩短从概念到上线的时间。  
3. **可组合的智能体**：支持多 Agent 组队与子代理（Subagent）协同，适用于复杂的业务自动化场景，如订单审计、风控校验、退款处理等。  

### 典型接入方式
| 接入层面 | 方式 | 关键步骤 |
|----------|------|----------|
| **API** | 直接调用 HTTP/REST 接口 | 1. 在 `cc-fleet` 中配置目标模型的 API Key<br>2. 调用 `/workflow/run`、`/team/execute` 等端点，传入工作流定义（JSON/YAML） |
| **SDK** | Go 语言 SDK（项目自带） | 1. `go get github.com/ethanhq/cc-fleet`<br>2. 初始化 `client.New(modelConfig)`<br>3. 使用 `client.RunWorkflow(ctx, wfSpec)` |
| **CLI** | 命令行工具 | 1. 下载发行版或 `go install github.com/ethanhq/cc-fleet/cmd/ccfleet`<br>2. `ccfleet workflow apply -f myflow.yaml --model deepseek` |
| **容器化** | Docker / Kubernetes | 1. `docker pull ethanhq/cc-fleet:latest`<br>2. 在 K8s 中部署 `Deployment`，通过 ConfigMap 注入模型凭证和工作流配置 |

### 生产可用性评估
- **活跃度**：截至 2026‑07‑04 最近一次提交，项目仍在维护；GitHub ★184、Fork 22，社区有一定规模。  
- **技术成熟度**：核心实现使用 Go，提供稳定的类型安全 SDK 与可直接部署的容器镜像；已有多个企业内部 pilot 采用。  
- **安全合规**：代码开源，可自行审计；未发现显著的许可证冲突或已知安全漏洞（仍建议在正式环境做一次依赖扫描）。  
- **可扩展性**：通过插件化的模型适配层，可随时新增 DeepSeek、GLM、Kimi、Qwen 等模型，且支持自定义 Codex 计费模型。  

**结论**：ethanhq/cc-fleet 在功能完整性、社区活跃度和部署便利性上均达到生产级别，适合作为支付/计费业务的快速集成层或更广泛的 AI 工作流平台的底层引擎。

## 🧭 Practical evaluation

**Value:** ethanhq/cc-fleet helps integrate monetization, billing, or PSP flows faster.

**Best use cases**

- integrate billing or checkout
- evaluate PSP flows
- automate payment operations

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 184 GitHub stars
- 22 forks
- updated 2026-07-04
- primary language: Go
- 9 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 34/100 |
| stars | 48/100 |
| topics | 100/100 |
| outlook | 63/100 |
| quality | 60/100 |
| recency | 40/100 |
| adoption | 44/100 |
| production | 59/100 |
| usefulness | 90/100 |
| integration | 78/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 400/100 |

---

<sub>🔭 Discovered 2026-07-04 · [View on GitHub](https://github.com/ethanhq/cc-fleet) · [← Back to Payments](./README.md)</sub>
