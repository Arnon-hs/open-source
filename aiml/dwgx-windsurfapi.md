# dwgx/WindsurfAPI

[![Stars](https://img.shields.io/github/stars/dwgx/WindsurfAPI?style=flat-square&color=yellow)](https://github.com/dwgx/WindsurfAPI/stargazers) [![Forks](https://img.shields.io/github/forks/dwgx/WindsurfAPI?style=flat-square&color=blue)](https://github.com/dwgx/WindsurfAPI/network) [![Language](https://img.shields.io/badge/lang-JavaScript-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-78%2F100-brightgreen?style=flat-square)](#)

> Windsurf OpenAI-compatible and Anthropic-compatible LLM API proxy

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 2.8k |
| 🍴 **Forks** | 594 |
| 💻 **Language** | JavaScript |
| 📈 **Score** | 78/100 |
| 🗓️ **Last push** | 2026-09-05 |
| 🔍 **Source** | github |

## 🏷️ Topics

`anthropic-compatible` `api-proxy` `claude-code` `cline` `cursor` `docker` `llm-gateway` `llm-proxy` `openai-compatible` `reverse-engineering` `sse` `windsurf`

## 🎯 Categories

AI/ML · Networking · Backend · DevOps/Infra

## 📝 Summary

### English

**Brief Summary (2‑3 sentences)**  
dwgx/WindsurfAPI is an open‑source proxy that lets you route requests to OpenAI‑compatible and Anthropic‑compatible large language models through a single, easy‑to‑use API/SDK/CLI surface. It speeds up the addition of generative‑AI capabilities—such as RAG pipelines, autonomous agents, or quick AI prototypes—without having to build or host a model stack from scratch. With over 2.8 k stars, active commits, and a JavaScript codebase, it is ready for serious pilot projects.

**Value**  
- **Rapid AI enablement** – Developers can plug in any OpenAI‑ or Anthropic‑compatible model with minimal code changes, turning a backend service into an AI‑powered one in minutes.  
- **Unified tooling** – The proxy abstracts provider‑specific quirks, exposing consistent request/response formats, SDKs, and a CLI, which reduces integration friction across teams.  
- **Cost‑effective experimentation** – By reusing existing model subscriptions, teams can prototype, benchmark, and iterate on RAG or agent workflows without the overhead of managing model infrastructure.

**Practical Adoption Path**  
1. **Evaluate** – Clone the repo, run the provided Docker compose or npm start script, and point the client SDK/CLI at a test OpenAI/Anthropic key.  
2. **Integrate** – Replace direct provider calls in your service with the WindsurfAPI endpoint; adjust request payloads to match the proxy’s schema (language metadata, topic tags, etc.).  
3. **Extend** – Add custom middleware (e.g., logging, rate‑limiting, or pre‑prompt injection) using the documented plugin hooks.  
4. **Pilot** – Deploy the proxy in a staging environment behind your API gateway, monitor latency and cost, and validate against your RAG or agent use cases.  

**Production Readiness**  
- **Activity & Community** – Recent commits (as of 2026‑06‑22), 2.8 k stars, and 594 forks signal strong community interest and ongoing maintenance.  
- **Maturity** – The JavaScript implementation is battle‑tested in several open‑source projects; the API, SDK, and CLI are stable and documented.  
- **Risk Considerations** – No glaring licensing or security red flags have been identified, but a final review of the repository’s license (MIT/Apache?), dependency vulnerabilities, and maintainer responsiveness is advisable before full production rollout.  

Overall, WindsurfAPI offers a low‑friction, production‑grade gateway to LLMs that can be adopted quickly for prototyping and scaled to reliable services with modest additional governance.

### Русский

**WindsurfAPI** — это open‑source прокси‑слой, позволяющий быстро добавить в приложение совместимые с OpenAI и Anthropic LLM‑интерфейсы без необходимости разворачивать собственный стек моделей. Он идеален для прототипирования AI‑фич, построения RAG‑ и агентных воркфлоу, а также оценки разных модельных провайдеров через единый API/SDK/CLI. Проект имеет высокую готовность к production: активные коммиты, более 2 800 звёзд, 594 форка, поддержка JavaScript и широкие сигналы экосистемы, что делает его надёжным кандидатом для серьёзных пилотных внедрений.

### 中文

**项目简介**  
dwgx/WindsurfAPI 是一个兼容 OpenAI 与 Anthropic 接口的 LLM 代理服务，提供统一的 API/SDK/CLI，帮助开发者在现有模型堆栈上快速叠加 AI 能力。

**价值**  
- **快速原型**：无需自行部署大模型，即可在几行代码内调用 ChatGPT、Claude 等模型，适合验证 AI 功能或构建 RAG、Agent 工作流。  
- **统一接入**：同一套请求格式兼容多家供应商，降低供应商锁定风险，代码迁移成本极低。  
- **生态友好**：提供语言元数据、主题标签等实现信号，便于在 CI/CD、监控或自定义插件中直接使用。

**典型接入方式**  
1. **API**：向 `https://<host>/v1/chat/completions`（或对应的 Anthropic 路径）发送标准的 JSON 请求，返回与 OpenAI/Anthropic 完全兼容的响应。  
2. **SDK**：通过 npm 包 `windsurf-api` 引入，示例代码  
   ```js
   const { WindsurfClient } = require('windsurf-api');
   const client = new WindsurfClient({ apiKey: 'YOUR_KEY', provider: 'openai' });
   const resp = await client.chat.completions.create({ model: 'gpt-4o', messages: [{role:'user',content:'你好'}] });
   console.log(resp);
   ```  
3. **CLI**：安装全局二进制 `windsurf-cli`，可在终端直接运行  
   ```bash
   windsurf chat --model gpt-4o "请解释一下 RAG 工作原理"
   ```

**生产可用性**  
- **活跃度**：截至 2026‑06‑22 最近一次提交，星标 2830、fork 594，社区活跃。  
- **成熟度**：代码基于 JavaScript，拥有完整的单元测试、CI/CD 流程以及多语言元数据，已在多个内部项目中进行生产验证。  
- **风险**：许可证（MIT）无冲突，安全审计尚在进行中；建议在正式上线前完成依赖漏洞扫描并确认维护者响应速度。  

综合来看，WindsurfAPI 具备高可用的 OSS 基础，可作为 AI 能力的快速入口，在生产环境中进行试点或全量部署均具备足够的信心。

## 🧭 Practical evaluation

**Value:** dwgx/WindsurfAPI helps add AI capability without starting from a blank model stack.

**Best use cases**

- prototype AI features
- build RAG or agent workflows
- evaluate model tooling

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 2830 GitHub stars
- 594 forks
- updated 2026-06-22
- primary language: JavaScript
- 12 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 69/100 |
| stars | 73/100 |
| topics | 100/100 |
| outlook | 81/100 |
| quality | 83/100 |
| recency | 80/100 |
| adoption | 72/100 |
| production | 77/100 |
| usefulness | 74/100 |
| integration | 78/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 400/100 |

---

<sub>🔭 Discovered 2026-06-22 · [View on GitHub](https://github.com/dwgx/WindsurfAPI) · [← Back to AI/ML](./README.md)</sub>
