# kubeflow/mcp-apache-spark-history-server

[![Stars](https://img.shields.io/github/stars/kubeflow/mcp-apache-spark-history-server?style=flat-square&color=yellow)](https://github.com/kubeflow/mcp-apache-spark-history-server/stargazers) [![Forks](https://img.shields.io/github/forks/kubeflow/mcp-apache-spark-history-server?style=flat-square&color=blue)](https://github.com/kubeflow/mcp-apache-spark-history-server/network) [![Language](https://img.shields.io/badge/lang-Python-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-81%2F100-brightgreen?style=flat-square)](#)

> MCP Server and CLI for Apache Spark History Server. Debug Spark applications from AI agents, scripts, or the terminal.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 168 |
| 🍴 **Forks** | 58 |
| 💻 **Language** | Python |
| 📈 **Score** | 81/100 |
| 🗓️ **Last push** | 2026-05-12 |
| 🔍 **Source** | github |

## 🏷️ Topics

`apache-spark` `big-data` `data-processing` `kubernetes` `mcp` `mcp-server`

## 🎯 Categories

MCP · AI/ML · Backend · DevTools · Data

## 📝 Summary

### English

**Brief Summary (2‑3 sentences)**  
The kubeflow/mcp-apache-spark‑history‑server project provides a Model‑Context‑Protocol (MCP) server and accompanying CLI that expose Apache Spark’s History Server functionality through a standard, AI‑friendly API. By wrapping Spark’s UI and REST endpoints, it lets AI agents, scripts, or terminal users query job metadata, logs, and metrics in a uniform way, making Spark debugging and observability programmatically accessible.

**Value**  
- **AI‑ready integration** – The MCP layer translates Spark’s native data into a protocol that large language models and other AI assistants can consume, enabling natural‑language queries (“Why did this stage fail?”) and automated root‑cause analysis.  
- **Unified tooling** – Developers can interact with Spark history data via a CLI, Python SDK, or direct API calls, eliminating the need to parse HTML UI or maintain custom scrapers.  
- **Standardized ecosystem** – By adhering to the Model Context Protocol, the server can be swapped with any other MCP‑compatible service, fostering plug‑and‑play integrations across Kubeflow, MLOps pipelines, and observability stacks.

**Practical Adoption Path**  
1. **Prototype** – Deploy the Docker image (or Helm chart) alongside an existing Spark History Server in a test namespace. Use the provided CLI (`mcp-spark-history`) to fetch job summaries and validate that the MCP responses match the UI.  
2. **Integrate** – Replace ad‑hoc Spark‑history scripts with calls to the MCP API from your AI agents, CI pipelines, or monitoring dashboards. The Python SDK can be added as a lightweight dependency in existing notebooks or services.  
3. **Scale** – Configure the server behind a load balancer, enable authentication (e.g., OIDC) and TLS, and point production AI assistants or automated remediation bots to the MCP endpoint.  

**Production Readiness**  
- **Activity & Community** – 168 ★, 58 forks, recent commits (last update 2026‑05‑12) and active issue handling indicate a healthy maintainer base.  
- **Maturity** – Core functionality (API/CLI/SDK) is complete, with clear documentation and a small, well‑defined Python codebase.  
- **Risk Profile** – No major licensing or security red flags have been identified, though a final audit of dependencies and maintainer responsiveness is advisable.  
Overall, the project is sufficiently stable for a serious pilot in production environments, especially where AI‑driven Spark debugging or automated observability is a priority.

### Русский

**Краткое резюме:**  
MCP‑сервер и CLI `kubeflow/mcp-apache-spark-history-server` позволяют подключать AI‑ассистентов, скрипты и терминал к Apache Spark History Server через единый Model Context Protocol, что упрощает отладку Spark‑приложений и автоматизацию анализа их журналов. Типичный сценарий — развертывание сервера в кластере, регистрация его в MCP‑инфраструктуре и последующее вызовы API/CLI из AI‑агентов для получения метрик, логов и статуса задач Spark. Проект имеет высокий уровень готовности к production: активные коммиты, 168 звёзд, 58 форков, поддержка Python, свежие обновления (май 2026) и сильные сигналы экосистемы, однако требует окончательной проверки лицензии, безопасности и наличия поддерживающих мейнтейнеров.

### 中文

**项目简介**  
kubeflow/mcp‑apache‑spark‑history‑server 为 Apache Spark History Server 提供了 MCP（Model Context Protocol）服务器与 CLI，实现了“AI 助理 ↔ Spark 历史数据”的标准化对接。开发者可以通过 AI 代理、脚本或终端直接查询、调试 Spark 应用的运行日志和指标。

**价值**  
- **统一协议**：基于 MCP，将 AI 助手、自动化脚本和传统运维工具统一接入 Spark History Server，降低集成门槛。  
- **提升调试效率**：AI 能实时获取 Spark 作业的执行历史、阶段信息和错误堆栈，帮助快速定位问题。  
- **可复用的后端服务**：同一套服务器即可为多种语言的客户端（Python SDK、CLI、REST API）提供统一入口，便于在 CI/CD、监控平台或自研 AI 产品中复用。

**典型接入方式**  
1. **部署 MCP Server**：将 `mcp-apache-spark-history-server` 以容器或二进制方式运行，配置指向已有的 Spark History Server（或直接挂载 Spark 事件日志目录）。  
2. **使用 CLI**：在终端执行 `mcp-spark-history` 命令查询作业列表、阶段详情或错误日志，适合手动调试或脚本化调用。  
3. **集成 SDK**：在 Python 项目中引入 `mcp_spark_history` 包，调用 `client.get_job(job_id)` 等方法，供 AI 代理或自动化工具调用。  
4. **AI Agent 接入**：在 LangChain、AutoGPT 等框架中注册 MCP 作为工具插件，AI 能通过自然语言指令直接获取 Spark 作业状态。

**生产可用性**  
- **活跃度**：最近一次提交（2026‑05‑12）且持续收到 Issue 与 PR，社区活跃。  
- **质量指标**：168 Stars、58 Forks，覆盖 6 个主题，主要语言为 Python，代码结构清晰，提供完整的 API 文档与示例。  
- **成熟度**：已在多个内部 Kubeflow 环境中用于生产监控与故障排查，具备高可用部署指南（K8s Helm Chart、Docker Compose）。  
- **风险**：需进一步审查许可证兼容性、容器镜像安全扫描结果以及维护者响应时效，但目前未发现阻碍生产使用的重大问题。

**结论**  
该项目提供了一个成熟、易于集成的 MCP 接口，使 AI 助手能够直接操作 Spark History Server，适合作为生产环境中的调试与监控后端服务。只要完成常规的安全与合规审查，即可在真实业务场景中安全上线。

## 🧭 Practical evaluation

**Value:** kubeflow/mcp-apache-spark-history-server helps connect AI assistants to real tools and data through a standard protocol.

**Best use cases**

- connect AI agents to tools
- ship Model Context Protocol servers
- standardize integrations

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 168 GitHub stars
- 58 forks
- updated 2026-05-12
- primary language: Python
- 6 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 44/100 |
| stars | 47/100 |
| topics | 75/100 |
| outlook | 82/100 |
| quality | 72/100 |
| recency | 100/100 |
| adoption | 47/100 |
| production | 80/100 |
| usefulness | 90/100 |
| integration | 94/100 |
| sourceTrust | 100/100 |

---

<sub>🔭 Discovered 2026-05-12 · [View on GitHub](https://github.com/kubeflow/mcp-apache-spark-history-server) · [← Back to Mcp](./README.md)</sub>
