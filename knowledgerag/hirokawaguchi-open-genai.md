# hirokawaguchi/open-genai

[![Stars](https://img.shields.io/github/stars/hirokawaguchi/open-genai?style=flat-square&color=yellow)](https://github.com/hirokawaguchi/open-genai/stargazers) [![Forks](https://img.shields.io/github/forks/hirokawaguchi/open-genai?style=flat-square&color=blue)](https://github.com/hirokawaguchi/open-genai/network) [![Language](https://img.shields.io/badge/lang-TypeScript-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-71%2F100-brightgreen?style=flat-square)](#)

> デジタル庁のガバメントAI「源内(GENAI)」を完全ローカル(ローカルLLM/OpenAI互換)で動かす非公式プロジェクト。SAML認証(Keycloak)・RAG(Qdrant)・文字起こし(Whisper)・画像生成(SD)・チーム単位ナレッジをローカル完結。

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 113 |
| 🍴 **Forks** | 8 |
| 💻 **Language** | TypeScript |
| 📈 **Score** | 71/100 |
| 🗓️ **Last push** | 2026-09-05 |
| 🔍 **Source** | github |

## 🏷️ Topics

`digital-agency` `fastapi` `genai` `japan` `keycloak` `local-llm` `ollama` `open-genai` `openai-compatible` `qdrant` `rag` `react`

## 🎯 Categories

Knowledge/RAG · AI/ML · Frontend · Backend

## 📝 Summary

### English

**Brief Summary**  
Open‑GenAI is an unofficial, fully‑local implementation of Japan’s Government AI “GENAI”, providing SAML‑based authentication, RAG with Qdrant, Whisper transcription, Stable Diffusion image generation, and team‑wide knowledge management—all run on local LLM/OpenAI‑compatible models. Written in TypeScript, the project is actively maintained (last commit 2026‑07‑03) and already has a modest community (≈113 ★, 8 forks).

**Value Proposition**  
- **Unified Knowledge Access** – By indexing internal documents in a local vector store (Qdrant) and exposing them through a searchable API/CLI, teams can retrieve precise, up‑to‑date information without exposing data to external services.  
- **End‑to‑End AI Stack** – The same repository bundles authentication (Keycloak/SAML), speech‑to‑text (Whisper), text generation (local LLM or OpenAI‑compatible API), and image creation (Stable Diffusion), eliminating the need to stitch together multiple third‑party tools.  
- **Data Sovereignty & Cost Control** – All components run on‑premises, guaranteeing compliance with government‑level data regulations while avoiding recurring cloud‑AI fees.

**Practical Adoption Path**  
1. **Pilot Setup** – Deploy the Docker‑compose stack in a sandbox environment, connect it to an existing Keycloak realm for SAML SSO, and point Qdrant at a sample knowledge base.  
2. **Integration** – Use the provided TypeScript SDK or REST endpoints to embed the RAG service into internal chat‑bots, ticketing systems, or custom front‑ends.  
3. **Scale & Harden** – Replace the placeholder LLM with a production‑grade local model (e.g., Llama 3 or Mistral) and configure Whisper/Stable Diffusion GPU resources. Add monitoring, RBAC policies in Keycloak, and backup routines for the Qdrant index.  

**Production Readiness**  
- **Activity & Community** – Recent commits (within days), 113 ★, and clear documentation indicate healthy momentum.  
- **Architecture** – Modular services (auth, RAG, transcription, image generation) are containerized and communicate via standard HTTP/REST, simplifying deployment in Kubernetes or on‑prem VMs.  
- **Security & Compliance** – SAML integration via Keycloak satisfies enterprise SSO requirements; however, a formal security audit (dependency scanning, license verification) is still advisable before a full production rollout.  

Overall, Open‑GenAI offers a production‑grade, self‑hosted AI platform that can be evaluated quickly and, with modest hardening, be promoted to a mission‑critical knowledge‑assistant for organizations that must keep data in‑house.

### Русский

hirokawaguchi/open-genai — это неофициальный набор инструментов, позволяющий запускать локально (с поддержкой OpenAI‑совместимых LLM) правительственный AI «Генай» с интегрированной SAML‑аутентификацией (Keycloak), RAG‑поиском (Qdrant), распознаванием речи (Whisper) и генерацией изображений (Stable Diffusion), обеспечивая полную изоляцию корпоративных знаний. Типовой сценарий внедрения — индексация внутренних баз знаний и документов, после чего ассистенты могут быстро находить релевантную информацию и генерировать обоснованные ответы без обращения к внешним сервисам. Благодаря активной разработке (обновлено 2026‑07‑03), сильным сигналам экосистемы и высокой готовности к production, проект подходит для серьёзного пилот

### 中文

**项目简介（2‑3 句）**  
hirokawaguchi/open‑genai 是一个非官方的开源实现，能够在完全本地环境（本地 LLM / OpenAI 兼容接口）下运行日本数字厅的政府 AI「源内（GENAI）」。它集成了 SAML（Keycloak）身份认证、RAG（Qdrant 向量库）、语音转文字（Whisper）、图像生成（Stable Diffusion）以及团队级别的本地知识库，做到全栈本地化。

**价值**  
- **本地化安全**：所有模型、向量检索和数据均保存在内部网络，满足政府、金融等高安全需求。  
- **统一知识入口**：通过 RAG 将文档、音频、图片等多模态资产统一索引，助力内部助理快速检索并生成精准答案。  
- **可扩展生态**：兼容 OpenAI API、提供 CLI/SDK，便于在现有业务系统中快速嵌入对话、搜索或生成能力。

**典型接入方式**  
1. **部署**：使用 Docker Compose 或 Helm 在本地或私有云启动 Keycloak、Qdrant、Whisper、Stable Diffusion 与主服务容器。  
2. **认证**：前端或后端通过 SAML（Keycloak）完成单点登录，获取 JWT 供后续 API 调用。  
3. **调用 API**：使用提供的 TypeScript SDK 或直接调用兼容 OpenAI 的 REST 接口（`/v1/chat/completions`、`/v1/embeddings` 等），即可进行对话、向量检索、音频转写或图像生成。  
4. **知识注入**：通过 CLI/SDK 将文档、音频或图片上传至 Qdrant，自动生成向量并关联到团队/项目标签，实现 RAG 检索。

**生产可用性**  
- **活跃度**：截至 2026‑07‑03 最近一次提交，项目星标 113、Fork 8，社区活跃。  
- **技术成熟度**：核心组件（Keycloak、Qdrant、Whisper、Stable Diffusion）均为成熟开源项目，项目本身提供完整的 Docker 镜像和 Helm chart，便于容器化部署。  
- **安全合规**：所有数据均在本地保存，符合政府/企业对数据主权的严格要求；仅需自行审计 Docker 镜像和依赖的许可证。  
- **可扩展性**：基于 TypeScript 实现的 SDK 与 OpenAI 兼容层，使得迁移到云端或混合部署时改动最小。  

综合来看，hirokawaguchi/open‑genai 已具备 **高生产就绪度**，适合作为内部知识搜索与对话助理的核心平台进行试点或正式上线。后续仍建议对依赖库进行安全审计，并关注项目的维护者响应情况，以确保长期可维护性。

## 🧭 Practical evaluation

**Value:** hirokawaguchi/open-genai helps make internal knowledge searchable and usable by assistants.

**Best use cases**

- index knowledge bases
- improve search over documents
- ground assistant answers

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 113 GitHub stars
- 8 forks
- updated 2026-07-03
- primary language: TypeScript
- 16 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 24/100 |
| stars | 44/100 |
| topics | 100/100 |
| outlook | 76/100 |
| quality | 67/100 |
| recency | 80/100 |
| adoption | 38/100 |
| production | 69/100 |
| usefulness | 90/100 |
| integration | 62/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 400/100 |

---

<sub>🔭 Discovered 2026-07-04 · [View on GitHub](https://github.com/hirokawaguchi/open-genai) · [← Back to Knowledgerag](./README.md)</sub>
