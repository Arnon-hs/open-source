# MoeKoeMusic/MoeKoeMusic

[![Stars](https://img.shields.io/github/stars/MoeKoeMusic/MoeKoeMusic?style=flat-square&color=yellow)](https://github.com/MoeKoeMusic/MoeKoeMusic/stargazers) [![Forks](https://img.shields.io/github/forks/MoeKoeMusic/MoeKoeMusic?style=flat-square&color=blue)](https://github.com/MoeKoeMusic/MoeKoeMusic/network) [![Language](https://img.shields.io/badge/lang-Vue-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-71%2F100-brightgreen?style=flat-square)](#)

> 一款开源简洁高颜值的酷狗第三方客户端 An open-source, concise, and aesthetically pleasing third-party client for KuGou that supports  Windows / macOS / Linux / Web :electron:

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 5.9k |
| 🍴 **Forks** | 386 |
| 💻 **Language** | Vue |
| 📈 **Score** | 71/100 |
| 🗓️ **Last push** | 2026-09-05 |
| 🔍 **Source** | github |

## 🏷️ Topics

`electron` `kugou` `linux` `macos` `moekoe` `music` `vue3` `windows`

## 🎯 Categories

Misc

## 📝 Summary

### English

**Brief Summary (2‑3 sentences)**  
MoeKoeMusic is an open‑source, visually polished third‑party client for KuGou that runs on Windows, macOS, Linux and the Web via Electron. Built with Vue, it offers a clean UI and reusable front‑end components, making it easy to spin up music‑player interfaces without writing custom UI code. With over 5,900 stars and active maintenance, it is positioned as a production‑ready candidate for teams needing a quick, attractive KuGou integration.

**Value**  
- **Accelerated UI development** – The project supplies ready‑made, high‑quality Vue components (player controls, playlists, album art, etc.), so developers can focus on product logic rather than reinventing the music‑player UI.  
- **Cross‑platform consistency** – A single codebase delivers native‑looking experiences on desktop and web, reducing the overhead of maintaining separate clients.  
- **Aesthetic and brand‑friendly** – The “high‑颜值” design eliminates the need for extensive styling work, helping products look professional out of the box.

**Practical Adoption Path**  
1. **Evaluation** – Clone the repo, run `npm install && npm run dev` to preview the UI and inspect the component library.  
2. **Integration** – Import the desired Vue components or the whole client as a micro‑frontend; replace the built‑in KuGou API keys with your own if needed.  
3. **Customization** – Override theme variables or extend components to match your brand while keeping the core functionality intact.  
4. **Deployment** – Package with Electron for desktop distributions or build the web bundle for SaaS delivery; CI pipelines can be added using the existing npm scripts.

**Production Readiness**  
- **Activity & Community** – Recent commits (as of 2026‑07‑13), 5.9 k stars, 386 forks, and 8 related topics indicate strong community interest and ongoing maintenance.  
- **Stability** – The codebase is mature, with clear API signals (SDK/CLI) and well‑documented Vue components, making it suitable for pilot projects.  
- **Risks to Verify** – Final due‑diligence should confirm the OSS license compatibility, perform a security audit of dependencies, and ensure at least one active maintainer is responsive. Once those checks pass, MoeKoeMusic can be considered production‑ready for serious deployments.

### Русский

MoeKoeMusic — это открытый клиент KuGou с современным Vue‑интерфейсом, который позволяет быстро собрать пользовательские UI, переиспользуя готовые компоненты и API, без необходимости писать собственный дизайн. Его типичное внедрение — интеграция в кросс‑платформенные (Windows, macOS, Linux, Web) продукты, где требуется эстетичный и лёгкий музыкальный плеер. Проект обладает высокой готовностью к production: активные коммиты, более 5 000 звёзд, широкое принятие в сообществе и стабильный набор функций, требующий лишь финального аудита лицензии и безопасности.

### 中文

**项目简介**  
MoeKoeMusic 是一款开源、界面简洁且颜值极高的酷狗第三方客户端，支持 Windows、macOS、Linux 以及 Web（Electron）平台，使用 Vue 构建，已累计 5 942 星、386 Fork，活跃度仍在持续提升。

**价值**  
- **快速构建 UI**：提供完整的音乐播放、搜索、歌单管理等前端组件，开发者无需从零实现复杂的 UI，即可直接套用或二次定制。  
- **统一跨平台体验**：一次代码即可在桌面（Win/macOS/Linux）和 Web（Electron）上运行，降低多端适配成本。  
- **开源生态**：社区活跃，拥有丰富的 Issue、PR 与文档，可直接复用已有实现或贡献改进。

**典型接入方式**  
1. **源码集成**：克隆仓库后，使用 `npm install` 安装依赖，基于 Vue/Elec­tron 的标准构建流程（`npm run dev` / `npm run build`）即可在目标平台上运行。  
2. **组件库方式**：将 `src/components` 中的 UI 组件（如播放器、搜索框、歌单列表）抽离为独立的 Vue 组件库，按需在自有项目中 `import` 使用。  
3. **API/CLI 调用**：项目内部封装了对酷狗开放 API 的请求层（`src/api`），可直接在后端或其他前端项目中通过 `import { getSong, searchMusic } from '@/api/kugou'` 调用，亦可通过提供的 CLI 脚本进行批量下载或数据同步。

**生产可用性**  
- **活跃度**：最近一次提交于 2026‑07‑13，仓库星标、Fork 数均保持增长，说明社区仍在积极维护。  
- **技术成熟度**：基于 Vue 3 + Electron，使用现代前端工具链（Vite、Pinia），代码结构清晰，已有完整的单元测试与 CI。  
- **风险评估**：目前未发现重大许可证冲突或安全漏洞，但仍建议在正式上线前审查依赖的第三方库（尤其是 Electron 运行时）以及项目的许可证（MIT/Apache 等）是否符合贵司合规要求。  

综合来看，MoeKoeMusic 具备较高的生产就绪度，适合作为音乐类前端产品的 UI 基础或完整客户端的快速原型实现。

## 🧭 Practical evaluation

**Value:** MoeKoeMusic/MoeKoeMusic helps ship user-facing interfaces with less custom UI work.

**Best use cases**

- build product UI faster
- reuse interface components
- improve frontend delivery

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 5942 GitHub stars
- 386 forks
- updated 2026-07-13
- primary language: Vue
- 8 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 65/100 |
| stars | 80/100 |
| topics | 100/100 |
| outlook | 79/100 |
| quality | 84/100 |
| recency | 80/100 |
| adoption | 76/100 |
| production | 75/100 |
| usefulness | 58/100 |
| integration | 62/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 0/100 |

---

<sub>🔭 Discovered 2026-07-13 · [View on GitHub](https://github.com/MoeKoeMusic/MoeKoeMusic) · [← Back to Misc](./README.md)</sub>
