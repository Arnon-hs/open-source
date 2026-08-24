# symgraph/GhidrAssistMCP

[![Stars](https://img.shields.io/github/stars/symgraph/GhidrAssistMCP?style=flat-square&color=yellow)](https://github.com/symgraph/GhidrAssistMCP/stargazers) [![Forks](https://img.shields.io/github/forks/symgraph/GhidrAssistMCP?style=flat-square&color=blue)](https://github.com/symgraph/GhidrAssistMCP/network) [![Language](https://img.shields.io/badge/lang-Java-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-56%2F100-brightgreen?style=flat-square)](#)

> An native MCP server extension for Ghidra

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 601 |
| 🍴 **Forks** | 46 |
| 💻 **Language** | Java |
| 📈 **Score** | 56/100 |
| 🗓️ **Last push** | 2026-08-24 |
| 🔍 **Source** | github |

## 🏷️ Topics

`ghidra` `ghidra-extension` `ghidra-plugin` `llm` `mcp` `mcp-server` `reverse-engineering`

## 🎯 Categories

MCP · AI/ML · Backend

## 📝 Summary

### English

**Brief Summary**  
symgraph/GhidrAssistMCP is a native MCP (Model Context Protocol) server extension for Ghidra that lets AI assistants interact directly with Ghidra’s reverse‑engineering capabilities via a standard protocol. With 600+ stars, active commits, and a Java‑based SDK/CLI, it offers a ready‑made bridge for integrating large‑language‑model agents into real‑world binary analysis workflows.  

**Value**  
By exposing Ghidra’s functionality through MCP, the project enables AI agents to query, manipulate, and extend disassembly data without custom glue code, turning Ghidra into a first‑class tool in an AI‑driven tooling ecosystem. This standardization reduces integration effort, improves reproducibility, and opens up use cases such as automated vulnerability triage, guided reverse engineering, and on‑demand model‑driven analysis.  

**Practical Adoption Path**  
1. **Prototype** – Clone the repo, run the provided Docker image or start the Java server locally, and use the MCP client SDK to send simple queries (e.g., “list functions in binary”).  
2. **Integrate** – Wrap the MCP client in your AI agent’s toolchain (Python, Java, or any language with gRPC support) and map high‑level prompts to concrete Ghidra commands.  
3. **Scale** – Deploy the MCP server as a microservice behind a load balancer, configure authentication/authorization, and add custom plugins for organization‑specific analyses.  

**Production Readiness**  
The project scores high on production readiness: recent commits (last updated 2026‑05‑11), a healthy star/fork count, and clear API/CLI documentation indicate a mature codebase. While the license and security posture still require a final audit, the active maintainer community and existing adoption signals make it suitable for a serious pilot in environments that already use Ghidra.

### Русский

symgraph/GhidrAssistMCP — это нативное расширение MCP‑сервера для Ghidra, которое позволяет подключать AI‑ассистентов к реальным инструментам и данным через единый протокол Model Context Protocol. Типовой сценарий — развертывание MCP‑сервера, интеграция с Ghidra и последующее подключение AI‑агентов для автоматизированного анализа и взаимодействия с бинарными объектами. Проект имеет высокую готовность к production: активные обновления, более 600 звёзд на GitHub, широкая экосистема и подтверждённая совместимость, хотя лицензия и безопасность требуют окончательной проверки.

### 中文

**项目简介（2‑3 句）**  
symgraph/GhidrAssistMCP 是 Ghidra 的原生 MCP（Model Context Protocol）服务器扩展，提供统一的协议接口，使 AI 助手能够直接调用 Ghidra 的逆向分析功能。它通过标准化的 API/SDK/CLI 将 AI 与真实工具和数据桥接，实现“AI‑in‑the‑loop”的自动化分析工作流。

**价值**  
- **统一协议**：采用 MCP 标准，消除不同 AI 平台与逆向工具之间的集成壁垒。  
- **即插即用**：AI 代理只需遵循协议即可调用 Ghidra 的强大分析能力，无需自行实现复杂的插件或脚本。  
- **加速研发**：帮助安全团队、漏洞研究员快速搭建基于大模型的自动化分析系统，提升效率并降低误差。

**典型接入方式**  
1. **部署 MCP 服务器**：在已有的 Ghidra 环境中启动 GhidrAssistMCP（Java 程序），监听指定端口。  
2. **调用 API/SDK**：AI 代理通过 HTTP/gRPC（或 MCP 定义的消息格式）发送任务请求（如加载二进制、执行函数分析），服务器返回结构化结果。  
3. **CLI 交互**：在脚本或 CI/CD 流程中使用提供的命令行工具，直接发送 MCP 消息，实现自动化批处理。  

**生产可用性**  
- **活跃度**：截至 2026‑05‑11 最近一次提交，GitHub ★601、Fork 46，社区活跃，具备持续维护的潜力。  
- **技术成熟度**：核心使用 Java 实现，符合 Ghidra 官方插件开发规范，易于在企业内部部署。  
- **风险**：暂无重大元数据风险，但仍需对许可证（MIT/Apache）兼容性、代码安全审计以及维护者响应速度进行最终确认。  
总体而言，symgraph/GhidrAssistMCP 已具备在生产环境中进行试点或正式上线的条件。

## 🧭 Practical evaluation

**Value:** symgraph/GhidrAssistMCP helps connect AI assistants to real tools and data through a standard protocol.

**Best use cases**

- connect AI agents to tools
- ship Model Context Protocol servers
- standardize integrations

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 601 GitHub stars
- 46 forks
- updated 2026-05-11
- primary language: Java
- 7 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 42/100 |
| stars | 59/100 |
| topics | 88/100 |
| outlook | 51/100 |
| quality | 58/100 |
| recency | 20/100 |
| adoption | 54/100 |
| production | 51/100 |
| usefulness | 58/100 |
| integration | 62/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 300/100 |

---

<sub>🔭 Discovered 2026-05-11 · [View on GitHub](https://github.com/symgraph/GhidrAssistMCP) · [← Back to Mcp](./README.md)</sub>
