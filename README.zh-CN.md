![Team Leader：给 AI 项目配一位负责人，带领团队朝正确的方向前进](assets/cover.zh.svg)

[English](README.md) · [繁體中文](README.zh-Hant.md) · [简体中文](README.zh-CN.md)

**Codex · Astra** ｜ **v0.5.16** ｜ **MIT**

[快速上手](#start) · [设计原理](#loop) · [岗位分工](#roles) · [使用反馈](#feedback) · [下载完整 Skill](https://github.com/aidesign996/team-leader/releases/download/team-leader-v0.5.16/team-leader-0.5.16.zip)

**做 AI 项目时，你是否还要反复提醒目标、检查结果，再催下一步？**

我设计了 Team Leader，把持续协调项目这件事交给一位职责明确的 AI 负责人：它围绕你的目标安排专业岗位，检查做出来的结果，并组织修正。已经确认的需求、决定和进度则保存到项目文件中，方便后续接着做。

它面向需要持续迭代、跨产品设计、技术设计、开发和验证的项目。希望减少使用者反复转述和协调的负担；实际效果仍需要更多场景验证。

<a id="start"></a>

## 两步开始使用

**1. 把这句话交给能够联网和安装 Skill 的 AI 工具：**

> 请阅读 <https://github.com/aidesign996/team-leader>，帮我安装其中完整的 Team Leader Skill。

**2. 安装后，在项目对话中选中 Team Leader，或点名 `$team-leader`，然后说：**

> 接下来这个项目由你负责，你跟进一下。

按照这套方法，负责人应先读取现有资料和目标；缺少关键需求时主动问你，明确后继续推进。你可以像向团队负责人交代工作一样，逐步补充想法。首次选中 Skill 很重要，短句本身不保证所有工具都能自动发现技能。

希望采用团队模式时，再补一句：“请为这个项目建立完整团队，由你负责协调。”实际建队取决于工具支持和你的授权，已有岗位会复用。

<details>
<summary>工具不能直接安装？查看手动安装方法</summary>

1. [下载完整 ZIP](https://github.com/aidesign996/team-leader/releases/download/team-leader-v0.5.16/team-leader-0.5.16.zip)并解压。
2. 将完整的 `team-leader` 文件夹放到个人 `~/.agents/skills/`，或项目的 `.agents/skills/` 中。完整包共22个文件，包含 MIT 许可，不要只复制 `SKILL.md`。
3. 在新项目对话中确认能读取 Skill；若未发现，重启 Codex。升级前备份已有自定义修改，并保留项目记录。

</details>

<a id="loop"></a>

## 它怎样带队：目标、反馈、行动

设计受到《系统之美》的调节反馈启发：用户确定目标，负责人观察结果并判断差距，专业岗位据此行动，再把新的结果带回检查。

<p align="center"><img src="assets/loop.zh.png" width="470" alt="目标输入负责人，负责人对照项目成果判断差距，再协调专业岗位更新成果。"></p>

负责人既要安排谁来做，也要持续判断“这轮工作有没有让项目更接近目标”。早期可以探索多个方案，进入实现时再依据目标与约束收敛。新增负责人并不自动保证稳定，观察质量、反馈及时性和修正落实同样重要。

<a id="roles"></a>

## 一个负责人，五类专业职责

| 角色 | 负责什么 |
| --- | --- |
| **0 · 团队负责人** | 维护目标，安排工作，检查差距并协调交付。 |
| **1 · 环境配置** | 准备和检查可复现的工作条件。 |
| **2 · 产品设计** | 明确需求、使用流程与体验。 |
| **3 · 技术设计** | 设计架构、接口和实现边界。 |
| **4 · 开发** | 实现、自查与修正。 |
| **5 · 独立 AI 验收** | 由未参与该项制作的角色检查结果。 |

0.5.16 在采用团队模式且获得授权后补齐六类职责；每轮按任务需要调动相关岗位。负责人还会组织项目文档，让需求、产品方案、技术方案、进度和经验各有可查找的位置。记录需要在后续任务中主动读取和应用，保存文件本身不等于自动记住。

<a id="fit"></a>

## 适用范围与投入

- **主要设计对象是 Codex 中的 Astra。** Sol 有部分专业岗位实践，尚无同条件下完整 Sol 团队的效果结论。
- **可能消耗较多额度。** 负责人通常从 XHigh 起步，按任务安排专业岗位推理级别，并在工具支持时整理上下文；实际设置遵循用户偏好和工具能力。
- **简单任务可以保持单人。** 当前已检查包完整性、干净目录解压与基础结构；新账号完整首次运行、长期自主纠偏和节省额度尚未系统验证。

[阅读完整设计文章（GitHub）](https://github.com/aidesign996/ai-practice/blob/main/docs/team-leader/ARTICLE.md) · [查看版本说明与校验文件](https://github.com/aidesign996/team-leader/releases/tag/team-leader-v0.5.16)

<a id="feedback"></a>

## 欢迎把工作中遇到的问题带回来

**不需要先写一份规范报告，一条留言说清楚就好：** 你在做什么、它实际怎样处理、你希望怎样处理会更好。模型和输出片段有助于理解问题，分享前可去掉私人信息。

例如：“我让负责人接手一个已有项目，它重新拟了计划，却没接着做上一轮未完成的事。我更希望它先找到继续点，完成后再提出调整。”这是说明反馈方式的假设场景。

[查看 GitHub 公开讨论](https://github.com/aidesign996/ai-practice/discussions/1) · [在现有共享评论区留言](https://aidesign996.github.io/ai-practice/article-team-leader.zh.html#comments)

网站英文、繁体、简体版本共用同一讨论映射，留言以原语言公开显示。我会结合真实场景整理反馈，改进方法，并在后续版本说明里交代已做的调整。

---

Team Leader Skill 采用 [MIT 许可](team-leader/LICENSE)，署名 AI Design 996。文章与配图单独提供。[设计参考](https://github.com/aidesign996/ai-practice/blob/main/SOURCES.md)
