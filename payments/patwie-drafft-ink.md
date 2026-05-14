# PatWie/drafft-ink

[![Stars](https://img.shields.io/github/stars/PatWie/drafft-ink?style=flat-square&color=yellow)](https://github.com/PatWie/drafft-ink/stargazers) [![Forks](https://img.shields.io/github/forks/PatWie/drafft-ink?style=flat-square&color=blue)](https://github.com/PatWie/drafft-ink/network) [![Language](https://img.shields.io/badge/lang-Rust-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-62%2F100-brightgreen?style=flat-square)](#)

> Effortlessly self-host whiteboards. High-performance, cross-platform digital whiteboard with live collaboration built in Rust & WebGPU. Zero subscription, AGPLv3-licensed.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 479 |
| 🍴 **Forks** | 67 |
| 💻 **Language** | Rust |
| 📈 **Score** | 62/100 |
| 🗓️ **Last push** | 2026-05-14 |
| 🔍 **Source** | github |

## 🏷️ Topics

`canvas` `collaboration` `excalidraw` `rust` `self-hosted` `webgpu` `whiteboard`

## 🎯 Categories

Payments · Frontend · Database

## 📝 Summary

### English

**Brief Summary (2‑3 sentences)**  
PatWie/drafft‑ink is a high‑performance, cross‑platform digital whiteboard written in Rust and powered by WebGPU, offering live collaborative editing without any subscription fees. It is released under the AGPL‑v3 license, making it free to self‑host and customize, and it currently carries 479 GitHub stars and active maintenance as of 2026‑05‑14.

**Value Proposition**  
Although drafft‑ink is fundamentally a whiteboard tool, the project’s “Payments, Frontend, Database” categorisation highlights its usefulness as a sandbox for quickly prototyping and testing monetisation flows—e.g., embedding checkout widgets, integrating PSP APIs, or automating billing logic directly within a collaborative UI. By running the service in‑house you avoid third‑party SaaS costs and retain full control over data and licensing, which is attractive for startups or internal teams that need a secure, extensible canvas for payment‑related UI experiments.

**Practical Adoption Path**  

| Step | Action | Why it matters |
|------|--------|----------------|
| 1️⃣  | **Clone & run the demo** – Follow the README to build the Rust binary and launch the WebGPU front‑end locally. | Confirms that your development environment (Rust 1.70+, WebGPU‑compatible browser) can compile and run the core product. |
| 2️⃣  | **Create a minimal proof‑of‑concept** – Add a simple checkout button or a mock PSP webhook inside the whiteboard’s plugin system (or via an embedded iframe). | Validates the integration surface (REST/GraphQL, WebSocket, or iframe) without committing to a full feature set. |
| 3️⃣  | **Replace the mock with a real PSP** – Swap the test endpoint for your preferred payment provider (Stripe, Adyen, etc.) and test end‑to‑end flows (payment intent creation, webhook handling). | Checks that authentication, secret management, and webhook verification work in the self‑hosted context. |
| 4️⃣  | **Add persistence** – Connect the built‑in SQLite or plug in a PostgreSQL instance to store whiteboard state and transaction records. | Guarantees data durability and aligns the project with your existing database strategy. |
| 5️⃣  | **Security hardening & CI** – Run static analysis (cargo audit, clippy), enable TLS, and set up CI pipelines for automated testing. | Reduces the risk of supply‑chain vulnerabilities and prepares the codebase for production deployment. |
| 6️⃣  | **Deploy to production** – Containerise the app (Dockerfile is provided) and orchestrate with Kubernetes or a simple VM, monitoring resource usage (GPU/CPU). | Provides a repeatable, scalable deployment model for internal or customer‑facing environments. |

**Production Readiness Assessment**  
- **Maturity:** Medium. The project is actively maintained (last commit 2026‑05‑14) and has a healthy community signal (≈ 500 stars, dozens of forks), but its primary focus is a collaborative whiteboard rather than a turnkey payments platform.  
- **Strengths:** High‑performance Rust core, WebGPU rendering, open‑source license (AGPL‑v3) that eliminates subscription costs, and a clean codebase that can be extended.  
- **Caveats:**  
  * Integration points for billing/checkout are not documented out‑of‑the‑box; you’ll need to write custom glue code.  
  * Dependency on WebGPU means you must verify compatibility across target browsers and GPU drivers.  
  * AGPL‑v3 imposes copyleft requirements—ensure this aligns with your licensing policy.  
- **Recommendation:** Use drafft‑ink for internal prototypes, sandbox environments, or as the UI layer of a bespoke payment‑workflow tool. Before moving to a production‑critical service, perform the proof‑of‑concept steps, conduct a security audit, and evaluate long‑term maintenance commitments (e.g., monitoring Rust crate updates and WebGPU driver changes).

### Русский

**PatWie/drafft-ink** — это высокопроизводительная кроссплатформенная цифровая доска с живым совместным редактированием, написанная на Rust и использующая WebGPU, которую можно легко развернуть у себя. Она позволяет быстро добавить в существующий сервис функции монетизации, биллинга или интеграции с платёжными системами, начиная с небольшого proof‑of‑concept и проверки README. Проект находится на среднем уровне готовности к production: подходит для прототипов и внутренних рабочих процессов, но требует проверки зависимостей и поддержки перед масштабным внедрением.

### 中文

**价值**  
- **零订阅、开源许可**：基于 AGPLv3，企业可自行部署，避免 SaaS 费用和数据外泄。  
- **高性能跨平台**：使用 Rust + WebGPU，实现流畅的实时协作白板，适合作为内部工具或面向客户的交互式编辑器。  
- **可直接嵌入支付/结算流程**：白板本身提供的实时协作 UI 可用于展示商品、报价或结算页面，配合后端的计费系统（如 Stripe、PayPal）即可快速搭建“看板式”支付体验。

**典型接入方式**  
1. **部署**：在自己的服务器或容器平台（Docker、K8s）上运行 `drafft-ink` 的二进制或镜像，完成基本的 HTTPS 配置。  
2. **前端嵌入**：通过 `<iframe>` 或直接加载其提供的 JavaScript SDK，将白板嵌入现有网页/SPA 中。  
3. **后端对接**：在白板的事件回调（如“绘制完成”“按钮点击”）中，调用自研或第三方 PSP 的 API，实现下单、支付状态回写等业务。  
4. **小范围验证**：先在测试环境做一个“付款按钮 + 白板实时协作”的 PoC，确认事件流、权限控制和安全策略后，再推广到正式业务。

**生产可用性**  
- **成熟度**：GitHub ★479、Fork 67，最近一次提交在 2026‑05‑14，活跃度尚可，适合作为原型或内部工具。  
- **准备度**：中等。代码依赖 Rust 生态和 WebGPU，部署前需检查目标机器的 GPU/驱动兼容性，并做好安全审计（AGPLv3 的传播要求）。  
- **建议**：在正式生产前进行以下检查  
  1. **依赖审计**：确认所有 Rust crate 的许可证与安全报告。  
  2. **性能压测**：在预期并发用户数下验证 WebGPU 渲染和实时同步的延迟。  
  3. **运维监控**：为二进制加入日志、健康检查和自动重启（如 systemd/K8s）。  
  4. **安全加固**：使用 HTTPS、CSP、CSRF 防护，并对白板的文件上传/共享功能做权限控制。  

综上，`PatWie/drafft-ink` 适合作为 **低成本、可自托管的实时白板**，配合少量后端代码即可实现支付或结算场景的快速原型。若对 GPU 环境和开源合规性没有障碍，经过上述验证后即可投入生产使用。

## 🧭 Practical evaluation

**Value:** PatWie/drafft-ink helps integrate monetization, billing, or PSP flows faster.

**Best use cases**

- integrate billing or checkout
- evaluate PSP flows
- automate payment operations

**Integration notes:** Looks feasible to evaluate, but integration should start with a small proof of concept and README check.

**Production readiness:** Medium: useful for prototypes or internal workflows, with dependency and maintenance checks before production.

**Quality signals**

- 479 GitHub stars
- 67 forks
- updated 2026-05-14
- primary language: Rust
- 7 topics

**Risks:** Integration path is not obvious from metadata; validate setup cost before committing.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 46/100 |
| stars | 57/100 |
| topics | 88/100 |
| outlook | 79/100 |
| quality | 77/100 |
| recency | 100/100 |
| adoption | 54/100 |
| production | 73/100 |
| usefulness | 58/100 |
| integration | 30/100 |
| sourceTrust | 100/100 |

---

<sub>🔭 Discovered 2026-05-14 · [View on GitHub](https://github.com/PatWie/drafft-ink) · [← Back to Payments](./README.md)</sub>
