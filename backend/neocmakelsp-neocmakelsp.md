# neocmakelsp/neocmakelsp

[![Stars](https://img.shields.io/github/stars/neocmakelsp/neocmakelsp?style=flat-square&color=yellow)](https://github.com/neocmakelsp/neocmakelsp/stargazers) [![Forks](https://img.shields.io/github/forks/neocmakelsp/neocmakelsp?style=flat-square&color=blue)](https://github.com/neocmakelsp/neocmakelsp/network) [![Language](https://img.shields.io/badge/lang-Rust-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-43%2F100-brightgreen?style=flat-square)](#)

> Another CMake LSP

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 390 |
| 🍴 **Forks** | 35 |
| 💻 **Language** | Rust |
| 📈 **Score** | 43/100 |
| 🗓️ **Last push** | 2026-08-24 |
| 🔍 **Source** | github |

## 🏷️ Topics

`cmake` `lsp` `lsp-server` `rust`

## 🎯 Categories

Backend

## 📝 Summary

### English

**Brief Summary (2‑3 sentences)**  
*neocmakelsp* is an open‑source Language Server Protocol implementation for CMake, written in Rust. It provides IDE‑like features (completion, diagnostics, hover, etc.) for CMake scripts, helping developers work faster and more reliably with CMake‑based projects. With ~390 ★ on GitHub and active maintenance, it is a mature alternative to existing CMake LSPs.

**Value**  
- **Accelerates backend development** – By delivering immediate feedback while editing CMake files, teams can avoid costly configuration errors and ship API services more quickly.  
- **Promotes reuse and standardisation** – The same LSP can be adopted across all services in an organisation, ensuring a consistent CMake experience and reducing the need to maintain custom tooling.  
- **Low‑cost entry** – Being written in Rust, the server is lightweight, fast, and easy to compile for most platforms, making it suitable for both local developer machines and CI pipelines.

**Practical Adoption Path**  
1. **Proof‑of‑concept** – Clone the repo, run the provided `cargo build` or use the pre‑built binary, and point your editor (VS Code, Neovim, etc.) to the executable via the LSP client settings. Verify basic features (completion, diagnostics) on a small internal CMake project.  
2. **Documentation check** – Follow the README to configure the server, add a CI step that ensures the binary is available, and optionally package it as a Docker image for uniform deployment.  
3. **Pilot rollout** – Enable the LSP for a single service team, collect feedback on false‑positives or missing CMake constructs, and adjust the configuration (e.g., custom include paths).  
4. **Organisation‑wide rollout** – Publish the binary or Docker image to an internal artifact repository, update editor configuration templates, and add a health‑check in CI to confirm the LSP is reachable.

**Production Readiness**  
- **Maturity**: Medium. The project is actively maintained (last commit 2026‑05‑13), has a healthy star/fork count, and is written in a performant language, making it suitable for prototypes and internal workflows.  
- **Risks**: The integration steps are not fully documented in the metadata; teams should verify the build/installation process and test for any missing CMake features that are critical to their build system. Dependency management (Rust toolchain, binary distribution) and long‑term maintenance need to be assessed before committing to production use.  

Overall, *neocmakelsp* offers a solid, low‑overhead way to improve CMake authoring across a codebase, with a clear incremental adoption path and reasonable production readiness for internal services after a modest validation effort.

### Русский

**neocmakelsp** — это открытый LSP‑сервер для CMake, написанный на Rust, который позволяет командам быстро подключать готовую инфраструктуру анализа и автодополнения CMake‑скриптов, избавляясь от собственного написания и поддержки подобных инструментов. Типичный сценарий внедрения — запуск небольшого proof‑of‑concept в существующей IDE/CI, проверка работы через README и последующее добавление сервера в пайплайн разработки для ускорения создания и поддержки API‑сервисов. Проект имеет средний уровень готовности к продакшну: достаточное количество звёзд и форков, активные обновления, но требуется предварительная проверка зависимостей и поддерживаемости перед масштабным использованием.

### 中文

**项目简介**  
neocmakelsp 是一个用 Rust 编写的 CMake 语言服务器（LSP），为编辑器提供智能补全、跳转、诊断等功能，让 CMake 脚本的开发体验更接近现代语言。

**价值**  
- **提升开发效率**：通过 LSP 提供的实时语法检查、符号跳转和自动补全，减少手工调试和文档查找的时间。  
- **统一团队标准**：所有成员使用同一套 CMake 智能提示，避免因不同编辑器或插件导致的行为不一致。  
- **易于复用**：作为独立的后端服务，可在 CI/CD 流水线或代码审查工具中嵌入，统一检查 CMake 项目质量。

**典型接入方式**  
1. **编辑器插件**：在 VS Code、Neovim、Emacs 等支持 LSP 的编辑器中配置 `neocmakelsp` 的可执行文件路径，即可获得完整功能。  
2. **CI 集成**：在 CI 脚本（GitHub Actions、GitLab CI 等）中调用 `neocmakelsp --check <CMakeLists.txt>`，将诊断结果输出为报告或注释。  
3. **小型 PoC**：克隆仓库，运行 `cargo install --path .` 安装二进制；先在本地项目中打开一个 CMake 文件验证 LSP 是否正常工作，再根据 README 完成编辑器或 CI 的配置。

**生产可用性**  
- **成熟度**：已有 390+ 星、35+ Fork，活跃维护至 2026‑05‑13，代码基于 Rust，具备较好的性能和安全性。  
- **适用场景**：适合内部原型、研发团队的日常开发以及中小规模的 CI 检查。  
- **注意事项**：  
  - 需要自行评估与现有编辑器或 CI 环境的兼容性，尤其是 LSP 启动方式和端口管理。  
  - 在正式生产环境部署前，建议完成一次完整的集成验证（PoC），并检查依赖（Rust 运行时、Cargo 版本）以及后续维护成本。  

总体而言，neocmakelsp 在提升 CMake 开发体验和统一团队工作流方面具有明显价值，经过一次小范围验证后即可在内部项目中投入使用；若需在大规模生产环境中长期运行，则需进一步做好依赖管理和升级策略。

## 🧭 Practical evaluation

**Value:** neocmakelsp/neocmakelsp helps teams reuse service infrastructure instead of rebuilding common backend pieces.

**Best use cases**

- ship API services faster
- reuse backend infrastructure
- standardize service patterns

**Integration notes:** Looks feasible to evaluate, but integration should start with a small proof of concept and README check.

**Production readiness:** Medium: useful for prototypes or internal workflows, with dependency and maintenance checks before production.

**Quality signals**

- 390 GitHub stars
- 35 forks
- updated 2026-05-13
- primary language: Rust
- 4 topics

**Risks:** Integration path is not obvious from metadata; validate setup cost before committing.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 39/100 |
| stars | 55/100 |
| topics | 50/100 |
| outlook | 43/100 |
| quality | 50/100 |
| recency | 20/100 |
| adoption | 51/100 |
| production | 44/100 |
| usefulness | 42/100 |
| integration | 30/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 100/100 |

---

<sub>🔭 Discovered 2026-05-13 · [View on GitHub](https://github.com/neocmakelsp/neocmakelsp) · [← Back to Backend](./README.md)</sub>
