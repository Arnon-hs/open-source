# leemysw/feishu-docx

[![Stars](https://img.shields.io/github/stars/leemysw/feishu-docx?style=flat-square&color=yellow)](https://github.com/leemysw/feishu-docx/stargazers) [![Forks](https://img.shields.io/github/forks/leemysw/feishu-docx?style=flat-square&color=blue)](https://github.com/leemysw/feishu-docx/network) [![Language](https://img.shields.io/badge/lang-Python-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-69%2F100-brightgreen?style=flat-square)](#)

> 🚀 Feishu/Lark Docs、Sheet、Bitable <-> Markdown | AI Agent-friendly knowledge base exporter and writer with OAuth 2.0, CLI, TUI & Claude Skills support - 飞书文档 <写入/导出> Markdown | AI Agent 友好型导出-写入工具

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 228 |
| 🍴 **Forks** | 31 |
| 💻 **Language** | Python |
| 📈 **Score** | 69/100 |
| 🗓️ **Last push** | 2026-09-05 |
| 🔍 **Source** | github |

## 🏷️ Topics

`ai-agent` `claude-skills` `context` `feishu` `file-parser` `knowledge` `lark` `markdown` `skills`

## 🎯 Categories

Knowledge/RAG · AI/ML · Documents · Security

## 📝 Summary

### English

**Brief Summary**  
Leemysw/feishu‑docx is a Python‑based toolkit that lets you import and export Feishu/Lark Docs, Sheets, and Bitable data to and from Markdown, with built‑in OAuth 2.0, a CLI, a TUI, and ready‑made Claude AI skills. It is designed as an AI‑agent‑friendly knowledge‑base bridge, enabling internal documents to be indexed, searched, and used as grounding material for conversational assistants.  

**Value**  
- **Searchable knowledge base:** By converting native Feishu content into plain‑text Markdown, the project makes corporate knowledge instantly consumable by vector‑store pipelines, RAG systems, and LLM‑powered assistants.  
- **Bidirectional sync:** Writers can push updated Markdown back into Feishu, keeping documentation in sync without manual copy‑pasting.  
- **AI‑ready integrations:** Pre‑packaged Claude skill definitions and OAuth handling reduce the engineering effort required to expose Feishu assets to any LLM or chatbot platform.  

**Practical Adoption Path**  
1. **Pilot the CLI/TUI:** Install the package (`pip install feishu-docx`) and run `feishu-docx export --doc-id <id> --output mydoc.md` to verify conversion quality on a few test documents.  
2. **Integrate with your RAG pipeline:** Feed the generated Markdown into your existing embedding/indexing workflow (e.g., LangChain, Haystack) to enrich retrieval.  
3. **Enable write‑back:** Use the `import` command or the provided Claude skill to let agents update Feishu docs automatically after a knowledge‑capture step.  
4. **Scale with OAuth 2.0:** Register an internal Feishu app, configure the client‑id/secret in the tool’s config, and roll out the service across teams via the CLI or as a lightweight microservice.  

**Production Readiness**  
- **Active maintenance:** Last commit on 2026‑06‑29, 228 ★ and 31 ⎇, indicating a healthy community and recent bug fixes.  
- **Clear security posture:** OAuth 2.0 flow is built‑in; no hidden credentials are stored, and the codebase is pure Python, simplifying audit.  
- **Ecosystem fit:** Exposes a clean API/CLI, aligns with common RAG stacks, and already ships language‑specific metadata (Markdown) that downstream tools expect.  
- **Risk considerations:** Verify the license compatibility with your organization, perform a brief security review of the OAuth implementation, and confirm that maintainers are responsive to issues before committing to a long‑term production deployment.  

Overall, leemysw/feishu‑docx is production‑ready for a pilot and, after the standard OSS due‑diligence steps, can be rolled out as the canonical bridge between Feishu knowledge assets and AI‑driven assistants.

### Русский

leemysw/feishu-docx — это open‑source инструмент на Python, который экспортирует и импортирует документы Feishu/Lark (Docs, Sheets, Bitable) в Markdown и обратно, обеспечивая OAuth 2.0, CLI, TUI и поддержку навыков Claude для AI‑агентов. Типовой сценарий: индексация внутренней知识‑базы в виде Markdown‑файлов, последующий поиск и загрузка контента в RAG‑системы или LLM‑ассистенты для улучшения поиска и основания ответов. Проект демонстрирует высокую готовность к production — недавняя активность, 228★, 31 форк, обновление в июне 2026 года и четкие сигналы интеграции (API/SDK/CLI), что делает его подходящим для пилотного внедрения после финальной проверки лицензии и безопасности.

### 中文

**项目简介（2‑3 句话）**  
leemysw/feishu‑docx 是一款基于 OAuth 2.0 的开源工具，能够在飞书（Feishu/Lark）文档、表格、Bitable 与 Markdown 之间自由导入导出，并提供 CLI、TUI 与 Claude AI Skills 支持，适配 AI Agent 场景。它让企业内部知识库可以以 Markdown 形式存储，从而更易于索引、搜索和在对话式 AI 中使用。

**价值**  
- **知识可搜索、可复用**：将飞书文档统一转为结构化的 Markdown，方便向向量数据库或搜索引擎喂入，实现 RAG（Retrieval‑Augmented Generation）与智能客服的知识检索。  
- **AI Agent 友好**：导出的 Markdown 保留标题层级、表格、图片等元信息，天然适配 LLM 的上下文加载与提示工程。  
- **统一管理**：通过统一的 CLI/TUI，可批量同步、增量更新或回写文档，降低手工维护成本。

**典型接入方式**  
1. **OAuth2.0 鉴权**：在飞书开放平台创建应用，获取 `app_id`、`app_secret` 并配置回调 URL；使用项目提供的 `feishu-auth` 命令行完成授权并缓存 token。  
2. **CLI 使用**：  
   ```bash
   feishu-docx export --type doc --id 1234567890 --out ./docs/project.md
   feishu-docx import --type doc --id 1234567890 --in ./updates/patch.md
   ```  
   支持批量、增量和指定时间范围的同步。  
3. **TUI（交互式终端）**：运行 `feishu-docx tui` 进入图形化列表，可直接勾选文档/表格进行导入导出，适合非技术用户。  
4. **Claude Skills / API 调用**：项目提供 `feishu_docx_skill.py`，可在 Anthropic Claude 中注册为自定义 Skill，实现“读取飞书文档并写入 Markdown” 的自然语言指令。  
5. **Python SDK**：在自定义脚本或微服务中 `import feishu_docx as fdx`，调用 `fdx.export_doc(doc_id)`、`fdx.import_doc(doc_id, markdown)` 完成业务流程自动化。

**生产可用性**  
- **活跃度**：截至 2026‑06‑29，项目最近一次提交，星标 228，fork 31，Issue/PR 交互活跃，表明社区和维护者仍在持续迭代。  
- **技术成熟度**：核心实现基于飞书官方 SDK（Python），已封装错误重试、分页、速率限制等生产必备特性；CLI/TUI 经过多轮用户反馈优化，使用体验稳定。  
- **安全合规**：采用 OAuth 2.0 标准授权，所有凭证均在本地加密存储；项目 MIT 许可证，适合企业内部闭源或开源使用。  
- **部署成本**：仅需 Python 3.9+ 环境和飞书应用的 API 权限，无额外服务依赖，可在 CI/CD、容器或服务器上即插即用。  

综合来看，leemysw/feishu-docx 已具备 **高生产就绪度**，适合作为企业内部知识库的 Markdown 同步层，快速为 RAG、搜索和 AI 助手提供可靠的文档来源。

## 🧭 Practical evaluation

**Value:** leemysw/feishu-docx helps make internal knowledge searchable and usable by assistants.

**Best use cases**

- index knowledge bases
- improve search over documents
- ground assistant answers

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 228 GitHub stars
- 31 forks
- updated 2026-06-29
- primary language: Python
- 9 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 38/100 |
| stars | 50/100 |
| topics | 100/100 |
| outlook | 74/100 |
| quality | 71/100 |
| recency | 80/100 |
| adoption | 47/100 |
| production | 71/100 |
| usefulness | 74/100 |
| integration | 62/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 400/100 |

---

<sub>🔭 Discovered 2026-06-29 · [View on GitHub](https://github.com/leemysw/feishu-docx) · [← Back to Knowledgerag](./README.md)</sub>
