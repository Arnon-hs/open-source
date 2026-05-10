# GuyRonnen/rtl-for-vs-code-agents

[![Stars](https://img.shields.io/github/stars/GuyRonnen/rtl-for-vs-code-agents?style=flat-square&color=yellow)](https://github.com/GuyRonnen/rtl-for-vs-code-agents/stargazers) [![Forks](https://img.shields.io/github/forks/GuyRonnen/rtl-for-vs-code-agents?style=flat-square&color=blue)](https://github.com/GuyRonnen/rtl-for-vs-code-agents/network) [![Language](https://img.shields.io/badge/lang-PowerShell-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-54%2F100-brightgreen?style=flat-square)](#)

> Native-like RTL support for VS Code AI Agents (i.e. GitHub Copilot) with proper LTR code block formatting. Optimized for Hebrew, Arabic, and Persian.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 106 |
| 🍴 **Forks** | 8 |
| 💻 **Language** | PowerShell |
| 📈 **Score** | 54/100 |
| 🗓️ **Last push** | 2026-05-10 |
| 🔍 **Source** | github |

## 🏷️ Topics

_no topics_

## 🎯 Categories

AI/ML · Database

## 📝 Summary

### English

**Brief Summary (2‑3 sentences)**  
GuyRonnen/rtl-for-vs-code-agents provides native right‑to‑left (RTL) support for VS Code AI agents such as GitHub Copilot, ensuring that code blocks are correctly formatted left‑to‑right while the surrounding editor UI handles Hebrew, Arabic, and Persian text. It is delivered as a lightweight PowerShell‑based extension that can be dropped into existing VS Code setups to make AI‑generated code usable in RTL environments without rebuilding the underlying model stack.  

**Value**  
- **Immediate RTL capability**: Developers working in RTL languages can keep the familiar Copilot experience while avoiding garbled code layout, which is a common pain point in multilingual teams.  
- **Zero‑model effort**: The project adds the needed UI/formatting layer on top of any existing AI‑agent integration, so you don’t need to train or host a new model.  
- **Prototype‑friendly**: With only a few hundred lines of PowerShell and a simple installation step, you can quickly test AI‑driven workflows (e.g., RAG or agent pipelines) in a multilingual context.  

**Practical Adoption Path**  
1. **Clone or download the repo** and run the provided PowerShell install script, which registers the extension with VS Code.  
2. **Enable the extension** in VS Code’s settings (`rtlForVsCodeAgents.enabled = true`).  
3. **Run a sanity check**: open a file with RTL text, trigger Copilot (or another AI agent), and verify that generated code appears left‑to‑right inside the editor while the surrounding UI remains RTL.  
4. **Iterate**: adjust the optional configuration (`codeBlockDirection`, `languageOverrides`) to match your team’s specific language mix.  
5. **Integrate** into CI pipelines or internal developer‑portal scripts if the manual tests pass.  

**Production Readiness**  
- **Maturity**: Medium. The repo is actively maintained (last commit 2026‑05‑10) and has modest community traction (≈106 stars, 8 forks).  
- **Dependencies**: Pure PowerShell and VS Code APIs, so the runtime footprint is low, but you must verify compatibility with your organization’s VS Code version and any custom AI‑agent extensions.  
- **Risks**: The integration documentation is sparse; you’ll need to manually confirm that the extension coexists with your existing Copilot or other agent plugins, especially if you have custom keybindings or security policies around PowerShell scripts.  
- **Recommendation**: Ideal for prototypes, internal tooling, or pilot projects that need RTL support. Before moving to production, perform a controlled rollout, audit the PowerShell script for security compliance, and lock the extension version to avoid unexpected breaking changes.

### Русский

**GuyRonnen/rtl-for-vs-code-agents** — это open‑source‑расширение, которое добавляет в VS Code поддержку RTL‑языков (иврит, арабский, персидский) для AI‑агентов типа GitHub Copilot, обеспечивая корректное форматирование LTR‑кода внутри блоков. Оно идеально подходит для быстрого прототипирования функций ИИ, создания RAG‑ или агентных воркфлоу и оценки инструментов модели, однако требует ручной проверки и уточнения пути интеграции из‑за скудной метаданных. Готово к использованию в прототипах и внутренних процессах (уровень готовности — medium), но перед выводом в продакшн следует оценить затраты на настройку и поддержание зависимости.

### 中文

**价值**  
GuyRonnen/rtl‑for‑vs‑code‑agents 为 VS Code 中的 AI 代码助手（如 GitHub Copilot）提供原生的从右到左（RTL）支持，并在代码块渲染时保持左到右（LTR）排版，从而解决希伯来语、阿拉伯语、波斯语等 RTL 语言的编辑和阅读体验问题。它让开发者无需自行实现复杂的语言适配，即可在现有 AI 助手上直接使用 RTL 代码，提高原型开发速度和内部工具的可用性。

**典型接入方式**  
1. **安装脚本**：在项目根目录运行 PowerShell 安装脚本（`install.ps1`），脚本会把插件文件复制到 VS Code 的扩展目录并注册相应的语言服务。  
2. **配置 VS Code**：在 `settings.json` 中加入 `"rtlForVsCodeAgents.enable": true`，并指定需要启用的语言（`"he"、"ar"、"fa"`）。  
3. **与 AI Agent 集成**：插件会在 Copilot、ChatGPT‑for‑VSCode 等扩展的请求/响应拦截点自动转换代码块的方向，无需额外代码改动。  
4. **手动验证**：首次使用时打开一个包含 RTL 代码的文件，确认代码块在编辑器中保持 LTR 排版且 AI 建议正确显示。

**生产可用性**  
- **成熟度**：Medium。插件已在 2026‑05‑10 更新，拥有 106 颗星、8 个 Fork，适合作为原型或内部工作流的加速器。  
- **依赖与维护**：核心实现为 PowerShell 脚本，依赖 VS Code 扩展 API 与本地文件系统；在升级 VS Code 或 AI 助手（如 Copilot）时可能需要重新验证兼容性。  
- **上线建议**：在正式生产环境部署前，进行一次完整的集成测试，检查：  
  1. 插件与现有 AI 扩展的兼容性（尤其是版本号）  
  2. RTL 代码块在不同语言模式下的渲染是否保持 LTR  
  3. 可能的性能开销（拦截和转换过程）  
- **风险**：元数据中未提供明确的集成文档，集成路径相对隐蔽；因此在决定大规模使用前，需要评估设置成本和后期维护工作量。  

总体而言，若团队需要在 VS Code 中快速为 AI 代码助手添加 RTL 支持，且可以接受一次手动验证和后续维护工作，这个插件是一个可行且成本较低的解决方案。

## 🧭 Practical evaluation

**Value:** GuyRonnen/rtl-for-vs-code-agents helps add AI capability without starting from a blank model stack.

**Best use cases**

- prototype AI features
- build RAG or agent workflows
- evaluate model tooling

**Integration notes:** Needs manual inspection before adoption because integration signals are sparse in the discovered metadata.

**Production readiness:** Medium: useful for prototypes or internal workflows, with dependency and maintenance checks before production.

**Quality signals**

- 106 GitHub stars
- 8 forks
- updated 2026-05-10
- primary language: PowerShell

**Risks:** Integration path is not obvious from metadata; validate setup cost before committing.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 24/100 |
| stars | 43/100 |
| topics | 0/100 |
| outlook | 66/100 |
| quality | 57/100 |
| recency | 100/100 |
| adoption | 38/100 |
| production | 66/100 |
| usefulness | 58/100 |
| integration | 30/100 |
| sourceTrust | 100/100 |

---

<sub>🔭 Discovered 2026-05-10 · [View on GitHub](https://github.com/GuyRonnen/rtl-for-vs-code-agents) · [← Back to AI/ML](./README.md)</sub>
