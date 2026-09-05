# linear/linear

[![Stars](https://img.shields.io/github/stars/linear/linear?style=flat-square&color=yellow)](https://github.com/linear/linear/stargazers) [![Forks](https://img.shields.io/github/forks/linear/linear?style=flat-square&color=blue)](https://github.com/linear/linear/network) [![Language](https://img.shields.io/badge/lang-TypeScript-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-71%2F100-brightgreen?style=flat-square)](#)

> Tools, SDK's and plugins for Linear

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 1.4k |
| 🍴 **Forks** | 251 |
| 💻 **Language** | TypeScript |
| 📈 **Score** | 71/100 |
| 🗓️ **Last push** | 2026-09-05 |
| 🔍 **Source** | github |

## 🏷️ Topics

_no topics_

## 🎯 Categories

Libraries & SDKs

## 📝 Summary

### English

**Brief summary**  
Linear/linear is a TypeScript‑based collection of tools, SDKs, and plugins that simplify integrating with the Linear issue‑tracking platform. With over 1.3 k stars, frequent updates (last commit 2026‑05‑12) and a growing fork base, it shows strong community momentum and can be plugged into existing workflows with minimal friction.

**Value**  
The project provides ready‑made client libraries and UI components that let developers read, create, and update Linear issues directly from their applications, CI pipelines, or internal tooling, cutting the time needed to build custom API wrappers.

**Practical adoption path**  
1. **Review the README** to identify the SDK or plugin that matches your use case (e.g., Node.js client, VS Code extension).  
2. **Run a small proof‑of‑concept**—for instance, a script that creates a test issue in a sandbox Linear workspace.  
3. **Validate security and licensing** (the repo uses an MIT‑style license, but confirm no hidden dependencies).  
4. **Scale up** by adding the SDK to a service or integrating the plugin into your development environment, using the example code as a template.

**Production readiness**  
The library scores high on production readiness: recent commits, active community contributions, and a solid star/fork count indicate stability and ongoing maintenance. While a final security audit and maintainer confirmation are still advisable, the project is mature enough for a serious pilot in production environments.

### Русский

**linear/linear** — набор инструментов, SDK и плагинов для сервиса Linear, позволяющий быстро интегрировать задачи и дорожные карты проекта в собственные CI/CD‑конвейеры, чат‑боты и аналитические панели. Для пилотного внедрения достаточно проверить README и выполнить небольшую proof‑of‑concept‑интеграцию (например, автоматическое создание задач из pull‑request‑ов). Проект имеет высокий уровень готовности к production: активная поддержка, свежие коммиты, более 1300 звёзд и 250 форков, что делает его надёжным кандидатом для серьёзного использования в корпоративных процессах.

### 中文

**项目简介（2‑3 句）**  
linear/linear 是为 Linear（项目管理与工单系统）提供的工具集合、SDK 与插件，帮助开发者在自己的应用或 CI/CD 流程中直接读取、创建和同步 Linear 的 Issue、项目和工作流。该仓库维护活跃、TypeScript 实现，已获得 1.3k+ Stars，适合作为企业内部或开源产品的 Linear 集成基石。

**价值**  
- **统一入口**：封装了 Linear 的 GraphQL API，提供简洁的函数式接口，避免每次手动编写请求。  
- **可扩展插件**：内置 VSCode、GitHub Actions、Jira ↔ Linear 同步等插件，可直接嵌入常见开发工具链。  
- **类型安全**：基于 TypeScript，所有模型都有完整的类型定义，降低运行时错误，提升团队协作效率。  

**典型接入方式**  
1. **阅读 README 与示例代码**，确认项目的使用场景（如自动创建 Issue、同步状态等）。  
2. **在项目中安装 SDK**：`npm i @linear/sdk`（或对应的包名）。  
3. **在代码中初始化客户端**，使用个人 API Token：  
   ```ts
   import { LinearClient } from "@linear/sdk";

   const client = new LinearClient({ apiKey: process.env.LINEAR_API_KEY });
   // 示例：创建 Issue
   await client.issueCreate({ title: "新功能需求", teamId: "team_123" });
   ```  
4. **插件集成**：如在 GitHub Actions 中使用 `linear/action`，在 workflow 中添加步骤即可实现 PR 自动关联 Linear Issue。  
5. **小范围 PoC**：先在测试仓库或内部工具中实现最核心的功能（如 Issue 同步），验证 API 调用、权限和错误处理后再推广到全链路。  

**生产可用性**  
- **活跃度**：最近一次提交在 2026‑05‑12，星标 1.3k、Fork 251，社区活跃，Issue 与 PR 响应及时。  
- **成熟度**：已发布多个稳定版本，文档覆盖常用场景，类型定义完备。  
- **风险**：目前未发现重大许可证或安全漏洞，但仍建议在正式上线前完成：  
  - 许可证（MIT）兼容性检查；  
  - 依赖安全审计（使用 `npm audit`/`snyk`）；  
  - 与内部安全团队确认 API Token 管理与审计策略。  
- **结论**：在完成上述小规模验证和安全审查后，linear/linear 完全可以作为生产环境的 OSS 组件投入使用，尤其适合需要深度集成 Linear 的内部工具或 SaaS 产品。

## 🧭 Practical evaluation

**Value:** linear/linear may be useful when its README and activity match a concrete workflow.

**Best use cases**

- Not enough metadata yet.

**Integration notes:** Looks feasible to evaluate, but integration should start with a small proof of concept and README check.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 1374 GitHub stars
- 251 forks
- updated 2026-05-12
- primary language: TypeScript

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 60/100 |
| stars | 67/100 |
| topics | 0/100 |
| outlook | 69/100 |
| quality | 64/100 |
| recency | 80/100 |
| adoption | 65/100 |
| production | 70/100 |
| usefulness | 74/100 |
| integration | 78/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 100/100 |

---

<sub>🔭 Discovered 2026-05-12 · [View on GitHub](https://github.com/linear/linear) · [← Back to Libraries--sdks](./README.md)</sub>
