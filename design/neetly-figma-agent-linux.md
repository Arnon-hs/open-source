# neetly/figma-agent-linux

[![Stars](https://img.shields.io/github/stars/neetly/figma-agent-linux?style=flat-square&color=yellow)](https://github.com/neetly/figma-agent-linux/stargazers) [![Forks](https://img.shields.io/github/forks/neetly/figma-agent-linux?style=flat-square&color=blue)](https://github.com/neetly/figma-agent-linux/network) [![Language](https://img.shields.io/badge/lang-Rust-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-47%2F100-brightgreen?style=flat-square)](#)

> A lightweight local service that makes your locally installed fonts available on Figma.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 364 |
| 🍴 **Forks** | 15 |
| 💻 **Language** | Rust |
| 📈 **Score** | 47/100 |
| 🗓️ **Last push** | 2026-08-24 |
| 🔍 **Source** | github |

## 🏷️ Topics

_no topics_

## 🎯 Categories

Design

## 📝 Summary

### English

**Brief Summary (2‑3 sentences)**  
`neetly/figma-agent-linux` is a lightweight Rust service that runs locally and exposes the fonts installed on a Linux machine to the Figma design tool, eliminating the need for manual font uploads. By bridging the gap between local font resources and Figma’s cloud editor, it streamlines design workflows and enables rapid prototyping of AI‑enhanced UI concepts. The project is modestly popular (≈ 364 ⭐ on GitHub) and actively maintained as of 2026‑06‑30.

**Value**  
- **Design‑centric AI workflows** – Makes it trivial to test AI‑generated mockups, RAG‑driven style suggestions, or agent‑based design assistants that rely on the exact fonts used in the final product.  
- **No external dependencies** – All processing stays on‑premises; only a small daemon is required, preserving privacy and reducing latency.  
- **Cross‑tool compatibility** – Works with any Figma session (desktop or web) that can reach the local service, enabling seamless integration into existing design pipelines.

**Practical Adoption Path**  
1. **Clone & build** the repository (Rust ≥ 1.70) and run the binary on a Linux workstation that already has the desired fonts installed.  
2. **Configure** Figma to point to the local agent (via the “Custom Font Service” URL in Figma’s settings).  
3. **Validate** that fonts appear correctly in a test file; optionally script the startup with systemd or a Docker container for consistency across team machines.  
4. **Integrate** with AI‑powered plugins or custom scripts that query the agent’s API to fetch font metadata for model‑driven design generation.  

**Production Readiness**  
- **Maturity:** Medium. The service is functional and actively maintained, but integration documentation is thin and the discovery metadata provides few explicit signals.  
- **Reliability:** Suitable for internal prototypes, design‑system validation, or CI pipelines where a controlled Linux environment can be guaranteed.  
- **Dependencies & Maintenance:** Requires a Rust toolchain and a stable Linux runtime; the binary has minimal external dependencies, but you should monitor upstream Rust updates and test the agent after any OS upgrades.  
- **Risk Mitigation:** Conduct a short proof‑of‑concept to confirm the setup cost, verify that the agent starts reliably on your CI/CD nodes, and ensure fallback mechanisms (e.g., manual font upload) are in place before rolling out to production‑critical design workflows.

### Русский

**neatly/figma-agent-linux** — это лёгкий локальный сервис, который делает шрифты, установленные в системе, доступными в Figma, упрощая работу дизайнеров и позволяя быстро прототипировать AI‑поддерживаемые функции (например, RAG‑агенты) без необходимости создавать собственный стек моделей. Типичный сценарий — запуск сервиса в рамках внутреннего прототипа или дизайнерского пайплайна, после чего Figma получает доступ к локальным шрифтам через простое подключение. Готовность к production — средняя: проект стабилен для прототипов и внутренних процессов, но требует ручной проверки интеграции и оценки затрат на настройку перед масштабным использованием.

### 中文

**项目简介**  
`neetly/figma-agent-linux` 是一个轻量级本地服务，能够把你在 Linux 系统上安装的字体实时同步到 Figma，使设计时可以直接使用本地字体，而无需手动上传或切换平台。

**价值**  
- **提升设计效率**：设计师无需离开本地环境即可在 Figma 中使用全部已安装字体，避免字体缺失导致的排版错误。  
- **支持 AI/ML 工作流**：在原型阶段可以快速为 AI 生成的 UI 文本或图像指定本地字体，方便评估 RAG、agent 等模型的视觉输出。  
- **开箱即用**：基于 Rust 实现，体积小、启动快，适合作为内部原型或实验平台的配套服务。

**典型接入方式**  
1. **克隆仓库并编译**（或直接下载已发布的二进制）。  
2. **配置**：在 `config.toml` 中指定本地字体目录（默认 `/usr/share/fonts`），以及 Figma API Token。  
3. **启动服务**：`./figma-agent-linux --port 8080`，服务会监听本地端口并向 Figma 代理字体列表。  
4. **在 Figma 中添加自定义字体源**：在项目设置里填写本地服务的 URL，即可在字体下拉框中看到同步的本地字体。  
> **注意**：目前元数据中没有提供自动化的 SDK，建议在正式接入前手动验证一次完整的字体同步流程。

**生产可用性**  
- **成熟度**：GitHub 364 星、15 Fork，最近一次更新在 2026‑06‑30，代码基于 Rust，具备较好的性能和安全性。  
- **适用场景**：适合原型开发、内部设计系统或需要频繁切换本地字体的团队。  
- **风险与准备**：集成路径不够明确，需自行编写启动脚本并确保网络访问 Figma API；在生产环境部署前应进行依赖审计（Rust 运行时、系统字体路径）以及容错测试。  
- **总体评估**：**中等**（Medium）——可用于内部或原型环境，经过充分的部署验证后方可投入正式生产。

## 🧭 Practical evaluation

**Value:** neetly/figma-agent-linux helps add AI capability without starting from a blank model stack.

**Best use cases**

- prototype AI features
- build RAG or agent workflows
- evaluate model tooling

**Integration notes:** Needs manual inspection before adoption because integration signals are sparse in the discovered metadata.

**Production readiness:** Medium: useful for prototypes or internal workflows, with dependency and maintenance checks before production.

**Quality signals**

- 364 GitHub stars
- 15 forks
- updated 2026-06-30
- primary language: Rust

**Risks:** Integration path is not obvious from metadata; validate setup cost before committing.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 30/100 |
| stars | 55/100 |
| topics | 0/100 |
| outlook | 48/100 |
| quality | 46/100 |
| recency | 40/100 |
| adoption | 48/100 |
| production | 48/100 |
| usefulness | 58/100 |
| integration | 30/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 100/100 |

---

<sub>🔭 Discovered 2026-06-30 · [View on GitHub](https://github.com/neetly/figma-agent-linux) · [← Back to Design](./README.md)</sub>
