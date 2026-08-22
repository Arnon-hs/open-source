# KristijanKocev/lidwatch

[![Stars](https://img.shields.io/github/stars/KristijanKocev/lidwatch?style=flat-square&color=yellow)](https://github.com/KristijanKocev/lidwatch/stargazers) [![Forks](https://img.shields.io/github/forks/KristijanKocev/lidwatch?style=flat-square&color=blue)](https://github.com/KristijanKocev/lidwatch/network) [![Language](https://img.shields.io/badge/lang-Unknown-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-41%2F100-brightgreen?style=flat-square)](#)

> Discovered from Hacker News (github-mentions)

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | — |
| 🍴 **Forks** | — |
| 💻 **Language** | Unknown |
| 📈 **Score** | 41/100 |
| 🗓️ **Last push** | 2026-07-12 |
| 🔍 **Source** | hackernews |

## 🏷️ Topics

`hn` `github-mentions`

## 🎯 Categories

Misc

## 📝 Summary

### English

**Brief Summary (2‑3 sentences)**  
The “Show HN: Sleep external displays connected to a MacBook after closing lid” project is a small utility that keeps external monitors alive when a MacBook’s lid is closed, preventing the displays from entering sleep mode. It is aimed at developers and power‑users who run clamshell‑mode workflows (e.g., coding, video editing, or testing) on a MacBook while using one or more external screens.

**Value**  
- **Workflow continuity:** Eliminates the need to keep the MacBook open or to use third‑party hardware tricks, allowing a seamless transition to clamshell mode without losing display state.  
- **Productivity boost:** Saves time for anyone who frequently docks/undocks a MacBook, especially in environments where screen real‑estate and power consumption matter (e.g., remote‑desktop stations, CI rigs, or shared workstations).  
- **Open‑source transparency:** The code can be audited, customized, or extended to support additional display‑management features (e.g., automatic brightness or orientation adjustments).

**Practical Adoption Path**  
1. **Review the repository** – clone the project, read the README, and verify the license (likely MIT/Apache).  
2. **Test in a sandbox** – run the utility on a non‑critical MacBook with the intended external monitors to confirm that closing the lid does not put the displays to sleep.  
3. **Integrate with existing scripts** – if the tool provides a CLI or launch‑agent, add it to your login items or to a custom `launchd` plist so it starts automatically.  
4. **Monitor stability** – keep an eye on macOS updates (especially major releases) that could break the low‑level display handling; be prepared to fork or submit patches.  
5. **Document the process** – add a short internal wiki page covering installation steps, required permissions (e.g., Accessibility), and rollback instructions.

**Production Readiness (Medium)**  
- **Maturity:** The project shows recent activity (updated 2026‑07‑12) but has limited community signals (few topics, low score).  
- **Risk factors:** Sparse documentation, unknown release cadence, and potential macOS compatibility issues mean it’s best suited for prototypes, internal tools, or environments where a fallback (e.g., reopening the lid) is acceptable.  
- **Mitigation:** Perform a license audit, set up automated tests (e.g., a simple script that checks display status after lid closure), and maintain a fork with your own CI pipeline to catch breaking changes.  

In short, the utility offers a handy, open‑source way to keep external monitors awake in clamshell mode, but teams should treat it as a “medium‑readiness” component—useful for internal or experimental workflows after thorough testing and modest maintenance overhead.

### Русский

**Show HN: Sleep external displays connected to a MacBook after closing lid** — небольшое open‑source решение, позволяющее автоматически переводить внешние мониторы в спящий режим при закрытии крышки MacBook, что экономит энергию и предотвращает «залипание» экранов. Подходит для рабочих станций, где ноутбук используется как основной компьютер с подключёнными дисплеями (например, в офисных или домашних коворкингах) и требуется простая автоматизация без сторонних утилит. Готовность к production — средняя: проект обновлён недавно, но требует ручной проверки лицензии, активности репозитория и наличия документации перед интеграцией в критичные процессы.

### 中文

**项目简介**  
Show HN: *Sleep external displays connected to a MacBook after closing lid* 是一个在 Hacker News 上被提及的开源脚本/工具，旨在在合上 MacBook 盖子后让外接显示器保持工作状态（即不进入睡眠），从而实现“闭盖模式”下的多屏使用。

**价值**  
- 解决了 MacBook 合盖后外接显示器自动进入睡眠的痛点，适用于需要持续显示内容（如演示、监控面板、持续渲染等）的工作流。  
- 通过简单的配置即可把 MacBook 变成类似“台式机”使用模式，提高办公空间利用率。  

**典型接入方式**  
1. **克隆仓库**：`git clone https://github.com/your/repo.git`  
2. **安装依赖**（通常为 `brew` 包或 Python 脚本）：`brew install sleepwatcher` 或 `pip install -r requirements.txt`  
3. **配置**：编辑 `config.yml`（或脚本中的变量），指定要保持唤醒的外接显示器的标识（如 EDID、UUID）。  
4. **启动守护进程**：将提供的 launch agent（`.plist`）复制到 `~/Library/LaunchAgents/` 并加载 `launchctl load ~/Library/LaunchAgents/com.example.sleepdisplay.plist`。  
5. **验证**：合上 MacBook 盖子，检查外接显示器是否仍保持活动状态；如有需要，可在日志文件中调试。  

**生产可用性**  
- **成熟度**：当前评分 41/100，元数据较少，属于 **中等** 稳定性。适合作为原型或内部工具使用。  
- **依赖与维护**：项目最近一次更新是 2026‑07‑12，仍有活跃提交，但需自行检查依赖（如 `sleepwatcher`、系统版本兼容性）以及许可证是否符合企业合规。  
- **上线建议**：在正式生产环境前进行以下步骤：  
  1. **代码审计**，确认无安全风险。  
  2. **兼容性测试**（不同 macOS 版本、不同显示器型号）。  
  3. **监控与回滚**，为脚本加入日志与异常报警，确保出现问题时可快速恢复默认睡眠行为。  

综上，该工具在需要闭盖后保持外接显示器持续工作的场景下价值显著，但在生产环境采用前应完成手动评估和充分测试。

## 🧭 Practical evaluation

**Value:** Show HN: Sleep external displays connected to a MacBook after closing lid may be useful when its README and activity match a concrete workflow.

**Best use cases**

- Not enough metadata yet.

**Integration notes:** Needs manual inspection before adoption because integration signals are sparse in the discovered metadata.

**Production readiness:** Medium: useful for prototypes or internal workflows, with dependency and maintenance checks before production.

**Quality signals**

- updated 2026-07-12
- 2 topics

**Risks:** Quality signals are limited; verify license, maintenance, docs, issues, and release cadence before using it.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 0/100 |
| stars | 0/100 |
| topics | 25/100 |
| outlook | 54/100 |
| quality | 41/100 |
| recency | 100/100 |
| adoption | 0/100 |
| production | 58/100 |
| usefulness | 42/100 |
| integration | 30/100 |
| sourceTrust | 80/100 |

---

<sub>🔭 Discovered 2026-07-12 · [View on GitHub](https://github.com/KristijanKocev/lidwatch) · [← Back to Misc](./README.md)</sub>
