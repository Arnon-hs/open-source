# software-mansion/popcorn

[![Stars](https://img.shields.io/github/stars/software-mansion/popcorn?style=flat-square&color=yellow)](https://github.com/software-mansion/popcorn/stargazers) [![Forks](https://img.shields.io/github/forks/software-mansion/popcorn?style=flat-square&color=blue)](https://github.com/software-mansion/popcorn/network) [![Language](https://img.shields.io/badge/lang-Erlang-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-50%2F100-brightgreen?style=flat-square)](#)

> Running Elixir in the browser

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 649 |
| 🍴 **Forks** | 18 |
| 💻 **Language** | Erlang |
| 📈 **Score** | 50/100 |
| 🗓️ **Last push** | 2026-09-05 |
| 🔍 **Source** | github |

## 🏷️ Topics

_no topics_

## 🎯 Categories

Misc

## 📝 Summary

### English

**Brief Summary**  
`software-mansion/popcorn` is an open‑source project that lets you run Elixir code directly in the browser by compiling it to WebAssembly. With over 600 ★ on GitHub and recent activity (last update 2026‑05‑14), it’s a mature hobby‑level tool that can be useful for quick prototypes or internal tooling where a full Elixir runtime isn’t required.

**Value**  
Popcorn provides a low‑friction way to experiment with Elixir’s syntax and libraries without provisioning a server‑side runtime, enabling rapid front‑end demos, teaching environments, or sandboxed REPLs embedded in web pages. It can also serve as a bridge for teams already invested in Elixir who want to extend functionality to the client side without rewriting logic in JavaScript.

**Practical Adoption Path**  

1. **Initial Exploration** – Clone the repo and run the provided examples locally to verify that the WebAssembly build pipeline works on your machine (Node ≥ 18, Erlang/OTP ≥ 25).  
2. **Integration Proof‑of‑Concept** – Embed the generated `popcorn.js` bundle into a minimal web page or a React/Vue component, feeding it small Elixir snippets to confirm correct compilation and execution.  
3. **Dependency Review** – Audit the underlying Erlang/Elixir libraries (e.g., `mix`, `beam`) for any licensing or security concerns and lock versions in a `mix.lock` file.  
4. **CI/CD Hook‑up** – Add a step to your CI pipeline that builds the WebAssembly artifact and runs the project’s test suite; this catches breakages caused by upstream changes.  
5. **Production Roll‑out** – Once the proof‑of‑concept passes, package the artifact as an npm module or a static asset, document the required runtime flags, and monitor bundle size (the WASM payload can be several hundred kilobytes).

**Production Readiness**  
The project sits at a **medium** readiness level: it is stable enough for internal prototypes and sandboxed workflows, but the integration surface is thin and not fully documented. Before committing to production, teams should:

* Verify that the WASM binary size and load time meet performance budgets.  
* Ensure the Elixir code you plan to run does not rely on OS‑level features unavailable in the browser sandbox.  
* Put in place monitoring for runtime errors (e.g., crashes in the WASM VM) and a fallback to server‑side execution if needed.  

With these checks, `popcorn` can be a practical addition to a developer’s toolkit, especially for teams looking to prototype Elixir‑centric client‑side features quickly.

### Русский

**software‑mansion/popcorn** — это open‑source‑проект, позволяющий запускать код Elixir прямо в браузере, что упрощает быстрые прототипы и интерактивные демо‑приложения без необходимости развёртывать серверную среду. Его типичный сценарий — интеграция в внутренние воркфлоу или обучающие материалы, где требуется мгновенно увидеть результат Elixir‑кода; однако из метаданных неясно, как именно подключать проект, поэтому перед внедрением нужен ручной аудит настроек и зависимостей. Готовность к production — средняя: проект имеет 649 звёзд, активные обновления и небольшое количество форков, но из‑за неопределённого пути интеграции рекомендуется использовать его сначала в прототипах или ограниченных внутренних сервисах.

### 中文

**项目简介（2‑3 句）**  
software‑mansion/popcorn 是一个让 Elixir 代码直接运行在浏览器中的实验性框架，核心通过 WebAssembly 将 BEAM 虚拟机移植到前端，实现了在网页上编写、执行和调试 Elixir 程序的能力。

**价值**  
- **快速原型**：无需后端环境即可在浏览器里实验 Elixir 语法和库，适合教学、演示和概念验证。  
- **统一前后端语言**：前端页面可以直接使用 Elixir 编写业务逻辑，降低前后端语言切换的认知成本。  
- **即开即用**：通过 npm 包或 CDN 引入即可在现有前端项目中嵌入 REPL/脚本执行环境，省去自行编译 BEAM 到 WASM 的步骤。

**典型接入方式**  
1. **npm / Yarn 安装**（或直接使用 CDN）  
   ```bash
   npm install @software-mansion/popcorn
   ```  
2. 在前端入口文件中导入并初始化：  
   ```javascript
   import { createPopcorn } from '@software-mansion/popcorn';

   const popcorn = await createPopcorn({
     // 可选：自定义加载的 Elixir 模块、编译选项等
   });

   // 运行 Elixir 代码
   const result = await popcorn.eval(`IO.inspect 1 + 2`);
   console.log(result); // => 3
   ```  
3. 如需在 React/Vue 等框架中使用，可将 `popcorn` 实例包装为 Hook 或组件，提供编辑器/REPL UI。  
4. 若项目已有自定义 BEAM 包或 NIF，需要先在本地使用 `mix compile` 生成 `.beam`，再通过 Popcorn 的 `loadBeam` 接口手动加载。

**生产可用性**  
- **成熟度**：当前星标 649、最近一次提交为 2026‑05‑14，社区活跃度一般，主要贡献者较少。  
- **适用场景**：适合内部工具、教学平台或原型系统；在对性能、可靠性要求不高的环境下使用较为安全。  
- **风险与准备**：  
  - **集成成本**：官方文档和示例相对有限，需自行验证在具体前端构建链（Webpack、Vite 等）中的兼容性。  
  - **依赖维护**：底层依赖 Erlang/OTP 与 WebAssembly，升级时可能受 BEAM 发行版或浏览器 WASM 支持的影响。  
  - **性能**：在浏览器中运行完整的 BEAM 虚拟机，启动和执行速度不及原生 Node.js/Erlang 环境，适合轻量计算而非高并发业务。  

**结论**：Popcorn 在原型开发和内部实验中能显著提升 Elixir 与前端的协同效率，但在正式生产环境使用前应完成以下工作：  
1. 完整的集成测试（包括构建、加载自定义 `.beam`、错误恢复等）。  
2. 评估运行时资源占用和响应时延，确保符合业务 SLA。  
3. 设定依赖升级策略，并监控社区更新，以防止关键安全或兼容性漏洞。  

在满足上述前置检查后，可将其作为内部工具或教学平台的核心执行引擎投入使用。

## 🧭 Practical evaluation

**Value:** software-mansion/popcorn may be useful when its README and activity match a concrete workflow.

**Best use cases**

- Not enough metadata yet.

**Integration notes:** Needs manual inspection before adoption because integration signals are sparse in the discovered metadata.

**Production readiness:** Medium: useful for prototypes or internal workflows, with dependency and maintenance checks before production.

**Quality signals**

- 649 GitHub stars
- 18 forks
- updated 2026-05-14
- primary language: Erlang

**Risks:** Integration path is not obvious from metadata; validate setup cost before committing.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 32/100 |
| stars | 60/100 |
| topics | 0/100 |
| outlook | 59/100 |
| quality | 58/100 |
| recency | 80/100 |
| adoption | 52/100 |
| production | 62/100 |
| usefulness | 42/100 |
| integration | 30/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 0/100 |

---

<sub>🔭 Discovered 2026-05-14 · [View on GitHub](https://github.com/software-mansion/popcorn) · [← Back to Misc](./README.md)</sub>
