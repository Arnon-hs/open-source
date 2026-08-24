# thorvg/thorvg

[![Stars](https://img.shields.io/github/stars/thorvg/thorvg?style=flat-square&color=yellow)](https://github.com/thorvg/thorvg/stargazers) [![Forks](https://img.shields.io/github/forks/thorvg/thorvg?style=flat-square&color=blue)](https://github.com/thorvg/thorvg/network) [![Language](https://img.shields.io/badge/lang-C%2B%2B-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-61%2F100-brightgreen?style=flat-square)](#)

> A production-ready C++ vector graphics engine supporting SVG and Lottie formats, featuring advanced rendering backends such as WebGPU for high-performance graphics.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 1.7k |
| 🍴 **Forks** | 215 |
| 💻 **Language** | C++ |
| 📈 **Score** | 61/100 |
| 🗓️ **Last push** | 2026-07-06 |
| 🔍 **Source** | github |

## 🏷️ Topics

`animation` `drawing-library` `jpeg` `lottie` `opengl3` `opengles3` `otf` `path-drawing` `png` `rendering-engine` `shapes` `svg`

## 🎯 Categories

Backend · Database · Product

## 📝 Summary

### English

**Project Summary**

Thorvg is an open-source, production-ready C++ vector graphics engine that supports SVG and Lottie formats, offering high-performance rendering with advanced backends like WebGPU. This engine enables teams to reuse backend infrastructure, accelerating the development of API services and standardizing service patterns. By leveraging thorvg, teams can ship services faster and reduce the cost of rebuilding common backend components.

**Value Proposition**

The primary value proposition of thorvg lies in its ability to help teams reuse existing backend infrastructure, reducing the time and resources required to rebuild common components. This enables teams to focus on delivering high-quality services faster, while also standardizing service patterns across the organization.

**Practical Adoption Path**

To adopt thorvg, teams should start by evaluating its feasibility through a small proof of concept and carefully reviewing the project's README documentation. This will help identify potential integration challenges and validate the setup cost before committing to a larger-scale implementation. With thorvg's strong ecosystem signals and recent activity, teams can be confident in its production readiness.

**Production Readiness**

Thorvg is considered production-ready, with a high score for an open-source project. Its recent activity, adoption, and ecosystem signals demonstrate a strong foundation for a serious pilot. With 1669 GitHub stars, 215 forks, and

### Русский

**ThorVG** — это готовый к продакшену движок векторной графики на C++, поддерживающий SVG и Lottie и предлагающий высокопроизводительные бекэнды (в том числе WebGPU). Командам он позволяет быстро добавить мощный графический сервис, переиспользуя проверенную инфраструктуру вместо собственного построения рендеринга, что ускоряет выпуск API‑сервисов и стандартизирует паттерны работы. Проект имеет активную разработку, более 1600 звёзд и недавние коммиты, поэтому готов к пилотному внедрению, однако стоит начать с небольшого proof‑of‑concept и проверить процесс установки по README.

### 中文

**项目简介**  
thorvg 是一个面向生产环境的 C++ 向量图形引擎，原生支持 SVG 与 Lottie，并提供包括 WebGPU 在内的多种高性能渲染后端，能够在桌面、移动端乃至 Web 环境中实现流畅的矢量渲染。

**价值主张**  
- **统一图形基础设施**：团队无需自行实现 SVG/Lottie 解析与渲染，只需引入 thorvg 即可在所有业务系统中共享同一套向量渲染能力，降低重复开发成本。  
- **高性能、跨平台**：WebGPU、OpenGL、CPU 软件渲染等后端可根据目标平台自由切换，满足从低功耗嵌入式设备到高端服务器的不同性能需求。  
- **成熟生态**：超过 1.6k 星、200+ Fork，活跃的社区和持续更新（截至 2026‑07‑06），已在多款商业产品中验证，适合作为长期技术栈。

**典型接入方式**  
1. **快速验证**：克隆仓库，按照 README 中的 CMake 示例编译一个最小示例（`thorvg_example`），确认渲染后端（如 `-DTHORVG_BACKEND=webgpu`）能够在本机运行。  
2. **库集成**：在业务项目的 CMakeLists 中添加 `add_subdirectory(thorvg)`，或使用官方提供的 `install` 包通过 `find_package(thorvg REQUIRED)` 引入。随后在代码中创建 `tvg::SwCanvas`（CPU）或 `tvg::GlCanvas`/`tvg::WgCanvas`（GPU），加载 SVG/Lottie 并调用 `draw()`、`sync()` 完成渲染。  
3. **CI/CD 与包装**：将编译好的静态/动态库及依赖（WebGPU SDK、Vulkan/GL）打包进内部镜像，配合测试用例确保不同平台的渲染一致性。  

**生产可用性**  
- **活跃维护**：最近一次提交在 2026‑07‑06，社区每周都有 PR 与 Issue 交互，表明项目仍在积极迭代。  
- **成熟度**：已在多家企业级产品中用于实时动画与 UI 渲染，且拥有完整的文档、示例和跨平台 CI。  
- **风险点**：项目的部署脚本和后端切换方式在元数据中不够显式，建议在正式投入前完成一次小规模的 PoC（例如在一台测试服务器上跑 SVG 渲染），评估依赖（WebGPU runtime、GPU 驱动）以及构建成本。  

总体来看，thorvg 具备高生产就绪度，适合作为统一的向量图形服务层，帮助团队快速交付 API/渲染服务并统一后端图形处理模式。

## 🧭 Practical evaluation

**Value:** thorvg/thorvg helps teams reuse service infrastructure instead of rebuilding common backend pieces.

**Best use cases**

- ship API services faster
- reuse backend infrastructure
- standardize service patterns

**Integration notes:** Looks feasible to evaluate, but integration should start with a small proof of concept and README check.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 1669 GitHub stars
- 215 forks
- updated 2026-07-06
- primary language: C++
- 18 topics

**Risks:** Integration path is not obvious from metadata; validate setup cost before committing.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 58/100 |
| stars | 69/100 |
| topics | 100/100 |
| outlook | 80/100 |
| quality | 85/100 |
| recency | 100/100 |
| adoption | 66/100 |
| production | 76/100 |
| usefulness | 42/100 |
| integration | 30/100 |
| sourceTrust | 100/100 |

---

<sub>🔭 Discovered 2026-07-06 · [View on GitHub](https://github.com/thorvg/thorvg) · [← Back to Backend](./README.md)</sub>
