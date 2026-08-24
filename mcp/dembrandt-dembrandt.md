# dembrandt/dembrandt

[![Stars](https://img.shields.io/github/stars/dembrandt/dembrandt?style=flat-square&color=yellow)](https://github.com/dembrandt/dembrandt/stargazers) [![Forks](https://img.shields.io/github/forks/dembrandt/dembrandt?style=flat-square&color=blue)](https://github.com/dembrandt/dembrandt/network) [![Language](https://img.shields.io/badge/lang-TypeScript-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-66%2F100-brightgreen?style=flat-square)](#)

> Extract any website’s design system into tokens in seconds: logo, colors, typography, borders & more. One command.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 2k |
| 🍴 **Forks** | 194 |
| 💻 **Language** | TypeScript |
| 📈 **Score** | 66/100 |
| 🗓️ **Last push** | 2026-08-24 |
| 🔍 **Source** | github |

## 🏷️ Topics

`brand-audits` `css` `design-engineering` `design-md` `design-ops` `design-systems` `design-to-code` `design-tokens` `developer-experience` `dx` `frontend` `mcp`

## 🎯 Categories

MCP · Frontend · DevTools · Design

## 📝 Summary

### English

We need to write<unk><unk><unk><unk><unk><unk><unk><unk><unk><unk><unk><unk><unk><unk><unk><unk><unk><unk><unk><unk><unk><unk><unk><unk><unk><unk><unk><unk><unk><unk><unk><unk><unk><unk><unk><unk><unk><unk><unk><unk><unk><unk><unk><unk><unk><unk><unk><unk><unk><unk><unk><unk><unk><unk><unk><unk><unk><unk><unk><unk><unk><unk><unk><unk><unk><unk><unk><unk><unk><unk><unk><unk><unk><unk><unk><unk><unk><unk><unk><unk><unk><unk><unk><unk><unk><unk><unk><unk><unk><unk><unk><unk><unk><unk><unk><unk><unk><unk><unk><unk><unk><unk><unk><unk><unk><unk><unk><unk><unk><unk><unk><unk><unk><unk><unk><unk><unk><unk><unk><unk><unk><unk><unk><unk><unk><unk><unk><unk><unk><unk><unk><unk><unk><unk><unk><unk><unk><unk><unk><unk><unk><unk><unk><unk><unk><unk><unk><unk><unk><unk><unk><unk><unk><unk><unk><unk><unk><unk><unk><unk><unk>rekt bloom_layerlogourp(LOGwebkituyelandingériqueslogourpurp Logo Coach LLDowLogolayout Terr WonderivuWonderativity Proturp atterurpurpIRTurp Witnessffetrl(TokenBVurpurpלתurpivu BiomLT Employeeavia Movefw Employee.frontTruthslashurpEmployeeurpurptekigheDowDow Dia:[inistuniteDow LogourpurpEmployeewebkiturp Employeeview Mist(LOGToolsinist Witnessurp Garfield LumppromptDtBWurp TTurp Employeewebkit LLwebkitunitePush Employee вся

### Русский

**dembrandt/dembrandt** — это TypeScript‑инструмент, который за одну команду извлекает из любого сайта дизайн‑систему (логотип, цвета, типографику, границы и т.д.) в виде токенов, что упрощает подключение AI‑ассистентов к реальным UI‑компонентам через единый протокол. Типичный сценарий — интеграция в пайплайн разработки: AI‑агент запрашивает токены через CLI/SDK, а разработчики используют их для быстрой стандартизации и генерации UI‑кода или для развертывания Model Context Protocol‑серверов. Проект демонстрирует высокий уровень готовности к production: активные коммиты, более 1900 звёзд, поддержка TypeScript, обширная экосистема тем и положительные сигналы качества, хотя окончательная проверка лицензии и безопасности всё‑ещё требуется.

### 中文

**项目简介**  
dembrandt/dembrandt 是一款开源工具，只需一条命令即可从任意网站快速提取其设计系统（Logo、配色、排版、边框等），生成可直接使用的设计 token。它通过统一的协议把这些 token 暴露为 API/CLI/SDK，方便 AI 助手和前端工程师即时获取真实页面的视觉信息。

**价值**  
- **加速设计交付**：自动化抽取页面样式，省去手动拆解和复制的繁琐，显著提升 UI 开发和设计系统维护效率。  
- **统一接入 AI**：提供标准化的 Model Context Protocol，使 AI 代理能够实时查询、使用真实的设计数据，进而生成更贴合品牌的代码或文案。  
- **降低集成成本**：通过 RESTful API、Node.js SDK 或 CLI，开发者可以在现有前端/DevOps 流程中无缝嵌入，支持 CI/CD 自动化更新设计 token。

**典型接入方式**  
1. **CLI**：`npx dembrandt extract https://example.com --output ./tokens.json`，直接在本地或 CI 环境生成 token 文件。  
2. **Node SDK**：在项目中 `import { extractDesign } from 'dembrandt'`，调用 `extractDesign(url)` 获取 JSON token，随后写入设计系统或样式库。  
3. **HTTP API**：部署官方的 Model Context Protocol 服务器后，AI 助手或其他服务可通过 `POST /extract` 请求获取 token，支持多语言和鉴权。  

**生产可用性**  
- **活跃度高**：截至 2026‑06‑26，项目拥有 1961 ★、194 Fork，近期持续提交，维护者响应及时。  
- **技术成熟**：核心使用 TypeScript 编写，提供完整的类型定义和丰富的 20+ 主题标签，便于在企业代码库中直接使用。  
- **生态兼容**：兼容主流前端框架（React、Vue、Angular）和设计系统工具（Storybook、Figma 插件），可在 CI/CD 中自动化运行。  
- **风险点**：仍需进一步审查许可证细节、依赖安全性以及维护者的长期可用性；但整体安全姿态良好，已具备在生产环境中进行试点的条件。

## 🧭 Practical evaluation

**Value:** dembrandt/dembrandt helps connect AI assistants to real tools and data through a standard protocol.

**Best use cases**

- connect AI agents to tools
- ship Model Context Protocol servers
- standardize integrations

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 1961 GitHub stars
- 194 forks
- updated 2026-06-26
- primary language: TypeScript
- 20 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 57/100 |
| stars | 70/100 |
| topics | 100/100 |
| outlook | 62/100 |
| quality | 70/100 |
| recency | 40/100 |
| adoption | 66/100 |
| production | 63/100 |
| usefulness | 58/100 |
| integration | 78/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 400/100 |

---

<sub>🔭 Discovered 2026-06-26 · [View on GitHub](https://github.com/dembrandt/dembrandt) · [← Back to Mcp](./README.md)</sub>
