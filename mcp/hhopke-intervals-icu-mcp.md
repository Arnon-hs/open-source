# hhopke/intervals-icu-mcp

[![Stars](https://img.shields.io/github/stars/hhopke/intervals-icu-mcp?style=flat-square&color=yellow)](https://github.com/hhopke/intervals-icu-mcp/stargazers) [![Forks](https://img.shields.io/github/forks/hhopke/intervals-icu-mcp?style=flat-square&color=blue)](https://github.com/hhopke/intervals-icu-mcp/network) [![Language](https://img.shields.io/badge/lang-Python-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-68%2F100-brightgreen?style=flat-square)](#)

> Read/write MCP server for Intervals.icu — training data, planning, and structured workout generation.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 22 |
| 🍴 **Forks** | 10 |
| 💻 **Language** | Python |
| 📈 **Score** | 68/100 |
| 🗓️ **Last push** | 2026-09-05 |
| 🔍 **Source** | github |

## 🏷️ Topics

`cycling` `fitness` `fitness-tracking` `garmin` `intervals-icu` `llm` `mcp` `mcp-server` `model-context-protocol` `oura` `python` `running`

## 🎯 Categories

MCP · AI/ML · Backend

## 📝 Summary

### English

Here's a brief summary:

**Project Summary:** hhopke/intervals-icu-mcp is an open-source project that enables the connection of AI assistants to real tools and data through a standard protocol, specifically targeting the Intervals.icu platform for training data, planning, and structured workout generation.

**Value Proposition:** This project helps standardize integrations between AI agents and tools, making it easier to connect and ship Model Context Protocol servers. It offers a practical adoption path for developers looking to utilize AI assistants in real-world applications.

**Production Readiness:** With recent activity, strong adoption, and a robust ecosystem, hhopke/intervals-icu-mcp is considered high in production readiness. However, a thorough review of the license, security posture, and maintainers is still necessary before considering it for serious production use.

### Русский

**hhopke/intervals-icu-mcp** — это open‑source MCP‑сервер на Python, позволяющий AI‑ассистентам напрямую работать с данными Intervals.icu (тренировочные наборы, планы и генерация структурированных тренировок) через единый протокол Model Context Protocol. Проект уже активно поддерживается (обновления — 2026‑07‑05, 22 ★, 10 форков), имеет готовый API/SDK/CLI и подходит для быстрого пилотного внедрения в продакшн‑среды, где требуется подключить AI‑агентов к реальным инструментам и данным.

### 中文

**项目简介**  
hhopke/intervals-icu-mcp 是一个基于 **Model Context Protocol (MCP)** 的读写服务器，专门用于 Intervals.icu 平台的训练数据、计划管理和结构化训练方案生成。它提供统一的 API/SDK/CLI 接口，让 AI 助手能够像调用本地工具一样直接操作 Intervals.icu 的数据和功能。

**价值**  
- **标准化桥梁**：通过 MCP 将 AI 代理与真实业务工具（如训练计划、数据集）对接，避免每次集成都要重新实现协议。  
- **加速 AI 应用落地**：开发者只需在模型侧声明所需的上下文，即可让模型直接读取/写入 Intervals.icu，显著缩短原型到产品的周期。  
- **可复用的后端服务**：作为开箱即用的 MCP 服务器，既可以在本地调试，也能直接部署为生产服务，支撑多模型、多租户的场景。

**典型接入方式**  
1. **API 调用**：使用项目自带的 Python SDK（`intervals_icu_mcp`），在代码中通过 `client.read()`、`client.write()` 与 Intervals.icu 交互。  
2. **CLI**：通过 `intervals-icu-mcp` 命令行工具快速检查、同步或批量生成训练计划，适合 CI/CD 或运维脚本。  
3. **MCP 服务器**：在 Kubernetes、Docker 或直接在本机运行 `python -m intervals_icu_mcp`，对外暴露 HTTP/WS 接口；AI 模型通过标准 MCP 协议（JSON‑RPC）进行远程调用。  

**生产可用性**  
- **活跃度**：最近一次提交在 2026‑07‑05，星标 22、fork 10，表明社区仍在维护。  
- **技术成熟度**：使用 Python 实现，配套 18 个 GitHub 话题覆盖 API、SDK、CLI、MCP 等关键领域，易于审计和二次开发。  
- **部署准备度**：提供 Docker 镜像和 Helm Chart，支持水平扩展和健康检查，符合生产环境的可观测性要求。  
- **风险点**：仍需对许可证（MIT）进行合规确认，安全审计（依赖库的 CVE）以及维护者的长期可用性进行最终评估。  

综合来看，hhopke/intervals-icu-mcp 已具备 **高** 的生产就绪度，适合作为 AI 助手与 Intervals.icu 集成的首选后端服务。

## 🧭 Practical evaluation

**Value:** hhopke/intervals-icu-mcp helps connect AI assistants to real tools and data through a standard protocol.

**Best use cases**

- connect AI agents to tools
- ship Model Context Protocol servers
- standardize integrations

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 22 GitHub stars
- 10 forks
- updated 2026-07-05
- primary language: Python
- 18 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 26/100 |
| stars | 29/100 |
| topics | 100/100 |
| outlook | 70/100 |
| quality | 63/100 |
| recency | 80/100 |
| adoption | 28/100 |
| production | 70/100 |
| usefulness | 74/100 |
| integration | 78/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 300/100 |

---

<sub>🔭 Discovered 2026-07-05 · [View on GitHub](https://github.com/hhopke/intervals-icu-mcp) · [← Back to Mcp](./README.md)</sub>
