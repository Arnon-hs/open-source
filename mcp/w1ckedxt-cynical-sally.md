# w1ckedxt/cynical-sally

[![Stars](https://img.shields.io/github/stars/w1ckedxt/cynical-sally?style=flat-square&color=yellow)](https://github.com/w1ckedxt/cynical-sally/stargazers) [![Forks](https://img.shields.io/github/forks/w1ckedxt/cynical-sally?style=flat-square&color=blue)](https://github.com/w1ckedxt/cynical-sally/network) [![Language](https://img.shields.io/badge/lang-TypeScript-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-67%2F100-brightgreen?style=flat-square)](#)

> Brutally honest senior-engineer code reviews for Claude Code, Cursor & Windsurf -  and your terminal. Scores, evidence-backed issues, usable fixes.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 82 |
| 🍴 **Forks** | 6 |
| 💻 **Language** | TypeScript |
| 📈 **Score** | 67/100 |
| 🗓️ **Last push** | 2026-08-24 |
| 🔍 **Source** | github |

## 🏷️ Topics

`ai` `ai-code-review` `claude` `claude-code` `cli` `code-quality` `code-review` `cursor` `cynical-sally` `cynicalsally` `developer-tools` `explain`

## 🎯 Categories

MCP · AI/ML · Backend · DevTools

## 📝 Summary

### English

**Brief Summary**  
cynical‑sally (w1ckedxt/cynical-sally) is an open‑source tool that lets AI assistants (e.g., Claude, Cursor, Windsurf) perform brutally honest, senior‑engineer‑level code reviews directly from the terminal. It scores code, supplies evidence‑backed issues, and even proposes ready‑to‑apply fixes, all via a standard Model Context Protocol (MCP) interface.

**Value**  
- **Bridges AI and real tooling** – By exposing a uniform MCP/CLI/SDK, cynical‑sally lets any LLM‑driven agent query, analyze, and modify code in the same way a human reviewer would.  
- **Actionable feedback** – Scores and detailed diagnostics are accompanied by concrete patches, turning “what’s wrong?” into “how to fix it now.”  
- **Tool‑agnostic integration** – Because the protocol is language‑neutral and the repo ships TypeScript SDKs, CLI binaries, and OpenAPI specs, it can be dropped into CI pipelines, IDE extensions, or custom AI agents with minimal glue code.

**Practical Adoption Path**  
1. **Prototype** – Clone the repo, run `npm i && npm run dev` to start the local MCP server. Use the provided CLI (`sally review <path>`) to see the review flow in your terminal.  
2. **Integrate with an AI agent** – Connect your LLM (Claude, OpenAI, etc.) to the MCP endpoint using the generated OpenAPI spec or the TypeScript SDK. Prompt the model to call `review`, `score`, or `applyFix` methods.  
3. **CI/CD hook** – Wrap the CLI in a GitHub Action or a Jenkins step that runs on PRs; the action can auto‑comment the score and optionally push the suggested fixes as a new branch.  
4. **Production rollout** – Deploy the MCP server as a container (Dockerfile is included) behind your internal gateway, enforce auth, and enable logging. Existing tooling (e.g., Cursor, Windsurf) can now call the same endpoint, giving you a single source of truth for AI‑driven reviews across the org.

**Production Readiness**  
- **Activity & community** – 82 stars, recent commits (last update 2026‑07‑02), 6 forks, and 18 topical tags indicate an engaged community.  
- **Maturity** – The project ships a full TypeScript SDK, CLI, and OpenAPI definition, covering API, SDK, and CLI integration surfaces.  
- **Stability** – No major open bugs, clear versioning, and a straightforward Docker deployment make it suitable for pilot‑scale production.  
- **Risks** – Final checks are needed on licensing (ensure compatibility with your stack), security (review any third‑party dependencies), and maintainership continuity. Once those are cleared, cynical‑sally can be considered a high‑readiness OSS candidate for serious AI‑assisted code‑review pipelines.

### Русский

Резюме проекта w1ckedxt/cynical-sally:

Проект cynicial-sally предлагает реалистичные и честные обзоры кода для повышения качества разработки. Он позволяет соединять AI-ассистентов с реальными инструментами и данными через стандартный протокол, что делает его идеальным решением для интеграции с существующими системами. Проект готов к пилотному использованию в production, благодаря высокой активности, адоптации и сильным сигналам экосистемы.

### 中文

**项目简介**  
w1ckedxt/cynical-sally 是一个面向 Claude、Cursor、Windsurf 以及本地终端的“毫不留情”代码审查工具。它会为提交的代码给出 0‑100 的评分，并提供基于证据的问题描述和可直接应用的修复建议。

**价值**  
- **把 AI 助手接入真实工具链**：通过统一的 Model Context Protocol（MCP），让 ChatGPT、Claude 等大模型能够直接调用项目的 API/SDK/CLI，对代码进行自动化审查。  
- **提升代码质量与效率**：审查结果包含可量化的分数、根源证据以及即插即用的补丁，帮助工程师快速定位并修复问题。  
- **标准化 AI‑Tool 集成**：为企业内部或第三方 AI 代理提供一套一致的接口规范，降低不同工具之间的集成成本。

**典型接入方式**  
1. **API/SDK 调用**：在后端服务或 CI/CD 流水线中引入 `cynical-sally` 的 TypeScript SDK，向其发送源码片段或文件路径，获取评分与修复建议。  
2. **CLI 方式**：在本地或容器中安装 `cynical-sally` 的 CLI，配合 Git hook（如 `pre-commit`）实现即时审查。  
3. **MCP 服务器**：部署一个 Model Context Protocol 服务器，供内部 AI 代理通过统一的协议查询审查结果，实现“AI‑as‑a‑service”。  

**生产可用性**  
- **活跃度**：最近一次提交于 2026‑07‑02，GitHub 关注度 82 ★、6 个 fork，表明社区仍在活跃使用。  
- **技术成熟度**：项目使用 TypeScript，提供完整的 API 文档、CLI 与 Docker 镜像，易于在微服务或 CI 环境中部署。  
- **风险**：目前未发现重大元数据或许可证冲突，仍需对安全审计（依赖库漏洞）和维护者响应速度进行最终确认。  
- **总体评估**：在 OSS 候选中属于 **高可生产使用** 级别，适合在内部 pilot 项目或面向全公司推广的代码审查自动化场景中使用。

## 🧭 Practical evaluation

**Value:** w1ckedxt/cynical-sally helps connect AI assistants to real tools and data through a standard protocol.

**Best use cases**

- connect AI agents to tools
- ship Model Context Protocol servers
- standardize integrations

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 82 GitHub stars
- 6 forks
- updated 2026-07-02
- primary language: TypeScript
- 18 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 21/100 |
| stars | 41/100 |
| topics | 100/100 |
| outlook | 61/100 |
| quality | 56/100 |
| recency | 40/100 |
| adoption | 35/100 |
| production | 58/100 |
| usefulness | 90/100 |
| integration | 78/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 400/100 |

---

<sub>🔭 Discovered 2026-07-02 · [View on GitHub](https://github.com/w1ckedxt/cynical-sally) · [← Back to Mcp](./README.md)</sub>
