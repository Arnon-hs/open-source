# waycrate/wayshot

[![Stars](https://img.shields.io/github/stars/waycrate/wayshot?style=flat-square&color=yellow)](https://github.com/waycrate/wayshot/stargazers) [![Forks](https://img.shields.io/github/forks/waycrate/wayshot?style=flat-square&color=blue)](https://github.com/waycrate/wayshot/network) [![Language](https://img.shields.io/badge/lang-Rust-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-58%2F100-brightgreen?style=flat-square)](#)

> screenshot tool for wayland compositors.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 174 |
| 🍴 **Forks** | 49 |
| 💻 **Language** | Rust |
| 📈 **Score** | 58/100 |
| 🗓️ **Last push** | 2026-05-12 |
| 🔍 **Source** | github |

## 🏷️ Topics

`hyprland` `screenshot` `sway` `wayland`

## 🎯 Categories

Misc

## 📝 Summary

### English

**Brief Summary**  
Wayshot (waycrate/wayshot) is a lightweight, Rust‑based screenshot utility for Wayland compositors. With a modest but active community (174 ★, recent updates) it can capture full‑screen, region, or window shots and pipe the result to other tools, making it handy for developers and power users on Wayland desktops.

**Value**  
Wayshot fills the gap left by traditional X‑org screenshot tools that don’t work on Wayland. Because it is written in Rust, it offers strong safety guarantees, a small binary footprint, and easy extensibility through its command‑line interface, allowing teams to embed screen‑capture steps directly into CI pipelines, UI tests, or internal documentation workflows.

**Practical Adoption Path**  
1. **Proof‑of‑concept** – Clone the repo, build the binary (`cargo build --release`), and run a quick test (`wayshot -f png -o /tmp/test.png`). Verify that it works with the target compositor (e.g., Sway, River).  
2. **Readme validation** – Follow the usage examples in the README to confirm flag syntax and output piping (e.g., `wayshot -g | wl-copy`). Adjust any compositor‑specific configuration (e.g., DBus permissions).  
3. **Integration** – Wrap the binary in a small wrapper script or Docker image and replace any existing X‑org screenshot calls in your tooling.  
4. **Dependency audit** – Check the Rust crate dependencies for licensing and security updates; lock the version in `Cargo.lock` or use a pre‑built binary to simplify deployment.

**Production Readiness**  
Wayshot is **medium‑ready**: it is actively maintained (last commit 2026‑05‑12) and stable enough for prototypes or internal tooling, but it lacks formal release cycles, extensive documentation, and built‑in logging. Before production use, ensure:  

* The Wayland compositor in production is supported (test on the exact version).  
* All Rust dependencies are vetted and pinned to known‑good versions.  
* A fallback mechanism is in place (e.g., fallback to `grim` or `slurp`) in case of future breaking changes.  

With these checks, Wayshot can be safely introduced for internal workflows and gradually expanded to broader production scenarios.

### Русский

**waycrate/wayshot** — это лёгкий скриншот‑инструмент для Wayland‑композиторов, написанный на Rust, с более чем 170 звёздами на GitHub и активным обновлением (последний коммит — 12 мая 2026). Он подходит для прототипов и внутренних рабочих процессов, где требуется быстро захватывать экран без тяжёлых зависимостей; типичный сценарий внедрения — добавить небольшую proof‑of‑concept в CI/CD, проверить README и собрать бинарник, после чего оценить стабильность и необходимость дополнительных библиотек. Готовность к production — средняя: функциональность достаточна, но перед масштабным использованием следует протестировать совместимость с используемыми compositor‑ами и убедиться в поддержке долгосрочного обслуживания.

### 中文

**项目简介**  
Waycrate/wayshot 是一款基于 Rust 开发的 Wayland 截图工具，专为 Wayland 合成器（如 GNOME‑Shell、KDE‑Plasma、Sway 等）提供轻量、无依赖的屏幕捕获功能。它支持全屏、窗口、区域以及光标捕获，并可直接将截图保存为 PNG、JPEG 或复制到剪贴板。

**价值**  
- **原生 Wayland 支持**：绕过 XWayland，避免兼容性问题，截图更快、更稳定。  
- **可脚本化**：提供命令行界面，可在 CI、自动化文档生成或自定义快捷键中直接调用。  
- **轻量安全**：使用 Rust 编写，内存安全且二进制体积小，适合作为内部工具或原型快速集成。

**典型接入方式**  
1. **二进制直接使用**：在目标机器上 `cargo install wayshot` 或下载预编译的 Release 包，加入系统路径后即能通过 `wayshot -f png -o /tmp/screenshot.png` 等命令调用。  
2. **脚本/快捷键集成**：在 i3‑sway、Hyprland 等 compositor 的配置文件中绑定快捷键，例如  
   ```bash
   bindsym $mod+Print exec wayshot -r -c   # 选区截图并复制到剪贴板
   ```  
3. **CI/自动化**：在 CI 脚本中使用 `wayshot --output screenshot.png && curl -F file=@screenshot.png https://api.example.com/upload`，实现 UI 回归测试的截图上传。

**生产可用性**  
- **成熟度**：已有 174+ 星、49+ Fork，活跃维护至 2026‑05‑12，代码基于 Rust，具备较好的安全性和可维护性。  
- **准备度**：适合作为原型或内部工具使用；在生产环境部署前建议：  
  1. 验证目标 Wayland 合成器的兼容性（目前已在 Sway、GNOME、KDE 测试通过）。  
  2. 确认二进制或 Cargo 依赖的版本锁定，避免因 upstream 更新导致的破坏。  
  3. 编写简单的包装脚本或 systemd 服务，以统一错误处理和日志收集。  
- **风险**：项目文档相对简洁，集成路径主要依赖命令行参数，需要自行编写包装层；若对高级功能（如多显示器同步）有特殊需求，可能需要自行扩展或贡献代码。  

总体而言，wayshot 在 Wayland 环境下提供了可靠且易于脚本化的截图能力，适合作为内部工具或原型快速集成，经过少量验证即可投入生产使用。

## 🧭 Practical evaluation

**Value:** waycrate/wayshot may be useful when its README and activity match a concrete workflow.

**Best use cases**

- Not enough metadata yet.

**Integration notes:** Looks feasible to evaluate, but integration should start with a small proof of concept and README check.

**Production readiness:** Medium: useful for prototypes or internal workflows, with dependency and maintenance checks before production.

**Quality signals**

- 174 GitHub stars
- 49 forks
- updated 2026-05-12
- primary language: Rust
- 4 topics

**Risks:** Integration path is not obvious from metadata; validate setup cost before committing.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 42/100 |
| stars | 48/100 |
| topics | 50/100 |
| outlook | 73/100 |
| quality | 68/100 |
| recency | 100/100 |
| adoption | 46/100 |
| production | 70/100 |
| usefulness | 58/100 |
| integration | 30/100 |
| sourceTrust | 100/100 |

---

<sub>🔭 Discovered 2026-05-12 · [View on GitHub](https://github.com/waycrate/wayshot) · [← Back to Misc](./README.md)</sub>
