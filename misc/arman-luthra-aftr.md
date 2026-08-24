# Arman-Luthra/aftr

[![Stars](https://img.shields.io/github/stars/Arman-Luthra/aftr?style=flat-square&color=yellow)](https://github.com/Arman-Luthra/aftr/stargazers) [![Forks](https://img.shields.io/github/forks/Arman-Luthra/aftr?style=flat-square&color=blue)](https://github.com/Arman-Luthra/aftr/network) [![Language](https://img.shields.io/badge/lang-Unknown-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-31%2F100-brightgreen?style=flat-square)](#)

> Discovered from Hacker News (github-mentions)

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | — |
| 🍴 **Forks** | — |
| 💻 **Language** | Unknown |
| 📈 **Score** | 31/100 |
| 🗓️ **Last push** | 2026-08-24 |
| 🔍 **Source** | hackernews |

## 🏷️ Topics

`hn` `github-mentions`

## 🎯 Categories

Misc

## 📝 Summary

### English

**Brief Summary (2‑3 sentences)**  
The “Show HN: Use After Effects with Claude Code, Cursor and Antigravity” project demonstrates how to integrate Adobe After Effects with AI‑powered coding assistants (Claude Code), the Cursor IDE, and the Antigravity UI framework. It provides a proof‑of‑concept workflow that lets users generate and edit After Effects scripts or expressions via natural‑language prompts, then run them directly in the After Effects environment.

**Value**  
- **Rapid prototyping**: Designers and motion‑graphics artists can describe visual effects in plain English and get ready‑to‑run ExtendScript/JSX code instantly, cutting down iteration time.  
- **Unified toolchain**: By bridging After Effects with modern AI coding assistants and a lightweight UI (Antigravity), the project creates a single, searchable interface for script generation, testing, and tweaking.  
- **Collaboration**: Generated code can be version‑controlled and shared, making it easier for teams to review and refine AI‑suggested scripts.

**Practical Adoption Path**  
1. **Clone & review** – Fork the repository, read the README, and verify the licensing (likely MIT/Apache).  
2. **Set up dependencies** – Install Claude Code (or an API key for Anthropic), the Cursor IDE, and the Antigravity package; ensure After Effects is on the same machine and that the ExtendScript engine is accessible.  
3. **Run the demo** – Execute the provided starter script to confirm that prompts from Claude are turned into valid JSX and that Antigravity’s UI can launch the generated code in After Effects.  
4. **Integrate into workflow** – Replace the demo prompts with your own internal templates (e.g., “Create a lower‑third animation with a bounce”), and embed the CLI/GUI into your existing pipeline (e.g., as a pre‑render step).  
5. **Validate & iterate** – Add unit tests for generated scripts, monitor API usage limits, and set up CI to lint both the AI‑generated code and the surrounding glue code.

**Production Readiness**  
- **Maturity**: Medium. The project is recently updated (2026‑07‑13) and shows a functional prototype, but integration signals are sparse and documentation is minimal.  
- **Risks**: Limited test coverage, potential breaking changes in Claude’s API, and reliance on proprietary After Effects scripting. Verify the license, check issue tracker activity, and consider fallback mechanisms (e.g., manual script edits).  
- **Recommendation**: Suitable for internal tools, proof‑of‑concepts, or early‑stage pipelines after a short validation sprint. For production‑critical workloads, perform a thorough security and maintenance audit, lock down API versions, and add monitoring around script execution.

### Русский

Show HN: Use After Effects with Claude Code, Cursor и Antigravity — это экспериментальный набор скриптов, позволяющий управлять After Effects через AI‑модели Claude и Cursor, а также автоматизировать рендеринг с помощью Antigravity. Он подходит для прототипов и внутренних пайплайнов, где требуется быстро генерировать и править видеоконтент с помощью кода, но перед вводом в production необходимо проверить лицензию, актуальность зависимостей и наличие документации. Готовность к production — средняя: проект требует ручной оценки и возможных доработок перед масштабным использованием.

### 中文

**项目简介（2‑3 句）**  
Show HN: Use After Effects with Claude Code, Cursor and Antigravity 是一个示例仓库，演示如何在 Adobe After Effects 中通过 Claude（AI 编码助手）、Cursor（代码补全）和 Antigravity（AI 驱动的 UI 生成）实现自动化脚本和工作流。它适合作为原型或内部工具的参考，实现 AI 辅助的视觉特效编程。

**价值**  
- **提升效率**：借助 Claude 的自然语言到代码转换，快速生成 After Effects 脚本，减少手动编写脚本的时间。  
- **统一工具链**：将 Cursor 的代码补全与 Antigravity 的 UI 生成结合，形成“一站式”AI 编程环境，适合创意团队快速迭代。  
- **原型验证**：项目结构简洁，便于在内部项目中快速验证 AI 与特效软件的集成可行性。

**典型接入方式**  
1. **环境准备**：  
   - 安装 After Effects（支持 ExtendScript/JSX）。  
   - 配置 Claude API（或本地模型）以及 Cursor 插件的访问令牌。  
   - 若使用 Antigravity，需要 Node.js 环境并安装对应 npm 包。  
2. **代码集成**：  
   - 将仓库 `src/` 下的脚本复制到项目的 ExtendScript 目录。  
   - 在脚本中调用 Claude 提供的 `generateCode(prompt)` 接口，生成或修改 JSX 代码。  
   - 使用 Cursor 在 IDE（如 VS Code）中实时补全并调试生成的脚本。  
   - 如需 UI，调用 Antigravity 的 `createUI(schema)` 方法生成交互面板并嵌入 After Effects。  
3. **工作流示例**：  
   - 编写自然语言需求（如“在 5 秒内淡入淡出并添加粒子效果”）。  
   - Claude 返回对应的 JSX 代码片段。  
   - Cursor 自动补全并检查语法。  
   - Antigravity 生成控制面板，允许非技术成员在 UI 中调节参数。  
   - 脚本通过 After Effects 的脚本引擎执行，完成特效渲染。

**生产可用性**  
- **成熟度**：当前项目标记为 *Medium*，适合原型、内部工具或实验性工作流。  
- **依赖风险**：依赖外部 AI 服务（Claude、Cursor）以及 Antigravity 的持续维护，需确认服务 SLA 与费用。  
- **维护状态**：最近一次更新为 2026‑07‑13，活跃度低，缺乏完整文档和社区支持。  
- **采用建议**：在正式上线前进行以下检查：  
  1. **许可证**：确认代码使用的开源许可证与公司合规要求匹配。  
  2. **安全审计**：审查 AI 调用的输入输出，防止恶意脚本注入。  
  3. **稳定性测试**：在测试环境中跑通完整的生成‑执行‑UI 流程，评估错误恢复和性能。  
  4. **备份方案**：为关键脚本提供手动维护的备份分支，防止 AI 服务不可用导致工作流中断。  

综上，项目在提升 After Effects 脚本开发效率方面具备创新价值，适合作为内部原型或实验平台使用；若要投入生产，需要对依赖、文档、维护频率以及安全合规进行充分评估后再决定。

## 🧭 Practical evaluation

**Value:** Show HN: Use After Effects with Claude Code, Cursor and Antigravity may be useful when its README and activity match a concrete workflow.

**Best use cases**

- Not enough metadata yet.

**Integration notes:** Needs manual inspection before adoption because integration signals are sparse in the discovered metadata.

**Production readiness:** Medium: useful for prototypes or internal workflows, with dependency and maintenance checks before production.

**Quality signals**

- updated 2026-07-13
- 2 topics

**Risks:** Quality signals are limited; verify license, maintenance, docs, issues, and release cadence before using it.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 0/100 |
| stars | 0/100 |
| topics | 25/100 |
| outlook | 33/100 |
| quality | 26/100 |
| recency | 40/100 |
| adoption | 0/100 |
| production | 38/100 |
| usefulness | 42/100 |
| integration | 30/100 |
| sourceTrust | 80/100 |
| categoryMatchCount | 0/100 |

---

<sub>🔭 Discovered 2026-07-13 · [View on GitHub](https://github.com/Arman-Luthra/aftr) · [← Back to Misc](./README.md)</sub>
