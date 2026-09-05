# marcopiovanello/yt-dlp-web-ui

[![Stars](https://img.shields.io/github/stars/marcopiovanello/yt-dlp-web-ui?style=flat-square&color=yellow)](https://github.com/marcopiovanello/yt-dlp-web-ui/stargazers) [![Forks](https://img.shields.io/github/forks/marcopiovanello/yt-dlp-web-ui?style=flat-square&color=blue)](https://github.com/marcopiovanello/yt-dlp-web-ui/network) [![Language](https://img.shields.io/badge/lang-Go-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-66%2F100-brightgreen?style=flat-square)](#)

> A terrible web ui and RPC server for yt-dlp. Designed to be self-hosted.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 2.5k |
| 🍴 **Forks** | 242 |
| 💻 **Language** | Go |
| 📈 **Score** | 66/100 |
| 🗓️ **Last push** | 2026-09-05 |
| 🔍 **Source** | github |

## 🏷️ Topics

`download-manager` `golang` `raspberrypi` `rpc-server` `self-hosted` `webui` `youtube-dl` `yt-dlp` `yt-dlp-rpc` `yt-dlp-wrapper`

## 🎯 Categories

Backend

## 📝 Summary

### English

**Summary**  
marcopiovanello/yt‑dlp‑web‑ui is a self‑hosted web UI and RPC server built in Go that wraps yt‑dlp, letting users control downloads through a browser‑based interface. With over 2 400 stars and recent commits, it offers ready‑made UI components that can speed up the delivery of user‑facing video‑download features.  

**Value**  
The project eliminates the need to design and code a custom front‑end for yt‑dlp, providing reusable components (playlist view, progress bars, job management) and a simple JSON‑RPC API that can be embedded in any Go‑based backend. This cuts development time, standardises the user experience, and lets teams focus on core product logic rather than UI plumbing.  

**Practical adoption path**  
1. **Proof‑of‑concept** – Clone the repo, run the provided Docker compose or binary, and verify basic download tasks against your own yt‑dlp installation.  
2. **Integration** – Replace the demo RPC endpoint with your internal service URL, adjust authentication (e.g., JWT or IP‑allowlist), and embed the UI in a sub‑path of your existing web app.  
3. **Customization** – Fork the repo to tweak styling or extend the RPC schema for additional yt‑dlp options, then redeploy via your CI/CD pipeline.  

**Production readiness**  
The project scores high on OSS maturity: recent activity (last commit 2026‑06‑29), strong community signals (2 490 stars, 242 forks), and a clean Go codebase with clear documentation. While the license and security posture still need a formal review, the overall health and active maintainers make it suitable for a serious pilot in production environments.

### Русский

marcopiovanello/yt-dlp-web-ui — это открытый веб‑интерфейс и RPC‑сервер для yt‑dlp, позволяющий быстро развернуть пользовательский UI без написания собственного фронтенда. При типовом внедрении проект удобно подключать в виде небольшого proof‑of‑concept: развернуть контейнер, настроить API‑ключи и сразу получить готовый интерфейс для загрузки и управления медиаконтентом. По оценке готовности к production проект находится на высоком уровне — активные коммиты, более 2400 звёзд, регулярные обновления и широкая экосистема, что делает его надёжным кандидатом для пилотного использования после финальной проверки лицензии и безопасности.

### 中文

**项目简介**  
marcopiovanello/yt-dlp-web-ui 是一个基于 Go 实现的轻量级 Web UI 与 RPC 服务器，专为自托管 yt‑dlp 下载器而生。界面虽简陋，却提供了即插即用的前端组件，让用户无需自行编写繁杂的 UI 即可管理下载任务。

**价值**  
- **快速交付**：复用现成的界面与 RPC 接口，显著缩短产品 UI 开发周期。  
- **统一管理**：通过网页即可查看、控制、调度 yt‑dlp，提升运维效率。  
- **开源生态**：拥有 2.5k+ 星、242 个 Fork，社区活跃，可直接借鉴或二次定制。

**典型接入方式**  
1. **部署服务**：使用 Docker 镜像或直接 `go run` 启动后端 RPC 与 Web UI。  
2. **配置 yt‑dlp**：在 `config.yaml` 中指定 yt‑dlp 可执行文件路径及默认参数。  
3. **小范围验证**：在本地或测试环境通过 README 中的示例请求调用 RPC，确认下载、进度回报等功能正常。  
4. **前端集成**：如需在已有平台嵌入，可通过 iframe 引入 UI，或直接调用公开的 JSON‑RPC 接口进行二次开发。

**生产可用性**  
- **活跃度**：最近一次提交在 2026‑06‑29，代码维护频繁，Issue 响应及时。  
- **成熟度**：具备完整的 Docker 部署方案、健康检查与日志输出，已在多个开源项目中实际使用。  
- **风险**：需进一步审查许可证兼容性、依赖安全（尤其是 yt‑dlp 本身）以及维护者的长期可用性。总体而言，已具备在内部或受控生产环境进行试点的条件。

## 🧭 Practical evaluation

**Value:** marcopiovanello/yt-dlp-web-ui helps ship user-facing interfaces with less custom UI work.

**Best use cases**

- build product UI faster
- reuse interface components
- improve frontend delivery

**Integration notes:** Looks feasible to evaluate, but integration should start with a small proof of concept and README check.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 2490 GitHub stars
- 242 forks
- updated 2026-06-29
- primary language: Go
- 10 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 60/100 |
| stars | 72/100 |
| topics | 100/100 |
| outlook | 77/100 |
| quality | 81/100 |
| recency | 80/100 |
| adoption | 69/100 |
| production | 72/100 |
| usefulness | 58/100 |
| integration | 46/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 100/100 |

---

<sub>🔭 Discovered 2026-06-29 · [View on GitHub](https://github.com/marcopiovanello/yt-dlp-web-ui) · [← Back to Backend](./README.md)</sub>
