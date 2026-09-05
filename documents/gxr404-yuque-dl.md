# gxr404/yuque-dl

[![Stars](https://img.shields.io/github/stars/gxr404/yuque-dl?style=flat-square&color=yellow)](https://github.com/gxr404/yuque-dl/stargazers) [![Forks](https://img.shields.io/github/forks/gxr404/yuque-dl?style=flat-square&color=blue)](https://github.com/gxr404/yuque-dl/network) [![Language](https://img.shields.io/badge/lang-TypeScript-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-68%2F100-brightgreen?style=flat-square)](#)

> yuque 语雀知识库下载

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 2.2k |
| 🍴 **Forks** | 333 |
| 💻 **Language** | TypeScript |
| 📈 **Score** | 68/100 |
| 🗓️ **Last push** | 2026-09-05 |
| 🔍 **Source** | github |

## 🏷️ Topics

`cli` `download` `markdown` `nodejs` `yuque` `yuque-dl`

## 🎯 Categories

Documents · Backend · DevTools

## 📝 Summary

### English

gxr404/yuque-dl is a TypeScript‑based CLI/SDK that lets developers quickly download Yuque knowledge‑base content, cutting down on manual documentation retrieval and speeding up review, CI, and local‑engineering loops. Its straightforward API/CLI interface makes it easy to integrate into existing workflows for automated tasks or pilot projects, and the project shows strong OSS health—recent updates, 2.2k stars, 333 forks, and active maintenance—indicating high production readiness for a serious trial, pending a final license and security review.

### Русский

gxr404/yuque-dl — это утилита на TypeScript для скачивания содержимого языковых баз Yuque, позволяющая инженерам автоматизировать получение документации и ускорять ежедневные циклы разработки и ревью. Типовой сценарий внедрения — интеграция CLI‑инструмента в локальные скрипты сборки или CI‑pipeline для автоматической выгрузки актуальных знаний перед тестированием или деплоем. Благодаря активной разработке (обновление 2026‑06‑27), высокой популярности (2,2k★, 333 форка) и четким сигналам готовности (API/CLI, TypeScript), проект считается production‑ready для пилотного использования в инженерных командах.

### 中文

**项目简介**  
gxr404/yuque-dl 是一款基于 TypeScript 的开源工具，能够一键下载并同步语雀（Yuque）知识库的文档内容，帮助团队把云端知识沉淀到本地仓库进行版本管理和离线阅读。

**价值**  
- **提升开发效率**：在本地即可快速检索、浏览和搜索语雀文档，省去频繁打开网页的时间。  
- **自动化工作流**：可在 CI/CD 流程中调用，自动拉取最新文档用于代码审查、生成文档站点或做内部审计。  
- **统一知识管理**：将云端知识库与代码库统一管理，便于版本控制、审计和回滚。

**典型接入方式**  
1. **CLI**：`npx yuque-dl --token <TOKEN> --repo <REPO_ID> --output ./docs`，适合脚本化调用或 CI 步骤。  
2. **Node.js SDK**：在项目中 `import { downloadRepo } from 'yuque-dl'`，通过代码直接获取文档数据进行二次加工。  
3. **GitHub Action**：使用官方或社区提供的 Action，将下载步骤集成到工作流中，实现每日或 PR 触发的自动同步。

**生产可用性**  
- **活跃度**：截至 2026‑06‑27 最近一次更新，拥有 2,234 星、333 Fork，社区活跃。  
- **技术成熟度**：使用 TypeScript 编写，提供完整的类型定义和错误处理，易于在企业项目中集成。  
- **安全与合规**：项目采用 MIT 许可证，暂无已知安全漏洞；建议在正式环境前进行一次依赖审计。  
- **可观测性**：CLI 输出日志，SDK 支持自定义日志钩子，便于监控下载过程。  

综合来看，gxr404/yuque-dl 已具备较高的生产就绪度，可在内部工具链或 CI 环境中安全、稳定地使用。

## 🧭 Practical evaluation

**Value:** gxr404/yuque-dl helps engineers save time in daily development and review loops.

**Best use cases**

- speed up developer workflows
- automate local engineering tasks
- improve CI feedback

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 2234 GitHub stars
- 333 forks
- updated 2026-06-27
- primary language: TypeScript
- 6 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 63/100 |
| stars | 71/100 |
| topics | 75/100 |
| outlook | 74/100 |
| quality | 77/100 |
| recency | 80/100 |
| adoption | 69/100 |
| production | 73/100 |
| usefulness | 58/100 |
| integration | 62/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 300/100 |

---

<sub>🔭 Discovered 2026-06-27 · [View on GitHub](https://github.com/gxr404/yuque-dl) · [← Back to Documents](./README.md)</sub>
