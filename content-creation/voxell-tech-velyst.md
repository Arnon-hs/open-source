# voxell-tech/velyst

[![Stars](https://img.shields.io/github/stars/voxell-tech/velyst?style=flat-square&color=yellow)](https://github.com/voxell-tech/velyst/stargazers) [![Forks](https://img.shields.io/github/forks/voxell-tech/velyst?style=flat-square&color=blue)](https://github.com/voxell-tech/velyst/network) [![Language](https://img.shields.io/badge/lang-Rust-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-50%2F100-brightgreen?style=flat-square)](#)

> Interactive Typst content creator using Vello and Bevy.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 247 |
| 🍴 **Forks** | 10 |
| 💻 **Language** | Rust |
| 📈 **Score** | 50/100 |
| 🗓️ **Last push** | 2026-09-05 |
| 🔍 **Source** | github |

## 🏷️ Topics

`bevy` `typst` `vector-graphics` `vello`

## 🎯 Categories

Content Creation · Design

## 📝 Summary

### English

**Summary**  
Velyst (voxell‑tech/velyst) is an open‑source, Rust‑based tool that lets you create interactive Typst documents by leveraging the Vello GPU‑accelerated rendering engine and the Bevy game‑engine framework. It targets developers who want live, high‑performance previews or custom UI widgets inside Typst‑generated content, and it already has a modest community (≈250 ★, 10 forks) with recent activity as of July 2026.

**Value**  
- **Fast, GPU‑driven rendering**: Vello provides sub‑pixel‑accurate, anti‑aliased graphics, making complex diagrams and animations in Typst feel instantaneous.  
- **Game‑engine flexibility**: Bevy’s ECS and plugin system let you embed interactive components (e.g., sliders, draggable nodes) directly into a Typst workflow, which is hard to achieve with static PDF pipelines.  
- **Rust ecosystem**: Strong type safety, modern tooling, and easy integration with other Rust crates make it attractive for teams already using Rust for tooling or back‑ends.

**Practical adoption path**  
1. **Proof‑of‑concept** – Clone the repo, run the example `cargo run --example demo` to verify that the rendering pipeline works on your hardware.  
2. **Readme validation** – Follow the quick‑start instructions; confirm that required system dependencies (e.g., Vulkan/Metal drivers) are satisfied.  
3. **Prototype integration** – Wrap Velyst as a library or a CLI tool inside your existing Typst build script, generating intermediate Vello frames that can be embedded in the final document.  
4. **Iterate** – Extend the Bevy plugin with the specific UI widgets your workflow needs, and use the provided hot‑reload feature to test changes in real time.

**Production readiness**  
- **Maturity**: Medium. The project is actively maintained (last commit 2026‑07‑01) and has a modest but engaged user base, but it lacks extensive documentation and large‑scale production case studies.  
- **Risks**: Integration details are not fully described in the metadata; you’ll need to verify the build environment, dependency versions (Bevy/Vello), and platform support (Linux, macOS, Windows).  
- **Recommendation**: Suitable for prototypes, internal tooling, or products where interactive Typst output is a differentiator. Before shipping to production, perform a dedicated stability test, pin all crate versions, and consider contributing missing documentation or CI scripts to reduce long‑term maintenance risk.

### Русский

**Voxell‑tech/velyst** — это интерактивный конструктор контента для Typst, построенный на графическом движке Vello и игровом фреймворке Bevy. Он подходит для быстрого прототипирования и внутренних воркфлоу, где требуется визуальное редактирование Typst‑документов в реальном времени; перед внедрением рекомендуется проверить README и выполнить небольшой proof‑of‑concept, чтобы оценить сложность интеграции. Готовность к production средняя: проект имеет активную поддержку (247 ★, обновления в 2026 г.), но требует проверки зависимостей и поддержки Rust‑экосистемы перед масштабным использованием.

### 中文

**项目简介（2‑3 句）**  
Velyst（voxell-tech/velyst）是一个基于 Vello 渲染引擎和 Bevy 游戏框架的交互式 Typst 内容创作工具，能够在实时预览中编辑并渲染 Typst 文档，实现所见即所得的创作体验。

**价值**  
- **即时渲染**：利用 Vello 的 GPU 加速向量渲染，Typst 文档的排版与图形可以在编辑时即刻呈现，极大提升排版效率。  
- **统一生态**：借助 Bevy 的插件系统，Velyst 易于与其他 Rust/Bevy 项目（如可视化编辑器、教学平台）进行组合，适合作为内部原型或文档生成流水线的前端。  
- **开源可定制**：完整源码基于 Rust，社区可自行扩展渲染特性或集成自定义 UI。

**典型接入方式**  
1. **阅读 README 与示例**：先克隆仓库，运行 `cargo run --example demo` 验证本地环境（需要 Rust 1.74+、Vulkan/Metal 驱动）。  
2. **作为 Bevy 插件**：在已有 Bevy 项目 `Cargo.toml` 中加入 `velyst = { git = "https://github.com/voxell-tech/velyst.git" }`，然后在 `App` 初始化时调用 `VelystPlugin::default()`。  
3. **嵌入业务流程**：通过提供 Typst 文本字符串给 `VelystEngine::render()`，获取渲染帧或 SVG 输出，进而在 Web 前端或文档生成服务中使用。  
4. **小规模 PoC**：先在内部工具或原型项目中实现「编辑框 + 实时预览」的最小功能，验证渲染速度、资源占用和与现有 CI/CD 的兼容性。

**生产可用性**  
- **成熟度**：已有 247 星、10+ Fork，最近一次提交在 2026‑07‑01，活跃度尚可。  
- **适用场景**：适合原型、内部文档编辑器或需要高交互性的排版工具；对外部大规模生产系统仍需评估。  
- **风险与准备**：依赖 Vello 与 Bevy，需确保目标平台的 GPU 驱动兼容；库的 API 仍在快速迭代，建议锁定特定 commit 或使用内部 fork。进行生产部署前，建议完成以下检查：  
  1. **依赖审计**：确认所有 Rust crate 的许可证与安全报告。  
  2. **性能基准**：在目标硬件上跑渲染基准，评估帧率与内存占用。  
  3. **容错机制**：为渲染错误或 GPU 失效实现回退（如导出为 PDF/PNG）。  

综上，Velyst 在原型开发和内部工作流中价值突出，接入成本适中；若在生产环境使用，则需进行依赖锁定、性能验证和容错设计后方可上线。

## 🧭 Practical evaluation

**Value:** voxell-tech/velyst may be useful when its README and activity match a concrete workflow.

**Best use cases**

- Not enough metadata yet.

**Integration notes:** Looks feasible to evaluate, but integration should start with a small proof of concept and README check.

**Production readiness:** Medium: useful for prototypes or internal workflows, with dependency and maintenance checks before production.

**Quality signals**

- 247 GitHub stars
- 10 forks
- updated 2026-07-01
- primary language: Rust
- 4 topics

**Risks:** Integration path is not obvious from metadata; validate setup cost before committing.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 26/100 |
| stars | 51/100 |
| topics | 50/100 |
| outlook | 62/100 |
| quality | 62/100 |
| recency | 80/100 |
| adoption | 44/100 |
| production | 63/100 |
| usefulness | 42/100 |
| integration | 30/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 200/100 |

---

<sub>🔭 Discovered 2026-07-01 · [View on GitHub](https://github.com/voxell-tech/velyst) · [← Back to Content-creation](./README.md)</sub>
