# PhotonVision/photonvision

[![Stars](https://img.shields.io/github/stars/PhotonVision/photonvision?style=flat-square&color=yellow)](https://github.com/PhotonVision/photonvision/stargazers) [![Forks](https://img.shields.io/github/forks/PhotonVision/photonvision?style=flat-square&color=blue)](https://github.com/PhotonVision/photonvision/network) [![Language](https://img.shields.io/badge/lang-Java-informational?style=flat-square)](#) [![Score](https://img.shields.io/badge/score-46%2F100-brightgreen?style=flat-square)](#)

> PhotonVision is the free, fast, and easy-to-use computer vision solution for the FIRST Robotics Competition.

## 📊 Stats

| | |
|---|---|
| ⭐ **Stars** | 411 |
| 🍴 **Forks** | 297 |
| 💻 **Language** | Java |
| 📈 **Score** | 46/100 |
| 🗓️ **Last push** | 2026-08-24 |
| 🔍 **Source** | github |

## 🏷️ Topics

`computer-vision` `frc` `java` `opencv` `vision` `vision-processing` `wpilib`

## 🎯 Categories

Misc

## 📝 Summary

### English

**Brief Summary (2‑3 sentences)**  
PhotonVision is an open‑source, Java‑based computer‑vision framework built for the FIRST Robotics Competition. It provides a fast, plug‑and‑play pipeline that lets teams replace hand‑crafted image‑processing scripts with a reusable, real‑time vision system. With over 400 GitHub stars and active maintenance, it is positioned as a practical tool for automating repetitive vision tasks in robotics projects.

**Value**  
PhotonVision eliminates the need for teams to write low‑level image‑processing code, letting them focus on higher‑level robot logic. By delivering a ready‑made calibration UI, network tables integration, and support for common cameras, it turns a labor‑intensive, error‑prone step into a repeatable, maintainable component of the robot’s software stack.

**Practical Adoption Path**  

1. **Proof‑of‑Concept** – Clone the repo, follow the README to set up a supported USB or CSI camera, and run the sample pipeline on a development laptop or the robot’s roboRIO.  
2. **Integration Test** – Connect the vision output (e.g., target pose) to a small subsystem (such as a shooter or alignment routine) using NetworkTables, verifying latency and accuracy in a controlled environment.  
3. **Iterate & Extend** – Add custom pipelines or adjust camera parameters as needed, leveraging the built‑in calibration tools.  
4. **Scale** – Once the pipeline reliably meets performance goals, embed it into the main robot codebase and document the setup for future teams.

**Production Readiness**  
PhotonVision is at a **medium** readiness level: it is stable enough for prototypes and internal robotics workflows, but production deployment should include:

* A dependency audit (Java libraries, camera drivers).  
* Verification of the integration path for your specific hardware (camera model, network topology).  
* A small‑scale pilot to measure setup time and maintenance overhead.  

If these checks pass, PhotonVision can be promoted to a production‑grade vision solution for competition robots.

### Русский

PhotonVision — это бесплатное и быстрое решение компьютерного зрения, ориентированное на команды FIRST Robotics Competition, которое автоматизирует повторяющиеся ручные операции, позволяя собрать конвейер обработки изображений и планировать задачи без постоянного вмешательства. Типичный сценарий внедрения — небольшое proof‑of‑concept: установить библиотеку по инструкциям в README, интегрировать её в существующий пайплайн (например, для распознавания целей робота) и проверить работоспособность, после чего расширять на более масштабные автоматизированные потоки. Готовность к production — средняя: проект подходит для прототипов и внутренних процессов, но требует проверки зависимостей, стабильности и поддержки перед выводом в продакшн.

### 中文

**项目简介**  
PhotonVision 是面向 FIRST 机器人竞赛的免费、快速且易用的计算机视觉库，提供即插即用的目标检测与姿态估计功能，帮助团队在赛场上实现自动化定位与目标追踪。

**价值**  
- **降低人工成本**：自动识别目标、计算位姿，省去手动调参和数据采集的重复工作。  
- **提升可靠性**：基于深度学习和传统图像处理的混合算法，提供稳定的检测结果，适合在赛场噪声和光照变化下使用。  
- **加速原型迭代**：配套的可视化工具和示例代码让团队快速搭建并验证视觉方案，缩短开发周期。

**典型接入方式**  
1. **依赖引入**：在项目的 `build.gradle`（或 Maven）中添加 PhotonVision 的 Maven 坐标。  
2. **硬件准备**：使用兼容的 USB 摄像头或 Raspberry Pi Camera，确保摄像头帧率 ≥ 30 fps。  
3. **配置文件**：在 `photonvision.json` 中声明摄像头参数、目标模型（如 AprilTag、Retro‑Reflective）以及网络端口。  
4. **代码调用**：在机器人主循环中创建 `PhotonCamera` 实例，调用 `getLatestResult()` 获取 `PhotonPipelineResult`，从中读取目标的 `pose`、`yaw`、`area` 等信息并用于控制逻辑。  
5. **小规模验证**：先在本地机器或单片机上运行示例 Demo，确认检测准确率后再集成到完整的机器人代码库。

**生产可用性**  
- **成熟度**：GitHub 411 星、297 Fork，活跃维护（截至 2026‑05‑11），适合作为原型或内部工具使用。  
- **依赖与维护**：主要语言 Java，依赖少且可通过 Gradle 自动管理；但需自行评估摄像头驱动兼容性及网络带宽。  
- **上线建议**：先在实验室完成端到端的 PoC（包括摄像头布置、网络延迟、错误恢复），随后在赛前进行压力测试；在正式比赛或生产线使用前，做好版本锁定和回滚方案。  

总体而言，PhotonVision 在自动化视觉任务上提供了即插即用的解决方案，适合快速验证和中小规模部署；在进入正式生产或高可靠性场景前，需要通过小范围试点验证集成成本和运维风险。

## 🧭 Practical evaluation

**Value:** PhotonVision/photonvision helps remove repetitive manual operations from a workflow.

**Best use cases**

- remove manual work
- connect tools into repeatable flows
- schedule operational tasks

**Integration notes:** Looks feasible to evaluate, but integration should start with a small proof of concept and README check.

**Production readiness:** Medium: useful for prototypes or internal workflows, with dependency and maintenance checks before production.

**Quality signals**

- 411 GitHub stars
- 297 forks
- updated 2026-05-11
- primary language: Java
- 7 topics

**Risks:** Integration path is not obvious from metadata; validate setup cost before committing.

## 🧮 Score breakdown

| Dimension | Score |
|---|---:|
| forks | 62/100 |
| stars | 56/100 |
| topics | 88/100 |
| outlook | 48/100 |
| quality | 59/100 |
| recency | 20/100 |
| adoption | 57/100 |
| production | 47/100 |
| usefulness | 42/100 |
| integration | 30/100 |
| sourceTrust | 100/100 |
| categoryMatchCount | 0/100 |

---

<sub>🔭 Discovered 2026-05-11 · [View on GitHub](https://github.com/PhotonVision/photonvision) · [← Back to Misc](./README.md)</sub>
