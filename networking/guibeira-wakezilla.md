# guibeira/wakezilla

[![Stars](https://img.shields.io/github/stars/guibeira/wakezilla?style=flat-square&color=yellow)](https://github.com/guibeira/wakezilla/stargazers) [![Forks](https://img.shields.io/github/forks/guibeira/wakezilla?style=flat-square&color=blue)](https://github.com/guibeira/wakezilla/network) [![Language](https://img.shields.io/badge/lang-Rust-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-55%2F100-brightgreen?style=flat-square)](#)

> A simple Wake-on-LAN & reverse proxy toolkit — wake, route, and control your machines from anywhere. 🦖

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 291 |
| 🍴 **Forks** | 12 |
| 💻 **Language** | Rust |
| 📈 **Score** | 55/100 |
| 🗓️ **Last push** | 2026-09-05 |
| 🔍 **Source** | github |

## 🏷️ Topics

`proxy` `proxy-server` `rust` `wake-on-lan`

## 🎯 Categories

Networking · Backend

## 📝 Summary

### English

**Summary**  
Wakezilla (guibeira/wakezilla) is a Rust‑based toolkit that combines Wake‑on‑LAN capabilities with a lightweight reverse‑proxy, letting you power on, route traffic to, and remotely control machines through a simple web UI. With a ready‑made front‑end and back‑end stack, it reduces the amount of custom UI code you need to write for internal dashboards or prototype control panels.  

**Value**  
- **Speed to market** – The pre‑built interface and proxy logic let teams ship user‑facing control panels without building the UI and networking glue from scratch.  
- **Component reuse** – UI widgets for machine status, wake actions, and connection logs are bundled, so they can be dropped into other Rust or WebAssembly front‑ends.  
- **Unified workflow** – By handling both the wake‑on‑LAN packet and the reverse‑proxy routing, the project eliminates the need for separate scripts or services, simplifying deployment and maintenance.  

**Practical adoption path**  
1. **Proof‑of‑concept** – Clone the repo, run the provided Dockerfile or `cargo run` to spin up the demo UI, and verify that you can wake a test machine on your LAN.  
2. **README validation** – Follow the quick‑start instructions; adjust the configuration file (hosts, ports, authentication) to match your environment.  
3. **Integration** – Replace the demo UI components with your own branding or embed the UI as an iframe in an existing dashboard. Hook the proxy endpoint into your internal network routing.  
4. **Testing** – Write a few integration tests that exercise the wake request and proxy forwarding to ensure the tool works with your security policies.  

**Production readiness**  
Wakezilla scores a medium readiness level. It is actively maintained (last update 2026‑07‑01) and has a modest community (≈ 291 ★, 12 forks). The codebase is small and written in Rust, which is a plus for performance and safety, but the integration documentation is sparse and the setup steps are not fully automated. Before production use, you should:  

- Perform a dependency audit (check for outdated crates).  
- Harden the reverse‑proxy (TLS termination, auth, rate limiting).  
- Validate that the wake‑on‑LAN broadcast works across your network topology (VLANs, firewalls).  

With these checks, Wakezilla is well‑suited for internal tools, prototypes, or low‑risk production services that need quick remote‑machine control.

### Русский

**Wakezilla** — это набор инструментов на Rust для Wake‑on‑LAN и обратного прокси, позволяющий удалённо включать машины и маршрутизировать трафик через единый пользовательский интерфейс. Его типичное внедрение — быстрый прототип или внутренний сервис, где нужен готовый UI‑компонент для управления устройствами без разработки собственного фронтенда; рекомендуется начать с небольшого proof‑of‑concept и проверки README. Проект имеет средний уровень готовности к продакшну — достаточно звёзд и недавних обновлений, но требует проверки зависимостей и уточнения пути интеграции перед масштабным использованием.

### 中文

guibeira/wakezilla 是一个基于 Rust 的轻量级 Wake‑on‑LAN 与反向代理工具包，能够让你从任何地方唤醒、路由和控制机器，从而大幅降低自定义 UI 工作量，加速产品界面的构建和组件复用。典型的接入方式是先阅读 README 并搭建一个小规模的概念验证（PoC），确认其与现有前后端栈的兼容性后再逐步集成。目前该项目处于中等成熟度，适用于原型

## 🧭 Practical evaluation

**Value:** guibeira/wakezilla helps ship user-facing interfaces with less custom UI work.

**Best use cases**

- build product UI faster
- reuse interface components
- improve frontend delivery

**Integration notes:** Looks feasible to evaluate, but integration should start with a small proof of concept and README check.

**Production readiness:** Medium: useful for prototypes or internal workflows, with dependency and maintenance checks before production.

**Quality signals**

- 291 GitHub stars
- 12 forks
- updated 2026-07-01
- primary language: Rust
- 4 topics

**Risks:** Integration path is not obvious from metadata; validate setup cost before committing.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 28/100 |
| stars | 52/100 |
| topics | 50/100 |
| outlook | 66/100 |
| quality | 63/100 |
| recency | 80/100 |
| adoption | 46/100 |
| production | 63/100 |
| usefulness | 58/100 |
| integration | 30/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 200/100 |

---

<sub>🔭 Discovered 2026-07-01 · [View on GitHub](https://github.com/guibeira/wakezilla) · [← Back to Networking](./README.md)</sub>
