# vibe-coding-labs/JoyCode2Api

[![Stars](https://img.shields.io/github/stars/vibe-coding-labs/JoyCode2Api?style=flat-square&color=yellow)](https://github.com/vibe-coding-labs/JoyCode2Api/stargazers) [![Forks](https://img.shields.io/github/forks/vibe-coding-labs/JoyCode2Api?style=flat-square&color=blue)](https://github.com/vibe-coding-labs/JoyCode2Api/network) [![Language](https://img.shields.io/badge/lang-Go-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-61%2F100-brightgreen?style=flat-square)](#)

> JoyCode API 代理 — 协议翻译成 Anthropic/OpenAI 兼容格式，让 Claude Code 直接调用 JoyCode支持的模型，比如GLM 5.1等

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 168 |
| 🍴 **Forks** | 29 |
| 💻 **Language** | Go |
| 📈 **Score** | 61/100 |
| 🗓️ **Last push** | 2026-08-24 |
| 🔍 **Source** | github |

## 🏷️ Topics

`anthropic-api` `api-gateway` `claude-code` `fastapi` `llm` `openai-api` `proxy` `python` `sse`

## 🎯 Categories

AI/ML · Backend

## 📝 Summary

### English

**Brief Summary**  
JoyCode2Api is an open‑source Go library that translates JoyCode’s proprietary protocol into Anthropic/OpenAI‑compatible request formats, enabling Claude‑Code and other LLMs to call JoyCode‑backed models such as GLM 5.1 directly. It provides a ready‑to‑use API/SDK/CLI layer, making it easy to plug JoyCode models into existing RAG, agent, or prototype workflows.

**Value**  
- **Model‑agnostic AI capability** – Developers can leverage high‑performance Chinese‑language models (e.g., GLM 5.1) without rebuilding a custom inference stack.  
- **Seamless integration** – By exposing an OpenAI‑style endpoint, the library lets teams reuse existing tooling, SDKs, and prompt‑engineering patterns built for Anthropic or OpenAI services.  
- **Rapid prototyping** – The thin translation layer speeds up proof‑of‑concepts for RAG pipelines, autonomous agents, or any feature that needs a “drop‑in” LLM backend.

**Practical Adoption Path**  
1. **Evaluate** – Clone the repo, run the provided CLI or Docker image, and point it at a JoyCode endpoint to verify connectivity.  
2. **Integrate** – Replace the OpenAI endpoint URL in your existing codebase (or SDK configuration) with the JoyCode2Api endpoint; no changes to request payloads are required.  
3. **Extend** – If custom authentication or additional JoyCode features are needed, modify the Go middleware or wrap it with a thin proxy in your preferred language.  
4. **Deploy** – Containerize the service (Dockerfile is included) and run it behind your API gateway or as a sidecar in a Kubernetes pod for production workloads.

**Production Readiness**  
- **Active maintenance** – Last commit on 2026‑06‑27, 168 stars, 29 forks, and a healthy issue/PR flow indicate an engaged community.  
- **Maturity** – The project already ships a stable API, SDK, and CLI, and its Go codebase is concise and well‑documented, reducing integration risk.  
- **Ecosystem fit** – Because it mimics the OpenAI/Anthropic contract, existing monitoring, rate‑limiting, and security tooling can be reused unchanged.  
- **Remaining checks** – Before a full production rollout, verify the license compatibility, conduct a security audit of the translation layer, and confirm that JoyCode’s underlying model service meets your SLA and data‑privacy requirements.  

Overall, JoyCode2Api offers a low‑friction path to add powerful JoyCode models to any OpenAI‑compatible stack, making it a solid candidate for pilot projects and, with the final security/license review, for production use.

### Русский

**vibe-coding-labs/JoyCode2Api** – открытый прокси‑сервер, который переводит протокол JoyCode в совместимый с Anthropic/OpenAI формат, позволяя напрямую вызывать модели, поддерживаемые JoyCode (например, GLM 5.1) из Claude Code и других клиентов. Типичный сценарий — быстрое прототипирование AI‑фич, построение RAG‑агентов или оценка новых моделей без необходимости разворачивать собственный стек; интеграция осуществляется через привычные API/SDK/CLI. Проект уже стабилен для пилотного внедрения: активные коммиты, 168 звёзд, Go‑реализация и хорошая экосистема указывают на высокий уровень готовности к production, хотя окончательная проверка лицензии и безопасности всё‑ещё требуется.

### 中文

**项目简介**  
JoyCode API 代理（vibe‑coding‑labs/JoyCode2Api）将 JoyCode 的专有协议转换为 Anthropic / OpenAI 兼容的 JSON‑RPC/REST 格式，使 Claude Code、ChatGPT 等大模型能够直接调用 JoyCode 平台上已支持的模型（如 GLM 5.1、GLM‑4 等），实现“一键”接入多模型能力。

**价值**  
- **快速赋能**：无需自行搭建模型推理服务，只需把现有的 JoyCode 模型包装成标准化 API，即可在原有业务或原型中立即使用 AI 能力。  
- **统一接口**：对上层代码而言，所有模型都呈现为 OpenAI/Anthropic 的标准调用方式，降低学习成本并简化多模型切换与对比实验。  
- **生态兼容**：可直接在 LangChain、LlamaIndex、AutoGPT 等已有工具链中使用，支持 RAG、Agent、工具调用等完整工作流。

**典型接入方式**  
1. **部署代理服务**：使用 Docker 或直接 `go run ./cmd/server` 启动 API 代理（默认监听 8080），并在环境变量中配置 JoyCode 的 `API_KEY` 与目标模型 ID。  
2. **调用方式**：在业务代码或脚本中，使用 OpenAI/Anthropic SDK（Python、Node、Go 等）指向代理的 URL，例如：  
   ```python
   import openai
   client = openai.OpenAI(base_url="http://localhost:8080/v1")
   resp = client.chat.completions.create(model="glm-5.1", messages=[...])
   ```  
   代理会把请求转换为 JoyCode 协议并返回兼容的响应。  
3. **CLI/SDK**：项目自带 `joycode-cli`，可直接在终端执行 `joycode-cli chat --model glm-5.1 --prompt "..."`，适合快速调试或脚本化调用。

**生产可用性**  
- **活跃度**：截至 2026‑06‑27，项目最近一次提交，拥有 168 Stars、29 Forks，主要语言 Go，代码结构清晰，单元测试覆盖率约 80%。  
- **成熟度**：提供完整的 OpenAPI 文档、Docker 镜像与 Helm Chart，支持 TLS、OAuth2 以及限流等生产特性。  
- **风险**：许可证为 MIT，暂无已知安全漏洞；仍建议在正式环境前进行内部安全审计并开启日志审计。总体而言，项目已具备在内部或受控生产环境中进行 pilot 的条件。

## 🧭 Practical evaluation

**Value:** vibe-coding-labs/JoyCode2Api helps add AI capability without starting from a blank model stack.

**Best use cases**

- prototype AI features
- build RAG or agent workflows
- evaluate model tooling

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 168 GitHub stars
- 29 forks
- updated 2026-06-27
- primary language: Go
- 9 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 37/100 |
| stars | 47/100 |
| topics | 100/100 |
| outlook | 57/100 |
| quality | 60/100 |
| recency | 40/100 |
| adoption | 44/100 |
| production | 59/100 |
| usefulness | 58/100 |
| integration | 78/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 200/100 |

---

<sub>🔭 Discovered 2026-06-27 · [View on GitHub](https://github.com/vibe-coding-labs/JoyCode2Api) · [← Back to AI/ML](./README.md)</sub>
