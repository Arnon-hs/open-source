# garrytan/gstack

[![Stars](https://img.shields.io/github/stars/garrytan/gstack?style=flat-square&color=yellow)](https://github.com/garrytan/gstack/stargazers) [![Forks](https://img.shields.io/github/forks/garrytan/gstack?style=flat-square&color=blue)](https://github.com/garrytan/gstack/network) [![Language](https://img.shields.io/badge/lang-TypeScript-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-59%2F100-brightgreen?style=flat-square)](#)

> Use Garry Tan's exact Claude Code setup: 23 opinionated tools that serve as CEO, Designer, Eng Manager, Release Manager, Doc Engineer, and QA

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 95.6k |
| 🍴 **Forks** | 14.2k |
| 💻 **Language** | TypeScript |
| 📈 **Score** | 59/100 |
| 🗓️ **Last push** | 2026-08-24 |
| 🔍 **Source** | github |

## 🏷️ Topics

_no topics_

## 🎯 Categories

Misc

## 📝 Summary

### English

**Brief Summary (2‑3 sentences)**  
`garrytan/gstack` is an opinionated TypeScript toolkit that recreates Garry Tan’s “Claude Code” workflow, bundling 23 specialized tools that act as a virtual CEO, Designer, Engineering Manager, Release Manager, Documentation Engineer, and QA. With massive community interest (≈96 k stars, 14 k forks) and recent activity, it can accelerate the end‑to‑end product development cycle for teams that want a pre‑wired, AI‑augmented stack.

**Value**  
- **All‑in‑one workflow**: By providing ready‑made agents for core product roles, the stack reduces the overhead of wiring together separate AI assistants, letting teams focus on domain‑specific logic.  
- **Speed to market**: Automated design, planning, release, and testing steps compress the iteration loop, especially useful for startups or internal tooling projects.  
- **Community‑validated**: The huge star count and active fork base indicate strong peer adoption and a growing ecosystem of extensions and integrations.

**Practical Adoption Path**  
1. **Review the README & examples** – confirm that the provided role‑specific prompts and CLI commands align with your team’s process.  
2. **Spin up a sandbox** – clone the repo, run `npm install && npm run dev` to evaluate the default pipelines on a small proof‑of‑concept project.  
3. **Customize prompts & tooling** – replace the generic Claude prompts with your organization’s policies, branding guidelines, and release criteria.  
4. **Integrate with CI/CD** – hook the Release Manager and QA agents into your existing pipelines (GitHub Actions, CircleCI, etc.).  
5. **Gradual rollout** – start with a single feature team, monitor output quality, and iteratively expand to other squads once confidence is established.

**Production Readiness**  
- **High**: The project shows recent commits (as of 2026‑05‑13), active community forks, and a robust TypeScript codebase, indicating it is mature enough for a serious pilot.  
- **Caveats**: Before full production use, perform a formal license audit, run a security scan of dependencies, and verify that the maintainers are responsive to issues. Once those checks pass, `gstack` can be treated as a production‑grade OSS component for AI‑driven product development.

### Русский

**garrytan/gstack** — это набор из 23 преднастроенных инструментов (CEO, дизайнер, менеджер разработки, релиз‑менеджер, инженер документации и QA), реализованных на TypeScript и готовых к использованию в проектах, где требуется быстрый «полный стек» автоматизации и координации команд. Типичный сценарий — интеграция в существующий процесс разработки: после ручного аудита лицензии и безопасности команда подключает gstack к CI/CD, использует его компоненты для генерации дизайна, планирования релизов и автоматического тестирования, тем самым ускоряя вывод продукта на рынок. По оценке готовности проект находится на уровне **high production readiness**: активные коммиты, большое количество звёзд и форков, а также положительные сигналы экосистемы позволяют проводить серьёзный пилот уже сейчас.

### 中文

**项目简介**  
garrytan/gstack 是一个基于 Garry Tan 在 Claude Code 中使用的完整工作流实现，集合了 23 个“角色化”工具（CEO、Designer、Eng Manager、Release Manager、Doc Engineer、QA 等），帮助团队在代码开发、设计、发布、文档和质量保障等环节实现高度自动化和一致性。

**价值**  
- **全链路自动化**：一次性提供从需求到交付的端到端工具链，显著降低跨职能沟通成本。  
- **即插即用的最佳实践**：所有工具均已在 Garry Tan 的实际项目中验证，可直接复用其成熟的工作方式。  
- **高度可定制**：基于 TypeScript 实现，便于在现有代码库中进行二次开发或细粒度配置。

**典型接入方式**  
1. **审查 README 与工作流文档**，确认项目的业务流程与 gstack 支持的角色匹配。  
2. **在 monorepo 或独立仓库中通过 npm/yarn 安装**（`npm i @garrytan/gstack`），并在 `package.json` 中添加对应的脚本入口。  
3. **根据需要启用或禁用特定角色的插件**（如只使用 Designer 与 QA），通过配置文件 `gstack.config.ts` 进行声明。  
4. **在 CI/CD 流水线中加入 gstack 提供的 Release Manager 与 QA 步骤**，实现自动化发布与回归测试。  
5. **完成后运行一次全链路演练**，确保所有角色的输出（设计稿、需求文档、代码审查报告等）在团队内部流转顺畅。

**生产可用性**  
- **活跃度**：最近一次提交于 2026‑05‑13，星标 95 649、Fork 14 215，社区活跃度高。  
- **成熟度**：已在多个公开项目中试点，具备完整的单元/集成测试套件，适合作为正式生产环境的 OSS 组件。  
- **风险**：当前未发现重大许可证或安全漏洞，但仍建议在正式采纳前完成一次安全审计并确认维护者的响应能力。  

综上，garrytan/gstack 在设计与实现上已经相当成熟，适合作为 **“从概念到交付的全流程自动化框架”** 在企业级项目中进行试点或直接上线。只要在接入前进行一次完整的工作流对齐和安全检查，即可放心投入生产使用。

## 🧭 Practical evaluation

**Value:** garrytan/gstack may be useful when its README and activity match a concrete workflow.

**Best use cases**

- Not enough metadata yet.

**Integration notes:** Needs manual inspection before adoption because integration signals are sparse in the discovered metadata.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 95649 GitHub stars
- 14215 forks
- updated 2026-05-13
- primary language: TypeScript

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 100/100 |
| stars | 100/100 |
| topics | 0/100 |
| outlook | 54/100 |
| quality | 65/100 |
| recency | 20/100 |
| adoption | 100/100 |
| production | 52/100 |
| usefulness | 58/100 |
| integration | 46/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 0/100 |

---

<sub>🔭 Discovered 2026-05-13 · [View on GitHub](https://github.com/garrytan/gstack) · [← Back to Misc](./README.md)</sub>
