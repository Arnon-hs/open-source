# bitnami/sealed-secrets

[![Stars](https://img.shields.io/github/stars/bitnami/sealed-secrets?style=flat-square&color=yellow)](https://github.com/bitnami/sealed-secrets/stargazers) [![Forks](https://img.shields.io/github/forks/bitnami/sealed-secrets?style=flat-square&color=blue)](https://github.com/bitnami/sealed-secrets/network) [![Language](https://img.shields.io/badge/lang-Go-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-74%2F100-brightgreen?style=flat-square)](#)

> A Kubernetes controller and tool for one-way encrypted Secrets

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 9.2k |
| 🍴 **Forks** | 774 |
| 💻 **Language** | Go |
| 📈 **Score** | 74/100 |
| 🗓️ **Last push** | 2026-09-05 |
| 🔍 **Source** | github |

## 🏷️ Topics

`devops-workflow` `encrypt-secrets` `gitops` `kubernetes` `kubernetes-secrets`

## 🎯 Categories

Automation · DevOps/Infra

## 📝 Summary

### English

**Brief Summary (2‑3 sentences)**  
Bitnami Sealed Secrets is an open‑source Kubernetes controller and CLI that lets you create “sealed” versions of Secrets—encrypted objects that can be safely stored in version control and later decrypted only by the controller running in the cluster. By automating the encryption and de‑cryption steps, it eliminates repetitive manual handling of sensitive data and enables repeatable, Git‑Ops‑friendly workflows.  

**Value**  
- **Automation of secret management** – developers can commit sealed secrets alongside application manifests, removing the need for ad‑hoc `kubectl create secret` commands or manual key distribution.  
- **Safety for GitOps** – sealed secrets are one‑way encrypted, so they can live in public or shared repositories without exposing plaintext credentials.  
- **Consistent, repeatable pipelines** – the controller integrates with CI/CD tools, allowing secrets to be provisioned automatically during deployments or scheduled operational tasks.  

**Practical Adoption Path**  
1. **Proof‑of‑Concept** – Clone the repo, follow the README to install the controller in a test namespace, and generate a sealed secret for a non‑critical credential. Verify that the secret is decrypted correctly by a pod.  
2. **Integrate into CI/CD** – Add the `kubeseal` CLI step to your build pipeline to seal secrets before committing manifests to Git.  
3. **Scale to production namespaces** – Deploy the controller cluster‑wide (or per‑team) with appropriate RBAC, and replace all existing plain‑text `Secret` objects with sealed equivalents.  

**Production Readiness**  
- **Maturity** – 9 163 GitHub stars, 774 forks, frequent commits (last update 2026‑06‑24) and a healthy Go codebase indicate strong community adoption.  
- **Stability** – The controller is widely used in production environments; its API is stable and backward compatible.  
- **Risk Assessment** – No major metadata or licensing issues have been identified, though a final security audit and confirmation of active maintainers are recommended before a full rollout. Overall, the project is considered high‑readiness for a serious pilot in production.

### Русский

**bitnami/sealed-secrets** — это контроллер и CLI‑утилита для Kubernetes, позволяющие хранить и распространять «запечатанные» (one‑way encrypted) Secrets, избавляя команды от ручного шифрования и копирования конфиденциальных данных. Типичный сценарий — внедрение небольшого proof‑of‑concept: установить контроллер в кластер, заменить обычные Secret‑ы на SealedSecret‑ы в CI/CD пайплайне и автоматизировать их расшифровку в runtime, тем самым устраняя повторяющиеся ручные операции. Проект считается почти готовым к продакшену: активная поддержка (обновления до 2026‑06‑24), широкое принятие (9 163 звёзд, 774 форка), зрелый Go‑код и хорошая экосистема, однако перед масштабным rollout стоит окончательно проверить лицензию, безопасность и наличие активных мейнтейнеров.

### 中文

**项目简介**  
`bitnami/sealed-secrets` 是一个基于 Go 实现的 Kubernetes 控制器和 CLI 工具，能够对 Secret 进行单向加密（Sealed Secret），从而在 GitOps 工作流中安全地存储和同步机密数据。  

**价值**  
- **消除手工操作**：开发者只需一次性加密 Secret，后续所有部署都可以直接使用已加密的 SealedSecret，避免了在 CI/CD 流程中手动创建或导入明文 Secret。  
- **实现可重复的流水线**：加密后的对象可以和代码一起提交到 Git，配合 Argo CD、Flux 等 GitOps 工具，实现“代码即配置、配置即部署”。  
- **支持自动化任务**：可在定时任务或自定义控制器中调用 `kubeseal`，实现批量加密、轮转密钥等运维操作。  

**典型接入方式**  
1. **部署控制器**：使用 Helm、Kustomize 或直接 `kubectl apply -f https://github.com/bitnami/sealed-secrets/releases/download/vX.Y.Z/controller.yaml` 将 SealedSecrets 控制器安装到目标集群。  
2. **生成密钥对**：在本地或 CI 环境运行 `kubeseal --fetch-cert > pubkey.pem`，获取集群公开密钥。  
3. **加密 Secret**：使用 `kubeseal --cert pubkey.pem -o yaml < plain-secret.yaml > sealed-secret.yaml` 将普通 Secret 加密为 SealedSecret。  
4. **提交到 Git**：将生成的 `sealed-secret.yaml` 与其他 K8s 资源一起提交，GitOps 工具会自动把它解密并创建真实的 Secret。  
5. **验证**：在集群中执行 `kubectl get sealedsecret` 或 `kubectl get secret` 确认解密成功。  

**生产可用性**  
- **活跃度高**：截至 2026‑06‑24，项目拥有 9,163+ 星、774+ Fork，最近一次提交在同一天，说明维护持续且活跃。  
- **生态兼容**：官方提供 Helm Chart、Kustomize 示例，兼容主流 GitOps 平台（Argo CD、Flux），并已被多家企业在生产环境中使用。  
- **安全性**：采用单向加密，密钥只保存在控制器内部；即使 SealedSecret 泄露，也无法逆向得到明文。  
- **风险**：仍需对许可证（Apache‑2.0）和安全审计报告进行最终确认，确保符合组织合规要求。  

综上，`bitnami/sealed-secrets` 在自动化、DevOps 场景下具备高可用性和易集成的特性，适合作为机密管理的首选 OSS 方案，在小规模 PoC 验证后即可推广到生产环境。

## 🧭 Practical evaluation

**Value:** bitnami/sealed-secrets helps remove repetitive manual operations from a workflow.

**Best use cases**

- remove manual work
- connect tools into repeatable flows
- schedule operational tasks

**Integration notes:** Looks feasible to evaluate, but integration should start with a small proof of concept and README check.

**Production readiness:** High for an OSS candidate: recent activity, adoption, and ecosystem signals are strong enough for a serious pilot.

**Quality signals**

- 9163 GitHub stars
- 774 forks
- updated 2026-06-24
- primary language: Go
- 5 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 72/100 |
| stars | 84/100 |
| topics | 63/100 |
| outlook | 79/100 |
| quality | 81/100 |
| recency | 80/100 |
| adoption | 81/100 |
| production | 74/100 |
| usefulness | 74/100 |
| integration | 62/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 200/100 |

---

<sub>🔭 Discovered 2026-06-24 · [View on GitHub](https://github.com/bitnami/sealed-secrets) · [← Back to Automation](./README.md)</sub>
