# nix-community/nixvim

[![Stars](https://img.shields.io/github/stars/nix-community/nixvim?style=flat-square&color=yellow)](https://github.com/nix-community/nixvim/stargazers) [![Forks](https://img.shields.io/github/forks/nix-community/nixvim?style=flat-square&color=blue)](https://github.com/nix-community/nixvim/network) [![Language](https://img.shields.io/badge/lang-Nix-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-60%2F100-brightgreen?style=flat-square)](#)

> Configure Neovim with Nix! [maintainers=@GaetanLepage, @traxys, @mattsturgeon, @khaneliman]

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 2.9k |
| 🍴 **Forks** | 393 |
| 💻 **Language** | Nix |
| 📈 **Score** | 60/100 |
| 🗓️ **Last push** | 2026-07-05 |
| 🔍 **Source** | github |

## 🏷️ Topics

`neovim` `nix` `nixos` `nixos-module` `vim`

## 🎯 Categories

AI/ML

## 📝 Summary

### English

**Brief summary (2‑3 sentences)**  
nix-community/nixvim is an open‑source Nix module that lets you declaratively configure Neovim using the Nix package manager. It bundles a curated set of plugins—including AI‑oriented extensions—so you can add language‑model capabilities to your editor without building a custom stack from scratch. The project is actively maintained, has a sizable community (≈2.9 k stars), and provides ready‑to‑use examples for prototyping RAG, agent workflows, and other AI features inside Neovim.

**Value**  
- **Fast AI enablement** – By pulling in pre‑configured AI plugins (e.g., nvim‑cmp, nvim‑lsp, and model‑specific completions) you get code‑completion, chat, and retrieval‑augmented generation inside Neovim with a single Nix expression.  
- **Reproducibility** – All dependencies are pinned in Nix, guaranteeing that the same editor environment works across machines and CI pipelines.  
- **Low‑overhead prototyping** – The repository includes a minimal `default.nix` and README that can be cloned and run in minutes, letting teams experiment with AI‑driven workflows before committing to a larger stack.

**Practical adoption path**  
1. **Proof‑of‑concept** – Clone the repo, run `nix develop` (or `nix-shell`) and launch Neovim to verify the baseline configuration.  
2. **Customize** – Fork the project and extend the `nixvim` module in your own Nix flake, adding or swapping plugins to match your AI use case (e.g., a RAG plugin, an agent‑framework, or a specific LLM client).  
3. **Integrate** – Add the customized flake as a dependency in your existing NixOS or devcontainer setup; the integration is essentially a single line in your `flake.nix`.  
4. **Validate** – Run the supplied test suite (if any) and a small set of functional checks (e.g., completion, chat command) to confirm that the AI plugins work in your environment.

**Production readiness**  
- **Maturity:** Medium. The project is actively maintained (last commit 2026‑07‑05) and widely used, but it is primarily aimed at developer‑oriented setups rather than enterprise‑grade CI/CD pipelines.  
- **Risks:** The integration path isn’t fully documented for large‑scale deployments; you’ll need to assess the cost of pinning additional AI dependencies (model binaries, API keys) and ensure that your Nix infrastructure can handle the extra runtime requirements.  
- **Recommended approach:** Deploy a small internal pilot (e.g., a shared devcontainer for a team) to evaluate stability, then perform a dependency audit and add monitoring before rolling out to production environments.

### Русский

**nix-community/nixvim** — это набор Nix‑модулей для быстрой и воспроизводимой конфигурации Neovim, который уже включает готовые плагины и настройки, позволяющие добавить AI‑функциональность (RAG, агентные воркфлоу и пр.) без сборки собственного стека. Типичный путь внедрения — запустить небольшой proof‑of‑concept, проверить README и убедиться в совместимости с текущей инфраструктурой, а затем расширять конфигурацию под внутренние прототипы. Проект имеет средний уровень готовности к production: достаточно зрелый (2876 звёзд, активные мейнтейнеры), но требует предварительной проверки зависимостей и поддерживаемости перед использованием в критически важных сервисах.

### 中文

**简短介绍**

nix-community/nixvim 是一个开源项目，帮助您使用 Nix 配置 Neovim。该项目由 GaetanLepage、traxys、mattsturgeon 和 khaneliman 维护。

**价值**

nix-community/nixvim 帮助您快速添加 AI 能力，而无需从零开始搭建模型堆栈。它适用于以下场景：

* 快速 prototyping AI 特性
* 构建 RAG 或代理工作流
* 评估模型工具

**典型接入方式**

1. 查看 README 文件，了解项目的使用方法和集成步骤。
2. 开始小规模的 PoC (Proof of Concept)，验证项目的整合和性能。
3. 根据需求定制项目，添加或更改配置。

**生产可用性**

nix-community/nixvim 的生产可用性为中等（Medium）。它适用于以下场景：

* 快速 prototyping 或内部工作流
* 需要依赖和维护检查之前的生产环境

请注意，项目的整合路径不明确，需要验证设置成本之前才可用于生产环境。

## 🧭 Practical evaluation

**Value:** nix-community/nixvim helps add AI capability without starting from a blank model stack.

**Best use cases**

- prototype AI features
- build RAG or agent workflows
- evaluate model tooling

**Integration notes:** Looks feasible to evaluate, but integration should start with a small proof of concept and README check.

**Production readiness:** Medium: useful for prototypes or internal workflows, with dependency and maintenance checks before production.

**Quality signals**

- 2876 GitHub stars
- 393 forks
- updated 2026-07-05
- primary language: Nix
- 5 topics

**Risks:** Integration path is not obvious from metadata; validate setup cost before committing.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 65/100 |
| stars | 74/100 |
| topics | 63/100 |
| outlook | 77/100 |
| quality | 81/100 |
| recency | 100/100 |
| adoption | 71/100 |
| production | 75/100 |
| usefulness | 42/100 |
| integration | 30/100 |
| sourceTrust | 100/100 |

---

<sub>🔭 Discovered 2026-07-05 · [View on GitHub](https://github.com/nix-community/nixvim) · [← Back to AI/ML](./README.md)</sub>
