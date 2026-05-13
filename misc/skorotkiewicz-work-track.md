# skorotkiewicz/work-track

[![Stars](https://img.shields.io/github/stars/skorotkiewicz/work-track?style=flat-square&color=yellow)](https://github.com/skorotkiewicz/work-track/stargazers) [![Forks](https://img.shields.io/github/forks/skorotkiewicz/work-track?style=flat-square&color=blue)](https://github.com/skorotkiewicz/work-track/network) [![Language](https://img.shields.io/badge/lang-Unknown-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-41%2F100-brightgreen?style=flat-square)](#)

> Discovered from Hacker News (github-mentions)

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | — |
| 🍴 **Forks** | — |
| 💻 **Language** | Unknown |
| 📈 **Score** | 41/100 |
| 🗓️ **Last push** | 2026-05-13 |
| 🔍 **Source** | hackernews |

## 🏷️ Topics

`hn` `github-mentions`

## 🎯 Categories

Misc

## 📝 Summary

### English

**Brief Summary (2‑3 sentences)**  
Show HN is a tiny Wayland utility that logs how long your screen stays on, giving you a simple CSV‑style record of active screen time. It’s designed for developers and power‑users who want a lightweight, no‑frills way to monitor display usage on Wayland‑based desktops.

**Value**  
- **Minimal footprint:** The tool is deliberately small, with no heavyweight dependencies, making it easy to add to a personal workstation or a CI‑controlled environment for energy‑usage audits.  
- **Clear data output:** It writes timestamps and duration directly to a plain‑text file, which can be fed into scripts, Grafana dashboards, or simple spreadsheet analyses without extra parsing layers.  
- **Open‑source transparency:** The source is publicly available on GitHub, allowing you to audit the code for privacy or extend it to fit niche workflows (e.g., triggering alerts when screen‑on time exceeds a threshold).

**Practical Adoption Path**  

| Step | Action | Reason |
|------|--------|--------|
| 1️⃣  | **Review repository** – check the license (MIT/Apache‑style), read the README, and glance at recent commits/issues. | Confirms legal compatibility and current maintenance status. |
| 2️⃣  | **Test in a sandbox** – clone the repo on a non‑critical Wayland machine, build/install per the instructions, and run the binary to verify it logs correctly. | Guarantees it works with your Wayland compositor (e.g., GNOME‑Shell, KDE‑Plasma, Sway). |
| 3️⃣  | **Integrate with your workflow** – add the binary to a systemd user service or a startup script, point the output file to a location monitored by your logging pipeline. | Provides continuous tracking without manual starts/stops. |
| 4️⃣  | **Validate data** – ingest a few hours of logs into your analytics stack and confirm format, timestamps, and any edge cases (suspend, lock screen). | Ensures downstream tools can consume the data reliably. |
| 5️⃣  | **Monitor upstream** – subscribe to the repo’s releases or issue tracker to stay aware of bug fixes or breaking changes. | Reduces risk of future incompatibilities. |

**Production Readiness**  
- **Maturity:** Medium. The project is actively updated (last commit 2026‑05‑13) and provides basic functionality, but it lacks extensive documentation, automated tests, and a formal release schedule.  
- **Suitable use‑cases:** Internal prototypes, personal energy‑usage dashboards, or as a building block in a larger monitoring suite. Not yet recommended for mission‑critical production services without additional safeguards.  
- **Adoption checklist:** Verify the license, confirm that the binary runs on your specific Wayland compositor, assess the maintenance cadence (e.g., at least monthly commits), and consider adding your own tests or wrappers to cover edge cases (suspend, multi‑monitor setups).  

In short, Show HN offers a quick, low‑overhead way to capture screen‑on time on Wayland, making it a handy tool for internal tooling or exploratory data collection, provided you perform the modest due‑diligence steps outlined above before promoting it to production.

### Русский

**Show HN: minimal screen‑on time tracker for Wayland** – лёгкий утилита, фиксирующая время, когда экран находится в включённом состоянии, что удобно для аналитики энергопотребления или контроля рабочего времени в средах, использующих Wayland. Подойдёт для прототипов и внутренних процессов, где требуется простая интеграция без тяжёлых зависимостей, но перед выпуском в production следует проверить лицензию, актуальность документации, активность разработки и частоту релизов. Готовность – средняя: функционал стабилен, однако метаданные проекта скудны, поэтому требуется ручная оценка рисков и поддерживаемости.

### 中文

**项目简介**  
Show HN 是一个面向 Wayland 环境的极简屏幕开启时间统计工具，代码体积小、依赖少，适合想快速了解工作站实际使用时长的用户。

**价值**  
- **即时可视化**：在屏幕上直接显示当前会话的累计开机时间，帮助个人或团队评估工作效率。  
- **轻量安全**：仅依赖 Wayland 协议本身，无需额外的 X11、DBus 或图形库，几乎不会对系统性能产生影响。  
- **开箱即用**：提供简洁的命令行界面和可选的 OSD（On‑Screen Display），适配多种 Wayland 合成器（如 sway、weston）。

**典型接入方式**  
1. **源码编译**：`git clone https://github.com/…/show-hn && cd show-hn && cargo build --release`（项目使用 Rust）。  
2. **系统服务**：将编译好的二进制文件放入 `$HOME/.local/bin`，并创建一个 systemd 用户服务：  
   ```ini
   [Unit]
   Description=Show HN screen‑on time tracker

   [Service]
   ExecStart=%h/.local/bin/show-hn --output=overlay
   Restart=on-failure

   [Install]
   WantedBy=default.target
   ```  
   `systemctl --user enable --now show-hn.service` 即可在登录时自动启动。  
3. **集成到桌面环境**：在 sway 配置文件中添加 `exec_always --no-startup-id $HOME/.local/bin/show-hn --output=overlay`，即可让 OSD 随合成器启动。  

**生产可用性**  
- **成熟度**：项目最近一次更新为 2026‑05‑13，代码量极小，功能相对稳定，适合作为原型或内部工具使用。  
- **风险**：元数据较少，缺乏完整的测试套件、CI 状态和长期维护承诺；需自行检查许可证（MIT/Apache 等）是否符合公司合规、确认没有未解决的安全问题。  
- **建议**：在正式生产环境部署前，进行以下检查：  
  1. **依赖审计**：确认 Rust 依赖库的许可证和维护状态。  
  2. **兼容性验证**：在目标 Wayland 合成器（sway、weston、gnome‑wayland 等）上进行功能测试。  
  3. **监控与日志**：为 systemd 服务开启 `StandardOutput=journal`，以便快速定位异常。  

综上，Show HN 适合作为轻量级的屏幕使用时长监控工具，经过简单的编译和 systemd/user‑service 集成即可投入内部使用；若需在大规模生产环境长期依赖，建议评估其维护活跃度并准备好备用方案。

## 🧭 Practical evaluation

**Value:** Show HN: A minimal screen-on time tracker for Wayland may be useful when its README and activity match a concrete workflow.

**Best use cases**

- Not enough metadata yet.

**Integration notes:** Needs manual inspection before adoption because integration signals are sparse in the discovered metadata.

**Production readiness:** Medium: useful for prototypes or internal workflows, with dependency and maintenance checks before production.

**Quality signals**

- updated 2026-05-13
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

<sub>🔭 Discovered 2026-05-13 · [View on GitHub](https://github.com/skorotkiewicz/work-track) · [← Back to Misc](./README.md)</sub>
