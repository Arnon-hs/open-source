# craigmccaskill/posthorn

[![Stars](https://img.shields.io/github/stars/craigmccaskill/posthorn?style=flat-square&color=yellow)](https://github.com/craigmccaskill/posthorn/stargazers) [![Forks](https://img.shields.io/github/forks/craigmccaskill/posthorn?style=flat-square&color=blue)](https://github.com/craigmccaskill/posthorn/network) [![Language](https://img.shields.io/badge/lang-Go-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-65%2F100-brightgreen?style=flat-square)](#)

> Self-hosted email gateway between your apps and a transactional mail provider (Postmark, Resend, Mailgun, AWS SES, or outbound-SMTP). Three ingress shapes (HTTP form, HTTP API, SMTP). One Docker container, one TOML config.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 203 |
| 🍴 **Forks** | 10 |
| 💻 **Language** | Go |
| 📈 **Score** | 65/100 |
| 🗓️ **Last push** | 2026-08-24 |
| 🔍 **Source** | github |

## 🏷️ Topics

`docker` `email` `email-gateway` `go` `homelab` `mail-gateway` `postmark` `self-hosted` `smtp-relay` `transactional-email`

## 🎯 Categories

DevOps/Infra

## 📝 Summary

### English

**Brief summary**  
Posthorn is a single‑container, Go‑based email gateway that sits between your applications and any transactional mail provider (Postmark, Resend, Mailgun, AWS SES, or an outbound SMTP server). It accepts inbound mail via three “ingress shapes” – an HTTP form, a REST‑style HTTP API, or raw SMTP – and forwards the messages to the configured provider, all driven by a tiny TOML configuration file.

**Value**  
- **Unified interface**: Developers can switch providers or add a new one without changing application code, because Posthorn abstracts the provider’s API behind a consistent HTTP/SMTP endpoint.  
- **Fast AI‑enabled prototypes**: By handling email delivery reliably, teams can focus on building AI features (e.g., RAG pipelines, agent notifications) without wrestling with provider‑specific quirks.  
- **Low operational overhead**: One Docker image and a single config file make deployment trivial in any container‑orchestrated environment (Docker Compose, Kubernetes, Nomad, etc.).  

**Practical adoption path**  
1. **Deploy** – Pull the official Docker image, mount a TOML file with your chosen provider credentials, and run the container (or add it to your existing compose/k8s stack).  
2. **Configure ingress** – Choose the appropriate ingress shape for your app (e.g., HTTP API for microservices, SMTP for legacy systems).  
3. **Update your app** – Point your email‑sending code to the Posthorn endpoint; no code changes are needed for the underlying provider.  
4. **Iterate** – Swap providers or add new ones by editing the TOML and restarting the container; no redeployment of the consuming services.  

**Production readiness**  
- **Activity & community**: 203 ★, recent commit (2026‑07‑04), 10 forks, and active issue discussions indicate a healthy maintainer base.  
- **Stability**: The single‑binary, statically compiled Go binary reduces runtime dependencies; the Docker image is immutable and easy to version.  
- **Observability**: Built‑in logging and health‑check endpoints make monitoring straightforward in production environments.  
- **Risk considerations**: The license and security posture appear clean, but a final audit of the repository’s licensing terms and any disclosed vulnerabilities is advisable before a critical rollout.  

Overall, Posthorn is a mature, low‑friction component that can be dropped into existing stacks to standardize email delivery while freeing developers to concentrate on higher‑level AI and business logic.

### Русский

Резюме проекта craigmccaskill/posthorn:

Проект craigmccaskill/posthorn представляет собой автономный почтовый шлюз, который позволяет соединять приложения с провайдерами транзакционных сообщений (Postmark, Resend, Mailgun, AWS SES или исходящий SMTP). Этот проект предлагает три формы входа (HTTP-форм, HTTP-API, SMTP) и предоставляет одну контейнерную установку Docker и одну конфигурацию в формате TOML. 

Проект особенно полезен для добавления функциональности AI без создания собственного набора моделей. Обычная сценарий внедрения включает в себя прототипирование функций AI, построение рабочих процессов RAG или агентов и оценку инструментов для моделей.

Проект демонстрирует высокий уровень готовности к производству, поскольку он имеет свежую активность, адопцию и сигналы экосистемы, которые достаточно сильны для серьезного пилота. Однако перед внедрением необходимо тщательно проверить лицензию, безопасность и активных поддерживающих разработчиков.

### 中文

**项目简介**

craigmccaskill/posthorn 是一个开源项目，用于在应用程序和事务性邮件提供商（Postmark、Resend、Mailgun、AWS SES 或 SMTP）之间建立一个自主的邮件网关。它支持三种不同的接入方式（HTTP 表单、HTTP API 和 SMTP），并且只需要一个 Docker 容器和一个 TOML 配置文件。

**价值**

该项目的价值在于，它可以帮助开发者在不从零开始构建 AI 模型堆栈的情况下，轻松地添加 AI 能力。它适用于以下场景：

* prototype AI 特性
* 构建 RAG 或代理工作流
* 评估模型工具

**典型接入方式**

该项目提供三种接入方式：

1. HTTP 表单：用户可以通过 HTTP 表单提交邮件信息。
2. HTTP API：开发者可以通过 HTTP API 接口发送邮件请求。
3. SMTP：该项目可以接收 SMTP 邮件并转发到事务性邮件提供商。

**生产可用性**

该项目的生产可用性很高，主要原因是：

* 最

## 🧭 Practical evaluation

**Value:** craigmccaskill/posthorn helps add AI capability without starting from a blank model stack.

**Best use cases**

- prototype AI features
- build RAG or agent workflows
- evaluate model tooling

**Integration notes:** Looks straightforward to evaluate: it exposes implementation signals such as API/SDK/CLI, language metadata, or focused topics.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 203 GitHub stars
- 10 forks
- updated 2026-07-04
- primary language: Go
- 10 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 26/100 |
| stars | 49/100 |
| topics | 100/100 |
| outlook | 59/100 |
| quality | 59/100 |
| recency | 40/100 |
| adoption | 43/100 |
| production | 59/100 |
| usefulness | 74/100 |
| integration | 78/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 100/100 |

---

<sub>🔭 Discovered 2026-07-04 · [View on GitHub](https://github.com/craigmccaskill/posthorn) · [← Back to DevOps & Infra](./README.md)</sub>
