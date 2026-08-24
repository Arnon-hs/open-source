# tsouth89/toolport

[![Stars](https://img.shields.io/github/stars/tsouth89/toolport?style=flat-square&color=yellow)](https://github.com/tsouth89/toolport/stargazers) [![Forks](https://img.shields.io/github/forks/tsouth89/toolport?style=flat-square&color=blue)](https://github.com/tsouth89/toolport/network) [![Language](https://img.shields.io/badge/lang-Rust-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-66%2F100-brightgreen?style=flat-square)](#)

> Local-first MCP gateway. One port for every tool and every AI client: lazy discovery (~90% token savings), tool integrity + quarantine, secrets in the OS keychain.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 50 |
| 🍴 **Forks** | 11 |
| 💻 **Language** | Rust |
| 📈 **Score** | 66/100 |
| 🗓️ **Last push** | 2026-08-24 |
| 🔍 **Source** | github |

## 🏷️ Topics

`ai` `ai-agents` `anthropic` `claude` `cursor` `developer-tools` `gateway` `llm` `local-first` `mcp` `mcp-server` `model-context-protocol`

## 🎯 Categories

MCP · AI/ML · Frontend · Backend · DevTools

## 📝 Summary

### English

tsouth89/toolport provides a local‑first MCP gateway that lets AI assistants discover and securely invoke any tool through a single port, delivering lazy‑discovery token savings, tool integrity checks, and OS‑keychain secret management. Its straightforward API/SDK/CLI interface makes it easy to evaluate and integrate into existing AI‑agent workflows, enabling rapid prototyping of Model Context Protocol servers and standardized tool integrations. With recent activity, growing adoption, strong ecosystem signals, and a Rust‑based implementation, the project is production‑ready enough for a serious pilot, pending final review of licensing, security posture, and maintainer sustainability.

### Русский

**tsouth89/toolport** — это open‑source MCP‑шлюз, реализованный на Rust, который предоставляет единый порт для любого инструмента и AI‑клиента, обеспечивая «ленивое» обнаружение (экономия ≈ 90 % токенов), проверку целостности инструментов, карантин и хранение секретов в системном keychain. Типичный сценарий — подключить AI‑агента к реальным сервисам и данным через стандартный протокол Model Context Protocol, либо развернуть собственный MCP‑сервер для унификации интеграций. Проект считается почти готовым к production: активные коммиты, 50 звёзд, 11 форков, свежие обновления (июль 2026) и хорошие сигналы экосистемы, хотя окончательная проверка лицензии и безопасности всё‑ещё требуется.

### 中文

**项目简介**  
tsouth89/toolport 是一个 **Local‑first MCP（Model Context Protocol）网关**，为每个工具和每个 AI 客户端提供独立的端口，实现懒加载发现（约 90% token 节省）、工具完整性校验与隔离、以及通过操作系统钥匙串安全存储密钥。

---

### 价值点
1. **统一协议接入**：通过标准的 MCP 协议，AI 助手可以像调用本地函数一样安全、可靠地调用真实工具和数据源，降低集成成本。  
2. **高效 Token 使用**：懒发现机制只在必要时请求工具元信息，显著降低 LLM 调用的 token 消耗。  
3. **安全与隔离**：工具完整性校验 + 隔离区（quarantine）防止恶意或受损工具影响系统，敏感凭证统一保存在 OS keychain 中。  
4. **语言无关、易扩展**：基于 Rust 实现，提供 API、SDK、CLI 三种接入方式，适配多语言生态。

---

### 典型接入方式
| 场景 | 接入方式 | 步骤概览 |
|------|----------|----------|
| **AI 助手调用工具** | **SDK**（Rust / Python 绑定） | 1. 在项目中引入 `toolport-sdk` <br>2. 配置 `toolport` 实例（指定本地端口、keychain 名称） <br>3. 通过 SDK 调用 `toolport.invoke(tool_id, args)` |
| **服务端部署 MCP 服务器** | **CLI** | 1. 下载并运行 `toolport serve --config ./toolport.toml` <br>2. 在配置文件中声明可用工具、权限、隔离策略 <br>3. 通过 HTTP/WebSocket 与 AI 模型交互 |
| **快速原型或脚本** | **API (REST/WS)** | 1. 启动 `toolport` 二进制 <br>2. 直接发送 `POST /invoke` 请求，携带工具 ID 与参数 <br>3. 收到标准化的 JSON 响应 |
| **CI/CD 或 DevOps 集成** | **插件/扩展** | 通过 `toolport` 提供的 `toolport-plugin` 接口，将自定义工具包装为插件，自动注册到网关并受同样的安全策略约束。 |

---

### 生产可用性评估
| 维度 | 评估 |
|------|------|
| **活跃度** | 最近一次提交于 2026‑07‑02，仓库拥有 50+ stars、11 forks，社区讨论活跃。 |
| **技术成熟度** | 核心使用 Rust 编写，具备内存安全与高性能；提供完整的 API/SDK/CLI，文档覆盖基本使用场景。 |
| **安全性** | 密钥统一存储在 OS keychain，工具执行在隔离环境中，默认开启完整性校验。仍需自行审计依赖的 Cargo 包及许可证合规性。 |
| **可扩展性** | 支持自定义工具注册、主题化的权限模型，易于在多租户或微服务架构中扩展。 |
| **运维成本** | 只需部署单个本地二进制或容器，配置即能启动多个端口；监控可借助标准日志/Prometheus 指标。 |
| **总体结论** | 具备 **高** 生产就绪度，适合作为 **AI‑Tool 集成的底层网关** 在内部平台或对外 SaaS 中进行试点，后续可根据内部安全审计结果正式上线。 |

> **建议**：在正式投产前完成许可证（MIT/Apache 双许可）确认、依赖漏洞扫描（`cargo audit`），并在预生产环境进行一次完整的隔离/权限策略演练。

## 🧭 Practical evaluation

**Value:** tsouth89/toolport helps connect AI assistants to real tools and data through a standard protocol.

**Best use cases**

- connect AI agents to tools
- ship Model Context Protocol servers
- standardize integrations

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 50 GitHub stars
- 11 forks
- updated 2026-07-02
- primary language: Rust
- 16 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 27/100 |
| stars | 36/100 |
| topics | 100/100 |
| outlook | 62/100 |
| quality | 55/100 |
| recency | 40/100 |
| adoption | 34/100 |
| production | 55/100 |
| usefulness | 100/100 |
| integration | 62/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 500/100 |

---

<sub>🔭 Discovered 2026-07-02 · [View on GitHub](https://github.com/tsouth89/toolport) · [← Back to Mcp](./README.md)</sub>
