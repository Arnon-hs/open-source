# elixir-lsp/vscode-elixir-ls

[![Stars](https://img.shields.io/github/stars/elixir-lsp/vscode-elixir-ls?style=flat-square&color=yellow)](https://github.com/elixir-lsp/vscode-elixir-ls/stargazers) [![Forks](https://img.shields.io/github/forks/elixir-lsp/vscode-elixir-ls?style=flat-square&color=blue)](https://github.com/elixir-lsp/vscode-elixir-ls/network) [![Language](https://img.shields.io/badge/lang-TypeScript-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-49%2F100-brightgreen?style=flat-square)](#)

> Elixir language support and debugger for VS Code, powered by ElixirLS.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 597 |
| 🍴 **Forks** | 108 |
| 💻 **Language** | TypeScript |
| 📈 **Score** | 49/100 |
| 🗓️ **Last push** | 2026-08-24 |
| 🔍 **Source** | github |

## 🏷️ Topics

`elixir` `language-server`

## 🎯 Categories

Backend

## 📝 Summary

### English

**Elixir Language Support and Debugger for VS Code**

The elixir-lsp/vscode-elixir-ls project provides open-source language support and debugging capabilities for Elixir in Visual Studio Code (VS Code), powered by ElixirLS. This tool enables teams to streamline their backend development process by reusing service infrastructure, thereby reducing the time and effort required to ship API services.

**Value:**
The primary value proposition of elixir-lsp/vscode-elixir-ls lies in its ability to help teams standardize service patterns and reuse backend infrastructure, ultimately leading to faster API service deployment.

**Practical Adoption Path:**
Before adopting this project, teams should conduct a manual inspection of the integration process to ensure a smooth onboarding experience. This involves reviewing the discovered metadata for sparse integration signals. Once adopted, teams can utilize the project's features to standardize service patterns and reuse backend infrastructure.

**Production Readiness:**
While elixir-lsp/vscode-elixir-ls has a medium level of production readiness, it is suitable for use in prototypes or internal workflows. However, teams should perform dependency and maintenance checks before deploying the project in a production environment to ensure its stability and security.

### Русский

Резюме проекта elixir-lsp/vscode-elixir-ls:

Этот открытый исходный проект обеспечивает поддержку языка Elixir и отладчика для редактора VS Code, облегчая командам повторно использовать инфраструктуру сервисов, а не создавать ее заново. Типовой сценарий внедрения заключается в ускорении развертывания API-сервисов и стандартизации шаблонов сервисов. Проект имеет средний уровень готовности к production, что делает его подходящим для прототипов или внутренних потоков работы, но требует тщательного проверки зависимостей и поддержки перед выпуском в производство.

### 中文

**项目简介**  
`elixir-lsp/vscode-elixir-ls` 为 VS Code 提供基于 ElixirLS 的 Elixir 语言支持和调试功能，让开发者在编辑器中即可获得完整的代码补全、跳转、类型检查和交互式调试体验。

**价值**  
- **统一后端基础设施**：团队无需自行搭建或维护语言服务器，只需安装插件即可获得专业的 Elixir 开发环境，节省维护成本。  
- **加速 API 服务交付**：即时的编译错误提示、函数跳转和调试能力帮助开发者快速定位问题，提升开发效率，进而更快上线后端服务。  
- **标准化开发流程**：统一的 LSP（Language Server Protocol）实现确保所有成员使用相同的代码检查和调试规则，降低代码不一致风险。

**典型接入方式**  
1. 在 VS Code 市场搜索并安装 **ElixirLS** 插件（或直接在项目根目录执行 `code --install-extension elixir-lsp.vscode-elixir-ls`）。  
2. 项目根目录需包含 `mix.exs`，插件会自动启动 ElixirLS 并根据 `mix.lock` 下载对应依赖。  
3. 如需自定义调试配置，可在 `.vscode/launch.json` 中添加 `elixir` 调试配置，示例：

```json
{
  "type": "elixir",
  "request": "launch",
  "name": "Debug Mix Test",
  "task": "test",
  "projectDir": "${workspaceFolder}"
}
```

4. 对于 CI/CD 环境或容器化部署，可在 Dockerfile 中预装 `elixir-ls`（`mix escript.install hex elixir_ls`），确保团队成员在相同的开发镜像中使用一致的语言服务器。

**生产可用性**  
- **成熟度**：GitHub 近 600 星、100+ Fork，最近一次更新在 2026‑07‑05，活跃度良好。  
- **适用场景**：适合作为内部开发或原型阶段的标准化工具；在正式生产环境使用前，建议检查以下几点：  
  - 许可证兼容性（MIT）是否符合公司合规要求。  
  - 安全审计：确认依赖的 ElixirLS 版本无已知 CVE。  
  - 维护者活跃度：关注 Issue 与 PR 的响应速度，确保后续 bug 能及时修复。  
- **风险等级**：中等。功能完整且已在多数社区项目中验证，可在内部业务系统中使用，但在关键业务的生产环境部署前，建议进行一次集成测试并制定回滚方案。

## 🧭 Practical evaluation

**Value:** elixir-lsp/vscode-elixir-ls helps teams reuse service infrastructure instead of rebuilding common backend pieces.

**Best use cases**

- ship API services faster
- reuse backend infrastructure
- standardize service patterns

**Integration notes:** Needs manual inspection before adoption because integration signals are sparse in the discovered metadata.

**Production readiness:** Medium: useful for prototypes or internal workflows, with dependency and maintenance checks before production.

**Quality signals**

- 597 GitHub stars
- 108 forks
- updated 2026-07-05
- primary language: TypeScript
- 2 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 51/100 |
| stars | 59/100 |
| topics | 25/100 |
| outlook | 49/100 |
| quality | 54/100 |
| recency | 40/100 |
| adoption | 57/100 |
| production | 53/100 |
| usefulness | 42/100 |
| integration | 46/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 100/100 |

---

<sub>🔭 Discovered 2026-07-05 · [View on GitHub](https://github.com/elixir-lsp/vscode-elixir-ls) · [← Back to Backend](./README.md)</sub>
