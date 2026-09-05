# Fanju6/NetProxy-Magisk

[![Stars](https://img.shields.io/github/stars/Fanju6/NetProxy-Magisk?style=flat-square&color=yellow)](https://github.com/Fanju6/NetProxy-Magisk/stargazers) [![Forks](https://img.shields.io/github/forks/Fanju6/NetProxy-Magisk?style=flat-square&color=blue)](https://github.com/Fanju6/NetProxy-Magisk/network) [![Language](https://img.shields.io/badge/lang-Shell-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-60%2F100-brightgreen?style=flat-square)](#)

> Based on the sing-box core, this Android proxy module supports one-click start/stop of transparent proxy and is designed for Android devices.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 998 |
| 🍴 **Forks** | 53 |
| 💻 **Language** | Shell |
| 📈 **Score** | 60/100 |
| 🗓️ **Last push** | 2026-09-05 |
| 🔍 **Source** | github |

## 🏷️ Topics

`kernelsu-module` `magisk-module` `tproxy`

## 🎯 Categories

Networking · Mobile

## 📝 Summary

### English

**Summary**  
Fan ju6’s **NetProxy‑Magisk** is an Android‑focused proxy module built on the sing‑box core that lets users start or stop a transparent proxy with a single command. Packaged as a Magisk module, it targets engineers who need a quick, on‑device network proxy for development, testing, or CI feedback loops.  

**Value**  
- **Time‑saving**: One‑click activation eliminates the manual setup of VPN‑style proxies, letting developers spin up a transparent proxy in seconds.  
- **Workflow acceleration**: By routing traffic locally, it speeds up debugging of mobile back‑ends, API mocking, and performance testing without needing external hardware or cloud proxies.  
- **CI integration**: The module can be scripted in CI pipelines to provision a consistent network environment on Android test devices, improving reproducibility of test results.  

**Practical adoption path**  
1. **Proof‑of‑concept** – Clone the repo, follow the README to flash the Magisk module on a test device, and verify that transparent proxy start/stop works with your existing sing‑box configuration.  
2. **Pilot integration** – Wrap the start/stop commands in a small shell script or Gradle task used by a subset of developers; capture any dependency or permission issues.  
3. **Documentation & automation** – Extend the README with your internal usage patterns (e.g., CI job steps, environment variables) and add unit tests for the wrapper scripts.  
4. **Full rollout** – Deploy the scripted module across the device fleet via your device‑management tool, and monitor logs for stability.  

**Production readiness**  
- **Maturity**: Medium. The project has 998 ★, recent updates (June 2026), and a small but active codebase (Shell). It is suitable for prototypes, internal tooling, or staging environments.  
- **Considerations before production**:  
  * Verify the license compatibility with your product.  
  * Conduct a security audit of the Magisk module and the underlying sing‑box binary.  
  * Assess long‑term maintenance – confirm that maintainers are responsive and that you have a fallback plan for updates.  
- **Conclusion**: With a modest proof‑of‑concept and the above checks, NetProxy‑Magisk can be safely adopted for internal developer workflows and CI pipelines, while production‑grade deployments should await a formal security and maintenance review.

### Русский

**Fan​ju6/NetProxy‑Magisk** — модуль прокси для Android, построенный на ядре sing‑box, позволяющий одним нажатием включать и выключать прозрачный прокси прямо на устройстве. Он ускоряет рабочие процессы инженеров, автоматизируя локальные задачи разработки и улучшая обратную связь в CI, что делает его удобным для прототипов и внутренних пайплайнов; однако перед выводом в продакшн рекомендуется провести небольшой proof‑of‑concept, проверить README и уточнить вопросы лицензии, безопасности и поддержки. В целом готовность к production — средняя: проект имеет 998 звёзд, активные обновления и небольшие зависимости, но требует окончательной проверки сопровождаемости.

### 中文

**项目简介**  
Fanju6/NetProxy‑Magisk 基于 sing‑box 内核，实现了 Android 设备上一键启动/停止的透明代理模块，适配 Magisk 环境，便于在手机上快速搭建本地代理。

**价值**  
- **提升研发效率**：开发者只需几秒即可在手机上开启透明代理，省去手动配置 VPN/代理的繁琐步骤。  
- **加速本地调试与 CI 反馈**：在移动端进行接口抓包、流量重放或自动化测试时，可即时切换代理，缩短调试-验证循环。  
- **降低运维成本**：统一的 Magisk 模块可在多台设备上批量部署，避免每台设备单独配置。

**典型接入方式**  
1. **准备环境**：确保设备已 root 并安装 Magisk。  
2. **安装模块**：在 Magisk Manager 中添加本仓库的 Release 包（或自行编译 `install.sh`），点击“一键安装”。  
3. **启动代理**：打开系统 UI（或通过 `adb shell netproxy start`）即可激活透明代理；同理使用 `netproxy stop` 停止。  
4. **验证**：通过 `curl`、`adb logcat` 或抓包工具确认流量已走代理。  
5. **CI 集成（可选）**：在 CI 脚本中加入 `adb push install.sh /data/local/tmp && adb shell sh /data/local/tmp/install.sh && adb shell netproxy start`，实现自动化部署。

**生产可用性**  
- **成熟度**：当前评分 63/100，适合作为原型或内部工具使用。  
- **依赖与维护**：核心为 Shell 脚本，依赖 sing‑box 二进制；项目最近更新（2026‑06‑27），但仍需确认维护者活跃度和安全审计。  
- **上线建议**：在正式生产前，先在小范围设备上完成 PoC，检查：  
  - 许可证兼容性（MIT/Apache 等）  
  - sing‑box 版本安全性  
  - Magisk 模块的升级与回滚流程  
- **风险**：暂无重大元数据风险，但仍需对代码审计、漏洞披露渠道以及长期维护计划进行最终评估。

**总结**  
NetProxy‑Magisk 为 Android 开发者提供了“一键透明代理”的便捷方案，能够显著缩短本地调试和 CI 反馈时间。通过 Magisk 模块化部署，接入成本低，适合作为内部研发或原型环境的加速工具；在正式生产环境使用前，建议完成小规模验证并进行安全/维护审查。

## 🧭 Practical evaluation

**Value:** Fanju6/NetProxy-Magisk helps engineers save time in daily development and review loops.

**Best use cases**

- speed up developer workflows
- automate local engineering tasks
- improve CI feedback

**Integration notes:** Looks feasible to evaluate, but integration should start with a small proof of concept and README check.

**Production readiness:** Medium: useful for prototypes or internal workflows, with dependency and maintenance checks before production.

**Quality signals**

- 998 GitHub stars
- 53 forks
- updated 2026-06-27
- primary language: Shell
- 3 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 43/100 |
| stars | 64/100 |
| topics | 38/100 |
| outlook | 68/100 |
| quality | 67/100 |
| recency | 80/100 |
| adoption | 58/100 |
| production | 67/100 |
| usefulness | 58/100 |
| integration | 46/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 200/100 |

---

<sub>🔭 Discovered 2026-06-27 · [View on GitHub](https://github.com/Fanju6/NetProxy-Magisk) · [← Back to Networking](./README.md)</sub>
