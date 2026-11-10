# tinqiao-oss/engramory

[![Stars](https://img.shields.io/github/stars/tinqiao-oss/engramory?style=flat-square&color=yellow)](https://github.com/tinqiao-oss/engramory/stargazers) [![Forks](https://img.shields.io/github/forks/tinqiao-oss/engramory?style=flat-square&color=blue)](https://github.com/tinqiao-oss/engramory/network) [![Language](https://img.shields.io/badge/lang-JavaScript-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-64%2F100-brightgreen?style=flat-square)](#)

> Agent 通用长期记忆层：Agent 将重要信息按类型记录为多篇可读的 markdown 记忆文档，文档以链接形式列在限长索引中，索引随会话自动注入。DeepSeek Harness（dsh）有专用插件 dsh-engramory。

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 204 |
| 🍴 **Forks** | 12 |
| 💻 **Language** | JavaScript |
| 📈 **Score** | 64/100 |
| 🗓️ **Last push** | 2026-11-06 |
| 🔍 **Source** | github |

## 🏷️ Topics

`agent-memory` `ai-agents` `claude-code` `codex` `knowledge-base` `llm-memory` `long-term-memory` `markdown` `mcp` `memory` `prompt-engineering` `zero-dependency`

## 🎯 Categories

Orchestration · MCP · Knowledge/RAG · AI/ML · Documents

## 📝 Summary

### English

Engramory is a file-based memory protocol for AI agents. Notes are ordinary Markdown files listed in a MEMORY.md index. The repository provides the SKILL.md specification, Python tools for initializing and checking a memory collection, host-specific hooks and adapters, and the dsh-engramory plugin for DeepSeek Harness. Follow the documented setup for your host and validate the index before sharing a memory collection.

### Русский

Engramory хранит память AI-агента в обычных Markdown-файлах с индексом MEMORY.md. В репозитории есть спецификация SKILL.md, Python-инструменты для создания и проверки коллекции памяти, адаптеры и хуки для поддерживаемых приложений, а также плагин dsh-engramory для DeepSeek Harness. Для подключения используйте инструкцию своего приложения и проверяйте индекс памяти.

### 中文

Engramory 是面向 AI 智能体的文件式记忆协议。记忆保存在普通 Markdown 文件中，由 MEMORY.md 索引列出。仓库提供 SKILL.md 规范、用于初始化和检查记忆库的 Python 工具、适用于不同宿主的适配器和钩子，以及 DeepSeek Harness 的 dsh-engramory 插件。请按照对应宿主的文档配置并检查索引。

## 🧭 Practical evaluation

**Value:** Maintain portable agent memory as readable Markdown notes and a small index.

**Best use cases**

- Maintain an indexed Markdown memory collection
- Share a memory collection between supported hosts
- Check memory index size and consistency

**Integration notes:** Read SKILL.md and the adapter instructions for your host. Use the documented tools/ scripts and hooks; DeepSeek Harness users can use dsh-engramory.

**Production readiness:** Source-documented memory protocol and host adapters. Evaluate file permissions, hooks and backups in your environment; no independent production validation is asserted.

**Quality signals**

- README and SKILL.md describe the file-based memory protocol
- Repository includes memory initialization and checking tools

**Risks:** Host integration and memory-file access require review. Follow the upstream adapter instructions rather than inferred SDK or service interfaces.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 12/100 |
| stars | 33/100 |
| topics | 100/100 |
| outlook | 70/100 |
| quality | 62/100 |
| recency | 80/100 |
| adoption | 27/100 |
| production | 67/100 |
| usefulness | 74/100 |
| integration | 62/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 500/100 |

---

<sub>🔭 Discovered 2026-06-23 · [View on GitHub](https://github.com/tinqiao-oss/engramory) · [← Back to Orchestration](./README.md)</sub>
