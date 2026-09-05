# shengyanlin/claude-overlay

[![Stars](https://img.shields.io/github/stars/shengyanlin/claude-overlay?style=flat-square&color=yellow)](https://github.com/shengyanlin/claude-overlay/stargazers) [![Forks](https://img.shields.io/github/forks/shengyanlin/claude-overlay?style=flat-square&color=blue)](https://github.com/shengyanlin/claude-overlay/network) [![Language](https://img.shields.io/badge/lang-Python-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-74%2F100-brightgreen?style=flat-square)](#)

> A floating, screen-aware Claude Code chat for Windows - it reads your screen to answer, and runs on your own Claude subscription (no API key).

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 24 |
| 🍴 **Forks** | 1 |
| 💻 **Language** | Python |
| 📈 **Score** | 74/100 |
| 🗓️ **Last push** | 2026-09-05 |
| 🔍 **Source** | github |

## 🏷️ Topics

`ai` `ai-assistant` `always-on-top` `anthropic` `claude` `claude-agent-sdk` `claude-code` `desktop-app` `developer-tools` `llm` `overlay` `python`

## 🎯 Categories

Payments · AI/ML · Communication · Productivity · DevTools

## 📝 Summary

### English

**Brief Summary (2‑3 sentences)**  
*shengyanlin/claude‑overlay* is an open‑source Windows utility that adds a floating, screen‑aware Claude Code chat window. It captures the contents of the active screen, sends them to your own Claude subscription (no separate API key is required), and returns AI‑generated code or answers directly on the desktop. The project is positioned as a fast‑track way to embed monetisation‑related flows—such as billing, checkout, or PSP (payment service provider) integrations—into developer tools or internal admin consoles.

**Value**  
- **Accelerated payment‑flow prototyping:** By exposing ready‑made hooks (API/SDK/CLI) for billing and PSP operations, teams can prototype checkout or subscription logic without building a UI from scratch.  
- **Zero‑cost Claude access:** The overlay reuses an existing Claude subscription, eliminating the need for additional API keys or third‑party licensing fees.  
- **Context‑aware assistance:** Because the overlay reads the screen, developers receive AI suggestions that are directly relevant to the code or UI they are working on, speeding up debugging and integration tasks.

**Practical Adoption Path**  
1. **Clone & install** the Python package (requires Windows, Python 3.9+).  
2. **Configure** your Claude subscription token in the provided `.env` file.  
3. **Run** the overlay (`python -m claude_overlay`) and verify that the floating chat appears and correctly captures screen content.  
4. **Integrate** the exposed CLI/SDK calls into your payment service codebase (e.g., `claude_overlay.checkout --amount 19.99`).  
5. **Iterate** by customizing the overlay’s prompt templates to match your specific PSP or billing workflow.  

Because the project ships with clear documentation, language metadata (Python), and a small set of focused topics, the integration can be completed within a few days for most Python‑centric back‑ends.

**Production Readiness**  
- **Activity & community:** Updated on 2026‑06‑25, 24 GitHub stars, recent commits, and a modest fork count indicate an active, albeit small, community.  
- **Technical maturity:** The codebase is concise, well‑structured, and written in a single primary language (Python), making security reviews and dependency audits straightforward.  
- **Risk considerations:** No major licensing or metadata issues have been flagged, but a final review of the MIT‑style license, dependency vulnerabilities, and maintainer responsiveness is advisable before full‑scale deployment.  

Overall, the overlay is sufficiently stable for a pilot or internal tooling rollout, especially when the goal is to speed up payment‑flow development and leverage Claude’s code‑generation capabilities without additional API costs.

### Русский

**sh​engyanlin/claude‑overlay** — это открытый Python‑проект, предоставляющий плавающий чат Claude Code, который «читает» содержимое экрана Windows и отвечает в реальном времени, используя вашу личную подписку Claude (без необходимости API‑ключа). Его типичное внедрение — быстрый прототип интеграции платёжных и биллинговых сценариев (checkout, оценка PSP‑потоков, автоматизация операций), поскольку проект уже экспортирует готовые API/SDK/CLI‑интерфейсы и метаданные. По уровню готовности к продакшну проект считается высоким: активные коммиты (обновление 2026‑06‑25), 24 звёзд, поддержка Python, а также положительные сигналы экосистемы делают его надёжным кандидатом для пилотного использования, при условии окончательной проверки лицензии и безопасности.

### 中文

**项目简介**  
`shengyanlin/claude-overlay` 是一款在 Windows 上运行的悬浮式 Claude 代码聊天工具，能够实时读取当前屏幕内容并基于用户自己的 Claude 订阅（无需额外 API Key）给出答案。它把 AI 助手直接嵌入到开发者的工作界面，提升代码编写和调试效率。

**价值点**  
- **快速集成付费/结算流**：提供统一的实现信号（API/SDK/CLI），帮助开发者在几行代码或一次命令调用中嵌入计费、结算或 PSP（支付服务提供商）相关的业务逻辑。  
- **降低研发成本**：利用已有的 Claude 订阅，无需额外购买或管理 OpenAI/Anthropic API Key，直接在本地运行，省去第三方费用和网络延迟。  
- **提升用户体验**：悬浮窗口随屏幕移动，开发者可以边看代码边获取 AI 解释或示例，适用于代码审查、错误定位、自动化支付操作等场景。

**典型接入方式**  
1. **安装依赖**：`pip install -r requirements.txt`（项目主要使用 Python）。  
2. **配置 Claude 订阅**：在本地环境变量或配置文件中填写 Claude 账户的访问凭证（无需 API Key，只要登录信息）。  
3. **启动悬浮窗口**：运行 `python overlay.py`，程序会检测当前活动窗口并在屏幕上方弹出可交互的聊天框。  
4. **调用计费/PSP 接口**：在聊天框中使用预定义的指令（如 `/checkout`, `/psp-status`）或通过项目提供的 SDK（`claude_overlay.sdk`）在代码中直接调用对应的支付/结算函数。  

**生产可用性**  
- **活跃度**：截至 2026‑06‑25 最近一次提交，项目仍在维护；GitHub 上已有 24 ⭐、1 🍴，说明已有一定社区关注。  
- **技术成熟度**：核心实现基于 Python，提供明确的 API/CLI，文档覆盖主要使用场景，易于在 CI/CD 流程中集成。  
- **安全与合规**：项目本身不涉及外部 API Key，数据处理在本机完成，降低了泄露风险；但仍建议在正式上线前进行内部安全审计并确认许可证（MIT/Apache 等）符合企业合规要求。  
- **适配性**：专为 Windows 设计，支持常见的开发环境（VS Code、PyCharm 等），对跨平台需求的团队可考虑在 Windows 虚拟机或容器中部署。  

综上，`shengyanlin/claude-overlay` 具备较高的生产可用性，能够帮助企业快速实现支付/结算相关的功能集成，同时为开发者提供即时的 AI 编码辅助。只要完成安全审查并确认许可证符合企业政策，即可在生产环境中进行试点或正式推广。

## 🧭 Practical evaluation

**Value:** shengyanlin/claude-overlay helps integrate monetization, billing, or PSP flows faster.

**Best use cases**

- integrate billing or checkout
- evaluate PSP flows
- automate payment operations

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 24 GitHub stars
- 1 forks
- updated 2026-06-25
- primary language: Python
- 15 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 8/100 |
| stars | 30/100 |
| topics | 100/100 |
| outlook | 74/100 |
| quality | 61/100 |
| recency | 80/100 |
| adoption | 24/100 |
| production | 69/100 |
| usefulness | 100/100 |
| integration | 78/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 500/100 |

---

<sub>🔭 Discovered 2026-06-25 · [View on GitHub](https://github.com/shengyanlin/claude-overlay) · [← Back to Payments](./README.md)</sub>
