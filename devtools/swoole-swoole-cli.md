# swoole/swoole-cli

[![Stars](https://img.shields.io/github/stars/swoole/swoole-cli?style=flat-square&color=yellow)](https://github.com/swoole/swoole-cli/stargazers) [![Forks](https://img.shields.io/github/forks/swoole/swoole-cli?style=flat-square&color=blue)](https://github.com/swoole/swoole-cli/network) [![Language](https://img.shields.io/badge/lang-C-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-61%2F100-brightgreen?style=flat-square)](#)

> SWOOLE-CLI is a php binary distribution composed swoole & php-core & cli & fpm and mostly of common extensions.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 239 |
| 🍴 **Forks** | 43 |
| 💻 **Language** | C |
| 📈 **Score** | 61/100 |
| 🗓️ **Last push** | 2026-05-14 |
| 🔍 **Source** | github |

## 🏷️ Topics

`cli` `php` `swoole`

## 🎯 Categories

DevTools

## 📝 Summary

### English

**Brief Summary**  
SWOOLE‑CLI bundles a pre‑compiled PHP binary with the Swoole extension, core PHP, CLI, and FPM, plus a curated set of common extensions. It lets developers spin up a fully‑functional PHP + Swoole environment instantly, cutting the time spent on manual compilation and dependency management.

**Value**  
- **Speed up daily workflows** – No need to compile Swoole or install PHP extensions locally; the ready‑made binary lets engineers run, test, and benchmark code immediately.  
- **Consistent CI feedback** – Using the same binary in CI pipelines eliminates “works on my machine” discrepancies and accelerates feedback loops.  
- **Simplified automation** – Scripts and local tooling can rely on a predictable runtime, reducing the overhead of environment provisioning.

**Practical Adoption Path**  
1. **Proof‑of‑concept** – Clone the repo, run the provided README commands on a developer workstation, and verify that a simple Swoole script executes.  
2. **CI integration** – Add the binary to your CI image (e.g., as a Docker layer or a cached artifact) and replace existing PHP/Swoole install steps.  
3. **Team rollout** – Document the binary version, usage flags, and any required extensions; distribute via internal package manager or a shared script.  
4. **Feedback & iteration** – Collect any missing extensions or version mismatches, then adjust the build (fork if needed) before wider adoption.

**Production Readiness**  
- **Maturity**: Medium – suitable for prototypes, internal services, or non‑critical production workloads.  
- **Signals**: 239 ★, recent update (2026‑05‑14), modest fork count, primarily C code, and a small set of topics indicate an active but niche project.  
- **Risks**: License compliance, security posture of bundled extensions, and long‑term maintainer activity still need verification.  
- **Next steps**: Perform a security scan of the binary, confirm the license matches your policy, and set up a monitoring process for upstream updates before promoting to production‑critical services.

### Русский

SWOOLE‑CLI — это готовый PHP‑бинарник, объединяющий Swoole, ядро PHP, CLI и FPM с набором часто‑используемых расширений, что позволяет инженерам ускорить локальную разработку, автоматизировать рутинные задачи и получить более быстрый фидбэк в CI. Для внедрения рекомендуется начать с небольшого proof‑of‑concept, проверив README и совместимость с текущим стеком, а затем постепенно интегрировать в пайплайны. Проект имеет средний уровень готовности к продакшну: подходит для прототипов и внутренних сервисов, но требует проверки лицензии, безопасности и поддержки зависимостей перед масштабным использованием.

### 中文

**项目简介**  
SWOOLE‑CLI 是一个打包好的 PHP 二进制发行版，内置 Swoole、PHP‑Core、CLI、FPM 以及常用扩展，旨在为开发者提供“一键即用”的运行时环境。

**价值**  
- **提升开发效率**：统一的二进制包省去本地编译、扩展安装等繁琐步骤，开发、调试、代码审查循环更快。  
- **自动化本地任务**：可在 CI 本地模拟环境、脚本化执行常见运维任务，减少环境不一致导致的故障。  
- **加速原型与内部工具**：对需要高并发、协程特性的项目，直接使用 Swoole‑CLI 可快速验证概念。

**典型接入方式**  
1. **小范围验证**：在项目根目录添加 `README.md` 中的安装指令（如 `curl -L https://.../swoole-cli.tar.gz | tar -xz && ./swoole-cli php -v`），确认二进制能正常运行。  
2. **CI 集成**：在 CI 脚本（GitHub Actions、GitLab CI 等）中下载并缓存二进制，使用 `swoole-cli php` 代替系统 php 执行单元测试、静态分析或部署脚本。  
3. **本地开发**：将二进制路径加入 `$PATH`，所有终端直接使用 `php`、`php-fpm`、`php-cli` 命令，无需额外配置扩展。

**生产可用性**  
- **成熟度**：目前得分 61/100，GitHub 239 ⭐、43 🍴，最近一次更新为 2026‑05‑14，活跃度尚可。  
- **适用场景**：适合原型、内部工具或对 Swoole 高并发特性有需求的服务；在正式生产环境使用前，需要进行依赖锁定、二进制安全审计以及升级策略评估。  
- **风险**：许可证、长期维护者状态以及安全漏洞需进一步确认；若计划在关键业务中使用，建议先在预生产环境做完整的兼容性和性能测试。  

综上，swoole/swoole-cli 可显著缩短开发与 CI 环节的准备时间，适合作为快速验证或内部服务的运行时；在投入正式生产前，务必完成依赖审计和可靠性验证。

## 🧭 Practical evaluation

**Value:** swoole/swoole-cli helps engineers save time in daily development and review loops.

**Best use cases**

- speed up developer workflows
- automate local engineering tasks
- improve CI feedback

**Integration notes:** Looks feasible to evaluate, but integration should start with a small proof of concept and README check.

**Production readiness:** Medium: useful for prototypes or internal workflows, with dependency and maintenance checks before production.

**Quality signals**

- 239 GitHub stars
- 43 forks
- updated 2026-05-14
- primary language: C
- 3 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 41/100 |
| stars | 51/100 |
| topics | 38/100 |
| outlook | 72/100 |
| quality | 67/100 |
| recency | 100/100 |
| adoption | 48/100 |
| production | 72/100 |
| usefulness | 58/100 |
| integration | 46/100 |
| sourceTrust | 100/100 |

---

<sub>🔭 Discovered 2026-05-14 · [View on GitHub](https://github.com/swoole/swoole-cli) · [← Back to DevTools](./README.md)</sub>
