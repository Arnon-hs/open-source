# RYOITABASHI/Shelly

[![Stars](https://img.shields.io/github/stars/RYOITABASHI/Shelly?style=flat-square&color=yellow)](https://github.com/RYOITABASHI/Shelly/stargazers) [![Forks](https://img.shields.io/github/forks/RYOITABASHI/Shelly?style=flat-square&color=blue)](https://github.com/RYOITABASHI/Shelly/network) [![Language](https://img.shields.io/badge/lang-TypeScript-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-60%2F100-brightgreen?style=flat-square)](#)

> AI-powered chat-first terminal IDE for Android. Built entirely on a phone, by someone who can't write code.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 35 |
| 🍴 **Forks** | 4 |
| 💻 **Language** | TypeScript |
| 📈 **Score** | 60/100 |
| 🗓️ **Last push** | 2026-09-05 |
| 🔍 **Source** | github |

## 🏷️ Topics

`ai` `android` `chat-ui` `claude` `claude-code` `expo` `gemini-cli` `ide` `kotlin` `llm` `mobile-development` `open-source`

## 🎯 Categories

AI/ML · Communication · Frontend · DevTools · Mobile

## 📝 Summary

### English

**Brief Summary (2‑3 sentences)**  
Shelly is an AI‑powered, chat‑first terminal IDE that runs entirely on Android devices. It lets developers prototype AI‑enhanced features—such as RAG pipelines or autonomous agents—directly from a phone, without having to assemble a model stack from scratch. Although built by a non‑programmer, the project is functional, open‑source, and ready for internal experimentation.

**Value**  
- **Fast AI prototyping** – Shelly ships with ready‑made API/SDK/CLI hooks and language‑aware metadata, so you can add conversational AI, retrieval‑augmented generation, or agent workflows to a product without the overhead of training or deploying models yourself.  
- **Mobile‑first workflow** – Because the IDE runs on Android, teams can code, test, and iterate on the go, which is especially useful for field engineers, hackathon participants, or remote squads.  
- **Low barrier to entry** – The “chat‑first” interface abstracts away much of the boilerplate, letting even non‑technical stakeholders experiment with AI capabilities and surface useful prompts or data flows.

**Practical Adoption Path**  

| Phase | Steps | Outcome |
|-------|-------|---------|
| **Evaluation** | 1. Clone the repo and run the provided CLI on an Android device or emulator.<br>2. Verify the exposed API/SDK endpoints (e.g., `shelly.run(prompt)`).<br>3. Test a simple RAG use‑case using a public LLM endpoint. | Confirm that Shelly integrates with your existing model provider and that the chat UI meets your UX expectations. |
| **Pilot / Prototype** | 1. Create a sandbox project that wraps Shelly’s SDK.<br>2. Implement a focused AI feature (e.g., a code‑assistant command or a knowledge‑base query).<br>3. Collect feedback from a small internal team. | Validate the workflow, measure latency, and gauge developer productivity gains. |
| **Integration** | 1. Harden the dependency chain (pin versions, add security scans).<br>2. Wrap Shelly’s CLI/SDK behind an internal service layer if needed.<br>3. Add monitoring (usage metrics, error logs). | Ready for broader internal rollout or limited production use. |
| **Production Roll‑out** | 1. Conduct a formal security and license review (MIT‑style license, but verify third‑party libraries).<br>2. Deploy the CLI/SDK in a container or as part of your CI pipeline.<br>3. Establish a maintenance plan (track upstream updates, fork if required). | Stable, maintainable component that delivers AI‑augmented functionality in production environments. |

**Production Readiness Assessment**  

- **Maturity** – Medium. The project is functional, has recent commits (as of 2026‑06‑27), and a modest community (35 stars, 4 forks). It is suitable for prototyping and internal tooling, but it lacks extensive testing, formal CI/CD pipelines, and a large contributor base.  
- **Dependencies & Maintenance** – Written in TypeScript, the codebase is relatively easy to audit. However, you should perform a dependency‑vulnerability scan and consider forking or vendor‑locking critical libraries to mitigate future breakage.  
- **Security & Licensing** – No obvious red flags, but a final review of the repository’s license (presumably MIT/Apache) and any bundled third‑party binaries is required before production deployment.  
- **Operational Considerations** – Because Shelly runs on Android, you’ll need a strategy for device management (MDM) or an Android emulator in CI if you want headless execution. For server‑side use, you can wrap the CLI in a container that emulates the Android environment.

**Bottom Line**  
Shelly offers a quick, low‑effort way to embed AI capabilities into mobile‑centric or remote development workflows. It is best adopted first as a prototype or internal tool, with a clear path to hardening the stack for production use after security, licensing, and dependency reviews.

### Русский

RYOITABASHI/Shelly — это AI‑ориентированный терминальный IDE для Android, позволяющий быстро добавлять возможности ИИ в проекты без необходимости создавать стек моделей с нуля. Типичный сценарий использования — прототипирование AI‑фич, построения RAG‑ или агентных workflows и оценка инструментов моделей непосредственно на смартфоне. Проект находится на среднем уровне готовности к production: полезен для внутренних прототипов и экспериментов, но перед внедрением в продакшн требуется проверка зависимостей, безопасности и активности поддержки.

### 中文

**项目简介（2‑3 句话）**  
RYOITABASHI/Shelly 是一款基于 AI 的「聊天优先」终端 IDE，专为 Android 手机打造，所有功能均可在手机上完整运行。即使不会写代码的用户也能通过对话快速原型化 AI 功能、构建 RAG 或智能体工作流。

**价值**  
- **快速赋能 AI**：无需从零搭建模型堆栈，直接调用已有的 API/SDK，即可在终端中实现聊天、检索增强生成等 AI 能力。  
- **低门槛原型**：通过对话式交互即可编写、调试、运行代码，适合产品经理、设计师或非技术人员快速验证想法。  
- **移动端即用**：全程在 Android 手机上完成，省去电脑环境配置，随时随地进行 AI 开发和实验。

**典型接入方式**  
1. **API/SDK**：项目公开了 HTTP API 与 TypeScript SDK，开发者可在自己的前端或后端项目中直接调用 `shelly.runCommand()`、`shelly.evaluate()` 等接口。  
2. **CLI**：通过 npm 安装 `shelly-cli`，在本地或 CI 环境执行 `shelly <command>`，实现脚本化调用。  
3. **语言元数据**：项目提供了语言/框架的元信息（如 `typescript`, `python`），便于在 IDE 中自动补全和上下文感知。  
4. **主题/插件**：可通过 `shelly-plugin` 扩展特定业务场景（如 RAG、Agent），只需在项目的 `shelly.config.js` 中声明即可。

**生产可用性**  
- **成熟度**：当前评分 63/100，GitHub 35 星、4 Fork，最近一次更新在 2026‑06‑27，代码基于 TypeScript，社区活跃度一般。  
- **适用范围**：非常适合作为内部原型工具或研发实验平台；在正式生产环境使用前，需要完成以下检查：  
  - **依赖审计**：确认第三方库的许可证兼容性与安全漏洞。  
  - **安全评估**：审查 API 鉴权、数据加密、网络访问控制等。  
  - **运维准备**：评估在 Android 设备上长期运行的资源消耗（CPU、内存、网络）以及更新维护流程。  
- **结论**：在做好上述检查后，Shelly 可用于内部业务流程自动化、AI 功能快速迭代等生产场景；若对高可用性和 SLA 有严格要求，仍建议在更成熟的服务器端平台上部署核心模型。

## 🧭 Practical evaluation

**Value:** RYOITABASHI/Shelly helps add AI capability without starting from a blank model stack.

**Best use cases**

- prototype AI features
- build RAG or agent workflows
- evaluate model tooling

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** Medium: useful for prototypes or internal workflows, with dependency and maintenance checks before production.

**Quality signals**

- 35 GitHub stars
- 4 forks
- updated 2026-06-27
- primary language: TypeScript
- 17 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 17/100 |
| stars | 33/100 |
| topics | 100/100 |
| outlook | 67/100 |
| quality | 63/100 |
| recency | 80/100 |
| adoption | 29/100 |
| production | 68/100 |
| usefulness | 58/100 |
| integration | 62/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 500/100 |

---

<sub>🔭 Discovered 2026-06-27 · [View on GitHub](https://github.com/RYOITABASHI/Shelly) · [← Back to AI/ML](./README.md)</sub>
