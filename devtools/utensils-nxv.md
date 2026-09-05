# utensils/nxv

[![Stars](https://img.shields.io/github/stars/utensils/nxv?style=flat-square&color=yellow)](https://github.com/utensils/nxv/stargazers) [![Forks](https://img.shields.io/github/forks/utensils/nxv?style=flat-square&color=blue)](https://github.com/utensils/nxv/network) [![Language](https://img.shields.io/badge/lang-Rust-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-58%2F100-brightgreen?style=flat-square)](#)

> nxv — Nix Version Index. A blazingly fast CLI for finding any version of any Nix package.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 130 |
| 🍴 **Forks** | 1 |
| 💻 **Language** | Rust |
| 📈 **Score** | 58/100 |
| 🗓️ **Last push** | 2026-09-05 |
| 🔍 **Source** | github |

## 🏷️ Topics

`cli` `nix` `nixos` `nixpkgs` `package-manager` `rust` `sqlite` `version-search`

## 🎯 Categories

DevTools · Database

## 📝 Summary

### English

**Brief Summary**  
`utensils/nxv` is a Rust‑based command‑line tool that quickly looks up any version of any Nix package from the Nix Version Index. Its blazingly fast queries let developers retrieve exact package versions on the fly, making it ideal for speeding up local workflows, CI pipelines, and automated tooling.  

**Value**  
- **Time savings** – One‑line queries replace manual browsing of the Nixpkgs repository, cutting down the “find‑the‑right‑version” step in daily development and code‑review cycles.  
- **Workflow acceleration** – Scripts can call `nxv` to pin exact versions, generate lockfiles, or validate CI builds, leading to more deterministic builds and faster feedback loops.  
- **Low friction** – A single binary with a clear CLI interface integrates easily into existing shells, Makefiles, or CI configurations without additional runtime dependencies.  

**Practical Adoption Path**  
1. **Trial** – Install the binary (`cargo install nxv` or download a pre‑built release) and run a few exploratory commands (`nxv nixpkgs hello`) to verify lookup speed and output format.  
2. **Integration** – Wrap `nxv` in wrapper scripts or add it to your project's `devShell` so that developers can pin versions automatically (`VERSION=$(nxv nixpkgs rustc)`).  
3. **CI/CD** – Embed the command in CI steps that need to verify or lock package versions, e.g., generating a `versions.lock` file before a build.  
4. **Automation** – Use the CLI from higher‑level tooling (e.g., a Rust SDK or a small Python wrapper) to drive larger automation pipelines.  

**Production Readiness**  
- **Maturity**: Medium. The project has ~130 stars, recent activity (last update 2026‑06‑26), and a clean Rust codebase, making it suitable for prototypes, internal tooling, or as a “golden‑path” utility.  
- **Considerations before production**: Verify the licensing terms, perform a security audit of the binary, and assess the maintenance cadence (few contributors, limited forks). Adding a small internal wrapper that validates the output can mitigate any edge‑case bugs.  
- **Risk level**: Low to moderate; no major metadata issues, but final checks on license compliance and long‑term maintainer commitment are recommended before adopting it in mission‑critical pipelines.

### Русский

utensils/nxv — это быстрый CLI‑инструмент на Rust, позволяющий мгновенно находить любые версии пакетов Nix, что существенно ускоряет локальные задачи разработчиков и улучшает обратную связь в CI‑процессах. Его удобно интегрировать в ежедневные рабочие потоки (скрипты автоматизации, проверки зависимостей) благодаря простому API/CLI и ясной мета‑информации. Проект считается готовым к использованию в прототипах и внутренних сервисах (уровень готовности — Medium), однако перед выводом в продакшн рекомендуется проверить лицензию, безопасность и наличие активных мейнтейнеров.

### 中文

**项目简介**  
utensils/nxv（Nix Version Index）是一款基于 Rust 实现的超高速 CLI 工具，能够在几毫秒内查找任意 Nix 包的所有可用版本。它帮助开发者在日常开发、代码审查以及 CI 流程中快速定位依赖版本，从而显著提升工作效率。

**价值**  
- **节省时间**：一键检索任意 Nix 包的历史和最新版本，避免手动翻阅文档或仓库。  
- **加速工作流**：在本地调试、脚本自动化、CI/CD 反馈等场景中快速获取版本信息，缩短迭代周期。  
- **提升可靠性**：统一的版本查询入口减少因版本不一致导致的构建或部署错误。

**典型接入方式**  
1. **CLI 直接使用**：在终端中执行 `nxv <package-name>` 即可得到版本列表，适合手动调试或脚本调用。  
2. **脚本/CI 集成**：将 `nxv` 作为子进程嵌入 Bash、Python、GitHub Actions、GitLab CI 等自动化脚本中，例如：  
   ```bash
   VERSION=$(nxv nixpkgs.hello | head -n1)
   echo "使用版本 $VERSION 构建镜像"
   ```  
3. **API/SDK 包装**：项目已提供标准的输出格式（JSON、plain），开发者可自行封装为内部 SDK，供其他工具或服务调用。  

**生产可用性**  
- **成熟度**：当前评分 61/100，适合原型、内部工具或非关键业务的生产环境。  
- **社区与维护**：已有 130+ 星，最近一次更新在 2026‑06‑26，使用 Rust 编写，代码质量较高。仍需确认许可证（MIT/Apache 等）以及安全审计结果。  
- **依赖风险**：项目本身依赖较少，但在生产环境使用前建议检查其与现有 Nix 版本的兼容性，并做好版本锁定。  

总体而言，utensils/nxv 是一款轻量且高效的 Nix 版本查询工具，适合快速提升开发与 CI 流程的响应速度；在完成许可证、持续维护和安全评估后，可安全投入生产环境使用。

## 🧭 Practical evaluation

**Value:** utensils/nxv helps engineers save time in daily development and review loops.

**Best use cases**

- speed up developer workflows
- automate local engineering tasks
- improve CI feedback

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** Medium: useful for prototypes or internal workflows, with dependency and maintenance checks before production.

**Quality signals**

- 130 GitHub stars
- 1 forks
- updated 2026-06-26
- primary language: Rust
- 8 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 8/100 |
| stars | 45/100 |
| topics | 100/100 |
| outlook | 68/100 |
| quality | 66/100 |
| recency | 80/100 |
| adoption | 35/100 |
| production | 66/100 |
| usefulness | 58/100 |
| integration | 46/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 200/100 |

---

<sub>🔭 Discovered 2026-06-26 · [View on GitHub](https://github.com/utensils/nxv) · [← Back to DevTools](./README.md)</sub>
