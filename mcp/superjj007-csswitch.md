# SuperJJ007/CSswitch

[![Stars](https://img.shields.io/github/stars/SuperJJ007/CSswitch?style=flat-square&color=yellow)](https://github.com/SuperJJ007/CSswitch/stargazers) [![Forks](https://img.shields.io/github/forks/SuperJJ007/CSswitch?style=flat-square&color=blue)](https://github.com/SuperJJ007/CSswitch/network) [![Language](https://img.shields.io/badge/lang-Rust-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-64%2F100-brightgreen?style=flat-square)](#)

> 让 Claude Science 的推理走自选的第三方 API（DeepSeek / 通义千问 / 任意 OpenAI 兼容端点），保留工具调用·Skill·MCP·代码执行，含本地虚拟登录跳过。macOS 菜单栏 app。仅供个人学习研究，使用者自负风险。

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 39 |
| 🍴 **Forks** | 3 |
| 💻 **Language** | Rust |
| 📈 **Score** | 64/100 |
| 🗓️ **Last push** | 2026-09-05 |
| 🔍 **Source** | github |

## 🏷️ Topics

`anthropic` `claude` `claude-science` `dashscope` `deepseek` `llm` `macos` `mcp` `menubar` `openai-compatible` `proxy` `qwen`

## 🎯 Categories

MCP · AI/ML · Networking

## 📝 Summary

### English

**Brief summary**  
SuperJJ007/CSswitch is a macOS menu‑bar application written in Rust that lets Claude Science route its reasoning through any third‑party LLM endpoint (DeepSeek, Tongyi Qianwen, or any OpenAI‑compatible API) while preserving tool‑calling, Skill, MCP, and code‑execution capabilities, and even supports a local virtual login bypass. It is intended for personal learning and experimentation, with users assuming all risk.

**Value proposition**  
- **Unified gateway** – Provides a single, configurable front‑end for swapping between different LLM providers without changing the underlying Claude Science prompts or tool‑calling logic.  
- **Full feature parity** – Keeps advanced Claude Science capabilities (tool calls, Skill, Model Context Protocol, code execution) intact, enabling richer, data‑driven interactions.  
- **Rapid prototyping** – Developers can experiment with cost, latency, or model‑specific behavior by simply pointing the app at a new endpoint, accelerating evaluation of alternative APIs.  

**Practical adoption path**  
1. **Clone & build** – Pull the repo, install Rust toolchain, and compile the binary (`cargo build --release`).  
2. **Configure endpoints** – Edit the provided TOML/JSON config to add API keys and URLs for the desired LLMs (DeepSeek, Tongyi, OpenAI‑compatible).  
3. **Run as a menu‑bar app** – Launch the binary; it sits in the macOS menu bar, exposing a UI to toggle the active provider and manage credentials.  
4. **Integrate with Claude Science** – Point Claude Science’s “custom API” setting to the local HTTP address exposed by CSswitch; the app forwards requests to the selected third‑party model.  
5. **Iterate & test** – Use the built‑in logging and response tracing to compare model outputs, latency, and cost, then lock in the preferred endpoint for downstream tooling or internal services.  

**Production readiness**  
- **Maturity** – Medium. The project is actively maintained (last commit 2026‑07‑03) and has modest community interest (≈40 ★, 3 forks).  
- **Stability** – Core functionality (API routing, tool‑call preservation) works, but the “virtual login bypass” and some edge‑case error handling may need additional testing in production environments.  
- **Dependencies** – Relies on Rust’s ecosystem and external LLM endpoints; ensure you audit the crates for security vulnerabilities and verify the compliance of the chosen third‑party APIs.  
- **Operational considerations** – Deploy the binary behind a secure host or as a containerized service if used beyond a personal workstation; implement rate‑limiting, secrets management, and monitoring of API health.  

Overall, CSswitch is a solid prototype for teams that need a flexible bridge between Claude‑style agents and multiple LLM providers, but it should undergo a focused security and reliability review before being used in mission‑critical production pipelines.

### Русский

SuperJJ007/CSswitch — это macOS‑приложение, позволяющее перенаправлять запросы Claude Science к произвольным совместимым с OpenAI API (DeepSeek, Tongyi Qianwen и др.), сохраняя при этом поддержку вызова инструментов, Skill, MCP и локального выполнения кода, включая виртуальный вход без пароля. Типичный сценарий — интеграция AI‑агента с реальными сервисами и данными через единый протокол Model Context Protocol, что упрощает прототипирование и внутренние рабочие процессы. Проект находится на среднем уровне готовности к production: имеет рабочий Rust‑код, базовую документацию и небольшую, но активную пользовательскую базу, однако требует дополнительной проверки лицензии, безопасности и поддержки перед масштабным развертыванием.

### 中文

SuperJJ007/CSswitch 通过把 Claude Science 的推理请求转发至任意 OpenAI 兼容的第三方 API（如 DeepSeek、通义千问），实现工具调用、Skill、MCP 及代码执行的无缝衔接，同时提供 macOS 菜单栏客户端和本地虚拟登录跳过功能，旨在为个人学习研究提供灵活的 AI‑工具连接方案。典型的接入方式是将目标模型的 API 端点配置到 CSswitch 中，随后在 Claude Science 中使用其提供的统一接口即可调用外部工具和数据。由于项目仍处于原型阶段，依赖维护和安全性尚需进一步审查，生产可用性目前属于中等，适合用于内部验证或实验流程，正式产品化

## 🧭 Practical evaluation

**Value:** SuperJJ007/CSswitch helps connect AI assistants to real tools and data through a standard protocol.

**Best use cases**

- connect AI agents to tools
- ship Model Context Protocol servers
- standardize integrations

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** Medium: useful for prototypes or internal workflows, with dependency and maintenance checks before production.

**Quality signals**

- 39 GitHub stars
- 3 forks
- updated 2026-07-03
- primary language: Rust
- 13 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 15/100 |
| stars | 34/100 |
| topics | 100/100 |
| outlook | 70/100 |
| quality | 63/100 |
| recency | 80/100 |
| adoption | 29/100 |
| production | 68/100 |
| usefulness | 74/100 |
| integration | 62/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 300/100 |

---

<sub>🔭 Discovered 2026-07-03 · [View on GitHub](https://github.com/SuperJJ007/CSswitch) · [← Back to Mcp](./README.md)</sub>
