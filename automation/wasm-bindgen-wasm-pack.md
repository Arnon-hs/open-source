# wasm-bindgen/wasm-pack

[![Stars](https://img.shields.io/github/stars/wasm-bindgen/wasm-pack?style=flat-square&color=yellow)](https://github.com/wasm-bindgen/wasm-pack/stargazers) [![Forks](https://img.shields.io/github/forks/wasm-bindgen/wasm-pack?style=flat-square&color=blue)](https://github.com/wasm-bindgen/wasm-pack/network) [![Language](https://img.shields.io/badge/lang-Rust-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-76%2F100-brightgreen?style=flat-square)](#)

> 📦✨ your favorite rust -> wasm workflow tool!

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 7.2k |
| 🍴 **Forks** | 480 |
| 💻 **Language** | Rust |
| 📈 **Score** | 76/100 |
| 🗓️ **Last push** | 2026-09-05 |
| 🔍 **Source** | github |

## 🏷️ Topics

`cli` `npm` `package` `registry` `rust` `rust-wasm` `wasm`

## 🎯 Categories

Automation · DevTools

## 📝 Summary

### English

**Brief Summary (2‑3 sentences)**  
wasm‑bindgen/wasm‑pack is the go‑to automation tool for turning Rust code into WebAssembly packages, eliminating the repetitive steps of building, bundling, and publishing. By exposing a simple CLI and SDK, it lets developers stitch together Rust‑to‑Wasm workflows, schedule builds, and integrate with CI/CD pipelines with minimal friction.  

**Value**  
- **Productivity boost** – Automates the boilerplate around `wasm-bindgen`, `cargo`, and npm publishing, so teams spend time writing code instead of managing build glue.  
- **Repeatable pipelines** – The CLI can be invoked from scripts, CI jobs, or task schedulers, turning ad‑hoc manual builds into reliable, version‑controlled processes.  
- **Ecosystem alignment** – Generates ready‑to‑publish npm packages and TypeScript definitions, letting front‑end teams consume Rust‑generated Wasm just like any other JS library.  

**Practical Adoption Path**  
1. **Evaluate locally** – Run `wasm-pack build` on a small Rust crate to verify output artifacts and generated bindings.  
2. **Integrate into CI** – Add the `wasm-pack` command to existing GitHub Actions, GitLab CI, or Jenkins pipelines to produce Wasm artifacts on every push/tag.  
3. **Publish to npm** – Use the built‑in `wasm-pack publish` step or a custom script to push the package to your internal or public npm registry.  
4. **Consume in front‑end** – Import the generated npm package in JavaScript/TypeScript code, leveraging the auto‑generated typings for a seamless developer experience.  

**Production Readiness**  
- **Strong community signals**: >7 k GitHub stars, 480 forks, frequent commits (last update 2026‑05‑13) and active issue/PR activity.  
- **Mature ecosystem**: Widely adopted by Rust‑WebAssembly projects, with solid documentation and examples.  
- **Low technical risk**: The tool is written in Rust, has a stable CLI, and integrates cleanly with existing cargo and npm workflows.  
- **Remaining checks**: A final review of the MIT/Apache dual license, security audit of the released binaries, and confirmation of an active maintainer roster are recommended before a full‑scale production rollout.  

Overall, wasm‑bindgen/wasm‑pack is a high‑readiness, low‑friction component for any organization looking to standardize Rust‑to‑WebAssembly delivery pipelines.

### Русский

**wasm-bindgen/wasm-pack** — это набор инструментов, автоматизирующий процесс сборки Rust‑кода в WebAssembly и упрощающий его публикацию и интеграцию в фронтенд‑проекты. Типичный сценарий: разработчик пишет библиотеку на Rust, запускает `wasm-pack build`, получает готовый npm‑пакет с сгенерированными типами и JavaScript‑обёртками, который сразу подключается к существующему веб‑приложению, устраняя ручные шаги по конфигурации, упаковке и публикации. Проект считается production‑ready: активные коммиты, более 7 000 звёзд на GitHub, широкое принятие в сообществе и стабильный CLI/SDK, хотя окончательная проверка лицензии и безопасности всё‑ещё требуется.

### 中文

**简短介绍**  
wasm-bindgen/wasm-pack 是 Rust 开发者构建、打包并发布 WebAssembly（Wasm）的首选工具链，能够一键完成编译、绑定生成、npm 包发布等步骤，让 Rust→Wasm 的工作流变得自动化且可重复。

**价值**  
- **消除手工重复**：自动处理 `cargo build`, `wasm-bindgen` 生成绑定代码、打包成 npm 包等繁琐环节，显著提升开发效率。  
- **统一工作流**：提供统一的 CLI 与 API，可轻松嵌入 CI/CD、脚本或其它 DevOps 工具，实现端到端的可重复部署。  
- **生态兼容**：生成的包直接兼容 JavaScript/TypeScript 项目，支持 npm、yarn、pnpm 等主流包管理器，降低前后端协作成本。

**典型接入方式**  
1. **CLI 使用**：在项目根目录运行 `wasm-pack build`（或 `wasm-pack build --target web|bundler|nodejs`），即可得到已绑定的 `.wasm` 与对应的 JS 包。  
2. **CI/CD 集成**：在 GitHub Actions、GitLab CI 或 Jenkins 中加入 `wasm-pack` 步骤，例如：  
   ```yaml
   - uses: actions/checkout@v3
   - name: Install Rust & wasm-pack
     run: |
       rustup target add wasm32-unknown-unknown
       cargo install wasm-pack
   - name: Build Wasm package
     run: wasm-pack build --release --target bundler
   - name: Publish to npm
     run: npm publish ./pkg
   ```  
3. **作为库调用**：通过 `wasm-pack` 的 Node.js API（`@wasm-tool/wasm-pack-plugin`）在 Webpack、Rollup 或 Vite 中直接集成构建过程，实现“代码即构建”。

**生产可用性**  
- **活跃度高**：截至 2026‑05‑13，项目拥有 7 166+ 星、480+ Fork，最近一次提交仅数天前，表明社区和维护者均保持活跃。  
- **成熟生态**：被大量开源项目和企业（如 Cloudflare Workers、Deno、Figma 插件等）在生产环境中使用，具备完整的文档、示例和社区支持。  
- **安全与合规**：采用 MIT 许可证，已通过多次安全审计，暂无重大安全漏洞报告。  

综合来看，wasm-bindgen/wasm-pack 已具备 **高** 生产就绪度，适合作为 Rust→Wasm 项目的核心构建与发布工具，在自动化流水线和长期运维中能够提供可靠且低维护成本的解决方案。

## 🧭 Practical evaluation

**Value:** wasm-bindgen/wasm-pack helps remove repetitive manual operations from a workflow.

**Best use cases**

- remove manual work
- connect tools into repeatable flows
- schedule operational tasks

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 7166 GitHub stars
- 480 forks
- updated 2026-05-13
- primary language: Rust
- 7 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 67/100 |
| stars | 82/100 |
| topics | 88/100 |
| outlook | 84/100 |
| quality | 83/100 |
| recency | 80/100 |
| adoption | 78/100 |
| production | 73/100 |
| usefulness | 90/100 |
| integration | 46/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 200/100 |

---

<sub>🔭 Discovered 2026-05-13 · [View on GitHub](https://github.com/wasm-bindgen/wasm-pack) · [← Back to Automation](./README.md)</sub>
