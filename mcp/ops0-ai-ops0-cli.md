# ops0-ai/ops0-cli

[![Stars](https://img.shields.io/github/stars/ops0-ai/ops0-cli?style=flat-square&color=yellow)](https://github.com/ops0-ai/ops0-cli/stargazers) [![Forks](https://img.shields.io/github/forks/ops0-ai/ops0-cli?style=flat-square&color=blue)](https://github.com/ops0-ai/ops0-cli/network) [![Language](https://img.shields.io/badge/lang-Go-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-79%2F100-brightgreen?style=flat-square)](#)

> Stop your AI agent from shipping insecure IaC. ops0 CLI sits between Claude Code, Codex or Gemini and your cloud, scanning every .tf the agent writes and blocking destroy commands before they run.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 64 |
| 🍴 **Forks** | 3 |
| 💻 **Language** | Go |
| 📈 **Score** | 79/100 |
| 🗓️ **Last push** | 2026-05-13 |
| 🔍 **Source** | github |

## 🏷️ Topics

`ai-agents` `audit-log` `claude-code` `cli-tool` `codex` `devsecops` `gemini-cli` `golang-cli` `governance` `iac` `mcp` `opentofu`

## 🎯 Categories

MCP · AI/ML · DevTools · Database · DevOps/Infra

## 📝 Summary

### English

**Brief Summary (2‑3 sentences)**  
The ops0‑cli project acts as a safety gate between AI code‑generation models (Claude, Codex, Gemini) and your cloud infrastructure, automatically scanning every Terraform file the agent produces and blocking any `destroy` commands before they are applied. By exposing a standard protocol for connecting AI assistants to real tools and data, it lets teams integrate generative AI into DevOps workflows without risking insecure or destructive IaC changes.  

**Value**  
- **Security‑first AI integration** – Prevents accidental or malicious destruction of cloud resources, addressing a major concern when letting LLMs write infrastructure‑as‑code.  
- **Standardized connectivity** – Implements the Model Context Protocol, making it easy to plug any compatible AI assistant or custom model into your existing CI/CD pipeline.  
- **Low‑overhead enforcement** – Works as a CLI wrapper around Terraform, requiring no changes to existing IaC codebases while providing real‑time validation.

**Practical Adoption Path**  
1. **Install the CLI** (`go install github.com/ops0-ai/ops0-cli/...`) on the machine that runs Terraform.  
2. **Configure the hook** by adding the provided wrapper script to your CI/CD pipeline or local development workflow (e.g., replace `terraform apply` with `ops0-cli apply`).  
3. **Connect your AI agent** – set the model’s output endpoint to point at the CLI or use the supplied SDK to invoke the CLI programmatically.  
4. **Tune policies** – adjust the built‑in rule set or add custom filters (e.g., block specific resource types) via the simple YAML config.  
5. **Monitor & iterate** – use the generated audit logs to refine the policy and to demonstrate compliance to security teams.

**Production Readiness**  
- **Activity & community** – Recent commits (as of 2026‑05‑13), 64 GitHub stars, and active issue discussions indicate a healthy open‑source project.  
- **Maturity** – The Go implementation is lightweight, the CLI has a clear API/SDK surface, and the repository includes example integrations and CI pipelines.  
- **Risk profile** – No major licensing or security red flags have been identified, though a final review of the license and maintainer responsiveness is advisable before a full‑scale rollout.  
Overall, ops0‑cli is a strong candidate for a pilot in production environments where AI‑generated IaC is being adopted, offering immediate security safeguards with a modest integration effort.

### Русский

ops0‑cli — это open‑source‑утилита, которая ставит барьер между LLM‑агентами (Claude, Codex, Gemini) и вашими облачными ресурсами, автоматически сканируя генерируемый код Terraform и блокируя команды `destroy` до их выполнения, тем самым устраняя риск внедрения небезопасной инфраструктуры. Типичный сценарий: подключаете ops0‑cli к вашему CI/CD или к Model Context Protocol‑серверу, и любой AI‑ассистент, пишущий `.tf`‑файлы, проходит через проверку безопасности перед деплоем. По активности репозитория (Go‑код, 64 звёзд, недавние коммиты, поддержка API/SDK/CLI) проект считается готовым к пилотному запуску в продакшн, хотя окончательная проверка лицензии и безопасности всё‑ещё требуется.

### 中文

**项目简介**  
ops0‑cli 是一款位于 AI 代码生成模型（Claude Code、Codex、Gemini 等）和云基础设施之间的安全守门员。它会在 AI 生成的 Terraform（*.tf）文件中实时扫描，拦截所有可能导致资源销毁的 `destroy` 指令，从而防止不安全的 IaC 直接上线。

**核心价值**  
- **安全防护**：在 AI 自动化写 IaC 时即时检测并阻断破坏性操作，避免因模型误判导致的云资源意外删除或费用激增。  
- **标准化接入**：通过统一的 Model Context Protocol（MCP）以及提供的 CLI、API/SDK 接口，让各种 AI 助手、内部工具或自研模型都能以同一方式接入并受益。  
- **快速集成**：只需在 CI/CD 流程或本地开发环境中把 `ops0-cli` 加入 Terraform 执行前的步骤，即可实现全链路安全审计。

**典型接入方式**  
| 场景 | 接入方式 | 关键步骤 |
|------|----------|----------|
| 本地开发 | 直接使用 CLI | `ops0 scan --path ./infra` → 通过后再执行 `terraform apply` |
| CI/CD 流水线 | 在 Terraform 步骤前插入 CLI 调用 | 在 GitHub Actions、GitLab CI、Jenkins 等脚本中加入 `ops0 scan`，失败即中止后续部署 |
| AI Agent 集成 | 调用提供的 Go SDK / HTTP API | AI 生成 `.tf` 后，使用 SDK 将文件发送至 ops0，获取审计结果后决定是否提交 |
| MCP 服务器 | 部署 ops0 作为 MCP 后端 | 通过标准化的 Model Context Protocol 与多种 AI 模型交互，实现统一审计与策略下发 |

**生产可用性**  
- **活跃度**：最近一次提交（2026‑05‑13）且持续收到社区 PR，GitHub ★64、Fork 3，表明项目仍在维护。  
- **技术成熟度**：核心实现使用 Go，语言本身具备高并发、低资源占用的特性，适合在高频率的 CI/CD 场景中运行。  
- **生态兼容**：提供 CLI、REST API 与 Go SDK，能够轻松嵌入现有的 Terraform 工作流或自研 AI 平台。  
- **风险**：目前尚未完成完整的许可证审查和安全审计；在正式大规模部署前建议进行内部代码审查并确认维护者的响应能力。

**结论**  
ops0‑cli 已具备较高的生产就绪度，适合作为 AI‑generated IaC 的安全层，在保证开发效率的同时显著降低因模型失误导致的基础设施风险。只要完成最终的许可证与安全合规检查，即可在企业级环境中进行试点或直接上线。

## 🧭 Practical evaluation

**Value:** ops0-ai/ops0-cli helps connect AI assistants to real tools and data through a standard protocol.

**Best use cases**

- connect AI agents to tools
- ship Model Context Protocol servers
- standardize integrations

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 64 GitHub stars
- 3 forks
- updated 2026-05-13
- primary language: Go
- 15 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 15/100 |
| stars | 39/100 |
| topics | 100/100 |
| outlook | 83/100 |
| quality | 69/100 |
| recency | 100/100 |
| adoption | 32/100 |
| production | 77/100 |
| usefulness | 100/100 |
| integration | 78/100 |
| sourceTrust | 100/100 |

---

<sub>🔭 Discovered 2026-05-13 · [View on GitHub](https://github.com/ops0-ai/ops0-cli) · [← Back to Mcp](./README.md)</sub>
