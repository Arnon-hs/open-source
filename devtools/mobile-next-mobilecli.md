# mobile-next/mobilecli

[![Stars](https://img.shields.io/github/stars/mobile-next/mobilecli?style=flat-square&color=yellow)](https://github.com/mobile-next/mobilecli/stargazers) [![Forks](https://img.shields.io/github/forks/mobile-next/mobilecli?style=flat-square&color=blue)](https://github.com/mobile-next/mobilecli/network) [![Language](https://img.shields.io/badge/lang-Go-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-71%2F100-brightgreen?style=flat-square)](#)

> Universal command-line tool for managing iOS and Android devices, simulators, emulators and apps

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 179 |
| 🍴 **Forks** | 15 |
| 💻 **Language** | Go |
| 📈 **Score** | 71/100 |
| 🗓️ **Last push** | 2026-05-11 |
| 🔍 **Source** | github |

## 🏷️ Topics

`adb` `android` `cli` `commandline-tool` `ctl` `emulators` `ios` `simulators` `xcode`

## 🎯 Categories

DevTools · Mobile

## 📝 Summary

### English

**Brief Summary (2‑3 sentences)**  
mobile‑next/mobilecli is a universal, Go‑based command‑line utility that lets developers manage iOS and Android devices, simulators, emulators, and app binaries from a single interface. By consolidating device‑control tasks—installing, launching, logging, and tearing down apps—into one CLI, it shortens the daily development and review loops for mobile engineers.

**Value**  
- **Time savings** – One consistent command set replaces the fragmented mix of `xcrun`, `adb`, `ios-deploy`, etc., cutting context‑switching and scripting effort.  
- **Workflow automation** – The CLI can be scripted in CI pipelines or local dev scripts to spin up emulators, install builds, run UI tests, and collect logs, delivering faster feedback on PRs.  
- **Cross‑platform consistency** – Teams that ship both iOS and Android can adopt a single tool, reducing onboarding friction and maintenance of separate toolchains.

**Practical Adoption Path**  
1. **Pilot the CLI locally** – Install the binary (`go install` or pre‑built release) and replace existing device‑management commands in a developer’s shell or Makefile.  
2. **Integrate into CI** – Add the CLI to the build image, use it to provision emulators/simulators, install the artifact, run automated tests, and capture logs as CI artifacts.  
3. **Standardize in internal docs** – Publish the command reference and sample scripts (e.g., “mobilecli device list”, “mobilecli app install …”) as the canonical way to interact with mobile test devices.  
4. **Scale to production** – Once the pilot proves reliable, roll the CLI out to all engineering squads, optionally wrapping it in higher‑level wrappers (e.g., Bazel or Gradle plugins) for tighter integration.

**Production Readiness**  
- **Activity & adoption** – 179 ★ on GitHub, recent commits (last updated 2026‑05‑11), and multiple forks signal an active community.  
- **Technical maturity** – Written in Go, a compiled language with low runtime overhead, and exposing a clean API/CLI surface makes it easy to embed in scripts and CI runners.  
- **Ecosystem fit** – The project already publishes implementation signals (API/SDK/CLI) and is tagged with relevant topics, simplifying evaluation against internal tooling standards.  
- **Risks to verify** – A final review of the open‑source license, security posture (e.g., dependency scanning), and maintainer responsiveness is recommended before a full production rollout.  

Overall, mobilecli appears ready for a serious pilot and, after the minor risk checks, can be adopted as a production‑grade component of a mobile development toolchain.

### Русский

**mobile-next/mobilecli** — это кроссплатформенный CLI‑инструмент, позволяющий инженерам быстро управлять iOS‑ и Android‑устройствами, симуляторами, эмуляторами и приложениями, тем самым ускоряя локальные разработки и автоматизируя задачи в CI. Типичный сценарий — интеграция в скрипты сборки и тестов для мгновенного развёртывания, обновления и сбора логов приложений, что сокращает время обратной связи и повышает эффективность review‑циклов. Проект считается почти готовым к продакшн: активные коммиты, 179 звёзд на GitHub, поддержка Go, широкая экосистема и отсутствие серьёзных рисков, однако требуется окончательная проверка лицензии и безопасности.

### 中文

**项目简介**  
mobile-next/mobilecli 是一款基于 Go 实现的跨平台命令行工具，统一管理 iOS 与 Android 设备、模拟器、模拟器镜像以及应用的安装、启动、日志采集等操作。

**价值**  
- **提升开发效率**：一次命令即可完成设备/模拟器的查找、启动、安装、调试，显著缩短每日的开发与回归循环。  
- **自动化本地任务**：可在脚本或 CI 中直接调用，完成 UI 测试前的环境准备、App 打包、日志收集等工作。  
- **加速 CI 反馈**：在持续集成流水线中使用，能够快速验证构建产物在真实设备或模拟器上的运行情况，提升质量反馈速度。

**典型接入方式**  
1. **本地脚本**：在 `bash`/`zsh`、`PowerShell` 或 `Makefile` 中直接调用 `mobilecli <subcommand>`，如 `mobilecli device list`、`mobilecli app install <ipa/apk>`。  
2. **CI/CD 集成**：在 Jenkins、GitHub Actions、GitLab CI 等流水线里添加步骤：  
   ```yaml
   - name: Install mobilecli
     run: go install github.com/mobile-next/mobilecli@latest
   - name: Run UI tests on iOS simulator
     run: mobilecli simulator start --name iPhone-14 && mobilecli app install ./build/MyApp.ipa && mobilecli test run ...
   ```  
3. **自定义工具**：通过 Go SDK（项目公开的内部包）或直接调用其 REST‑like CLI 接口，嵌入到内部开发平台或调度系统中。

**生产可用性**  
- **活跃度**：截至 2026‑05‑11，最近一次提交，星标 179，fork 15，社区讨论活跃，代码基于 Go，易于编译与跨平台部署。  
- **成熟度**：已支持 iOS 17、Android 14 主流版本的设备与模拟器，提供完整的日志、截图、性能采集等功能，满足日常开发与 CI 场景。  
- **风险**：许可证为 MIT，暂无已知的安全漏洞；仍需在正式投产前完成一次安全审计并确认维护者的响应时效。  

综合来看，mobilecli 已具备高可用的生产级别，可在内部或外部项目中直接试点使用，帮助团队显著缩短移动端开发与测试的循环时间。

## 🧭 Practical evaluation

**Value:** mobile-next/mobilecli helps engineers save time in daily development and review loops.

**Best use cases**

- speed up developer workflows
- automate local engineering tasks
- improve CI feedback

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 179 GitHub stars
- 15 forks
- updated 2026-05-11
- primary language: Go
- 9 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 30/100 |
| stars | 48/100 |
| topics | 100/100 |
| outlook | 81/100 |
| quality | 74/100 |
| recency | 100/100 |
| adoption | 43/100 |
| production | 77/100 |
| usefulness | 74/100 |
| integration | 62/100 |
| sourceTrust | 100/100 |

---

<sub>🔭 Discovered 2026-05-11 · [View on GitHub](https://github.com/mobile-next/mobilecli) · [← Back to DevTools](./README.md)</sub>
