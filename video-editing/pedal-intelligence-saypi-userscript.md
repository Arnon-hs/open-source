# Pedal-Intelligence/saypi-userscript

[![Stars](https://img.shields.io/github/stars/Pedal-Intelligence/saypi-userscript?style=flat-square&color=yellow)](https://github.com/Pedal-Intelligence/saypi-userscript/stargazers) [![Forks](https://img.shields.io/github/forks/Pedal-Intelligence/saypi-userscript?style=flat-square&color=blue)](https://github.com/Pedal-Intelligence/saypi-userscript/network) [![Language](https://img.shields.io/badge/lang-TypeScript-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-53%2F100-brightgreen?style=flat-square)](#)

> Enterprise-grade browser extension bringing multilingual voice interaction to AI chatbots (Pi, Claude, ChatGPT). Features real-time speech detection with Silero VAD, accurate transcription via OpenAI Whisper, and ElevenLabs TTS. Built with TypeScript, XState, and modern web standards. Progressive enhancement across Chrome, Firefox, and Safari

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 24 |
| 🍴 **Forks** | 8 |
| 💻 **Language** | TypeScript |
| 📈 **Score** | 53/100 |
| 🗓️ **Last push** | 2026-09-05 |
| 🔍 **Source** | github |

## 🏷️ Topics

`ai` `chat` `chatbot` `chatgpt` `claude` `conversation` `dictation` `endpointing` `llm` `multi-turn-conversations` `openai` `pi`

## 🎯 Categories

Video Editing · AI/ML · Communication

## 📝 Summary

### English

**Brief Summary**  
Pedal‑Intelligence’s *saypi‑userscript* is an enterprise‑grade browser extension that adds multilingual voice interaction to AI chatbots such as Pi, Claude, and ChatGPT. It combines real‑time speech detection (Silero VAD), high‑accuracy transcription (OpenAI Whisper), and natural‑sounding text‑to‑speech (ElevenLabs) using TypeScript, XState, and modern web standards, and works across Chrome, Firefox, and Safari.

**Value**  
The script eliminates the repetitive copy‑paste and typing steps that developers and power users normally perform when testing or using AI chatbots, turning spoken input into instant, multilingual chatbot responses and reading the replies back aloud. This hands‑free workflow speeds up prototyping, improves accessibility, and enables rapid “voice‑first” experimentation without building a custom backend.

**Practical Adoption Path**  

| Step | Action | Reason |
|------|--------|--------|
| 1️⃣  | **Clone & run the README demo** – install the userscript via a manager (e.g., Tampermonkey) on a test browser. | Verifies basic functionality and ensures the required API keys (OpenAI, ElevenLabs) are correctly set. |
| 2️⃣  | **Create a small proof‑of‑concept flow** – e.g., voice‑controlled ticket creation in a private Slack channel using ChatGPT for summarisation. | Confirms integration with your own chatbot endpoints and validates latency/accuracy in a controlled scenario. |
| 3️⃣  | **Wrap in a CI‑checked build** – lock dependency versions (Silero, Whisper, ElevenLabs SDKs) and add lint/type checks. | Reduces risk of breaking changes and prepares the script for internal distribution. |
| 4️⃣  | **Deploy to a pilot group** – roll out to a limited set of power users or QA engineers and collect feedback on UX, language coverage, and error handling. | Allows you to gauge real‑world performance and identify any security or privacy concerns (e.g., audio data handling). |
| 5️⃣  | **Scale to production** – package the script as an internal extension, enforce API‑key rotation, and monitor usage metrics. | Provides a controlled, maintainable production artifact. |

**Production Readiness**  
- **Maturity:** Medium – the project is functional and actively maintained (last update 2026‑06‑24) with 24 stars and 8 forks, making it suitable for prototypes or internal tooling.  
- **Dependencies:** Relies on external AI services (OpenAI Whisper, ElevenLabs TTS) and a VAD model; you’ll need to manage API quotas, latency, and cost.  
- **Maintenance:** Written in TypeScript with XState, which eases future extensions, but you should audit the license, verify no hidden security issues, and pin third‑party versions before wide deployment.  
- **Risk Mitigation:** Conduct a short security review (especially around audio data transmission), set up monitoring for API failures, and establish a fallback (e.g., text‑only mode) for environments where voice is not permitted.

Overall, *saypi‑userscript* offers a compelling way to automate voice‑driven interactions with AI chatbots; it can be adopted incrementally, starting with a proof‑of‑concept, and, after proper dependency locking and security vetting, it can serve as a reliable component of internal automation pipelines.

### Русский

**Pedal‑Intelligence/saypi‑userscript** — это открытая браузерная надстройка, позволяющая управлять AI‑чат‑ботами (Pi, Claude, ChatGPT) голосом на любом из поддерживаемых языков. В типичном сценарии её подключают к уже существующему веб‑интерфейсу: скрипт в реальном времени определяет речь (Silero VAD), преобразует её в текст (OpenAI Whisper) и озвучивает ответы (ElevenLabs TTS), что избавляет от ручного ввода и ускоряет повторяющиеся задачи. Готовность к production — средняя: проект пригоден для прототипов и внутренних автоматизаций, но перед развёртыванием в продакшн требуется проверка лицензии, безопасности и стабильности зависимостей.

### 中文

**项目简介**  
Pedal‑Intelligence/sayui‑userscript 是一款企业级浏览器扩展（Chrome、Firefox、Safari），为主流 AI 聊天机器人（Pi、Claude、ChatGPT）提供多语言语音交互。它基于 Silero VAD 实时检测语音、使用 OpenAI Whisper 完成高精度转写，并通过 ElevenLabs 实现自然的文本‑转‑语音（TTS），全程采用 TypeScript、XState 与现代 Web 标准实现。

**价值体现**  
- **消除手动输入**：用户只需说话即可完成提问、指令或对话，大幅降低键盘操作的重复劳动。  
- **跨语言、跨平台**：支持多语言识别与合成，兼容主流浏览器，适用于全球化团队。  
- **可嵌入工作流**：通过脚本化方式可与内部工具、自动化平台（如 Zapier、Make）快速对接，实现“一键触发‑语音交互‑结果回写”的闭环。

**典型接入方式**  
1. **脚本注入**：在目标网页（如 ChatGPT 页面）通过 Tampermonkey/Greasemonkey 安装 userscript。  
2. **API 配置**：在脚本的配置文件中填写 OpenAI Whisper、ElevenLabs 的 API Key（或自行部署对应服务）。  
3. **事件编排**：利用 XState 状态机定义“监听‑转写‑调用‑合成”流程，必要时可在业务系统中通过自定义事件触发。  
4. **小范围验证**：先在内部测试环境或单个用户账号上进行功能验证，确认语音识别、TTS 与目标聊天机器人的交互符合预期。

**生产可用性评估**  
- **成熟度**：项目已有 24 ★、8 Fork，最近一次提交在 2026‑06‑24，代码基于 TypeScript，结构清晰，适合作为原型或内部工具。  
- **依赖风险**：依赖外部 Whisper 与 ElevenLabs 服务，需要确保 API 配额、网络可达性以及费用预算。  
- **维护状态**：目前维护者活跃度不明，建议在正式上线前与仓库维护者确认长期支持计划，并自行设立内部维护分支。  
- **安全合规**：暂无显著的元数据风险，但仍需审查许可证、第三方库的安全漏洞以及对用户语音数据的隐私处理。  

**结论**  
在做好小规模 PoC、完成安全与许可证审查后，saypi‑userscript 可在内部业务流程中实现“语音驱动‑AI 对话”的自动化，适合作为原型或内部生产环境使用；若需对外提供服务，则建议进一步强化维护、监控与合规措施后再投入正式生产。

## 🧭 Practical evaluation

**Value:** Pedal-Intelligence/saypi-userscript helps remove repetitive manual operations from a workflow.

**Best use cases**

- remove manual work
- connect tools into repeatable flows
- schedule operational tasks

**Integration notes:** Looks feasible to evaluate, but integration should start with a small proof of concept and README check.

**Production readiness:** Medium: useful for prototypes or internal workflows, with dependency and maintenance checks before production.

**Quality signals**

- 24 GitHub stars
- 8 forks
- updated 2026-06-24
- primary language: TypeScript
- 17 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 24/100 |
| stars | 30/100 |
| topics | 100/100 |
| outlook | 63/100 |
| quality | 63/100 |
| recency | 80/100 |
| adoption | 28/100 |
| production | 65/100 |
| usefulness | 42/100 |
| integration | 46/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 300/100 |

---

<sub>🔭 Discovered 2026-06-24 · [View on GitHub](https://github.com/Pedal-Intelligence/saypi-userscript) · [← Back to Video-editing](./README.md)</sub>
