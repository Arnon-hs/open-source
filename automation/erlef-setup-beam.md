# erlef/setup-beam

[![Stars](https://img.shields.io/github/stars/erlef/setup-beam?style=flat-square&color=yellow)](https://github.com/erlef/setup-beam/stargazers) [![Forks](https://img.shields.io/github/forks/erlef/setup-beam?style=flat-square&color=blue)](https://github.com/erlef/setup-beam/network) [![Language](https://img.shields.io/badge/lang-JavaScript-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-54%2F100-brightgreen?style=flat-square)](#)

> Set up your BEAM-based GitHub Actions workflow (Erlang, Elixir, Gleam, ...)

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 449 |
| 🍴 **Forks** | 85 |
| 💻 **Language** | JavaScript |
| 📈 **Score** | 54/100 |
| 🗓️ **Last push** | 2026-09-05 |
| 🔍 **Source** | github |

## 🏷️ Topics

_no topics_

## 🎯 Categories

Automation

## 📝 Summary

### English

**Brief Summary (2‑3 sentences)**  
`erlef/setup-beam` is a GitHub Action that automates the installation and configuration of BEAM‑based runtimes (Erlang, Elixir, Gleam, etc.) for CI/CD pipelines. By handling version selection, dependency caching, and environment setup, it eliminates the repetitive manual steps developers normally perform when preparing a workflow for BEAM languages.

**Value**  
- **Time‑saving** – No more ad‑hoc scripts to download and compile the correct runtime version; the action does it in a single step.  
- **Consistency** – Guarantees that every workflow run uses the exact same BEAM version and toolchain, reducing “works on my machine” failures.  
- **Extensibility** – Supports multiple BEAM languages, making it a one‑stop solution for polyglot projects that blend Erlang, Elixir, Gleam, etc.

**Practical Adoption Path**  

| Step | Action |
|------|--------|
| 1️⃣ Evaluate | Clone a minimal repo and add `uses: erlef/setup-beam@vX` to a test workflow. Verify that the desired BEAM version is installed and that your build/test commands run successfully. |
| 2️⃣ Pin Versions | Lock the action to a specific release tag (e.g., `v1.2.3`) and specify exact runtime versions in the `with:` block to avoid accidental upgrades. |
| 3️⃣ Integrate Caching | Add the optional cache inputs (`cache: true`, `cache-dependency-path`) to speed up subsequent runs. |
| 4️⃣ Review Security | Scan the action’s source (JavaScript) for vulnerabilities and confirm that the maintained maintainers respond to security issues. |
| 5️⃣ Roll‑out | Replace existing custom scripts in your production pipelines with the action, monitoring the first few runs for any edge‑case failures. |

**Production Readiness**  
- **Maturity:** 449 ★, 85 forks, last update 2026‑06‑30 – indicates active maintenance but not a large ecosystem.  
- **Readiness Level:** *Medium* – suitable for prototypes, internal CI, or non‑critical services after a short validation period.  
- **Risks:** The metadata provides limited insight into integration nuances (e.g., how it interacts with other actions or custom toolchains). Conduct a pilot run to measure setup cost, confirm that caching works with your dependency manager, and ensure the action’s JavaScript runtime complies with your organization’s security policies.  

If those checks pass, `erlef/setup-beam` can be promoted to production CI pipelines with confidence, providing a repeatable, low‑maintenance BEAM environment.

### Русский

**erlef/setup-beam** — это GitHub Action, который автоматизирует настройку BEAM‑стека (Erlang, Elixir, Gleam и др.) в CI/CD‑конвейерах, избавляя от повторяющихся ручных шагов по установке и конфигурации окружения. Его обычно подключают в начале workflow, чтобы быстро получить готовый к использованию набор зависимостей и инструментов, что упрощает прототипирование и внутренние автоматизированные процессы. Проект имеет средний уровень готовности к production: достаточно стабилен для прототипов и внутренних пайплайнов, но требует предварительной проверки интеграции и контроля зависимостей перед использованием в критически важных системах.

### 中文

**项目简介（2‑3 句话）**  
`erlef/setup-beam` 是一个 GitHub Actions 官方插件，能够在工作流中一键安装并配置 BEAM 生态的运行时（Erlang、Elixir、Gleam 等），帮助开发者省去手动下载、编译和环境变量设置的繁琐步骤。

**价值**  
- **消除重复操作**：统一、可复用的步骤取代每个仓库里手写的安装脚本，降低人为错误。  
- **加速 CI/CD**：通过缓存和预编译的方式缩短构建时间，让测试、发布流程更快更可靠。  
- **统一标准**：团队可统一使用同一套 BEAM 版本和工具链，提升代码可移植性和协作效率。

**典型接入方式**  
1. 在 `.github/workflows/*.yml` 中添加步骤：  
   ```yaml
   - name: Set up BEAM
     uses: erlef/setup-beam@v1
     with:
       otp-version: '26.0'      # Erlang/OTP 版本
       elixir-version: '1.16'   # Elixir 版本（可选）
       gleam-version: '0.30'    # Gleam 版本（可选）
   ```  
2. 后续步骤直接使用 `mix`, `rebar3`, `gleam` 等命令，无需额外的安装或路径配置。  
3. 如需缓存编译产物，可配合 `actions/cache` 一起使用，以进一步提升速度。

**生产可用性**  
- **成熟度**：已有 449+ 星、85+ Fork，活跃维护至 2026‑06‑30，代码主要为 JavaScript，社区反馈良好。  
- **适用场景**：适合原型、内部 CI 流程以及对 BEAM 版本有统一需求的生产项目。  
- **注意事项**：元数据中集成提示较少，首次引入时建议在分支或测试工作流中验证：  
  - 检查所需的 OTP/Elixir/Gleam 版本是否被官方镜像完整提供。  
  - 确认缓存策略与项目的依赖锁文件（`mix.lock`、`rebar.lock` 等）匹配。  
- **风险**：若项目依赖自定义编译选项或私有镜像，可能需要额外的手动步骤；在正式环境部署前，请完成一次完整的 CI 运行验证。  

综上，`erlef/setup-beam` 在消除手工配置、提升 CI 效率方面价值突出，经过简单的测试验证后即可在生产流水线中安全使用。

## 🧭 Practical evaluation

**Value:** erlef/setup-beam helps remove repetitive manual operations from a workflow.

**Best use cases**

- remove manual work
- connect tools into repeatable flows
- schedule operational tasks

**Integration notes:** Needs manual inspection before adoption because integration signals are sparse in the discovered metadata.

**Production readiness:** Medium: useful for prototypes or internal workflows, with dependency and maintenance checks before production.

**Quality signals**

- 449 GitHub stars
- 85 forks
- updated 2026-06-30
- primary language: JavaScript

**Risks:** Integration path is not obvious from metadata; validate setup cost before committing.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 48/100 |
| stars | 56/100 |
| topics | 0/100 |
| outlook | 63/100 |
| quality | 59/100 |
| recency | 80/100 |
| adoption | 54/100 |
| production | 62/100 |
| usefulness | 58/100 |
| integration | 30/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 100/100 |

---

<sub>🔭 Discovered 2026-06-30 · [View on GitHub](https://github.com/erlef/setup-beam) · [← Back to Automation](./README.md)</sub>
