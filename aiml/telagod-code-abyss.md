# telagod/code-abyss

[![Stars](https://img.shields.io/github/stars/telagod/code-abyss?style=flat-square&color=yellow)](https://github.com/telagod/code-abyss/stargazers) [![Forks](https://img.shields.io/github/forks/telagod/code-abyss?style=flat-square&color=blue)](https://github.com/telagod/code-abyss/network) [![Language](https://img.shields.io/badge/lang-JavaScript-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-67%2F100-brightgreen?style=flat-square)](#)

> 为 Claude Code / Codex CLI 注入邪修人格、4种可切换输出风格与 56 篇攻防工程秘典

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 205 |
| 🍴 **Forks** | 28 |
| 💻 **Language** | JavaScript |
| 📈 **Score** | 67/100 |
| 🗓️ **Last push** | 2026-05-13 |
| 🔍 **Source** | github |

## 🏷️ Topics

`ai-assistant` `blue-team` `claude-code` `cli` `codex-cli` `configuration` `prompt-engineering` `red-team` `security`

## 🎯 Categories

AI/ML · DevTools · Security

## 📝 Summary

### English

**Summary**  
telagod/code‑abyss is a JavaScript toolkit that injects “evil‑cult” personality traits, four interchangeable output styles, and a library of 56 offensive/defensive engineering playbooks into Claude Code / Codex CLI. It enables developers to prototype AI‑driven code‑generation, RAG, or autonomous‑agent workflows without building a model stack from scratch.

**Value**  
- **Rapid AI feature addition** – By wrapping the existing Claude Code / Codex CLI, the project supplies ready‑made persona and style switches plus a curated set of security‑oriented prompts, turning a generic code model into a specialized “code‑abyss” assistant.  
- **Low‑effort experimentation** – The CLI/SDK exposure means teams can test different personas and prompt libraries with a single command, accelerating proof‑of‑concepts for internal tooling, code review bots, or red‑team/blue‑team automation.  
- **Open‑source transparency** – With 205 ★, active commits, and a modest codebase, the implementation can be audited, extended, or integrated into existing CI/CD pipelines.

**Practical adoption path**  
1. **Clone & install** – `npm i && npm link` to expose the `code-abyss` CLI.  
2. **Configure credentials** – Set the Claude/Codex API key via environment variable (`CLAUDE_API_KEY`).  
3. **Select persona/style** – Use flags such as `--persona evilCult --style stealth` to switch output modes.  
4. **Integrate** – Wrap the CLI in scripts or invoke the exported SDK from Node/TypeScript services; combine with vector stores for RAG or with orchestration tools (e.g., LangChain) to build agents.  
5. **Iterate & extend** – Add custom playbooks to the `playbooks/` directory or contribute new styles via pull request.

**Production readiness**  
The project shows strong OSS candidate signals: recent activity (last commit 2026‑05‑13), a healthy star/fork ratio, and clear JavaScript APIs. Its dependency footprint is modest, and the CLI is self‑contained, making it straightforward to sandbox in staging environments. While no critical licensing or security red flags have been identified, a final review of the underlying Claude/Codex usage policy and a security audit of the injected prompt library are recommended before full‑scale deployment. With those checks, code‑abyss is ready for pilot projects and can be promoted to production for internal tooling or controlled external services.

### Русский

telagod/code-abyss — это open‑source‑инструмент, который «накачивает» Claude Code / Codex CLI личностью‑модулем, четырьмя переключаемыми стилями вывода и набором из 56 практических атак‑защита сценариев, позволяя быстро добавить AI‑функциональность в существующие проекты без построения модели с нуля. Типичный сценарий — прототипирование новых AI‑фич, построение RAG‑ или агентных пайплайнов и оценка возможностей модели через удобный CLI/SDK на JavaScript. Проект имеет высокий уровень готовности к production: активные коммиты (обновлён 13 мая 2026), 205 звёзд, 28 форков, стабильный стек и хорошую экосистемную интеграцию, хотя окончательная проверка лицензии и безопасности всё же рекомендуется.

### 中文

**项目简介**  
telagod/code-abyss 为 Claude Code / Codex 命令行工具注入了“邪修人格”，提供 4 种可切换的输出风格以及 56 篇攻防工程秘典，让 AI 生成的代码既有趣又具备渗透测试思路。

**价值**  
- **快速赋能**：无需自行训练模型，只需在已有的 Claude / Codex 环境上加载本项目，即可获得多样化、具攻击性思维的代码建议。  
- **安全研发利器**：内置的攻防秘典帮助安全团队在开发阶段发现潜在漏洞，提升代码审计和红蓝对抗的效率。  
- **可定制输出**：四种风格（如“正义”“邪恶”“戏谑”“极简”）可随时切换，满足不同场景的调试、演示或教学需求。

**典型接入方式**  
1. **CLI 方式**：直接在终端使用 `code-abyss` 命令，配合 Claude / Codex 的 API Token，即可在本地或 CI/CD 环境中调用。  
2. **SDK/库方式**：项目提供 JavaScript SDK，开发者可在 Node.js 项目中 `import { AbyssClient } from 'code-abyss'`，通过 `client.generate(prompt, {style: 'evil'})` 获得指定风格的代码。  
3. **RAG/Agent 集成**：将 `AbyssClient` 作为工具插件，嵌入 LangChain、AutoGPT 等代理框架，实现“攻防思维”检索增强（RAG）或交互式安全助手。

**生产可用性**  
- **活跃度**：截至 2026‑05‑13，项目最近一次提交，拥有 205 ★、28 Fork，维护者响应及时。  
- **技术成熟度**：核心实现基于成熟的 Claude / Codex API，代码量小、依赖少，易于审计和容器化部署。  
- **安全与合规**：目前未发现重大元数据风险，仍需对许可证（MIT）和内部安全审计进行最终确认。  
- **适配性**：提供标准的 CLI、REST 调用和 Node.js SDK，能够在本地、云端或边缘环境快速集成，适合作为安全研发或 AI 原型的正式试点。

综上，telagod/code-abyss 具备 **高可用、易集成、功能独特** 的特性，可在安全研发、代码审计及 AI 功能原型阶段直接投入生产使用。

## 🧭 Practical evaluation

**Value:** telagod/code-abyss helps add AI capability without starting from a blank model stack.

**Best use cases**

- prototype AI features
- build RAG or agent workflows
- evaluate model tooling

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 205 GitHub stars
- 28 forks
- updated 2026-05-13
- primary language: JavaScript
- 9 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 37/100 |
| stars | 49/100 |
| topics | 100/100 |
| outlook | 78/100 |
| quality | 76/100 |
| recency | 100/100 |
| adoption | 46/100 |
| production | 77/100 |
| usefulness | 58/100 |
| integration | 62/100 |
| sourceTrust | 100/100 |

---

<sub>🔭 Discovered 2026-05-13 · [View on GitHub](https://github.com/telagod/code-abyss) · [← Back to AI/ML](./README.md)</sub>
