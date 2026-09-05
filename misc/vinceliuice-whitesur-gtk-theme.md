# vinceliuice/WhiteSur-gtk-theme

[![Stars](https://img.shields.io/github/stars/vinceliuice/WhiteSur-gtk-theme?style=flat-square&color=yellow)](https://github.com/vinceliuice/WhiteSur-gtk-theme/stargazers) [![Forks](https://img.shields.io/github/forks/vinceliuice/WhiteSur-gtk-theme?style=flat-square&color=blue)](https://github.com/vinceliuice/WhiteSur-gtk-theme/network) [![Language](https://img.shields.io/badge/lang-CSS-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-60%2F100-brightgreen?style=flat-square)](#)

> MacOS like theme for all gtk based desktops

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 9.1k |
| 🍴 **Forks** | 734 |
| 💻 **Language** | CSS |
| 📈 **Score** | 60/100 |
| 🗓️ **Last push** | 2026-09-05 |
| 🔍 **Source** | github |

## 🏷️ Topics

`gnome` `gtk` `gtk-theme` `gtk3` `gtk4` `macos`

## 🎯 Categories

Misc

## 📝 Summary

### English

**Summary:** WhiteSur-gtk-theme is an open-source project that provides a MacOS-like theme for all gtk-based desktops, allowing developers to build user-friendly interfaces with minimal custom UI work. This theme offers a faster and more efficient way to create product UI, enabling the reuse of interface components and improved frontend delivery. With a strong ecosystem and recent activity, WhiteSur-gtk-theme is production-ready for serious pilots.

**Value:** The primary value proposition of WhiteSur-gtk-theme lies in its ability to help developers ship user-facing interfaces with less custom UI work. This theme enables faster product UI development, reusability of interface components, and improved frontend delivery, ultimately reducing the time and effort required to create high-quality user interfaces.

**Practical Adoption Path:** To adopt WhiteSur-gtk-theme, start by evaluating its feasibility through a small proof of concept and checking the README documentation. This will help determine the integration path and validate the setup cost before committing to a full implementation. With a strong GitHub presence (9056 stars, 734 forks), recent activity, and a well-maintained ecosystem, WhiteSur-gtk-theme is an attractive option for serious pilots.

**Production Readiness:** WhiteSur-gtk-theme is considered production-ready due to its recent activity, strong adoption (905

### Русский

**WhiteSur‑gtk‑theme** — это открытая CSS‑тема, имитирующая внешний вид macOS и совместимая со всеми GTK‑десктопами. Она позволяет быстро оформить пользовательский интерфейс, переиспользуя готовый набор стилей, что ускоряет вывод продукта на рынок и снижает объём кастомной UI‑работы; типичный путь внедрения — установить тему в небольшом прототипе, проверить её работу через README и затем масштабировать на остальные компоненты. Проект имеет высокую готовность к продакшену: активные коммиты, более 9 тыс. звёзд, сотни форков и широкое сообщество, что делает его надёжным кандидатом для пилотного внедрения.

### 中文

**价值**  
- **快速交付 UI**：WhiteSur‑gtk‑theme 为所有基于 GTK 的桌面环境提供了完整的 macOS 风格外观，开发者无需自行编写大量 CSS/GTK 样式，即可让应用拥有现代、统一且美观的界面。  
- **复用与一致性**：通过统一的主题文件，团队可以在多个项目之间共享同一套视觉规范，降低 UI 设计和实现的维护成本。  
- **提升用户体验**：macOS 的视觉语言在业界广受好评，使用该主题可以让 Linux/Unix 用户获得熟悉且高质量的使用感受，从而提升产品的整体满意度。

**典型接入方式**  
1. **克隆或下载**：`git clone https://github.com/vinceliuice/WhiteSur-gtk-theme.git`，或直接下载发行版压缩包。  
2. **安装主题**  
   - 对于单用户：运行 `./install.sh`（会把主题文件复制到 `~/.themes`），或手动将 `WhiteSur` 目录拷贝到 `~/.themes`。  
   - 对于全局使用：以 root 权限执行 `./install.sh --tint=dark --dest=/usr/share/themes`。  
3. **在桌面环境中启用**：打开 GNOME‑Tweaks、KDE‑System‑Settings、XFCE‑Appearance 等对应的外观设置，选择 “WhiteSur” 主题（可选暗/亮配色、圆角大小等参数）。  
4. **在 CI / Docker 环境中验证**：在容器或 CI 脚本里执行 `install.sh --dest=/usr/share/themes && gsettings set org.gnome.desktop.interface gtk-theme "WhiteSur"`，随后运行 UI 测试即可确认主题渲染是否符合预期。  
5. **自定义**：如需微调颜色或圆角，可编辑 `src/gtk-3.0/gtk.css`、`src/gtk-4.0/gtk.css`，或使用 `--color`、`--radius` 参数重新生成主题。

**生产可用性**  
- **活跃度**：截至 2026‑07‑05，项目仍在持续更新，最近一次提交仅几天前；拥有 9 000+ ⭐、700+ fork，社区活跃度高。  
- **成熟度**：主题已在多个主流发行版（Ubuntu、Fedora、Arch）以及多种桌面环境（GNOME、Cinnamon、MATE、XFCE）中得到实际使用，兼容性经过广泛验证。  
- **风险控制**：唯一需要关注的是安装脚本对不同发行版的路径假设（`/usr/share/themes` vs `~/.themes`），在正式上线前建议在目标平台做一次完整的 POC，确认依赖的 GTK 版本（≥3.24、≥4.0）与主题匹配。  

**结论**：WhiteSur‑gtk‑theme 已具备高生产就绪度，适合作为 macOS 风格 UI 的快速底层实现。建议先在内部的 UI 自动化测试环境中完成小规模验证，确认主题在目标 GTK 版本和桌面环境下的表现后，即可在正式产品中推广使用。

## 🧭 Practical evaluation

**Value:** vinceliuice/WhiteSur-gtk-theme helps ship user-facing interfaces with less custom UI work.

**Best use cases**

- build product UI faster
- reuse interface components
- improve frontend delivery

**Integration notes:** Looks feasible to evaluate, but integration should start with a small proof of concept and README check.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 9056 GitHub stars
- 734 forks
- updated 2026-07-05
- primary language: CSS
- 6 topics

**Risks:** Integration path is not obvious from metadata; validate setup cost before committing.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 72/100 |
| stars | 84/100 |
| topics | 75/100 |
| outlook | 74/100 |
| quality | 83/100 |
| recency | 80/100 |
| adoption | 81/100 |
| production | 70/100 |
| usefulness | 42/100 |
| integration | 30/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 0/100 |

---

<sub>🔭 Discovered 2026-07-05 · [View on GitHub](https://github.com/vinceliuice/WhiteSur-gtk-theme) · [← Back to Misc](./README.md)</sub>
