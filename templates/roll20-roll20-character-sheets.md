# Roll20/roll20-character-sheets

[![Stars](https://img.shields.io/github/stars/Roll20/roll20-character-sheets?style=flat-square&color=yellow)](https://github.com/Roll20/roll20-character-sheets/stargazers) [![Forks](https://img.shields.io/github/forks/Roll20/roll20-character-sheets?style=flat-square&color=blue)](https://github.com/Roll20/roll20-character-sheets/network) [![Language](https://img.shields.io/badge/lang-HTML-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-56%2F100-brightgreen?style=flat-square)](#)

> Character sheet templates created by the community for use in Roll20 VTT. Submit a ticket at roll20.net/help if critical hotfixes are to be requested.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 1.2k |
| 🍴 **Forks** | 4.3k |
| 💻 **Language** | HTML |
| 📈 **Score** | 56/100 |
| 🗓️ **Last push** | 2026-08-24 |
| 🔍 **Source** | github |

## 🏷️ Topics

`hacktoberfest`

## 🎯 Categories

Templates

## 📝 Summary

### English

**Brief Summary**  
Roll20/roll20‑character‑sheets is a community‑maintained repository of HTML‑based character sheet templates for the Roll20 virtual tabletop. The sheets can be dropped into a Roll20 game to give players a ready‑made UI for tracking stats, inventory, and abilities, and the project is actively forked and starred on GitHub.

**Value**  
The collection provides a curated set of UI components that can be repurposed as a front‑end for AI‑driven gameplay features—such as automated stat calculations, natural‑language‑to‑action parsing, or retrieval‑augmented generation (RAG) of character back‑stories—without having to build a sheet from scratch. Because the templates are already structured for data binding, they serve as a convenient “sandbox” for prototyping AI agents that read/write character data in real time.

**Practical Adoption Path**  
1. **Proof‑of‑Concept** – Clone the repo, pick a single sheet that matches your game system, and run it locally to confirm the HTML/CSS works in Roll20.  
2. **Integration** – Add a lightweight middleware (e.g., a Node.js server or a serverless function) that reads the sheet’s JSON payloads, invokes your AI model, and writes back updated values via Roll20’s API.  
3. **Iterate** – Extend the middleware to support RAG or agent workflows, using the sheet’s field IDs as prompts for the model.  
4. **README & Tests** – Verify the repository’s README instructions, add automated tests for the data exchange, and lock down dependencies.

**Production Readiness**  
- **Maturity**: Medium. The repo is popular (1,231 stars, 4,288 forks) and actively updated, making it reliable for internal prototypes.  
- **Dependencies**: Pure HTML/CSS with minimal JavaScript; integration work is isolated to your own backend, keeping the attack surface small.  
- **Risks**: License compliance, security posture of any third‑party scripts, and the need for an active maintainer to address critical bugs must be confirmed before a public release.  
- **Recommendation**: Start with a small, isolated proof‑of‑concept, perform a security/license audit, and only promote to production once the integration layer is hardened and monitoring is in place.

### Русский

Резюме проекта Roll20/roll20-character-sheets:

Этот open-source проект предоставляет шаблоны листов персонажей, созданных сообществом для использования в онлайн-платформе Roll20. Он позволяет добавлять функции AI без создания новой модели стека, что делает его ценным инструментом для прототипирования и внутренних рабочих процессов. Проект готов к использованию в прототипах и внутренних рабочих процессах, но требует проверки зависимостей и поддержки перед внедрением в производство.

### 中文

**项目简介（2‑3 句话）**  
Roll20/roll20-character-sheets 是社区贡献的 Roll20 虚拟桌面（VTT）角色卡模板库，提供可直接在 Roll20 中使用的 HTML/JS 表单。若发现关键 bug，可在 roll20.net/help 提交工单请求紧急修复。

---

## 价值

1. **快速落地 AI 功能**：模板已经内置了表单、计算和数据绑定逻辑，开发者只需在此基础上嵌入 AI 调用（如 LLM 生成角色背景、自动计算属性），无需从零搭建完整的角色卡系统。  
2. **原型与实验平台**：适合作为 RAG（检索增强生成）或智能代理的前端入口，帮助团队快速验证 AI 交互、自动化规则或剧情生成的可行性。  
3. **社区维护与可见度**：拥有 1.2k+ 星、4.3k+ Fork，活跃的社区贡献意味着模板质量和兼容性相对可靠，且易于获取使用案例和改进建议。

## 典型接入方式

| 步骤 | 操作 | 说明 |
|------|------|------|
| 1️⃣ | **Fork / Clone** | 将仓库 fork 到自己的组织或直接 clone 到本地工作区。 |
| 2️⃣ | **本地调试** | 在本机启动一个轻量 HTTP 服务器（如 `python -m http.server`），在 Roll20 中使用 “Import Sheet” 功能加载本地 HTML。 |
| 3️⃣ | **嵌入 AI 调用** | 在模板的 `<script>` 中引入后端 API（REST、GraphQL 或 WebSocket），例如调用 OpenAI、Claude、或自研模型的对话接口，实现自动生成角色描述、技能建议等。 |
| 4️⃣ | **数据持久化** | 使用 Roll20 的 `setAttrs` / `getAttrs` 接口将 AI 生成的结果写回角色卡，或通过外部数据库（如 Firebase）同步。 |
| 5️⃣ | **部署** | 将修改后的模板推送到公开仓库或内部私有仓库，使用 Roll20 的 “Sheet URL” 功能指向该地址，供玩家在实际游戏中使用。 |
| 6️⃣ | **CI/CD（可选）** | 配置 GitHub Actions 检查 HTML/JS 语法、依赖安全（npm audit）以及自动化部署到 CDN（如 Cloudflare Pages）。 |

> **小贴士**：如果只想验证 AI 能力，可先在本地用静态 HTML 加载 OpenAI 的 `fetch` 示例，确认返回结构后再迁移到 Roll20 环境。

## 生产可用性评估

| 维度 | 评估 | 说明 |
|------|------|------|
| **成熟度** | 中等 | 模板本身成熟、社区活跃，但 AI 集成仍需自行实现，缺少官方的 AI 插件或 SDK。 |
| **依赖风险** | 低‑中 | 主要依赖浏览器原生 API 与 Roll20 提供的 `setAttrs/getAttrs`，外部依赖（如 npm 包）可自行锁定版本。 |
| **安全性** | 待评估 | 需要审查模板中是否存在 XSS 漏洞，以及 AI 调用的身份验证方式（API Key 管理）。 |
| **运维成本** | 低 | 只需维护 HTML/JS 代码和后端 AI 接口，部署成本可通过 CDN 或静态站点托管解决。 |
| **上线建议** | **先做 PoC → 代码审计 → 小范围内部测试 → 逐步推广** | 先在内部玩家组进行功能验证，确认 AI 调用的响应时间、费用与可靠性后，再面向更大社区发布。 |

**结论**：Roll20/roll20-character-sheets 适合作为 AI‑增强角色卡的原型平台，具备快速集成的优势。通过一次小规模的 PoC 并完成安全审计后，即可在内部或受控的生产环境中使用；若要面向公开玩家，需要进一步完善权限管理和持续维护机制。

## 🧭 Practical evaluation

**Value:** Roll20/roll20-character-sheets helps add AI capability without starting from a blank model stack.

**Best use cases**

- prototype AI features
- build RAG or agent workflows
- evaluate model tooling

**Integration notes:** Looks feasible to evaluate, but integration should start with a small proof of concept and README check.

**Production readiness:** Medium: useful for prototypes or internal workflows, with dependency and maintenance checks before production.

**Quality signals**

- 1231 GitHub stars
- 4288 forks
- updated 2026-07-02
- primary language: HTML
- 1 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 91/100 |
| stars | 66/100 |
| topics | 13/100 |
| outlook | 55/100 |
| quality | 60/100 |
| recency | 40/100 |
| adoption | 73/100 |
| production | 55/100 |
| usefulness | 58/100 |
| integration | 46/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 100/100 |

---

<sub>🔭 Discovered 2026-07-02 · [View on GitHub](https://github.com/Roll20/roll20-character-sheets) · [← Back to Templates](./README.md)</sub>
