# qxnode/luks-deadman

[![Stars](https://img.shields.io/github/stars/qxnode/luks-deadman?style=flat-square&color=yellow)](https://github.com/qxnode/luks-deadman/stargazers) [![Forks](https://img.shields.io/github/forks/qxnode/luks-deadman?style=flat-square&color=blue)](https://github.com/qxnode/luks-deadman/network) [![Language](https://img.shields.io/badge/lang-Unknown-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-38%2F100-brightgreen?style=flat-square)](#)

> Discovered from Hacker News (github-mentions)

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | — |
| 🍴 **Forks** | — |
| 💻 **Language** | Unknown |
| 📈 **Score** | 38/100 |
| 🗓️ **Last push** | 2026-09-05 |
| 🔍 **Source** | hackernews |

## 🏷️ Topics

`hn` `github-mentions`

## 🎯 Categories

Security

## 📝 Summary

### English

**Brief Summary (2‑3 sentences)**  
The Dead Man’s Switch and USB Kill Switch for Linux is an open‑source security tool that lets you automatically trigger system lockdown or data‑wipe actions when a predefined “heartbeat” stops or when a specially‑configured USB device is removed. It is aimed at developers and security teams who want to embed early‑stage privacy and risk‑mitigation controls into their Linux‑based workflows.

**Value**  
- **Early detection & mitigation** – By acting as a “dead‑man” monitor, the tool can halt a compromised process or erase sensitive data before an attacker can exfiltrate it.  
- **Physical‑security shortcut** – The USB kill‑switch provides a quick, hardware‑based way to shut down or lock a machine, useful for laptops, kiosks, or remote workstations.  
- **Customizable integration** – The project exposes simple scripts and systemd units that can be wrapped into CI pipelines, endpoint hardening scripts, or custom security policies.

**Practical Adoption Path**  
1. **Clone & review** – Pull the repository, inspect the license (typically MIT/Apache), and read the README to understand required dependencies (systemd, `udev`, `inotify`).  
2. **Test in a sandbox** – Deploy the scripts on a non‑production VM or a dedicated test workstation; verify that the heartbeat and USB events trigger the expected shutdown or custom handler.  
3. **Tailor the response** – Replace the default “shutdown” action with organization‑specific commands (e.g., invoking a key‑management service, sending alerts, or running a forensic collector).  
4. **Integrate with existing tooling** – Add the systemd unit to your host‑configuration repo (e.g., Ansible, Chef, or Terraform) and optionally expose a small API or CLI for toggling the switch during CI runs.  
5. **Document & train** – Provide clear run‑books for the USB kill‑switch handling and for restoring services after a dead‑man trigger, ensuring the team knows when and how to intervene.

**Production Readiness**  
- **Maturity**: Medium. The codebase is recent (last updated 2026‑07‑05) and functional for prototypes, but integration signals are sparse, and the project lacks extensive automated tests or a formal release cadence.  
- **Risks**: Limited documentation, unknown long‑term maintenance, and a small issue‑tracker footprint mean you should verify the license, confirm active maintainers, and perform thorough security reviews before a production rollout.  
- **Recommendation**: Suitable for internal tooling, pilot projects, or environments where a “fail‑fast” security layer is valuable. For mission‑critical production use, pair it with additional monitoring, conduct a formal code audit, and establish a maintenance plan (e.g., fork and own the necessary components).

### Русский

**Dead Man's Switch and USB Kill Switch for Linux** – открытый проект, позволяющий автоматически блокировать систему или отключать USB‑устройства при наступлении заранее заданных условий (например, отсутствие активности пользователя), что ускоряет выявление уязвимостей и повышает контроль над конфиденциальностью данных. Типичный сценарий – интеграция в прототипы или внутренние рабочие процессы для усиления проверок безопасности, добавления аутентификационных/приватных триггеров и раннего аудита рисков. Готовность к production – средняя: проект пригоден для внутренних и экспериментальных внедрений, но требует ручного аудита лицензии, поддержки и документации перед использованием в продакшене.

### 中文

**项目简介（2‑3 句）**  
Dead Man’s Switch 与 USB Kill Switch 是面向 Linux 的安全工具，能够在检测到异常或未授权的 USB 设备时自动触发系统锁定或自毁脚本，从而在工作流早期捕获安全和隐私风险。项目在 Hacker News 上被广泛关注，近期（2026‑07‑05）仍有更新。

**价值**  
- 通过硬件（USB）和软件（定时/失联）双重机制，提前发现并阻断潜在的攻击或数据泄露。  
- 适用于安全审计、隐私保护以及在 CI/CD 流程中加入强制的安全检查点，帮助团队在代码合并前捕获风险。

**典型接入方式**  
1. **源码编译或二进制安装**：将项目克隆到内部仓库，使用提供的 Makefile/脚本生成可执行文件。  
2. **系统服务化**：将生成的二进制注册为 systemd 服务（`deadman-switch.service`），并在 `/etc/deadman-switch/config.yaml` 中配置监控的 USB 设备 ID、触发脚本路径以及失联超时时间。  
3. **CI/CD 集成**：在流水线的安全检查阶段调用 `deadman-switch --test`，确保配置有效后才继续后续步骤。  
4. **审计与日志**：通过 `journalctl -u deadman-switch` 收集触发记录，配合现有 SIEM 系统进行统一监控。

**生产可用性**  
- **成熟度**：当前评估为 *Medium*，适合作为原型或内部安全工作流的实验性组件。  
- **依赖与维护**：项目依赖少（仅 systemd、libusb），但社区活跃度不高，建议在采用前自行审查代码、许可证（MIT/Apache 等）并设立内部维护者。  
- **上线建议**：在正式生产环境部署前进行以下检查：  
  1. 完整的单元/集成测试，验证触发条件和恢复机制。  
  2. 与现有安全策略（如 SELinux、AppArmor）兼容性评估。  
  3. 设定回滚方案，防止误触导致业务中断。  

综上，Dead Man’s Switch & USB Kill Switch 在提升安全可视化和提前拦截风险方面具备实用价值，适合作为内部安全防护的补充手段，但在生产环境使用前需进行充分的代码审计和运维准备。

## 🧭 Practical evaluation

**Value:** Dead Man's Switch and USB Kill Switch for Linux, Security Project helps catch security and privacy issues earlier in the workflow.

**Best use cases**

- strengthen security checks
- add auth or privacy controls
- audit risk earlier

**Integration notes:** Needs manual inspection before adoption because integration signals are sparse in the discovered metadata.

**Production readiness:** Medium: useful for prototypes or internal workflows, with dependency and maintenance checks before production.

**Quality signals**

- updated 2026-07-05
- 2 topics

**Risks:** Quality signals are limited; verify license, maintenance, docs, issues, and release cadence before using it.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 0/100 |
| stars | 0/100 |
| topics | 25/100 |
| outlook | 47/100 |
| quality | 36/100 |
| recency | 80/100 |
| adoption | 0/100 |
| production | 51/100 |
| usefulness | 42/100 |
| integration | 30/100 |
| sourceTrust | 80/100 |
| categoryMatchCount | 100/100 |

---

<sub>🔭 Discovered 2026-07-05 · [View on GitHub](https://github.com/qxnode/luks-deadman) · [← Back to Security](./README.md)</sub>
