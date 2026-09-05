# franzvill/lad

[![Stars](https://img.shields.io/github/stars/franzvill/lad?style=flat-square&color=yellow)](https://github.com/franzvill/lad/stargazers) [![Forks](https://img.shields.io/github/forks/franzvill/lad?style=flat-square&color=blue)](https://github.com/franzvill/lad/network) [![Language](https://img.shields.io/badge/lang-Python-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-65%2F100-brightgreen?style=flat-square)](#)

> An open protocol for discovering A2A-capable AI agents on local networks — the discovery & trust bootstrap layer beneath A2A (mDNS/DNS-SD, well-known endpoints, signed AgentCards).

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 77 |
| 🍴 **Forks** | 2 |
| 💻 **Language** | Python |
| 📈 **Score** | 65/100 |
| 🗓️ **Last push** | 2026-09-05 |
| 🔍 **Source** | github |

## 🏷️ Topics

`a2a` `agent-discovery` `ai-agents` `dns-sd` `mcp` `mdns` `protocol` `protocol-specification` `service-discovery` `zeroconf`

## 🎯 Categories

MCP · AI/ML

## 📝 Summary

### English

**Brief Summary (2‑3 sentences)**  
franzvill/lad is an open‑source protocol that lets AI agents discover and trust one another on a local network using mDNS/DNS‑SD, well‑known endpoints, and signed AgentCards. It provides the bootstrap layer for A2A (agent‑to‑agent) communication, enabling assistants to locate and securely interact with tools, services, and data sources without custom wiring.

**Value**  
- **Standardised discovery** – eliminates ad‑hoc networking code; any A2A‑capable agent can find peers automatically.  
- **Built‑in trust** – signed AgentCards give a verifiable identity, reducing the risk of rogue agents.  
- **Tool integration** – once discovered, agents can invoke real‑world tools (databases, APIs, CLIs) through a common handshake, accelerating the “AI‑assistant‑as‑tool” use case.

**Practical Adoption Path**  
1. **Prototype** – add the Python SDK/CLI to an existing AI assistant and run the bundled discovery service on a dev machine or Docker container.  
2. **Integrate** – expose your tool or service as a “Model Context Protocol” server and register its AgentCard with lad; the assistant will auto‑discover it via mDNS.  
3. **Validate trust** – configure your CA or public‑key store for AgentCard signatures; test end‑to‑end calls in a sandbox.  
4. **Scale** – deploy lad agents on each host (or as side‑car containers) in your internal network; use the well‑known endpoint fallback for environments where mDNS is blocked.  

**Production Readiness**  
- **Maturity:** Medium. The codebase is recent (last update 2026‑07‑01), well‑documented, and has modest community interest (77 ★, 2 forks).  
- **Dependencies:** Pure‑Python with a small set of networking libs; easy to audit.  
- **Risks:** License and long‑term maintainer commitment still need verification; security review of the signing workflow is recommended before exposing it to external networks.  
- **Fit:** Ideal for internal prototypes, sandbox environments, or early‑stage services that need a reliable discovery layer before committing to a full production‑grade service mesh. With a short hardening sprint (license check, security audit, CI/CD integration) it can be promoted to production use.

### Русский

franzvill/lad — это открытый протокол, позволяющий автоматически обнаруживать и доверительно подключать AI‑агенты, способные к A2A‑взаимодействию, в локальной сети (mDNS/DNS‑SD, известные эндпоинты, подписанные AgentCards). Типичный сценарий — интеграция ассистентов с реальными инструментами и данными: разработчики могут быстро подключать свои модели к сервисам через стандартный bootstrap‑слой, а компании — развертывать серверы Model Context Protocol и унифицировать интеграции. Проект находится на среднем уровне готовности: подходит для прототипов и внутренних workflow, но перед запуском в продакшен следует проверить лицензирование, безопасность и активность поддержки.

### 中文

**简短介绍**  
franzvill/lad 是一个开源的发现与信任引导层协议，基于 mDNS/DNS‑SD、固定端点和签名的 AgentCard，帮助在局域网内快速定位并验证具备 A2A 能力的 AI 代理。它为 AI 助手与真实工具、数据源的连接提供统一的标准化入口。

**价值**  
- **统一发现**：通过零配置的局域网广播或已知 URL，自动发现网络中的 AI 代理，省去手动配置和硬编码。  
- **安全信任**：AgentCard 使用签名机制，确保发现的代理身份可验证，降低中间人或伪造代理的风险。  
- **生态互通**：为不同厂商、不同语言实现的 AI 助手提供统一的接入点，促进工具、模型及上下文协议的互操作。

**典型接入方式**  
1. **SDK / API**：在 Python 项目中引入 `lad` 包，调用 `discover_agents()` 获取本地可用的 AgentCard 列表；随后使用返回的端点直接发起 A2A 调用。  
2. **CLI**：通过 `lad-cli discover` 命令行工具快速列出网络中的代理，适合调试或脚本化集成。  
3. **服务端实现**：在需要提供 AgentCard 的服务（如 Model Context Protocol 服务器）中使用 `lad.server` 模块注册自己的端点并签名卡片，即可被其他客户端自动发现。

**生产可用性**  
- **成熟度**：当前评分 68/100，代码活跃（截至 2026‑07‑01），拥有 77 星、10+ 话题标签，适合作为原型或内部工作流的基础设施。  
- **依赖与维护**：主要语言为 Python，依赖相对轻量；但项目维护者数量有限，建议在生产环境前进行以下检查：  
  - 代码审计（尤其是签名/验证实现）  
  - 兼容性测试（不同 OS、网络环境）  
  - 监控与日志方案，以捕获发现失败或安全异常  
- **部署建议**：在内部网络中先做灰度部署，结合自研的健康检查服务；如需对外暴露，可在边界网关上加固 TLS 并限制 AgentCard 的签名密钥管理。  

综上，franzvill/lad 为 AI‑to‑AI 场景提供了可靠的发现与信任层，适合快速搭建原型并在经过安全与运维评估后逐步推向生产。

## 🧭 Practical evaluation

**Value:** franzvill/lad helps connect AI assistants to real tools and data through a standard protocol.

**Best use cases**

- connect AI agents to tools
- ship Model Context Protocol servers
- standardize integrations

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** Medium: useful for prototypes or internal workflows, with dependency and maintenance checks before production.

**Quality signals**

- 77 GitHub stars
- 2 forks
- updated 2026-07-01
- primary language: Python
- 10 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 12/100 |
| stars | 40/100 |
| topics | 100/100 |
| outlook | 71/100 |
| quality | 65/100 |
| recency | 80/100 |
| adoption | 32/100 |
| production | 68/100 |
| usefulness | 74/100 |
| integration | 62/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 200/100 |

---

<sub>🔭 Discovered 2026-07-01 · [View on GitHub](https://github.com/franzvill/lad) · [← Back to Mcp](./README.md)</sub>
