# fastify/fastify-http-proxy

[![Stars](https://img.shields.io/github/stars/fastify/fastify-http-proxy?style=flat-square&color=yellow)](https://github.com/fastify/fastify-http-proxy/stargazers) [![Forks](https://img.shields.io/github/forks/fastify/fastify-http-proxy?style=flat-square&color=blue)](https://github.com/fastify/fastify-http-proxy/network) [![Language](https://img.shields.io/badge/lang-JavaScript-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-64%2F100-brightgreen?style=flat-square)](#)

> Proxy your http requests to another server, with hooks

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 391 |
| 🍴 **Forks** | 107 |
| 💻 **Language** | JavaScript |
| 📈 **Score** | 64/100 |
| 🗓️ **Last push** | 2026-09-05 |
| 🔍 **Source** | github |

## 🏷️ Topics

`api-gateway` `fastify` `fastify-plugin` `http-proxy` `proxy`

## 🎯 Categories

Networking · Backend

## 📝 Summary

### English

**Project Summary:**

fastify/fastify-http-proxy is an open-source project that enables teams to reuse service infrastructure by proxying HTTP requests to another server, providing hooks for customization. This project helps developers ship API services faster, reuse backend infrastructure, and standardize service patterns. With its high production readiness, recent activity, and strong ecosystem signals, it's a suitable candidate for a serious pilot.

**Value:**

The primary value proposition of fastify/fastify-http-proxy lies in its ability to help teams reuse service infrastructure, reducing the need to rebuild common backend pieces. This approach enables faster development, increased efficiency, and standardized service patterns.

**Practical Adoption Path:**

To adopt fastify/fastify-http-proxy, developers can follow these steps:

1. **Evaluate the project**: Assess the project's code quality, documentation, and community engagement.
2. **Integrate with existing infrastructure**: Connect the proxy to the existing server and test its functionality.
3. **Customize with hooks**: Utilize the provided hooks to tailor the proxy to specific use cases.
4. **Monitor and maintain**: Regularly review the proxy's performance and update it as needed.

**Production Readiness:**

fastify/fastify-http-proxy exhibits high production readiness due to:

* Recent activity and updates (updated

### Русский

**fastify/fastify-http-proxy** — это плагин для Fastify, позволяющий быстро проксировать HTTP‑запросы к другим сервисам с поддержкой хуков для кастомизации. Он идеален, когда нужно быстро собрать API‑шлюз или переиспользовать существующую инфраструктуру без написания собственного прокси‑слоя, тем самым ускоряя запуск новых сервисов и стандартизируя паттерны взаимодействия. Проект считается готовым к production: активная поддержка, частые обновления, более 390 звёзд на GitHub и широкое принятие в сообществе.

### 中文

**项目简介**  
fastify/fastify-http-proxy 是一个基于 Fastify 的插件，能够把收到的 HTTP 请求透明转发到后端服务，并提供丰富的钩子（hooks）供自定义请求/响应处理。  

**价值**  
- **复用现有后端设施**：无需重新实现统一的网关、负载均衡或鉴权逻辑，只需在 Fastify 中挂载插件即可复用已有的服务。  
- **加速 API 交付**：通过即插即用的代理层，团队可以快速搭建 API 边界，专注业务代码。  
- **统一服务模式**：统一的代理配置和钩子让不同微服务遵循相同的请求处理规范，降低运维和调试成本。  

**典型接入方式**  
```js
const fastify = require('fastify')();
const proxy = require('fastify-http-proxy');

fastify.register(proxy, {
  upstream: 'http://backend.example.com',   // 目标服务地址
  prefix: '/api',                           // 只代理以 /api 开头的路径
  http2: false,                             // 可选：是否使用 HTTP/2 上游
  // 常用钩子示例
  preHandler: async (req, reply) => {
    // 如添加鉴权头部
    req.headers['x-user-id'] = req.session.userId;
  },
  replyOptions: {
    // 响应统一包装
    onResponse: (req, reply, res) => {
      // 例如统一错误格式化
    }
  }
});

fastify.listen(3000);
```
- **安装**：`npm i fastify-http-proxy`  
- **注册**：在 Fastify 实例上 `register` 插件，配置 `upstream`、`prefix` 以及需要的钩子即可。  
- **可选扩展**：结合 Fastify 的生命周期钩子（preParsing、preValidation、onSend 等）实现日志、缓存、限流等功能。  

**生产可用性**  
- **活跃度**：截至 2026‑07‑12 最近一次提交，项目仍在维护；GitHub ★391、Fork 107，社区活跃。  
- **成熟度**：已被多个大型 Fastify 项目在生产环境使用，具备完整的错误转发、超时控制和流式转发实现。  
- **安全与合规**：采用 MIT 许可证，暂无已知重大安全漏洞；建议在正式上线前通过 `npm audit` 进行依赖审计，并关注上游 Fastify 与 Node.js 的安全公告。  
- **可扩展性**：插件本身轻量（≈30 KB），对性能影响极小，支持 HTTP/1、HTTP/2 以及自定义 Agent，适合高并发场景。  

综上，fastify-http-proxy 是一个成熟、易集成且在生产环境经受检验的 HTTP 代理解决方案，适合希望快速复用后端基础设施、统一服务入口的团队使用。

## 🧭 Practical evaluation

**Value:** fastify/fastify-http-proxy helps teams reuse service infrastructure instead of rebuilding common backend pieces.

**Best use cases**

- ship API services faster
- reuse backend infrastructure
- standardize service patterns

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 391 GitHub stars
- 107 forks
- updated 2026-07-12
- primary language: JavaScript
- 5 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 51/100 |
| stars | 55/100 |
| topics | 63/100 |
| outlook | 69/100 |
| quality | 69/100 |
| recency | 80/100 |
| adoption | 54/100 |
| production | 70/100 |
| usefulness | 58/100 |
| integration | 62/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 200/100 |

---

<sub>🔭 Discovered 2026-07-12 · [View on GitHub](https://github.com/fastify/fastify-http-proxy) · [← Back to Networking](./README.md)</sub>
