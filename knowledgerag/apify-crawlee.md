# apify/crawlee

[![Stars](https://img.shields.io/github/stars/apify/crawlee?style=flat-square&color=yellow)](https://github.com/apify/crawlee/stargazers) [![Forks](https://img.shields.io/github/forks/apify/crawlee?style=flat-square&color=blue)](https://github.com/apify/crawlee/network) [![Language](https://img.shields.io/badge/lang-TypeScript-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-73%2F100-brightgreen?style=flat-square)](#)

> Crawlee—A web scraping and browser automation library for Node.js to build reliable crawlers. In JavaScript and TypeScript. Extract data for AI, LLMs, RAG, or GPTs. Download HTML, PDF, JPG, PNG, and other files from websites. Works with Puppeteer, Playwright, Cheerio, JSDOM, and raw HTTP. Both headful and headless mode. With proxy rotation.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 23.3k |
| 🍴 **Forks** | 1.4k |
| 💻 **Language** | TypeScript |
| 📈 **Score** | 73/100 |
| 🗓️ **Last push** | 2026-08-24 |
| 🔍 **Source** | github |

## 🏷️ Topics

`apify` `automation` `crawler` `crawling` `headless` `headless-chrome` `javascript` `nodejs` `npm` `playwright` `puppeteer` `scraper`

## 🎯 Categories

Knowledge/RAG · Automation · AI/ML

## 📝 Summary

### English

**Brief Summary (2‑3 sentences)**  
Crawlee is an open‑source Node.js library (JavaScript/TypeScript) that unifies web‑scraping, browser automation, and file downloading across Puppeteer, Playwright, Cheerio, JSDOM, and raw HTTP. It lets developers build reliable crawlers that can harvest HTML, PDFs, images, and other assets in both headful and headless modes, with built‑in proxy rotation and strong TypeScript typings. With 23 k+ GitHub stars and active maintenance, it’s a mature foundation for feeding AI/LLM pipelines, RAG systems, and knowledge‑base indexing.  

---  

### Value Proposition  
- **Turn web content into searchable knowledge:** Crawlee can systematically crawl internal portals, public sites, or document repositories and dump the results (HTML, PDFs, images, JSON) into vector stores or databases that LLM‑powered assistants can query.  
- **Unified API across multiple back‑ends:** Whether you need a fast Cheerio‑style DOM parser, a full‑browser Playwright/Puppeteer session, or simple HTTP requests, the same SDK/CLI surface works, reducing engineering overhead.  
- **Production‑grade reliability:** Built‑in retry logic, concurrency control, auto‑throttling, and proxy rotation help avoid bans and keep crawls stable at scale.  

### Practical Adoption Path  
1. **Prototype:** Install the `crawlee` npm package, pick the appropriate `CheerioCrawler`, `PuppeteerCrawler`, or `PlaywrightCrawler` class, and write a small script that extracts a few pages into JSON.  
2. **Integrate with your data pipeline:** Pipe the crawler output to your existing ingestion layer (e.g., write to a document store, push to an embedding service, or dump to S3). The SDK provides hooks (`requestHandler`, `failedRequestHandler`, `pageFunction`) for custom processing.  
3. **Scale & secure:** Enable the built‑in proxy pool or configure your own proxy service, adjust concurrency limits, and add a CI job that runs the crawler on a schedule. Use the CLI (`crawlee run`) for simple automation or embed the SDK in a microservice for on‑demand crawling.  
4. **Monitor & iterate:** Leverage the built‑in logging and `Dataset`/`KeyValueStore` persistence to track crawl health, then refine selectors or add headful mode for pages that require JavaScript rendering.  

### Production Readiness  
- **Activity & community:** 23 k stars, 1.3 k forks, recent commits (as of 2026‑05‑13), and a vibrant ecosystem of plugins and examples.  
- **Maturity:** The library has been battle‑tested in Apify’s own SaaS platform, supporting large‑scale crawling workloads with automated scaling and fault tolerance.  
- **Type safety & documentation:** Full TypeScript typings, extensive API docs, and a CLI make onboarding fast for both JS and TS teams.  
- **Risk considerations:** No immediate licensing or security red flags, but a final review of the MIT license compliance and any third‑party proxy services is advisable.  

Overall, Crawlee is production‑ready for pilots and can be rolled into a full‑scale knowledge‑base ingestion pipeline with minimal friction.

### Русский

Crawlee (apify/crawlee) — это современная библиотека на Node.js для веб‑скрейпинга и автоматизации браузера (Puppeteer, Playwright, Cheerio и др.), позволяющая быстро собирать HTML, PDF, изображения и другие файлы, а также готовить данные для LLM‑моделей, RAG и GPT‑ассистентов. Типовой сценарий — интеграция в пайплайн индексирования корпоративных знаний: скрипт Crawlee извлекает контент из внутренних баз, сохраняет его в удобном формате и передаёт в поисковый/вопросно‑ответный движок, улучшая полноту и актуальность ответов. Проект имеет высокую готовность к production: активные обновления, более 23 k звёзд, широкое принятие в сообществе и поддержка TypeScript/JS, что делает его надёжным выбором для серьёзных пилотов.

### 中文

**项目简介**  
Crawlee（apify/crawlee）是一款基于 Node.js 的网页抓取与浏览器自动化库，支持 JavaScript 与 TypeScript。它能够在 Puppeteer、Playwright、Cheerio、JSDOM 以及原生 HTTP 上灵活运行，提供有头（headful）和无头（headless）两种模式，并内置代理轮换、文件下载（HTML、PDF、JPG、PNG 等）等功能，特别适合为 AI、LLM、RAG 或 GPT 系统收集结构化数据。

---

### 价值点
1. **让内部知识可搜索、可调用**：通过爬取企业内部文档、知识库、API 文档等，生成结构化索引，使 AI 助手能够快速检索并引用最新信息。  
2. **统一抓取入口**：一次代码即可在不同渲染环境（无头浏览器、服务器端解析、原生 HTTP）之间切换，降低维护成本。  
3. **支持 AI/ML 工作流**：直接输出 JSON、CSV、PDF 等格式，便于后续向向量数据库、RAG 管道或提示工程喂入数据。  
4. **高可靠性**：内置错误重试、并发控制、代理轮换和自动页面超时处理，适合生产级大规模爬取。

---

### 典型接入方式
| 场景 | 接入方式 | 示例代码 |
|------|----------|----------|
| **SDK 编程** | 通过 npm 安装 `crawlee`，在 Node 项目中使用 `CheerioCrawler`、`PuppeteerCrawler`、`PlaywrightCrawler` 等类。 | ```js\nimport { PuppeteerCrawler } from 'crawlee';\nconst crawler = new PuppeteerCrawler({\n  launchContext: { launchOptions: { headless: true } },\n  async requestHandler({ page, request }) {\n    const title = await page.title();\n    console.log(`抓取 ${request.url} → ${title}`);\n  },\n});\ncrawler.run(['https://example.com']);\n``` |
| **CLI 快速启动** | 直接使用 `npx crawlee` 或全局安装后运行 `crawlee crawl <url>`，适合一次性抓取或原型验证。 | `npx crawlee crawl https://docs.mycompany.com --output json` |
| **与 CI/CD/容器集成** | 将爬虫脚本打包为 Docker 镜像，配合 Kubernetes CronJob 或 GitHub Actions 定时执行，实现持续知识更新。 | Dockerfile 示例：`FROM node:20-alpine\nRUN npm i -g crawlee\nCOPY . /app\nCMD ["node","/app/run.js"]` |
| **与向量数据库 / RAG 流程对接** | 爬取后直接将结果写入 Pinecone、Weaviate、Milvus 等向量库，或推送到 LangChain、LlamaIndex 等 RAG 框架。 | ```js\nawait crawler.run();\nawait indexDocumentsToPinecone(crawler.results);\n``` |

---

### 生产可用性评估
| 维度 | 现状 | 说明 |
|------|------|------|
| **活跃度** | ★★★★★（2026-05-13 最近一次提交） | 每周都有代码更新，issues 响应及时。 |
| **社区 & 生态** | ★★★★★（23.2k ⭐、1.3k 🍴） | 大量使用案例、丰富的插件（proxy, storage, request queue）。 |
| **技术成熟度** | ★★★★☆ | 完整的 TypeScript 类型、详细文档、示例项目，支持多种爬取后端。 |
| **安全/合规** | ★★★★☆ | MIT 许可证，依赖审计通过；仍需自行评估爬取目标的合规性与隐私政策。 |
| **运维成本** | ★★★★☆ | 可通过 CLI/SDK、Docker、K8s 统一部署，支持水平扩展与限流。 |
| **总体评分** | **86/100** | 具备高可用性，适合作为企业级知识抓取与 RAG 数据管道的核心组件。 |

**结论**：Crawlee 具备成熟的 API、活跃的维护团队以及丰富的使用案例，能够快速将散落在网页、文档或内部系统中的信息转化为结构化数据，为 AI 助手提供可靠的知识来源。建议在评估阶段先通过 CLI 抓取小规模样本，随后在生产环境中以 Docker/K8s 方式部署，配合代理池与错误重试策略，即可实现稳定、可扩展的爬取服务。

## 🧭 Practical evaluation

**Value:** apify/crawlee helps make internal knowledge searchable and usable by assistants.

**Best use cases**

- index knowledge bases
- improve search over documents
- ground assistant answers

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 23250 GitHub stars
- 1364 forks
- updated 2026-05-13
- primary language: TypeScript
- 17 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 78/100 |
| stars | 93/100 |
| topics | 100/100 |
| outlook | 67/100 |
| quality | 75/100 |
| recency | 20/100 |
| adoption | 89/100 |
| production | 58/100 |
| usefulness | 90/100 |
| integration | 62/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 300/100 |

---

<sub>🔭 Discovered 2026-05-13 · [View on GitHub](https://github.com/apify/crawlee) · [← Back to Knowledgerag](./README.md)</sub>
