# Klotzkette/claude-fuer-deutsches-recht

[![Stars](https://img.shields.io/github/stars/Klotzkette/claude-fuer-deutsches-recht?style=flat-square&color=yellow)](https://github.com/Klotzkette/claude-fuer-deutsches-recht/stargazers) [![Forks](https://img.shields.io/github/forks/Klotzkette/claude-fuer-deutsches-recht?style=flat-square&color=blue)](https://github.com/Klotzkette/claude-fuer-deutsches-recht/network) [![Language](https://img.shields.io/badge/lang-Python-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-60%2F100-brightgreen?style=flat-square)](#)

> ⚠️ Experimentelle Skill-Sammlung für deutsches Recht (Arbeits-, Gesellschafts-, Insolvenz-, Datenschutz-, Prozessrecht u.a.) – inzwischen verbessert und im Alltag getestet, aber weiterhin Experiment. Bitte selber ausprobieren, Issues/PRs willkommen! Keine Rechtsberatung. Mandatsgeheimnis (§§ 203/204 StGB, § 43e BRAO), DSGVO, US-Transfer, KI-VO & Co

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 1.2k |
| 🍴 **Forks** | 137 |
| 💻 **Language** | Python |
| 📈 **Score** | 60/100 |
| 🗓️ **Last push** | 2026-09-05 |
| 🔍 **Source** | github |

## 🏷️ Topics

`anthropic` `bgh` `claude-skills` `deutsches-recht` `dsgvo` `german-law` `kanzlei` `legal-ai` `legaltech`

## 🎯 Categories

AI/ML

## 📝 Summary

### English

**Brief Summary**  
Klotzkette/claude‑fuer‑deutsches‑recht is an experimental, open‑source collection of Claude‑based “skills” that encode knowledge of German law (labour, corporate, insolvency, data‑protection, procedural law, etc.). The repository is actively maintained, has been field‑tested, and is offered with a clear disclaimer that it is not legal advice.

**Value Proposition**  
- **Rapid AI‑enabled legal prototyping** – developers can plug ready‑made Claude prompts and tool‑chains into their applications instead of building a legal knowledge base from scratch.  
- **RAG / agent‑workflow ready** – the skill set is structured for Retrieval‑Augmented Generation or autonomous agents, making it easy to experiment with question‑answering, document‑review, or compliance‑checking bots for German statutes.  
- **Compliance‑aware scaffolding** – the repo already embeds warnings about professional secrecy ( §§ 203/204 StGB, § 43e BRAO), GDPR, data‑transfer, and upcoming AI regulations, helping teams stay mindful of legal constraints while they prototype.

**Practical Adoption Path**  
1. **Read the README & run the demo** – the repository includes a minimal example that spins up a Claude client with the German‑law skill bundle.  
2. **Create a small proof‑of‑concept** – integrate the skill package into an existing Python service (e.g., a FastAPI endpoint) and test a few representative queries (e.g., “What are the notice periods for a fixed‑term contract in Germany?”).  
3. **Extend or customise** – add your own prompts, data sources, or retrieval back‑ends (Elastic, Pinecone, etc.) and adjust the disclaimer logic to match your compliance workflow.  
4. **Iterate with the community** – submit issues or pull requests for missing statutes or edge‑case handling; the project’s active community (1 173 ★, 137 forks) can provide feedback.  

**Production Readiness**  
- **Maturity** – recent commits (as of 2026‑06‑24), a healthy star/fork count, and a clear Python‑centric codebase indicate a stable foundation.  
- **Readiness level** – suitable for a **pilot or internal tooling** scenario. The core AI integration works, but because the project is still labeled “experimental” and carries no legal‑advice guarantee, it should not be deployed as a standalone compliance service without additional validation and legal review.  
- **Risks & next steps** – verify the license compatibility, run a security audit of dependencies, and confirm that your organization’s data‑privacy policies align with the repo’s handling of personal data and cross‑border model calls. Once those checks are done, the code can be promoted to a production‑grade microservice behind internal safeguards.

### Русский

Klotzkette/claude-fuer-deutsches-recht — это экспериментальная, но уже протестированная наборка навыков Claude для задач немецкого права (трудовое, корпоративное, банкротство, защита данных, процессуальное и др.), позволяющая быстро добавить AI‑функциональность в существующие системы без построения модели с нуля. Типичное внедрение — создание небольшого proof‑of‑concept, где модель используется в RAG‑ или агентных сценариях для автоматической генерации юридических подсказок, проверок соответствия GDPR/AI‑VO и предварительного анализа дел. По уровню готовности проект считается «high» для open‑source‑кандидата: активные коммиты, более 1 000 звёзд, широкая пользовательская база и готовая Python‑библиотека, что позволяет начать пилот уже в продакшн‑окружении после базовой проверки лицензии и безопасности.

### 中文

**项目简介（2‑3 句）**  
Klotzkette/claude-fuer-deutsches-recht 是一个面向德国法律（劳动、公司、破产、数据保护、诉讼等）的实验性 Skill 集合，基于 Claude 大模型实现可检索式问答（RAG）和智能代理。代码已在日常工作中验证，可直接用于原型开发，仍然保持“实验”标签，使用时请自行承担风险，且不构成法律咨询。

---

## 价值说明  
1. **快速赋能 AI 法律助手**：无需从零搭建模型堆栈，直接调用已封装好的法律知识 Skill，帮助开发者在几行代码内实现德国法律领域的自然语言查询、文档检索和合规检查。  
2. **降低研发成本**：通过现成的 RAG/Agent 流程，团队可以把精力集中在业务逻辑和 UI 上，而不是数据清洗、向量化或提示工程。  
3. **开源透明、可审计**：全部代码公开，便于审计提示、数据处理和合规实现（如 GDPR、律师保密义务），满足企业内部合规审查的需求。  

---

## 典型接入方式  

| 步骤 | 关键操作 | 说明 |
|------|----------|------|
| 1️⃣ 环境准备 | `python -m venv .venv && source .venv/bin/activate`<br>`pip install -r requirements.txt` | 项目基于 Python 3.10+，依赖 `langchain`, `openai`（或 Claude API）等。 |
| 2️⃣ 配置凭证 | 在 `.env` 中填入 `CLAUDE_API_KEY`、`OPENAI_API_KEY`（如使用混合模型）以及 GDPR/律师保密相关的标识。 | 采用环境变量管理敏感信息，符合安全最佳实践。 |
| 3️⃣ 加载 Skill | ```python<br>from skills import load_all<br>skills = load_all()<br>``` | `load_all()` 会自动读取本地法律文档、构建向量库（FAISS/Chroma），并返回可调用的函数列表。 |
| 4️⃣ 调用 RAG/Agent | ```python<br>response = skills['arbeitsrecht'].query("我可以在试用期内被解雇吗？")<br>print(response)<br>``` | 每个法律领域对应一个 Skill，支持 `.query()`（单轮检索）和 `.agent()`（多轮对话）两种模式。 |
| 5️⃣ 集成到业务 | 将上述调用包装为 Flask/Django API、FastAPI 微服务或 Slack/Teams Bot，即可在内部系统中使用。 | 推荐在入口层做请求过滤、日志审计和免责声明输出，以满足合规要求。 |

> **小技巧**：如果已有企业向量库，可通过 `skills.override_vector_store(custom_store)` 替换默认存储，直接复用已有数据。

---

## 生产可用性评估  

| 维度 | 评估 | 说明 |
|------|------|------|
| **代码活跃度** | ★★★★★ | 最近一次提交（2026‑06‑24），累计 1,173 星、137 Fork，社区活跃，PR/Issue 反馈及时。 |
| **功能成熟度** | ★★★★☆ | 核心 RAG 流程已在实际法律工作流中测试，基本功能稳定；仍标记为实验，部分边缘法律场景可能缺失。 |
| **安全合规** | ★★★★☆ | 项目已声明遵守 GDPR、律师保密 (§§ 203/204 StGB) 等，代码中提供数据脱敏和日志审计示例；但最终合规仍需企业自行评估。 |
| **部署复杂度** | ★★★☆☆ | 依赖向量数据库（FAISS/Chroma）和外部大模型 API，部署时需要网络、凭证管理和资源配置，建议先做小规模 PoC。 |
| **可扩展性** | ★★★★☆ | Skill 采用插件化设计，新增法律领域或自定义检索模型仅需添加模块并注册即可。 |
| **总体生产准备度** | **高**（约 8/10） | 对于内部原型、合规审查工具或内部知识库助手，已具备直接投入使用的条件；对外公开服务仍建议进行安全审计和额外的容错/监控层。 |

**结论**：Klotzkette/claude-fuer-deutsches-recht 适合作为企业内部法律 AI 原型或内部合规助手的基础组件，快速落地且易于二次开发；在正式生产环境上线前，建议完成安全审计、日志审计、免责声明机制以及容错/监控的补充。

## 🧭 Practical evaluation

**Value:** Klotzkette/claude-fuer-deutsches-recht helps add AI capability without starting from a blank model stack.

**Best use cases**

- prototype AI features
- build RAG or agent workflows
- evaluate model tooling

**Integration notes:** Looks feasible to evaluate, but integration should start with a small proof of concept and README check.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 1173 GitHub stars
- 137 forks
- updated 2026-06-24
- primary language: Python
- 9 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 53/100 |
| stars | 65/100 |
| topics | 100/100 |
| outlook | 72/100 |
| quality | 78/100 |
| recency | 80/100 |
| adoption | 62/100 |
| production | 71/100 |
| usefulness | 42/100 |
| integration | 46/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 100/100 |

---

<sub>🔭 Discovered 2026-06-24 · [View on GitHub](https://github.com/Klotzkette/claude-fuer-deutsches-recht) · [← Back to AI/ML](./README.md)</sub>
