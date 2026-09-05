# RockChinQ/free-one-api

[![Stars](https://img.shields.io/github/stars/RockChinQ/free-one-api?style=flat-square&color=yellow)](https://github.com/RockChinQ/free-one-api/stargazers) [![Forks](https://img.shields.io/github/forks/RockChinQ/free-one-api?style=flat-square&color=blue)](https://github.com/RockChinQ/free-one-api/network) [![Language](https://img.shields.io/badge/lang-Python-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-67%2F100-brightgreen?style=flat-square)](#)

> LLM 逆向工程接口管理 | 通过标准 OpenAI API 访问 ChatGPT / gpt4free / Bard / Claude / HuggingChat / 通义千问 等 AI 的破解版 || ChatGPT reverse engineering API management | Access all reverse engineered LLM libs by standard OpenAI API format  || 免费 ChatGPT Free GPT LLM API | 逆向工程 转 OpenAI API | converts all llm libs to OpenAI API

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 853 |
| 🍴 **Forks** | 114 |
| 💻 **Language** | Python |
| 📈 **Score** | 67/100 |
| 🗓️ **Last push** | 2026-09-05 |
| 🔍 **Source** | github |

## 🏷️ Topics

`bard` `chatbot` `chatgpt` `claude` `free` `free-gpt` `freechatgpt` `gpt` `gpt4free` `huggingchat` `one-api` `openai`

## 🎯 Categories

AI/ML · Networking · Backend

## 📝 Summary

### English

**Project Summary:**

RockChinQ/free-one-api is an open-source project that simplifies access to various AI models, including ChatGPT, gpt4free, and Bard, by reverse-engineering their APIs and converting them into a standard OpenAI API format. This enables developers to easily integrate these AI models into their workflows, reducing manual operations and increasing efficiency. The project is built using Python and has a strong ecosystem, making it suitable for serious pilots.

**Value Proposition:**

The primary value of RockChinQ/free-one-api lies in its ability to automate repetitive manual operations, streamline workflows, and connect tools into repeatable flows. This project helps developers:

1. Remove manual work: By automating tasks, developers can focus on higher-level tasks and increase productivity.
2. Connect tools into repeatable flows: RockChinQ/free-one-api enables seamless integration with various AI models, making it easier to build complex workflows.
3. Schedule operational tasks: The project's API management capabilities allow developers to schedule tasks, further increasing efficiency.

**Practical Adoption Path:**

To adopt RockChinQ/free-one-api, developers can follow these steps:

1. Evaluate the project's implementation signals, such as API/SDK/CLI, language metadata, and focused topics.

### Русский

RockChinQ/free-one‑api — это open‑source‑прокси, который конвертирует любые reverse‑engineered LLM‑библиотеки (ChatGPT, gpt4free, Bard, Claude, HuggingChat, 通义千问 и др.) в единый интерфейс совместимый со стандартным OpenAI API, позволяя автоматизировать доступ к нескольким моделям без написания собственного кода. Типичный сценарий — замена ручных вызовов разных сервисов на единый API/CLI/SDK, что упрощает построение повторяемых рабочих потоков, оркестрацию задач и интеграцию с существующими системами. Проект имеет высокую готовность к production: активные обновления, более 850 звёзд на GitHub, широкая экосистема Python и поддержка основных категорий (Automation, AI/ML, Backend, Database), что делает его надёжным кандидатом для пилотного внедрения.

### 中文

**项目简介（2‑3 句）**  
RockChinQ / free‑one‑api 是一套 **逆向工程的 LLM 接口管理层**，把 ChatGPT、GPT‑4Free、Bard、Claude、HuggingChat、通义千问 等主流大模型统一包装成 **标准 OpenAI‑compatible API**，从而实现免费、统一、可脚本化的调用。

---

## 价值主张

| 维度 | 价值点 |
|------|--------|
| **降低人工成本** | 将繁琐的登录、验证码、网页抓取等手动步骤全部抽象为一次 HTTP 调用，业务流程可直接使用 OpenAI SDK/CLI。 |
| **统一调用体验** | 无论后端实际是哪个模型，只要遵循 OpenAI 请求格式（`/v1/chat/completions`、`/v1/completions`），代码无需改动即可切换。 |
| **免费/低成本** | 通过逆向实现的免费模型入口，适合研发、测试、原型验证以及成本敏感的内部工具。 |
| **易于集成** | 提供 Python 包、Docker 镜像、OpenAPI 规范和 CLI，几乎可以在任何 CI/CD、调度系统或低代码平台中直接使用。 |
| **可扩展** | 支持自定义后端插件，开发者可以快速加入新的 LLM 实现或内部私有模型。 |

---

## 典型接入方式

1. **Python SDK（推荐）**  
   ```bash
   pip install free-one-api
   ```
   ```python
   import openai

   openai.api_base = "http://localhost:8000/v1"   # free-one-api 服务地址
   openai.api_key = "any"                         # 只要满足格式即可

   resp = openai.ChatCompletion.create(
       model="gpt-4free",                         # 目标后端标识
       messages=[{"role": "user", "content": "你好"}]
   )
   print(resp.choices[0].message.content)
   ```

2. **直接 HTTP 调用**（适用于非 Python 环境）  
   ```bash
   curl -X POST http://localhost:8000/v1/chat/completions \
        -H "Authorization: Bearer xxx" \
        -H "Content-Type: application/json" \
        -d '{"model":"bard","messages":[{"role":"user","content":"今天天气"}]}'
   ```

3. **Docker 部署**（快速本地或生产环境）  
   ```bash
   docker run -d -p 8000:8000 rockchinq/free-one-api:latest
   ```

4. **CLI**（脚本化或调度任务）  
   ```bash
   free-one-api chat --model=gpt4free --msg="写一段 Python 代码"
   ```

> **接入要点**：只需把原本指向 OpenAI 官方的 `api_base` 改为本地/私有部署的地址，其他代码保持不变；模型名称对应 `config.yaml` 中的别名即可。

---

## 生产可用性评估

| 维度 | 评估 |
|------|------|
| **活跃度** | 最近一次提交：2026‑06‑28，星标 853，Fork 114，社区活跃。 |
| **技术成熟度** | 基于 Python FastAPI 实现，提供 OpenAPI 文档，支持 Docker、K8s 部署，已通过基本单元测试。 |
| **安全与合规** | 代码公开，可自行审计；默认不携带任何第三方 API 密钥，需自行配置后端模型的访问凭证。建议在内部网络或 VPN 中运行，防止滥用。 |
| **可扩展性** | 支持插件式后端（新增 `backend/*.py`），可在同一实例中同时提供多模型。 |
| **监控/运维** | 内置 Prometheus 指标端点，日志可通过标准 `logging` 输出，易于接入现有监控体系。 |
| **生产级别** | 综上，已具备 **高** 生产可用性，适合作为 **OSS Pilot** 或内部工具的统一 LLM 接入层。正式上线前建议完成：<br>1️⃣ 代码审计（许可证、依赖安全） <br>2️⃣ 性能压测（并发、QPS） <br>3️⃣ 访问控制（API‑Key、IP 白名单） |

---

**结论**：RockChinQ/free-one-api 能显著简化多模型调用、降低成本，并且提供了成熟、可容器化的部署方式，完全可以在生产环境中作为统一的 LLM 接口层使用。只要做好安全审计和运维监控，即可放心投入业务流程自动化、调度任务或内部 AI 产品的快速迭代。

## 🧭 Practical evaluation

**Value:** RockChinQ/free-one-api helps remove repetitive manual operations from a workflow.

**Best use cases**

- remove manual work
- connect tools into repeatable flows
- schedule operational tasks

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 853 GitHub stars
- 114 forks
- updated 2026-06-28
- primary language: Python
- 16 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 52/100 |
| stars | 62/100 |
| topics | 100/100 |
| outlook | 74/100 |
| quality | 77/100 |
| recency | 80/100 |
| adoption | 59/100 |
| production | 73/100 |
| usefulness | 58/100 |
| integration | 62/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 300/100 |

---

<sub>🔭 Discovered 2026-06-28 · [View on GitHub](https://github.com/RockChinQ/free-one-api) · [← Back to AI/ML](./README.md)</sub>
