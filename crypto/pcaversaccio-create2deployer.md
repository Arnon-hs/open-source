# pcaversaccio/create2deployer

[![Stars](https://img.shields.io/github/stars/pcaversaccio/create2deployer?style=flat-square&color=yellow)](https://github.com/pcaversaccio/create2deployer/stargazers) [![Forks](https://img.shields.io/github/forks/pcaversaccio/create2deployer?style=flat-square&color=blue)](https://github.com/pcaversaccio/create2deployer/network) [![Language](https://img.shields.io/badge/lang-TypeScript-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-55%2F100-brightgreen?style=flat-square)](#)

> Helper smart contract to make easier and safer usage of the `CREATE2` EVM opcode.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 306 |
| 🍴 **Forks** | 43 |
| 💻 **Language** | TypeScript |
| 📈 **Score** | 55/100 |
| 🗓️ **Last push** | 2026-09-05 |
| 🔍 **Source** | github |

## 🏷️ Topics

`create2` `deployment` `ethereum` `smart-contracts` `solidity`

## 🎯 Categories

Crypto

## 📝 Summary

### English

**Brief Summary**  
pcaversaccio/create2deployer is an open‑source helper contract that abstracts the low‑level `CREATE2` opcode, making it easier and safer to deploy deterministic smart‑contract addresses. With a clean TypeScript wrapper and a well‑documented README, it is suited for rapid prototyping of Web3, wallet, or DeFi workflows that need predictable contract deployment.  

**Value**  
The library removes the boilerplate and error‑prone calculations normally required when using `CREATE2`, letting developers focus on business logic while still being able to audit the exact deployment code. Its open implementation and modest size (≈300 ★, 40 ✂) provide transparency for security reviews and enable quick inspection of how deterministic addresses are generated.  

**Practical Adoption Path**  
1. **Proof‑of‑concept** – Clone the repo, run the TypeScript examples, and verify that the generated addresses match expectations on a testnet.  
2. **Integration** – Add the npm package (or the contract source) to your existing Hardhat/Foundry workflow, replace any custom `CREATE2` scripts with the helper’s `deployDeterministic` function, and write unit tests around the expected address output.  
3. **Security Review** – Perform a static analysis (e.g., Slither, MythX) and a manual audit of the contract’s fallback logic, then confirm the license is compatible with your project.  

**Production Readiness**  
- **Maturity**: Medium. The project is actively maintained (last update 2026‑05‑13) and has a solid user base, but it lacks formal audits and a dedicated maintainer team.  
- **Risks**: No major metadata issues, but the open‑source license, long‑term maintainer commitment, and potential edge‑case bugs need verification before a high‑value production launch.  
- **Recommendation**: Use it for internal prototypes, test‑net deployments, or as a vetted building block in larger systems after a small PoC and a focused security review; for mission‑critical main‑net deployments, consider adding an external audit and monitoring the repository for future updates.

### Русский

**pcaversaccio/create2deployer** — это открытый helper‑контракт, упрощающий и повышающий безопасность работы с opcode `CREATE2` в EVM, что делает прототипирование и отладку Web3‑процессов (создание кошельков, DeFi‑протоколов, интеграций) более прозрачными. Для внедрения рекомендуется начать с небольшого proof‑of‑concept, изучив README и запустив тесты, после чего можно интегрировать контракт в существующие Solidity‑проекты, проверив зависимости и актуальность поддержки. Готовность к production — средняя: проект подходит для прототипов и внутренних сервисов, но требует дополнительного аудита лицензии, безопасности и подтверждения активности мейнтейнеров перед запуском в продакшн.

### 中文

**价值**  
`pcaversaccio/create2deployer` 提供了一个轻量级的 Helper 合约，封装了 `CREATE2` opcode 的复杂细节，使开发者在原型设计、合约部署以及 DeFi/钱包功能的实现过程中能够更安全、更便捷地使用确定性部署。它的开源实现透明，可直接阅读和审计，帮助团队快速验证链上工作流而无需自行编写底层 `CREATE2` 逻辑。

**典型接入方式**  

1. **阅读 README 与示例**：先克隆仓库，查看 `README.md` 中的使用说明和示例脚本（一般为 TypeScript/Hardhat）。  
2. **在本地或测试网部署 Helper 合约**：使用 Hardhat、Foundry 或 Remix 将 `Create2Deployer` 合约部署到目标网络。  
3. **调用部署接口**：在业务合约或脚本中调用 `deploy(bytes32 salt, bytes memory bytecode)`（或相似的封装函数），传入盐值和待部署合约的字节码，即可得到确定性的部署地址。  
4. **验证**：使用 `computeAddress(salt, bytecodeHash)` 方法预先计算地址，确认部署后地址是否匹配。  
5. **集成到 CI/CD**：把上述步骤写入自动化脚本，作为原型或内部测试流水线的一环。

**生产可用性**  

- **成熟度**：已有 300+ GitHub Stars、数十个 Fork，社区关注度较高。代码最近一次更新在 2026‑05‑13，说明仍在维护。  
- **适用场景**：非常适合原型开发、内部工具、合约安全审计以及需要确定性部署的 DeFi/钱包功能。  
- **生产风险**：  
  - 仍需自行完成安全审计，尤其是对 `salt` 管理和重入风险的检查。  
  - 依赖的 TypeScript/Hardhat 环境需确认与现有构建链兼容。  
  - 许可证（MIT/Apache 等）需核对是否符合公司合规要求。  
- **推荐做法**：在生产环境使用前，先在测试网完成完整的 POC，审计代码并加入额外的访问控制或审计日志；确认维护者活跃度后再决定是否将其作为长期依赖。

综上，`create2deployer` 是一个 **中等成熟度、适合快速原型和内部工作流** 的工具，经过适当审计和测试后可安全投入生产使用。

## 🧭 Practical evaluation

**Value:** pcaversaccio/create2deployer helps prototype or inspect blockchain workflows with open implementation details.

**Best use cases**

- build Web3 workflows
- inspect blockchain integrations
- prototype wallet or DeFi features

**Integration notes:** Looks feasible to evaluate, but integration should start with a small proof of concept and README check.

**Production readiness:** Medium: useful for prototypes or internal workflows, with dependency and maintenance checks before production.

**Quality signals**

- 306 GitHub stars
- 43 forks
- updated 2026-05-13
- primary language: TypeScript
- 5 topics

**Risks:** No major metadata risk found, but license, security posture, and active maintainers still need final review.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 41/100 |
| stars | 53/100 |
| topics | 63/100 |
| outlook | 65/100 |
| quality | 67/100 |
| recency | 80/100 |
| adoption | 50/100 |
| production | 67/100 |
| usefulness | 42/100 |
| integration | 46/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 100/100 |

---

<sub>🔭 Discovered 2026-05-13 · [View on GitHub](https://github.com/pcaversaccio/create2deployer) · [← Back to Crypto](./README.md)</sub>
