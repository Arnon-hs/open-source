# shivammathur/homebrew-extensions

[![Stars](https://img.shields.io/github/stars/shivammathur/homebrew-extensions?style=flat-square&color=yellow)](https://github.com/shivammathur/homebrew-extensions/stargazers) [![Forks](https://img.shields.io/github/forks/shivammathur/homebrew-extensions?style=flat-square&color=blue)](https://github.com/shivammathur/homebrew-extensions/network) [![Language](https://img.shields.io/badge/lang-Ruby-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-56%2F100-brightgreen?style=flat-square)](#)

> Homebrew tap for PHP extensions :beers:

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 804 |
| 🍴 **Forks** | 48 |
| 💻 **Language** | Ruby |
| 📈 **Score** | 56/100 |
| 🗓️ **Last push** | 2026-09-05 |
| 🔍 **Source** | github |

## 🏷️ Topics

`amqp` `apcu` `grpc` `hacktoberfest` `homebrew` `homebrew-tap` `http` `igbinary` `imagick` `imap` `memcached` `msgpack`

## 🎯 Categories

Communication · Database

## 📝 Summary

### English

**Brief Summary (2‑3 sentences)**  
`shivammathur/homebrew-extensions` is a Homebrew tap that packages a wide range of PHP extensions, letting macOS and Linux developers install, upgrade, and manage them with a single `brew` command. It streamlines the setup of PHP environments for projects that need extra functionality—such as database drivers, caching, or image processing—without manually compiling extensions from source. The tap is actively maintained (last update 2026‑05‑12) and has attracted a solid community (≈ 800 ★, 48 forks).

**Value**  
- **Speed & consistency** – Installing extensions via Homebrew eliminates the “compile‑and‑install” steps that are error‑prone and time‑consuming, ensuring the same version across all team members and CI agents.  
- **Broad coverage** – The tap includes many commonly‑used extensions (e.g., `pdo_mysql`, `redis`, `imagick`), so teams can quickly add the capabilities they need for persistence, caching, or data transformation.  
- **Single source of truth** – All extensions are version‑pinned in the Homebrew formulae, making it easy to lock down a reproducible environment for development, testing, and staging.

**Practical Adoption Path**  
1. **Proof‑of‑concept** – Add the tap to a fresh development machine (`brew tap shivammathur/homebrew-extensions`) and install a single extension needed for a prototype (`brew install shivammathur/extensions/redis`). Verify that the extension loads in PHP (`php -m`).  
2. **Documentation audit** – Review the tap’s README and formulae for the specific extensions you plan to use; confirm any required system libraries (e.g., `libyaml`, `openssl`) are also satisfied.  
3. **CI integration** – Add the tap installation step to your CI pipeline (GitHub Actions, GitLab CI, etc.) and lock the Homebrew version to avoid unexpected upgrades.  
4. **Gradual rollout** – Replace manually‑compiled extensions in existing projects with the Homebrew equivalents, starting with low‑risk services (e.g., internal tools) before moving to production‑critical services.

**Production Readiness**  
- **Maturity**: Medium. The project is actively updated and widely starred, indicating community trust, but it is primarily aimed at developer convenience rather than enterprise‑grade lifecycle management.  
- **Risks**: The integration path isn’t documented in depth; you’ll need to verify that the tap’s formulae match the exact PHP version and OS architecture you run in production. Dependency drift (e.g., Homebrew core updates) can introduce breaking changes, so pinning versions is advisable.  
- **Recommendation**: Suitable for prototypes, internal services, and CI environments where rapid setup outweighs the need for formal support. For mission‑critical production workloads, perform a thorough dependency audit, lock formula versions, and consider a fallback plan (e.g., building extensions from source) before fully committing.

### Русский

**sh​ivammathur/homebrew-extensions** — это Homebrew‑tap, позволяющий быстро устанавливать и обновлять популярные расширения PHP (например, pdo_mysql, redis, xdebug) через привычный пакетный менеджер. Типичный сценарий — добавить tap в CI/CD или локальную среду, установить нужные расширения одной командой и сразу приступить к разработке или прототипированию приложений, требующих доступа к базе данных. Проект имеет средний уровень готовности к production: достаточный набор звёзд и активные обновления делают его подходящим для прототипов и внутренних сервисов, но перед выводом в продакшн стоит проверить совместимость зависимостей и оформить небольшое proof‑of‑concept, чтобы убедиться в простоте интеграции.

### 中文

**项目简介**  
`shivammathur/homebrew-extensions` 是一个 Homebrew tap，提供常用 PHP 扩展的二进制安装包，使用 Ruby 编写的 Formula，便于在 macOS/Linux 环境中一键装配所需的 PHP 扩展。

**价值**  
- **降低运维成本**：不必手动编译或解决依赖冲突，直接通过 `brew install` 获得预编译好的扩展。  
- **加速开发迭代**：团队可以快速为本地或 CI 环境补齐缺失的扩展，保持开发环境与生产环境一致。  
- **统一管理**：所有扩展统一托管在同一个 tap 中，便于审计、版本锁定和批量升级。

**典型接入方式**  
1. **添加 tap**  
   ```bash
   brew tap shivammathur/homebrew-extensions
   ```
2. **安装所需扩展**（以 `redis` 为例）  
   ```bash
   brew install php@8.2-redis
   ```
3. **在 `php.ini` 中启用**（大多数 Formula 已自动创建 symlink，通常只需重启 PHP-FPM/CLI）  
   ```bash
   echo "extension=redis.so" >> $(php --ini | grep "Loaded Configuration" | awk '{print $4}')
   ```
4. **CI/CD 集成**  
   在 CI 脚本中加入上述两行，即可在每次构建时确保环境拥有相同的扩展版本。

**生产可用性**  
- **成熟度**：已有 800+ ⭐、48 个 fork，最近一次提交在 2026‑05‑12，活跃度良好。  
- **适用场景**：非常适合原型、内部工具或对扩展版本要求不极端严格的生产环境。  
- **风险与准备**：  
  - 依赖于 Homebrew 与系统库，需在部署机器上预装 Homebrew。  
  - 对于高可用或容器化部署，建议在 Dockerfile 中固定扩展版本或自行编译，以避免运行时因 tap 更新导致不可预期的版本变动。  
  - 在正式生产前进行小规模 POC，确认扩展与现有 PHP、Web 服务器（nginx、apache）兼容，并做好版本锁定（`brew pin`）和回滚策略。  

综上，`shivammathur/homebrew-extensions` 能显著简化 PHP 扩展的获取与管理，适合作为快速交付和内部平台的依赖来源；在生产环境使用时，只要做好版本锁定和依赖审查，即可达到中等可靠性要求。

## 🧭 Practical evaluation

**Value:** shivammathur/homebrew-extensions helps teams persist, query, and move data with less custom plumbing.

**Best use cases**

- manage persistence
- speed up data access
- prototype database-backed apps

**Integration notes:** Looks feasible to evaluate, but integration should start with a small proof of concept and README check.

**Production readiness:** Medium: useful for prototypes or internal workflows, with dependency and maintenance checks before production.

**Quality signals**

- 804 GitHub stars
- 48 forks
- updated 2026-05-12
- primary language: Ruby
- 20 topics

**Risks:** Integration path is not obvious from metadata; validate setup cost before committing.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 42/100 |
| stars | 62/100 |
| topics | 100/100 |
| outlook | 70/100 |
| quality | 75/100 |
| recency | 80/100 |
| adoption | 56/100 |
| production | 68/100 |
| usefulness | 42/100 |
| integration | 30/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 200/100 |

---

<sub>🔭 Discovered 2026-05-12 · [View on GitHub](https://github.com/shivammathur/homebrew-extensions) · [← Back to Communication](./README.md)</sub>
