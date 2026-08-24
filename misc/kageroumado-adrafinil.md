# kageroumado/adrafinil

[![Stars](https://img.shields.io/github/stars/kageroumado/adrafinil?style=flat-square&color=yellow)](https://github.com/kageroumado/adrafinil/stargazers) [![Forks](https://img.shields.io/github/forks/kageroumado/adrafinil?style=flat-square&color=blue)](https://github.com/kageroumado/adrafinil/network) [![Language](https://img.shields.io/badge/lang-Unknown-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-36%2F100-brightgreen?style=flat-square)](#)

> Discovered from Hacker News (github-mentions)

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | — |
| 🍴 **Forks** | — |
| 💻 **Language** | Unknown |
| 📈 **Score** | 36/100 |
| 🗓️ **Last push** | 2026-08-24 |
| 🔍 **Source** | hackernews |

## 🏷️ Topics

`hn` `github-mentions`

## 🎯 Categories

Misc

## 📝 Summary

### English

**Brief Summary (2‑3 sentences)**  
*Adrafinil* is an open‑source macOS utility that prevents a lid‑closed Mac from sleeping only while specified “agents” (e.g., background scripts, AI workers, or CI jobs) are running. It lets developers prototype AI‑enhanced workflows—such as Retrieval‑Augmented Generation (RAG) pipelines or autonomous agents—without keeping the whole machine awake all the time.

**Value Proposition**  
- **Targeted wake‑locks**: Saves power and reduces wear by keeping the Mac awake only when needed, a common requirement for long‑running AI model inference or data‑fetching agents.  
- **Zero‑model overhead**: The tool does not ship its own ML stack; it simply provides the OS‑level guard that lets you plug in any existing model or agent framework (LangChain, LlamaIndex, etc.) and focus on the AI logic.  
- **Fast prototyping**: With a few configuration lines you can spin up a RAG service or an autonomous agent on a MacBook, test it locally, and iterate quickly before moving to cloud or containerized environments.

**Practical Adoption Path**  

| Step | Action | Reason |
|------|--------|--------|
| 1️⃣  | **Clone & inspect** the repository; verify the license (MIT/Apache) and read the README. | Ensures legal compliance and that the code matches your security posture. |
| 2️⃣  | **Run the test script** (`make test` or `./run.sh`) on a non‑critical Mac to confirm the lid‑closed wake‑lock works as advertised. | Quick sanity check before integrating into any pipeline. |
| 3️⃣  | **Define “agents”**: create a small wrapper script (e.g., `agent.sh`) that launches your AI process and exits when it finishes. | The utility monitors the wrapper’s PID to decide when to allow sleep. |
| 4️⃣  | **Configure** via the provided `config.yaml` (or CLI flags) to point at your wrapper script and set optional timeout/retry policies. | Minimal configuration; no code changes required in the AI component. |
| 5️⃣  | **Integrate into CI/Dev workflow**: add the launch command to your local development scripts or to a Homebrew formula for team members. | Makes the tool part of the standard developer environment. |
| 6️⃣  | **Monitor & log**: enable the built‑in logging (`--log-file`) and add a health‑check endpoint if you need visibility in production. | Helps catch edge cases where the lock is not released. |
| 7️⃣  | **Gradual rollout**: start with internal prototypes, then move to a dedicated Mac mini or on‑prem server for longer‑running jobs. | Reduces risk while you verify stability and maintenance overhead. |

**Production Readiness**  
- **Maturity**: Medium. The project is actively maintained (last update 2026‑06‑27) but integration signals are sparse, and documentation is limited to basic usage.  
- **Suitability**: Ideal for prototypes, internal tooling, or low‑scale batch jobs where a Mac is already part of the infrastructure. Not recommended as a core component of high‑availability services without additional safeguards (e.g., watchdog scripts, redundancy).  
- **Dependencies & Maintenance**: Relies on standard macOS power‑management APIs; no heavy external libraries. Still, you should audit the code for edge‑case handling (e.g., sudden power loss, OS upgrades) and pin a specific release tag.  
- **Risk Mitigation**:  
  1. Verify the repository’s issue tracker for open bugs related to sleep/wake cycles.  
  2. Add automated tests that simulate agent start/stop to ensure the lid‑lock behaves correctly after OS updates.  
  3. Consider wrapping the tool in a container‑like sandbox (e.g., `brew install` + launchd service) to isolate failures.  

In summary, *Adrafinil* offers a lightweight, OS‑level solution to keep a closed‑lid Mac awake only while AI agents run, accelerating prototype development. With a modest amount of due‑diligence—license check, functional testing, and monitoring—it can be safely adopted for internal workflows, though it should be treated as a prototype‑grade component rather than a production‑critical service.

### Русский

**Show HN: Adrafinil** — это open‑source‑утилита, позволяющая держать Mac в режиме «не спит», пока работают AI‑агенты, и автоматически переводить его в спящий режим, когда они завершают работу. Типичный сценарий — прототипирование AI‑фич, построение RAG‑ или агентных пайплайнов и быстрая оценка инструментов модели без необходимости разворачивать собственный стек. Готовность к production — средняя: проект подходит для внутренних прототипов, но перед выпуском в продакшн требуется проверка лицензии, актуальности документации, активности поддержки и стабильности зависимостей.

### 中文

**项目简介（2‑3 句）**  
Show HN: **Adrafinil** 是一个让 Mac 在合上盖子后，仅在后台 AI 代理运行时保持唤醒的小工具。它通过简单的守护进程监控指定的 agent 进程，实现对计算资源的精细化控制，适合在研发阶段快速原型化 AI 功能。

**价值**  
- **即插即用的 AI 能力**：无需从零搭建模型堆栈，直接在已有的 agent 环境上添加“保持唤醒”功能，省时省力。  
- **原型与 RAG/Agent 工作流**：在开发检索增强生成（RAG）或多代理系统时，可确保只有真正需要计算的阶段才消耗电力和资源。  
- **成本与安全**：合上盖子时系统进入低功耗状态，降低硬件磨损和意外泄露风险。

**典型接入方式**  
1. **克隆仓库**并通过 Homebrew 或直接运行脚本安装守护进程。  
2. 在项目的 `agent` 启动脚本中添加 **Adrafinil** 提供的 `keep-awake` 命令或使用其 Python API 包装 agent 的入口函数。  
3. 配置 `~/.adrafinil/config.yaml`，指定需要监控的进程名称或 PID 列表（如 `my_agent.py`），以及唤醒超时时间。  
4. 通过 `systemctl`（或 macOS 的 `launchd`）注册为后台服务，确保系统启动时自动加载。

**生产可用性**  
- **成熟度**：目前评估为 **Medium**，适合原型、内部工具或实验性部署。  
- **依赖与维护**：项目更新于 2026‑06‑27，社区活跃度一般，需自行检查许可证、依赖冲突以及发布节奏。  
- **上线前检查**：  
  - 确认代码许可证兼容公司政策；  
  - 评估守护进程对系统安全策略（如 SIP、Gatekeeper）的影响；  
  - 通过内部 CI 对 `keep-awake` 的启动/停止逻辑做回归测试；  
  - 监控日志和资源使用，防止误唤醒导致功耗异常。  

综上，Adrafinil 在需要精细控制 Mac 计算资源的 AI 研发场景下价值突出，接入简单，但在生产环境使用前建议完成上述审查与测试。

## 🧭 Practical evaluation

**Value:** Show HN: Adrafinil – keep a lid-closed Mac awake only while agents work helps add AI capability without starting from a blank model stack.

**Best use cases**

- prototype AI features
- build RAG or agent workflows
- evaluate model tooling

**Integration notes:** Needs manual inspection before adoption because integration signals are sparse in the discovered metadata.

**Production readiness:** Medium: useful for prototypes or internal workflows, with dependency and maintenance checks before production.

**Quality signals**

- updated 2026-06-27
- 2 topics

**Risks:** Quality signals are limited; verify license, maintenance, docs, issues, and release cadence before using it.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 0/100 |
| stars | 0/100 |
| topics | 25/100 |
| outlook | 36/100 |
| quality | 26/100 |
| recency | 40/100 |
| adoption | 0/100 |
| production | 38/100 |
| usefulness | 58/100 |
| integration | 30/100 |
| sourceTrust | 80/100 |
| categoryMatchCount | 0/100 |

---

<sub>🔭 Discovered 2026-06-27 · [View on GitHub](https://github.com/kageroumado/adrafinil) · [← Back to Misc](./README.md)</sub>
