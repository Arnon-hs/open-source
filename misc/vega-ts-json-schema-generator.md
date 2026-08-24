# vega/ts-json-schema-generator

[![Stars](https://img.shields.io/github/stars/vega/ts-json-schema-generator?style=flat-square&color=yellow)](https://github.com/vega/ts-json-schema-generator/stargazers) [![Forks](https://img.shields.io/github/forks/vega/ts-json-schema-generator?style=flat-square&color=blue)](https://github.com/vega/ts-json-schema-generator/network) [![Language](https://img.shields.io/badge/lang-TypeScript-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-53%2F100-brightgreen?style=flat-square)](#)

> Generate JSON schema from your Typescript sources

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 1.7k |
| 🍴 **Forks** | 237 |
| 💻 **Language** | TypeScript |
| 📈 **Score** | 53/100 |
| 🗓️ **Last push** | 2026-08-24 |
| 🔍 **Source** | github |

## 🏷️ Topics

`compiler` `generator` `json-schema` `typescript`

## 🎯 Categories

Misc

## 📝 Summary

### English

Here's a brief summary of the open-source project:

**Vega/ts-json-schema-generator Summary**
This project generates JSON schema from TypeScript sources, making it useful for developers who need to define the structure of their JSON data. To adopt this project, start with a small proof of concept and review the README to ensure it matches your workflow. With recent activity, strong adoption, and a healthy ecosystem, it's ready for a serious pilot.

**Value Proposition**
The value of this project lies in its ability to automate the process of generating JSON schema from TypeScript sources, saving developers time and effort. This can be particularly useful for large-scale applications or projects with complex data structures.

**Practical Adoption Path**
To adopt this project, follow these steps:

1. Review the README to ensure it matches your workflow and understand how to use the project.
2. Start with a small proof of concept to evaluate the project's feasibility and effectiveness.
3. Integrate the project into your development workflow and test its performance.
4. Monitor the project's activity and updates to ensure it remains suitable for your needs.

**Production Readiness**
With 1711 GitHub stars, 237 forks, and recent activity, Vega/ts-json-schema-generator has a high production readiness score. Its strong adoption and healthy ecosystem signals indicate

### Русский

**vega/ts-json-schema-generator** — это открытый TypeScript‑инструмент, автоматически генерирующий JSON‑схемы из исходного кода, что упрощает валидацию и документирование API без ручного описания схем. Типичный сценарий внедрения — добавить небольшую фазу генерации в CI/CD (например, запуск `ts-json-schema-generator` после сборки) и использовать полученные схемы в инструментах проверки запросов/ответов (Swagger, AJV и т.п.). Проект обладает высокой готовностью к production: активные коммиты, более 1700 звёзд, регулярные обновления и широкое принятие в сообществе, что делает его надёжным кандидатом для пилотного внедрения.

### 中文

**项目简介**  
vega/ts-json-schema-generator 是一个开源工具，可直接从 TypeScript 源码生成符合 JSON Schema Draft‑07/2020‑12 规范的 JSON Schema。它通过 TypeScript 编译器 API 解析类型信息，自动输出可用于数据校验、API 文档、Mock 数据生成等场景的 schema 文件。

**价值**  
- **统一模型**：一次维护 TypeScript 类型，即可同步得到 JSON Schema，避免手动编写或维护两套模型导致的不一致。  
- **提升效率**：在 CI/CD 流程中自动生成 schema，配合 AJV、Zod 等校验库实现运行时校验，减少人为错误。  
- **生态兼容**：生成的 schema 可直接用于 OpenAPI、GraphQL 代码生成、前端表单生成等常见工具链，提升跨团队协作效率。

**典型接入方式**  
1. **项目依赖**：`npm i -D @vega/ts-json-schema-generator`（或对应的 Yarn/PNPM 命令）。  
2. **配置文件**：在项目根目录创建 `ts-json-schema-generator.json`，指定入口文件、要生成的类型以及编译选项，例如：  
   ```json
   {
     "path": "src/**/*.ts",
     "type": "*",
     "skipTypeCheck": false,
     "expose": "all",
     "topRef": true,
     "jsDoc": "extended"
   }
   ```
3. **脚本化生成**：在 `package.json` 中添加脚本：  
   ```json
   "scripts": {
     "gen:schema": "ts-json-schema-generator -p tsconfig.json -o schema.json"
   }
   ```
   在 CI 中执行 `npm run gen:schema`，将生成的 `schema.json` 交给后续的校验或文档工具。  
4. **增量使用**：如果只需要对部分类型生成 schema，可在代码中使用 `/** @jsonSchema */` 注释或在配置里指定 `type`，实现按需生成，降低构建开销。

**生产可用性**  
- **活跃度**：截至 2026‑07‑02，仓库最近一次提交在当日，拥有 1.7k+ Stars、237 Forks，表明社区活跃且维护及时。  
- **生态兼容**：基于官方 TypeScript 编译器 API，兼容最新的 TS 版本，生成的 schema 完全符合 JSON Schema 标准，可无缝接入 AJV、Fastify、NestJS 等后端框架以及前端表单库。  
- **风险**：许可证为 MIT，商业使用无障碍；暂无已知重大安全漏洞。建议在正式上线前通过内部安全审计确认依赖链的完整性，并在 CI 中加入 schema 生成与校验步骤，以确保生成过程的可重复性。  

综上，vega/ts-json-schema-generator 已具备高生产就绪度，适合作为 TypeScript 项目统一数据模型的核心组件，先在小范围（如单个微服务或内部工具）进行 PoC 验证，确认工作流后即可推广到全链路生产环境。

## 🧭 Practical evaluation

**Value:** vega/ts-json-schema-generator may be useful when its README and activity match a concrete workflow.

**Best use cases**

- Not enough metadata yet.

**Integration notes:** Looks feasible to evaluate, but integration should start with a small proof of concept and README check.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 1711 GitHub stars
- 237 forks
- updated 2026-07-02
- primary language: TypeScript
- 4 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 59/100 |
| stars | 69/100 |
| topics | 50/100 |
| outlook | 54/100 |
| quality | 62/100 |
| recency | 40/100 |
| adoption | 66/100 |
| production | 56/100 |
| usefulness | 42/100 |
| integration | 46/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 0/100 |

---

<sub>🔭 Discovered 2026-07-02 · [View on GitHub](https://github.com/vega/ts-json-schema-generator) · [← Back to Misc](./README.md)</sub>
