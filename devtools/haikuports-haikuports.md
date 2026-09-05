# haikuports/haikuports

[![Stars](https://img.shields.io/github/stars/haikuports/haikuports?style=flat-square&color=yellow)](https://github.com/haikuports/haikuports/stargazers) [![Forks](https://img.shields.io/github/forks/haikuports/haikuports?style=flat-square&color=blue)](https://github.com/haikuports/haikuports/network) [![Language](https://img.shields.io/badge/lang-Shell-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-53%2F100-brightgreen?style=flat-square)](#)

> Software ports for the Haiku operating system.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 515 |
| 🍴 **Forks** | 361 |
| 💻 **Language** | Shell |
| 📈 **Score** | 53/100 |
| 🗓️ **Last push** | 2026-09-05 |
| 🔍 **Source** | github |

## 🏷️ Topics

`haiku` `haiku-os` `package-manager`

## 🎯 Categories

DevTools

## 📝 Summary

### English

**Brief summary (2‑3 sentences)**  
haikuports/haikuports is an open‑source collection of build scripts and packaging definitions that bring a wide range of third‑party software—including AI/ML tools—to the Haiku operating system. By providing ready‑made ports, it lets developers add AI capabilities to Haiku without having to start from scratch or maintain complex build chains. The repository is actively maintained (last update 2026‑06‑23) and has gathered a modest community (≈ 515 ★, 361 forks).  

**Value**  
- **Accelerates AI prototyping on Haiku** – you can quickly pull in libraries, frameworks, or utilities needed for RAG, agents, or other model‑driven workflows.  
- **Reduces engineering overhead** – the ports handle dependency resolution, compilation flags, and packaging, so you avoid reinventing the wheel for each component.  
- **Community‑backed** – the star/fork count shows a base of contributors who can help troubleshoot edge cases.

**Practical adoption path**  
1. **Clone the repository** and run the provided `haikuports` scripts to list available AI‑related ports.  
2. **Select the needed packages** (e.g., TensorFlow, PyTorch, or smaller inference runtimes) and install them via the Haiku package manager (`pkgman`).  
3. **Validate the installation** by running a small sanity‑check script (e.g., import the library in a Haiku shell and run a “Hello‑World” inference).  
4. **Integrate** the installed binaries into your project’s build pipeline or container, adjusting any environment variables the ports may require.  
5. **Iterate**: if a port fails to build, consult the `README` and issue tracker; the project’s modest size means you may need to patch or manually compile the problematic component.

**Production readiness**  
- **Readiness level: Medium** – the ports are stable enough for internal prototypes and limited production use, but they lack exhaustive CI/CD validation for every AI stack.  
- **Dependencies & maintenance** – verify that the versions of AI libraries match your model requirements and that any native dependencies (e.g., GPU drivers) are supported on Haiku.  
- **Risk mitigation** – perform a manual integration test before committing to a production rollout; keep an eye on upstream upstream changes, as the integration signals in the metadata are sparse.  

In short, haikuports/haikuports offers a convenient shortcut to bring AI tooling onto Haiku, suitable for experimentation and internal services, provided you allocate time for a one‑off validation and ongoing dependency checks before scaling to production.

### Русский

**haikuports/haikuports** — набор портов программного обеспечения для операционной системы Haiku, позволяющий быстро добавить готовые AI‑инструменты в проекты без необходимости собирать стек моделей с нуля. Типичный сценарий: разработчики используют репозиторий для прототипирования AI‑фич, построения RAG‑ или агентных воркфлоу, после чего проводят ручную проверку и адаптацию, поскольку метаданные дают ограниченную информацию о процессе интеграции. Готовность к продакшну — средняя: проект подходит для внутренних прототипов и небольших сервисов, но требует проверки зависимостей и дополнительного тестирования перед масштабным внедрением.

### 中文

**项目简介**  
haikuports/haikuports 是 Haiku 操作系统的官方软件移植仓库，提供数千个经过打包、编译和测试的第三方软件，使得在 Haiku 上快速获取常用工具和库成为可能。

**价值**  
- **即插即用**：无需自行编译源码，直接通过 `pkgman` 安装即可获得完整的依赖链，极大降低了在 Haiku 上部署新软件的门槛。  
- **加速原型开发**：对于需要 AI 能力的实验（如 RAG、Agent 工作流），可以直接在 Haiku 环境中拉取对应的 Python、TensorFlow、PyTorch 等包，省去从零构建堆栈的时间。  
- **社区维护**：超过 500 星、300+ Fork，活跃的社区会持续跟进上游更新，保证常用库的安全性和兼容性。

**典型接入方式**  
1. **安装 Port**：在 Haiku 终端执行 `pkgman install <package>`（例如 `pkgman install python3`、`pkgman install tensorflow`）。  
2. **手动审查**：因为元数据较为简略，建议在生产环境前检查生成的依赖列表和构建脚本，确认没有不必要或冲突的库。  
3. **本地镜像**：如需在离线或内部网络中使用，可使用 `pkgman create-repo` 将所需的 ports 导出为本地仓库，随后通过 `pkgman add-repo` 接入。

**生产可用性**  
- **成熟度**：Medium。仓库已稳定维护，适合作为原型或内部服务的基础设施。  
- **准备工作**：在正式上线前需进行依赖完整性检查、版本锁定以及安全审计，尤其是涉及 AI 框架的 GPU/CPU 兼容性。  
- **运维成本**：维护成本相对低，只需定期同步上游更新并测试关键组件即可。  

综上，haikuports 为在 Haiku 上快速引入 AI 及其他软件提供了便捷的入口，适合原型验证和受控的生产环境使用，只要在采纳前做好依赖审查和测试即可。

## 🧭 Practical evaluation

**Value:** haikuports/haikuports helps add AI capability without starting from a blank model stack.

**Best use cases**

- prototype AI features
- build RAG or agent workflows
- evaluate model tooling

**Integration notes:** Needs manual inspection before adoption because integration signals are sparse in the discovered metadata.

**Production readiness:** Medium: useful for prototypes or internal workflows, with dependency and maintenance checks before production.

**Quality signals**

- 515 GitHub stars
- 361 forks
- updated 2026-06-23
- primary language: Shell
- 3 topics

**Risks:** Integration path is not obvious from metadata; validate setup cost before committing.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 64/100 |
| stars | 58/100 |
| topics | 38/100 |
| outlook | 65/100 |
| quality | 67/100 |
| recency | 80/100 |
| adoption | 59/100 |
| production | 65/100 |
| usefulness | 42/100 |
| integration | 30/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 100/100 |

---

<sub>🔭 Discovered 2026-06-23 · [View on GitHub](https://github.com/haikuports/haikuports) · [← Back to DevTools](./README.md)</sub>
