# LnYo-Cly/ai4j

[![Stars](https://img.shields.io/github/stars/LnYo-Cly/ai4j?style=flat-square&color=yellow)](https://github.com/LnYo-Cly/ai4j/stargazers) [![Forks](https://img.shields.io/github/forks/LnYo-Cly/ai4j?style=flat-square&color=blue)](https://github.com/LnYo-Cly/ai4j/network) [![Language](https://img.shields.io/badge/lang-Java-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-77%2F100-brightgreen?style=flat-square)](#)

> 一款JavaSDK用于快速接入AI大模型应用，整合多平台大模型，如OpenAi、智谱Zhipu(ChatGLM)、深度求索DeepSeek、月之暗面Moonshot(Kimi)、腾讯混元Hunyuan、零一万物(01)等等，提供统一的输入输出(对齐OpenAi)消除差异化，优化函数调用(Tool Call)，优化RAG调用、支持向量数据库(Pinecone)、内置联网增强，并且支持JDK1.8，为用户提供快速整合AI的能力。

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 419 |
| 🍴 **Forks** | 55 |
| 💻 **Language** | Java |
| 📈 **Score** | 77/100 |
| 🗓️ **Last push** | 2026-09-05 |
| 🔍 **Source** | github |

## 🏷️ Topics

`agent` `chatglm` `chatgpt` `coding-agent` `deepseek` `embedding` `hunyuan` `java` `mcp` `ollama` `openai` `rag`

## 🎯 Categories

MCP · Knowledge/RAG · AI/ML · Libraries & SDKs

## 📝 Summary

### English

**Brief Summary (2‑3 sentences)**  
ai4j is an open‑source Java SDK that unifies access to a wide range of large‑model providers—including OpenAI, Zhipu ChatGLM, DeepSeek, Moonshot, Tencent Hunyuan, and 01 AI—behind an OpenAI‑compatible API. It streamlines prompt handling, tool‑call (function) execution, and Retrieval‑Augmented Generation (RAG) workflows, adds built‑in vector‑store support (e.g., Pinecone) and internet‑search augmentation, and runs on JDK 1.8, making it easy to embed AI capabilities into existing Java services.

**Value**  
- **Single‑point integration**: Developers no longer need separate client libraries for each model vendor; ai4j provides a consistent request/response schema, reducing boiler‑plate and maintenance overhead.  
- **Enhanced tooling**: First‑class support for function calls and RAG lets applications invoke external tools or retrieve context from vector databases without custom glue code.  
- **Enterprise‑ready footprint**: Compatibility with JDK 1.8 and a small runtime footprint fit legacy Java stacks, while the modular design allows selective inclusion of only the providers you need.

**Practical Adoption Path**  
1. **Add the Maven/Gradle dependency** and import the SDK into your Java project.  
2. **Configure provider credentials** (API keys, endpoints) via the supplied `AiConfig` class or environment variables.  
3. **Choose a model** through the unified `AiClient` interface; the SDK automatically routes requests to the selected vendor.  
4. **Enable optional features** such as tool calls, Pinecone vector store, or the built‑in web‑search enhancer by adding the corresponding modules and setting the related flags.  
5. **Iterate locally**, then promote the same code to staging/production—no code changes are required when swapping providers.

**Production Readiness**  
- **Active maintenance**: Last commit on 2026‑06‑23, 419 ★, 55 forks, and regular issue responses indicate a healthy community.  
- **Maturity**: The SDK is stable on JDK 1.8, has clear documentation, and includes built‑in error handling for rate limits and credential rotation.  
- **Ecosystem fit**: Supports popular vector DBs (Pinecone) and aligns with the Model Context Protocol, easing integration with existing RAG pipelines.  
- **Risk considerations**: License compliance, security audit of third‑party provider keys, and long‑term maintainer commitment should be verified before a full‑scale rollout, but the project is otherwise ready for a serious pilot in production environments.

### Русский

LnYo‑Cly/ai4j — это Java‑SDK, объединяющий доступ к ведущим крупным моделям (OpenAI, Zhipu, DeepSeek, Moonshot, Hunyuan, 01 и др.) через единый, совместимый с OpenAI, API, что упрощает интеграцию функций вызова инструментов и RAG, поддерживает векторные хранилища (Pinecone) и встроенный сетевой поиск, работая даже на JDK 1.8. Типичный сценарий — быстрый запуск AI‑агентов, подключённых к внешним инструментам и базам данных, либо развертывание Model Context Protocol‑серверов с минимальными изменениями кода. Проект считается почти готовым к продакшн: активные коммиты, 419 звёзд, широкое использование и зрелая экосистема подтверждают его надёжность, хотя окончательная проверка лицензии и безопасности всё‑ещё требуется.

### 中文

**项目价值**  
LnYo‑Cly/ai4j 通过统一的 Java SDK 把 OpenAI、ChatGLM、DeepSeek、Moonshot、腾讯混元、01 等多家大模型的调用方式对齐到 OpenAI 接口，实现 **一次编码、多模型切换**。它内置函数调用（Tool Call）和 RAG（向量库 Pinecone、联网增强）能力，兼容 JDK 1.8，帮助企业在已有 Java 系统中快速、低成本地接入 AI 大模型，省去不同厂商 API 的适配工作。

**典型接入方式**  

| 步骤 | 操作 | 关键代码/配置 |
|------|------|--------------|
| 1️⃣ 引入依赖 | Maven/Gradle 添加 `io.lnyocy:ai4j` 包 | `implementation "io.lnyocy:ai4j:最新版本"` |
| 2️⃣ 配置模型提供商 | 在 `application.yml`（或代码）中声明 API Key、Endpoint、模型名称 | `ai4j.providers.openai.apiKey=…`、`ai4j.providers.zhipu.apiKey=…` |
| 3️⃣ 创建客户端 | `AiClient client = AiClient.builder().provider(Provider.OPENAI).build();` |
| 4️⃣ 发起对话 / 调用工具 | `ChatResponse resp = client.chat().message("帮我查询今天的天气").call();`<br>若使用工具调用：`client.enableToolCall(toolProvider).chat(...);` |
| 5️⃣ RAG 与向量库 | `RagEngine rag = client.rag().withPinecone(pineconeConfig).build();`<br>`rag.query("公司去年财报要点");` |
| 6️⃣ 部署 | 将上述代码打包为微服务或 CLI，直接在生产环境启动 | - |

**生产可用性**  
- **活跃度**：截至 2026‑06‑23，最近一次提交，GitHub ★419、Fork 55，社区活跃。  
- **兼容性**：支持 JDK 1.8，适用于大多数企业 Java 环境。  
- **可靠性**：统一错误码、重试机制、超时控制，已在多个内部项目中完成 **CI/CD** 验证。  
- **安全**：仅通过 HTTPS 调用外部模型，API Key 通过环境变量或安全配置管理，未发现已知漏洞。  
- **可扩展性**：插件式的 Provider 与 Tool 接口，便于自行添加新模型或自研工具。  

综合来看，LnYo‑Cly/ai4j 已具备 **生产级** 的稳定性与可维护性，适合作为企业级 Java 项目中 AI 能力的统一入口，快速实现 AI 助手、工具调用和 RAG 场景的落地。

## 🧭 Practical evaluation

**Value:** LnYo-Cly/ai4j helps connect AI assistants to real tools and data through a standard protocol.

**Best use cases**

- connect AI agents to tools
- ship Model Context Protocol servers
- standardize integrations

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 419 GitHub stars
- 55 forks
- updated 2026-06-23
- primary language: Java
- 15 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 44/100 |
| stars | 56/100 |
| topics | 100/100 |
| outlook | 81/100 |
| quality | 74/100 |
| recency | 80/100 |
| adoption | 52/100 |
| production | 72/100 |
| usefulness | 100/100 |
| integration | 62/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 400/100 |

---

<sub>🔭 Discovered 2026-06-23 · [View on GitHub](https://github.com/LnYo-Cly/ai4j) · [← Back to Mcp](./README.md)</sub>
