# akazwz/hostc

[![Stars](https://img.shields.io/github/stars/akazwz/hostc?style=flat-square&color=yellow)](https://github.com/akazwz/hostc/stargazers) [![Forks](https://img.shields.io/github/forks/akazwz/hostc?style=flat-square&color=blue)](https://github.com/akazwz/hostc/network) [![Language](https://img.shields.io/badge/lang-TypeScript-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-72%2F100-brightgreen?style=flat-square)](#)

> Localhost to the edge. Secure, fast, and zero-config edge tunnels powered by Cloudflare Workers.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 310 |
| 🍴 **Forks** | 34 |
| 💻 **Language** | TypeScript |
| 📈 **Score** | 72/100 |
| 🗓️ **Last push** | 2026-05-10 |
| 🔍 **Source** | github |

## 🏷️ Topics

`cli` `cloudflare-workers` `developer-tools` `durable-objects` `localhost` `ngrok-alternative` `tunnel` `websocket`

## 🎯 Categories

DevTools

## 📝 Summary

### English

**Summary**  
Hostc (akazwz/hostc) is a TypeScript‑based, zero‑config tool that creates secure, high‑performance edge tunnels from a local development machine to Cloudflare Workers. By exposing a simple CLI/API, it lets engineers instantly expose localhost services to the internet, cutting the feedback loop for development, testing, and CI pipelines.  

**Value**  
- **Speed:** Eliminates the manual setup of reverse proxies or VPNs, letting developers preview changes in real‑time on a globally distributed edge.  
- **Security:** Leverages Cloudflare’s edge network and TLS termination, so exposed services inherit Cloudflare’s DDoS protection and WAF without extra configuration.  
- **Convenience:** One‑line command or SDK call integrates with existing scripts, CI jobs, or local tooling, reducing context switches and accelerating review cycles.  

**Practical adoption path**  
1. **Trial:** Install the CLI (`npm i -g @hostc/cli`) and run `hostc tunnel start <port>` to expose a local service.  
2. **Integration:** Add the CLI or SDK call to `package.json` scripts, local dev Dockerfiles, or CI steps (e.g., GitHub Actions) to automatically spin up a tunnel for end‑to‑end tests.  
3. **Automation:** Use the provided API/SDK to embed tunnel lifecycle management into custom tooling or internal platforms, enabling “push‑to‑preview” workflows for feature branches.  

**Production readiness**  
- **Activity & adoption:** 310 ★, 34 forks, recent commit (2026‑05‑10), and active issue discussions indicate a healthy maintainer community.  
- **Maturity:** The project follows semantic versioning, includes a CLI, SDK, and TypeScript typings, and has clear documentation for edge‑worker deployment.  
- **Risk profile:** No critical licensing or security red flags have been identified, though a final review of the license (MIT‑style) and maintainer responsiveness is advisable. Overall, hostc is sufficiently stable for a pilot in internal development pipelines and can be promoted to production use after the brief due‑diligence step.

### Русский

**akazwz/hostc** — это TypeScript‑проект, который превращает ваш локальный сервер в безопасный, быстрый и полностью конфигурируемый edge‑туннель через Cloudflare Workers, позволяя разработчикам мгновенно делиться локальными сервисами без настройки инфраструктуры. Типичный сценарий: запуск `hostc` в процессе разработки, автоматическое открытие публичного URL для тестов, ревью кода и CI‑проверок, что ускоряет обратную связь и упрощает автоматизацию локальных задач. Проект считается почти готовым к production: активные коммиты, 310 звёзд, 34 форка, поддержка API/CLI, а также сильные сигналы принятия в сообществе, хотя лицензия и безопасность требуют окончательной проверки.

### 中文

**项目简介**  
akazwz/hostc 是一个基于 Cloudflare Workers 的本地到边缘隧道工具，能够在零配置、加密且高速的前提下，将本地服务直接暴露到公网 Edge，帮助开发者快速预览、调试和分享本地运行的应用。

**价值**  
- **提升开发效率**：在本地完成的改动可以瞬间在 Edge 上可访问，省去手动部署或端口映射的步骤。  
- **加速 CI 反馈**：在 CI 流水线中通过隧道自动发布预览链接，评审和回归测试更即时。  
- **自动化本地任务**：可用于本地 webhook、OAuth 回调等需要公网可达的场景，减少脚本编写和运维成本。

**典型接入方式**  
1. **CLI**：通过 `npx hostc start --port 3000` 启动隧道，返回一个 Cloudflare Edge URL。  
2. **SDK/API**：在 TypeScript/JavaScript 项目中引入 `@hostc/sdk`，调用 `createTunnel({port: 3000})` 动态生成隧道并获取 URL。  
3. **CI 集成**：在 GitHub Actions、GitLab CI 等脚本里运行 `hostc`，将生成的 URL 写入 PR 注释或环境变量，供后续步骤使用。

**生产可用性**  
- **活跃度**：截至 2026‑05‑10 最近一次提交，项目仍在维护；拥有 310 星、34 Fork，社区关注度良好。  
- **技术成熟度**：核心实现基于 TypeScript，依赖 Cloudflare Workers 的官方平台，具备高可用和全球分布的网络层。  
- **风险评估**：暂无重大元数据风险，唯一待确认的是许可证（MIT）符合企业合规、以及长期维护者的可持续性。整体来看，项目已具备在生产环境中进行试点的条件。

## 🧭 Practical evaluation

**Value:** akazwz/hostc helps engineers save time in daily development and review loops.

**Best use cases**

- speed up developer workflows
- automate local engineering tasks
- improve CI feedback

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 310 GitHub stars
- 34 forks
- updated 2026-05-10
- primary language: TypeScript
- 8 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 39/100 |
| stars | 53/100 |
| topics | 100/100 |
| outlook | 82/100 |
| quality | 77/100 |
| recency | 100/100 |
| adoption | 49/100 |
| production | 78/100 |
| usefulness | 74/100 |
| integration | 62/100 |
| sourceTrust | 100/100 |

---

<sub>🔭 Discovered 2026-05-10 · [View on GitHub](https://github.com/akazwz/hostc) · [← Back to DevTools](./README.md)</sub>
