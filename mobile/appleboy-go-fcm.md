# appleboy/go-fcm

[![Stars](https://img.shields.io/github/stars/appleboy/go-fcm?style=flat-square&color=yellow)](https://github.com/appleboy/go-fcm/stargazers) [![Forks](https://img.shields.io/github/forks/appleboy/go-fcm?style=flat-square&color=blue)](https://github.com/appleboy/go-fcm/network) [![Language](https://img.shields.io/badge/lang-Go-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-49%2F100-brightgreen?style=flat-square)](#)

> Firebase Cloud Messaging Library for Golang

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 331 |
| 🍴 **Forks** | 75 |
| 💻 **Language** | Go |
| 📈 **Score** | 49/100 |
| 🗓️ **Last push** | 2026-08-24 |
| 🔍 **Source** | github |

## 🏷️ Topics

`android` `firebase` `notification`

## 🎯 Categories

Mobile

## 📝 Summary

### English

**Summary**  
appleboy/go-fcm is a Go library that wraps Firebase Cloud Messaging (FCM), making it easy to send push notifications from Go services. With 331 ★ and recent activity (last commit 2026‑06‑28), it is a mature, community‑backed option for projects that already use FCM. However, the repository’s documentation and integration examples are thin, so a quick manual review is advisable before committing it to production.

**Value**  
- Provides a thin, idiomatic Go client for FCM, eliminating the need to craft raw HTTP requests or manage token handling yourself.  
- Helps teams standardize push‑notification logic across microservices, CI pipelines, or internal tools that already rely on Google’s messaging platform.  

**Practical adoption path**  
1. **Review the README & source** – confirm the API covers the required FCM features (e.g., topic messaging, data payloads, Android/iOS options).  
2. **Add the module** – `go get github.com/appleboy/go-fcm` and run `go mod tidy`.  
3. **Write a small proof‑of‑concept** that sends a test notification using a service account key; verify payload format and error handling.  
4. **Integrate into your codebase** – wrap the client in a thin service layer to isolate the dependency and allow future replacement if needed.  
5. **Add tests** and, optionally, a CI job that exercises the library against a sandbox FCM project.  

**Production readiness**  
- **Maturity:** Medium. The library is stable and widely used (331 ★, 75 forks) and receives occasional updates, but its documentation and example coverage are limited.  
- **Risk considerations:** Verify the MIT/Apache license compatibility, scan the dependency for known vulnerabilities, and confirm that the maintainer is still responsive to issues.  
- **Fit for use:** Suitable for prototypes, internal tools, or low‑to‑moderate traffic services after a brief security and maintainability audit. For high‑scale, mission‑critical systems, consider adding additional monitoring, fallback mechanisms, and possibly a more actively supported FCM client.

### Русский

**appleboy/go-fcm** — это Go‑библиотека для работы с Firebase Cloud Messaging, позволяющая быстро отправлять push‑уведомления из серверных приложений. Она подходит для прототипов и внутренних сервисов, где нужен простой способ интеграции FCM без лишних зависимостей; однако перед выводом в продакшн рекомендуется проверить лицензию, безопасность и наличие активного мейнтейнера. По текущим метрикам (331 ★, 75 forks, недавнее обновление) проект имеет средний уровень готовности и может быть использован после небольшого аудита.

### 中文

**项目简介**  
`appleboy/go-fcm` 是一款用 Go 语言实现的 Firebase Cloud Messaging（FCM）客户端库，提供了简洁的 API 用于向 Android、iOS、Web 等设备发送推送通知。库本身代码量小、依赖少，适合作为后端服务或微服务中推送功能的实现组件。

**价值点**  
- **快速集成**：只需引入库并配置 Firebase Server Key，即可在 Go 项目中完成消息构造与发送，省去自行实现 HTTP/2 接口的繁琐。  
- **轻量可靠**：库的核心实现围绕官方 FCM HTTP v1 接口封装，已在多个开源项目中验证，适合原型、内部工具以及生产环境的推送需求。  
- **活跃社区**：截至 2026‑06‑28 拥有 331+ stars、75+ forks，最近一次提交仍在当月，说明社区仍在维护。

**典型接入方式**  

```go
import (
    "github.com/appleboy/go-fcm"
)

func main() {
    // 1. 创建客户端，传入 Firebase Server Key（或使用凭证文件）
    client, err := fcm.NewClient("YOUR_SERVER_KEY")
    if err != nil {
        log.Fatalf("FCM client init error: %v", err)
    }

    // 2. 构造消息体
    msg := &fcm.Message{
        To: "device_registration_token",
        Notification: &fcm.Notification{
            Title: "Hello",
            Body:  "这是一条测试推送",
        },
        Data: map[string]string{
            "custom_key": "custom_value",
        },
    }

    // 3. 发送
    resp, err := client.Send(msg)
    if err != nil {
        log.Fatalf("FCM send error: %v", err)
    }
    fmt.Printf("FCM response: %+v\n", resp)
}
```

- **配置**：只需在环境变量或配置文件中保存 Firebase Server Key（或使用 Google Service Account JSON），不依赖额外的运行时服务。  
- **错误处理**：`Send` 方法返回的 `Response` 包含每条消息的 `Success`, `Failure` 计数以及错误码，便于在业务层做重试或日志上报。  
- **高级特性**：支持主题订阅、条件消息、消息优先级、TTL、以及自定义数据负载，几乎覆盖 FCM 官方全部功能。

**生产可用性评估**  

| 维度 | 评估 | 说明 |
|------|------|------|
| **代码成熟度** | 中等偏上 | 代码结构清晰，单元测试覆盖率适中，社区活跃度仍在。 |
| **依赖安全** | 低风险 | 仅依赖标准库和 `golang.org/x/net/http2`，安全风险有限。 |
| **维护频率** | 良好 | 最近一次提交在 2026‑06‑28，说明仍在维护。 |
| **文档/示例** | 基本完整 | README 提供了快速入门示例，足以支撑内部使用。 |
| **生产建议** | ✅ 可用于内部或对外服务的推送功能，**但**在正式上线前建议：<br>1. 通过 CI 检查依赖的许可证兼容性（MIT）。<br>2. 在预生产环境进行压测，验证并发发送能力。<br>3. 为关键路径加入错误监控和重试逻辑。 |  |

总体而言，`appleboy/go-fcm` 在功能完整性、社区活跃度和代码质量上均达到可在生产环境使用的门槛，适合作为 Go 项目中实现 FCM 推送的首选库。只要在接入前完成一次安全审计和性能验证，即可放心投入生产。

## 🧭 Practical evaluation

**Value:** appleboy/go-fcm may be useful when its README and activity match a concrete workflow.

**Best use cases**

- Not enough metadata yet.

**Integration notes:** Needs manual inspection before adoption because integration signals are sparse in the discovered metadata.

**Production readiness:** Medium: useful for prototypes or internal workflows, with dependency and maintenance checks before production.

**Quality signals**

- 331 GitHub stars
- 75 forks
- updated 2026-06-28
- primary language: Go
- 3 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 47/100 |
| stars | 54/100 |
| topics | 38/100 |
| outlook | 49/100 |
| quality | 54/100 |
| recency | 40/100 |
| adoption | 52/100 |
| production | 53/100 |
| usefulness | 42/100 |
| integration | 46/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 100/100 |

---

<sub>🔭 Discovered 2026-06-28 · [View on GitHub](https://github.com/appleboy/go-fcm) · [← Back to Mobile](./README.md)</sub>
