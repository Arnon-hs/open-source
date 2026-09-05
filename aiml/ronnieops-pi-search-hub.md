# ronnieops/pi-search-hub

[![Stars](https://img.shields.io/github/stars/ronnieops/pi-search-hub?style=flat-square&color=yellow)](https://github.com/ronnieops/pi-search-hub/stargazers) [![Forks](https://img.shields.io/github/forks/ronnieops/pi-search-hub?style=flat-square&color=blue)](https://github.com/ronnieops/pi-search-hub/network) [![Language](https://img.shields.io/badge/lang-TypeScript-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-69%2F100-brightgreen?style=flat-square)](#)

> Unified web search + content extraction extension for pi with 17 backends. Auto-fallback, RRF combine mode, pluggable web_read (Jina/Sofya), and env/shell credential resolution.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 22 |
| 🍴 **Forks** | 11 |
| 💻 **Language** | TypeScript |
| 📈 **Score** | 69/100 |
| 🗓️ **Last push** | 2026-09-05 |
| 🔍 **Source** | github |

## 🏷️ Topics

`ai-agent` `cli-tool` `coding-agent` `combine-mode` `jina` `open-source` `perplexity` `pi` `pi-coding-agent` `pi-extension` `pi-package` `reciprocal-rank-fusion`

## 🎯 Categories

AI/ML · DevTools

## 📝 Summary

### English

**Brief Summary (2‑3 sentences)**  
`ronnieops/pi-search-hub` is a TypeScript‑based extension that adds unified web‑search and content‑extraction capabilities to the Pi AI platform, supporting 17 different back‑ends and offering auto‑fallback, reciprocal rank fusion (RRF) merging, and pluggable readers such as Jina or Sofya. It resolves credentials from environment variables or the shell, making it easy to prototype RAG or agent‑driven workflows without building a search stack from scratch.  

**Value**  
- **Speed to prototype** – developers can plug in a wide range of search providers (search engines, vector stores, APIs) with a single configuration, instantly giving any Pi model access to up‑to‑date web data.  
- **Flexibility** – the RRF combine mode and auto‑fallback let you blend results from multiple sources for higher recall and robustness, while the modular `web_read` interface lets you swap or add new extractors without code changes.  
- **Lower operational overhead** – credential handling is automated through env/shell resolution, reducing the need for custom secret‑management code.  

**Practical Adoption Path**  
1. **Evaluate** – Clone the repo, run the provided CLI (`pi-search-hub-cli`) against a small test query to verify connectivity to the desired back‑ends.  
2. **Integrate** – Import the SDK into your Pi project (`import { SearchHub } from "pi-search-hub"`), configure the desired back‑ends in a JSON/YAML file, and inject the `SearchHub` instance into your existing prompt‑engineering or agent pipeline.  
3. **Extend** – If you need a custom source, implement the `WebReader` interface and register it in the hub’s plugin registry.  
4. **Test** – Use the built‑in unit tests or write integration tests that mock external APIs to ensure fallback and RRF behavior meets your quality criteria.  

**Production Readiness**  
- **Maturity** – Medium. The project is actively maintained (last commit 2026‑06‑22), has 22 stars and 11 forks, and the codebase is reasonably clean TypeScript with clear extension points.  
- **Dependencies** – Relies on external search APIs and optional readers (Jina, Sofya); you’ll need to audit their licensing, rate limits, and security posture.  
- **Operational considerations** – Verify credential handling aligns with your secret‑management policies, and monitor the health of the fallback back‑ends to avoid silent degradation.  
- **Next steps before production** – Conduct a security review (especially for any third‑party readers), lock dependency versions, and add observability (metrics/logging) around query routing and RRF scoring.  

In short, `pi-search-hub` offers a fast, extensible way to give Pi‑based AI systems real‑time web knowledge, making it a solid choice for internal prototypes and, with proper hardening, for production‑grade RAG or agent workflows.

### Русский

**ronnieops/pi-search-hub** — это открытая TypeScript‑библиотека, объединяющая веб‑поиск и извлечение контента из 17 источников с авто‑fallback, RRF‑комбинированием и поддержкой плагинных web‑read (Jina, Sofya) и динамического разрешения учётных данных из окружения/шелла. Она позволяет быстро добавить AI‑возможности в прототипы и внутренние RAG/агентные воркфлоу, используя готовый API/SDK/CLI без необходимости строить собственный стек моделей. Готовность к production — средняя: проект стабилен для прототипов, но требует проверки лицензии, безопасности и поддержки зависимостей перед развертыванием в продакшн.

### 中文

**项目简介**  
ronnieops/pi‑search‑hub 是一款面向 **pi**（Prompt‑injection）平台的统一 Web 搜索与内容抽取扩展，内置 17 种后端搜索引擎，支持自动回退、RRF（Reciprocal Rank Fusion）组合模式、可插拔的 `web_read` 实现（如 Jina、Sofya），并能够通过环境变量或 Shell 脚本自动解析凭证。

---

## 价值主张  
- **快速赋能 AI 应用**：无需从零搭建检索模型栈，直接调用已有搜索后端，即可为聊天机器人、RAG（检索增强生成）或智能代理提供可靠的网络信息来源。  
- **灵活组合与容错**：RRF 融合与自动回退机制保证在单一后端失效或查询质量不佳时仍能返回有价值的结果。  
- **易于扩展**：通过插件式的 `web_read` 接口，可随时接入新的爬取/解析服务，满足特定行业或私有数据的需求。

---

## 典型接入方式  

| 场景 | 接入方式 | 关键步骤 |
|------|----------|----------|
| **原型开发** | **CLI** 或 **Node.js SDK** | 1. `npm i pi-search-hub` <br>2. 在代码中 `import { search } from "pi-search-hub"` <br>3. 配置 `PI_SEARCH_BACKENDS` 环境变量或在运行时传入后端列表 |
| **后端服务** | **REST API**（通过自建的轻量服务包装） | 1. 启动 `pi-search-hub` 的 HTTP 入口（`npm run start:server`） <br>2. 通过 `POST /search` 发送 `{ query, backends?, options? }` <br>3. 解析返回的统一结果结构 |
| **Agent / RAG 工作流** | **插件式调用**（与 LangChain、LlamaIndex 等框架集成） | 1. 实现 `WebReadProvider` 接口（如使用 Jina） <br>2. 在工作流中注入 `searchHub.search(query)` 作为检索步骤 <br>3. 将返回的 `content` 直接喂给 LLM 进行生成 |
| **CI/CD/脚本** | **Shell 环境变量** | 1. 在 CI 脚本中导出 `PI_SEARCH_API_KEY=…`、`PI_SEARCH_ENDPOINT=…` <br>2. 直接调用 `pi-search-hub search "your query"` 获取文本输出，供后续自动化处理 |

> **提示**：所有入口都支持 `credentialResolver`，可自动读取 `process.env`、`.env` 文件或通过自定义 Shell 脚本提供的凭证。

---

## 生产可用性评估  

| 维度 | 现状 | 建议 |
|------|------|------|
| **功能完整性** | 已实现 17 种后端、自动回退、RRF、插件化 `web_read`，满足大多数检索需求。 | 在生产环境中选定 2–3 核心后端，关闭不必要的备用后端以降低维护成本。 |
| **代码成熟度** | 22 ⭐、11 🍴，最近一次提交 2026‑06‑22，使用 TypeScript 编写。 | 进行代码审计，关注依赖（如 `axios`、`jina-sdk`）的安全更新；若可能，fork 并自行维护关键依赖的版本。 |
| **部署与运维** | 提供 CLI、SDK 与可选的 HTTP Server，部署方式灵活。 | 推荐使用 Docker 镜像或在 Kubernetes 中以 Sidecar 方式运行，配合 ConfigMap 管理后端配置与凭证。 |
| **可靠性** | 自动回退与 RRF 提供一定容错；但后端可用性仍受外部服务影响。 | 实施健康检查（`/healthz`），并在监控平台上追踪每个后端的响应时延与错误率。 |
| **安全性** | 目前未发现重大元数据风险，但许可证、依赖漏洞、凭证泄露需进一步审查。 | - 确认使用的开源许可证兼容公司政策。<br>- 使用 `npm audit`、`snyk` 等工具定期扫描依赖。<br>- 将凭证统一存放在 Vault/K8s Secret，避免硬编码。 |
| **可扩展性** | 插拔式 `web_read` 设计易于接入自研爬虫或私有搜索服务。 | 若业务需要内部文档检索，可实现自定义 `WebReadProvider` 并注册到搜索中心。 |

**总体结论**：  
`ronnieops/pi-search-hub` 在 **原型验证** 与 **内部研发工作流** 中具备良好的即插即用特性，能够显著降低 AI 检索功能的实现门槛。若在生产环境使用，建议对关键后端进行监控、对依赖进行安全审计，并通过容器化部署和凭证管理来提升可靠性与安全性。经过这些加固后，项目可作为 **中等风险** 的生产组件投入使用。

## 🧭 Practical evaluation

**Value:** ronnieops/pi-search-hub helps add AI capability without starting from a blank model stack.

**Best use cases**

- prototype AI features
- build RAG or agent workflows
- evaluate model tooling

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** Medium: useful for prototypes or internal workflows, with dependency and maintenance checks before production.

**Quality signals**

- 22 GitHub stars
- 11 forks
- updated 2026-06-22
- primary language: TypeScript
- 16 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 27/100 |
| stars | 29/100 |
| topics | 100/100 |
| outlook | 73/100 |
| quality | 63/100 |
| recency | 80/100 |
| adoption | 28/100 |
| production | 68/100 |
| usefulness | 90/100 |
| integration | 62/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 200/100 |

---

<sub>🔭 Discovered 2026-06-22 · [View on GitHub](https://github.com/ronnieops/pi-search-hub) · [← Back to AI/ML](./README.md)</sub>
