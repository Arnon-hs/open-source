# dorssel/usbipd-win

[![Stars](https://img.shields.io/github/stars/dorssel/usbipd-win?style=flat-square&color=yellow)](https://github.com/dorssel/usbipd-win/stargazers) [![Forks](https://img.shields.io/github/forks/dorssel/usbipd-win?style=flat-square&color=blue)](https://github.com/dorssel/usbipd-win/network) [![Language](https://img.shields.io/badge/lang-C%23-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-60%2F100-brightgreen?style=flat-square)](#)

> Windows software for sharing locally connected USB devices to other machines, including Hyper-V guests and WSL 2.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 5.9k |
| 🍴 **Forks** | 360 |
| 💻 **Language** | C# |
| 📈 **Score** | 60/100 |
| 🗓️ **Last push** | 2026-09-05 |
| 🔍 **Source** | github |

## 🏷️ Topics

`hyper-v` `usb` `usbip` `usbip-win` `usbipd` `windows` `wsl` `wsl2`

## 🎯 Categories

Misc

## 📝 Summary

### English

**Brief Summary**  
dorssel/usbipd‑win is a Windows utility that lets you expose locally attached USB devices to other machines—such as Hyper‑V guests, WSL 2 instances, or remote hosts—by leveraging the USB/IP protocol. With over 5 800 stars, frequent updates (last commit 2026‑07‑03) and a solid C# codebase, it is a mature open‑source option for developers who need seamless USB passthrough across Windows‑based environments.

**Value**  
- **Cross‑environment USB sharing** – eliminates the need for physical device duplication or complex hardware KVMs when testing or running workloads in VMs, containers, or WSL 2.  
- **Open‑source & extensible** – you can audit, modify, or integrate the tool into custom CI/CD pipelines without licensing constraints.  
- **Broad community adoption** – the high star/fork count and recent activity indicate an active user base and quick issue resolution.

**Practical Adoption Path**  
1. **Proof‑of‑Concept** – Follow the README to install `usbipd-win` on the host, enable the USB/IP driver, and attach a test device to a WSL 2 or Hyper‑V VM.  
2. **Automation** – Script the `usbipd` commands (list, bind, attach) in PowerShell or your CI pipeline to provision devices on demand.  
3. **Integration** – Wrap the commands in a small wrapper service or Docker entrypoint if you need to expose devices to containerized workloads.  
4. **Validation** – Verify device stability, latency, and any driver‑specific quirks in a staging environment before rolling out to production.

**Production Readiness**  
- **Activity & Support** – Recent commits, active issue tracking, and a sizable contributor base suggest the project is well‑maintained.  
- **Stability** – The core USB/IP functionality is mature; most production concerns revolve around device‑specific drivers rather than the tool itself.  
- **Risk Mitigation** – The integration steps are not fully documented in metadata, so allocate time for initial setup validation and testing of your specific USB devices. Once the proof‑of‑concept passes, the tool is considered production‑ready for pilot deployments and can be scaled to larger environments.

### Русский

**dorssel/usbipd-win** — это open‑source‑утилита для Windows, позволяющая «выдавать» локально подключённые USB‑устройства другим машинам (например, гостям Hyper‑V или подсистеме WSL 2). При типичном внедрении достаточно установить пакет, настроить сервис и добавить нужные устройства в конфигурацию — после чего они становятся доступными в целевых средах без дополнительных драйверов. Проект демонстрирует высокий уровень готовности к продакшн: активная поддержка (обновления до 2026‑07‑03), более 5 800 звёзд, сотни форков и уже использующийся в реальных сценариях, однако перед масштабным rollout стоит проверить детали установки и интеграцию в конкретный workflow.

### 中文

**项目简介**  
dorssel/usbipd‑win 是一款 Windows 平台的开源工具，可将本机直接连接的 USB 设备通过网络共享给其他机器使用，支持 Hyper‑V 虚拟机、WSL 2 以及任意远程主机。  

**价值**  
- **跨平台 USB 访问**：在开发、测试或 CI 环境中，能够把本地硬件（如调试器、摄像头、加密狗）直接挂载到虚拟机或容器，避免重复采购硬件。  
- **即插即用**：通过简单的命令行或 PowerShell 脚本即可将设备绑定/解绑，几乎不需要额外驱动或复杂配置。  
- **开源且活跃**：拥有 5 880+ Stars、360+ Forks，最近一次提交就在 2026‑07‑03，社区响应及时，适合作为内部或商业项目的底层依赖。  

**典型接入方式**  
1. **环境准备**：在 Windows 主机上安装 `usbipd.exe`（可通过 GitHub Release 下载或使用 Chocolatey）。  
2. **设备注册**：`usbipd list` 查看本机 USB 列表，使用 `usbipd bind -b <busid>` 将目标设备绑定到 usbipd。  
3. **在目标机器上挂载**：  
   - **Hyper‑V**：在虚拟机设置里添加 “外部设备”，选择已绑定的 USB；或者在 VM 内部运行 `usbip attach -r <host_ip> -b <busid>`。  
   - **WSL 2**：在 WSL 终端执行 `usbip attach -r <host_ip> -b <busid>`，设备会出现在 `/dev/bus/usb`。  
4. **自动化**：把上述命令写入 PowerShell 脚本或 CI 步骤，实现“启动即挂载”、测试结束后 `usbipd unbind -b <busid>` 自动清理。  

**生产可用性**  
- **成熟度**：项目活跃，最近 3 个月内有多次代码提交和 Issue 响应，说明维护者对兼容性和安全性有持续关注。  
- **生态兼容**：已在多个公开案例中与 Hyper‑V、WSL 2、Docker Desktop（通过 Windows 主机）配合使用，且不依赖特定硬件。  
- **风险与建议**：集成路径主要通过命令行和 PowerShell，文档相对简洁，建议在正式上线前先做一个小范围的 PoC（例如在一台测试机器上把 USB 加密狗挂载到 WSL 2），评估网络延迟、权限配置（需要管理员或 “usbipd” 服务权限）以及设备兼容性。  

综上所述，dorssel/usbipd‑win 具备较高的生产就绪度，适合作为内部基础设施或 CI/CD 流水线中实现 USB 设备共享的关键组件。

## 🧭 Practical evaluation

**Value:** dorssel/usbipd-win may be useful when its README and activity match a concrete workflow.

**Best use cases**

- Not enough metadata yet.

**Integration notes:** Looks feasible to evaluate, but integration should start with a small proof of concept and README check.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 5880 GitHub stars
- 360 forks
- updated 2026-07-03
- primary language: C#
- 8 topics

**Risks:** Integration path is not obvious from metadata; validate setup cost before committing.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 64/100 |
| stars | 80/100 |
| topics | 100/100 |
| outlook | 75/100 |
| quality | 84/100 |
| recency | 80/100 |
| adoption | 76/100 |
| production | 71/100 |
| usefulness | 42/100 |
| integration | 30/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 0/100 |

---

<sub>🔭 Discovered 2026-07-03 · [View on GitHub](https://github.com/dorssel/usbipd-win) · [← Back to Misc](./README.md)</sub>
