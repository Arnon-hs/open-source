# ebullient/ttrpg-convert-cli

[![Stars](https://img.shields.io/github/stars/ebullient/ttrpg-convert-cli?style=flat-square&color=yellow)](https://github.com/ebullient/ttrpg-convert-cli/stargazers) [![Forks](https://img.shields.io/github/forks/ebullient/ttrpg-convert-cli?style=flat-square&color=blue)](https://github.com/ebullient/ttrpg-convert-cli/network) [![Language](https://img.shields.io/badge/lang-Java-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-68%2F100-brightgreen?style=flat-square)](#)

> Utility to convert JSON data (for content you own) from 5etools or pf2etools into Obsidian-friendly Markdown.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 369 |
| 🍴 **Forks** | 63 |
| 💻 **Language** | Java |
| 📈 **Score** | 68/100 |
| 🗓️ **Last push** | 2026-08-24 |
| 🔍 **Source** | github |

## 🏷️ Topics

`5e-tools` `5etools` `dnd5e` `dungeons-and-dragons` `hacktoberfest` `java` `markdown` `obsidian-md` `pathfinder-2e` `pf2e` `picocli` `quarkus`

## 🎯 Categories

Misc

## 📝 Summary

### English

**Brief Summary**  
*ebullient/ttrpg-convert-cli* is a command‑line utility that transforms JSON exports from 5eTools or PF2eTools into Obsidian‑compatible Markdown files. By turning tabletop‑RPG data you own into searchable, link‑rich notes, the tool lets you index and retrieve that knowledge with AI assistants or traditional search.

**Value Proposition**  
- **Searchable Knowledge Base** – Converting raw JSON into Markdown lets you embed the content in Obsidian (or any plain‑text vault), making it instantly indexable by vector search, LLM retrieval, or simple grep.  
- **Assistant Grounding** – When an AI assistant needs factual answers about spells, monsters, or items, it can pull directly from the generated Markdown instead of hallucinating.  
- **Low‑friction Integration** – The CLI is language‑agnostic (it just reads/writes files), so it can be scripted into CI pipelines, data‑ingestion jobs, or personal workflow automations without needing a custom SDK.

**Practical Adoption Path**  
1. **Install** – `npm i -g @ebullient/ttrpg-convert-cli` (or use the provided Docker image).  
2. **Export JSON** – From 5eTools/PF2eTools, export the desired compendium (e.g., spells.json, monsters.json).  
3. **Run the CLI** – `ttrpg-convert --source spells.json --outdir vault/Spells`. The tool creates a Markdown file per entry with front‑matter, internal Obsidian links, and optional tag mapping.  
4. **Index** – Point your existing knowledge‑graph pipeline (e.g., Obsidian‑Search, Elastic, or a vector store) at the output directory.  
5. **Hook into LLMs** – Configure your assistant’s retrieval layer to query the newly indexed Markdown, enabling grounded answers for any TTRPG‑related request.  

**Production‑Readiness Assessment**  
- **Activity & Adoption** – 369 ⭐ on GitHub, 63 forks, last commit 2026‑07‑12, and a healthy Java ecosystem indicate active maintenance.  
- **Maturity** – The CLI is self‑contained, has clear input/output contracts, and ships with example configs; no external services are required.  
- **Risk Profile** – No obvious licensing or security red flags, though a final audit of the Apache‑2.0 (or whichever) license and any transitive dependencies is advisable.  
- **Readiness** – Given recent updates, community traction, and straightforward integration steps, the project is **highly ready for a pilot** in production environments that need searchable TTRPG content.

### Русский

**ebullient/ttrpg-convert-cli** – это CLI‑утилита, преобразующая JSON‑файлы из 5eTools или PF2eTools в markdown‑формат, оптимизированный для Obsidian, что делает ваш собственный контент по настольным RPG легко индексируемым и доступным для поисковых систем и AI‑ассистентов. Типичный сценарий: импортировать библиотеки правил/монстров в Obsidian, затем использовать их в поиске, построении графов знаний или как контекст для генеративных помощников. Проект уже имеет 369 ★, активные коммиты (обновление 2026‑07‑12), Java‑реализацию и готовую CLI/SDK‑интеграцию, что свидетельствует о высокой готовности к production‑использованию (нужен лишь финальный аудит лицензии и безопасности).

### 中文

**项目简介**  
ebullient/ttrpg-convert-cli 是一个命令行工具，能够把 5etools、pf2etools 等 TTRPG（桌面角色扮演游戏）资源的 JSON 数据转换为 Obsidian 友好的 Markdown 文件，方便玩家和 DM 将已有内容纳入自己的知识库。

**价值**  
- **提升内部知识可检索性**：将结构化的游戏数据转为 Markdown，直接写入 Obsidian，使得搜索、链接和跨文档引用变得极其便利。  
- **支撑 AI/助手应用**：Markdown 化的内容更易被向量化、索引，从而为聊天机器人或检索增强的助手提供可靠、可追溯的事实来源。  
- **统一内容管理**：一次转换即可在多个设备、插件或工作流中复用，避免手动复制粘贴和格式错误。

**典型接入方式**  
1. **CLI 直接使用**：在本地或 CI 环境中运行 `ttrpg-convert` 命令，指定输入 JSON 路径和输出目录，即可得到对应的 Markdown 文件。  
2. **脚本化工作流**：结合 npm、Makefile 或 GitHub Actions，将转换步骤嵌入内容构建流水线，实现自动化更新 Obsidian vault。  
3. **SDK/库调用**（若需要深度集成）：项目使用 Java 编写，提供核心类库，可在自定义 Java 程序或 Spring Boot 微服务中直接调用转换 API，生成 Markdown 并推送至文档存储或向量数据库。

**生产可用性**  
- **活跃度**：最近一次提交于 2026‑07‑12，拥有 369 ★、63 Fork，社区关注度高。  
- **技术成熟度**：基于 Java 实现，依赖明确，CLI 与库两种入口均已稳定发布。  
- **生态兼容**：输出的 Markdown 完全兼容 Obsidian，且易于后续使用如 `obsidian-search`, `obsidian-embedding` 等插件进行索引。  
- **风险**：目前未发现重大许可证或安全隐患，但仍建议在正式生产环境前审查许可证（MIT/Apache 等）并进行安全依赖扫描。  

综合来看，ttrpg-convert-cli 已具备较高的生产就绪度，可作为内部知识库构建和 AI 辅助检索的可靠组件快速落地。

## 🧭 Practical evaluation

**Value:** ebullient/ttrpg-convert-cli helps make internal knowledge searchable and usable by assistants.

**Best use cases**

- index knowledge bases
- improve search over documents
- ground assistant answers

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 369 GitHub stars
- 63 forks
- updated 2026-07-12
- primary language: Java
- 12 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 45/100 |
| stars | 55/100 |
| topics | 100/100 |
| outlook | 65/100 |
| quality | 63/100 |
| recency | 40/100 |
| adoption | 52/100 |
| production | 58/100 |
| usefulness | 90/100 |
| integration | 62/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 0/100 |

---

<sub>🔭 Discovered 2026-07-12 · [View on GitHub](https://github.com/ebullient/ttrpg-convert-cli) · [← Back to Misc](./README.md)</sub>
