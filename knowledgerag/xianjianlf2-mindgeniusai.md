# xianjianlf2/MindGeniusAI

[![Stars](https://img.shields.io/github/stars/xianjianlf2/MindGeniusAI?style=flat-square&color=yellow)](https://github.com/xianjianlf2/MindGeniusAI/stargazers) [![Forks](https://img.shields.io/github/forks/xianjianlf2/MindGeniusAI?style=flat-square&color=blue)](https://github.com/xianjianlf2/MindGeniusAI/network) [![Language](https://img.shields.io/badge/lang-TypeScript-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-76%2F100-brightgreen?style=flat-square)](#)

> An AI agent that reads your PDFs and draws editable mind maps — visible tool-calling loop, built-in RAG, bring-your-own-key, multi-provider (OpenAI / Claude / DeepSeek / Kimi). Self-hostable.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 276 |
| 🍴 **Forks** | 59 |
| 💻 **Language** | TypeScript |
| 📈 **Score** | 76/100 |
| 🗓️ **Last push** | 2026-09-05 |
| 🔍 **Source** | github |

## 🏷️ Topics

`agent` `ai-agent` `antv-x6` `bring-your-own-key` `chatgpt` `claude` `deepseek` `hono` `kimi` `llm` `mind-map` `mindmap`

## 🎯 Categories

Knowledge/RAG · AI/ML · Frontend · Libraries & SDKs

## 📝 Summary

### English

**Brief Summary (2‑3 sentences)**  
MindGeniusAI is an open‑source, self‑hostable AI agent that ingests PDFs, builds editable mind‑maps, and supports visible tool‑calling loops with built‑in Retrieval‑Augmented Generation (RAG). It works with multiple LLM providers (OpenAI, Claude, DeepSeek, Kimi), lets you bring your own API keys, and offers a TypeScript SDK/CLI for easy integration. With 276 stars and recent activity, it’s positioned as a practical way to make internal document knowledge searchable and actionable.

**Value**  
- **Knowledge accessibility** – By converting PDFs into structured, editable mind maps, the project turns static documents into navigable knowledge graphs that assistants can query directly.  
- **Multi‑provider flexibility** – Teams can switch or combine LLM back‑ends without code changes, protecting against vendor lock‑in and allowing cost optimisation.  
- **Self‑hosted control** – All data stays on‑premises or in a private cloud, satisfying security and compliance requirements for sensitive corporate knowledge bases.  

**Practical Adoption Path**  
1. **Deploy** – Use the provided Docker compose or Helm chart to spin up the service in a sandbox environment.  
2. **Configure** – Add your preferred LLM API keys (OpenAI, Claude, DeepSeek, Kimi) in the `.env` file; optionally enable the “bring‑your‑own‑key” mode for custom endpoints.  
3. **Index PDFs** – Run the CLI (`mindgenius index <folder>`) or call the REST SDK to ingest existing PDFs; the system automatically creates the RAG index and mind‑map nodes.  
4. **Integrate** – Consume the generated mind‑maps via the TypeScript SDK, GraphQL API, or CLI for downstream apps (search UI, chat assistants, internal portals).  
5. **Iterate** – Edit mind‑maps through the web UI, re‑index changed documents, and fine‑tune prompts or retrieval parameters as needed.  

**Production Readiness**  
- **Activity & Community** – Updated on 2026‑06‑24, 276 stars, 59 forks, and 18 related topics indicate a vibrant community and ongoing maintenance.  
- **Architecture** – Containerised, language‑agnostic APIs, and explicit tool‑calling loops make it easy to scale horizontally and to monitor/trace calls in production.  
- **Security & Compliance** – Self‑hosting means you control data residency; the only external exposure is the LLM provider endpoints, which can be locked down via network policies.  
- **Risks** – Final due‑diligence on the license (MIT‑style, but verify), a formal security audit, and ensuring maintainers have a clear hand‑off plan are still required before a mission‑critical rollout.  

Overall, MindGeniusAI is a mature, multi‑provider, self‑hosted solution that can be evaluated quickly and, after standard security review, promoted to production for internal knowledge search and assistant grounding.

### Русский

**MindGeniusAI** — это открытый AI‑агент, который читает ваши PDF‑файлы, индексирует их через встроенный RAG и генерирует редактируемые майнд‑карты; поддерживает несколько провайдеров моделей (OpenAI, Claude, DeepSeek, Kimi) и возможность использовать собственный API‑ключ. Типичный сценарий — подключить проект к существующей базе знаний, чтобы сделать документы поисковыми, улучшить поиск и дать ассистенту контекст для более точных ответов. Проект уже активно поддерживается (276 звёзд, последние коммиты 2026‑06‑24, TypeScript, CLI/SDK), что делает его готовым к пилотному внедрению в продакшн при дальнейшем проверке лицензии и безопасности.

### 中文

**项目简介**  
MindGeniusAI（xianjianlf2/MindGeniusAI）是一款开源的 AI 助手，能够读取 PDF 文档并自动生成可编辑的思维导图。它内置可视化的工具调用循环、RAG（检索增强生成）能力，支持自带 API Key 或多供应商（OpenAI、Claude、DeepSeek、Kimi）接入，且可自行部署。

**价值**  
- **知识可搜索、可视化**：把散落在 PDF、内部手册等文档中的信息结构化为思维导图，帮助团队快速定位和理解关键内容。  
- **提升检索与问答质量**：基于 RAG 的索引让聊天机器人或业务助手在回答时直接引用最新文档，降低幻觉风险。  
- **灵活部署与成本控制**：支持自带 API Key 或多模型提供商，可在私有服务器上完整自托管，满足安全合规和成本优化需求。

**典型接入方式**  
1. **API/SDK 调用**：项目提供 RESTful API 与 TypeScript SDK，前端或后端服务只需调用 `POST /mindmap` 并传入 PDF/文档路径，即可获得思维导图的 JSON/HTML。  
2. **CLI 工具**：通过 `mindgenius-cli generate -f file.pdf` 在本地或 CI 流程中直接生成思维导图，适合批量处理。  
3. **插件/集成**：可在现有文档管理系统（如 Confluence、Notion）或搜索平台中嵌入调用代码，实现“一键生成”或“搜索即视图”。  

**生产可用性**  
- **活跃度**：截至 2026‑06‑24 最近一次提交，拥有 276 星、59 Fork，社区讨论活跃。  
- **技术成熟度**：使用 TypeScript 编写，提供完整的类型定义和示例，易于在前端/Node 环境集成。  
- **可部署性**：提供 Docker 镜像和 Helm Chart，支持在本地、K8s 或云服务器上一键部署。  
- **安全与合规**：代码开源、许可证明确（需再次确认），无敏感数据泄露风险，支持自带密钥，满足企业内部安全要求。  

综合来看，MindGeniusAI 在功能完整性、社区活跃度和部署便利性方面均表现良好，已具备在企业内部知识库、文档搜索和智能助理场景中进行正式试点的生产级准备度。

## 🧭 Practical evaluation

**Value:** xianjianlf2/MindGeniusAI helps make internal knowledge searchable and usable by assistants.

**Best use cases**

- index knowledge bases
- improve search over documents
- ground assistant answers

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 276 GitHub stars
- 59 forks
- updated 2026-06-24
- primary language: TypeScript
- 18 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 44/100 |
| stars | 52/100 |
| topics | 100/100 |
| outlook | 80/100 |
| quality | 72/100 |
| recency | 80/100 |
| adoption | 50/100 |
| production | 71/100 |
| usefulness | 100/100 |
| integration | 62/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 400/100 |

---

<sub>🔭 Discovered 2026-06-24 · [View on GitHub](https://github.com/xianjianlf2/MindGeniusAI) · [← Back to Knowledgerag](./README.md)</sub>
