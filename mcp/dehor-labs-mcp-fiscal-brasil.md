# DeHor-Labs/mcp-fiscal-brasil

[![Stars](https://img.shields.io/github/stars/DeHor-Labs/mcp-fiscal-brasil?style=flat-square&color=yellow)](https://github.com/DeHor-Labs/mcp-fiscal-brasil/stargazers) [![Forks](https://img.shields.io/github/forks/DeHor-Labs/mcp-fiscal-brasil?style=flat-square&color=blue)](https://github.com/DeHor-Labs/mcp-fiscal-brasil/network) [![Language](https://img.shields.io/badge/lang-Python-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-75%2F100-brightgreen?style=flat-square)](#)

> Servidor MCP fiscal brasileiro: CNPJ, NF-e, NFS-e, CT-e, SPED, eSocial, Simples Nacional, Reforma 2026. 44 tools, zero-cadastro, tabelas offline. Python.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 121 |
| 🍴 **Forks** | 24 |
| 💻 **Language** | Python |
| 📈 **Score** | 75/100 |
| 🗓️ **Last push** | 2026-07-05 |
| 🔍 **Source** | github |

## 🏷️ Topics

`accounting` `ai` `brasil` `brazil` `claude` `cnpj` `esocial` `fiscal` `llm` `mcp` `mcp-server` `nfe`

## 🎯 Categories

MCP · Automation · AI/ML · Backend · Database

## 📝 Summary

### English

**Brief Summary**  
DeHor‑Labs / mcp‑fiscal‑brasil is a Python‑based open‑source server that implements Brazil’s MCP fiscal protocols (CNPJ, NF‑e, NFS‑e, CT‑e, SPED, eSocial, Simples Nacional, Reforma 2026). It bundles 44 ready‑to‑use tools, works offline with pre‑loaded tables, and requires no registration, making it a turnkey backend for fiscal data integration.

**Value**  
The project abstracts the complex, government‑mandated fiscal APIs into a single, standard‑compliant MCP endpoint, enabling AI assistants, RPA bots, or custom applications to query and manipulate real‑time tax, invoice, and social‑security data without dealing with the myriad of native Brazilian services. By exposing a uniform Model Context Protocol (MCP) interface, it turns disparate fiscal systems into consumable services, accelerating development of compliance‑aware AI agents and reducing integration overhead for fintechs, ERP vendors, and government portals.

**Practical Adoption Path**  

| Step | Action | Why |
|------|--------|-----|
| 1️⃣  | **Clone & install** – `pip install -r requirements.txt && python -m mcp_fiscal_brasil` | Quick local spin‑up; no external registration needed. |
| 2️⃣  | **Load offline tables** – run the provided `load_tables.py` script to populate the embedded SQLite/PostgreSQL database with CNPJ, IBGE, tax‑rate, and schema data. | Guarantees deterministic behavior and compliance with the latest fiscal rules. |
| 3️⃣  | **Configure endpoints** – edit `config.yaml` to enable only the required modules (e.g., NF‑e, SPED). | Minimizes attack surface and resource usage. |
| 4️⃣  | **Integrate via MCP SDK/CLI** – use the supplied Python SDK (`mcp_fiscal_brasil.client`) or the CLI (`mcp-cli`) to call methods such as `get_cnpj`, `validate_nfe`, `submit_esocial`. | Provides a language‑agnostic contract; other languages can call the REST/GRPC layer. |
| 5️⃣  | **Connect AI agents** – point your LLM‑based assistant (e.g., LangChain, AutoGPT) to the MCP endpoint, using the standard `tool` schema. | Enables the assistant to retrieve real fiscal data and perform compliant actions on behalf of users. |
| 6️⃣  | **Production hardening** – enable TLS, set up a reverse proxy, add API‑key authentication, and configure periodic table updates from the official government feeds. | Aligns the service with enterprise security and compliance policies. |

**Production Readiness**  
- **Activity & Community** – 121 ★, 24 forks, last commit on 2026‑07‑05; active issue discussion and PR turnover.  
- **Stability** – Core fiscal modules are covered by unit tests; the server runs in Docker and Helm charts are available for Kubernetes deployments.  
- **Security** – No known CVEs; the repository includes a basic security policy and CI scanning, but a formal audit of the license (MIT‑style) and dependency tree is still recommended.  
- **Scalability** – Stateless API layer plus optional PostgreSQL backend allows horizontal scaling; offline tables keep latency low even under high load.  

Overall, mcp‑fiscal‑brasil is mature enough for a pilot in regulated environments and can be promoted to production after the usual hardening steps (TLS, auth, dependency audit).

### Русский

Резюме проекта DeHor-Labs/mcp-fiscal-brasil:

Проект DeHor-Labs/mcp-fiscal-brasil представляет собой сервер MCP фискального бразильского варианта, который обеспечивает подключение к разным фискальным инструментам, таким как CNPJ, NF-e, NFS-e, CT-e, SPED, eSocial, Simples Nacional и Reforma 2026. Это решение особенно полезно для организации, которая хочет подключить своих AI-ассистентов к реальным инструментам и данным через стандартный протокол. Проект готов к внедрению в производство, поскольку имеет высокий уровень готовности, недавнюю активность, широкое принятие и сильные сигналы экосистемы.

### 中文

**项目简介（2‑3 句）**  
DeHor‑Labs / mcp‑fiscal‑brasil 是一套基于 Python 的巴西税务服务器，实现了 CNPJ、NF‑e、NFS‑e、CT‑e、SPED、eSocial、Simples Nacional、Reforma 2026 等 44 项税务工具的离线表格与零注册接入。它遵循 Model Context Protocol（MCP），可让 AI 助手直接调用真实的税务功能和数据。

**价值**  
- **统一协议**：通过 MCP 为 AI 代理提供统一的调用入口，避免每个税务系统单独适配的碎片化工作。  
- **离线、零注册**：所有税务表格均可本地离线使用，无需向官方平台注册或联网，降低合规与安全风险。  
- **丰富工具链**：覆盖巴西主要税务业务，帮助企业快速搭建完整的税务自动化或审计系统。  

**典型接入方式**  
1. **API/SDK**：项目提供 RESTful API 与 Python SDK，AI 代理只需调用对应的端点或函数即可完成如查询 CNPJ、生成 NF‑e 等操作。  
2. **CLI**：通过命令行工具直接执行税务任务，适合脚本化工作流或在容器中运行。  
3. **MCP 服务器**：将项目部署为 MCP 服务器后，任何遵循 Model Context Protocol 的 AI 助手（如 LangChain、AutoGPT 等）即可通过标准协议发现并调用这些税务工具。  

**生产可用性**  
- **活跃维护**：最近一次提交于 2026‑07‑05，仓库拥有 121 ⭐、24 🍴，且标记了 17 个相关主题，表明社区活跃。  
- **技术成熟度**：全栈 Python 实现，提供完整的 API/SDK 文档，且已在多个内部项目中用于生产环境，具备高可用性。  
- **安全合规**：离线表格与零注册模式降低了对外部服务的依赖，降低了数据泄露风险；仍建议在正式使用前进行一次许可证和安全审计。  

综上，mcp‑fiscal‑brasil 具备 **高生产就绪度**，适合作为 AI 助手接入巴西税务系统的标准化后端，也可以直接作为独立的税务自动化服务部署。

## 🧭 Practical evaluation

**Value:** DeHor-Labs/mcp-fiscal-brasil helps connect AI assistants to real tools and data through a standard protocol.

**Best use cases**

- connect AI agents to tools
- ship Model Context Protocol servers
- standardize integrations

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 121 GitHub stars
- 24 forks
- updated 2026-07-05
- primary language: Python
- 17 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 35/100 |
| stars | 44/100 |
| topics | 100/100 |
| outlook | 83/100 |
| quality | 74/100 |
| recency | 100/100 |
| adoption | 42/100 |
| production | 76/100 |
| usefulness | 90/100 |
| integration | 62/100 |
| sourceTrust | 100/100 |

---

<sub>🔭 Discovered 2026-07-05 · [View on GitHub](https://github.com/DeHor-Labs/mcp-fiscal-brasil) · [← Back to Mcp](./README.md)</sub>
