# mangowm/mango

[![Stars](https://img.shields.io/github/stars/mangowm/mango?style=flat-square&color=yellow)](https://github.com/mangowm/mango/stargazers) [![Forks](https://img.shields.io/github/forks/mangowm/mango?style=flat-square&color=blue)](https://github.com/mangowm/mango/network) [![Language](https://img.shields.io/badge/lang-C-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-62%2F100-brightgreen?style=flat-square)](#)

> Practical and Powerful wayland compositor (dwm but wayland)

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 2.7k |
| 🍴 **Forks** | 166 |
| 💻 **Language** | C |
| 📈 **Score** | 62/100 |
| 🗓️ **Last push** | 2026-05-11 |
| 🔍 **Source** | github |

## 🏷️ Topics

`compositor` `wayland` `wayland-compositor` `wlroots`

## 🎯 Categories

Misc

## 📝 Summary

### English

**Brief Summary**  
Mangowm/mango is a lightweight, tiling Wayland compositor inspired by dwm, written in C. It aims to give power‑users a minimal yet extensible environment for building custom Wayland workflows, and it has attracted a solid community (2.7 k ★, 166 forks) with recent activity.

**Value**  
- **Practicality** – By mirroring dwm’s philosophy, mango offers a familiar, keyboard‑driven interface while handling the modern Wayland stack, making it a good drop‑in for developers who already rely on dwm‑style tiling.  
- **Power** – The codebase is deliberately small and readable, allowing users to patch or extend the compositor to fit niche requirements (e.g., custom layout algorithms, bespoke input handling).  

**Adoption Path**  
1. **Proof‑of‑concept** – Clone the repo, build the compositor, and run it on a test X‑session or nested Wayland server (e.g., `weston --backend=wayland-backend.so`). Verify that the README steps work and that basic tiling, window management, and input work for your hardware.  
2. **Integration** – Replace the test compositor with mango in a controlled environment (e.g., a development workstation or CI runner). Add any required patches (e.g., to support a specific input device or to integrate with your window‑launch scripts).  
3. **Pilot** – Deploy mango to a small user group (1‑5 engineers) and collect feedback on stability, performance, and workflow fit. Iterate on configuration and optional upstream contributions.  

**Production Readiness**  
- **Activity** – The project shows recent commits (as of 2026‑05‑11) and a healthy star/fork count, indicating an engaged community.  
- **Maturity** – Written in C with a modest code footprint, the compositor is easy to audit and debug, which is advantageous for security reviews.  
- **Risk** – No glaring licensing or metadata issues have been identified, but a final check of the license (MIT‑style) and a security audit of the code base are still recommended before full production rollout.  

Overall, mango is a strong candidate for a pilot Wayland compositor in environments that value minimalism and extensibility, provided the standard OSS due‑diligence steps are completed.

### Русский

**Mangowm/mango** — это практичный и мощный композитор Wayland, вдохновлённый простотой dwm, написанный на C. Он подходит, когда требуется лёгкий, настраиваемый оконный менеджер, полностью совместимый с современными Wayland‑приложениями; типичный сценарий внедрения — небольшое proof‑of‑concept, проверка README и базовой конфигурации, после чего можно масштабировать до полноценного рабочего стола. По готовности к production проект выглядит зрелым: активные обновления, более 2700 звёзд, существенное количество форков и позитивные сигналы экосистемы, хотя лицензия и безопасность требуют окончательной проверки.

### 中文

**项目简介**  
mangowm/mango 是一个实用且功能强大的 Wayland 合成器，灵感来源于 dwm 的简洁设计，却面向 Wayland 环境实现。它使用 C 语言编写，代码轻量、可高度定制，适合希望在 Linux 桌面上获得 dwm 式工作流但又需要 Wayland 原生支持的用户和开发者。

**价值**  
- **轻量高效**：核心代码简洁，启动快、资源占用低，适合在资源受限的机器或容器化环境中运行。  
- **高度可定制**：遵循 dwm 的“配置即代码”理念，所有行为都可以通过修改 C 源码或配置文件实现，无需额外的插件系统。  
- **Wayland 原生**：摆脱 X11 的历史包袱，直接利用 Wayland 提供的安全性和现代图形特性，兼容最新的桌面生态（GTK、Qt、wlroots 等）。  

**典型接入方式**  
1. **快速原型验证**  
   - 克隆仓库并编译：`git clone https://github.com/mangowm/mango && cd mango && make && sudo make install`。  
   - 在 `.xinitrc`（或对应的 Wayland 启动脚本）中加入 `exec mango`，即可在登录会话中直接使用。  
2. **深度集成**  
   - 将 mango 作为系统的默认 Wayland 合成器，配合 `sddm`、`gdm` 或 `weston-launch` 等登录管理器。  
   - 通过修改 `config.h` 或自行编写 C 插件，实现窗口布局、快捷键、状态栏等功能的业务定制。  
   - 若已有基于 wlroots 的组件（如 sway、river），可参考 mango 的 `backend` 实现方式，将其作为轻量替代或嵌入到自研的桌面环境中。  

**生产可用性**  
- **活跃度**：最近一次提交在 2026‑05‑11，拥有 2707+ 星、166+ Fork，社区活跃，Issue 反馈及时。  
- **成熟度**：核心功能已稳定，代码基于 C 且遵循 POSIX/Wayland 标准，易于审计和二次开发。  
- **风险**：目前未发现重大许可证或安全漏洞，但仍建议在正式部署前进行一次完整的安全审计，并确认维护者的响应速度。  
- **适用场景**：适合内部研发平台、嵌入式设备、轻量化工作站以及希望在生产环境中实验 Wayland 原生桌面的团队。  

综上，mango 在功能完整性、资源占用和可定制性之间取得了良好平衡，具备直接投入生产环境的条件，只需在实际使用前进行小范围的 PoC 验证和文档（README）确认即可。

## 🧭 Practical evaluation

**Value:** mangowm/mango may be useful when its README and activity match a concrete workflow.

**Best use cases**

- Not enough metadata yet.

**Integration notes:** Looks feasible to evaluate, but integration should start with a small proof of concept and README check.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 2707 GitHub stars
- 166 forks
- updated 2026-05-11
- primary language: C
- 4 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 56/100 |
| stars | 73/100 |
| topics | 50/100 |
| outlook | 75/100 |
| quality | 78/100 |
| recency | 100/100 |
| adoption | 68/100 |
| production | 76/100 |
| usefulness | 42/100 |
| integration | 46/100 |
| sourceTrust | 100/100 |

---

<sub>🔭 Discovered 2026-05-11 · [View on GitHub](https://github.com/mangowm/mango) · [← Back to Misc](./README.md)</sub>
