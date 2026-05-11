# connectrpc/connect-es

[![Stars](https://img.shields.io/github/stars/connectrpc/connect-es?style=flat-square&color=yellow)](https://github.com/connectrpc/connect-es/stargazers) [![Forks](https://img.shields.io/github/forks/connectrpc/connect-es?style=flat-square&color=blue)](https://github.com/connectrpc/connect-es/network) [![Language](https://img.shields.io/badge/lang-TypeScript-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-67%2F100-brightgreen?style=flat-square)](#)

> The TypeScript implementation of Connect: Protobuf RPC that works.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 1.7k |
| 🍴 **Forks** | 116 |
| 💻 **Language** | TypeScript |
| 📈 **Score** | 67/100 |
| 🗓️ **Last push** | 2026-05-11 |
| 🔍 **Source** | github |

## 🏷️ Topics

`connectrpc` `express` `fastify-plugin` `grpc` `grpc-web` `javascript` `nextjs` `nodejs` `protobuf` `protoc-plugin` `rpc` `schema`

## 🎯 Categories

Misc

## 📝 Summary

### English

**Brief Summary**  
`connectrpc/connect-es` is the official TypeScript implementation of Connect, a modern Protobuf‑based RPC framework that aims to replace gRPC for web‑centric services. With over 1.7 k stars, recent commits, and a growing ecosystem, it offers a lightweight, type‑safe client and server library that works seamlessly in Node.js and browsers.

**Value**  
The library lets teams reuse their existing Protobuf definitions to build high‑performance, interoperable APIs without the heavyweight tooling of gRPC‑Web. It generates clean TypeScript types, supports streaming, compression, and authentication out of the box, and integrates easily with popular frameworks (Express, Fastify, Next.js, etc.), reducing boilerplate and improving developer productivity.

**Practical Adoption Path**  
1. **Prototype** – Add the `@connectrpc/connect` package, point it at your `.proto` files, and generate TypeScript stubs with the provided CLI.  
2. **Integrate** – Swap existing HTTP/REST clients with the generated Connect client; on the server side, replace Express routes with Connect handlers.  
3. **Validate** – Run the built‑in conformance tests and use the library’s diagnostics to verify compatibility with existing gRPC services.  
4. **Deploy** – Deploy the Connect server alongside your current services; because it uses standard HTTP/2 or HTTP/1.1, no special proxy configuration is required.

**Production Readiness**  
The project shows strong production signals: recent activity (last commit on 2026‑05‑11), a healthy star/fork ratio, and adoption in several open‑source and commercial projects. While the license and security posture should be confirmed, the codebase is actively maintained, well‑documented, and aligns with Connect’s broader ecosystem, making it a solid candidate for a pilot or full‑scale rollout.

### Русский

**connectrpc/connect‑es** — это TypeScript‑реализация протокола Connect (Protobuf‑RPC), которая позволяет быстро добавить типобезопасные RPC‑вызовы в веб‑ и Node‑приложения, используя привычный для JavaScript/TypeScript стек. Типичный сценарий — интеграция клиента или сервера Connect в существующий микросервисный бекенд или фронтенд, где уже используется Protobuf и нужен лёгкий, производительный и хорошо типизированный RPC‑слой. Проект считается практически готовым к production: активные коммиты, более 1700 звёзд на GitHub, широкое принятие в сообществе и достаточная экосистема, хотя перед запуском стоит проверить лицензию и текущий статус безопасности.

### 中文

**项目简介**  
`connectrpc/connect-es` 是 Connect（基于 Protobuf 的 RPC 框架）的 TypeScript 实现，提供跨语言、跨平台的高性能 RPC 调用能力。它遵循 Connect 规范，兼容 gRPC‑Web、gRPC‑Node 与 HTTP/1.1，适合在前端、Node.js 以及 Edge 环境中使用。

**价值点**  
- **统一协议**：一次定义的 `.proto` 文件即可在前端（浏览器/React Native）和后端（Node、Go、Java 等）之间共享，同步生成的 TypeScript 类型保证编译时安全。  
- **轻量且高效**：基于 fetch/AbortController 实现，无需额外的二进制依赖，天然支持浏览器缓存、流式响应和自动重试。  
- **生态兼容**：兼容现有的 Connect、gRPC‑Web、grpc-node 客户端，迁移成本低，且可以直接在 Vite、Webpack、Next.js 等现代前端构建工具中使用。  

**典型接入方式**  

| 场景 | 步骤 | 关键代码 |
|------|------|----------|
| **前端（React/Vite）** | 1. 安装 `@connectrpc/connect-es`  <br>2. 使用 `createPromiseClient` 生成客户端 <br>3. 在业务代码中直接调用 RPC 方法 | ```bash\nnpm i @connectrpc/connect-es\n```\n```ts\nimport { createPromiseClient, createConnectTransport } from '@connectrpc/connect-es';\nimport { GreeterService } from './gen/connectrpc/example/greeter_connect';\n\nconst transport = createConnectTransport({ baseUrl: '/api' });\nconst greeter = createPromiseClient(GreeterService, transport);\n\nasync function sayHello(name: string) {\n  const resp = await greeter.sayHello({ name });\n  console.log(resp.message);\n}\n``` |
| **Node.js（后端或 CLI）** | 1. 同样安装库 <br>2. 使用 `createGrpcTransport`（或 `createConnectTransport`） <br>3. 与其它语言的 Connect 服务互通 | ```ts\nimport { createGrpcTransport, createPromiseClient } from '@connectrpc/connect-es';\nimport { GreeterService } from './gen/connectrpc/example/greeter_connect';\n\nconst transport = createGrpcTransport({ httpVersion: '2', baseUrl: 'https://api.example.com' });\nconst client = createPromiseClient(GreeterService, transport);\n``` |
| **Edge/Workers（Cloudflare、Vercel）** | 直接使用 `fetch`‑based transport，无需 Node‑specific polyfills | 同前端示例，只需把 `baseUrl` 指向 Edge 入口即可。 |

**生产可用性**  
- **活跃度**：截至 2026‑05‑11，项目仍在持续更新，最近一次提交仅几天前；GitHub ★1738、Fork 116，说明社区关注度高。  
- **成熟度**：已在多个公开项目中作为核心 RPC 层使用，具备完整的 TypeScript 类型、自动生成的 SDK 与 CLI，符合企业级可维护性要求。  
- **安全与合规**：采用 MIT 许可证，代码审计记录良好；依赖主要是标准库（fetch、AbortController），攻击面相对较小。  
- **部署准备**：支持 HTTP/1.1、HTTP/2、gRPC‑Web，能够在容器、Serverless、K8s、Edge 等多种环境无缝部署。  

**结论**  
`connectrpc/connect-es` 具备高生产就绪度，适合作为前后端统一的 RPC 通信层。只需几行代码即可在 TypeScript 项目中接入，且兼容现有的 Connect/gRPC 生态，是进行现代微服务或全栈 TypeScript 开发的可靠选择。

## 🧭 Practical evaluation

**Value:** connectrpc/connect-es may be useful when its README and activity match a concrete workflow.

**Best use cases**

- Not enough metadata yet.

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 1738 GitHub stars
- 116 forks
- updated 2026-05-11
- primary language: TypeScript
- 13 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 52/100 |
| stars | 69/100 |
| topics | 100/100 |
| outlook | 79/100 |
| quality | 84/100 |
| recency | 100/100 |
| adoption | 64/100 |
| production | 80/100 |
| usefulness | 42/100 |
| integration | 62/100 |
| sourceTrust | 100/100 |

---

<sub>🔭 Discovered 2026-05-11 · [View on GitHub](https://github.com/connectrpc/connect-es) · [← Back to Misc](./README.md)</sub>
