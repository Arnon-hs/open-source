# voidzero-dev/oxc-angular-compiler

[![Stars](https://img.shields.io/github/stars/voidzero-dev/oxc-angular-compiler?style=flat-square&color=yellow)](https://github.com/voidzero-dev/oxc-angular-compiler/stargazers) [![Forks](https://img.shields.io/github/forks/voidzero-dev/oxc-angular-compiler?style=flat-square&color=blue)](https://github.com/voidzero-dev/oxc-angular-compiler/network) [![Language](https://img.shields.io/badge/lang-Rust-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-48%2F100-brightgreen?style=flat-square)](#)

> Experimental Angular Compiler based Oxc

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 220 |
| 🍴 **Forks** | 17 |
| 💻 **Language** | Rust |
| 📈 **Score** | 48/100 |
| 🗓️ **Last push** | 2026-09-05 |
| 🔍 **Source** | github |

## 🏷️ Topics

_no topics_

## 🎯 Categories

Misc

## 📝 Summary

### English

Here's a summary of the open-source project:

The voidzero-dev/oxc-angular-compiler is an experimental Angular compiler based on Oxc, offering a potential solution for specific workflows. Its value lies in its ability to be useful when its documentation and activity align with a concrete project requirement. However, its practical adoption path requires manual inspection and validation due to sparse integration signals and a non-obvious integration path.

As for production readiness, the project is considered medium, making it suitable for prototypes or internal workflows after thorough dependency and maintenance checks. This means it can be used in controlled environments, but its adoption in production settings should be approached with caution.

### Русский

Резюме проекта voidzero-dev/oxc-angular-compiler:

Этот экспериментальный компилятор Angular, основанный на Oxc, предназначен для использования в прототипах или внутренних рабочих процессах. Он может быть полезен при соответствующей настройке и проверке, но требует ручного осмотра перед внедрением. Проект имеет средний уровень готовности к production, что означает, что он может использоваться в продакшен-окружении после необходимых проверок и оценок.

### 中文

**项目简介（2‑3 句）**  
`voidzero-dev/oxc-angular-compiler` 是一个基于 Oxc（Rust 编写的 JavaScript/TypeScript 解析器）的实验性 Angular 编译器实现。它尝试用 Rust 的高性能解析和代码生成能力来加速 Angular 模板的编译过程，为前端构建提供更快的增量编译选项。

**价值**  
- **性能提升**：借助 Oxc 的零拷贝 AST 与 Rust 编译器的速度，可在大型 Angular 项目中显著缩短模板编译时间。  
- **生态兼容**：在保持 Angular 编译器 API（`@angular/compiler`）兼容的前提下，提供可插拔的后端实现，方便在现有 Angular CLI 流程中试验。  
- **开源可审计**：全 Rust 实现，代码可审计，适合对编译安全和二进制体积有严格要求的团队。

**典型接入方式**  
1. **本地实验**：在项目根目录 `package.json` 中添加自定义编译器入口，例如  
   ```json
   "angularCompilerOptions": {
     "customCompiler": "node_modules/oxc-angular-compiler/bin/oxc-compiler.js"
   }
   ```  
   并通过 `npm i voidzero-dev/oxc-angular-compiler` 安装。  
2. **Angular CLI 插件**：使用 `ng add`（如果项目提供 schematics）或手动在 `angular.json` 的 `architect.build.options` 中指定 `builder: "oxc-angular-compiler:build"`。  
3. **CI/CD 集成**：在 CI 脚本里先构建 Rust 二进制（`cargo build --release`），随后将生成的 `oxc-compiler` 放入 `node_modules/.bin`，确保构建机器上已有 Rust 环境。

**生产可用性**  
- **成熟度**：当前评分 51/100，属于 **中等** 级别。代码已有 220+ 星、17 个 Fork，最近一次提交在 2026‑06‑29，活跃度尚可。  
- **适用场景**：适合内部原型、性能基准测试或对编译速度极端敏感的内部工具。直接用于对外生产系统前，建议：  
  1. 完整跑一遍 Angular 全量构建，比较产出体积与编译时长。  
  2. 验证与现有的 Angular 插件（如 Angular Language Service、Webpack/ESBuild）兼容性。  
  3. 将二进制交付纳入内部 CI，确保 Rust 编译链在所有构建节点上可用。  
- **风险**：集成路径和文档仍然稀疏，需要自行检查依赖（Rust 工具链、二进制分发）以及后续维护成本。若项目团队对 Rust 不熟悉，集成成本会相对较高。  

总体而言，`oxc-angular-compiler` 在性能实验和内部原型阶段具备一定价值，但在正式生产环境采用前应进行充分的兼容性与维护性评估。

## 🧭 Practical evaluation

**Value:** voidzero-dev/oxc-angular-compiler may be useful when its README and activity match a concrete workflow.

**Best use cases**

- Not enough metadata yet.

**Integration notes:** Needs manual inspection before adoption because integration signals are sparse in the discovered metadata.

**Production readiness:** Medium: useful for prototypes or internal workflows, with dependency and maintenance checks before production.

**Quality signals**

- 220 GitHub stars
- 17 forks
- updated 2026-06-29
- primary language: Rust

**Risks:** Integration path is not obvious from metadata; validate setup cost before committing.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 31/100 |
| stars | 50/100 |
| topics | 0/100 |
| outlook | 58/100 |
| quality | 55/100 |
| recency | 80/100 |
| adoption | 45/100 |
| production | 60/100 |
| usefulness | 42/100 |
| integration | 30/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 0/100 |

---

<sub>🔭 Discovered 2026-06-29 · [View on GitHub](https://github.com/voidzero-dev/oxc-angular-compiler) · [← Back to Misc](./README.md)</sub>
