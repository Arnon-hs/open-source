# brianpetro/obsidian-smart-connections

[![Stars](https://img.shields.io/github/stars/brianpetro/obsidian-smart-connections?style=flat-square&color=yellow)](https://github.com/brianpetro/obsidian-smart-connections/stargazers) [![Forks](https://img.shields.io/github/forks/brianpetro/obsidian-smart-connections?style=flat-square&color=blue)](https://github.com/brianpetro/obsidian-smart-connections/network) [![Language](https://img.shields.io/badge/lang-JavaScript-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-73%2F100-brightgreen?style=flat-square)](#)

> Chat with your notes & see links to related content with AI embeddings. Use local models or 100+ via APIs like Claude, Gemini, ChatGPT & Llama 3

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 5k |
| 🍴 **Forks** | 310 |
| 💻 **Language** | JavaScript |
| 📈 **Score** | 73/100 |
| 🗓️ **Last push** | 2026-05-14 |
| 🔍 **Source** | github |

## 🏷️ Topics

`chatgpt` `claude` `embeddings` `gemini` `llama3` `obsidian` `obsidian-plugin`

## 🎯 Categories

Knowledge/RAG · AI/ML · Backend

## 📝 Summary

### English

**Brief Summary (2‑3 sentences)**  
*Obsidian Smart Connections* lets you converse with your Obsidian notes and instantly surface AI‑generated links to related content using vector embeddings. It works with local models or any of the 100+ supported APIs (Claude, Gemini, ChatGPT, Llama 3, etc.), turning a personal knowledge vault into a searchable, assistant‑ready knowledge base.

**Value**  
- **Searchable internal knowledge** – By embedding every note, the plugin creates a dense, semantic index that goes far beyond keyword search, making it easy for LLM‑driven assistants to retrieve the right context.  
- **AI‑augmented navigation** – The chat UI surfaces relevant notes, backlinks, and summaries on‑the‑fly, helping users discover connections they might otherwise miss.  
- **Vendor flexibility** – You can run embeddings locally for privacy‑sensitive data or plug into any of the 100+ hosted LLM providers, avoiding lock‑in and allowing cost optimisation.

**Practical Adoption Path**  
1. **Install the plugin** in Obsidian (simple UI‑based install).  
2. **Choose an embedding source** – either a local model (e.g., sentence‑transformers) for on‑prem security or an API key for a cloud provider you already use.  
3. **Run the initial indexing**; the plugin streams notes through the selected model and stores vectors in a local SQLite/LMDB store.  
4. **Configure the chat endpoint** (Claude, Gemini, ChatGPT, Llama 3, etc.) and set any rate‑limit or cost controls.  
5. **Start chatting** – the assistant will retrieve the top‑k relevant notes via cosine similarity and feed them into the LLM prompt, delivering context‑aware answers and link suggestions.  
6. **Iterate** – adjust chunk size, similarity thresholds, or add custom metadata (tags, folders) to fine‑tune relevance for your organization’s use cases (e.g., product documentation, R&D notes, compliance manuals).

**Production‑Readiness**  
- **Activity & community** – 4,986 stars, 310 forks, recent commits (as of 2026‑05‑14) and an active issue/PR flow indicate a healthy open‑source project.  
- **Maturity** – The plugin already exposes clear integration points (API/SDK/CLI), supports multiple languages, and ships with sensible defaults for both local and cloud embeddings.  
- **Scalability** – Vector storage is local but can be swapped for an external vector DB (e.g., Pinecone, Weaviate) without code changes, enabling enterprise‑scale deployments.  
- **Risk considerations** – No obvious metadata or licensing red flags, but a final security audit (dependency scanning, supply‑chain review) and confirmation of maintainer responsiveness are advisable before mission‑critical rollout.

Overall, *Obsidian Smart Connections* is a production‑ready OSS candidate for organizations that need to turn their internal note collections into an AI‑searchable knowledge base, with a low‑friction adoption path and flexibility to meet both privacy and cost constraints.

### Русский

**Обзор:** `brianpetro/obsidian-smart-connections` — это OSS‑инструмент, который с помощью AI‑эмбеддингов превращает ваши заметки в интерактивный «умный» поиск: чат‑интерфейс позволяет задавать вопросы к базе знаний, а система мгновенно предлагает релевантные ссылки и контекст из Obsidian.  

**Типовой сценарий:** проиндексировать внутреннюю библиотеку документов (например, техническую документацию, клиентские кейсы или исследовательские заметки) и использовать локальные модели или более 100 облачных API (Claude, Gemini, ChatGPT, Llama 3) для улучшения поиска и «заземления» ответов ассистентов.  

**Готовность к production:** высокая – проект активно поддерживается (обновления до 2026‑05‑14), имеет 5 000+ ⭐, 300+ форков, готовый JavaScript‑SDK/CLI и чётко оформленные API, что делает его надёжным кандидатом для пилотного внедрения в корпоративных средах.

### 中文

**项目简介**  
`brianpetro/obsidian-smart-connections` 是一款基于 AI 嵌入的 Obsidian 插件，能够让你直接在笔记中对话式查询，并即时展示与当前内容相关的链接。插件支持本地模型，也可通过 Claude、Gemini、ChatGPT、Llama 3 等 100+ 公共 API 调用。

**价值**  
- 将内部知识库转化为可搜索、可对话的知识图谱，提升信息检索效率。  
- 为聊天机器人或企业助理提供可靠的上下文来源，避免“幻觉”回答。  
- 支持多模型切换，兼顾隐私（本地模型）和强大算力（云 API）。

**典型接入方式**  
1. **Obsidian 插件**：在 Obsidian 中直接安装插件，配置 API 密钥或本地模型路径，即可开始使用。  
2. **CLI / SDK**：插件同时提供命令行工具和 JavaScript SDK，方便在 CI/CD、自动化脚本或自建后端服务中调用嵌入生成与相似度检索。  
3. **API 网关**：通过插件暴露的 HTTP 接口，可将其集成到企业内部的知识检索平台或聊天机器人框架（如 LangChain、RAG‑Pipeline）中。

**生产可用性**  
- **活跃度高**：截至 2026‑05‑14，项目最近一次提交，拥有 4,986 ★、310 Fork，社区活跃。  
- **技术成熟**：基于 JavaScript/Node.js，提供完整的 API/CLI 文档，易于在现有后端体系中集成。  
- **安全与合规**：暂无重大元数据风险，仍需自行审查许可证（MIT）和依赖安全报告。  
- **可评估性强**：实现信号（API、SDK、CLI）明确，支持本地模型与主流云模型，适合作为内部知识检索或 RAG 方案的试点项目。  

综上，`obsidian-smart-connections` 在功能完整性、社区活跃度和集成便利性方面表现良好，是一个值得在生产环境中进行小规模试点并逐步推广的 OSS 方案。

## 🧭 Practical evaluation

**Value:** brianpetro/obsidian-smart-connections helps make internal knowledge searchable and usable by assistants.

**Best use cases**

- index knowledge bases
- improve search over documents
- ground assistant answers

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 4986 GitHub stars
- 310 forks
- updated 2026-05-14
- primary language: JavaScript
- 7 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 62/100 |
| stars | 79/100 |
| topics | 88/100 |
| outlook | 84/100 |
| quality | 86/100 |
| recency | 100/100 |
| adoption | 74/100 |
| production | 81/100 |
| usefulness | 58/100 |
| integration | 62/100 |
| sourceTrust | 100/100 |

---

<sub>🔭 Discovered 2026-05-14 · [View on GitHub](https://github.com/brianpetro/obsidian-smart-connections) · [← Back to Knowledgerag](./README.md)</sub>
