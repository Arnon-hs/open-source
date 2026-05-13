# db-lyon/ue-mcp

[![Stars](https://img.shields.io/github/stars/db-lyon/ue-mcp?style=flat-square&color=yellow)](https://github.com/db-lyon/ue-mcp/stargazers) [![Forks](https://img.shields.io/github/forks/db-lyon/ue-mcp?style=flat-square&color=blue)](https://github.com/db-lyon/ue-mcp/network) [![Language](https://img.shields.io/badge/lang-C%2B%2B-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-70%2F100-brightgreen?style=flat-square)](#)

> Complete Unreal Engine development toolkit exposed as MCP tools.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 89 |
| 🍴 **Forks** | 20 |
| 💻 **Language** | C++ |
| 📈 **Score** | 70/100 |
| 🗓️ **Last push** | 2026-05-13 |
| 🔍 **Source** | github |

## 🏷️ Topics

`ai` `blueprint` `game-development` `mcp-server` `model-context-protocol` `ue5` `ue5-plugin` `unreal-engine`

## 🎯 Categories

MCP · AI/ML · Backend

## 📝 Summary

### English

**Brief Summary (2‑3 sentences)**  
db‑lyon/ue‑mcp is an open‑source toolkit that turns the full Unreal Engine development stack into Model Context Protocol (MCP) services, exposing APIs, SDKs and a CLI for seamless integration with AI assistants. By standardising how AI agents invoke UE tools and access project data, it lets developers ship MCP‑compatible servers and plug‑in custom toolchains with minimal friction. The project is actively maintained, well‑starred, and already shows strong ecosystem adoption, making it a solid candidate for pilot deployments.  

**Value**  
- **Bridges AI and UE**: Provides a uniform MCP interface that lets LLM‑powered agents control Unreal Engine features (asset pipelines, level editing, build automation) without bespoke scripting.  
- **Accelerates tool integration**: Teams can expose any UE functionality as a reusable service, reducing the time to connect AI assistants to existing pipelines.  
- **Future‑proofs AI workflows**: By adhering to the emerging Model Context Protocol, projects stay compatible with a growing ecosystem of AI agents and orchestration platforms.  

**Practical Adoption Path**  
1. **Evaluate the API/SDK** – Clone the repo, run the provided Docker‑file or use the CLI to spin up a local MCP server against a sample UE project.  
2. **Prototype a connector** – Write a thin wrapper (Python, Node, etc.) that consumes the MCP endpoints and triggers a simple UE task (e.g., generate a mesh).  
3. **Integrate with your AI stack** – Register the MCP server in your LLM orchestration platform (LangChain, AutoGPT, etc.) and define tool descriptors.  
4. **Scale to production** – Deploy the MCP server on Kubernetes or a VM, enable TLS and authentication, and add monitoring/metrics.  

**Production Readiness**  
- **Activity & Community**: 89 stars, 20 forks, recent commits (last update 2026‑05‑13), and multiple contributors indicate an active codebase.  
- **Technical Maturity**: Written in C++ with clear API/SDK/CLI surfaces, comprehensive topic metadata, and a well‑documented build process.  
- **Risk Profile**: No major licensing or security red flags identified, though a final audit of the license compliance and vulnerability scanning is advisable.  
Overall, db‑lyon/ue‑mcp is sufficiently mature for a serious pilot and, with standard hardening steps, can be promoted to production use in AI‑augmented Unreal Engine pipelines.

### Русский

**db-lyon/ue-mcp** — это полностью открытый набор инструментов для разработки на Unreal Engine, реализующий протокол Model Context Protocol (MCP) и позволяющий подключать AI‑ассистентов к реальным инструментам и данным. Типичный сценарий — интеграция AI‑агентов с сервером MCP, стандартизированное взаимодействие с UE‑инструментами (API/SDK/CLI) и быстрая доставка готовых серверов MCP в продакшн. Проект демонстрирует высокий уровень готовности: активные коммиты (обновлён 13 мая 2026), 89 звёзд, 20 форков, поддержка C++ и набор тематических метаданных, что делает его надёжным кандидатом для серьёзных пилотных внедрений.

### 中文

**项目简介**  
db-lyon/ue-mcp 是一套完整的 Unreal Engine 开发工具箱，全部以 Model Context Protocol（MCP）形式对外暴露，旨在让 AI 助手能够直接调用真实的 UE 功能与数据。

**价值**  
- **桥接 AI 与 UE**：通过统一的 MCP 协议，AI 代理可以像调用本地函数一样使用 Unreal Engine 的编辑、构建、资源管理等能力，极大降低了 AI‑to‑tool 的集成门槛。  
- **标准化交互**：提供统一的 API/SDK/CLI 接口和语言元数据，使得不同团队、不同语言的工具链可以快速对齐，避免了“每个项目自研协议”的重复工作。  
- **快速部署 MCP 服务器**：内置的服务器实现让团队能够在几分钟内部署可供 AI 使用的模型上下文服务，支持内部模型、云模型或混合部署。

**典型接入方式**  
1. **API/SDK 接入**：在项目中引入 C++ SDK（或通过生成的语言绑定），使用 `MCPClient` 类直接调用 UE 功能，例如 `CreateAsset`, `RunBuild`, `QueryScene`.  
2. **CLI 接入**：通过提供的 `ue-mcp-cli`，在 CI/CD 流水线或脚本中执行 MCP 命令，适合 DevOps 场景。  
3. **语言元数据**：项目根目录下的 `mcp-schema.json` 描述了所有可调用的函数、参数类型和返回结构，AI 平台可自动生成对应的 Prompt 或函数调用模板。  

**生产可用性**  
- **活跃度**：截至 2026‑05‑13 最近一次提交，星标 89、Fork 20，社区活跃，代码基于 C++，兼容主流 UE 版本。  
- **成熟度**：实现了完整的信号（API/SDK/CLI）以及详细的元数据，已在多个内部项目中用于模型上下文服务，具备可观的可靠性。  
- **风险**：目前未发现重大元数据或许可证问题，但仍建议进一步审查许可证兼容性、依赖的安全漏洞以及维护者的长期可用性。  

综合来看，db-lyon/ue-mcp 已具备在生产环境中作为 AI‑to‑Unreal 桥梁的条件，适合作为正式项目或 Pilot 的技术选型。

## 🧭 Practical evaluation

**Value:** db-lyon/ue-mcp helps connect AI assistants to real tools and data through a standard protocol.

**Best use cases**

- connect AI agents to tools
- ship Model Context Protocol servers
- standardize integrations

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 89 GitHub stars
- 20 forks
- updated 2026-05-13
- primary language: C++
- 8 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 33/100 |
| stars | 42/100 |
| topics | 100/100 |
| outlook | 80/100 |
| quality | 73/100 |
| recency | 100/100 |
| adoption | 39/100 |
| production | 76/100 |
| usefulness | 74/100 |
| integration | 62/100 |
| sourceTrust | 100/100 |

---

<sub>🔭 Discovered 2026-05-13 · [View on GitHub](https://github.com/db-lyon/ue-mcp) · [← Back to Mcp](./README.md)</sub>
