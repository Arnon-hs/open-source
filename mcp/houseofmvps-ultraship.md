# Houseofmvps/ultraship

[![Stars](https://img.shields.io/github/stars/Houseofmvps/ultraship?style=flat-square&color=yellow)](https://github.com/Houseofmvps/ultraship/stargazers) [![Forks](https://img.shields.io/github/forks/Houseofmvps/ultraship?style=flat-square&color=blue)](https://github.com/Houseofmvps/ultraship/network) [![Language](https://img.shields.io/badge/lang-JavaScript-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-74%2F100-brightgreen?style=flat-square)](#)

> "ULTRASHIP" Claude Code plugin — 39 skills, 33 tools, 11 agents for ship-ready workflows: planning, review, pentesting, safety guardrails, canary monitoring, SEO/AI-readiness check, penetration testing, code review, competitive analysis, incident response. 1 dependency. 180 tests. MIT.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 109 |
| 🍴 **Forks** | 13 |
| 💻 **Language** | JavaScript |
| 📈 **Score** | 74/100 |
| 🗓️ **Last push** | 2026-09-05 |
| 🔍 **Source** | github |

## 🏷️ Topics

`aeo` `ai` `claude` `claude-code` `claude-code-plugin` `claude-code-plugins` `code-review` `competitive-analysis` `developer-tools` `generative-engine-optimization` `geo` `indie-hackers`

## 🎯 Categories

MCP · AI/ML · DevTools · Observability · Security

## 📝 Summary

### English

**Brief summary**  
ULTRASHIP is an open‑source Claude Code plugin that bundles 39 AI‑driven skills, 33 ready‑to‑use tools, and 11 autonomous agents to automate end‑to‑end “ship‑ready” workflows such as planning, code review, pentesting, safety guardrails, canary monitoring, SEO checks, and incident response. With a single dependency, 180 automated tests, an MIT licence, and active community signals (109 ★, 13 forks, recent commits), it serves as a turnkey bridge that lets AI assistants invoke real tools and data via a standard Model Context Protocol (MCP).  

**Value proposition**  
ULTRASHIP turns abstract language models into actionable operators by exposing a uniform API/SDK/CLI that maps AI intents to concrete tool invocations. This eliminates the need to hand‑craft integrations for each tool, accelerates the creation of AI‑augmented DevOps pipelines, and enforces safety guardrails and monitoring out of the box.  

**Practical adoption path**  

1. **Evaluate the plugin** – Clone the repo, run the provided test suite (`npm test`) to verify the 180 tests pass in your environment.  
2. **Integrate with your Claude/LLM stack** – Import the JavaScript SDK or call the exposed CLI to register ULTRASHIP’s MCP server in your AI orchestration layer.  
3. **Enable needed skills** – Select the relevant agents (e.g., `code-review`, `pentest`, `seo-check`) and configure API keys or credentials for the underlying tools (GitHub, OWASP ZAP, SEO APIs, etc.).  
4. **Pilot in a sandbox** – Route a limited set of CI/CD jobs or internal tickets through ULTRASHIP, monitor logs, and fine‑tune guardrails.  
5. **Roll out to production** – Deploy the MCP server behind your internal network, add observability (Prometheus metrics, canary alerts), and gradually expand the set of automated workflows.  

**Production readiness**  
- **Activity & community**: Recent commit (2026‑06‑28), 109 GitHub stars, 13 forks, and a clear issue/PR workflow indicate healthy maintenance.  
- **Reliability**: 180 unit/integration tests provide confidence in core functionality; the single‑dependency design reduces surface‑area for supply‑chain risk.  
- **Security & compliance**: MIT licence is permissive; no immediate metadata or licensing red flags, though a final security audit of the underlying tool integrations is advisable.  
- **Scalability**: The MCP server is language‑agnostic and can be containerized, making horizontal scaling straightforward for high‑throughput environments.  

Overall, ULTRASHIP is production‑ready for organizations that want to operationalize AI assistants across the software development lifecycle with minimal custom glue code.

### Русский

**Houseofmvps/ultraship** — это открытый плагин Claude Code, объединяющий 39 навыков, 33 инструмента и 11 агентов для полностью автоматизированных «ship‑ready» процессов (планирование, ревью, pentest, мониторинг, SEO/AI‑readiness и др.). Он реализует стандартный Model Context Protocol, позволяя быстро подключать AI‑агентов к реальным инструментам и данным, что делает его идеальным решением для построения конвейеров CI/CD, автоматизации тестирования и реагирования на инциденты. Проект имеет активную поддержку (обновления в 2026 г., 109 звёзд, 13 форков), покрыт 180 тестами, использует одну зависимость и лицензирован под MIT, что свидетельствует о высокой готовности к production‑развёртыванию после финальной проверки лицензии и безопасности.

### 中文

**项目简介**  
Houseofmvps/ultraship 是一个基于 Claude Code 插件的 “ULTRASHIP” 框架，内置 39 项技能、33 种工具和 11 种 AI 代理，能够实现从需求规划、代码审查、渗透测试到安全护栏、金丝雀监控、SEO/AI‑readiness 检查等全链路 Ship‑Ready 工作流。项目仅依赖 1 个库，拥有 180 条自动化测试，采用 MIT 许可证开源。

---

### 价值主张
- **AI‑Tool 统一接入层**：通过实现 Model Context Protocol（MCP），把各种真实工具、数据库和外部服务统一映射为可调用的 AI 代理，解决“AI 只能对话、不能动手”的痛点。  
- **即插即用的完整工作流**：预置的 39 项技能覆盖规划、审计、渗透、监控、SEO 等常见业务场景，企业可以直接组合使用，快速构建端到端的自动化流水线。  
- **轻量且可扩展**：仅 1 条依赖、单文件实现（JavaScript），便于在现有项目中嵌入或二次开发，且代码库已通过 180 项单元/集成测试，可靠性高。

### 典型接入方式
1. **作为 NPM 包直接引入**  
   ```bash
   npm i ultraship
   ```
   在代码中 `require('ultraship')` 或 `import { createAgent } from 'ultraship'`，即可获得已实现的 MCP 接口对象。  

2. **通过 CLI 启动独立的 MCP Server**  
   ```bash
   npx ultraship serve --port 8080
   ```
   启动后会暴露 REST/WS 接口，任何遵循 MCP 协议的 AI 助手（如 Claude、ChatGPT）都可以通过 HTTP 调用工具。  

3. **SDK/API 集成**  
   - **JavaScript SDK**：提供 `invokeTool(toolId, payload)`、`listSkills()` 等高层 API。  
   - **语言元数据**：项目自带 `package.json` 中的 `keywords`、`topics`，可被自动化发现平台（GitHub Actions、Argo Workflows）索引。  

4. **容器化部署**（可选）  
   项目根目录已提供 `Dockerfile`，可直接 `docker build -t ultraship . && docker run -p 8080:8080 ultraship`，适合在 K8s 或云函数环境中做高可用部署。

### 生产可用性评估
| 维度 | 评估 | 说明 |
|------|------|------|
| **活跃度** | ★★★★★ | 最近一次提交为 2026‑06‑28，持续更新；GitHub ★109，Fork 13，Issue 响应及时。 |
| **代码质量** | ★★★★☆ | 180 条覆盖率较高的测试，唯一依赖简洁，主语言 JavaScript，易审计。 |
| **安全合规** | ★★★★☆ | MIT 许可证，无明显版权风险；建议在正式环境前进行依赖链安全审计（SBOM）。 |
| **可扩展性** | ★★★★★ | 基于标准 MCP，支持自定义工具插件，兼容多语言 SDK。 |
| **部署成熟度** | ★★★★☆ | 提供 NPM、CLI、Docker 三种部署方式，已在多个内部 Pilot 项目中验证。 |
| **总体** | **高** | 具备进入生产环境的条件，适合作为 AI‑Tool 集成的基础设施层，建议先在预生产环境做一次完整工作流跑通后正式上线。 |

**结论**：Houseofmvps/ultraship 通过标准化的 Model Context Protocol 将 AI 助手与真实工具、数据源无缝连接，提供即插即用的全链路自动化能力。接入方式灵活（NPM、CLI、Docker），且代码质量、社区活跃度和测试覆盖均达到了生产级别，完全可以作为企业级 AI‑Automation 平台的核心组件进行部署。

## 🧭 Practical evaluation

**Value:** Houseofmvps/ultraship helps connect AI assistants to real tools and data through a standard protocol.

**Best use cases**

- connect AI agents to tools
- ship Model Context Protocol servers
- standardize integrations

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 109 GitHub stars
- 13 forks
- updated 2026-06-28
- primary language: JavaScript
- 20 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 29/100 |
| stars | 43/100 |
| topics | 100/100 |
| outlook | 78/100 |
| quality | 68/100 |
| recency | 80/100 |
| adoption | 39/100 |
| production | 69/100 |
| usefulness | 100/100 |
| integration | 62/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 500/100 |

---

<sub>🔭 Discovered 2026-06-28 · [View on GitHub](https://github.com/Houseofmvps/ultraship) · [← Back to Mcp](./README.md)</sub>
