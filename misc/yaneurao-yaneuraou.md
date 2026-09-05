# yaneurao/YaneuraOu

[![Stars](https://img.shields.io/github/stars/yaneurao/YaneuraOu?style=flat-square&color=yellow)](https://github.com/yaneurao/YaneuraOu/stargazers) [![Forks](https://img.shields.io/github/forks/yaneurao/YaneuraOu?style=flat-square&color=blue)](https://github.com/yaneurao/YaneuraOu/network) [![Language](https://img.shields.io/badge/lang-C%2B%2B-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-51%2F100-brightgreen?style=flat-square)](#)

> YaneuraOu is the World's Strongest Shogi engine(AI player) , WCSC29 1st winner , educational and USI compliant engine.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 664 |
| 🍴 **Forks** | 173 |
| 💻 **Language** | C++ |
| 📈 **Score** | 51/100 |
| 🗓️ **Last push** | 2026-09-05 |
| 🔍 **Source** | github |

## 🏷️ Topics

_no topics_

## 🎯 Categories

Misc

## 📝 Summary

### English

**Brief summary (2‑3 sentences)**  
YaneuraOu is a world‑class, USI‑compatible Shogi engine that won the 29th World Computer Shogi Championship. Written in C++, it is open‑source, actively maintained, and widely used as a reference implementation for strong Shogi AI research. The project provides a ready‑made, high‑performance engine that can be extended for custom AI experiments, RAG pipelines, or agent‑based workflows.

**Value**  
- **Instant AI capability** – Instead of building a Shogi engine from scratch, developers can plug into a proven, championship‑winning codebase, saving months of research and tuning.  
- **Educational resource** – The clean, well‑documented C++ code serves as a learning platform for game‑tree search, evaluation functions, and parallel search techniques.  
- **Extensible foundation** – Its USI (Universal Shogi Interface) compliance makes it easy to integrate with existing GUIs, self‑play loops, or higher‑level frameworks for reinforcement learning, model‑based evaluation, or RAG‑style knowledge retrieval.

**Practical adoption path**  
1. **Clone the repo and build** using the provided Makefile/CMake scripts (requires a recent C++ compiler and standard libraries).  
2. **Run the engine in USI mode** with a Shogi GUI (e.g., Shogidokoro) to verify correctness.  
3. **Replace or augment the evaluation module** with your own model (e.g., a neural net) by implementing the USI `eval` command or by linking a custom shared library.  
4. **Integrate into pipelines** – use the engine as a subprocess in Python/Node scripts, feed it positions via USI commands, and collect move outputs for self‑play or data generation.  
5. **Iterate and test** – because the repository lacks high‑level integration docs, you’ll need to manually validate the build environment and the USI handshake before scaling.

**Production readiness**  
- **Readiness level: Medium** – The engine is stable and battle‑tested, making it suitable for prototypes, internal tooling, or research platforms.  
- **Dependencies & maintenance** – The codebase is actively updated (last commit 2026‑06‑30) and has a healthy community (≈664 ★, 173 forks), but you must manage C++ build dependencies and ensure compatibility with your target platform.  
- **Risk considerations** – Integration signals are sparse; there is no out‑of‑the‑box wrapper for modern ML frameworks, so expect some engineering effort to connect custom models or orchestration tools. Perform a small‑scale validation (e.g., run a self‑play batch) before committing to production use.

### Русский

Резюме проекта yaneurao/YaneuraOu:

YaneuraOu - это мощный шатранджный движок (игрок с искусственным интеллектом), победитель чемпионата мира в 2029 году, предоставляющий образовательные возможности и поддержку протокола USI. Этот проект позволяет легко добавить в свои приложения функции искусственного интеллекта, что делает его идеальным решением для прототипирования и внутренних рабочих процессов. YaneuraOu готов к использованию, но требует тщательной проверки перед выпуском в production, что делает его средством средней готовности для прототипирования и внутренних рабочих процессов.

### 中文

**项目简介（2‑3 句）**  
YaneuraOu 是目前最强的将棋引擎，曾夺得 WCSC29 冠军，兼具教学意义并遵循 USI（Universal Shogi Interface）协议。它以 C++ 实现，代码活跃、社区规模可观，是开发和评估将棋 AI 的首选基准。

**价值**  
- **即插即用的强大 AI 能力**：无需从零构建搜索、评估等核心模块，直接复用业界顶尖的搜索算法和评估函数。  
- **教学与研究双重价值**：代码结构清晰、注释丰富，适合作为学习将棋 AI 的教材或进行新特征实验。  
- **可作原型平台**：在此基础上快速实现 RAG、策略生成或自定义对局流程，缩短研发周期。

**典型接入方式**  
1. **源码编译**：克隆仓库后使用 CMake/Make 编译生成可执行文件或库。  
2. **USI 接口对接**：通过标准 USI 协议与现有棋盘前端、对局服务器或自研平台交互，发送 `position`、`go` 等指令即可。  
3. **二次封装**：如需在 Python/Java 等语言中调用，可使用 `subprocess` 启动 USI 进程或自行实现轻量级 USI‑Bridge（已有社区的 Python‑USI 包可直接复用）。  

**生产可用性**  
- **成熟度**：GitHub ★ 664、Fork ★ 173，最近更新于 2026‑06‑30，代码活跃且社区活跃。  
- **准备度**：**中等**。适合作为内部原型或实验平台，但在正式生产环境部署前需完成以下检查：  
  - **依赖审计**：确认编译链、第三方库（如 SIMD、Boost）在目标系统上的兼容性。  
  - **性能基准**：根据业务需求测评搜索深度、响应时延，确保满足实时对局或批量评估的 SLA。  
  - **安全/合规**：由于缺乏完整的元数据和自动化部署脚本，建议手动审查构建产物和运行时权限。  

综上，YaneuraOu 为需要强大将棋 AI 能力的团队提供了高质量的底层实现，接入成本主要在编译与 USI 对接层面，经过适当的依赖与性能验证后即可在内部系统或受控生产环境中稳定运行。

## 🧭 Practical evaluation

**Value:** yaneurao/YaneuraOu helps add AI capability without starting from a blank model stack.

**Best use cases**

- prototype AI features
- build RAG or agent workflows
- evaluate model tooling

**Integration notes:** Needs manual inspection before adoption because integration signals are sparse in the discovered metadata.

**Production readiness:** Medium: useful for prototypes or internal workflows, with dependency and maintenance checks before production.

**Quality signals**

- 664 GitHub stars
- 173 forks
- updated 2026-06-30
- primary language: C++

**Risks:** Integration path is not obvious from metadata; validate setup cost before committing.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 56/100 |
| stars | 60/100 |
| topics | 0/100 |
| outlook | 61/100 |
| quality | 62/100 |
| recency | 80/100 |
| adoption | 59/100 |
| production | 63/100 |
| usefulness | 42/100 |
| integration | 30/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 0/100 |

---

<sub>🔭 Discovered 2026-06-30 · [View on GitHub](https://github.com/yaneurao/YaneuraOu) · [← Back to Misc](./README.md)</sub>
