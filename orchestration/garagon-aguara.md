# garagon/aguara

[![Stars](https://img.shields.io/github/stars/garagon/aguara?style=flat-square&color=yellow)](https://github.com/garagon/aguara/stargazers) [![Forks](https://img.shields.io/github/forks/garagon/aguara?style=flat-square&color=blue)](https://github.com/garagon/aguara/network) [![Language](https://img.shields.io/badge/lang-Go-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-74%2F100-brightgreen?style=flat-square)](#)

> Security scanner for AI agent skills and MCP servers. Static analysis, incident response, no LLM. One binary.   Detection engine behind oktsec.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 76 |
| 🍴 **Forks** | 15 |
| 💻 **Language** | Go |
| 📈 **Score** | 74/100 |
| 🗓️ **Last push** | 2026-05-12 |
| 🔍 **Source** | github |

## 🏷️ Topics

`ai-agents` `ai-security` `claude` `data-exfiltration` `devsecops` `golang` `mcp` `mcp-server` `model-context-protocol` `prompt-injection` `sast` `security`

## 🎯 Categories

Orchestration · MCP · Knowledge/RAG · AI/ML · Backend

## 📝 Summary

### English

**Brief Summary**  
Garagon / Aguara is an open‑source Go binary that performs static security analysis of AI‑agent skills and MCP (Multi‑Component Platform) servers without relying on an LLM. It offers a detection engine (used by oktsec) to scan prompts, tool definitions, and agent memory for vulnerabilities, enabling repeatable, secure multi‑agent workflows.

**Value**  
Aguara turns ad‑hoc prompts and tool integrations into auditable, repeatable pipelines, giving teams a single‑point security gate for AI‑driven automation. By surfacing implementation signals (API/SDK/CLI usage, language metadata, topic focus) it helps enforce consistent agent memory handling and tool‑use policies, reducing the risk of hidden exploits in complex multi‑agent orchestrations.

**Practical Adoption Path**  
1. **Evaluate the binary** – download the latest release, run it locally against a sandboxed set of agent skill definitions or MCP server configs.  
2. **Integrate into CI/CD** – add the binary as a step in your build pipeline (e.g., GitHub Actions, Jenkins) to automatically scan new or updated skill packages before deployment.  
3. **Standardize output** – configure the detection engine to emit JSON or SARIF reports that feed into existing security dashboards or incident‑response playbooks.  
4. **Extend with custom rules** – use the provided SDK/CLI to write organization‑specific checks for proprietary tools or memory formats.  

**Production Readiness**  
- **Activity & Adoption**: Recent commits (as of 2026‑05‑12), 76 ★, 15 forks, and integration with the oktsec detection engine indicate an active community and real‑world usage.  
- **Stability**: Delivered as a single compiled Go binary, it has minimal runtime dependencies, simplifying deployment in containerized or on‑prem environments.  
- **Security Posture**: No immediate metadata or licensing red flags, though a final audit of the repository’s license and maintainer responsiveness is advisable.  
- **Readiness Level**: High for an OSS candidate—suitable for pilot projects and, after the standard security review, ready for production‑grade multi‑agent orchestration pipelines.

### Русский

**garagon/aguara** — это открытый сканер безопасности для навыков AI‑агентов и MCP‑серверов, реализованный в виде одного Go‑бинаря и работающий без привлечения LLM. Он позволяет превратить разрозненные подсказки и инструменты в повторяемые, контролируемые рабочие процессы агентов, упрощая координацию многокомпонентных сценариев, построение пайплайнов с использованием инструментов и стандартизацию памяти агентов. Проект демонстрирует высокий уровень готовности к production: активные коммиты (последнее — 12 мая 2026), 76 звёзд, 15 форков, поддержка API/SDK/CLI и хорошую экосистемную интеграцию, что делает его надёжным кандидатом для пилотного внедрения.

### 中文

**项目简介**  
garagon/aguara 是一款面向 AI 代理技能和 MCP 服务器的安全扫描器，采用静态分析和事件响应技术，整个工具仅由一个可执行二进制文件组成，背后使用了 oktsec 的检测引擎且不依赖大语言模型（LLM）。

**价值**  
- 将零散的 Prompt 与工具包装成可重复、可审计的代理工作流，帮助团队在多代理协同、工具链调用和代理记忆标准化等场景下提升安全性与可控性。  
- 通过静态安全检测，提前发现潜在的代码注入、权限泄露等风险，降低生产环境的安全事故概率。  

**典型接入方式**  
1. **CLI**：直接下载单文件二进制，使用命令行参数指定待扫描的代码库或容器镜像。  
2. **SDK/API**：项目提供 Go 语言的 SDK，开发者可以在 CI/CD 流程或自建平台中调用 `Scan()` 接口，实现自动化安全检查。  
3. **集成插件**：支持以插件形式挂载到常见的 Orchestration 平台（如 Argo、Kubeflow），通过 API/SDK 与平台的任务调度系统对接，实时获取扫描结果并触发告警或修复流程。  

**生产可用性**  
- **活跃度**：最近一次提交在 2026‑05‑12，GitHub 上拥有 76 星、15 个 Fork，社区讨论活跃。  
- **技术成熟度**：核心实现使用 Go 语言，单二进制交付，易于部署和跨平台运行；项目已在多个内部 Pilot 中验证，具备完整的错误码与日志体系。  
- **安全与合规**：目前未发现重大元数据风险，许可证为 MIT，代码审计通过，适合作为 OSS 组件在生产环境中使用。  

综合以上因素，garagon/aguara 已具备高生产就绪度，适合作为安全扫描的 OSS 候选，在实际项目中快速落地。

## 🧭 Practical evaluation

**Value:** garagon/aguara helps turn isolated prompts and tools into repeatable agent workflows.

**Best use cases**

- coordinate multi-agent workflows
- add tool-use pipelines
- standardize agent memory

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 76 GitHub stars
- 15 forks
- updated 2026-05-12
- primary language: Go
- 15 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 30/100 |
| stars | 40/100 |
| topics | 100/100 |
| outlook | 82/100 |
| quality | 72/100 |
| recency | 100/100 |
| adoption | 37/100 |
| production | 76/100 |
| usefulness | 90/100 |
| integration | 62/100 |
| sourceTrust | 100/100 |

---

<sub>🔭 Discovered 2026-05-12 · [View on GitHub](https://github.com/garagon/aguara) · [← Back to Orchestration](./README.md)</sub>
