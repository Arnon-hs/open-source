# NOALBS/nginx-obs-automatic-low-bitrate-switching

[![Stars](https://img.shields.io/github/stars/NOALBS/nginx-obs-automatic-low-bitrate-switching?style=flat-square&color=yellow)](https://github.com/NOALBS/nginx-obs-automatic-low-bitrate-switching/stargazers) [![Forks](https://img.shields.io/github/forks/NOALBS/nginx-obs-automatic-low-bitrate-switching?style=flat-square&color=blue)](https://github.com/NOALBS/nginx-obs-automatic-low-bitrate-switching/network) [![Language](https://img.shields.io/badge/lang-Rust-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-56%2F100-brightgreen?style=flat-square)](#)

> Simple app to automatically switch scenes in OBS based on the current bitrate fetched from the ingest stats page.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 493 |
| 🍴 **Forks** | 110 |
| 💻 **Language** | Rust |
| 📈 **Score** | 56/100 |
| 🗓️ **Last push** | 2026-09-05 |
| 🔍 **Source** | github |

## 🏷️ Topics

`kick` `noalbs` `obs` `obs-switcher` `streaming` `switcher` `twitch` `twitch-bot`

## 🎯 Categories

Automation

## 📝 Summary

### English

**Brief summary**  
NOALBS/nginx‑obs‑automatic‑low‑bitrate‑switching is a small Rust utility that monitors the ingest‑statistics page of an NGINX‑RTMP server and automatically switches OBS scenes when the current stream bitrate drops below a configurable threshold. By handling this logic in real time, it eliminates the need for streamers to manually change scenes during low‑bitrate conditions.

**Value**  
The tool turns a repetitive, error‑prone manual step into an automated, repeatable action, letting broadcasters keep their production layout consistent even when network quality fluctuates. It is especially useful for anyone who runs a continuous live‑streaming workflow (e.g., gaming, webinars, or remote events) and wants to preserve a professional look without constant operator intervention.

**Practical adoption path**  
1. **Proof‑of‑concept** – Clone the repo, read the README, and run the binary in a test environment with a local NGINX‑RTMP instance and OBS to verify scene switching works as expected.  
2. **Configuration** – Define the bitrate threshold and map OBS scene names in the provided config file; adjust the NGINX stats endpoint if needed.  
3. **Integration** – Deploy the binary alongside your existing streaming stack (e.g., as a systemd service or Docker container) and point OBS to the same machine or network.  
4. **Validation** – Observe the behavior during simulated low‑bitrate events and fine‑tune thresholds before rolling out to production.

**Production readiness**  
The project scores a medium readiness level. It has solid community interest (≈ 500 ★, 110 forks) and recent updates (July 2026), but the integration steps are not fully documented, and the Rust dependency chain requires a review for long‑term maintenance. For internal prototypes or low‑risk streaming pipelines it can be adopted quickly after the PoC phase; for mission‑critical production streams, perform a dependency audit, add monitoring for the binary, and consider wrapping it in a container with version‑pinning to ensure stability before full deployment.

### Русский

Резюме:

NOALBS/nginx-obs-automatic-low-bitrate-switching - это простая приложение, которое автоматически переключает сцены в OBS на основе текущего битрейта, полученного из страницы статистики ингеста. Это позволяет сэкономить время и силы на удаление повторяющихся ручных операций из рабочего процесса. Проект готов к внедрению в прототипах или внутренних рабочих процессах, но требует проверки зависимостей и поддержки перед использованием в производстве.

### 中文

**简短介绍**
NOALBS/nginx-obs-automatic-low-bitrate-switching 是一个开源项目，旨在自动切换 OBS 视频流的场景，根据当前的比特率从 nginx  ingest 统计页面获取。这个项目可以帮助减少繁琐的重复操作，从而提高工作效率。

**价值**
NOALBS/nginx-obs-automatic-low-bitrate-switching 的价值在于，它可以自动化 OBS 视频流的场景切换，减少人工干预的次数，提高工作效率。

**典型接入方式**
接入 NOALBS/nginx-obs-automatic-low-bitrate-switching 可以通过以下步骤进行：

1. 检查 README 文件，了解项目的使用方法和集成指南。
2. 开始一个小的原型验证，测试项目的可用性和功能。
3. 根据项目的需求和您的系统环境，进行必要的配置和设置。

**生产可用性**
NOALBS/nginx-obs-automatic-low-bitrate-switching 的生产可用性为中等，适用于原型或内部工作流程。然而，需要注意以下几点：

* 依赖项和

## 🧭 Practical evaluation

**Value:** NOALBS/nginx-obs-automatic-low-bitrate-switching helps remove repetitive manual operations from a workflow.

**Best use cases**

- remove manual work
- connect tools into repeatable flows
- schedule operational tasks

**Integration notes:** Looks feasible to evaluate, but integration should start with a small proof of concept and README check.

**Production readiness:** Medium: useful for prototypes or internal workflows, with dependency and maintenance checks before production.

**Quality signals**

- 493 GitHub stars
- 110 forks
- updated 2026-07-06
- primary language: Rust
- 8 topics

**Risks:** Integration path is not obvious from metadata; validate setup cost before committing.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 51/100 |
| stars | 57/100 |
| topics | 100/100 |
| outlook | 70/100 |
| quality | 75/100 |
| recency | 80/100 |
| adoption | 56/100 |
| production | 68/100 |
| usefulness | 42/100 |
| integration | 30/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 100/100 |

---

<sub>🔭 Discovered 2026-07-06 · [View on GitHub](https://github.com/NOALBS/nginx-obs-automatic-low-bitrate-switching) · [← Back to Automation](./README.md)</sub>
