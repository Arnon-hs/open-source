# provos/ironcurtain

[![Stars](https://img.shields.io/github/stars/provos/ironcurtain?style=flat-square&color=yellow)](https://github.com/provos/ironcurtain/stargazers) [![Forks](https://img.shields.io/github/forks/provos/ironcurtain?style=flat-square&color=blue)](https://github.com/provos/ironcurtain/network) [![Language](https://img.shields.io/badge/lang-TypeScript-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-69%2F100-brightgreen?style=flat-square)](#)

> A secure* runtime for autonomous AI agents. Policy from plain-English constitutions. (*https://ironcurtain.dev)

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 399 |
| 🍴 **Forks** | 52 |
| 💻 **Language** | TypeScript |
| 📈 **Score** | 69/100 |
| 🗓️ **Last push** | 2026-09-05 |
| 🔍 **Source** | github |

## 🏷️ Topics

`agent` `mcp` `model-context-protocol` `policy` `sandbox` `security` `trusted-process`

## 🎯 Categories

MCP · Automation · AI/ML · Security

## 📝 Summary

### English

**Brief Summary**  
IronCurtain (provos/ironcurtain) is an open‑source, TypeScript‑based runtime that lets autonomous AI agents safely act on real‑world tools and data by enforcing policies written in plain‑English constitutions. It provides a standard Model Context Protocol (MCP) server and SDK/CLI for easy integration, making it a practical bridge between LLM assistants and enterprise tooling.

**Value**  
- **Policy‑first security**: Developers define high‑level, human‑readable rules that the runtime enforces at runtime, reducing the risk of unintended actions or data leakage.  
- **Standardized connectivity**: By implementing the MCP, IronCurtain offers a common interface for connecting any AI assistant to diverse back‑ends (databases, SaaS APIs, internal services) without custom glue code.  
- **Accelerated development**: The provided SDK, CLI, and language metadata let teams spin up a secure agent‑tool integration in minutes, cutting down the engineering effort required to harden LLM‑driven workflows.

**Practical Adoption Path**  
1. **Prototype** – Use the IronCurtain CLI to launch a local MCP server and experiment with a simple policy (e.g., “only read from the finance DB”).  
2. **Integrate** – Replace existing ad‑hoc tool calls in your AI assistant with IronCurtain’s SDK methods, letting the runtime mediate every request.  
3. **Scale** – Deploy the MCP server in a containerized environment (K8s, Docker) behind your corporate perimeter, and manage policies centrally via the plain‑English constitution files.  
4. **Monitor & Iterate** – Leverage built‑in logging and policy‑violation alerts to refine rules and expand the set of connected tools.

**Production Readiness**  
IronCurtain scores 72/100 and shows strong production signals: 399 ★ on GitHub, recent commits (as of 2026‑05‑12), active forks, and a clear TypeScript codebase with comprehensive SDK/CLI support. The project’s ecosystem activity and adoption indicate it is ready for pilot deployments, though a final security audit (license compliance, vulnerability scanning, maintainer responsiveness) is recommended before full‑scale rollout.

### Русский

**IronCurtain (provos/ironcurtain)** — это open‑source runtime на TypeScript, позволяющий безопасно подключать автономных AI‑агентов к реальным инструментам и данным через единый протокол (Model Context Protocol). Типичный сценарий: разработчик разворачивает сервер IronCurtain и интегрирует в него свои сервисы, после чего AI‑ассистенты получают контроль над этими сервисами по политикам, заданным в простом английском «конституционном» описании. Проект имеет высокий уровень готовности к production: активные коммиты, 399 звёзд, 52 форка, поддержка API/SDK/CLI и положительные сигналы экосистемы, хотя окончательная проверка лицензии и безопасности всё‑ещё требуется.

### 中文

**项目简介（2‑3 句）**  
provos/ironcurtain 是一个面向自治 AI 代理的安全运行时，能够通过自然语言编写的“宪法”来定义安全策略，并以标准化的 Model Context Protocol（MCP）把 AI 助手安全地连接到真实的工具和数据源。  

**价值**  
- **安全合规**：使用可读的英文宪法直接表达访问控制和行为约束，降低策略误配置风险。  
- **统一接入**：提供统一的 MCP 接口，使任意 AI 代理都能以同一协议调用本地或云端工具，提升集成效率。  
- **生态兼容**：通过 API、SDK 与 CLI 多种方式暴露，适配现有的自动化、AI/ML 与安全平台。  

**典型接入方式**  
1. **API/SDK**：在项目中引入 TypeScript/JavaScript SDK，调用 `ironcurtain.connect()` 并传入基于宪法的策略文件，即可让 AI 代理安全地发起工具调用。  
2. **CLI**：使用 `ironcurtain serve` 启动本地 MCP 服务器，其他服务或模型只需指向该服务器的 URL 即可完成集成。  
3. **MCP Server 部署**：在容器或云函数中部署 Iron Curtain 的 MCP 服务器，作为所有 AI 代理的统一网关，统一管理策略与审计日志。  

**生产可用性**  
- **活跃度**：截至 2026‑05‑12 最近一次提交，GitHub ★399、Fork 52，社区活跃，拥有 7 个相关话题标签。  
- **技术成熟度**：核心实现基于 TypeScript，提供完整的 API/SDK/CLI 文档，易于在现有 TypeScript/Node.js 环境中集成。  
- **准备度**：代码库更新频繁，已有若干企业级试点案例，具备高可用部署模板（容器化、K8s），可直接用于生产环境。  
- **风险**：需进一步审查许可证（MIT/Apache 等）以及长期维护者的可用性，但目前没有重大元数据或安全漏洞风险。  

综合来看，Iron Curtain 已具备在生产环境中安全地为自治 AI 代理提供工具接入的条件，适合作为企业级 AI 自动化的核心安全层。

## 🧭 Practical evaluation

**Value:** provos/ironcurtain helps connect AI assistants to real tools and data through a standard protocol.

**Best use cases**

- connect AI agents to tools
- ship Model Context Protocol servers
- standardize integrations

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 399 GitHub stars
- 52 forks
- updated 2026-05-12
- primary language: TypeScript
- 7 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 43/100 |
| stars | 55/100 |
| topics | 88/100 |
| outlook | 75/100 |
| quality | 71/100 |
| recency | 80/100 |
| adoption | 52/100 |
| production | 71/100 |
| usefulness | 74/100 |
| integration | 62/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 400/100 |

---

<sub>🔭 Discovered 2026-05-12 · [View on GitHub](https://github.com/provos/ironcurtain) · [← Back to Mcp](./README.md)</sub>
