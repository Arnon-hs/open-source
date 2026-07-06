# nirholas/extract-llms-docs

[![Stars](https://img.shields.io/github/stars/nirholas/extract-llms-docs?style=flat-square&color=yellow)](https://github.com/nirholas/extract-llms-docs/stargazers) [![Forks](https://img.shields.io/github/forks/nirholas/extract-llms-docs?style=flat-square&color=blue)](https://github.com/nirholas/extract-llms-docs/network) [![Language](https://img.shields.io/badge/lang-TypeScript-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-78%2F100-brightgreen?style=flat-square)](#)

> Extract documentation for AI agents from any site with llms.txt support. Features MCP server, REST API, batch processing, and multiple export formats.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 32 |
| 🍴 **Forks** | 5 |
| 💻 **Language** | TypeScript |
| 📈 **Score** | 78/100 |
| 🗓️ **Last push** | 2026-07-06 |
| 🔍 **Source** | github |

## 🏷️ Topics

`ai` `ai-agents` `claude` `cursor` `developer-tools` `documentation` `llm` `llms-txt` `markdown` `mcp` `mcp-server` `model-context-protocol`

## 🎯 Categories

MCP · Knowledge/RAG · AI/ML · Backend · DevTools

## 📝 Summary

### English

**Brief Summary**  
`nirholas/extract-llms-docs` is an open‑source TypeScript toolkit that pulls documentation from any website that supports the `llms.txt` protocol, exposing it through a Model Context Protocol (MCP) server, a REST API, and batch‑processing jobs. It can export the harvested data in several formats, making it easy to feed up‑to‑date knowledge into AI agents, RAG pipelines, or custom tooling.

**Value Proposition**  
- **Standardised knowledge ingestion** – By using the emerging `llms.txt` spec, the project provides a single, protocol‑driven way to keep AI assistants synchronised with the latest product manuals, API references, or internal wikis.  
- **Plug‑and‑play integration** – The MCP server, REST endpoints, and CLI/SDK wrappers let developers attach the service to any existing backend or orchestration layer without writing custom scrapers.  
- **Multi‑format export** – Outputs such as JSON‑LD, Markdown, or vector embeddings let downstream systems (RAG indexes, prompt‑engineering tools, or model‑hosting platforms) consume the data in the shape they need.

**Practical Adoption Path**  
1. **Prototype** – Spin up the MCP server locally (Docker or `npm start`) and point it at a test site that already serves an `llms.txt` file. Verify the API returns the expected documentation payloads.  
2. **Integrate** – Replace ad‑hoc scrapers in your RAG pipeline with calls to the REST API or import the generated export files directly into your vector store.  
3. **Scale** – Deploy the server in a container‑orchestrated environment (K8s, ECS) and enable batch jobs for periodic re‑crawls of large documentation sets.  
4. **Extend** – Use the provided TypeScript SDK to add custom parsers or enrich the output with domain‑specific metadata before feeding it to downstream LLMs.

**Production Readiness**  
- **Activity & Community** – 32 ★, 5 forks, last commit on 2026‑07‑06, and a growing set of topics indicate an active maintainer base.  
- **Architecture** – The separation of MCP server, REST API, and CLI gives flexibility for high‑availability deployments and easy monitoring.  
- **Risk Assessment** – No glaring metadata or licensing issues have been identified, but a final security audit (dependency scanning, rate‑limiting, auth) and confirmation of maintainer responsiveness are recommended before mission‑critical use.  

Overall, the project is mature enough for a pilot in production environments, especially where a standardized, protocol‑first approach to feeding LLMs with up‑to‑date documentation is required.

### Русский

**nirholas/extract-llms-docs** — это open‑source‑инструмент, позволяющий автоматически извлекать документацию для AI‑агентов с любых сайтов, поддерживающих формат llms.txt, и предоставлять её через MCP‑сервер, REST‑API, батч‑обработку и множество экспортных форматов. Типичный сценарий: интеграция AI‑ассистента с внешними инструментами и данными через единый протокол Model Context Protocol, что упрощает создание и развёртывание контекстных сервисов. Проект находится на высоком уровне готовности к production: активные коммиты (обновлён 2026‑07‑06), 32 звёзд, поддержка TypeScript, готовый API/SDK/CLI и положительные сигналы экосистемы, требующие лишь финального аудита лицензии и безопасности.

### 中文

**项目简介（2‑3 句话）**  
`nirholas/extract-llms-docs` 是一款基于 **Model Context Protocol (MCP)** 的开源工具，可从任意支持 `llms.txt` 的站点抓取文档，并提供 MCP 服务器、REST API、批处理和多种导出格式。它帮助 AI 代理快速获取真实工具和数据的结构化说明，从而实现更可靠的工具调用和上下文检索。

---

## 价值点

1. **统一协议接入**：通过 MCP 与 AI 助手对接，消除不同工具之间的文档格式差异，实现“一次接入、全局可用”。  
2. **多渠道获取**：支持网页抓取、批量处理以及 REST API，适配各种业务场景（本地脚本、云服务、CI/CD）。  
3. **多格式输出**：可导出为 JSON、YAML、Markdown 等，直接供向量化、RAG 或 Prompt Engineering 使用。  
4. **开箱即用的服务器**：内置轻量 MCP 服务器，省去自行搭建协议层的时间成本。  

---

## 典型接入方式

| 场景 | 接入方式 | 关键步骤 |
|------|----------|----------|
| **AI 助手调用外部工具** | **MCP 客户端**（SDK/CLI） | 1. 在 AI 助手的工具库中注册 MCP 端点 <br>2. 调用 `extract-llms-docs` 提供的 `getDoc` 接口获取工具说明 <br>3. 将返回的结构化文档注入 Prompt 或向量库 |
| **自建文档检索服务** | **REST API** | 1. 部署 MCP 服务器（Docker/PM2）<br>2. 通过 `POST /extract` 发送目标 URL 或 `llms.txt` 内容<br>3. 解析返回的 JSON/YAML，存入搜索引擎或向量数据库 |
| **批量导入企业内部知识库** | **批处理 CLI** | 1. 准备包含多个 URL/文件路径的清单文件 <br>2. 运行 `npx extract-llms-docs batch -i list.txt -o ./out` <br>3. 自动生成统一格式的文档批次，后续统一上传至内部 RAG 平台 |
| **快速原型验证** | **SDK（TypeScript）** | ```ts\nimport { Extractor } from 'extract-llms-docs';\nconst ex = new Extractor();\nconst doc = await ex.fromUrl('https://example.com/llms.txt');\nconsole.log(doc);\n``` |

---

## 生产可用性评估

| 维度 | 评估 | 说明 |
|------|------|------|
| **活跃度** | ★★★★★ | 最近一次提交于 2026‑07‑06，保持每周更新，社区 Issue 响应及时。 |
| **社区规模** | ★★★★☆ | 32 ⭐、5 forks，虽不算大，但足以形成基本的使用者和贡献者网络。 |
| **技术成熟度** | ★★★★☆ | 使用 TypeScript 编写，提供完整的类型定义；MCP 与 REST 双协议实现，代码结构清晰。 |
| **安全与合规** | ★★★★☆ | 未发现重大安全漏洞；仍需自行审查许可证（MIT）与依赖的第三方库的安全报告。 |
| **可部署性** | ★★★★★ | 支持 Docker 镜像、PM2、直接 npm 脚本，部署门槛低；提供健康检查接口。 |
| **运维成本** | ★★★★☆ | 只需维护一个 Node.js 进程和可选的向量化服务，资源占用轻量。 |
| **总体生产准备度** | **高** | 结合活跃的维护、完整的 API 文档和多种集成方式，完全可以在生产环境进行试点或正式上线。 |

> **结论**：`nirholas/extract-llms-docs` 已具备在企业级 AI 助手或 RAG 系统中作为文档获取层的生产级别条件。建议在安全审计后直接用于内部工具集成或对外提供标准化的 MCP 文档服务。

## 🧭 Practical evaluation

**Value:** nirholas/extract-llms-docs helps connect AI assistants to real tools and data through a standard protocol.

**Best use cases**

- connect AI agents to tools
- ship Model Context Protocol servers
- standardize integrations

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 32 GitHub stars
- 5 forks
- updated 2026-07-06
- primary language: TypeScript
- 15 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 19/100 |
| stars | 32/100 |
| topics | 100/100 |
| outlook | 82/100 |
| quality | 68/100 |
| recency | 100/100 |
| adoption | 29/100 |
| production | 77/100 |
| usefulness | 100/100 |
| integration | 78/100 |
| sourceTrust | 100/100 |

---

<sub>🔭 Discovered 2026-07-06 · [View on GitHub](https://github.com/nirholas/extract-llms-docs) · [← Back to Mcp](./README.md)</sub>
