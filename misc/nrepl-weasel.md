# nrepl/weasel

[![Stars](https://img.shields.io/github/stars/nrepl/weasel?style=flat-square&color=yellow)](https://github.com/nrepl/weasel/stargazers) [![Forks](https://img.shields.io/github/forks/nrepl/weasel?style=flat-square&color=blue)](https://github.com/nrepl/weasel/network) [![Language](https://img.shields.io/badge/lang-Clojure-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-49%2F100-brightgreen?style=flat-square)](#)

> ClojureScript browser REPL using WebSockets

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 325 |
| 🍴 **Forks** | 32 |
| 💻 **Language** | Clojure |
| 📈 **Score** | 49/100 |
| 🗓️ **Last push** | 2026-09-05 |
| 🔍 **Source** | github |

## 🏷️ Topics

_no topics_

## 🎯 Categories

Misc

## 📝 Summary

### English

**Brief Summary**  
nrepl/weasel is a ClojureScript library that provides a browser‑based REPL over WebSockets, letting developers interactively evaluate code in the browser from a nREPL client. With 325 GitHub stars and recent updates (June 2026), it is a mature hobby‑project that can accelerate prototyping and debugging of ClojureScript applications.

**Value**  
- **Live feedback**: Edit code in your editor and see results instantly in the browser without rebuilding or reloading the page.  
- **Tooling integration**: Works with standard nREPL tooling (cider, clojure‑lsp, etc.), so you can keep a single REPL workflow for both JVM and browser targets.  
- **Low entry cost**: Adding a single dependency and a few lines of startup code is enough to get a REPL session running in any modern browser.

**Practical Adoption Path**  
1. **Evaluate fit** – Review the README and example projects to confirm that the WebSocket‑based REPL matches your development workflow (e.g., you already run an nREPL server).  
2. **Add dependency** – Include `[nrepl/weasel "0.2.0"]` (or the latest tag) in your `deps.edn`/`project.clj`.  
3. **Bootstrap the REPL** – Insert `(weasel.repl/connect "ws://localhost:9000")` (or the provided helper) in your ClojureScript entry point and start the WebSocket server (`lein weasel` or a custom Ring handler).  
4. **Connect from editor** – Use your editor’s nREPL client (CIDER, Calva, etc.) to connect to the same nREPL port; you’ll now have a browser REPL alongside the server REPL.  
5. **Iterate & test** – Verify that code evaluation, namespace loading, and source‑map support work for your codebase; adjust firewall or CSP settings if needed.

**Production Readiness**  
- **Maturity**: Medium. The project is actively maintained (last commit 2026‑06‑27) and has a solid star count, indicating community interest, but it is still primarily aimed at development and prototyping.  
- **Stability**: The core REPL functionality is stable, yet edge‑case integration (e.g., complex build pipelines, custom WebSocket servers, or strict CSP policies) may require additional testing.  
- **Maintenance**: No formal release schedule; you should monitor the repository for breaking changes and consider pinning a specific version.  
- **Recommendation**: Suitable for internal tools, demos, and developer workflows. For production services, perform a short proof‑of‑concept to validate the integration cost, ensure the WebSocket endpoint can be secured, and confirm that the library’s dependency footprint aligns with your release policy before promoting it to a critical pipeline.

### Русский

**nrepl/weasel** — это open‑source‑библиотека, предоставляющая ClojureScript REPL в браузере через WebSocket, что упрощает интерактивную отладку и быстрый прототипинг клиентского кода. Она подходит для проектов, где требуется «живой» REPL в процессе разработки (например, UI‑прототипы или внутренние инструменты), но перед внедрением стоит проверить совместимость с вашей сборкой и убедиться в актуальности зависимостей, так как интеграционный путь из метаданных не очевиден. Готовность к production — средняя: библиотека стабильно работает в прототипах, но требует ручной проверки и возможных доработок перед использованием в продакшене.

### 中文

**项目简介（2‑3 句）**  
nrepl/weasel 是一个基于 WebSocket 的 ClojureScript 浏览器 REPL，实现了在浏览器中实时交互式编写、调试 ClojureScript 代码的能力。它通过 nREPL 协议与浏览器保持双向通信，使前端开发者能够像在本地 REPL 中一样即时查看求值结果、调试函数和热加载代码。

**价值**  
- **即时反馈**：无需刷新页面或重新编译，即可在浏览器中直接执行 ClojureScript 表达式，显著提升调试和原型开发效率。  
- **统一工具链**：与 nREPL、cider、shadow‑cljs 等常用 Clojure 开发生态保持兼容，团队可以在同一 REPL 环境下同时调试后端和前端代码。  
- **轻量易用**：只需在项目中加入几行依赖和启动代码，即可在任意支持 WebSocket 的浏览器中使用，适合作为内部原型或教学演示工具。

**典型接入方式**  
1. **依赖添加**  
   ```clojure
   ;; project.clj / deps.edn
   :dependencies [[nrepl/weasel "0.2.0"]]
   ```
2. **启动 WebSocket REPL**（常配合 shadow‑cljs）  
   ```clojure
   (require '[weasel.repl :as repl])
   (repl/connect "ws://localhost:9000")   ; 连接到浏览器端的 REPL
   ```
3. **在浏览器端注入脚本**（shadow‑cljs 示例）  
   ```clojure
   ;; shadow-cljs.edn
   {:builds {:app {:target :browser
                   :js-options {:js-provider :shadow}
                   :devtools {:preloads [weasel.repl]}}}}
   ```
   启动 `shadow-cljs watch app` 后，浏览器会自动建立 WebSocket 连接，REPL 即可使用。

**生产可用性**  
- **成熟度**：已有 325 ★、32 Fork，最近一次提交在 2026‑06‑27，社区活跃度一般。  
- **适用场景**：非常适合原型开发、内部工具、教学或调试阶段使用；在生产环境中可作为临时诊断手段，但不建议直接用于面向终端用户的服务。  
- **风险与注意事项**  
  - 集成路径不够明确，需要自行检查项目的 WebSocket 配置、CORS 策略以及与现有 nREPL 服务器的兼容性。  
  - 生产环境应关闭或限制 REPL 端口，防止未授权的代码执行。  
  - 需要评估依赖的维护状态以及与主流前端构建工具（如 shadow‑cljs、figwheel）配合的细节。  

综上，nrepl/weasel 在提升 ClojureScript 开发体验方面价值突出，接入成本适中，适合作为内部或原型项目的 REPL 方案；在正式生产环境使用前应进行安全加固和依赖审查。

## 🧭 Practical evaluation

**Value:** nrepl/weasel may be useful when its README and activity match a concrete workflow.

**Best use cases**

- Not enough metadata yet.

**Integration notes:** Needs manual inspection before adoption because integration signals are sparse in the discovered metadata.

**Production readiness:** Medium: useful for prototypes or internal workflows, with dependency and maintenance checks before production.

**Quality signals**

- 325 GitHub stars
- 32 forks
- updated 2026-06-27
- primary language: Clojure

**Risks:** Integration path is not obvious from metadata; validate setup cost before committing.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 38/100 |
| stars | 53/100 |
| topics | 0/100 |
| outlook | 59/100 |
| quality | 57/100 |
| recency | 80/100 |
| adoption | 49/100 |
| production | 61/100 |
| usefulness | 42/100 |
| integration | 30/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 0/100 |

---

<sub>🔭 Discovered 2026-06-27 · [View on GitHub](https://github.com/nrepl/weasel) · [← Back to Misc](./README.md)</sub>
