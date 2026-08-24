# f-is-h/Usage4Claude

[![Stars](https://img.shields.io/github/stars/f-is-h/Usage4Claude?style=flat-square&color=yellow)](https://github.com/f-is-h/Usage4Claude/stargazers) [![Forks](https://img.shields.io/github/forks/f-is-h/Usage4Claude?style=flat-square&color=blue)](https://github.com/f-is-h/Usage4Claude/network) [![Language](https://img.shields.io/badge/lang-Swift-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-52%2F100-brightgreen?style=flat-square)](#)

> Monitor all your Claude/Codex usage limits in real-time from your macOS menu bar - supports 5-hour, 7-day, extra usage, 7-day Opus and 7-day Sonnet quotas.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 334 |
| 🍴 **Forks** | 37 |
| 💻 **Language** | Swift |
| 📈 **Score** | 52/100 |
| 🗓️ **Last push** | 2026-08-24 |
| 🔍 **Source** | github |

## 🏷️ Topics

`claude` `claude-ai` `claude-code` `claude-desktop` `macos` `macos-app` `menubar-app` `monitoring` `native-app` `productivity` `status-bar` `swift`

## 🎯 Categories

AI/ML · Observability

## 📝 Summary

### English

**Project Summary:**

f-is-h/Usage4Claude is an open-source macOS menu bar application that provides real-time monitoring of Claude/Codex usage limits, supporting various quota types. This project helps developers add AI capabilities to their applications without starting from scratch by providing a pre-built solution for managing usage limits. It is suitable for prototyping AI features, building workflows, and evaluating model tooling.

**Value Proposition:**

f-is-h/Usage4Claude offers a convenient way to monitor AI usage limits, allowing developers to focus on building and evaluating AI features without worrying about quota management. This can save time and effort, making it easier to prototype and integrate AI capabilities into applications.

**Adoption Path:**

To adopt f-is-h/Usage4Claude, developers can follow these steps:

1. Evaluate the project by reviewing the README and checking the integration path.
2. Start with a small proof of concept to ensure the project meets their needs.
3. Assess the setup cost and validate it before committing to the project.
4. Use the application to monitor Claude/Codex usage limits and adjust their AI workflows accordingly.

**Production Readiness:**

f-is-h/Usage4Claude is considered medium-production-ready, making it suitable for prototypes, internal workflows, or

### Русский

`f-is-h/Usage4Claude` — это macOS‑утилита на Swift, отображающая в реальном времени текущие лимиты использования Claude/Codex (5‑hour, 7‑day, extra, Opus и Sonnet) прямо в строке меню, что упрощает контроль расходов при прототипировании AI‑фич и построении RAG/агентных воркфлоу. Для внедрения рекомендуется начать с небольшого proof‑of‑concept, проверив README и зависимости, после чего можно интегрировать в внутренние или клиентские проекты. Готовность к production — средняя: проект уже стабилен и имеет 334 звёзд, но требует проверки совместимости и обслуживания перед масштабным использованием.

### 中文

**简短介绍**  
f‑is‑h/Usage4Claude 是一款基于 Swift 的 macOS 菜单栏工具，实时监控 Claude 与 Codex 的使用配额（5 小时、7 天、额外配额以及 7 天 Opus、Sonnet 等），帮助开发者随时掌握 AI 调用消耗。

**价值**  
- **即时可视化**：在菜单栏直接展示配额剩余量，避免因配额耗尽导致的服务中断。  
- **多配额支持**：兼容多种 OpenAI/Anthropic 计费周期（5 h、7 d、额外、Opus、Sonnet），适用于不同业务模型。  
- **提升研发效率**：在原型开发、RAG 或智能体工作流中快速评估模型调用成本，无需自行实现配额监控逻辑。

**典型接入方式**  
1. **克隆仓库并使用 Xcode 编译**：项目主要语言为 Swift，提供完整的 Xcode 项目文件。  
2. **配置 API 密钥**：在 `Info.plist` 或环境变量中填入 Claude/Codex 的 API Key。  
3. **启动菜单栏应用**：运行后即在 macOS 菜单栏出现图标，点击可查看各配额的实时数值。  
4. **可选集成**：若已有内部监控平台，可通过项目提供的 `UsageProvider` 接口导出 JSON/Prometheus 指标，实现统一监控。

**生产可用性**  
- **成熟度**：GitHub ★334，近期（2026‑07‑13）仍在维护，代码量适中，依赖主要为系统自带的网络库，风险相对可控。  
- **适用场景**：非常适合作为原型或内部工具使用；在正式生产环境部署前，建议完成以下检查：  
  1. **依赖审计**：确认第三方库（若有）符合企业安全合规要求。  
  2. **错误容忍**：为 API 调用失败或配额查询异常添加 fallback（如本地缓存或告警）。  
  3. **CI/CD 集成**：将编译、签名、自动化测试纳入流水线，确保每次更新不影响现有监控。  
- **结论**：在做好上述检查后，Usage4Claude 可在内部或面向少量用户的生产环境中稳定运行，帮助团队实时掌握 AI 使用成本，避免意外超额。

## 🧭 Practical evaluation

**Value:** f-is-h/Usage4Claude helps add AI capability without starting from a blank model stack.

**Best use cases**

- prototype AI features
- build RAG or agent workflows
- evaluate model tooling

**Integration notes:** Looks feasible to evaluate, but integration should start with a small proof of concept and README check.

**Production readiness:** Medium: useful for prototypes or internal workflows, with dependency and maintenance checks before production.

**Quality signals**

- 334 GitHub stars
- 37 forks
- updated 2026-07-13
- primary language: Swift
- 14 topics

**Risks:** Integration path is not obvious from metadata; validate setup cost before committing.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 39/100 |
| stars | 54/100 |
| topics | 100/100 |
| outlook | 58/100 |
| quality | 62/100 |
| recency | 40/100 |
| adoption | 50/100 |
| production | 53/100 |
| usefulness | 58/100 |
| integration | 30/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 200/100 |

---

<sub>🔭 Discovered 2026-07-13 · [View on GitHub](https://github.com/f-is-h/Usage4Claude) · [← Back to AI/ML](./README.md)</sub>
