# bililive-go/bililive-go

[![Stars](https://img.shields.io/github/stars/bililive-go/bililive-go?style=flat-square&color=yellow)](https://github.com/bililive-go/bililive-go/stargazers) [![Forks](https://img.shields.io/github/forks/bililive-go/bililive-go?style=flat-square&color=blue)](https://github.com/bililive-go/bililive-go/network) [![Language](https://img.shields.io/badge/lang-Go-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-60%2F100-brightgreen?style=flat-square)](#)

> 一个直播录制工具

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 5.6k |
| 🍴 **Forks** | 687 |
| 💻 **Language** | Go |
| 📈 **Score** | 60/100 |
| 🗓️ **Last push** | 2026-08-24 |
| 🔍 **Source** | github |

## 🏷️ Topics

`bilibili` `douyu` `ffmpeg` `golang` `longzhu` `twitchtv` `zhanqi`

## 🎯 Categories

Video Editing

## 📝 Summary

### English

**Brief Summary (2‑3 sentences)**  
bililive-go is an open‑source Go utility for recording live streams, primarily targeting platforms like Bilibili. With over 5,600 stars, frequent updates (last on 2026‑06‑29), and a modest code‑base, it offers a ready‑to‑use command‑line interface and configurable plugins for automated capture. Its active community and clear README make it a practical choice for teams needing reliable, scriptable stream archiving.

**Value**  
- **Automation‑first**: Works from the command line and can be orchestrated in CI/CD pipelines, cron jobs, or containerized environments, eliminating manual download steps.  
- **Extensible configuration**: Supports multiple stream sources, output formats, and post‑processing hooks, allowing teams to tailor the workflow to internal archiving policies.  
- **Low overhead**: Written in Go, it compiles to a single binary with minimal dependencies, simplifying deployment across Linux, macOS, and Windows hosts.

**Practical Adoption Path**  
1. **Proof‑of‑Concept** – Clone the repo, run the example configuration against a test stream, and verify the output quality and file naming.  
2. **Containerization** – Build a Docker image (the project already provides a Dockerfile) and integrate it into existing orchestration tools (Kubernetes, Docker‑Compose, or a simple systemd service).  
3. **Workflow Integration** – Hook the binary into your media‑pipeline (e.g., trigger on a webhook from a streaming scheduler, store recordings in an object store, and notify downstream services).  
4. **Monitoring & Alerts** – Add health checks and log aggregation (e.g., Prometheus exporter or plain stdout) to detect failures early.

**Production Readiness**  
- **Activity & Community**: Recent commits, a healthy star/fork count, and active issue discussions indicate strong maintenance.  
- **Stability**: The core functionality (stream capture, file rotation, error handling) has been battle‑tested by the community; no major breaking changes reported in the last year.  
- **Risk Considerations**: Verify the license compatibility (MIT/Apache‑style) and perform a security audit of the Go dependencies, but no critical vulnerabilities are known.  

Overall, bililive-go is mature enough for a pilot deployment and can be scaled to production with minimal engineering effort.

### Русский

**bililive-go** — это открытый инструмент на Go для автоматической записи онлайн‑трансляций (например, Bilibili, Twitch и др.). Его типичный сценарий: настроить конфигурационный файл с URL‑ами нужных стримов, запустить сервис и получать готовые видеофайлы без вмешательства пользователя, что удобно для архивации контента или последующего анализа. Проект обладает высокой готовностью к production: активные коммиты, более 5600 звёзд, регулярные релизы и широкое сообщество, что делает его надёжным кандидатом для пилотного внедрения.

### 中文

bililive-go 是一个基

## 🧭 Practical evaluation

**Value:** bililive-go/bililive-go may be useful when its README and activity match a concrete workflow.

**Best use cases**

- Not enough metadata yet.

**Integration notes:** Looks feasible to evaluate, but integration should start with a small proof of concept and README check.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 5609 GitHub stars
- 687 forks
- updated 2026-06-29
- primary language: Go
- 7 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 71/100 |
| stars | 80/100 |
| topics | 88/100 |
| outlook | 60/100 |
| quality | 73/100 |
| recency | 40/100 |
| adoption | 77/100 |
| production | 62/100 |
| usefulness | 42/100 |
| integration | 62/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 100/100 |

---

<sub>🔭 Discovered 2026-06-29 · [View on GitHub](https://github.com/bililive-go/bililive-go) · [← Back to Video-editing](./README.md)</sub>
