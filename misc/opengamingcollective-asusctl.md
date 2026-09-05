# OpenGamingCollective/asusctl

[![Stars](https://img.shields.io/github/stars/OpenGamingCollective/asusctl?style=flat-square&color=yellow)](https://github.com/OpenGamingCollective/asusctl/stargazers) [![Forks](https://img.shields.io/github/forks/OpenGamingCollective/asusctl?style=flat-square&color=blue)](https://github.com/OpenGamingCollective/asusctl/network) [![Language](https://img.shields.io/badge/lang-Rust-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-57%2F100-brightgreen?style=flat-square)](#)

> Daemon and tools to control your ASUS ROG laptop. Supersedes rog-core.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 431 |
| 🍴 **Forks** | 58 |
| 💻 **Language** | Rust |
| 📈 **Score** | 57/100 |
| 🗓️ **Last push** | 2026-09-05 |
| 🔍 **Source** | github |

## 🏷️ Topics

`anime-matrix` `asus` `aura` `rog` `rog-core`

## 🎯 Categories

Misc

## 📝 Summary

### English

**Brief Summary (2‑3 sentences)**  
`asusctl` is an open‑source Rust daemon and accompanying CLI tools that let you manage power profiles, fan curves, keyboard backlighting, and other hardware features on ASUS ROG laptops, replacing the older `rog‑core` project. It is actively maintained (last commit 2026‑07‑12) and has attracted a modest community (≈ 430 ⭐, 58 forks). The project is positioned as a generic, scriptable alternative to vendor‑provided utilities, making it attractive for developers who need programmatic control over ROG hardware.

---

### Value Proposition
- **Programmatic hardware control** – Exposes a clean D‑Bus/CLI API for toggling GPU modes, fan speeds, and RGB lighting, enabling automation, custom scripts, or integration into larger system‑management tools.  
- **Rust implementation** – Offers safety, performance, and easy cross‑compilation, which is appealing for teams that already use Rust or prefer a compiled binary with minimal runtime dependencies.  
- **Supersedes `rog‑core`** – Consolidates previous fragmented tooling into a single daemon, reducing the maintenance burden for users who previously had to juggle multiple scripts.

### Practical Adoption Path
1. **Proof‑of‑concept** – Clone the repo, build the daemon (`cargo build --release`), and run it on a test ROG laptop. Verify that the README’s quick‑start steps (installing the systemd service, checking `asusctl -h`) work out‑of‑the‑box.  
2. **Integration prototype** – Wrap the CLI calls (`asusctl fan curve …`, `asusctl power‑profile …`) in a small wrapper script or a Python subprocess call to confirm that your workflow can drive the hardware as needed.  
3. **CI validation** – Add a lightweight health‑check job to your CI pipeline that starts the daemon in a container (or VM with GPU passthrough) and runs a couple of commands, ensuring future updates don’t break the API.  
4. **Documentation audit** – Review the README and generated `man` pages; if gaps exist, contribute a minimal usage guide for your internal team to reduce onboarding friction.

### Production Readiness
- **Maturity**: Medium. The project is actively updated and has a reasonable star count, but the ecosystem around it (e.g., packaging, extensive docs) is still thin.  
- **Stability**: The core daemon appears stable on the hardware it targets, but you should perform regression testing whenever a new release lands, especially after kernel upgrades.  
- **Dependencies & Maintenance**: Primary dependency is the Rust toolchain; the binary has no heavy runtime dependencies, making deployment straightforward. However, you’ll need to monitor upstream changes for compatibility with newer ASUS firmware or Linux kernel versions.  
- **Risk Mitigation**: Because the integration path isn’t fully documented, allocate time for a small pilot (as outlined above) and keep a fallback to the vendor’s official utilities in case of edge‑case failures.

**Bottom line:** `asusctl` is a solid choice for internal prototypes or tooling that requires scripted control of ASUS ROG laptops. With a brief pilot to validate the daemon’s API and a modest amount of monitoring, it can be promoted to production for internal workflows, though you should retain a contingency plan for any edge‑case hardware issues.

### Русский

OpenGamingCollective/asusctl — это набор демона и утилит на Rust для управления функциями ноутбуков ASUS ROG (питание, вентиляция, подсветка и пр.), пришедший на смену устаревшему rog‑core. Проект уже имеет более 400 звёзд и активную поддержку (обновления до 2026‑07‑12), поэтому его можно быстро протестировать в небольшом прототипе — например, добавить скрипт включения «TurboMode» в CI‑pipeline или автоматизировать переключение профилей в тестовой лаборатории. Готовность к production оценивается как средняя: функциональность стабильно работает, но требуется проверка зависимостей, настройка демона и оценка нагрузки перед использованием в критически важных системах.

### 中文

**价值**  
OpenGamingCollective/asusctl 为 ASUS ROG 系列笔记本提供了统一的守护进程和命令行工具，能够在 Linux 下完整控制风扇、键盘灯效、功耗模式等硬件特性。相较于旧的 `rog‑core`，它使用 Rust 编写，代码更安全、性能更好，并且已经集成了最新的 EC 接口，适合需要深度调教散热和游戏性能的开发者或内部运维团队。

**典型接入方式**  

| 步骤 | 说明 |
|------|------|
| 1. 环境准备 | 确保系统为支持的 Linux 发行版（Ubuntu 22.04、Fedora 38 等），内核 ≥ 6.5，已安装 `systemd`。 |
| 2. 安装 | 通过官方提供的 AUR / Debian 包或直接 `cargo install asusctl` 编译安装守护进程 `asusd`，并使用 `systemctl enable --now asusd` 启动。 |
| 3. 验证 | 执行 `asusctl status` 检查硬件检测是否正常，使用 `asusctl fan --set 60`、`asusctl keyboard --mode static --color ff0000` 等命令进行功能验证。 |
| 4. 集成 | 在 CI/CD 或内部脚本中调用 `asusctl` CLI（例如在游戏启动前调高风扇、在空闲时切换至低功耗模式），或通过 D‑Bus 与自研的监控服务交互。 |
| 5. 监控 & 日志 | `journalctl -u asusd` 记录守护进程日志，结合 Prometheus exporter（社区已有实现）实现可观测性。 |

**生产可用性**  

- **成熟度**：已有 430+ Stars、58 Forks，最近一次提交在 2026‑07‑12，活跃度良好。  
- **稳定性**：守护进程采用 systemd 管理，默认提供 `restart` 策略，异常时可自动恢复。  
- **风险**：项目文档主要集中在 README，完整的 API/DBus 文档相对薄弱；在非官方硬件（如非 ROG 系列）上可能出现兼容性问题，需要先做硬件检测。  
- **适用场景**：内部研发平台、游戏服务器的性能基准测试、或公司内部的笔记本统一管理。对于对可靠性要求极高的面向客户的生产系统，建议在正式部署前完成一次完整的功能验证（包括风扇曲线、键盘灯效的回滚测试）并制定监控/回滚方案。  

综上，asusctl 已具备在内部原型或受控生产环境中使用的条件，只要做好前期的硬件兼容性验证和监控体系，即可安全接入。

## 🧭 Practical evaluation

**Value:** OpenGamingCollective/asusctl may be useful when its README and activity match a concrete workflow.

**Best use cases**

- Not enough metadata yet.

**Integration notes:** Looks feasible to evaluate, but integration should start with a small proof of concept and README check.

**Production readiness:** Medium: useful for prototypes or internal workflows, with dependency and maintenance checks before production.

**Quality signals**

- 431 GitHub stars
- 58 forks
- updated 2026-07-12
- primary language: Rust
- 5 topics

**Risks:** Integration path is not obvious from metadata; validate setup cost before committing.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 44/100 |
| stars | 56/100 |
| topics | 63/100 |
| outlook | 69/100 |
| quality | 68/100 |
| recency | 80/100 |
| adoption | 53/100 |
| production | 65/100 |
| usefulness | 58/100 |
| integration | 30/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 0/100 |

---

<sub>🔭 Discovered 2026-07-12 · [View on GitHub](https://github.com/OpenGamingCollective/asusctl) · [← Back to Misc](./README.md)</sub>
