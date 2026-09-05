# devicelab-dev/maestro-runner

[![Stars](https://img.shields.io/github/stars/devicelab-dev/maestro-runner?style=flat-square&color=yellow)](https://github.com/devicelab-dev/maestro-runner/stargazers) [![Forks](https://img.shields.io/github/forks/devicelab-dev/maestro-runner?style=flat-square&color=blue)](https://github.com/devicelab-dev/maestro-runner/network) [![Language](https://img.shields.io/badge/lang-Go-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-62%2F100-brightgreen?style=flat-square)](#)

> Fast mobile UI test automation for Android, iOS, React Native, Flutter & Expo. Open-source Maestro alternative — 100% free, no features behind a paywall. Supports real iOS devices, simulators, emulators, and cloud providers.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 389 |
| 🍴 **Forks** | 33 |
| 💻 **Language** | Go |
| 📈 **Score** | 62/100 |
| 🗓️ **Last push** | 2026-09-05 |
| 🔍 **Source** | github |

## 🏷️ Topics

`android` `appium` `ci-cd` `golang` `ios` `maestro` `mobile-testing` `test-automation` `ui-testing`

## 🎯 Categories

Automation · Frontend · DevTools · Mobile

## 📝 Summary

### English

**Brief Summary (2‑3 sentences)**  
`devicelab-dev/maestro‑runner` is an open‑source test‑automation engine that lets teams script and run UI tests across Android, iOS, React Native, Flutter and Expo without paying for a commercial Maestro license. It works with real devices, simulators, emulators and cloud providers, and is written in Go, currently boasting ~389 stars and active maintenance.

**Value**  
- **Eliminates repetitive manual UI work** by turning UI flows into declarative scripts that can be run on any supported platform.  
- **Unifies test automation** across heterogeneous mobile stacks (native, RN, Flutter, Expo) under a single, free tool, reducing the need for multiple proprietary frameworks.  
- **Integrates easily** with CI/CD pipelines, device farms, and other DevOps tools, enabling repeatable, scheduled test runs and operational tasks.

**Practical Adoption Path**  
1. **Proof‑of‑concept** – Clone the repo, run the provided examples on a local emulator/simulator, and verify that the test scripts cover a core user journey.  
2. **Read the README & docs** – Confirm required Go version, device‑setup steps, and any environment variables for cloud providers.  
3. **Integrate into CI** – Add a lightweight step (e.g., a GitHub Action or Jenkins stage) that pulls the repo, builds the binary, and executes your Maestro scripts against a test device farm.  
4. **Scale** – Gradually migrate existing manual test suites to Maestro scripts, add parallel execution on multiple devices, and hook into reporting tools (e.g., Allure, Slack).  

**Production Readiness**  
- **Activity & Community** – Recent commits (as of 2026‑07‑01), 389 stars, 33 forks, and multiple topics indicate healthy interest and ongoing maintenance.  
- **Platform Coverage** – Supports real iOS devices, simulators, Android emulators, and major cloud providers, covering most production mobile test environments.  
- **Stability** – The Go codebase is compact and compiled, reducing runtime dependencies; the project shows no known critical security issues, though a final license and security audit is recommended.  
- **Risk** – Verify the open‑source license compatibility with your organization and confirm that maintainers are responsive to bug reports before a full rollout.  

Overall, `maestro‑runner` is a mature, free alternative to commercial mobile UI test tools and is ready for a serious pilot in production after a small PoC and due‑diligence checks.

### Русский

Резюме проекта devicelab-dev/maestro-runner:

**Польза:** devicelab-dev/maestro-runner - это быстрая система автоматизации тестирования мобильных интерфейсов для Android, iOS, React Native, Flutter и Expo. Он позволяет автоматизировать повторяющиеся операции, сокращая время и усилия, необходимые для ручной работы.

**Типовой сценарий внедрения:** Проект предназначен для удаления ручной работы, соединения инструментов в повторяющиеся потоки и планирования операционных задач. Это может быть полезно для команд, которые хотят автоматизировать процессы тестирования и развертывания мобильных приложений.

**Уровень готовности к production:** Проект демонстрирует высокий уровень готовности к production, благодаря своевременной активности, широкому адоптированию и положительным сигналам из экосистемы. Однако, как и в случае с любым открытым исходным кодом, необходимо тщательно оценить лицензию, безопасность и участие активных maintainers.

### 中文

**项目价值**  
devicelab-dev/maestro‑runner 提供一站式的移动 UI 自动化测试框架，覆盖 Android、iOS、React Native、Flutter 与 Expo，且全部功能 100% 开源免费。它能够把繁琐的手动点击、截图、验证等操作转化为可编排、可重复的脚本，帮助团队消除重复劳动、提升测试覆盖率，并且可以轻松接入 CI/CD 流程，实现持续集成与持续交付。

**典型接入方式**  
1. **本地快速试用**：克隆仓库后直接运行 `go run .`（或使用提供的二进制），在本机的 Android Emulator、iOS Simulator 或真实设备上执行 Maestro 脚本。  
2. **CI/CD 集成**：在 GitHub Actions、GitLab CI、Jenkins 等流水线中添加一个步骤，使用官方 Docker 镜像或 pre‑built binary，执行 `maestro-runner run <script>`，并把测试结果以 JUnit/XML、HTML 或 Slack 通知的形式输出。  
3. **云端/设备实验室**：通过环境变量或配置文件指定 AWS Device Farm、Firebase Test Lab、Sauce Labs 等云提供商的设备 ID，即可在云端真实设备上运行同一套脚本，实现跨平台、跨设备的统一测试。

**生产可用性**  
- **活跃度**：最近一次提交（2026‑07‑01）且持续更新，GitHub Stars 389、Forks 33，社区活跃。  
- **技术成熟度**：核心实现使用 Go，二进制体积小、启动快，支持真实 iOS 设备、模拟器、Android Emulator 以及主流云平台。  
- **可评估性**：推荐先在小范围（单个模块或单一设备）做 PoC，验证脚本兼容性和 CI 集成方式；随后逐步扩展到全套回归套件。  
- **风险**：目前未发现重大许可证或安全隐患，但仍建议在正式投产前完成一次安全审计并确认维护者的响应速度。

综合来看，maestro‑runner 已具备 **高生产就绪度**，适合作为移动 UI 自动化的主力工具，在去除手工操作、实现可重复、可调度的测试流程方面能够为团队带来显著效益。

## 🧭 Practical evaluation

**Value:** devicelab-dev/maestro-runner helps remove repetitive manual operations from a workflow.

**Best use cases**

- remove manual work
- connect tools into repeatable flows
- schedule operational tasks

**Integration notes:** Looks feasible to evaluate, but integration should start with a small proof of concept and README check.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 389 GitHub stars
- 33 forks
- updated 2026-07-01
- primary language: Go
- 9 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 38/100 |
| stars | 55/100 |
| topics | 100/100 |
| outlook | 72/100 |
| quality | 73/100 |
| recency | 80/100 |
| adoption | 50/100 |
| production | 69/100 |
| usefulness | 58/100 |
| integration | 46/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 400/100 |

---

<sub>🔭 Discovered 2026-07-01 · [View on GitHub](https://github.com/devicelab-dev/maestro-runner) · [← Back to Automation](./README.md)</sub>
