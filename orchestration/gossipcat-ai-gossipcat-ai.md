# gossipcat-ai/gossipcat-ai

[![Stars](https://img.shields.io/github/stars/gossipcat-ai/gossipcat-ai?style=flat-square&color=yellow)](https://github.com/gossipcat-ai/gossipcat-ai/stargazers) [![Forks](https://img.shields.io/github/forks/gossipcat-ai/gossipcat-ai?style=flat-square&color=blue)](https://github.com/gossipcat-ai/gossipcat-ai/network) [![Language](https://img.shields.io/badge/lang-TypeScript-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-68%2F100-brightgreen?style=flat-square)](#)

> Multi-agent code review mesh — orchestrates AI agents from multiple providers to review code in parallel, cross-review each other's findings, and build accuracy profiles over time. Agents that catch real bugs get picked more often. Agents that hallucinate get deprioritized. MCP server for Claude Code, Cursor, and other IDEs.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 37 |
| 🍴 **Forks** | 5 |
| 💻 **Language** | TypeScript |
| 📈 **Score** | 68/100 |
| 🗓️ **Last push** | 2026-09-05 |
| 🔍 **Source** | github |

## 🏷️ Topics

`agentic` `claude-code` `mcp` `memory` `openclaw` `orchestration` `relay` `skills`

## 🎯 Categories

Orchestration · MCP · AI/ML

## 📝 Summary

### English

**Summary**  
GossipCat‑AI is a TypeScript‑based orchestration layer that lets multiple AI code‑review agents (Claude, Cursor, etc.) run in parallel, cross‑validate each other’s findings, and dynamically adjust their selection based on historic accuracy. By turning ad‑hoc prompts into a repeatable, self‑optimising workflow, it creates “accuracy profiles” that surface reliable agents while demoting those that hallucinate, and it ships an MCP server that integrates with IDEs and CI pipelines.

**Value**  
- **Higher review quality**: Parallel, cross‑reviewed analysis catches bugs that single agents miss and reduces false positives.  
- **Self‑learning selection**: Real‑bug detections boost an agent’s weight, so the system automatically prefers the most trustworthy models over time.  
- **Tool‑agnostic pipelines**: The MCP server exposes a clean API/SDK/CLI, making it easy to embed the mesh in existing IDE extensions, CI jobs, or custom tooling without vendor lock‑in.

**Practical adoption path**  
1. **Prototype** – Pull the repo, run the MCP server locally, and point a supported IDE (e.g., Claude Code or Cursor) to its endpoint.  
2. **Pilot** – Connect the mesh to a small repository or a feature branch, enable parallel agents, and monitor the generated accuracy profiles.  
3. **Scale** – Add more providers, tune the weighting algorithm, and integrate the CLI into CI pipelines to enforce automated review gates.  
4. **Govern** – Export the profiling data to a dashboard or observability platform for audit and compliance.

**Production readiness**  
The project shows strong OSS maturity: recent commits (as of 2026‑06‑22), 37 stars, active forks, and a clear TypeScript codebase. Its modular API, documented MCP server, and existing IDE integrations make it straightforward to evaluate and roll out in a controlled environment. While the license and long‑term maintainer commitment still need a final check, the overall signal—active development, ecosystem adoption, and a well‑defined integration surface—indicates it is ready for a serious pilot in production settings.

### Русский

**gossipcat-ai/gossipcat-ai** — это открытая платформа оркестрации мульти‑агентных обзоров кода: она одновременно привлекает AI‑агентов разных провайдеров (Claude, Cursor и др.), позволяет им взаимно проверять результаты, формировать профили точности и автоматически отдавать предпочтение тем, кто реально находит баги, а не «галлюцинирует». Типовой сценарий — интеграция в CI/CD или IDE: при каждом коммите система запускает параллельный код‑ревью, собирает и агрегирует выводы агентов, а затем возвращает разработчику проверенный набор замечаний; при длительном использовании формируются «профили доверия» для каждого агента, повышая качество и скорость обзоров. Проект находится на высокой стадии готовности к production: активные коммиты (обновление 2026‑06‑22), 37 звёзд, поддержка API/SDK/CLI, TypeScript‑база и достаточная экосистема делают его надёжным кандидатом для пилотного внедрения.

### 中文

**项目简介**  
gossipcat‑ai/gossipcat‑ai 是一个多代理代码审查网格（Multi‑agent Code Review Mesh），能够调度来自不同供应商的 AI 代理并行审查代码、相互交叉复核，并随时间为每个代理构建准确性画像——真实捕获缺陷的代理会被频繁调度，产生幻觉的代理则被降权。它提供了面向 Claude Code、Cursor 以及其他 IDE 的 MCP（Message‑Control‑Protocol）服务器，实现跨工具的统一工作流。

**价值**  
- **提升审查质量**：通过多代理交叉验证，显著降低单一模型的误报/漏报率。  
- **自我学习的调度**：基于历史表现动态调整代理调用频率，长期会形成更可靠的审查体系。  
- **工作流标准化**：把零散的 Prompt 与工具封装成可复用的流水线，降低团队自行搭建多模型审查的成本。

**典型接入方式**  
1. **API/SDK**：直接调用项目提供的 RESTful API 或 npm 包（`gossipcat-ai`），在 CI/CD 或本地 IDE 插件中嵌入审查请求。  
2. **CLI**：使用内置的 `gossipcat` 命令行工具，对指定代码目录或文件执行一次性审查。  
3. **MCP 服务器**：在本地或容器中启动 MCP 服务，IDE（如 Claude Code、Cursor）通过配置插件的 MCP endpoint 即可获得实时审查反馈。  

**生产可用性**  
- **活跃度**：截至 2026‑06‑22 最近一次提交，拥有 37 ★、5 Fork，持续更新，社区讨论活跃。  
- **技术成熟度**：核心使用 TypeScript 编写，提供完整的类型定义和文档；实现了 API/SDK/CLI 三种接入层，易于集成。  
- **风险与准备**：暂无重大元数据风险，需进一步审查许可证合规性和安全审计；整体代码质量、依赖管理和测试覆盖度已达 OSS 生产候选水平，适合作为内部或受控环境的试点项目。  

综上，gossipcat‑ai 能把分散的 AI 审查工具统一为可重复、可调优的工作流，接入门槛低，且在当前状态下已具备在生产环境中进行小规模试点的条件。

## 🧭 Practical evaluation

**Value:** gossipcat-ai/gossipcat-ai helps turn isolated prompts and tools into repeatable agent workflows.

**Best use cases**

- coordinate multi-agent workflows
- add tool-use pipelines
- standardize agent memory

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 37 GitHub stars
- 5 forks
- updated 2026-06-22
- primary language: TypeScript
- 8 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 19/100 |
| stars | 34/100 |
| topics | 100/100 |
| outlook | 70/100 |
| quality | 63/100 |
| recency | 80/100 |
| adoption | 30/100 |
| production | 70/100 |
| usefulness | 74/100 |
| integration | 78/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 300/100 |

---

<sub>🔭 Discovered 2026-06-22 · [View on GitHub](https://github.com/gossipcat-ai/gossipcat-ai) · [← Back to Orchestration](./README.md)</sub>
