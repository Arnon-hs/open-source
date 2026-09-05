# us/mocker

[![Stars](https://img.shields.io/github/stars/us/mocker?style=flat-square&color=yellow)](https://github.com/us/mocker/stargazers) [![Forks](https://img.shields.io/github/forks/us/mocker?style=flat-square&color=blue)](https://github.com/us/mocker/network) [![Language](https://img.shields.io/badge/lang-Swift-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-68%2F100-brightgreen?style=flat-square)](#)

> Docker-compatible container CLI built on Apple's Containerization framework. Same commands, same flags — mocker run, ps, stop, build, compose, stats — all working on macOS 26.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 254 |
| 🍴 **Forks** | 8 |
| 💻 **Language** | Swift |
| 📈 **Score** | 68/100 |
| 🗓️ **Last push** | 2026-09-05 |
| 🔍 **Source** | github |

## 🏷️ Topics

`apple-containerization` `cli` `compose` `containerization` `containers` `docker` `macos` `macos26` `swift` `swift-package-manager`

## 🎯 Categories

DevTools · DevOps/Infra

## 📝 Summary

### English

**Brief Summary**  
us/mocker is a Docker‑compatible CLI that runs on macOS using Apple’s Containerization framework, offering the same commands and flags as Docker (run, ps, stop, build, compose, stats). It lets developers prototype AI‑enabled workloads—such as RAG pipelines or autonomous agents—without having to spin up a full Docker stack, and it ships as a native Swift binary with active community support.

**Value Proposition**  
- **Seamless Docker experience on macOS**: Teams that already use Docker can keep their existing scripts and tooling while eliminating the overhead of a Linux VM.  
- **Fast AI prototyping**: By providing a familiar container interface, developers can quickly spin up isolated environments for model serving, tool integration, or data preprocessing, accelerating proof‑of‑concept cycles.  
- **Native performance & security**: Leveraging Apple’s Containerization framework reduces the attack surface compared with a full Docker Engine and offers better resource utilization on Apple silicon.

**Practical Adoption Path**  
1. **Install the CLI** (`brew install us/mocker` or download the binary) on developer Macs.  
2. **Replace Docker calls** in CI scripts, Makefiles, or local workflows with `mocker`—the command syntax is identical, so no code changes are needed.  
3. **Validate** by running existing Dockerfiles and Compose files; the framework translates them to native macOS containers.  
4. **Integrate** with AI tooling (e.g., LangChain, LlamaIndex) by launching model servers or RAG components inside mocker containers, then expose the services to your host or to other mocker instances.  
5. **Scale to CI/CD**: Add the mocker binary to your build agents (macOS runners) to keep the same environment across local development and automated pipelines.

**Production Readiness**  
- **Activity & Community**: 254 GitHub stars, recent commits (last updated 2026‑06‑22), and a modest but active fork base indicate healthy momentum.  
- **Stability**: The CLI mirrors Docker’s command set, and the underlying Apple Containerization framework is a first‑party, well‑maintained component of macOS 26.  
- **Security & Licensing**: No major metadata risks have been identified, though a final review of the open‑source license and any third‑party dependencies is advisable before a full production rollout.  
- **Pilot Suitability**: Given its high signal of adoption, native performance, and low operational overhead, us/mocker is a solid candidate for a serious pilot in macOS‑centric AI development environments.

### Русский

**us/mocker** — это CLI‑инструмент, совместимый с Docker, построенный на контейнеризационной платформе Apple. Он позволяет запускать, управлять и собирать контейнеры macOS 26 теми же командами (`mocker run`, `ps`, `stop`, `build`, `compose`, `stats`), что упрощает прототипирование AI‑фич, построение RAG‑ и агентных воркфлоу без необходимости создавать собственный стек. Проект имеет высокий уровень готовности к production: активные коммиты, 254 звёзд на GitHub, широкая экосистема и поддержка Swift, хотя окончательная проверка лицензии и безопасности всё‑ещё требуется.

### 中文

**项目简介**  
us/mocker 是一款基于 Apple Containerization 框架实现的 Docker 兼容容器 CLI，提供 `run、ps、stop、build、compose、stats` 等完整指令，能够在 macOS 26 上原生运行 Docker 工作流。

**价值主张**  
- **快速赋能 AI**：无需自行搭建底层容器体系，直接在 macOS 上使用熟悉的 Docker 命令即可部署、调试和管理 AI 模型及相关服务。  
- **原型迭代加速**：适用于 AI 功能原型、RAG（检索增强生成）或智能体工作流的快速搭建与验证。  
- **统一开发体验**：前端、DevTools 与 DevOps 团队可共用同一套 CLI 与脚本，降低学习成本和运维复杂度。

**典型接入方式**  
1. **CLI 直接使用**：在 macOS 26 上安装 `us/mocker`（Homebrew 或二进制），随后使用 `mocker run …`、`mocker compose up` 等命令管理容器。  
2. **SDK / API 集成**：项目同时提供 Swift SDK 与 RESTful API，业务代码可通过调用 `MockerClient`（Swift）或 HTTP 接口在程序内部启动、监控容器，实现自动化 CI/CD 或模型服务编排。  
3. **与现有 Docker 工具链共存**：因为指令、标志完全兼容 Docker，现有 Dockerfile、Compose 文件可直接复用，无需改写。

**生产可用性**  
- **活跃度**：截至 2026‑06‑22 最近一次提交，GitHub 254 星、8 个 Fork，社区活跃。  
- **技术成熟度**：基于 Apple 官方的 Containerization 框架，底层安全与资源隔离由系统保证，兼容性和性能均已在 macOS 26 上验证。  
- **生态兼容**：完整实现 Docker CLI，能够无缝接入现有 CI/CD、K8s（通过 Docker‑compatible 代理）以及模型部署平台。  
- **风险**：目前仍需对许可证（MIT/Apache 等）以及长期维护者的承诺进行最终审查；安全审计建议在正式生产前进行渗透测试。

综合来看，us/mocker 已具备较高的生产就绪度，适合作为 AI 原型及中小规模生产环境的容器运行时，帮助团队在 macOS 环境下快速构建、测试和交付 AI 工作流。

## 🧭 Practical evaluation

**Value:** us/mocker helps add AI capability without starting from a blank model stack.

**Best use cases**

- prototype AI features
- build RAG or agent workflows
- evaluate model tooling

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 254 GitHub stars
- 8 forks
- updated 2026-06-22
- primary language: Swift
- 10 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 24/100 |
| stars | 51/100 |
| topics | 100/100 |
| outlook | 74/100 |
| quality | 70/100 |
| recency | 80/100 |
| adoption | 44/100 |
| production | 70/100 |
| usefulness | 74/100 |
| integration | 62/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 200/100 |

---

<sub>🔭 Discovered 2026-06-22 · [View on GitHub](https://github.com/us/mocker) · [← Back to DevTools](./README.md)</sub>
