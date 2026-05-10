# stumpwm/mahogany

[![Stars](https://img.shields.io/github/stars/stumpwm/mahogany?style=flat-square&color=yellow)](https://github.com/stumpwm/mahogany/stargazers) [![Forks](https://img.shields.io/github/forks/stumpwm/mahogany?style=flat-square&color=blue)](https://github.com/stumpwm/mahogany/network) [![Language](https://img.shields.io/badge/lang-Common%20Lisp-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-52%2F100-brightgreen?style=flat-square)](#)

> A stumpwm like Wayland compositor

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 355 |
| 🍴 **Forks** | 34 |
| 💻 **Language** | Common Lisp |
| 📈 **Score** | 52/100 |
| 🗓️ **Last push** | 2026-05-10 |
| 🔍 **Source** | github |

## 🏷️ Topics

_no topics_

## 🎯 Categories

Misc

## 📝 Summary

### English

**Brief summary (2‑3 sentences)**  
Mahogany is an experimental Wayland compositor written in Common Lisp that mimics the tiling‑window‑manager experience of StumpWM. It targets users who already enjoy StumpWM’s keyboard‑driven workflow and want a similar environment on modern Wayland systems. The project is actively maintained (last commit 2026‑05‑10) and has attracted modest community interest (≈ 355 stars).

**Value proposition**  
- **Familiar workflow**: Developers and power‑users who have built a StumpWM‑centric workflow can transition to Wayland without relearning window‑management concepts.  
- **Lisp‑centric extensibility**: Because the compositor is written in Common Lisp, it can be customized and extended using the same language and idioms that StumpWM users already employ.  
- **Lightweight prototype platform**: Its minimal feature set makes it a good sandbox for experimenting with new tiling concepts or Wayland integrations before committing to a larger compositor.

**Practical adoption path**  
1. **Evaluate the README and source** – Verify that the documented configuration model aligns with your existing StumpWM setup.  
2. **Build & test in an isolated environment** – Clone the repo, compile with SBCL (or your preferred Lisp implementation), and run Mahogany on a dedicated Wayland session (e.g., via `weston` or a nested compositor).  
3. **Port your StumpWM config** – Translate keybindings, hooks, and custom scripts into Mahogany’s configuration DSL; this may require modest Lisp refactoring.  
4. **Integrate with your stack** – Add Mahogany to your system’s session manager (e.g., a systemd service or `~/.xinitrc`‑style script) and validate interaction with essential applications (terminal, editor, browser).  
5. **Iterate and document** – Record any missing features or bugs; consider contributing patches upstream if they are broadly useful.

**Production readiness**  
- **Maturity**: Medium. The project is actively updated and has a reasonable star count, but the ecosystem is small and documentation is sparse.  
- **Risk**: Integration signals are limited; you’ll need to manually verify dependency compatibility (SBCL version, Wayland libraries) and assess maintenance commitments.  
- **Recommended use**: Suitable for internal tools, prototypes, or personal workstations where the benefits of a StumpWM‑style Wayland compositor outweigh the overhead of a custom setup. For critical production environments, perform a thorough stability and security audit, and be prepared to maintain a fork or contribute fixes as needed.

### Русский

**stumpwm/mahogany** — это Wayland‑композитор, написанный на Common Lisp и стилизованный под оконный менеджер StumpWM. Он подходит для быстрой прототипизации или внутренних рабочих процессов, где требуется гибкая, скриптируемая среда с управлением окнами через Lisp; однако из‑за скудной документации и неочевидных точек интеграции проект требует ручного анализа и проверки зависимостей перед вводом в продакшн. В текущем состоянии готовности (средний уровень) его можно безопасно использовать в тестовых и экспериментальных сценариях, но для критически важных систем рекомендуется провести дополнительную валидацию и оценку затрат на настройку.

### 中文

**项目简介**  
stumpwm/mahogany 是一个用 Common Lisp 编写的、类 StumpWM 风格的 Wayland 合成器，旨在为喜欢平铺窗口管理器的开发者提供一个高度可编程、轻量级的 Wayland 运行时环境。

**价值**  
- **可编程化**：继承了 StumpWM 的 Lisp 配置模型，用户可以用 Lisp 脚本实时修改窗口行为、布局和快捷键，适合需要深度定制的工作流。  
- **轻量且透明**：代码基于 Common Lisp，依赖相对少，便于审计和二次开发；对系统资源的占用也比主流的 GNOME/KDE 合成器要低。  
- **原型与内部工具**：因为其灵活的扩展能力，适合作为 UI 原型平台或内部工具的显示层，快速验证交互概念。

**典型接入方式**  
1. **源码编译**：克隆仓库后，使用 `sbcl`（或其他兼容的 Common Lisp 实现）编译生成可执行文件。  
2. **配置加载**：在 `~/.config/mahogany/` 目录放置 Lisp 配置文件（类似 StumpWM 的 `~/.stumpwmrc`），在启动时自动加载。  
3. **Wayland 会话**：在 `~/.xinitrc` 或 `~/.profile` 中添加 `exec mahogany`，并在登录管理器中选择 “Mahogany” 会话，或直接在终端执行 `mahogany` 启动 Wayland 会话。  
4. **与外部程序交互**：通过 Lisp 提供的 IPC 接口或 DBus（如有实现）与其他后台服务、窗口程序进行通信，实现自定义的工作流集成。

**生产可用性**  
- **成熟度**：项目已有 355 颗星、34 次 fork，且最近一次提交在 2026‑05‑10，活跃度尚可。  
- **适用场景**：适合内部原型、实验性平台或对窗口管理高度自定义的团队使用。直接在面向终端用户的生产环境部署仍需评估。  
- **风险与准备工作**  
  - **集成路径不明确**：官方文档和元数据提供的集成信息有限，需自行审查源码并验证与现有 Wayland 框架（如 `weston`、`sway`）的兼容性。  
  - **依赖与维护**：确认项目所依赖的 Common Lisp 实现、Wayland 协议版本以及底层库（如 `libwayland-client`）在目标系统上可用，并评估后续维护成本。  
  - **稳定性**：目前标记为 “Medium”，在关键业务系统使用前建议进行完整的功能、性能和安全性测试。  

综上，stumpwm/mahogany 为需要 Lisp 可编程窗口管理的团队提供了一个灵活的 Wayland 合成器原型平台，适合在受控环境或内部项目中先行试用，正式投入生产前需完成集成验证和运维准备。

## 🧭 Practical evaluation

**Value:** stumpwm/mahogany may be useful when its README and activity match a concrete workflow.

**Best use cases**

- Not enough metadata yet.

**Integration notes:** Needs manual inspection before adoption because integration signals are sparse in the discovered metadata.

**Production readiness:** Medium: useful for prototypes or internal workflows, with dependency and maintenance checks before production.

**Quality signals**

- 355 GitHub stars
- 34 forks
- updated 2026-05-10
- primary language: Common Lisp

**Risks:** Integration path is not obvious from metadata; validate setup cost before committing.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 39/100 |
| stars | 54/100 |
| topics | 0/100 |
| outlook | 66/100 |
| quality | 62/100 |
| recency | 100/100 |
| adoption | 50/100 |
| production | 68/100 |
| usefulness | 42/100 |
| integration | 30/100 |
| sourceTrust | 100/100 |

---

<sub>🔭 Discovered 2026-05-10 · [View on GitHub](https://github.com/stumpwm/mahogany) · [← Back to Misc](./README.md)</sub>
