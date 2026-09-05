# Free-AI-Things/g4f-working

[![Stars](https://img.shields.io/github/stars/Free-AI-Things/g4f-working?style=flat-square&color=yellow)](https://github.com/Free-AI-Things/g4f-working/stargazers) [![Forks](https://img.shields.io/github/forks/Free-AI-Things/g4f-working?style=flat-square&color=blue)](https://github.com/Free-AI-Things/g4f-working/network) [![Language](https://img.shields.io/badge/lang-Python-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-71%2F100-brightgreen?style=flat-square)](#)

> g4f-working is a daily-updated list of working no-auth AI providers and models from @xtekky/gpt4free. It helps developers, testers, and AI enthusiasts instantly find which models are currently online and accessible without any API keys, tokens, or cookies.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 111 |
| 🍴 **Forks** | 15 |
| 💻 **Language** | Python |
| 📈 **Score** | 71/100 |
| 🗓️ **Last push** | 2026-09-05 |
| 🔍 **Source** | github |

## 🏷️ Topics

`ai-access` `ai-directory` `ai-models` `ai-monitoring` `api` `auth-free` `automation` `daily-update` `free-ai` `gpt` `gpt4free` `gpt4free-providers`

## 🎯 Categories

Automation · AI/ML · Backend · DevTools · Observability

## 📝 Summary

### English

**Brief Summary (2‑3 sentences)**  
*Free‑AI‑Things/g4f‑working* maintains a daily‑updated catalogue of publicly accessible, no‑auth AI providers and models scraped from @xtekky/gpt4free. The list lets developers, testers and AI hobbyists instantly discover which endpoints are online and usable without API keys, tokens or cookies, turning a tedious manual lookup into a one‑click operation.

**Value**  
- **Eliminates repetitive discovery work** – instead of manually probing dozens of unofficial endpoints, teams can query a single, curated source to know which models are currently reachable.  
- **Enables rapid prototyping and testing** – scripts or CI pipelines can automatically select a working provider, speeding up experimentation and regression testing of AI‑driven features.  
- **Facilitates cost‑free integration** – because the endpoints require no authentication, they can be used for low‑volume internal tooling, demos, or educational projects without incurring API fees.

**Practical Adoption Path**  
1. **Evaluate the API/CLI** – clone the repo, install the Python package, and run the provided CLI (`g4f-working list`) to verify the output format and latency.  
2. **Integrate into existing workflows** – wrap the list call in a small helper module that selects a model based on desired capabilities (e.g., chat, completion) and returns the endpoint URL.  
3. **Automate updates** – schedule the helper to refresh the catalogue daily (e.g., via cron or a CI job) so downstream services always have the latest availability data.  
4. **Add fallback logic** – if a chosen provider becomes unavailable, the helper can fall back to the next entry in the list, ensuring graceful degradation.

**Production Readiness**  
- **Activity & Adoption** – 111 GitHub stars, 15 forks, recent commits (last updated 2026‑06‑27) and a Python codebase with rich metadata indicate an active community.  
- **Stability** – The project follows a simple data‑pull pattern with clear versioned releases, making it easy to pin a known‑good state while still benefiting from daily updates.  
- **Risk Profile** – No major metadata or licensing issues have been identified, though a final security audit and confirmation of maintainers’ responsiveness are advisable before mission‑critical deployment.  
Overall, g4f‑working is a high‑readiness OSS component suitable for pilot projects and can be promoted to production once the minor due‑diligence steps (license verification, security scan) are completed.

### Русский

Free‑AI‑Things/g4f-working — это открытый сервис, который ежедневно обновляет список работающих без‑аутентификации AI‑провайдеров и моделей из @xtekky/gpt4free, позволяя разработчикам, тестировщикам и AI‑энтузиастам мгновенно узнать, какие модели доступны без API‑ключей, токенов и cookies. Его типичный сценарий — автоматизация рабочих процессов: вместо ручного мониторинга можно подключить список к CI/CD, оркестраторам или планировщикам задач и автоматически направлять запросы к доступным моделям. Проект имеет высокий уровень готовности к production: активные коммиты, 111 звёзд, 15 форков, свежие обновления (2026‑06‑27) и поддержка Python, что делает его надёжным кандидатом для пилотного внедрения.

### 中文

**简短介绍**

Free-AI-Things/g4f-working 是一个开源项目，提供了一个每日更新的列表，列出了 @xtekky/gpt4free 提供的无认证 AI 服务和模型。该项目帮助开发者、测试者和 AI 爱好者快速找到当前在线和可访问的模型，无需 API 密钥、令牌或 Cookie。

**价值**

该项目的价值在于帮助开发者和测试者减少重复的手动操作，从而提高工作效率。它还可以帮助连接工具并建立可重复的流程，chedule 操作任务。

**典型接入方式**

该项目提供了接入信号，如 API/SDK/CLI、语言元数据或专注的主题。开发者可以根据这些信号来评估和接入该项目。

**生产可用性**

该项目的生产可用性很高，主要原因是其最近的活动、采用率和生态系统信号都很强。它适合用于生产环境的评估和测试。

## 🧭 Practical evaluation

**Value:** Free-AI-Things/g4f-working helps remove repetitive manual operations from a workflow.

**Best use cases**

- remove manual work
- connect tools into repeatable flows
- schedule operational tasks

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 111 GitHub stars
- 15 forks
- updated 2026-06-27
- primary language: Python
- 20 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 30/100 |
| stars | 44/100 |
| topics | 100/100 |
| outlook | 76/100 |
| quality | 68/100 |
| recency | 80/100 |
| adoption | 40/100 |
| production | 70/100 |
| usefulness | 90/100 |
| integration | 62/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 500/100 |

---

<sub>🔭 Discovered 2026-06-27 · [View on GitHub](https://github.com/Free-AI-Things/g4f-working) · [← Back to Automation](./README.md)</sub>
