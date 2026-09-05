# psinetron/echoes-vault-opencode

[![Stars](https://img.shields.io/github/stars/psinetron/echoes-vault-opencode?style=flat-square&color=yellow)](https://github.com/psinetron/echoes-vault-opencode/stargazers) [![Forks](https://img.shields.io/github/forks/psinetron/echoes-vault-opencode?style=flat-square&color=blue)](https://github.com/psinetron/echoes-vault-opencode/network) [![Language](https://img.shields.io/badge/lang-TypeScript-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-66%2F100-brightgreen?style=flat-square)](#)

> Persistent memory plugin for OpenCode. Obsidian-style knowledge base that survives across sessions

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 168 |
| 🍴 **Forks** | 2 |
| 💻 **Language** | TypeScript |
| 📈 **Score** | 66/100 |
| 🗓️ **Last push** | 2026-09-05 |
| 🔍 **Source** | github |

## 🏷️ Topics

`agentic-memory` `ai-agent` `developer-tools` `knowledge-base` `llm` `markdown` `memory` `obsidian` `okf` `opencode`

## 🎯 Categories

Knowledge/RAG · AI/ML · Documents · DevTools

## 📝 Summary

### English

**Brief Summary**  
psinetron/echoes‑vault‑opencode is a TypeScript‑based persistent‑memory plugin that turns an OpenCode workspace into an Obsidian‑style knowledge vault, keeping indexed information alive across sessions. It lets AI assistants query and ground their responses in your internal docs, turning a static repository into a searchable, RAG‑ready knowledge base.  

**Value**  
- **Searchable internal knowledge** – By continuously indexing markdown, code, and other assets, the plugin makes the full corpus instantly searchable for downstream assistants, reducing hallucinations and improving answer relevance.  
- **Seamless RAG integration** – The exposed API/SDK and CLI let you plug the vault into any LLM‑driven workflow (chatbots, coding assistants, support bots) without building a custom indexer.  
- **Developer‑friendly** – Built in TypeScript, it aligns with typical OpenCode toolchains, and its Obsidian‑like UI familiarizes users with minimal onboarding.  

**Practical Adoption Path**  
1. **Prototype** – Clone the repo, run the provided CLI to point the vault at an existing OpenCode project, and verify that documents are indexed and retrievable via the demo API.  
2. **Integrate** – Replace the demo calls with your assistant’s retrieval layer (e.g., LangChain, LlamaIndex) using the SDK’s `search` endpoint.  
3. **Secure & Extend** – Add authentication, role‑based access, and custom parsers for proprietary formats; optionally contribute those back to the project.  
4. **Pilot** – Deploy the vault as a containerized microservice in a staging environment, route a subset of assistant queries through it, and measure retrieval latency and answer quality.  

**Production Readiness**  
- **Activity & Adoption** – 168 ★, recent commits (last updated 2026‑06‑25), and a growing ecosystem of topics indicate active maintenance.  
- **Stability** – The core API is stable, documented, and exposed via both CLI and SDK, making integration straightforward.  
- **Risk Profile** – No glaring licensing or security red flags have been identified, though a final review of the open‑source license and a security audit are advisable before full rollout.  

Overall, the project is mature enough for a serious pilot in production environments, especially where an OpenCode‑based knowledge base needs to be leveraged by AI assistants.

### Русский

**psinetron/echoes-vault-opencode** — это плагин постоянной памяти для OpenCode, создающий Obsidian‑подобную базу знаний, которая сохраняется между сессиями и делает внутреннюю информацию доступной для AI‑ассистентов. Типичный сценарий: индексировать корпоративные документы, улучшать поиск и использовать сохранённые фрагменты как контекст для генерации ответов ассистентом. Проект уже активно поддерживается (обновления 2026‑06‑25, 168 звёзд, TypeScript‑код, API/SDK/CLI), что свидетельствует о высокой готовности к пилотному запуску в продакшн, хотя лицензия и безопасность требуют окончательной проверки.

### 中文

**项目简介**  
psinetron/echoes-vault-opencode 是一款面向 OpenCode 的持久化记忆插件，提供类似 Obsidian 的知识库结构，能够在不同会话之间保持并复用内部知识。  

**价值体现**  
- 将组织内部文档、笔记等知识资产统一索引，使得大模型或聊天助理能够快速检索并在回答中引用真实、最新的内容。  
- 改善文档搜索精度，支持基于主题、标签和全文的高级查询，帮助团队降低信息碎片化带来的效率损失。  

**典型接入方式**  
1. **API/SDK**：通过插件提供的 RESTful API 或 TypeScript SDK，在后端服务中调用 `indexDocument`、`search` 等接口，实现自动化文档写入和实时查询。  
2. **CLI**：使用自带的命令行工具 `echoes-vault`，可在 CI/CD 流程或本地脚本中批量导入/更新知识库。  
3. **语言元数据**：插件支持在 TypeScript 项目中直接通过装饰器标记知识点，实现“代码即知识”的双向绑定。  

**生产可用性**  
- **活跃度**：最近一次提交于 2026‑06‑25，星标 168，社区已有 2 次 Fork，说明项目仍在积极维护。  
- **生态兼容**：基于 TypeScript 开发，易于与现有 Node.js/React 项目集成；同时提供 OpenAPI 规范，便于跨语言调用。  
- **风险**：目前未发现重大许可证或安全漏洞，但仍建议在正式上线前完成许可证合规审查并进行安全渗透测试。  

综合来看，echoes‑vault‑opencode 在功能完整性、社区活跃度和技术栈兼容性方面表现良好，适合作为内部知识检索与大模型 grounding 的生产级组件进行试点。

## 🧭 Practical evaluation

**Value:** psinetron/echoes-vault-opencode helps make internal knowledge searchable and usable by assistants.

**Best use cases**

- index knowledge bases
- improve search over documents
- ground assistant answers

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 168 GitHub stars
- 2 forks
- updated 2026-06-25
- primary language: TypeScript
- 10 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 12/100 |
| stars | 47/100 |
| topics | 100/100 |
| outlook | 72/100 |
| quality | 67/100 |
| recency | 80/100 |
| adoption | 37/100 |
| production | 69/100 |
| usefulness | 74/100 |
| integration | 62/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 400/100 |

---

<sub>🔭 Discovered 2026-06-25 · [View on GitHub](https://github.com/psinetron/echoes-vault-opencode) · [← Back to Knowledgerag](./README.md)</sub>
