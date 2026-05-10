# home-assistant-ecosystem/home-assistant-cli

[![Stars](https://img.shields.io/github/stars/home-assistant-ecosystem/home-assistant-cli?style=flat-square&color=yellow)](https://github.com/home-assistant-ecosystem/home-assistant-cli/stargazers) [![Forks](https://img.shields.io/github/forks/home-assistant-ecosystem/home-assistant-cli?style=flat-square&color=blue)](https://github.com/home-assistant-ecosystem/home-assistant-cli/network) [![Language](https://img.shields.io/badge/lang-Python-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-76%2F100-brightgreen?style=flat-square)](#)

> :computer: Command-line tool for Home Assistant

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 558 |
| 🍴 **Forks** | 83 |
| 💻 **Language** | Python |
| 📈 **Score** | 76/100 |
| 🗓️ **Last push** | 2026-05-10 |
| 🔍 **Source** | github |

## 🏷️ Topics

`cli` `home-assistant` `home-automation` `iot` `smart-home`

## 🎯 Categories

Automation · DevTools

## 📝 Summary

### English

**Brief Summary**  
Home‑Assistant‑CLI is a Python‑based command‑line interface that lets you interact with a Home Assistant instance from the terminal. It streamlines repetitive tasks—such as entity management, service calls, and automations—so they can be scripted, chained with other tools, or scheduled for regular execution.

**Value**  
- **Automation of manual steps** – eliminates the need to click through the UI for routine actions, turning them into repeatable scripts.  
- **Tool‑chain friendly** – works well with CI/CD pipelines, cron jobs, or any shell‑based workflow, enabling “infrastructure‑as‑code” style management of Home Assistant.  
- **Rapid prototyping** – developers can test API calls and debug automations locally without opening the web UI.

**Practical Adoption Path**  
1. **Install** the package (`pip install homeassistant-cli`) on any machine that can reach your Home Assistant server.  
2. **Configure** a short‑lived long‑lived access token in Home Assistant and store it in `~/.homeassistant-cli`.  
3. **Start scripting**: use `hass-cli` commands (e.g., `hass-cli service call light.turn_on`) inside Bash, Python, or Makefiles.  
4. **Integrate** with existing automation platforms (Ansible, Terraform, GitHub Actions) or schedule with cron/systemd timers for recurring jobs.  
5. **Monitor** success/failure via CLI exit codes and logs, adding alerts to your observability stack if needed.

**Production Readiness**  
- **Active maintenance**: last commit on 2026‑05‑10, 558 stars, 83 forks, and a healthy issue/PR flow indicate an engaged community.  
- **Mature codebase**: written in Python, a language widely used for Home Assistant extensions, with clear API/SDK exposure.  
- **Low integration risk**: the CLI only talks to Home Assistant’s public REST/WebSocket API, so it can be sandboxed behind network policies.  
- **Remaining checks**: verify the MIT‑style license compatibility, run a security audit of the installed dependencies, and confirm that at least one maintainer is actively responding to security issues before a full production rollout.

Overall, Home‑Assistant‑CLI is a solid, production‑grade tool for turning Home Assistant interactions into automated, repeatable processes.

### Русский

**home-assistant-ecosystem/home-assistant-cli** — это Python‑инструмент командной строки, который автоматизирует рутинные операции с Home Assistant, позволяя интегрировать его в скрипты, CI/CD‑конвейеры и планировщики задач. Типичный сценарий: вместо ручного ввода запросов в веб‑интерфейс вы вызываете CLI для включения/выключения устройств, получения состояния датчиков или деплоя конфигураций, что упрощает построение повторяемых рабочих потоков. Проект имеет высокую готовность к production: активные коммиты, 558★, 83 форка, поддержка API/SDK и широкий набор тем, однако перед масштабным внедрением стоит уточнить лицензию, безопасность и наличие постоянных мейнтейнеров.

### 中文

**项目简介（2‑3 句）**  
home‑assistant‑ecosystem/home‑assistant‑cli 是一款基于 Python 的命令行工具，专为 Home Assistant 打造，可在终端直接调用 Home Assistant 的 API，实现设备查询、服务调用、自动化触发等操作。它帮助用户把日常的手工交互转化为可脚本化、可调度的工作流，从而提升智能家居管理的效率和可重复性。

**价值**  
- **消除重复手工**：所有常用的 Home Assistant 操作（比如获取实体状态、执行服务、管理配置）都可以通过一条 CLI 命令完成，避免在 UI 中逐层点击。  
- **支持可编排的流程**：CLI 完全兼容 Shell、cron、Ansible、GitHub Actions 等工具，便于把 Home Assistant 融入 CI/CD、监控或批量运维脚本中。  
- **提升可维护性**：将业务逻辑写在代码里后，可版本化、审计和回滚，降低因手动失误导致的故障风险。

**典型接入方式**  
1. **本地安装**：`pip install homeassistant-cli`，或通过 Docker 镜像直接运行。  
2. **环境配置**：在 `~/.homeassistant-cli` 或环境变量中配置 Home Assistant 的 URL、Long‑Lived Access Token（LLAT）等凭证。  
3. **脚本化使用**：在 Bash、PowerShell、Python 等脚本中调用 `hass`（或 `homeassistant-cli`) 命令，例如  
   ```bash
   # 获取灯光状态并在夜间自动关闭
   if hass --entity light.living_room --attribute state | grep -q on; then
       hass --service light.turn_off --entity light.living_room
   fi
   ```  
4. **任务调度**：配合 `cron`、`systemd timers` 或 CI 平台的定时任务，实现定期状态检查、备份或自动化触发。

**生产可用性**  
- **活跃度**：截至 2026‑05‑10，项目最近有提交，拥有 558 ⭐、83 🍴，说明社区活跃且持续维护。  
- **技术成熟度**：核心实现基于官方 Home Assistant REST API，使用官方推荐的 Long‑Lived Access Token，安全性与官方保持一致。  
- **语言与生态**：全 Python 实现，易于在任何支持 Python 的环境中部署；同时提供 Docker 镜像，适合容器化部署。  
- **风险**：目前未发现重大许可证或安全隐患，但在正式投入生产前仍建议完成一次内部安全审计，并确认维护者的响应速度符合业务 SLA。

综上，home‑assistant‑cli 已具备 **高可用性** 与 **易集成** 的特性，是在生产环境中实现 Home Assistant 自动化、批量运维和 DevOps 流水线的可靠工具。

## 🧭 Practical evaluation

**Value:** home-assistant-ecosystem/home-assistant-cli helps remove repetitive manual operations from a workflow.

**Best use cases**

- remove manual work
- connect tools into repeatable flows
- schedule operational tasks

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 558 GitHub stars
- 83 forks
- updated 2026-05-10
- primary language: Python
- 5 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 48/100 |
| stars | 58/100 |
| topics | 63/100 |
| outlook | 83/100 |
| quality | 74/100 |
| recency | 100/100 |
| adoption | 56/100 |
| production | 77/100 |
| usefulness | 90/100 |
| integration | 62/100 |
| sourceTrust | 100/100 |

---

<sub>🔭 Discovered 2026-05-10 · [View on GitHub](https://github.com/home-assistant-ecosystem/home-assistant-cli) · [← Back to Automation](./README.md)</sub>
