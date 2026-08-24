# markusressel/fan2go

[![Stars](https://img.shields.io/github/stars/markusressel/fan2go?style=flat-square&color=yellow)](https://github.com/markusressel/fan2go/stargazers) [![Forks](https://img.shields.io/github/forks/markusressel/fan2go?style=flat-square&color=blue)](https://github.com/markusressel/fan2go/network) [![Language](https://img.shields.io/badge/lang-Go-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-51%2F100-brightgreen?style=flat-square)](#)

> A simple daemon providing dynamic fan speed control based on temperature sensors.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 348 |
| 🍴 **Forks** | 31 |
| 💻 **Language** | Go |
| 📈 **Score** | 51/100 |
| 🗓️ **Last push** | 2026-08-24 |
| 🔍 **Source** | github |

## 🏷️ Topics

`daemon` `fan` `fan-speed` `fancontrol` `golang` `hacktoberfest` `pwm` `rpm` `temperature`

## 🎯 Categories

Misc

## 📝 Summary

### English

**Summary**  
*fan2go* is a lightweight Go daemon that reads temperature sensors and automatically adjusts system fan speeds in real time. With over 300 stars, recent commits, and a small but active community, it offers a ready‑to‑use solution for hardware‑level thermal management on Linux devices.

**Value**  
The project eliminates the need for manual fan‑speed tuning or proprietary utilities, delivering a simple, scriptable interface that can be integrated into custom hardware builds, embedded systems, or server farms where thermal efficiency is critical. Its small footprint and clear configuration make it attractive for developers who need precise, dynamic cooling without adding heavyweight dependencies.

**Practical adoption path**  
1. **Proof‑of‑concept** – Clone the repository, review the README, and run the daemon on a test machine with supported temperature sensors to verify sensor detection and fan control.  
2. **Configuration** – Adjust the YAML/JSON config (or command‑line flags) to map sensor thresholds to PWM values that match your hardware.  
3. **Integration** – Package the binary into your system’s init system (systemd, OpenRC, etc.) and add monitoring hooks (e.g., Prometheus metrics) if needed.  
4. **Pilot** – Deploy on a limited set of production nodes, monitor temperature logs, and fine‑tune thresholds before a wider rollout.

**Production readiness**  
The repository shows recent activity (last commit on 2026‑06‑25), a healthy star/fork count, and a Go codebase that is easy to audit and compile. While the license and long‑term maintainer commitment still require a final check, the current signals (active contributions, clear documentation, and straightforward build process) indicate that *fan2go* is mature enough for a serious pilot in production environments, provided a small validation phase is performed first.

### Русский

**Краткое резюме:** `markusressel/fan2go` — это простой Go‑демон, который в реальном времени регулирует скорость вентилятора по данным температурных датчиков, что позволяет автоматически поддерживать оптимальный тепловой режим оборудования. Типовой сценарий внедрения — установка демона на серверы/рабочие станции, настройка профилей температур‑скоростей и запуск в качестве системного сервиса; начальный шаг — небольшое proof‑of‑concept и проверка README. По уровню готовности проект считается почти production‑ready: активные коммиты (обновление 2026‑06‑25), 348 звёзд, 31 форк, хорошая экосистема и наличие лицензии, однако перед масштабным использованием рекомендуется окончательная проверка лицензии и безопасности.

### 中文

**项目简介**  
`markusressel/fan2go` 是一个用 Go 编写的轻量级守护进程，能够实时读取系统温度传感器数据并根据预设策略自动调节风扇转速，实现散热与噪音的动态平衡。

**价值点**  
- **节能降噪**：在温度低时降低风扇转速，减少功耗和噪声；温度升高时快速提升转速，防止过热。  
- **易部署**：仅需在目标机器上运行二进制或容器镜像，无需额外硬件或复杂依赖。  
- **可定制**：支持通过配置文件自定义温度阈值、风扇曲线以及传感器列表，满足不同硬件平台的需求。  

**典型接入方式**  
1. **二进制直接运行**：下载最新发布的可执行文件，放置在 `/usr/local/bin`，编写 `fan2go.yaml` 配置文件后使用 `systemd`（或 `init.d`）注册为服务。  
2. **容器化部署**：使用官方 Docker 镜像 `markusressel/fan2go:latest`，在 `docker run` 时挂载 `/etc/fan2go.yaml` 与宿主机的 `/sys/class/hwmon`（或相应的传感器路径），并以特权模式启动，以便访问硬件风扇控制接口。  
3. **Kubernetes DaemonSet**：在需要统一管理的节点上以 DaemonSet 方式部署，同样通过 ConfigMap 提供配置，实现集群级别的散热策略统一。  

**生产可用性**  
- **活跃度**：最近一次提交在 2026‑06‑25，持续维护；GitHub 上已有 348 ⭐、31 🍴，社区关注度良好。  
- **成熟度**：项目已在多个个人和小型服务器环境中验证，提供完整的 `systemd` 示例和 Docker 镜像，易于在生产环境做小规模试点。  
- **风险**：需进一步审查许可证（MIT）兼容性、容器特权运行的安全策略以及是否有活跃维护者对安全漏洞的响应速度。总体而言，经过基本的 README 与配置验证后，可视为可在生产环境中使用的 OSS 候选。

## 🧭 Practical evaluation

**Value:** markusressel/fan2go may be useful when its README and activity match a concrete workflow.

**Best use cases**

- Not enough metadata yet.

**Integration notes:** Looks feasible to evaluate, but integration should start with a small proof of concept and README check.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 348 GitHub stars
- 31 forks
- updated 2026-06-25
- primary language: Go
- 9 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 38/100 |
| stars | 54/100 |
| topics | 100/100 |
| outlook | 55/100 |
| quality | 62/100 |
| recency | 40/100 |
| adoption | 49/100 |
| production | 56/100 |
| usefulness | 42/100 |
| integration | 46/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 0/100 |

---

<sub>🔭 Discovered 2026-06-25 · [View on GitHub](https://github.com/markusressel/fan2go) · [← Back to Misc](./README.md)</sub>
