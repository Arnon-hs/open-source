# Indra55/bezel

[![Stars](https://img.shields.io/github/stars/Indra55/bezel?style=flat-square&color=yellow)](https://github.com/Indra55/bezel/stargazers) [![Forks](https://img.shields.io/github/forks/Indra55/bezel?style=flat-square&color=blue)](https://github.com/Indra55/bezel/network) [![Language](https://img.shields.io/badge/lang-Rust-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-49%2F100-brightgreen?style=flat-square)](#)

> A lightweight Rust daemon for trackpad gestures on Wayland compositor

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 107 |
| 🍴 **Forks** | 3 |
| 💻 **Language** | Rust |
| 📈 **Score** | 49/100 |
| 🗓️ **Last push** | 2026-09-05 |
| 🔍 **Source** | github |

## 🏷️ Topics

`evdev` `gestures` `linux` `rust` `wayland`

## 🎯 Categories

Misc

## 📝 Summary

### English

Here's a brief summary of the Indra55/bezel project:

Indra55/bezel is an open-source, lightweight Rust daemon designed for trackpad gestures on Wayland compositor, offering a unique solution for trackpad enthusiasts. Its value lies in its potential to enhance workflows for those who can adapt to its specific setup, as indicated by its 107 GitHub stars. However, its integration path is not immediately obvious, requiring a proof of concept and thorough setup cost validation before adoption.

**Value:** 
The project's value proposition is that it may be useful for users who can effectively integrate it into their workflow, as indicated by its README and activity. This suggests that the project's value lies in its ability to enhance specific use cases, rather than being a general-purpose solution.

**Practical Adoption Path:**
The practical adoption path for this project involves:

1. Reviewing the README to understand the project's setup and integration requirements.
2. Evaluating the setup cost and potential maintenance burden.
3. Creating a small proof of concept to test the project's feasibility and determine the integration path.
4. Validating the project's dependency and maintenance requirements before committing to production use.

**Production Readiness:**
The project's production readiness is classified as medium, indicating that it may be suitable

### Русский

Резюме:

Indra55/bezel - легковесный демон на языке Rust для реализации трекпадных жестов в окружении Wayland. Этот проект может быть полезен в сценариях, когда README и активность проекта соответствуют конкретному рабочему процессу. Проект готов к интеграции в среднем уровне, что делает его подходящим вариантом для прототипов или внутренних рабочих процессов после проверки зависимости и обслуживания.

### 中文

**项目简介（2‑3 句）**  
Indra55/bezel 是一个基于 Rust 实现的轻量级守护进程，专门在 Wayland 合成器上捕获并处理触控板手势。它通过 DBus/Unix socket 与桌面环境通信，提供可自定义的手势映射，适合需要在 Wayland 上实现快捷手势的用户和开发者。

**价值**  
- **低资源占用**：使用 Rust 编写，运行时内存和 CPU 开销极小，几乎不影响系统性能。  
- **可定制**：手势与命令的映射通过简单的 TOML 配置文件完成，支持自定义脚本或系统快捷键。  
- **Wayland 原生**：不依赖 X11 兼容层，直接在 Wayland 合成器（如 sway、river、wlroots 系列）上工作，解决了许多传统手势工具在 Wayland 上失效的问题。  

**典型接入方式**  
1. **阅读 README**：确认项目支持的合成器（目前已在 sway、river 上测试），并按照文档安装依赖（Rust toolchain、libinput）。  
2. **编译/安装**：`cargo install --locked --path .` 或使用提供的 prebuilt 二进制。  
3. **配置**：在 `~/.config/bezel/config.toml` 中定义手势 → 命令映射，例如：  
   ```toml
   [gesture.swipe_up]
   command = "playerctl play-pause"
   ```
4. **启动守护进程**：将 `bezel.service`（systemd）或 `bezel.desktop`（autostart）加入用户的启动项。  
5. **验证**：使用 `bezel --list` 查看已识别的手势，确保手势触发对应命令。  

**生产可用性**  
- **成熟度**：当前拥有 107+ 星、3 个 fork，最近一次提交在 2026‑07‑04，活跃度尚可。  
- **适用场景**：适合内部原型、个人工作站或需要快速实现手势功能的团队。  
- **风险与注意事项**：  
  - 项目文档相对简略，集成前需自行验证与目标 Wayland 合成器的兼容性。  
  - 依赖 `libinput` 与系统 DBus，生产环境需做好版本锁定和安全审计。  
  - 维护者人数有限，遇到重大 bug 时可能需要自行修复或提交 PR。  

综上，bezel 在资源占用和 Wayland 原生支持方面具备明显优势，适合作为原型或内部工具快速上线；若要在大规模生产环境使用，建议先做小范围的 PoC，评估兼容性、配置维护成本以及社区响应速度后再决定是否正式推广。

## 🧭 Practical evaluation

**Value:** Indra55/bezel may be useful when its README and activity match a concrete workflow.

**Best use cases**

- Not enough metadata yet.

**Integration notes:** Looks feasible to evaluate, but integration should start with a small proof of concept and README check.

**Production readiness:** Medium: useful for prototypes or internal workflows, with dependency and maintenance checks before production.

**Quality signals**

- 107 GitHub stars
- 3 forks
- updated 2026-07-04
- primary language: Rust
- 5 topics

**Risks:** Integration path is not obvious from metadata; validate setup cost before committing.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 15/100 |
| stars | 43/100 |
| topics | 63/100 |
| outlook | 61/100 |
| quality | 60/100 |
| recency | 80/100 |
| adoption | 35/100 |
| production | 62/100 |
| usefulness | 42/100 |
| integration | 30/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 0/100 |

---

<sub>🔭 Discovered 2026-07-04 · [View on GitHub](https://github.com/Indra55/bezel) · [← Back to Misc](./README.md)</sub>
