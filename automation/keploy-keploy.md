# keploy/keploy

[![Stars](https://img.shields.io/github/stars/keploy/keploy?style=flat-square&color=yellow)](https://github.com/keploy/keploy/stargazers) [![Forks](https://img.shields.io/github/forks/keploy/keploy?style=flat-square&color=blue)](https://github.com/keploy/keploy/network) [![Language](https://img.shields.io/badge/lang-Go-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-85%2F100-brightgreen?style=flat-square)](#)

> Open-source platform for creating safe, isolated production sandboxes for API, integration, and E2E testing.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 17.7k |
| 🍴 **Forks** | 2.2k |
| 💻 **Language** | Go |
| 📈 **Score** | 85/100 |
| 🗓️ **Last push** | 2026-09-05 |
| 🔍 **Source** | github |

## 🏷️ Topics

`agentic-ai` `ai-testing-tool` `api-testing` `code-quality` `mock` `mock-data-generator` `mock-framework` `test-automation` `test-automation-framework` `test-generation` `testing` `testing-library`

## 🎯 Categories

Automation · AI/ML · Backend · DevTools · Data

## 📝 Summary

### English

**Brief Summary**  
Keploy (keploy/keploy) is an open‑source platform that lets teams generate isolated, production‑like sandboxes for API, integration, and end‑to‑end testing. By automatically capturing real traffic and turning it into repeatable test suites, it removes the need for manual test‑case creation and enables reliable, automated testing pipelines.

**Value**  
- **Automation of repetitive work** – Keploy records live API calls and produces ready‑to‑run test scripts, cutting down the hours spent writing and maintaining test code.  
- **Consistent, production‑grade environments** – Sandboxes mirror the exact runtime configuration of your services, so tests run against realistic data and dependencies, reducing false positives/negatives.  
- **Extensible integration** – The platform offers an API/SDK/CLI, language metadata, and a rich set of topics, making it easy to plug into CI/CD pipelines, observability stacks, or custom tooling.

**Practical Adoption Path**  
1. **Pilot on a low‑risk service** – Clone the repo, run the Keploy CLI to capture traffic from a staging instance, and generate the first test suite.  
2. **Integrate with CI** – Add the Keploy CLI or SDK step to your build pipeline (GitHub Actions, GitLab CI, Jenkins, etc.) to automatically replay captured traffic on each commit.  
3. **Scale to multiple services** – Use the provided Go SDK or language‑agnostic API to centralise sandbox definitions, share them across teams, and schedule periodic re‑captures for evolving APIs.  
4. **Governance & monitoring** – Leverage Keploy’s metadata (e.g., API version, request/response schemas) to enforce contract testing and to audit test coverage over time.

**Production Readiness**  
- **Strong community signals**: 17 735 GitHub stars, 2 249 forks, active commits (latest 2026‑06‑22), and a vibrant Go ecosystem (14 topics).  
- **Mature codebase**: Regular releases, clear CLI/SDK interfaces, and well‑documented sandbox generation workflow.  
- **Adoption evidence**: Multiple downstream projects reference Keploy for CI/CD automation, indicating real‑world usage.  
- **Risk considerations**: License compliance, security audit of dependencies, and confirmation of an active maintainer team should be completed before a full production rollout, but no major red flags are currently evident.

Overall, Keploy is a high‑readiness OSS candidate for teams seeking to eliminate manual test creation and to run reliable, production‑mirrored test suites at scale.

### Русский

keploy — это открытая платформа, позволяющая автоматически создавать изолированные «песочницы» продакшн‑окружения для API, интеграционных и end‑to‑end тестов, тем самым устраняя повторяющиеся ручные операции в CI/CD‑процессе. Типичный сценарий: разработчик подключает keploy через API/SDK/CLI, генерирует тестовые сценарии из реального трафика, интегрирует их в пайплайн и планирует периодический запуск, получая надёжную проверку без риска воздействия на продакшн. Проект имеет высокую готовность к production: активные обновления, более 17 k звёзд на GitHub, широкое принятие в сообществе и зрелую экосистему, что делает его надёжным кандидатом для пилотного внедрения.

### 中文

**简短介绍**  
keploy（keploy/keploy）是一款开源平台，能够为 API、集成和端到端（E2E）测试创建安全、相互隔离的生产沙箱。它通过自动捕获和回放真实流量，帮助团队消除重复的手工操作，实现可重复、可靠的测试流水线。

**价值**  
- **降低重复劳动**：自动记录生产请求/响应并生成可直接复用的测试用例，省去手写脚本的时间。  
- **提升测试可靠性**：沙箱环境与生产环境高度一致，避免因环境差异导致的误报/漏报。  
- **加速交付**：可将 keploy 与 CI/CD、监控、告警等工具链无缝拼接，实现“一键回放”与持续回归测试。  

**典型接入方式**  
1. **SDK / API**：在业务代码中引入 keploy SDK（支持 Go、Java、Python、Node.js 等），在服务启动时初始化，keploy 会自动拦截 HTTP/gRPC 调用并记录。  
2. **CLI**：使用 `keploy record` 在本地或 CI 环境捕获流量，生成 `keploy.yml`/`keploy.json` 测试文件。  
3. **插件/集成**：通过官方提供的 Docker 镜像或 Kubernetes Operator，将 keploy 作为 side‑car 注入到微服务 Pod 中，实现无侵入式监控与回放。  
4. **与 CI/CD 对接**：在 GitHub Actions、GitLab CI、Jenkins 等流水线中加入 `keploy test` 步骤，自动执行回放并生成报告。  

**生产可用性**  
- **活跃社区**：17735 星、2249 叉，最近一次提交在 2026‑06‑22，表明项目仍在积极维护。  
- **技术成熟度**：核心实现基于 Go，提供完整的 API/SDK/CLI，已在多个企业级项目中实践。  
- **生态兼容**：支持 Docker、Kubernetes、CI/CD 常用工具，易于在现有 DevOps 流程中引入。  
- **风险提示**：仍需对许可证合规、潜在安全漏洞以及维护者响应速度进行最终评估，但整体信号表明 keploy 已具备在生产环境进行试点甚至全量使用的条件。

## 🧭 Practical evaluation

**Value:** keploy/keploy helps remove repetitive manual operations from a workflow.

**Best use cases**

- remove manual work
- connect tools into repeatable flows
- schedule operational tasks

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 17735 GitHub stars
- 2249 forks
- updated 2026-06-22
- primary language: Go
- 14 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 84/100 |
| stars | 90/100 |
| topics | 100/100 |
| outlook | 90/100 |
| quality | 90/100 |
| recency | 80/100 |
| adoption | 89/100 |
| production | 77/100 |
| usefulness | 100/100 |
| integration | 62/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 500/100 |

---

<sub>🔭 Discovered 2026-06-22 · [View on GitHub](https://github.com/keploy/keploy) · [← Back to Automation](./README.md)</sub>
