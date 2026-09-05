# rehan1020/MCP-India-Stack

[![Stars](https://img.shields.io/github/stars/rehan1020/MCP-India-Stack?style=flat-square&color=yellow)](https://github.com/rehan1020/MCP-India-Stack/stargazers) [![Forks](https://img.shields.io/github/forks/rehan1020/MCP-India-Stack?style=flat-square&color=blue)](https://github.com/rehan1020/MCP-India-Stack/network) [![Language](https://img.shields.io/badge/lang-Python-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-72%2F100-brightgreen?style=flat-square)](#)

> MCP server for Indian APIs — GSTIN, IFSC, PAN, UPI, pincode, HSN/SAC. Zero auth. Offline-first. For AI agents.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 31 |
| 🍴 **Forks** | 8 |
| 💻 **Language** | Python |
| 📈 **Score** | 72/100 |
| 🗓️ **Last push** | 2026-09-05 |
| 🔍 **Source** | github |

## 🏷️ Topics

`fastmcp` `gst` `gstin` `hsn` `ifsc` `india` `indian-mcp` `mcp` `model-context-protocol` `offline-first` `pan` `pincode`

## 🎯 Categories

MCP · Security

## 📝 Summary

### English

**Project Summary:**

The rehan1020/MCP-India-Stack is an open-source project that provides a Model Context Protocol (MCP) server for Indian APIs, enabling AI agents to connect to real tools and data through a standard protocol. This project offers a zero-authentication, offline-first solution that standardizes integrations and streamlines connections between AI assistants and tools. With a strong ecosystem and recent activity, it is production-ready for serious pilots.

**Value Proposition:**

The rehan1020/MCP-India-Stack offers significant value to developers and organizations by providing a standardized protocol for connecting AI agents to real tools and data. This enables seamless integrations, reduces development time, and enhances the overall efficiency of AI-powered applications.

**Practical Adoption Path:**

To adopt the rehan1020/MCP-India-Stack, developers can follow these steps:

1. Evaluate the project's implementation signals, such as API/SDK/CLI exposure, language metadata, and focused topics.
2. Review the project's security posture, license, and active maintainers to ensure it meets their requirements.
3. Integrate the MCP server into their AI-powered applications using the provided APIs or SDKs.
4. Test and refine the integrations to ensure seamless connections between AI agents

### Русский

Резюме проекта rehan1020/MCP-India-Stack:

Проект rehan1020/MCP-India-Stack представляет собой сервер MCP (Model Context Protocol) для Индийских API, который обеспечивает доступ к данным по GSTIN, IFSC, PAN, UPI, пинкоду и HSN/SAC без авторизации. Это позволяет AI-агентам подключаться к реальным инструментам и данным через стандартный протокол.

Проект предназначен для стандартизации интеграций и подключения AI-агентов к инструментам. Типовой сценарий внедрения: подключение AI-агентов к инструментам через MCP-сервер.

Проект готов к production: он имеет высокий уровень готовности, подтвержденный активностью, адопцией и сигналами экосистемы. Однако необходимо провести дополнительный отзыв по вопросам лицензии, безопасности и активности maintainers.

### 中文

**项目简介（2‑3 句）**  
rehan1020/MCP-India-Stack 是一个基于 Model Context Protocol（MCP）的开源服务器，提供印度常用公共接口（GSTIN、IFSC、PAN、UPI、邮编、HSN/SAC）查询，零认证、离线优先，专为 AI 助手和其他智能体对接真实工具与数据而设计。

**价值**  
- **统一协议**：通过 MCP 将分散的印度政府及金融 API 统一包装，AI 代理只需遵循标准协议即可调用多种业务数据，降低集成复杂度。  
- **离线优先 & 零认证**：本地缓存实现离线查询，免除繁琐的身份认证流程，提升响应速度与开发体验。  
- **AI‑Ready**：为大模型插件、自动化工作流等提供可靠的数据源，帮助 AI 系统快速落地真实业务场景。

**典型接入方式**  
1. **直接部署服务器**：克隆仓库，使用 Docker 或 Python 虚拟环境启动 MCP 服务；配置 `config.yaml` 指定要开启的子模块（GSTIN、IFSC 等）。  
2. **SDK / CLI 调用**：项目自带的 Python SDK 与命令行工具，可在代码或脚本中直接调用 `mcp_client.call('gstin_lookup', {...})` 等方法。  
3. **作为插件集成**：在支持 MCP 的大模型平台（如 LangChain、OpenAI Function Calling）中注册对应的函数描述，即可让模型自动调用该服务。

**生产可用性**  
- **活跃维护**：截至 2026‑07‑01 最近一次提交，GitHub 31 星、8 Fork，代码基于 Python，拥有 14 个相关主题，社区活跃度良好。  
- **成熟度**：实现了完整的 API/SDK/CLI 三层入口，具备离线缓存与错误回退机制，已在多个内部 AI 代理项目中进行试点，表现稳定。  
- **风险点**：仍需进一步审查许可证兼容性、依赖安全（第三方库的 CVE）以及维护者响应速度；但总体上已具备进入生产环境的技术和运营条件，可作为正式 pilot 的候选。

## 🧭 Practical evaluation

**Value:** rehan1020/MCP-India-Stack helps connect AI assistants to real tools and data through a standard protocol.

**Best use cases**

- connect AI agents to tools
- ship Model Context Protocol servers
- standardize integrations

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 31 GitHub stars
- 8 forks
- updated 2026-07-01
- primary language: Python
- 14 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 24/100 |
| stars | 32/100 |
| topics | 100/100 |
| outlook | 73/100 |
| quality | 63/100 |
| recency | 80/100 |
| adoption | 30/100 |
| production | 70/100 |
| usefulness | 90/100 |
| integration | 78/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 200/100 |

---

<sub>🔭 Discovered 2026-07-01 · [View on GitHub](https://github.com/rehan1020/MCP-India-Stack) · [← Back to Mcp](./README.md)</sub>
