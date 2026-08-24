# wanshuiyin/Anti-Autoresearch

[![Stars](https://img.shields.io/github/stars/wanshuiyin/Anti-Autoresearch?style=flat-square&color=yellow)](https://github.com/wanshuiyin/Anti-Autoresearch/stargazers) [![Forks](https://img.shields.io/github/forks/wanshuiyin/Anti-Autoresearch?style=flat-square&color=blue)](https://github.com/wanshuiyin/Anti-Autoresearch/network) [![Language](https://img.shields.io/badge/lang-Python-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-59%2F100-brightgreen?style=flat-square)](#)

> Don't trust an autoresearch paper at face value. Reviewer-side integrity forensics (self-consistency + fabrication), deterministic verdict. 61 signals: 46 integrity hack-patterns (families A–H, verdict-bearing) + 13 zero-weight AI writing-style impressions (AIS) + 2 advisory. Not an opaque AI-text classifier. The dual of ARIS.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 63 |
| 🍴 **Forks** | 2 |
| 💻 **Language** | Python |
| 📈 **Score** | 59/100 |
| 🗓️ **Last push** | 2026-08-24 |
| 🔍 **Source** | github |

## 🏷️ Topics

`ai-generated-content` `ai-research` `ai-scientist` `aris` `autoresearch` `claude` `claude-code` `claude-code-skills` `codex` `forensics` `gpt` `llm`

## 🎯 Categories

MCP · AI/ML

## 📝 Summary

### English

**Brief Summary**  
Anti‑Autoresearch is a Python‑based forensic toolkit that evaluates the trustworthiness of AI‑generated research papers. By analysing 61 signals—including 46 “integrity hack‑patterns” and 13 AI‑writing‑style impressions—it produces a deterministic, reviewer‑side verdict on self‑consistency and possible fabrication, offering a transparent alternative to black‑box text classifiers.

**Value Proposition**  
- **Concrete integrity checks** – The signal set maps directly to known manipulation patterns (families A‑H), giving reviewers actionable evidence rather than a vague “spam‑score.”  
- **Standardised integration** – Exposes a clean API/SDK/CLI that can be wrapped by any AI assistant or Model Context Protocol (MCP) server, turning the tool into a plug‑and‑play “integrity micro‑service.”  
- **Dual of ARIS** – Complements existing autoresearch detection (ARIS) by focusing on the reviewer’s perspective, completing a bidirectional trust‑loop for scholarly AI pipelines.  

**Practical Adoption Path**  

| Step | What to Do | Why |
|------|------------|-----|
| 1️⃣ Evaluate locally | Clone the repo, run the supplied CLI on a few sample PDFs/Markdowns. | Verify signal extraction works with your document formats. |
| 2️⃣ Wrap the API | Deploy the Python package as a lightweight Flask/FastAPI service exposing `/analyze`. | Provides a language‑agnostic endpoint that any AI agent can call. |
| 3️⃣ Connect to MCP | Register the service as an MCP “integrity” node, publishing its OpenAPI spec. | Enables other tools (e.g., citation managers, peer‑review platforms) to request deterministic verdicts. |
| 4️⃣ Pilot in workflow | Add a step in your review pipeline (e.g., after OCR, before human scoring) that automatically flags high‑risk papers. | Demonstrates ROI by reducing manual sanity‑checking time. |
| 5️⃣ Monitor & tune | Log signal scores, collect reviewer feedback, and optionally adjust the weight of the 13 AIS impressions. | Improves precision for your domain and builds a feedback loop for future releases. |

**Production Readiness**  

- **Maturity** – Medium. The codebase is recent (last update 2026‑06‑30), well‑documented, and has 63 ★ on GitHub, but only 2 forks, indicating limited real‑world stress testing.  
- **Dependencies** – Pure Python with optional PDF‑parsing libraries; easy to containerise. A review of third‑party packages for known CVEs is recommended before production deployment.  
- **Maintainability** – The repository is active, but the maintainer count is low; consider forking and adding internal CI/CD checks to guard against future stagnation.  
- **Security** – No obvious metadata leaks, but a formal license audit and runtime sandboxing (e.g., using gVisor or similar) are advisable because the tool processes untrusted documents.  

**Bottom Line**  
Anti‑Autoresearch offers a transparent, signal‑driven method for detecting fabricated or self‑inconsistent AI‑generated research, making it a valuable addition to any AI‑augmented scholarly workflow. With modest integration effort—exposing its API as an MCP service—it can be trialled in internal review pipelines today, while a short hardening phase (dependency audit, licensing check, CI) will bring it to a production‑ready state.

### Русский

**Краткое резюме:** wanshuiyin/Anti‑Autoresearch — это набор Python‑инструментов, который позволяет проверять научные статьи‑autoresearch на предмет самопротиворечий и подделок, используя 61 детектор (46 паттернов нарушения целостности, 13 нейтральных импрессий стиля ИИ и 2 советующих сигнала) и выдавая детерминированный вердикт без обращения к непрозрачным классификаторам. Типичный сценарий — интеграция проекта в пайплайн AI‑агентов через Model Context Protocol (MCP): серверы MCP получают сигналы о целостности, а фронтенд‑инструменты визуализируют результаты, что упрощает прототипирование и внутренние рабочие процессы. Готовность к production — средний уровень: проект стабилен для прототипов и внутренних систем, но требует проверки лицензии, безопасности и поддержки перед масштабным развертыванием.

### 中文

**项目简介**

wanshuiyin/Anti-Autoresearch 是一个开源项目，旨在检测自动生成的研究论文的真实性。它提供了 61 个信号，包括 46 个完整性攻击模式和 13 个 AI 生成文本风格的迹象。它不是一个黑盒式的 AI 文本分类器，而是一个透明的工具，旨在帮助连接 AI 助手与真实的工具和数据。

**价值**

wanshuiyin/Anti-Autoresearch 的价值在于它可以帮助连接 AI 代理与工具，标准化集成，并提供 Model Context Protocol 服务器。它可以用于连接 AI 代理与工具，实现 AI 和人工智能的高效集成。

**典型接入方式**

典型接入方式包括：

1. 连接 AI 代理与工具：通过 wanshuiyin/Anti-Autoresearch，可以连接 AI 代理与工具，实现 AI 和人工智能的高效集成。
2. 部署 Model Context Protocol 服务器：通过 wanshuiyin/Anti-Autoresearch，可以部署 Model Context Protocol 服务器

## 🧭 Practical evaluation

**Value:** wanshuiyin/Anti-Autoresearch helps connect AI assistants to real tools and data through a standard protocol.

**Best use cases**

- connect AI agents to tools
- ship Model Context Protocol servers
- standardize integrations

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** Medium: useful for prototypes or internal workflows, with dependency and maintenance checks before production.

**Quality signals**

- 63 GitHub stars
- 2 forks
- updated 2026-06-30
- primary language: Python
- 20 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 12/100 |
| stars | 38/100 |
| topics | 100/100 |
| outlook | 57/100 |
| quality | 54/100 |
| recency | 40/100 |
| adoption | 31/100 |
| production | 55/100 |
| usefulness | 74/100 |
| integration | 62/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 200/100 |

---

<sub>🔭 Discovered 2026-06-30 · [View on GitHub](https://github.com/wanshuiyin/Anti-Autoresearch) · [← Back to Mcp](./README.md)</sub>
