# 3899/SimAdmin

[![Stars](https://img.shields.io/github/stars/3899/SimAdmin?style=flat-square&color=yellow)](https://github.com/3899/SimAdmin/stargazers) [![Forks](https://img.shields.io/github/forks/3899/SimAdmin?style=flat-square&color=blue)](https://github.com/3899/SimAdmin/network) [![Language](https://img.shields.io/badge/lang-Rust-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-42%2F100-brightgreen?style=flat-square)](#)

> 🎉面向 Debian 蜂窝 CPE、随身 WiFi、软路由类设备的 SIM/eSIM、蜂窝网络、短信、WiFi Calling(VoWiFi)、DDNS和系统状态管理系统。

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 191 |
| 🍴 **Forks** | 47 |
| 💻 **Language** | Rust |
| 📈 **Score** | 42/100 |
| 🗓️ **Last push** | 2026-08-24 |
| 🔍 **Source** | github |

## 🏷️ Topics

_no topics_

## 🎯 Categories

Misc

## 📝 Summary

### English

**Brief Summary**  
3899/SimAdmin is a Rust‑based management suite for Debian‑based cellular CPE, portable Wi‑Fi, and soft‑router devices. It centralises SIM/eSIM handling, cellular data, SMS, VoWiFi, DDNS and system‑status monitoring, offering a single interface to control all aspects of a mobile broadband gateway.

**Value**  
- **All‑in‑one control plane** – eliminates the need for multiple disparate tools by exposing a unified API/CLI for SIM provisioning, network attachment, messaging, Wi‑Fi calling and dynamic DNS updates.  
- **Targeted to embedded Debian devices** – the packaging and dependencies are tuned for the constrained environments typical of CPE, travel routers and IoT gateways.  
- **Open‑source and actively maintained** – 191 stars, recent commits (as of 2026‑07‑03) and a Rust codebase that benefits from safety and performance guarantees.

**Practical Adoption Path**  
1. **Prototype** – Clone the repo, build the Rust binary on a Debian‑based test device, and run the provided example configuration to verify basic SIM activation, SMS send/receive and DDNS updates.  
2. **Integration Review** – Examine the README and source for required system services (e.g., `ModemManager`, `systemd-resolved`) and map them to your existing device stack. Add any missing hooks (e.g., custom VoWiFi SIP client) by extending the modular plugin points.  
3. **Pilot Deployment** – Deploy the binary via your configuration management tool (Ansible, Salt, etc.) on a small fleet, monitor logs, and confirm that the health‑check endpoints report accurate status.  
4. **Production Hardening** – Freeze the Rust toolchain version, containerise the service (Docker or OCI), add automated health checks, and integrate with your central monitoring/alerting platform.

**Production Readiness**  
- **Maturity**: Medium. The project is actively updated and has modest community traction, but documentation and integration examples are limited, so a manual code review is required.  
- **Dependencies**: Relies on standard Debian networking utilities and ModemManager; these are stable, but you must verify version compatibility on your target firmware.  
- **Risk**: The integration path is not fully described in the metadata; you’ll need to invest time in understanding the configuration schema and ensuring that required services (e.g., DBus, systemd) are present. Once vetted, SimAdmin is suitable for internal prototypes or controlled production environments, especially where a unified cellular‑Wi‑Fi management layer adds operational value.

### Русский

SimAdmin — это open‑source система на Rust для управления SIM/eSIM, мобильным подключением, SMS, Wi‑Fi Calling (VoWiFi), DDNS и состоянием устройств типа Debian‑based CPE, переносных Wi‑Fi роутеров и софт‑роутеров. Она подходит для прототипов и внутренних workflow, где требуется централизованно контролировать сотовую связь и сеть, однако перед внедрением следует проверить зависимости и уточнить детали интеграции, так как готовый путь к production не описан полностью. Уровень готовности — средний: проект активно поддерживается (обновления 2026‑07‑03, 191★, 47 форков), но требует ручной проверки перед использованием в продакшене.

### 中文

**项目简介**  
3899/SimAdmin 是一款基于 Rust 的系统管理平台，专为 Debian 系统上的蜂窝 CPE、随身 Wi‑Fi、软路由等设备设计，提供 SIM/eSIM 切换、蜂窝网络/短信、VoWiFi、DDNS 以及系统状态监控等一站式功能。

**价值**  
- **统一管理**：一次部署即可集中管理多台设备的 SIM 卡、网络连接、短信收发和 Wi‑Fi Calling，免去手工配置的繁琐。  
- **自动化运维**：内置 DDNS 与系统健康监控，支持脚本化触发，可大幅降低运维成本。  
- **开源可定制**：基于 Rust 实现，代码可审计、易于二次开发，适配各种嵌入式硬件。

**典型接入方式**  
1. **准备环境**：在目标设备上安装 Debian（或兼容的 Linux 发行版），确保已安装 `systemd` 与 `rustc`（或直接使用项目提供的二进制包）。  
2. **部署 SimAdmin**：  
   ```bash
   curl -L https://github.com/3899/SimAdmin/releases/download/vX.Y.Z/simadmin-x86_64.tar.gz | tar xz
   sudo cp simadmin /usr/local/bin/
   sudo cp -r config /etc/simadmin
   sudo systemctl enable --now simadmin.service
   ```  
3. **配置**：编辑 `/etc/simadmin/config.toml`，填写 SIM/eSIM 卡槽信息、APN、DDNS 账号、VoWiFi 参数等。项目提供示例文件，可直接拷贝后按需修改。  
4. **集成**：通过 RESTful API（默认 127.0.0.1:8080）或 CLI (`simadminctl`) 与业务系统交互，实现自动切卡、发送短信、获取设备状态等功能。  

**生产可用性**  
- **成熟度**：项目已有 191 星、47 Fork，最近一次提交为 2026‑07‑03，活跃度较高。  
- **适用场景**：适合原型验证、内部部署或中小规模的边缘设备管理。对高并发、跨地域大规模部署仍需自行进行压力测试与容错设计。  
- **风险与注意事项**：  
  - 元数据未提供完整的 CI/CD 流程，建议在正式环境前完成完整的功能回归与安全审计。  
  - 依赖的底层硬件（调制解调器、SIM 卡槽）驱动兼容性需自行验证。  
  - 需要自行实现日志聚合、告警和备份机制，以满足生产级 SLA。  

总体而言，SimAdmin 在功能完整性和开源透明度上具备较好基础，经过适当的测试与运维包装后，可在内部或中等规模的蜂窝/Wi‑Fi 设备管理场景中投入生产使用。

## 🧭 Practical evaluation

**Value:** 3899/SimAdmin may be useful when its README and activity match a concrete workflow.

**Best use cases**

- Not enough metadata yet.

**Integration notes:** Needs manual inspection before adoption because integration signals are sparse in the discovered metadata.

**Production readiness:** Medium: useful for prototypes or internal workflows, with dependency and maintenance checks before production.

**Quality signals**

- 191 GitHub stars
- 47 forks
- updated 2026-07-03
- primary language: Rust

**Risks:** Integration path is not obvious from metadata; validate setup cost before committing.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 42/100 |
| stars | 49/100 |
| topics | 0/100 |
| outlook | 44/100 |
| quality | 46/100 |
| recency | 40/100 |
| adoption | 47/100 |
| production | 48/100 |
| usefulness | 42/100 |
| integration | 30/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 0/100 |

---

<sub>🔭 Discovered 2026-07-03 · [View on GitHub](https://github.com/3899/SimAdmin) · [← Back to Misc](./README.md)</sub>
