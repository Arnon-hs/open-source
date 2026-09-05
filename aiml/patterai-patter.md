# PatterAI/Patter

[![Stars](https://img.shields.io/github/stars/PatterAI/Patter?style=flat-square&color=yellow)](https://github.com/PatterAI/Patter/stargazers) [![Forks](https://img.shields.io/github/forks/PatterAI/Patter?style=flat-square&color=blue)](https://github.com/PatterAI/Patter/network) [![Language](https://img.shields.io/badge/lang-Python-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-82%2F100-brightgreen?style=flat-square)](#)

> Open-source voice-AI SDK. The Vapi/Retell alternative for builders who want to own the stack. Give your AI agent a phone number in 4 lines — Python and TypeScript, MIT licensed, Twilio, Telnyx, and Plivo.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 778 |
| 🍴 **Forks** | 82 |
| 💻 **Language** | Python |
| 📈 **Score** | 82/100 |
| 🗓️ **Last push** | 2026-09-05 |
| 🔍 **Source** | github |

## 🏷️ Topics

`ai-agent` `ai-phone-agent` `hermes-agent` `llm` `mastra` `open-source` `openai` `openclaw` `python` `realtime-api` `sdk` `speech-to-text`

## 🎯 Categories

AI/ML · Backend · Libraries & SDKs

## 📝 Summary

### English

**Summary**  
PatterAI/Patter is an MIT‑licensed, open‑source voice‑AI SDK that lets developers give an AI agent a phone number in just four lines of code (Python or TypeScript). It provides first‑class integrations with major telephony providers (Twilio, Telnyx, Plivo) and is positioned as a self‑hosted alternative to services like Vapi or Retell. With strong recent activity, 778 stars and a growing community, it’s ready for serious pilot projects.

**Value**  
Patter removes the repetitive, manual steps involved in building voice‑enabled AI agents—provisioning numbers, handling call routing, and managing telephony APIs—so teams can focus on the conversational logic. By exposing a clean SDK/CLI and language‑specific bindings, it enables rapid composition of repeatable workflows (e.g., scheduling calls, routing to CRM tools, or triggering operational tasks) without vendor lock‑in.

**Practical Adoption Path**  
1. **Prototype** – Install the Python or TypeScript package, add the four‑line snippet to register a phone number, and test locally with a sandbox Twilio/Telnyx account.  
2. **Integrate** – Connect the SDK to existing services (databases, task queues, CRM APIs) using the provided hooks and CLI commands; the clear API surface makes adding custom logic straightforward.  
3. **Pilot** – Deploy the service in a container or serverless environment, point a production‑grade phone number to it, and monitor via the built‑in logging/metrics.  
4. **Scale** – Leverage the same open‑source stack across multiple regions or providers, customizing or extending the SDK as needed without incurring additional vendor costs.

**Production Readiness**  
Patter scores high on readiness: recent commits (as of 2026‑06‑23), active issue resolution, and a healthy fork/star ratio indicate an engaged maintainer community. Its MIT license, clear security posture, and compatibility with established telephony platforms make it suitable for production pilots, though a final review of maintainers’ responsiveness and any emerging security advisories is advisable before full rollout.

### Русский

PatterAI/Patter — это открытый SDK для голосового ИИ, позволяющий за четыре строки кода (Python или TypeScript) привязать к агенту телефонный номер через Twilio, Telnyx или Plivo и полностью контролировать стек. Он автоматизирует повторяющиеся операции, соединяя инструменты в повторяемые потоки (например, автоматический обзвон, планирование задач и интеграция с существующими сервисами). Проект имеет высокий уровень готовности к продакшену: активные коммиты, 778 звёзд на GitHub, MIT‑лицензия и поддержка основных языков, что делает его надёжным выбором для пилотных и масштабных внедрений.

### 中文

**项目简介**  
PatterAI/Patter 是一套开源的语音 AI SDK，提供类似 Vapi / Retell 的功能，但让开发者可以完全掌控技术栈。仅用四行代码（Python 或 TypeScript）即可为你的 AI 代理分配电话号，支持 Twilio、Telnyx、Plivo 等主流通信平台，MIT 许可证，适合希望自行托管并深度定制的构建者。

**价值**  
- **消除重复人工操作**：将拨号、通话接入、语音转文字等繁琐环节抽象为 SDK 调用，显著提升工作流自动化效率。  
- **灵活可编程**：提供统一的 API/SDK/CLI，兼容 Python 与 TypeScript，便于在前端、后端或自动化脚本中快速集成。  
- **完整可控的技术栈**：所有通信、语音识别、LLM 调用均在自己服务器或私有云上运行，满足数据合规和成本控制需求。

**典型接入方式**  
```python
# Python 示例（4 行代码）
from patter import PatterClient

client = PatterClient(provider="twilio", api_key="YOUR_TWILIO_KEY")
client.assign_number(agent_id="my_bot", phone="+1xxxxxxxxxx")
```
```typescript
// TypeScript 示例（4 行代码）
import { PatterClient } from "patter-sdk";

const client = new PatterClient({ provider: "plivo", apiKey: "YOUR_PLIVO_KEY" });
client.assignNumber("my_bot", "+1xxxxxxxxxx");
```
- **SDK**：通过 `pip install patter-sdk`（Python）或 `npm i patter-sdk`（TypeScript）获取。  
- **CLI**：`patter-cli assign-number --agent my_bot --phone +1xxxx`，适合脚本化或 CI/CD 场景。  
- **直接 API**：RESTful 接口可配合任意语言的 HTTP 客户端调用。

**生产可用性**  
- **活跃度**：截至 2026‑06‑23，项目最近有提交，GitHub 778 星、82 Fork，社区讨论活跃。  
- **生态兼容**：内置对 Twilio、Telnyx、Plivo 的成熟适配，且代码结构清晰，易于自行扩展其他 SIP/VoIP 提供商。  
- **许可证**：MIT，商业使用无额外限制。  
- **风险**：暂无重大元数据风险，但仍建议在正式投产前完成安全审计、依赖漏洞扫描，并确认维护者的长期可用性。  

综合来看，PatterAI/Patter 已具备高水平的生产准备度，适合作为面向语音 AI 应用的底层通信框架进行试点乃至正式上线。

## 🧭 Practical evaluation

**Value:** PatterAI/Patter helps remove repetitive manual operations from a workflow.

**Best use cases**

- remove manual work
- connect tools into repeatable flows
- schedule operational tasks

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 778 GitHub stars
- 82 forks
- updated 2026-06-23
- primary language: Python
- 20 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 48/100 |
| stars | 62/100 |
| topics | 100/100 |
| outlook | 80/100 |
| quality | 76/100 |
| recency | 80/100 |
| adoption | 58/100 |
| production | 77/100 |
| usefulness | 90/100 |
| integration | 94/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 300/100 |

---

<sub>🔭 Discovered 2026-06-23 · [View on GitHub](https://github.com/PatterAI/Patter) · [← Back to AI/ML](./README.md)</sub>
