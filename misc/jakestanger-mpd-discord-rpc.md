# JakeStanger/mpd-discord-rpc

[![Stars](https://img.shields.io/github/stars/JakeStanger/mpd-discord-rpc?style=flat-square&color=yellow)](https://github.com/JakeStanger/mpd-discord-rpc/stargazers) [![Forks](https://img.shields.io/github/forks/JakeStanger/mpd-discord-rpc?style=flat-square&color=blue)](https://github.com/JakeStanger/mpd-discord-rpc/network) [![Language](https://img.shields.io/badge/lang-Rust-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-55%2F100-brightgreen?style=flat-square)](#)

> Rust application which displays your currently playing song / album / artist from MPD in Discord using Rich Presence.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 157 |
| 🍴 **Forks** | 25 |
| 💻 **Language** | Rust |
| 📈 **Score** | 55/100 |
| 🗓️ **Last push** | 2026-05-11 |
| 🔍 **Source** | github |

## 🏷️ Topics

`discord` `discord-rpc` `mopidy` `mpd` `music` `rpc` `rust`

## 🎯 Categories

Misc

## 📝 Summary

### English

**Summary**  
`JakeStanger/mpd-discord-rpc` is a small Rust utility that reads the currently playing track from a local MPD (Music Player Daemon) server and updates your Discord Rich Presence with the song, album and artist information. With 157 ★ on GitHub and recent commits (as of 2026‑05‑11), it works out‑of‑the‑box for anyone already running MPD and wanting a quick, community‑maintained Discord integration.

**Value**  
- **Zero‑cost visibility**: Turns any MPD‑based listening session into a live Discord status, useful for streamers, remote teams, or personal music sharing.  
- **Lightweight & self‑contained**: Written in Rust, the binary has minimal runtime dependencies and can be run on any platform that supports MPD and Discord.  
- **Open‑source flexibility**: The code is easy to fork or extend (e.g., add custom icons or extra metadata) without licensing hurdles.

**Practical adoption path**  
1. **Proof‑of‑concept** – Clone the repo, follow the short README to configure the MPD address and Discord client ID, and run the binary locally.  
2. **CI/CD validation** – Add a simple health‑check script to your deployment pipeline that verifies the binary starts and can connect to MPD; this confirms the integration cost is low.  
3. **Production rollout** – Package the binary (e.g., as a systemd service or Docker container) and enable it on the machines that host MPD. Adjust the configuration for any custom Rich Presence assets you want to display.

**Production readiness**  
The project sits at a **medium** readiness level: it is actively maintained and stable enough for prototypes or internal tools, but it lacks extensive documentation, automated tests, and a clearly defined upgrade path. Before deploying to production, perform a small pilot to confirm that the setup steps (installing Rust or pre‑built binaries, configuring Discord OAuth, handling MPD reconnections) meet your reliability standards, and consider pinning a specific release tag to avoid breaking changes. With those checks in place, the tool can be safely used in production environments that already rely on MPD.

### Русский

**JakeStanger/mpd-discord-rpc** – небольшое Rust‑приложение, которое синхронно выводит в Discord информацию о текущем треке, альбоме и исполнителе из MPD через Rich Presence. Подойдёт для прототипов или внутренних инструментов, где требуется мгновенно показывать музыкальное состояние в Discord (например, в игровых сообществах или в команде разработки). Проект имеет среднюю готовность к production: 157 звёзд, активные коммиты и поддержка Rust, но требует проверки установки, зависимости и уточнения интеграционного сценария перед масштабным развертыванием.

### 中文

**项目简介**  
`JakeStanger/mpd-discord-rpc` 是一款用 Rust 编写的轻量级工具，它能够读取本地 MPD（Music Player Daemon）的播放信息，并通过 Discord 的 Rich Presence 将当前歌曲、专辑或艺术家实时展示在用户的 Discord 个人资料中。

**价值**  
- **即时共享音乐状态**：让 Discord 好友在聊天时直接看到你正在听的音乐，提升社交互动体验。  
- **低资源占用**：Rust 本身的高效性能使得该程序对系统资源几乎没有负担，适合在服务器或低配机器上运行。  
- **开源可定制**：源码公开，社区可根据个人需求自行扩展或修改展示内容（如添加专辑封面、歌词链接等）。

**典型接入方式**  
1. **准备环境**  
   - 确保系统已安装 MPD 并正常运行。  
   - 安装 Rust 工具链（`rustup`）或直接下载已编译的二进制文件。  
2. **获取并编译**  
   ```bash
   git clone https://github.com/JakeStanger/mpd-discord-rpc.git
   cd mpd-discord-rpc
   cargo build --release
   ```
   编译产物位于 `target/release/mpd-discord-rpc`。  
3. **配置**  
   - 在项目根目录创建 `config.toml`（或使用默认），内容示例：  
     ```toml
     [mpd]
     host = "127.0.0.1"
     port = 6600

     [discord]
     client_id = "YOUR_DISCORD_APP_CLIENT_ID"
     ```
   - 通过 Discord 开发者门户创建一个 “Rich Presence” 应用，获取 `client_id`。  
4. **运行**  
   ```bash
   ./target/release/mpd-discord-rpc
   ```
   程序会持续监听 MPD 状态并实时推送到 Discord。可使用 systemd、supervisord 等进程管理工具实现后台守护。

**生产可用性**  
- **成熟度**：项目已有 157 ⭐、25 🍴，最近一次提交在 2026‑05‑11，活跃度尚可。  
- **依赖风险**：仅依赖 `mpd`、`discord-rpc` 两个核心库，Rust 生态成熟，升级冲突概率低。  
- **部署成本**：只需一行二进制或一次 `cargo build`，无需额外数据库或网络服务，适合作为内部或原型环境的快速集成。  
- **运维建议**：在生产环境中建议使用容器化（Docker）或 systemd 单元管理，并监控进程退出日志，以便及时捕获 MPD 连接失效或 Discord API 变更导致的异常。  

总体而言，`mpd-discord-rpc` 在功能明确、实现轻量的前提下，可在原型验证或内部工具链中直接投入使用；若要在面向大量用户的生产环境中部署，建议进行一次完整的容错测试并锁定依赖版本。

## 🧭 Practical evaluation

**Value:** JakeStanger/mpd-discord-rpc may be useful when its README and activity match a concrete workflow.

**Best use cases**

- Not enough metadata yet.

**Integration notes:** Looks feasible to evaluate, but integration should start with a small proof of concept and README check.

**Production readiness:** Medium: useful for prototypes or internal workflows, with dependency and maintenance checks before production.

**Quality signals**

- 157 GitHub stars
- 25 forks
- updated 2026-05-11
- primary language: Rust
- 7 topics

**Risks:** Integration path is not obvious from metadata; validate setup cost before committing.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 35/100 |
| stars | 47/100 |
| topics | 88/100 |
| outlook | 73/100 |
| quality | 73/100 |
| recency | 100/100 |
| adoption | 44/100 |
| production | 72/100 |
| usefulness | 42/100 |
| integration | 30/100 |
| sourceTrust | 100/100 |

---

<sub>🔭 Discovered 2026-05-11 · [View on GitHub](https://github.com/JakeStanger/mpd-discord-rpc) · [← Back to Misc](./README.md)</sub>
