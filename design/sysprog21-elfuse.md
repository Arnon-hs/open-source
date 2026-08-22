# sysprog21/elfuse

[![Stars](https://img.shields.io/github/stars/sysprog21/elfuse?style=flat-square&color=yellow)](https://github.com/sysprog21/elfuse/stargazers) [![Forks](https://img.shields.io/github/forks/sysprog21/elfuse?style=flat-square&color=blue)](https://github.com/sysprog21/elfuse/network) [![Language](https://img.shields.io/badge/lang-Unknown-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-39%2F100-brightgreen?style=flat-square)](#)

> Discovered from Lobsters: elfuse: Run Arm64/x86-64 Linux ELF binaries on macOS Apple Silicon

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | — |
| 🍴 **Forks** | — |
| 💻 **Language** | Unknown |
| 📈 **Score** | 39/100 |
| 🗓️ **Last push** | 2026-07-15 |
| 🔍 **Source** | lobsters |

## 🏷️ Topics

`lobsters`

## 🎯 Categories

Design

## 📝 Summary

### English

elfuse lets macOS Apple Silicon users run native Arm64/x86‑64 Linux ELF binaries by providing a lightweight compatibility layer, eliminating the need for full virtual machines or cross‑compilation. Adoption is straightforward—clone the repo, build/install the tool, and point it at your Linux binaries—but you should first review its sparse documentation, license, and issue tracker to ensure it fits your workflow. The project is marked as medium‑readiness: suitable for prototypes or internal scripts, but production use requires additional dependency checks, maintenance verification, and testing before relying on it in critical environments.

### Русский

Эльфюз (elfuse) - открытый исходный проект, позволяющий запускать Linux-экзекутивные файлы (ELF) на macOS с Apple Silicon. Он может быть полезен в сценариях, когда требуется запускать Linux-приложения на macOS, но требует тщательного осмотра README и активности проекта перед внедрением. Проект готов к использованию в прототипах и внутренних потоках, но требует проверки зависимостей и поддержки перед использованием в производственной среде.

### 中文

elfuse 使得在 macOS Apple Silicon 上直接执行 Arm64 或 x86‑64 的 Linux ELF 二进制文件成为可能，省去了完整虚拟机或容器的开销，适合需要快速跑 Linux 工具或测试二进制的开发工作流。典型的接入方式是通过 Homebrew 源码编译或直接下载二进制后，使用 `elfuse ./your-linux-binary` 来加载并运行目标程序。该项目目前处于

## 🧭 Practical evaluation

**Value:** elfuse: Run Arm64/x86-64 Linux ELF binaries on macOS Apple Silicon may be useful when its README and activity match a concrete workflow.

**Best use cases**

- Not enough metadata yet.

**Integration notes:** Needs manual inspection before adoption because integration signals are sparse in the discovered metadata.

**Production readiness:** Medium: useful for prototypes or internal workflows, with dependency and maintenance checks before production.

**Quality signals**

- updated 2026-07-15
- 1 topics

**Risks:** Quality signals are limited; verify license, maintenance, docs, issues, and release cadence before using it.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 0/100 |
| stars | 0/100 |
| topics | 13/100 |
| outlook | 52/100 |
| quality | 37/100 |
| recency | 100/100 |
| adoption | 0/100 |
| production | 56/100 |
| usefulness | 42/100 |
| integration | 30/100 |
| sourceTrust | 70/100 |

---

<sub>🔭 Discovered 2026-07-16 · [View on GitHub](https://github.com/sysprog21/elfuse) · [← Back to Design](./README.md)</sub>
