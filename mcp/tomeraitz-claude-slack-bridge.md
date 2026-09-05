# tomeraitz/claude-slack-bridge

[![Stars](https://img.shields.io/github/stars/tomeraitz/claude-slack-bridge?style=flat-square&color=yellow)](https://github.com/tomeraitz/claude-slack-bridge/stargazers) [![Forks](https://img.shields.io/github/forks/tomeraitz/claude-slack-bridge?style=flat-square&color=blue)](https://github.com/tomeraitz/claude-slack-bridge/network) [![Language](https://img.shields.io/badge/lang-Python-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-58%2F100-brightgreen?style=flat-square)](#)

> MCP server that lets Claude Code pause mid-task and ask a human a question via Slack — then resume once you reply.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 32 |
| 🍴 **Forks** | 14 |
| 💻 **Language** | Python |
| 📈 **Score** | 58/100 |
| 🗓️ **Last push** | 2026-09-05 |
| 🔍 **Source** | github |

## 🏷️ Topics

`mcp` `mcp-server` `slack` `slack-bot`

## 🎯 Categories

MCP · Automation · Communication · Backend

## 📝 Summary

### English

**Brief Summary (2‑3 sentences)**  
tomeraitz/claude‑slack‑bridge is a lightweight MCP (Model Context Protocol) server that lets Claude Code pause its execution, post a clarification question to a Slack channel, and resume once a human replies. By bridging Claude’s reasoning loop with Slack’s real‑time messaging, it enables interactive, human‑in‑the‑loop AI workflows without custom webhook plumbing.

**Value**  
- **Human‑in‑the‑loop control:** AI agents can defer to experts for ambiguous or risky decisions, improving safety and correctness.  
- **Standardized integration:** Implements the Model Context Protocol, making it easy to swap in other MCP‑compatible tools or replace Slack with another channel.  
- **Rapid prototyping:** A few lines of Python configure the bridge, allowing teams to experiment with “ask‑when‑uncertain” patterns in minutes.

**Practical Adoption Path**  
1. **Prototype:** Clone the repo, install the Python dependencies, and run the server locally. Configure a Slack app with a bot token and channel ID, then point Claude Code’s MCP endpoint to the bridge URL.  
2. **Validate:** Run a few Claude tasks that intentionally trigger a pause (e.g., ambiguous code generation) and verify that the Slack message appears and that the response correctly resumes the task.  
3. **Integrate:** Containerize the bridge (Dockerfile is provided), add it to your CI/CD pipeline, and expose the MCP endpoint behind your internal API gateway.  
4. **Scale:** If needed, deploy multiple instances behind a load balancer and configure Slack’s event subscription to route messages to the appropriate instance (correlation IDs are included in the payload).

**Production Readiness**  
- **Maturity:** Medium. The project is actively maintained (last commit 2026‑06‑26), has 32 ★ and 14 forks, and is written in Python, which eases integration with existing back‑ends.  
- **Suitability:** Ideal for prototypes, internal tools, or low‑to‑moderate volume workflows where human oversight is expected.  
- **Considerations before production:**  
  * Review the MIT/Apache license (as listed in the repo) for compatibility with your stack.  
  * Perform a security audit of the Slack bot token handling and any exposed MCP endpoints.  
  * Assess dependency health (e.g., Flask, Slack SDK) and set up automated vulnerability scanning.  
  * Implement monitoring and retry logic for message delivery failures.  

With these steps, the bridge can move from a sandbox experiment to a reliable component in production AI pipelines.

### Русский

**tomeraitz/claude‑slack‑bridge** — это MCP‑сервер, позволяющий AI‑ассистенту Claude приостанавливать выполнение кода, задавать уточняющий вопрос в Slack и автоматически продолжать после получения ответа. Он упрощает интеграцию AI‑агентов с реальными инструментами и данными, делая возможным быстрый прототипинг и внутренние рабочие процессы, однако требует проверки зависимостей, лицензии и безопасности перед запуском в продакшн. В целом готовность — средняя: проект подходит для пилотных внедрений, но нуждается в дополнительном аудите перед масштабным использованием.

### 中文

**项目简介（2‑3 句话）**  
tomeraitz/claude‑slack‑bridge 是一个实现 Model Context Protocol（MCP）的服务器，能够在 Claude Code 执行任务时暂停并通过 Slack 向人类提问，收到回复后再继续执行。它为 AI 助手提供了一个简单、统一的方式来与真实工具和数据交互。

**价值**  
- **人机协同**：在 AI 需要外部信息或确认时，自动转到 Slack 让人类介入，避免盲目推理。  
- **标准化集成**：基于 MCP，任何遵循该协议的模型或工具都可以直接使用，无需为每个平台单独实现聊天/回调逻辑。  
- **加速原型**：开发者只需部署该桥接服务，即可快速构建需要“人类在环”交互的 AI 工作流。

**典型接入方式**  
1. **部署 MCP 服务器**：使用 Docker 或直接在 Python 环境中运行 `claude_slack_bridge`，配置 Slack Bot Token 与签名密钥。  
2. **在 Claude Code（或其他支持 MCP 的模型）中声明 MCP 端点**：在模型的系统提示或配置文件里加入 `mcp://<host>:<port>/`。  
3. **Slack 侧**：将 Bot 加入目标工作区，授予 `chat:write`、`channels:history` 等权限，确保能够发送/接收消息。  
4. **调用流程**：模型发送 `ask_human` 请求 → Bridge 转发到指定 Slack 频道 → 人类回复 → Bridge 将答案回传模型，模型继续执行。

**生产可用性**  
- **成熟度**：目前评分 61/100，适合原型或内部工具。代码以 Python 实现，结构清晰，提供 API/CLI，易于集成。  
- **依赖与维护**：项目已有 32 星、14 Fork，最近一次提交在 2026‑06‑26，活跃度尚可。但仍需自行审查依赖的安全性（如 Flask、Slack SDK）并确认许可证兼容。  
- **上线建议**：在生产环境部署前，进行以下检查：  
  1. **安全审计**：确保 Slack Token 受限、通信使用 HTTPS。  
  2. **容错与监控**：为桥接服务添加健康检查、日志和重试机制。  
  3. **扩展性**：如并发需求较高，可考虑使用容器编排（K8s）或水平扩容。  

综上，tomeraitz/claude‑slack‑bridge 为 AI 与人类交互提供了一个轻量、标准化的桥梁，适合作为原型或内部流程的核心组件，经过适当的安全和运维加固后即可投入生产使用。

## 🧭 Practical evaluation

**Value:** tomeraitz/claude-slack-bridge helps connect AI assistants to real tools and data through a standard protocol.

**Best use cases**

- connect AI agents to tools
- ship Model Context Protocol servers
- standardize integrations

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** Medium: useful for prototypes or internal workflows, with dependency and maintenance checks before production.

**Quality signals**

- 32 GitHub stars
- 14 forks
- updated 2026-06-26
- primary language: Python
- 4 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 29/100 |
| stars | 32/100 |
| topics | 50/100 |
| outlook | 62/100 |
| quality | 57/100 |
| recency | 80/100 |
| adoption | 32/100 |
| production | 65/100 |
| usefulness | 58/100 |
| integration | 62/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 400/100 |

---

<sub>🔭 Discovered 2026-06-26 · [View on GitHub](https://github.com/tomeraitz/claude-slack-bridge) · [← Back to Mcp](./README.md)</sub>
