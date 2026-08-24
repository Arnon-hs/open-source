# Jesseovo/last30days-skill-cn

[![Stars](https://img.shields.io/github/stars/Jesseovo/last30days-skill-cn?style=flat-square&color=yellow)](https://github.com/Jesseovo/last30days-skill-cn/stargazers) [![Forks](https://img.shields.io/github/forks/Jesseovo/last30days-skill-cn?style=flat-square&color=blue)](https://github.com/Jesseovo/last30days-skill-cn/network) [![Language](https://img.shields.io/badge/lang-Python-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-57%2F100-brightgreen?style=flat-square)](#)

> last30days-cn 是一个 AI Agent 技能（Skill），能够自动搜索中国互联网 8 大主流平台最近 30 天的内容，综合分析后生成有据可查的研究报告。

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 928 |
| 🍴 **Forks** | 110 |
| 💻 **Language** | Python |
| 📈 **Score** | 57/100 |
| 🗓️ **Last push** | 2026-08-24 |
| 🔍 **Source** | github |

## 🏷️ Topics

`claude-code` `openclaw` `openclaw-skills` `rednotebook` `research` `tiktok` `web-search`

## 🎯 Categories

AI/ML

## 📝 Summary

### English

**Project Summary:**

The last30days-cn project is an open-source AI Agent skill that automatically searches and analyzes content from China's 8 major internet platforms over the past 30 days, generating a comprehensive research report. This project offers a pre-built AI capability that can be easily integrated into various applications. With its recent activity, strong adoption, and robust ecosystem signals, last30days-cn is highly production-ready for serious pilots.

**Value Proposition:**

The primary value of last30days-cn lies in its ability to add AI capability without requiring a custom-built model stack from scratch. This makes it an ideal choice for developers who want to prototype AI features, build RAG (Reactive Agent Graph) or agent workflows, or evaluate model tooling.

**Practical Adoption Path:**

To adopt last30days-cn, developers can start by:

1. Evaluating the project's feasibility through a small proof of concept.
2. Reviewing the README documentation to understand the project's architecture and usage.
3. Integrate the skill into their application, taking into account any necessary modifications or customizations.

**Production Readiness:**

The project's production readiness is high due to:

1. Recent activity: The project has been updated recently (2026-07-06), indicating active maintenance

### Русский

**Jesseovo/last30days-skill-cn** — это открытый AI‑агент, который за один запрос собирает и анализирует контент за последние 30 дней с восьми крупнейших китайских интернет‑платформ, формируя проверяемый исследовательский отчёт. Его типичное внедрение — быстрый прототип RAG/агентных воркфлоу: подключаете навык к существующей модели, задаёте запрос и получаете готовый аналитический вывод без необходимости строить собственный пайплайн. Проект уже активен (обновления до 2026‑07‑06, 928 звёзд, 110 форков), имеет хорошую документацию и стабильный Python‑код, что делает его готовым к пилотному использованию в продакшн‑среде после небольшого PoC и проверки лицензии/безопасности.

### 中文

**项目简介**  
`Jesseovo/last30days-skill-cn` 是一款面向 AI Agent 的 Skill，能够自动抓取中国互联网 8 大主流平台（如微博、知乎、抖音等）最近 30 天的公开内容，经过多维度清洗与语义分析后，生成可溯源、结构化的研究报告。

**价值点**  
- **快速获取最新舆情**：无需手动爬虫或自行构建数据管道，一键得到近 30 天的热点信息。  
- **提升 AI 能力**：为 RAG（Retrieval‑Augmented Generation）或自主 Agent 工作流提供即时、可信的检索来源，显著降低模型训练和数据准备成本。  
- **可落地的业务洞察**：报告中包含数据来源、时间戳、关键指标和趋势分析，直接支撑市场调研、品牌监测和竞争情报等业务需求。

**典型接入方式**  
1. **环境准备**  
   ```bash
   git clone https://github.com/Jesseovo/last30days-skill-cn.git
   cd last30days-skill-cn
   pip install -r requirements.txt
   ```
2. **API 调用**（示例）  
   ```python
   from last30days_skill import Last30DaysSkill

   skill = Last30DaysSkill(api_key="YOUR_OPENAI_KEY")
   report = skill.run(topic="新能源车", platforms=["微博", "知乎"])
   print(report)
   ```
   - `topic`：查询关键词或主题。  
   - `platforms`（可选）：指定平台列表，默认全部 8 大平台。  
   - 返回值为 JSON 或 Markdown 格式的报告，包含原始来源链接、摘要、情感倾向等。

3. **Agent 工作流集成**  
   将该 Skill 注册为 LangChain、AutoGPT、CrewAI 等框架的工具函数，即可在多轮对话或自动化脚本中调用，实现“检索‑分析‑生成”闭环。

**生产可用性**  
- **活跃度**：截至 2026‑07‑06，项目最近一次提交，GitHub ★928、Fork 110，社区活跃。  
- **技术成熟度**：基于 Python 实现，使用成熟的爬虫库（requests、playwright）和 NLP 框架（spaCy、transformers），代码结构清晰，易于二次开发。  
- **安全与合规**：目前未发现重大元数据风险，仍建议在正式部署前完成许可证（MIT）审查、依赖安全扫描（如 Dependabot）以及对抓取频率的合规评估。  
- **生产建议**：先在测试环境完成小规模 POC（如单主题、单平台），验证数据质量和响应时延后，再扩展至全平台、并发调用。整体来看，该项目已具备 OSS 级别的生产候选资格，适合作为企业内部 AI 检索能力的快速落地组件。

## 🧭 Practical evaluation

**Value:** Jesseovo/last30days-skill-cn helps add AI capability without starting from a blank model stack.

**Best use cases**

- prototype AI features
- build RAG or agent workflows
- evaluate model tooling

**Integration notes:** Looks feasible to evaluate, but integration should start with a small proof of concept and README check.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 928 GitHub stars
- 110 forks
- updated 2026-07-06
- primary language: Python
- 7 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 51/100 |
| stars | 63/100 |
| topics | 88/100 |
| outlook | 59/100 |
| quality | 65/100 |
| recency | 40/100 |
| adoption | 60/100 |
| production | 57/100 |
| usefulness | 58/100 |
| integration | 46/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 100/100 |

---

<sub>🔭 Discovered 2026-07-06 · [View on GitHub](https://github.com/Jesseovo/last30days-skill-cn) · [← Back to AI/ML](./README.md)</sub>
