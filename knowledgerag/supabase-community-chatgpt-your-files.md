# supabase-community/chatgpt-your-files

[![Stars](https://img.shields.io/github/stars/supabase-community/chatgpt-your-files?style=flat-square&color=yellow)](https://github.com/supabase-community/chatgpt-your-files/stargazers) [![Forks](https://img.shields.io/github/forks/supabase-community/chatgpt-your-files?style=flat-square&color=blue)](https://github.com/supabase-community/chatgpt-your-files/network) [![Language](https://img.shields.io/badge/lang-TypeScript-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-66%2F100-brightgreen?style=flat-square)](#)

> Production-ready MVP for securely chatting with your documents using pgvector

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 514 |
| 🍴 **Forks** | 194 |
| 💻 **Language** | TypeScript |
| 📈 **Score** | 66/100 |
| 🗓️ **Last push** | 2026-05-12 |
| 🔍 **Source** | github |

## 🏷️ Topics

`ai` `db` `embeddings` `ml` `rag` `supabase` `vector`

## 🎯 Categories

Knowledge/RAG · AI/ML · Product

## 📝 Summary

### English

**Brief Summary (2‑3 sentences)**  
Supabase‑Community’s **chatgpt‑your‑files** is a production‑ready MVP that lets you securely chat with the contents of your documents by storing vector embeddings in a Supabase pgvector table. It turns internal knowledge bases into searchable, AI‑driven assistants, enabling more accurate, context‑grounded responses without moving data out of your own infrastructure.  

**Value**  
- **Searchable internal knowledge** – By indexing PDFs, markdown, or any text file as vector embeddings, the project makes previously siloed information instantly retrievable through natural‑language queries.  
- **Grounded AI assistants** – The retrieved chunks are fed to ChatGPT (or any compatible LLM), ensuring that generated answers are anchored in your own data rather than relying solely on the model’s pre‑training.  
- **Secure, self‑hosted stack** – All data lives in a Supabase Postgres instance with pgvector, giving you full control over access, encryption, and compliance.  

**Practical Adoption Path**  
1. **Proof‑of‑Concept** – Clone the repo, follow the README to spin up a Supabase project, and run the provided script to ingest a small set of test documents.  
2. **Integration** – Replace the demo ingestion pipeline with your own document source (e.g., internal wiki, Confluence export, or S3 bucket) and adjust the embedding model if needed.  
3. **API Hook‑up** – Call the `/chat` endpoint from your existing chatbot, help‑desk UI, or internal portal; the service returns the relevant context and the LLM‑generated answer.  
4. **Scale & Harden** – Enable Supabase Row Level Security, add rate limiting, and configure a production‑grade embedding model (e.g., OpenAI embeddings or an on‑premise alternative).  

**Production Readiness**  
- **Activity & Adoption** – 514 ★, 194 forks, recent commits (last update 2026‑05‑12), and a TypeScript codebase aligned with Supabase’s ecosystem indicate strong community momentum.  
- **MVP Completeness** – Core features (document ingestion, vector storage, retrieval, and LLM integration) are implemented and documented, making it suitable for a pilot in a controlled environment.  
- **Risk Considerations** – No major metadata or licensing issues identified, but a final review of the open‑source license, security posture of any third‑party APIs (e.g., OpenAI), and maintainer responsiveness is advisable before full production rollout.  

Overall, **chatgpt‑your‑files** offers a ready‑to‑use, self‑hosted RAG layer that can be evaluated with a small proof‑of‑concept and, after standard hardening steps, promoted to a production‑grade internal knowledge assistant.

### Русский

**supabase-community/chatgpt-your-files** – это готовый к продакшен MVP, позволяющий безопасно задавать вопросы вашим документам через ChatGPT, используя векторный поиск pgvector. Типичный сценарий — быстрая индексация внутренней базы знаний (ручные файлы, wiki, PDF) и последующее «заземление» ответов ассистента в актуальные данные, что повышает точность и релевантность поиска. Проект имеет высокую готовность к production: активные коммиты, 514 звёзд, 194 форка, поддержка TypeScript и интеграция с Supabase, что делает его надёжным выбором для пилотного внедрения в небольшом proof‑of‑concept, после чего можно масштабировать.

### 中文

**项目简介**  
supabase-community/chatgpt-your-files 是一个基于 Supabase + pgvector 的生产级 MVP，能够安全地将文档向量化后与 ChatGPT 对话，让用户在聊天窗口直接查询和引用内部文档内容。

**价值**  
- **内部知识可搜索、可用**：将企业内部手册、FAQ、技术文档等转化为向量索引，助理在回答时可以直接“引用”真实文档，提升答案的准确性和可信度。  
- **提升文档检索效率**：相较传统关键字搜索，向量检索支持语义相似度匹配，用户可用自然语言快速定位所需信息。  
- **降低集成成本**：基于 Supabase 完全托管的 Postgres 与 pgvector，省去自行部署向量数据库和身份鉴权的繁琐步骤。

**典型接入方式**  
1. **准备文档**：将 PDF、Markdown、TXT 等文件上传至 Supabase Storage。  
2. **向量化**：使用项目提供的脚本或 API（基于 OpenAI/Claude 等模型）将文档切片并生成向量，写入 Supabase 中的 pgvector 表。  
3. **配置 ChatGPT**：在 OpenAI 控制台设置自定义指令或函数调用，让 ChatGPT 在对话中调用 `/search` API 查询向量表并返回最相关的片段。  
4. **前端集成**：项目自带的 React/Next.js 示例页面可直接嵌入现有内部门户，也可以通过 REST/GraphQL 接口自行构建 UI。  

**生产可用性**  
- **活跃度高**：截至 2026‑05‑12，项目拥有 514 星、194 Fork，最近一次提交在当天，说明代码维护及时。  
- **技术成熟**：核心使用 TypeScript 编写，依赖 Supabase（托管 Postgres）和 pgvector，均为业界成熟组件，具备自动备份、访问控制和水平扩展能力。  
- **安全性**：文档存储在 Supabase 私有 bucket，向量查询通过 RLS（行级安全）和 JWT 鉴权，满足大多数企业内部合规要求。  
- **适合先行试点**：建议先在小规模文档集（如部门手册）上完成 PoC，验证检索准确率与成本后再推广至全公司知识库。  

综上，chatgpt-your-files 已具备生产级别的功能完整性和社区支持，是在内部知识库上实现 RAG（检索增强生成）的可靠开源选项。

## 🧭 Practical evaluation

**Value:** supabase-community/chatgpt-your-files helps make internal knowledge searchable and usable by assistants.

**Best use cases**

- index knowledge bases
- improve search over documents
- ground assistant answers

**Integration notes:** Looks feasible to evaluate, but integration should start with a small proof of concept and README check.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 514 GitHub stars
- 194 forks
- updated 2026-05-12
- primary language: TypeScript
- 7 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 57/100 |
| stars | 58/100 |
| topics | 88/100 |
| outlook | 80/100 |
| quality | 79/100 |
| recency | 100/100 |
| adoption | 58/100 |
| production | 76/100 |
| usefulness | 58/100 |
| integration | 46/100 |
| sourceTrust | 100/100 |

---

<sub>🔭 Discovered 2026-05-12 · [View on GitHub](https://github.com/supabase-community/chatgpt-your-files) · [← Back to Knowledgerag](./README.md)</sub>
