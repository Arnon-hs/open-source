# bilelmoussaoui/ashpd

[![Stars](https://img.shields.io/github/stars/bilelmoussaoui/ashpd?style=flat-square&color=yellow)](https://github.com/bilelmoussaoui/ashpd/stargazers) [![Forks](https://img.shields.io/github/forks/bilelmoussaoui/ashpd?style=flat-square&color=blue)](https://github.com/bilelmoussaoui/ashpd/network) [![Language](https://img.shields.io/badge/lang-Rust-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-54%2F100-brightgreen?style=flat-square)](#)

> A Rust wrapper around XDG portals DBus interfaces

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 359 |
| 🍴 **Forks** | 69 |
| 💻 **Language** | Rust |
| 📈 **Score** | 54/100 |
| 🗓️ **Last push** | 2026-09-05 |
| 🔍 **Source** | github |

## 🏷️ Topics

`flatpak` `libportal` `portals` `rust` `wrapper` `xdg` `zbus`

## 🎯 Categories

Misc

## 📝 Summary

### English

**Brief summary (2‑3 sentences)**  
*ashpd* is a Rust library that wraps the XDG Portal DBus interfaces, letting developers invoke sandbox‑friendly desktop services (e.g., file pickers, notifications, power management) without writing custom UI code. With 359 ★ on GitHub and active maintenance, it offers a convenient, cross‑desktop way to build user‑facing features while keeping the application sandbox‑compatible.

**Value**  
- **Accelerates UI development** – By delegating common tasks to the system portal, teams can ship functional front‑ends faster and avoid reinventing dialogs, notifications, or media controls.  
- **Consistent user experience** – Portals present native‑look‑and‑feel dialogs that automatically adapt to the user’s desktop environment, improving perceived quality without extra UI work.  
- **Sandbox‑friendly** – Works out‑of‑the‑box with Flatpak, Snap and other sandboxed runtimes, removing a major pain point for Rust applications targeting modern Linux distributions.

**Practical adoption path**  
1. **Proof‑of‑concept** – Clone the repo, run the examples, and add a minimal dependency (`ashpd = "X.Y"`) to a sandboxed Rust binary. Verify that a portal call (e.g., `FileChooser`) works on the target desktop.  
2. **README & CI check** – Follow the README to set up DBus session permissions; add a CI job that builds the crate on stable Rust to catch breaking changes early.  
3. **Component integration** – Replace existing custom dialogs with the corresponding portal calls, gradually expanding coverage (notifications → `ashpd::notification`, power actions → `ashpd::power`).  
4. **Testing & fallback** – Implement a small fallback UI for environments where portals are unavailable, ensuring graceful degradation.

**Production readiness**  
- **Maturity:** Medium. The library is actively maintained (last update 2026‑06‑28) and has a modest but healthy community (359 ★, 69 forks).  
- **Suitability:** Ideal for prototypes, internal tools, or any product that runs in sandboxed Linux environments. For large‑scale production, perform a dependency audit (check transitive crates, licensing, and DBus version compatibility) and add integration tests around portal failures.  
- **Risk mitigation:** Validate the setup cost (DBus policy, sandbox permissions) early, and keep an eye on upstream XDG Portal changes that could require library updates. Once the proof‑of‑concept is stable, the library can be promoted to production with confidence.

### Русский

**bilelmoussaoui/ashpd** – это Rust‑обертка над DBus‑интерфейсами XDG portals, позволяющая быстро добавить готовые пользовательские окна (файловый диалог, экранный шот, запрос доступа к устройствам) без написания собственного UI. Типичный сценарий: в небольшом прототипе или внутреннем инструменте подключить библиотеку, реализовать нужный портал и проверить работу через небольшую proof‑of‑concept‑программу, после чего постепенно интегрировать в основной фронтенд. Готовность к production — средняя: проект стабилен (359★, активные обновления), но требует проверки зависимости, настройки сборки и подтверждения, что интеграционный путь подходит под ваш стек.

### 中文

**简短介绍**

bilelmoussaoui/ashpd 是一个 Rust 包围器，用于简化基于 XDG 端口 DBus 接口的开发。它可以帮助开发者快速构建用户界面，减少自定义 UI 工作量。

**价值**

bilelmoussaoui/ashpd 的价值在于它可以帮助开发者快速构建用户界面，减少自定义 UI 工作量，从而提高前端交付效率。

**典型接入方式**

典型的接入方式是先评估 bilelmoussaoui/ashpd 的可行性，通过一个小的原型和 README 检查，来确定是否适合项目的需求。然后，可以按照 README 文档中的步骤进行集成。

**生产可用性**

bilelmoussaoui/ashpd 的生产可用性为中等。它适合用于原型设计或内部工作流程，但在生产环境中需要进行依赖和维护检查以确保其稳定性。

## 🧭 Practical evaluation

**Value:** bilelmoussaoui/ashpd helps ship user-facing interfaces with less custom UI work.

**Best use cases**

- build product UI faster
- reuse interface components
- improve frontend delivery

**Integration notes:** Looks feasible to evaluate, but integration should start with a small proof of concept and README check.

**Production readiness:** Medium: useful for prototypes or internal workflows, with dependency and maintenance checks before production.

**Quality signals**

- 359 GitHub stars
- 69 forks
- updated 2026-06-28
- primary language: Rust
- 7 topics

**Risks:** Integration path is not obvious from metadata; validate setup cost before committing.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 46/100 |
| stars | 54/100 |
| topics | 88/100 |
| outlook | 68/100 |
| quality | 72/100 |
| recency | 80/100 |
| adoption | 52/100 |
| production | 66/100 |
| usefulness | 42/100 |
| integration | 30/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 0/100 |

---

<sub>🔭 Discovered 2026-06-28 · [View on GitHub](https://github.com/bilelmoussaoui/ashpd) · [← Back to Misc](./README.md)</sub>
