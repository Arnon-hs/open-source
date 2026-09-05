# aws-actions/configure-aws-credentials

[![Stars](https://img.shields.io/github/stars/aws-actions/configure-aws-credentials?style=flat-square&color=yellow)](https://github.com/aws-actions/configure-aws-credentials/stargazers) [![Forks](https://img.shields.io/github/forks/aws-actions/configure-aws-credentials?style=flat-square&color=blue)](https://github.com/aws-actions/configure-aws-credentials/network) [![Language](https://img.shields.io/badge/lang-TypeScript-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-57%2F100-brightgreen?style=flat-square)](#)

> Configure AWS credential environment variables for use in other GitHub Actions.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 2.9k |
| 🍴 **Forks** | 568 |
| 💻 **Language** | TypeScript |
| 📈 **Score** | 57/100 |
| 🗓️ **Last push** | 2026-09-05 |
| 🔍 **Source** | github |

## 🏷️ Topics

_no topics_

## 🎯 Categories

Cloud & Storage

## 📝 Summary

### English

**Brief Summary**  
`aws-actions/configure-aws-credentials` is a GitHub Action that sets up AWS access keys, session tokens and region variables as environment variables for downstream steps in a workflow. It is written in TypeScript, has ~3 k stars and is actively maintained (last update 2026‑05‑12), making it a common building block for CI/CD pipelines that need to call AWS services.

**Value**  
The action abstracts away the boilerplate of exporting `AWS_ACCESS_KEY_ID`, `AWS_SECRET_ACCESS_KEY`, `AWS_SESSION_TOKEN` and `AWS_DEFAULT_REGION`, letting developers focus on the actual deployment logic (e.g., SAM, CDK, Serverless, Terraform). Because it is an official AWS‑maintained action, it follows AWS best‑practice patterns for credential handling (including support for OIDC‑based role assumption) and integrates seamlessly with GitHub’s secrets management.

**Practical Adoption Path**  

| Step | What to Do | Why |
|------|------------|-----|
| 1. Review the README & security policy | Verify the supported authentication methods (static keys vs. OIDC) and understand the required inputs (`aws-access-key-id`, `aws-secret-access-key`, `aws-region`, `role-to-assume`, etc.). | Ensures you pick the right configuration for your security posture. |
| 2. Add the action to your workflow | Insert `uses: aws-actions/configure-aws-credentials@vX` before any step that calls AWS CLI/SDK. | Sets the environment variables automatically for subsequent steps. |
| 3. Wire up secrets | Store AWS keys or OIDC role ARN in GitHub Secrets (or use GitHub Environments) and reference them in the action inputs. | Keeps credentials out of the repo and leverages GitHub’s secret‑masking. |
| 4. Test in a feature branch | Run a minimal workflow that runs `aws sts get-caller-identity` to confirm the credentials are correctly assumed. | Provides a quick sanity check before promoting to main. |
| 5. Promote to production pipelines | Once validated, replace any custom credential‑export scripts with the action across all relevant workflows. | Reduces maintenance overhead and standardizes credential handling. |

**Production Readiness**  
- **Maturity:** Medium – the action is widely used (≈3 k stars, >500 forks) and receives regular updates, but the surrounding ecosystem (e.g., OIDC role trust policies) still requires manual verification.  
- **Risk Profile:** Low on obvious metadata issues; however, you should still audit the underlying TypeScript code, confirm the license (MIT) aligns with your policy, and run a security scan of the released binaries.  
- **Operational Considerations:** Ensure your CI environment can rotate secrets regularly, and monitor the Action’s release notes for breaking changes. With those checks in place, the action is suitable for production workloads, especially internal or prototype pipelines, and can be hardened for external‑facing services after a brief security review.

### Русский

`aws-actions/configure-aws-credentials` — это официальное GitHub Action, которое автоматически задаёт переменные окружения AWS_ACCESS_KEY_ID, AWS_SECRET_ACCESS_KEY и AWS_SESSION_TOKEN, а также регион, делая их доступными для последующих шагов пайплайна. Типичный сценарий — в CI/CD‑процессе (например, сборка, деплой или тесты) требуется временный доступ к ресурсам AWS; действие получает роль/пользователя через OIDC или статические ключи и безопасно конфигурирует их без ручного вмешательства. Готовность к production — средняя: проект популярен (≈3 тыс. звёзд), активно поддерживается и написан на TypeScript, но перед вводом в продакшн стоит проверить лицензию, политику безопасности и совместимость с вашими зависимостями.

### 中文

**项目简介**  
`aws-actions/configure-aws-credentials` 是一个官方 GitHub Action，用于在工作流运行时自动配置 AWS 的 Access Key、Secret Key 以及 Session Token 等环境变量，使后续的 Action 能够直接调用 AWS SDK、CLI 或其他需要凭证的工具。

**价值**  
- **即插即用**：只需在 workflow 中添加一步，即可完成安全的凭证注入，省去手动 export 环境变量的繁琐。  
- **安全合规**：凭证通过 GitHub Secrets 传递，Action 会在运行时将其写入临时的 `~/.aws/credentials`，并在步骤结束后自动清理，降低泄露风险。  
- **跨语言/工具兼容**：配置后，Node、Python、Java、Terraform、Serverless 等任何依赖 AWS 凭证的工具都能直接使用。

**典型接入方式**  

```yaml
name: Deploy to AWS
on: push

jobs:
  deploy:
    runs-on: ubuntu-latest
    steps:
      # 1. 检出代码
      - uses: actions/checkout@v4

      # 2. 配置 AWS 凭证
      - name: Configure AWS credentials
        uses: aws-actions/configure-aws-credentials@v4
        with:
          aws-access-key-id: ${{ secrets.AWS_ACCESS_KEY_ID }}
          aws-secret-access-key: ${{ secrets.AWS_SECRET_ACCESS_KEY }}
          aws-region: us-east-1   # 可选，默认 us-east-1
          # 如需临时凭证，可开启 role-to-assume
          # role-to-assume: arn:aws:iam::123456789012:role/MyDeployRole

      # 3. 运行任意需要 AWS 权限的命令
      - run: aws s3 sync ./dist s3://my-bucket/
```

关键点：  
- **Secrets** 必须在仓库或组织层面预先配置。  
- 如需跨账户或最小权限，配合 `role-to-assume` 使用 IAM Role。  
- 可通过 `aws-session-token`、`aws-sso-session` 等高级参数满足 STS、SSO 场景。

**生产可用性**  
- **成熟度**：已有 2,918+ 星、568+ Fork，且在 2026‑05‑12 最近一次更新，社区活跃度高。  
- **适用范围**：已在大量公开仓库和企业内部 CI 中使用，适合原型、内部自动化以及正式生产环境。  
- **风险与注意事项**  
  - 仍需自行审查 IAM 权限，确保最小权限原则。  
  - 检查项目的许可证（MIT）与安全审计报告，确认符合组织合规要求。  
  - 对于高并发或长时间运行的工作流，建议结合缓存或自定义凭证轮换策略，以避免 STS Token 过期。  

综合来看，`aws-actions/configure-aws-credentials` 在安全、易用性和社区支持方面表现良好，经过一次性安全审计后即可在生产环境中放心使用。

## 🧭 Practical evaluation

**Value:** aws-actions/configure-aws-credentials may be useful when its README and activity match a concrete workflow.

**Best use cases**

- Not enough metadata yet.

**Integration notes:** Needs manual inspection before adoption because integration signals are sparse in the discovered metadata.

**Production readiness:** Medium: useful for prototypes or internal workflows, with dependency and maintenance checks before production.

**Quality signals**

- 2918 GitHub stars
- 568 forks
- updated 2026-05-12
- primary language: TypeScript

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 69/100 |
| stars | 74/100 |
| topics | 0/100 |
| outlook | 64/100 |
| quality | 68/100 |
| recency | 80/100 |
| adoption | 72/100 |
| production | 67/100 |
| usefulness | 42/100 |
| integration | 46/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 100/100 |

---

<sub>🔭 Discovered 2026-05-12 · [View on GitHub](https://github.com/aws-actions/configure-aws-credentials) · [← Back to Cloud--storage](./README.md)</sub>
