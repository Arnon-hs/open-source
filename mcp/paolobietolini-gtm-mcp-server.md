# paolobietolini/gtm-mcp-server

[![Stars](https://img.shields.io/github/stars/paolobietolini/gtm-mcp-server?style=flat-square&color=yellow)](https://github.com/paolobietolini/gtm-mcp-server/stargazers) [![Forks](https://img.shields.io/github/forks/paolobietolini/gtm-mcp-server?style=flat-square&color=blue)](https://github.com/paolobietolini/gtm-mcp-server/network) [![Language](https://img.shields.io/badge/lang-Go-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-73%2F100-brightgreen?style=flat-square)](#)

> An MCP server for Google Tag Manager. Connect it to your LLM, authenticate once, and start managing GTM through natural language.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 83 |
| 🍴 **Forks** | 18 |
| 💻 **Language** | Go |
| 📈 **Score** | 73/100 |
| 🗓️ **Last push** | 2026-05-12 |
| 🔍 **Source** | github |

## 🏷️ Topics

`ai` `chatgpt` `claude` `golang` `google-api` `google-tag-manager` `gtm` `llm` `mcp` `mcp-server` `model-context-protocol` `oauth2`

## 🎯 Categories

MCP · AI/ML · Backend · Security

## 📝 Summary

### English

**Brief Summary (2‑3 sentences)**  
paolobietolini/gtm‑mcp‑server is an open‑source Model‑Context‑Protocol (MCP) server that lets you control Google Tag Manager (GTM) with natural‑language prompts via any LLM. After a one‑time authentication step, the server exposes a simple API/CLI that AI agents can call to create, update, or query GTM containers, tags, triggers, and variables.  

**Value**  
- **Bridges the AI‑to‑tool gap**: By translating natural‑language intents into concrete GTM actions, the server enables conversational AI assistants to manage marketing tags without writing code.  
- **Standardized integration**: It implements the MCP spec, so the same server can be swapped with other MCP‑compatible tools, reducing vendor lock‑in and simplifying multi‑tool orchestration.  
- **Security‑first workflow**: Authentication is performed once, after which the server enforces scoped permissions, keeping GTM credentials safe while still permitting automated updates.  

**Practical Adoption Path**  
1. **Deploy the server** – Run the Go binary (Docker image is also provided) in your cloud or on‑prem environment.  
2. **Authenticate GTM** – Follow the built‑in OAuth flow to grant the server the required GTM scopes; the resulting token is stored securely.  
3. **Connect your LLM** – Configure your LLM (e.g., OpenAI, Anthropic) to use the server’s MCP endpoint as a tool plugin or via the provided SDK/CLI.  
4. **Define intents** – Map natural‑language commands (e.g., “Add a GA4 tag to the homepage”) to MCP calls; the server handles the translation to GTM’s REST API.  
5. **Iterate & monitor** – Use the server’s logs and optional webhook callbacks to audit changes and refine prompt handling.  

**Production Readiness**  
- **Activity & community**: 83 ★, 18 forks, recent commit (2026‑05‑12), and a Go codebase with clear module structure indicate an active project.  
- **Stability**: The MCP implementation is self‑contained, exposing a well‑documented HTTP/JSON interface; the Go runtime provides strong concurrency and low overhead.  
- **Security posture**: One‑time OAuth authentication isolates GTM credentials, and the repository follows standard Go security practices, though a formal security audit is still advisable.  
- **Ecosystem fit**: The server aligns with the growing MCP ecosystem, making it a drop‑in for any AI agent that already supports MCP.  

Overall, the project is mature enough for a pilot in a production environment, provided you perform a final license and security review and set up monitoring around the authentication token lifecycle.

### Русский

**paolobietolini/gtm-mcp-server** — это сервер Model Context Protocol (MCP) на Go, позволяющий подключить любой LLM к Google Tag Manager через единый протокол: после однократной аутентификации AI‑ассистент может читать, изменять и создавать теги GTM по естественным запросам. Типовой сценарий — развертывание сервера в контейнере (Docker/K8s), настройка OAuth‑токена GTM и интеграция LLM через MCP‑клиент, что дает возможность автоматизировать управление маркетинговыми тегами без написания кода. Проект считается готовым к production: активные коммиты (обновление 12‑05‑2026), 83 звёзды, 18 форков, хорошая документация и поддержка API/CLI, однако перед масштабным запуском рекомендуется проверить лицензию и провести аудит безопасности.

### 中文

**项目简介**  
paolobietolini/gtm-mcp-server 是一个基于 Model Context Protocol（MCP）的服务器，实现了对 Google Tag Manager（GTM）的自然语言控制。只需一次身份认证，即可将任意大语言模型（LLM）接入，使用自然语言指令创建、修改或查询 GTM 容器与标签。

**价值主张**  
- **统一协议**：通过 MCP 为 AI 助手提供标准化的工具接入层，降低不同 AI 与实际业务系统之间的集成成本。  
- **安全便捷**：一次性完成 OAuth/Service‑Account 认证后，后续所有操作均由模型发起，免去手工登录和 UI 操作。  
- **加速 AI‑ops**：让运营团队、营销人员或自动化脚本能够直接用自然语言管理 GTM，提升迭代速度和响应效率。

**典型接入方式**  
1. **部署服务器**：使用 Docker 镜像或直接 `go run` 启动，配置好 GTM 的 Service Account 凭证。  
2. **注册到 LLM**：在 OpenAI、Claude、Gemini 等模型的插件/工具库中注册该 MCP 端点（提供 OpenAPI 描述或 MCP schema）。  
3. **调用示例**  
   ```json
   {
     "action": "createTag",
     "containerId": "GTM-XXXXX",
     "tag": {
       "name": "GA4 Event",
       "type": "gtag",
       "parameters": { "event_name": "purchase" }
     }
   }
   ```
   LLM 生成上述请求后，MCP 服务器会转化为 GTM API 调用并返回结果。  

**生产可用性**  
- **活跃度**：截至 2026‑05‑12 最近一次提交，星标 83、fork 18，社区活跃，代码基于 Go，易于审计和容器化部署。  
- **安全性**：采用 Google 官方 OAuth / Service Account 进行身份验证，所有操作均在服务器端完成，避免凭证泄露。  
- **成熟度**：项目已具备完整的 API、CLI 示例和 SDK，文档覆盖常见使用场景，适合作为企业级 Pilot，进一步评估后可直接投入生产。  

综上，paolobietolini/gtm-mcp-server 为 AI 与 GTM 的深度集成提供了安全、标准且易于上线的解决方案，适合希望在营销自动化中引入自然语言交互的团队快速试点。

## 🧭 Practical evaluation

**Value:** paolobietolini/gtm-mcp-server helps connect AI assistants to real tools and data through a standard protocol.

**Best use cases**

- connect AI agents to tools
- ship Model Context Protocol servers
- standardize integrations

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 83 GitHub stars
- 18 forks
- updated 2026-05-12
- primary language: Go
- 12 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 32/100 |
| stars | 41/100 |
| topics | 100/100 |
| outlook | 79/100 |
| quality | 72/100 |
| recency | 100/100 |
| adoption | 38/100 |
| production | 78/100 |
| usefulness | 74/100 |
| integration | 78/100 |
| sourceTrust | 100/100 |

---

<sub>🔭 Discovered 2026-05-12 · [View on GitHub](https://github.com/paolobietolini/gtm-mcp-server) · [← Back to Mcp](./README.md)</sub>
