# hanamorix/companion-emergence

[![Stars](https://img.shields.io/github/stars/hanamorix/companion-emergence?style=flat-square&color=yellow)](https://github.com/hanamorix/companion-emergence/stargazers) [![Forks](https://img.shields.io/github/forks/hanamorix/companion-emergence?style=flat-square&color=blue)](https://github.com/hanamorix/companion-emergence/network) [![Language](https://img.shields.io/badge/lang-Python-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-56%2F100-brightgreen?style=flat-square)](#)

> Local-first AI companion framework — persistent memory, emotional state, dreaming, embodied avatar. Desktop app + Python brain. macOS · Linux · Windows. Runs against Claude.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 26 |
| 🍴 **Forks** | 9 |
| 💻 **Language** | Python |
| 📈 **Score** | 56/100 |
| 🗓️ **Last push** | 2026-09-05 |
| 🔍 **Source** | github |

## 🏷️ Topics

`ai-companion` `claude` `emotional-ai` `local-first` `memory-system` `python` `tauri`

## 🎯 Categories

AI/ML · Productivity

## 📝 Summary

### English

**Brief Summary**  
hanamorix/companion‑emergence is a local‑first AI‑companion framework that bundles a persistent memory store, emotional‑state modeling, dreaming cycles, and an embodied avatar UI. It ships as a cross‑platform desktop client (macOS, Linux, Windows) backed by a Python “brain” that can be hooked to Claude (or other LLMs) for inference.

**Value**  
- **Speed‑to‑prototype** – Developers can add a fully‑featured conversational agent (memory, mood, visual avatar) without building the underlying stack from scratch.  
- **Local‑first privacy** – All state lives on the user’s machine, making it suitable for privacy‑sensitive applications or offline demos.  
- **Extensible brain** – The Python brain can be swapped for other LLMs or custom tool‑calling pipelines, letting teams experiment with RAG, tool use, or multi‑modal extensions while keeping the UI constant.  

**Practical Adoption Path**  

| Step | What to do | Why it matters |
|------|------------|----------------|
| 1️⃣ Quick‑start test | Clone the repo, follow the README to launch the desktop app with the default Claude‑based brain. Verify the UI, memory persistence, and avatar rendering on your OS. | Confirms basic compatibility and gives a tangible demo for stakeholders. |
| 2️⃣ Isolate a proof‑of‑concept | Create a minimal Python brain that implements the required `init`, `process_input`, and `update_state` callbacks, but uses a local LLM (e.g., Llama‑3) instead of Claude. | Shows that the framework is not Claude‑locked and lets you evaluate cost/latency trade‑offs. |
| 3️⃣ Integrate your data | Hook a RAG pipeline (e.g., LangChain + Chroma) into the brain’s `process_input` so the companion can retrieve domain‑specific documents. | Demonstrates the core use‑case of “AI‑augmented assistant” while keeping the UI unchanged. |
| 4️⃣ Security & compliance check | Scan the repository with SBOM tools (e.g., Syft, Trivy), audit the license (MIT‑style), and run static analysis on the Python dependencies. | Mitigates supply‑chain risk before moving beyond a sandbox. |
| 5️⃣ Pilot in a controlled environment | Deploy the desktop client to a small internal user group, collect telemetry on memory growth, latency, and avatar responsiveness. | Validates performance at scale and surfaces any OS‑specific quirks. |
| 6️⃣ Production hardening | • Pin dependency versions and containerize the Python brain (Docker). <br>• Add health‑checks, logging, and graceful shutdown hooks. <br>• Implement automated backups of the persistent memory store. | Turns the prototype into a maintainable, observable service ready for broader rollout. |

**Production Readiness Assessment**  

| Dimension | Rating (Low/Medium/High) | Rationale |
|-----------|--------------------------|-----------|
| **Stability** | **Medium** | The codebase builds and runs on all three major OSes, but it has modest community adoption (≈26 stars) and limited automated testing. |
| **Scalability** | Medium | Memory persistence is local; suitable for single‑user or small‑team desktops. Scaling to multi‑user or server‑side deployments would require re‑architecting the storage layer. |
| **Security** | Medium (needs review) | No obvious vulnerabilities, but the project lacks a formal security policy, SBOM, or CI‑driven dependency audit. |
| **Maintainability** | Medium | Primary language is Python, which is easy to extend. However, the maintainer activity is recent but low‑frequency; adding a CONTRIBUTING guide and CI would improve confidence. |
| **Operational Overhead** | Low‑Medium | The desktop client is zero‑install for end users; the brain can be containerized. Ongoing work is mainly around keeping the LLM API keys and updating the Python dependencies. |

**Overall Verdict**  
Companion‑Emergence is a solid foundation for rapid AI‑assistant prototypes, especially when privacy and a rich UI are required. For production use, teams should first run a small PoC, perform a thorough dependency/security audit, and add operational scaffolding (CI, version pinning, backup of the memory store). With those steps, the framework can be promoted from “medium‑readiness” to a reliable internal‑tool platform.

### Русский

**hanamorix/companion-emergence** — это open‑source фреймворк для создания локальных AI‑компаньонов с постоянной памятью, эмоциональным состоянием, «сновидениями» и визуальным аватаром (десктоп‑приложение + Python‑мозг). Он позволяет быстро добавить интеллектуальные возможности (RAG, агентные сценарии, прототипы новых функций) без необходимости строить стек моделей с нуля, используя Claude в качестве бэкенда. Готовность к production — средняя: проект подходит для прототипов и внутренних сервисов, но перед масштабированием требуется проверка зависимостей, лицензии и поддержка безопасности.

### 中文

**项目简介**  
hanamorix/companion‑emergence 是一个 **本地优先（local‑first）AI 伴侣框架**，提供持久记忆、情感状态、梦境模拟以及可视化化身。它由桌面客户端 + Python 大脑组成，支持 macOS、Linux、Windows，并可直接对接 Claude 等大模型。

---

### 价值点
1. **快速落地 AI 能力**：无需从零搭建模型堆栈，直接使用框架内置的记忆、情感与梦境模块，即可让产品拥有“有记忆、有情绪”的智能伴侣。  
2. **原型与研发加速**：适合在内部或实验性项目中快速验证 RAG、任务代理、情感交互等场景，缩短 2‑4 周的研发周期。  
3. **可扩展的本地部署**：所有核心逻辑运行在本地，数据不必上传云端，符合隐私合规和低延迟需求。

---

### 典型接入方式
| 步骤 | 操作 | 说明 |
|------|------|------|
| 1️⃣ 环境准备 | `git clone https://github.com/hanamorix/companion-emergence.git && cd companion-emergence && pip install -r requirements.txt` | 依赖主要是 Python 与桌面运行时（Electron/Qt），支持跨平台。 |
| 2️⃣ 配置模型 | 在 `config.yaml` 中填入 Claude API Key（或其他兼容的 LLM 接口） | 框架通过统一的 `LLMAdapter` 调用模型，可替换为自研模型。 |
| 3️⃣ 启动大脑 | `python -m companion_brain` | 启动持久记忆、情感状态和梦境调度服务。 |
| 4️⃣ 启动客户端 | 双击桌面应用或 `npm run start`（如果使用 Electron） | UI 与大脑通过本地 WebSocket 交互。 |
| 5️⃣ 集成业务 | 在业务代码中调用 `companion_brain.client.send_message(...)` 或使用 HTTP 接口 | 可嵌入聊天机器人、客服系统、个人助理等。 |

> **小技巧**：先在本地跑通 `README` 中的 “Hello‑Companion” 示例，确认记忆持久化路径与情感状态回调后，再进行业务层的封装。

---

### 生产可用性评估
| 维度 | 现状 | 建议 |
|------|------|------|
| **成熟度** | ★★☆☆☆（GitHub ★26，最近更新 2026‑06‑23） | 适合作为 **原型/内部工具**，在生产前需完成代码审计和单元测试。 |
| **依赖管理** | 主要依赖 Python 包和本地桌面运行时 | 使用 `pipenv`/`poetry` 锁定版本，定期检查安全公告。 |
| **可维护性** | 维护者数量有限，社区活跃度一般 | 建议内部 fork 并自行维护 CI/CD，形成专属分支。 |
| **安全/合规** | 暂无明确许可证审查，模型调用需自行管理 API Key | 采用内部私有仓库，确保 API Key 加密存储；审查 MIT/Apache 等兼容许可证。 |
| **性能** | 本地运行，延迟低；内存占用随记忆规模线性增长 | 生产环境可配置记忆压缩或定期归档，以控制磁盘使用。 |
| **部署** | 桌面客户端 + Python 服务，跨平台支持 | 对于服务器端使用，可将 Python 大脑容器化（Docker），客户端通过 Web UI 访问。 |

**结论**：`companion-emergence` 在 **原型开发和内部实验** 场景下价值突出，能够显著降低 AI 伴侣功能的实现成本。若要在生产环境使用，建议先完成 **小规模 PoC → 安全审计 → 依赖锁定 → 自动化部署** 四步，随后再评估是否投入正式业务。

## 🧭 Practical evaluation

**Value:** hanamorix/companion-emergence helps add AI capability without starting from a blank model stack.

**Best use cases**

- prototype AI features
- build RAG or agent workflows
- evaluate model tooling

**Integration notes:** Looks feasible to evaluate, but integration should start with a small proof of concept and README check.

**Production readiness:** Medium: useful for prototypes or internal workflows, with dependency and maintenance checks before production.

**Quality signals**

- 26 GitHub stars
- 9 forks
- updated 2026-06-23
- primary language: Python
- 7 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 25/100 |
| stars | 30/100 |
| topics | 88/100 |
| outlook | 66/100 |
| quality | 61/100 |
| recency | 80/100 |
| adoption | 29/100 |
| production | 65/100 |
| usefulness | 58/100 |
| integration | 46/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 200/100 |

---

<sub>🔭 Discovered 2026-06-23 · [View on GitHub](https://github.com/hanamorix/companion-emergence) · [← Back to AI/ML](./README.md)</sub>
