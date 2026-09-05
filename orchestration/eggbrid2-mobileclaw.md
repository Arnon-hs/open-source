# eggbrid2/mobileClaw

[![Stars](https://img.shields.io/github/stars/eggbrid2/mobileClaw?style=flat-square&color=yellow)](https://github.com/eggbrid2/mobileClaw/stargazers) [![Forks](https://img.shields.io/github/forks/eggbrid2/mobileClaw?style=flat-square&color=blue)](https://github.com/eggbrid2/mobileClaw/network) [![Language](https://img.shields.io/badge/lang-Kotlin-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-70%2F100-brightgreen?style=flat-square)](#)

> Open Android AI agent runtime for phone control, app automation, VLM screen reading, skill routing, mini apps, and Mihomo VPN workflows.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 400 |
| 🍴 **Forks** | 16 |
| 💻 **Language** | Kotlin |
| 📈 **Score** | 70/100 |
| 🗓️ **Last push** | 2026-09-05 |
| 🔍 **Source** | github |

## 🏷️ Topics

`accessibility-service` `ai` `ai-agent` `ai-group-chat` `android` `android-automation` `automation` `jetpack-compose` `kotlin` `llm-agent` `mihomo` `mobile-agent`

## 🎯 Categories

Orchestration · Automation · AI/ML · Communication · Networking

## 📝 Summary

### English

**Summary**  
eggbrid2/mobileClaw is an open‑source Android runtime that lets developers build AI agents capable of controlling the phone, automating apps, reading screens with vision‑language models, routing skills, hosting mini‑apps, and chaining Mihomo VPN workflows. It transforms isolated prompts and tools into repeatable, orchestrated agent pipelines, making multi‑agent coordination and tool‑use pipelines easy to standardize and reuse.  

**Value**  
- **Unified agent workflow engine** – turns ad‑hoc prompts into reproducible, version‑controlled pipelines, reducing engineering overhead for mobile AI automation.  
- **End‑to‑end capabilities** – combines UI interaction, VLM screen parsing, skill routing, and VPN management under a single Kotlin SDK, eliminating the need to stitch together disparate libraries.  
- **Extensible mini‑app framework** – lets teams plug in custom “mini‑apps” (e.g., data collectors, chat interfaces) that agents can invoke on‑device, fostering rapid prototyping and reuse.  

**Practical adoption path**  
1. **Proof‑of‑concept** – clone the repo, run the provided README example on a test device, and verify basic screen‑reading and app‑automation functions.  
2. **Pilot integration** – replace a manual automation script with a mobileClaw skill, using the built‑in skill‑routing API to connect VLM‑based screen parsing to the new skill.  
3. **Scale to multi‑agent flows** – define a workflow YAML (or Kotlin DSL) that chains multiple skills (e.g., VPN setup → app login → data extraction) and store the definition in version control for CI/CD testing.  
4. **Production hardening** – add persistent agent memory (SQLite or encrypted storage), enforce permission policies, and integrate with your existing monitoring/observability stack.  

**Production readiness**  
- **Activity & community** – 400 ★, 16 forks, recent commits (last update 2026‑06‑26), and a Kotlin codebase with 17 relevant topics indicate a healthy, actively maintained project.  
- **Ecosystem fit** – aligns with orchestration, automation, and mobile AI use cases; the SDK is lightweight enough for on‑device deployment yet extensible for backend orchestration.  
- **Risk considerations** – no obvious licensing or metadata red flags, but a final security audit (dependency scanning, permission review) and confirmation of active maintainers are recommended before a full‑scale rollout.  

Overall, mobileClaw is mature enough for a serious pilot and, with the outlined incremental integration steps, can be promoted to production for robust mobile AI agent workflows.

### Русский

**eggbrid2/mobileClaw** — это открытая Android‑платформа для запуска AI‑агентов, позволяющая автоматизировать управление телефоном, выполнять скрипты приложений, читать экран через VLM, маршрутизировать навыки и интегрировать мини‑приложения и Mihomo VPN. Типичный сценарий — построение повторяемых цепочек из изолированных подсказок и инструментов (мульти‑агентные воркфлоу, пайплайны с использованием внешних сервисов и централизованное хранилище памяти агента). Проект находится в высокой готовности к production: активные коммиты, 400 звёзд, Kotlin‑код, recent update 2026‑06‑26, а также хорошие сигналы экосистемы, что делает его подходящим для пилотного внедрения после небольшого proof‑of‑concept и проверки README.

### 中文

**项目简介**  
eggbrid2/mobileClaw 是一款基于 Android 的开源 AI 代理运行时，提供手机控制、应用自动化、视觉语言模型（VLM）屏幕读取、技能路由、迷你应用以及 Mihomo VPN 工作流等能力。它把零散的 Prompt 与工具封装成可复用的 agent 流程，帮助开发者快速搭建多代理协同、工具调用和记忆管理的完整方案。

**价值**  
- **统一工作流**：将分散的 AI Prompt、工具链和手机操作统一到同一运行时，实现“一键式”可重复执行的业务流程。  
- **多代理协同**：支持在同一设备上并行调度多个 AI 代理，便于实现复杂的跨应用任务（如先读取屏幕再自动填表再启动 VPN）。  
- **标准化记忆与路由**：内置记忆层和技能路由机制，降低每次开发时对状态管理和工具选择的重复实现成本。  

**典型接入方式**  
1. **阅读 README 并完成环境准备**（Android SDK、Kotlin 编译环境、Mihomo VPN 配置等）。  
2. **在现有 Android 项目中引入 mobileClaw**：通过 Gradle 添加 `implementation "com.eggbrid2:mobileclaw:<latest-version>"`。  
3. **编写简单的 Agent 配置**（JSON/YAML）或使用 Kotlin DSL 定义工作流，例如：  
   ```kotlin
   val workflow = workflow {
       step { vlmReadScreen() }
       step { appAutomation("com.example.app") }
       step { startMihomoVpn() }
   }
   MobileClaw.start(workflow)
   ```  
4. **先做 PoC**：在测试设备或模拟器上运行，验证 Prompt 与工具链的交互是否符合预期。  
5. **逐步迁移到生产**：在 CI 中加入单元/集成测试，使用日志与监控（如 Logcat、Prometheus exporter）确保运行时稳定。  

**生产可用性**  
- **活跃度**：截至 2026‑06‑26 最近一次提交，拥有 400+ stars、16 forks，社区活跃，代码基于 Kotlin，生态兼容性好。  
- **成熟度**：已实现核心功能（手机控制、VLM 读取、VPN 工作流），并提供完整的文档和示例，适合作为 OSS 级别的 Pilot 项目。  
- **风险**：目前尚未完成最终的许可证合规、完整安全审计以及维护者长期承诺的确认，建议在正式投产前完成这些审查。  

**结论**  
mobileClaw 在功能完整性、社区活跃度和技术栈现代性方面具备较高的生产就绪度，适合作为 Android 环境下 AI 代理编排的核心组件。通过先行 PoC 验证后，配合安全与合规审查，即可在生产环境中安全、稳定地使用。

## 🧭 Practical evaluation

**Value:** eggbrid2/mobileClaw helps turn isolated prompts and tools into repeatable agent workflows.

**Best use cases**

- coordinate multi-agent workflows
- add tool-use pipelines
- standardize agent memory

**Integration notes:** Looks feasible to evaluate, but integration should start with a small proof of concept and README check.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 400 GitHub stars
- 16 forks
- updated 2026-06-26
- primary language: Kotlin
- 17 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 31/100 |
| stars | 55/100 |
| topics | 100/100 |
| outlook | 78/100 |
| quality | 72/100 |
| recency | 80/100 |
| adoption | 48/100 |
| production | 69/100 |
| usefulness | 90/100 |
| integration | 46/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 500/100 |

---

<sub>🔭 Discovered 2026-06-26 · [View on GitHub](https://github.com/eggbrid2/mobileClaw) · [← Back to Orchestration](./README.md)</sub>
