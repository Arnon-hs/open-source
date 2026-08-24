# lycorp-jp/sim-use

[![Stars](https://img.shields.io/github/stars/lycorp-jp/sim-use?style=flat-square&color=yellow)](https://github.com/lycorp-jp/sim-use/stargazers) [![Forks](https://img.shields.io/github/forks/lycorp-jp/sim-use?style=flat-square&color=blue)](https://github.com/lycorp-jp/sim-use/network) [![Language](https://img.shields.io/badge/lang-Swift-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-55%2F100-brightgreen?style=flat-square)](#)

> Give your AI agent eyes and hands on iOS Simulator and Android emulator/devices.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 374 |
| 🍴 **Forks** | 18 |
| 💻 **Language** | Swift |
| 📈 **Score** | 55/100 |
| 🗓️ **Last push** | 2026-08-24 |
| 🔍 **Source** | github |

## 🏷️ Topics

`accessibility` `ai-agents` `ai-development` `android-emulator` `ios-simulator` `mobile-automation`

## 🎯 Categories

Automation · AI/ML · Mobile

## 📝 Summary

### English

**Brief Summary**  
`lycorp-jp/sim-use` is an open‑source toolkit that lets AI agents interact with iOS Simulators and Android emulators/devices, turning visual and touch actions into programmable inputs. By automating repetitive UI tasks, it enables developers to embed AI‑driven testing, data‑collection, or bot‑driven workflows directly into mobile pipelines.

**Value**  
- **Automation of manual UI work** – eliminates the “click‑through” steps that developers and QA engineers normally perform by hand.  
- **AI‑ready interface** – the agent can “see” the screen (via screenshots) and “act” (tap, swipe, type), making it easy to plug in vision or language models for tasks such as automated testing, content generation, or device‑level data harvesting.  
- **Workflow integration** – can be chained with CI/CD tools, scheduling systems, or other automation scripts to create repeatable, end‑to‑end pipelines.

**Practical Adoption Path**  
1. **Proof‑of‑Concept** – clone the repo, run the provided README examples on a local Mac (iOS) or Android Studio instance to confirm the agent can launch the simulator/emulator and perform basic actions.  
2. **Wrap in a CLI/Script** – expose the core functions (e.g., `runAction`, `captureScreen`) as a small command‑line wrapper that your CI job can invoke.  
3. **Integrate with your AI model** – feed the screenshots to your model, parse its output, and call the wrapper to execute the suggested UI actions.  
4. **Scale to Scheduling** – once the loop works reliably, add a scheduler (cron, GitHub Actions, Jenkins) to run the flow on a regular basis or as part of pull‑request validation.

**Production Readiness**  
- **Maturity**: Medium. The project is actively maintained (last update 2026‑07‑01), has 374 stars and 18 forks, and is written in Swift, indicating a solid base for iOS work.  
- **Suitability**: Ideal for prototypes, internal tooling, or QA automation where the integration cost can be evaluated early.  
- **Risks**: The integration steps are not fully documented; you’ll need to verify device‑setup scripts, simulator licensing, and Android SDK versions before committing to production. A small pilot will surface any hidden dependencies and allow you to gauge maintenance effort.  

Overall, `sim-use` offers a compelling way to give AI agents “eyes and hands” on mobile platforms, with a clear, incremental path from experiment to production‑grade automation.

### Русский

**lycorp-jp/sim-use** — открытый инструмент, позволяющий AI‑агентам управлять iOS‑симулятором и Android‑эмуляторами/устройствами, тем самым автоматизируя рутинные действия в мобильных тестах и CI‑процессах. Типичный сценарий: в рамках небольшого proof‑of‑concept подключаем библиотеку к существующему пайплайну, заменяем ручные клики и ввод данных, а затем масштабируем процесс в повторяемый workflow с планированием задач. Готовность к production — средняя: проект стабилен для прототипов и внутренних систем, но требует проверки зависимостей, настройки окружения и небольших доработок перед выводом в продакшн.

### 中文

**简短介绍**

lycorp-jp/sim-use 是一个开源项目，允许为您的 AI 代理在 iOS Simulator 和 Android 模拟器/设备上添加视觉和操作能力。它可以帮助减少重复的手动操作，提高工作流的自动化程度。

**价值**

* 移除重复的手动操作
* 连接工具形成可重复的流程
* 规划操作任务

**典型接入方式**

1. 首先评估项目的可行性
2. 阅读 README 文档
3. 开始一个小的原型验证
4. 检查依赖项和维护成本

**生产可用性**

* 项目的生产可用性为中等
* 适合用于原型或内部工作流
* 必须检查依赖项和维护成本才能确保项目的稳定性

## 🧭 Practical evaluation

**Value:** lycorp-jp/sim-use helps remove repetitive manual operations from a workflow.

**Best use cases**

- remove manual work
- connect tools into repeatable flows
- schedule operational tasks

**Integration notes:** Looks feasible to evaluate, but integration should start with a small proof of concept and README check.

**Production readiness:** Medium: useful for prototypes or internal workflows, with dependency and maintenance checks before production.

**Quality signals**

- 374 GitHub stars
- 18 forks
- updated 2026-07-01
- primary language: Swift
- 6 topics

**Risks:** Integration path is not obvious from metadata; validate setup cost before committing.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 32/100 |
| stars | 55/100 |
| topics | 75/100 |
| outlook | 58/100 |
| quality | 58/100 |
| recency | 40/100 |
| adoption | 48/100 |
| production | 52/100 |
| usefulness | 74/100 |
| integration | 30/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 300/100 |

---

<sub>🔭 Discovered 2026-07-01 · [View on GitHub](https://github.com/lycorp-jp/sim-use) · [← Back to Automation](./README.md)</sub>
