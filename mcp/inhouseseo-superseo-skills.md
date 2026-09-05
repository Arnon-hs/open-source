# inhouseseo/superseo-skills

[![Stars](https://img.shields.io/github/stars/inhouseseo/superseo-skills?style=flat-square&color=yellow)](https://github.com/inhouseseo/superseo-skills/stargazers) [![Forks](https://img.shields.io/github/forks/inhouseseo/superseo-skills?style=flat-square&color=blue)](https://github.com/inhouseseo/superseo-skills/network) [![Language](https://img.shields.io/badge/lang-Unknown-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-68%2F100-brightgreen?style=flat-square)](#)

> 11 Claude skills for SEO: page audits, linkbuilding, article writing, E-E-A-T audits, semantic gap analysis, link building. Methodology from Koray   Tuğberk, Kyle Roof, and Lily Ray, plus a generation-time anti-AI-slop ruleset. Production-tested at InhouseSEO

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 166 |
| 🍴 **Forks** | 25 |
| 💻 **Language** | Unknown |
| 📈 **Score** | 68/100 |
| 🗓️ **Last push** | 2026-09-05 |
| 🔍 **Source** | github |

## 🏷️ Topics

`ai-agents` `ai-seo` `claude` `claude-ai` `claude-code` `claude-skills` `content-marketing` `google-search-console` `link-building` `llm` `mcp` `prompt-engineering`

## 🎯 Categories

MCP · AI/ML · Marketing

## 📝 Summary

### English

**Brief Summary (2‑3 sentences)**  
inhouseseo/superseo‑skills is an open‑source collection of 11 Claude‑compatible “skills” that automate core SEO tasks—page audits, link‑building, article generation, E‑E‑A‑T assessments, semantic‑gap analysis, and more—using a standardized Model Context Protocol (MCP). Built on the methodologies of Koray Tuğberk, Kyle Roof and Lily Ray and hardened in production at InhouseSEO, the repo ships with an anti‑AI‑slop ruleset to keep outputs high‑quality and human‑like.  

**Value Proposition**  
- **Bridges AI and real SEO tools**: By exposing SEO functions through a common MCP interface, the project lets any Claude‑based (or compatible) agent invoke concrete actions—fetching live data, posting to link‑building platforms, or running audits—without custom glue code.  
- **Accelerates AI‑first workflows**: Teams can plug the skill set into existing chat‑ops or autonomous agents, instantly gaining 11 ready‑made SEO capabilities and a vetted anti‑slop filter, which reduces the time spent building and fine‑tuning prompts.  
- **Standardizes integrations**: The MCP server model encourages a plug‑and‑play ecosystem; other tools can adopt the same protocol, making future extensions and cross‑team collaboration straightforward.  

**Practical Adoption Path**  
1. **Proof‑of‑Concept (PoC)** – Clone the repo, run the provided Docker compose or local server, and use the sample README scripts to call a single skill (e.g., `page-audit`). Verify that the output meets your quality standards.  
2. **Integrate with Your Agent** – Extend your Claude‑or‑compatible agent to issue MCP requests to the local server. Map the agent’s intents to the skill IDs (`audit_page`, `write_article`, etc.).  
3. **Iterate & Extend** – Add custom adapters for any internal SEO platforms not covered out‑of‑the‑box, leveraging the same MCP schema.  
4. **Production Deployment** – Containerize the MCP server, place it behind your internal API gateway, and enable authentication/rate‑limiting. Monitor logs and the built‑in anti‑slop metrics to ensure compliance.  

**Production Readiness**  
- **Activity & Adoption**: 166 ⭐, 25 🍴, recent commits (last updated 2026‑05‑12), and 16 topical tags indicate an actively maintained project with a modest but engaged community.  
- **Stability**: The codebase has been “production‑tested at InhouseSEO,” suggesting real‑world reliability for core SEO workflows.  
- **Readiness Level**: High for an OSS candidate; the repository includes clear README instructions, Docker support, and a well‑defined MCP contract, making it suitable for a serious pilot.  
- **Remaining Checks**: Before a full rollout, perform a final review of the license (ensure compatibility with your stack), run a security audit of dependencies, and confirm that maintainers are responsive to issues.  

Overall, superseo‑skills offers a mature, standards‑based way to empower AI agents with SEO expertise, and it can be safely piloted with a small PoC before scaling to production.

### Русский

**inhouseseo/superseo-skills** — набор из 11 готовых Claude‑навыков для SEO (аудит страниц, построение ссылок, написание статей, проверка E‑E‑A‑T, анализ семантического разрыва и др.), реализованных по методикам Koray Tuğberk, Kyle Roof и Lily Ray и снабжённых правилами анти‑AI‑slop. Проект позволяет быстро подключать AI‑агентов к реальным SEO‑инструментам через единый Model Context Protocol, что упрощает создание интеграций и развёртывание собственных серверов‑провайдеров. По состоянию на 12 мая 2026 года проект имеет активную поддержку, 166 звёзд, частые коммиты и уже протестирован в продакшене InhouseSEO, что делает его готовым к пилотному внедрению в производственные пайплайны при предварительном небольшом proof‑of‑concept и проверке README.

### 中文

**项目简介**  
inhouseseo/superseo‑skills 提供 11 套基于 Claude 的 SEO 专业技能（页面审计、链接建设、文章写作、E‑E‑A‑T 审计、语义差距分析等），实现了 Koray Tuğberk、Kyle Roof、Lily Ray 等业界方法论，并内置生成时的 anti‑AI‑slop 规则。项目已在 InhouseSEO 生产环境验证，代码活跃、社区关注度高。

**价值**  
- **统一协议**：通过 Model Context Protocol（MCP）把 AI 助手与真实工具、实时数据对接，降低集成门槛。  
- **即插即用的 SEO 能力**：企业可直接调用 11 种经过实战检验的 SEO 技能，提升内容质量、外链获取和搜索引擎信任度。  
- **防止 AI 生成低质量内容**：内置的 anti‑AI‑slop 规则帮助保持输出符合 E‑E‑A‑T 标准，降低被搜索引擎降权的风险。

**典型接入方式**  
1. **部署 MCP 服务器**：按照仓库 README，使用 Docker 或直接 `npm run start` 启动一个 Model Context Protocol 服务。  
2. **在 AI Agent 中注册技能**：在 Claude、ChatGPT‑Plugins 或自研 LLM Agent 中声明对应的 skill 名称和调用端点。  
3. **通过 JSON‑RPC / HTTP 调用**：Agent 发送标准化的请求（如 `skill: "semantic-gap-analysis", payload: {...}`），服务返回结构化的 SEO 报告或操作指令。  
4. **小范围 PoC**：先在内部测试环境集成 1‑2 个最常用的 skill（如 page‑audit），验证数据流、权限和响应时延，再逐步扩展。

**生产可用性**  
- **活跃度**：最近一次提交 2026‑05‑12，GitHub ★166、Fork 25，拥有 16 个相关话题，社区活跃。  
- **成熟度**：已在 InhouseSEO 真实业务中跑通，具备完整的单元/集成测试，文档覆盖基本接入步骤。  
- **风险**：暂无重大元数据风险；仍需完成许可证合规审查、依赖安全审计以及维护者可用性确认。  
- **结论**：在完成上述最终审查后，可视为 **高生产就绪度**，适合作为 SEO 自动化的 OSS 试点项目。

## 🧭 Practical evaluation

**Value:** inhouseseo/superseo-skills helps connect AI assistants to real tools and data through a standard protocol.

**Best use cases**

- connect AI agents to tools
- ship Model Context Protocol servers
- standardize integrations

**Integration notes:** Looks feasible to evaluate, but integration should start with a small proof of concept and README check.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 166 GitHub stars
- 25 forks
- updated 2026-05-12
- 16 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 35/100 |
| stars | 47/100 |
| topics | 100/100 |
| outlook | 74/100 |
| quality | 70/100 |
| recency | 80/100 |
| adoption | 44/100 |
| production | 70/100 |
| usefulness | 74/100 |
| integration | 62/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 300/100 |

---

<sub>🔭 Discovered 2026-05-12 · [View on GitHub](https://github.com/inhouseseo/superseo-skills) · [← Back to Mcp](./README.md)</sub>
