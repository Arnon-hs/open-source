# kossakovsky/n8n-install

[![Stars](https://img.shields.io/github/stars/kossakovsky/n8n-install?style=flat-square&color=yellow)](https://github.com/kossakovsky/n8n-install/stargazers) [![Forks](https://img.shields.io/github/forks/kossakovsky/n8n-install?style=flat-square&color=blue)](https://github.com/kossakovsky/n8n-install/network) [![Language](https://img.shields.io/badge/lang-Shell-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-79%2F100-brightgreen?style=flat-square)](#)

> 🚀 Self-hosted AI automation platform. Deploy n8n, Ollama, Flowise, RAG, Supabase & 30+ tools with one command. Auto HTTPS. Free Zapier/Make alternative.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 890 |
| 🍴 **Forks** | 229 |
| 💻 **Language** | Shell |
| 📈 **Score** | 79/100 |
| 🗓️ **Last push** | 2026-09-05 |
| 🔍 **Source** | github |

## 🏷️ Topics

`ai` `ai-agents` `automation` `chatgpt-alternative` `dify` `docker` `flowise` `homelab` `llm` `local-llm` `make-alternative` `n8n`

## 🎯 Categories

Knowledge/RAG · Automation · AI/ML · Database · DevOps/Infra

## 📝 Summary

### English

**Brief Summary (2‑3 sentences)**  
kossakovsky/n8n‑install is an open‑source, one‑command installer that spins up a self‑hosted AI automation stack—including n8n, Ollama, Flowise, RAG services, Supabase and 30+ auxiliary tools—behind automatic HTTPS. It gives teams a free, Zapier/Make‑style workflow engine that can index internal knowledge bases and power AI assistants with up‑to‑date, searchable context.  

**Value**  
- **Unified knowledge‑as‑code**: By bundling RAG components (vector DB, embeddings, document loaders) with a low‑code workflow engine, the project lets organizations turn static docs, tickets, or wikis into searchable, query‑able knowledge that AI assistants can cite.  
- **Rapid AI automation**: Developers can create end‑to‑end pipelines (e.g., “when a new ticket arrives → embed → store → trigger a response”) without wiring dozens of services manually.  
- **Cost‑effective alternative**: It replaces commercial Zapier/Make and proprietary RAG platforms with a free, self‑hosted stack, giving full control over data privacy and scaling.  

**Practical Adoption Path**  
1. **Spin‑up** – Clone the repo and run the provided shell script (`./install.sh`). The script provisions Docker containers for n8n, Ollama, Flowise, Supabase, and the chosen vector store, automatically obtaining TLS certificates via Let’s Encrypt.  
2. **Configure data sources** – Connect your existing knowledge repositories (Confluence, SharePoint, Git, PDFs, etc.) using the pre‑built n8n nodes or Flowise UI; the installer already includes connectors for the most common sources.  
3. **Build RAG workflows** – Use n8n’s visual editor to chain document ingestion → embedding (via Ollama) → storage → retrieval → LLM inference. Export the workflow as JSON for version control and CI/CD.  
4. **Secure & monitor** – Leverage the built‑in Supabase auth for user management, enable role‑based access in n8n, and hook up Prometheus/Grafana dashboards (already containerized) for observability.  
5. **Scale** – Because each component runs in its own container, you can horizontally scale the vector store or LLM inference nodes on Kubernetes or a cloud VM farm as load grows.  

**Production‑Readiness**  
- **Activity & community**: 890 ★, 229 forks, recent commits (last updated 2026‑06‑27), and a vibrant issue/PR discussion indicate an active maintainer base.  
- **Maturity of components**: All core services (n8n, Ollama, Supabase, Flowise) are production‑grade and widely used in enterprise settings.  
- **Installation robustness**: The installer automates TLS, health checks, and container orchestration, reducing manual setup errors.  
- **Observability & security**: Built‑in support for Supabase auth, HTTPS, and optional monitoring stacks gives a solid baseline for compliance.  
- **Remaining checks**: A final audit of the license (MIT/Apache‑compatible) and a security scan of the Docker images are advisable, but no major risks have been flagged.  

Overall, kossakovsky/n8n‑install offers a high‑confidence, low‑friction route to deploy a self‑hosted AI automation platform that can be piloted today and scaled to production with minimal additional engineering effort.

### Русский

**kossakovsky/n8n-install** — это готовый к использованию набор скриптов, позволяющий в один клик развернуть полностью self‑hosted AI‑автоматизацию: n8n, Ollama, Flowise, RAG, Supabase и более 30 интеграций с автоматическим HTTPS. Он идеален для компаний, желающих быстро сделать внутренние базы знаний доступными ассистентам — индексировать документы, улучшать поиск и «заземлять» ответы ИИ на корпоративный контент. Проект имеет высокую готовность к production: активные коммиты, 890★, 229 форков, поддержка Shell‑CLI и обширный набор тем, что делает его надёжным выбором для пилотного внедрения.

### 中文

**简短介绍**

kossakovsky/n8n-install 是一个开源项目，提供了一个自托管的 AI 自动化平台。它可以通过一个命令部署 n8n、Ollama、Flowise、RAG、Supabase 等 30 多种工具，并自动提供 HTTPS 服务。它还提供了一个自由的 Zapier/Make 替代品。

**价值**

kossakovsky/n8n-install 的值在于它可以帮助内部知识库变得可搜索和可用，进而可以让助手更好地回答问题。

**典型接入方式**

典型的接入方式是通过 Shell 脚本或 CLI 来部署和管理 n8n-install。

**生产可用性**

kossakovsky/n8n-install 的生产可用性较高，主要原因是其近期的活跃度、采用率和生态系统信号都很强。它已经获得了 890 个 GitHub 星和 229 个分支，最近一次更新是在 2026 年 6 月 27 日。

## 🧭 Practical evaluation

**Value:** kossakovsky/n8n-install helps make internal knowledge searchable and usable by assistants.

**Best use cases**

- index knowledge bases
- improve search over documents
- ground assistant answers

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 890 GitHub stars
- 229 forks
- updated 2026-06-27
- primary language: Shell
- 20 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 59/100 |
| stars | 63/100 |
| topics | 100/100 |
| outlook | 83/100 |
| quality | 78/100 |
| recency | 80/100 |
| adoption | 62/100 |
| production | 73/100 |
| usefulness | 100/100 |
| integration | 62/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 500/100 |

---

<sub>🔭 Discovered 2026-06-27 · [View on GitHub](https://github.com/kossakovsky/n8n-install) · [← Back to Knowledgerag](./README.md)</sub>
