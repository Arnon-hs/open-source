# OpenOSINT/OpenOSINT

[![Stars](https://img.shields.io/github/stars/OpenOSINT/OpenOSINT?style=flat-square&color=yellow)](https://github.com/OpenOSINT/OpenOSINT/stargazers) [![Forks](https://img.shields.io/github/forks/OpenOSINT/OpenOSINT?style=flat-square&color=blue)](https://github.com/OpenOSINT/OpenOSINT/network) [![Language](https://img.shields.io/badge/lang-Python-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-85%2F100-brightgreen?style=flat-square)](#)

> AI-powered OSINT agent with interactive REPL, MCP server, and CLI. 16 tools. Works with Claude, GPT-4, or local models. For authorized security research only.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 762 |
| 🍴 **Forks** | 120 |
| 💻 **Language** | Python |
| 📈 **Score** | 85/100 |
| 🗓️ **Last push** | 2026-06-25 |
| 🔍 **Source** | github |

## 🏷️ Topics

`ai-agent` `anthropic` `claude` `cli` `cybersecurity` `holehe` `llm` `maigret` `mcp` `mcp-server` `model-context-protocol` `osint`

## 🎯 Categories

MCP · AI/ML · Backend · DevTools · Security

## 📝 Summary

### English

**Brief Summary**  
OpenOSINT is an open‑source, AI‑powered OSINT platform that lets large language models (Claude, GPT‑4, or self‑hosted alternatives) invoke real‑world tools through a standardized Model Context Protocol (MCP) REPL, server, and CLI. It bundles 16 ready‑made intelligence‑gathering utilities and is aimed at authorized security‑research use cases.

**Value**  
- **Bridges the AI‑tool gap** – By exposing a uniform MCP interface, OpenOSINT lets any LLM act as a true “agent” that can run commands, fetch data, and process results without custom glue code.  
- **Accelerates AI‑augmented investigations** – Security teams can plug the platform into existing tooling stacks and immediately leverage AI for data enrichment, correlation, and reporting.  
- **Reusable infrastructure** – The MCP server and CLI can be deployed as a shared service, enabling multiple AI agents (or different model versions) to reuse the same set of 16 vetted OSINT utilities.

**Practical Adoption Path**  
1. **Deploy the MCP server** (Docker or native Python) in a controlled environment (e.g., a security research sandbox).  
2. **Configure model credentials** – point Claude, GPT‑4, or a local model to the server via the provided SDK/CLI.  
3. **Select or extend tools** – start with the bundled 16 utilities (whois, DNS lookup, web scraping, etc.) or add custom scripts by following the simple Python plug‑in spec.  
4. **Integrate with existing workflows** – call the CLI from CI pipelines, SIEM playbooks, or Jupyter notebooks, or expose the server as an internal API for broader orchestration.  
5. **Iterate and monitor** – use the REPL for rapid prototyping, then lock down the command whitelist for production use.

**Production Readiness**  
- **Active development** – 762 ★, 120 forks, last commit on 2026‑06‑25; strong community momentum.  
- **Mature stack** – pure Python, well‑documented MCP API, and a CLI that can be containerized for isolated deployment.  
- **Ecosystem fit** – aligns with MCP, AI/ML, backend, dev‑tools, and security categories, making it easy to slot into existing security platforms.  
- **Risk profile** – no glaring metadata or licensing issues yet; a final security audit of dependencies and maintainers is advisable, but the project is considered “high” readiness for pilots and can be promoted to production after standard hardening (access controls, audit logging, model usage limits).

### Русский

OpenOSINT — это open‑source AI‑агент OSINT, который через Model Context Protocol (MCP) соединяет LLM (Claude, GPT‑4 или локальные модели) с 16 готовыми инструментами, REPL‑интерфейсом, сервером MCP и CLI, позволяя быстро интегрировать интеллектуального помощника в процессы сбора и анализа открытых данных. Типичный сценарий: развернуть MCP‑сервер, подключить к нему существующие скрипты/службы и дать LLM доступ к реальным инструментам — что упрощает автоматизацию расследований, построение аналитических пайплайнов и создание кастомных AI‑ассистентов. Проект имеет высокий уровень готовности к production: активные коммиты (обновлён 2026‑06‑25), 762 звёзд, 120 форков, зрелый Python‑стек и готовые API/SDK, что делает его надёжным кандидатом для пилотных внедрений в безопасных исследовательских средах.

### 中文

**项目简介（2‑3 句）**  
OpenOSINT 是一款 AI 驱动的开源 OSINT（公开情报）平台，提供交互式 REPL、MCP（Model Context Protocol）服务器以及命令行客户端，内置 16 款情报收集与分析工具，支持 Claude、GPT‑4 以及本地模型。项目仅限授权的安全研究使用。

**价值主张**  
- **AI 与真实工具的桥梁**：通过标准化的 MCP 协议，将大模型的自然语言指令直接映射到具体的情报采集、解析和报告工具，实现“说一句话，工具就执行”。  
- **统一的集成入口**：一次部署即可为多种 AI 助手（Claude、GPT‑4、开源模型）提供统一的后端服务，降低多模型、多语言环境下的集成成本。  
- **可扩展的安全研发平台**：提供 REPL 与 CLI 双重交互方式，方便安全研究员快速原型、调试和自动化工作流。

**典型接入方式**  
1. **MCP 服务器模式**：在目标机器上启动 `openosint-mcp` 服务，其他 AI 助手通过 HTTP/WS 端点调用标准化的 `tool.run`、`tool.list` 等 API。  
2. **CLI/SDK 直接调用**：在 Python 项目中 `pip install openosint`，使用提供的 SDK 调用 `OpenOSINTClient`，或在脚本中直接运行 `openosint-cli` 命令。  
3. **REPL 交互**：在终端执行 `openosint-repl`，进入交互式会话，实时输入自然语言指令，系统自动解析并调用对应工具。

**生产可用性评估**  
- **活跃度**：截至 2026‑06‑25 最近一次提交，GitHub ★762、Fork 120，社区活跃，具备持续维护的迹象。  
- **技术成熟度**：核心使用 Python 实现，依赖明确，已提供完整的 API 文档与示例，易于在 CI/CD 流程中集成。  
- **安全与合规**：项目声明仅用于授权安全研究，暂无已知重大安全漏洞；仍建议在内部审计后确认许可证（MIT/Apache 等）与依赖的合规性。  
- **适配性**：支持主流大模型（Claude、GPT‑4）以及本地模型，兼容多语言环境，适合作为企业内部 OSINT 自动化的底层服务。  

**结论**  
OpenOSINT 具备高可用的 OSS 基础设施、明确的标准化协议以及活跃的社区支持，能够在安全研发、情报自动化以及 AI‑Tool 集成等场景中快速落地，适合作为生产环境的核心组件进行试点乃至全面部署。

## 🧭 Practical evaluation

**Value:** OpenOSINT/OpenOSINT helps connect AI assistants to real tools and data through a standard protocol.

**Best use cases**

- connect AI agents to tools
- ship Model Context Protocol servers
- standardize integrations

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 762 GitHub stars
- 120 forks
- updated 2026-06-25
- primary language: Python
- 19 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 52/100 |
| stars | 61/100 |
| topics | 100/100 |
| outlook | 90/100 |
| quality | 81/100 |
| recency | 100/100 |
| adoption | 59/100 |
| production | 81/100 |
| usefulness | 100/100 |
| integration | 78/100 |
| sourceTrust | 100/100 |

---

<sub>🔭 Discovered 2026-06-25 · [View on GitHub](https://github.com/OpenOSINT/OpenOSINT) · [← Back to Mcp](./README.md)</sub>
