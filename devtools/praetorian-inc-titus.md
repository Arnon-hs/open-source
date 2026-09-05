# praetorian-inc/titus

[![Stars](https://img.shields.io/github/stars/praetorian-inc/titus?style=flat-square&color=yellow)](https://github.com/praetorian-inc/titus/stargazers) [![Forks](https://img.shields.io/github/forks/praetorian-inc/titus?style=flat-square&color=blue)](https://github.com/praetorian-inc/titus/network) [![Language](https://img.shields.io/badge/lang-Go-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-66%2F100-brightgreen?style=flat-square)](#)

> High-performance secrets scanner. CLI, Go library, Burp Suite extension, and Chrome extension. 487 detection rules with live credential validation.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 600 |
| 🍴 **Forks** | 64 |
| 💻 **Language** | Go |
| 📈 **Score** | 66/100 |
| 🗓️ **Last push** | 2026-09-05 |
| 🔍 **Source** | github |

## 🏷️ Topics

`appsec` `burp-suite-extension` `capability` `chrome-extension` `credential-scanner` `devsecops` `external-network-security` `go` `golang` `penetration-testing` `red-team` `secret-scanner`

## 🎯 Categories

DevTools · Security

## 📝 Summary

### English

**Brief Summary**  
praetorian‑inc/titus is a high‑performance secrets‑scanning toolkit written in Go that ships as a CLI, a Go library, a Burp Suite extension, and a Chrome extension. It ships with 487 detection rules and performs live credential validation, making it a comprehensive solution for finding hard‑coded secrets in code, binaries, and network traffic.

**Value Proposition**  
Titus lets development and security teams catch credential leaks early, reducing the risk of data breaches and the cost of remediation. Its multi‑modal delivery (CLI, SDK, Burp, Chrome) means it can be embedded directly into CI/CD pipelines, integrated into security testing tools, or used interactively by developers, eliminating the need to cobble together separate scanners.

**Practical Adoption Path**  

| Step | Action | Why it matters |
|------|--------|----------------|
| 1️⃣ Evaluate | Clone the repo and run `titus scan ./...` on a sample codebase. Verify detection rules and live validation against a test credential store. | Confirms rule coverage and false‑positive rate for your language stack. |
| 2️⃣ Integrate CI | Add a simple step in your pipeline (e.g., GitHub Actions, GitLab CI) that runs `titus scan` and fails on detections. | Provides automated, early‑stage secret detection with no manual effort. |
| 3️⃣ Extend via SDK | Import the Go library in internal tooling to scan artifacts produced by custom build steps (Docker images, compiled binaries). | Enables secret scanning beyond source code, covering build outputs. |
| 4️⃣ Harden Pen‑Testing | Deploy the Burp Suite and Chrome extensions for interactive testing of web applications and APIs. | Gives security teams a unified view of secrets exposed at runtime. |
| 5️⃣ Govern & Alert | Hook the CLI output into a SIEM or alerting system (e.g., Slack, PagerDuty). | Turns detections into actionable security incidents. |

**Production Readiness**  
- **Activity & Community**: 600 ★, 64 forks, last commit 2026‑06‑25, 14 relevant topics, and regular releases indicate an active maintainer base.  
- **Stability**: The core scanner is written in Go, a compiled language with strong concurrency support, and the CLI has proven performance in large codebases.  
- **Ecosystem Fit**: Works out‑of‑the‑box with common CI/CD tools and can be called from any environment that can execute a binary or import the Go module.  
- **Risk Considerations**: No major licensing or metadata red flags have been identified, but a final security audit of the repository and confirmation of active maintainers are recommended before enterprise‑wide rollout.  

Overall, Titus is mature enough for a pilot in production environments, with a clear, low‑friction path from evaluation to full integration.

### Русский

**praetorian-inc/titus** — это высокопроизводительный сканер секретов, предоставляющий CLI, Go‑библиотеку, а также расширения для Burp Suite и Chrome; в него включено 487 правил обнаружения с живой проверкой учётных данных. Его типичное применение — интеграция в процесс разработки UI, когда требуется быстро проверять и защищать пользовательские интерфейсы без написания собственного кода сканирования. Проект демонстрирует высокий уровень готовности к production: активные обновления, более 600 звёзд на GitHub, широкая экосистема (API/SDK/CLI), а также сильные сигналы принятия, что делает его надёжным кандидатом для серьёзного пилотного внедрения.

### 中文

**项目简介**  
praetorian‑inc/titus 是一款高性能的 secrets 扫描工具，提供 CLI、Go 库、Burp Suite 插件和 Chrome 扩展，内置 487 条检测规则并支持实时凭证验证。

**价值**  
- 自动发现代码、配置、网络请求等各类泄露的敏感信息，帮助团队在交付前把安全风险拦在入口。  
- 多端实现（CLI、SDK、浏览器、渗透测试插件），可在 CI/CD、开发本地环境、渗透测试以及浏览器调试中统一使用，降低重复建设成本。  
- 规则库持续更新并支持自定义，能够快速适配新业务场景，提升前端/后端交付的安全合规速度。

**典型接入方式**  
1. **CI/CD 流水线**：在构建脚本中调用 `titus scan`，将检测结果作为构建状态返回或生成报告。  
2. **Go 项目**：通过 `import "github.com/praetorian-inc/titus"` 调用库函数，在业务代码或内部工具中实现细粒度扫描。  
3. **Burp Suite**：在渗透测试时加载 Burp 插件，实时捕获并检测响应体中的泄露凭证。  
4. **Chrome 扩展**：前端开发者可在浏览器中直接审查页面请求/响应，快速定位潜在泄露。

**生产可用性**  
- **活跃度**：最近一次提交于 2026‑06‑25，星标 600+、Fork 64，社区活跃，具备持续维护的迹象。  
- **技术成熟度**：使用 Go 实现，性能优秀，规则库已覆盖常见凭证类型，且支持自定义扩展。  
- **安全与合规**：提供实时凭证验证，降低误报；开源许可证需进一步确认，但暂无明显风险。  
- **适配性**：提供标准化的 API/CLI/SDK，易于集成到现有 DevOps 流程和安全平台。  

综合来看，titus 已具备高可用的生产级特征，适合作为组织内部或云原生环境的 secrets 检测核心组件进行试点乃至全面部署。

## 🧭 Practical evaluation

**Value:** praetorian-inc/titus helps ship user-facing interfaces with less custom UI work.

**Best use cases**

- build product UI faster
- reuse interface components
- improve frontend delivery

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 600 GitHub stars
- 64 forks
- updated 2026-06-25
- primary language: Go
- 14 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 45/100 |
| stars | 59/100 |
| topics | 100/100 |
| outlook | 73/100 |
| quality | 75/100 |
| recency | 80/100 |
| adoption | 55/100 |
| production | 72/100 |
| usefulness | 58/100 |
| integration | 62/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 200/100 |

---

<sub>🔭 Discovered 2026-06-25 · [View on GitHub](https://github.com/praetorian-inc/titus) · [← Back to DevTools](./README.md)</sub>
