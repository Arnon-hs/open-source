# lzwme/scoop-proxy-cn

[![Stars](https://img.shields.io/github/stars/lzwme/scoop-proxy-cn?style=flat-square&color=yellow)](https://github.com/lzwme/scoop-proxy-cn/stargazers) [![Forks](https://img.shields.io/github/forks/lzwme/scoop-proxy-cn?style=flat-square&color=blue)](https://github.com/lzwme/scoop-proxy-cn/network) [![Language](https://img.shields.io/badge/lang-templ-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-45%2F100-brightgreen?style=flat-square)](#)

> 适合中国大陆的 Scoop buckets 代理镜像库。从多个开源 bucket 仓库同步更新，包含应用 1.6w+。

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 400 |
| 🍴 **Forks** | 26 |
| 💻 **Language** | templ |
| 📈 **Score** | 45/100 |
| 🗓️ **Last push** | 2026-08-24 |
| 🔍 **Source** | github |

## 🏷️ Topics

`scoop` `scoop-apps` `scoop-bucket`

## 🎯 Categories

Misc

## 📝 Summary

### English

**Brief Summary**  
lzwme/scoop‑proxy‑cn is a community‑maintained mirror of popular Scoop bucket repositories tailored for users in mainland China. It synchronises more than 16 000 applications from multiple upstream buckets, providing faster, locally‑cached downloads behind the Great Firewall.

**Value**  
The project solves the chronic latency and reliability problems that Chinese developers face when using the default Scoop buckets, which are hosted on GitHub and other overseas CDNs. By routing Scoop’s package manifests and installers through a China‑based proxy, it reduces download times, lowers failure rates, and avoids occasional network blocks, making the Windows package manager practical for everyday use in that region.

**Practical Adoption Path**  

| Step | Action | Reason |
|------|--------|--------|
| 1️⃣ | **Inspect the repository** – clone the repo, read the README, and verify the list of mirrored buckets matches the tools you need. | Confirms relevance to your workflow. |
| 2️⃣ | **Add the proxy bucket** – run `scoop bucket add proxy-cn https://github.com/lzwme/scoop-proxy-cn` (or the provided URL). | Simple CLI integration; no code changes required. |
| 3️⃣ | **Test a few packages** – install a common app (e.g., `scoop install 7zip`) and compare download speed and success rate against the default bucket. | Validates the performance benefit. |
| 4️⃣ | **Audit security** – review the bucket manifests for any unexpected modifications and optionally sign the bucket with your own GPG key. | Mitigates supply‑chain risk. |
| 5️⃣ | **Automate updates** – enable periodic `scoop update` or schedule a CI job to refresh the bucket if you rely on the latest versions. | Keeps the mirror in sync with upstream. |
| 6️⃣ | **Roll out internally** – document the new bucket URL in your internal developer onboarding guide and add it to any container images or VM images you ship. | Ensures consistent usage across the team. |

**Production Readiness**  
- **Maturity:** The repository has ~400 stars, 26 forks, and recent activity (last commit 2026‑06‑29), indicating an active maintainer.  
- **Stability:** As a mirror, it inherits the stability of the upstream Scoop buckets; the main risk is synchronization lag or occasional breakage if upstream bucket structures change.  
- **Risk Level:** Medium. The integration path is straightforward, but because the bucket is community‑driven, you should verify critical packages and consider pinning versions for production services.  
- **Recommendation:** Suitable for prototypes, internal developer workstations, or CI agents in China after a short validation period. For high‑availability production pipelines, pair the mirror with a fallback to the official bucket and implement monitoring of update failures.

### Русский

**lzwme/scoop-proxy-cn** — это открытый репозиторий‑прокси, предоставляющий зеркальные Scoop‑buckets, оптимизированные для доступа из КНР. Он автоматически синхронизирует более 16 000 приложений из популярных открытых bucket‑ов, что упрощает установку и обновление программ в корпоративных или экспериментальных средах, где прямой доступ к оригинальным репозиториям ограничен. Проект имеет средний уровень готовности – подходит для прототипов и внутренних процессов после проверки зависимости и настройки, но требует ручного аудита перед выводом в продакшн.

### 中文

**项目简介**  
lzwme/scoop‑proxy‑cn 是面向中国大陆用户的 Scoop **bucket 代理镜像**，自动同步多个官方与第三方 bucket，收录超过 1.6 万个常用 Windows 软件，解决国内网络访问慢、下载失败的问题。

**价值**  
- **加速下载**：所有 manifest 与安装包均通过国内 CDN 提供，下载速度比直接访问 GitHub 快 5‑10 倍。  
- **完整性**：定期从官方 bucket 拉取更新，保持与 upstream 同步，几乎不落后。  
- **省时省力**：企业或个人只需配置一次代理，即可在内部网络中统一使用，免去每台机器自行配置代理的繁琐。

**典型接入方式**  
1. **在本机或内部 CI 机器上安装 Scoop**（`iwr -useb get.scoop.sh | iex`）。  
2. **添加代理 bucket**：  
   ```powershell
   scoop bucket add proxy-cn https://github.com/lzwme/scoop-proxy-cn
   ```
3. **使用时指定 bucket**（或将其设为默认 bucket）：  
   ```powershell
   scoop install <package> -g   # -g 表示全局使用已添加的 bucket
   ```
   也可以在企业内部搭建私有镜像（Fork 本仓库并自行部署 CDN），只需把 `https://github.com/lzwme/scoop-proxy-cn` 换成内部地址即可。

**生产可用性**  
- **成熟度**：已获 400+ ⭐、26 次 fork，最近一次更新在 2026‑06‑29，活跃度良好。  
- **适用场景**：内部工具链、研发环境、自动化部署脚本等 **原型或内部使用** 均可直接采用。  
- **风险与注意事项**：  
  - 依赖外部 CDN，需确认公司网络对该 CDN 的访问策略。  
  - 由于项目主要提供镜像，若业务对 “零风险、全托管” 有严格要求，建议自行 fork 并在受控环境中运行，以便对更新进行审计。  
  - 目前项目的集成文档较少，接入前最好做一次手动验证（如安装几款常用软件）确认兼容性。  

综上，lzwme/scoop‑proxy‑cn 在国内提供了 **快速、完整且免配置的 Scoop 软件源**，适合作为研发内部的加速层；在正式生产环境使用时，只需做好 CDN 可达性检查和镜像审计，即可达到中等可靠性要求。

## 🧭 Practical evaluation

**Value:** lzwme/scoop-proxy-cn may be useful when its README and activity match a concrete workflow.

**Best use cases**

- Not enough metadata yet.

**Integration notes:** Needs manual inspection before adoption because integration signals are sparse in the discovered metadata.

**Production readiness:** Medium: useful for prototypes or internal workflows, with dependency and maintenance checks before production.

**Quality signals**

- 400 GitHub stars
- 26 forks
- updated 2026-06-29
- primary language: templ
- 3 topics

**Risks:** Integration path is not obvious from metadata; validate setup cost before committing.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 36/100 |
| stars | 55/100 |
| topics | 38/100 |
| outlook | 49/100 |
| quality | 53/100 |
| recency | 40/100 |
| adoption | 50/100 |
| production | 50/100 |
| usefulness | 42/100 |
| integration | 30/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 0/100 |

---

<sub>🔭 Discovered 2026-06-29 · [View on GitHub](https://github.com/lzwme/scoop-proxy-cn) · [← Back to Misc](./README.md)</sub>
