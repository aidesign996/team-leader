![Team Leader: Give your AI project a lead to keep the team moving toward its goal](assets/cover.en.svg)

[English](README.md) · [繁體中文](README.zh-Hant.md) · [简体中文](README.zh-CN.md)

**Codex · Astra** | **v0.5.16** | **MIT**

[Quick start](#start) · [How it works](#loop) · [Roles](#roles) · [Feedback](#feedback) · [Download the complete Skill](https://github.com/aidesign996/team-leader/releases/download/team-leader-v0.5.16/team-leader-0.5.16.zip)

**Does your AI project still need you to restate the goal, check the results, and prompt the next step?**

I designed Team Leader to give ongoing coordination to an AI lead with explicit responsibilities. It organizes specialist work around your goal, examines the results, and coordinates corrections. Project files preserve agreed requirements, decisions, and progress so work can continue with context.

It is intended for continuing projects that span product design, technical design, development, and review. Reducing the user's coordination burden is a design aim; broader evidence of outcomes is still needed.

<a id="start"></a>

## Start in two steps

**1. Give this instruction to an AI tool that can access the web and install Skills:**

> Please read https://github.com/aidesign996/team-leader and help me install the complete Team Leader Skill from it.

**2. After installation, select Team Leader or mention `$team-leader` in your project conversation. Then say:**

> You're in charge of this project now. Please take it forward.

The lead should read the existing context and goal, ask about essential missing requirements, and proceed with clear, authorized work. Share your ideas as the conversation develops. Select the Skill first: the sentence alone does not guarantee discovery in every tool.

For team mode, add: “Please establish the complete team for this project and coordinate its work.” Team creation depends on the host's tools and your authorization; existing roles are reused.

<details>
<summary>Need to install it manually?</summary>

1. [Download the complete ZIP](https://github.com/aidesign996/team-leader/releases/download/team-leader-v0.5.16/team-leader-0.5.16.zip) and extract it.
2. Place the complete `team-leader` folder in your personal `~/.agents/skills/` or a project's `.agents/skills/`. There are 22 files including the MIT license. Do not copy only `SKILL.md`.
3. Confirm that the Skill is readable in a new project conversation; restart Codex if it is not discovered. Back up custom modifications before upgrading and preserve project records.

</details>

<a id="loop"></a>

## How it works: goal, feedback, action

The design draws on balancing feedback in *Thinking in Systems*. The user defines the goal, the lead observes results and identifies the gap, and specialist roles take action. The updated results return for another check.

<p align="center"><img src="assets/loop.en.png" width="470" alt="The lead compares project results with the user's goal and coordinates specialist actions to update the work."></p>

The lead coordinates who does the work and keeps checking whether it advances the goal. Early work can explore alternatives before converging against the goal and constraints. A lead alone does not guarantee stability: observations, feedback timing, and completed corrections matter.

<a id="roles"></a>

## One lead, five specialist responsibilities

| Role | Responsibility |
| --- | --- |
| **0 · Team Leader** | Maintain the goal, assign work, identify gaps, and coordinate delivery. |
| **1 · Environment setup** | Prepare and check reproducible working conditions. |
| **2 · Product design** | Clarify needs, workflows, and user experience. |
| **3 · Technical design** | Define architecture, interfaces, and implementation boundaries. |
| **4 · Development** | Build, self-check, and correct. |
| **5 · Independent AI review** | Check results through a role that did not produce that work. |

Version 0.5.16 establishes all six responsibilities when team mode is chosen and authorized, then activates the roles needed for each task. The lead also organizes requirements, product and technical decisions, progress, and experience into findable project documents. Records must be read and applied in later work; saving them alone is not automatic memory.

<a id="fit"></a>

## Fit and effort

- **Primarily designed around Astra in Codex.** Sol has some specialist-role experience, but there is no comparable evaluation of a complete Sol team.
- **Multi-role work can use substantial quota.** The lead typically starts at XHigh, selects specialist effort for the task, and manages context when supported. Actual settings follow user preferences and host capabilities.
- **Simple tasks can remain solo.** Package integrity, extraction into a clean directory, and basic structure were checked. A complete first run on a new account, long-term correction, and quota savings have not been evaluated systematically.

[Read the full design article on GitHub](https://github.com/aidesign996/ai-practice/blob/main/docs/team-leader/ARTICLE.en.md) · [Release notes and checksums](https://github.com/aidesign996/team-leader/releases/tag/team-leader-v0.5.16)

<a id="feedback"></a>

## Bring back a real work situation

**One message is enough:** what you were doing, what actually happened, and what would have worked better. The model and a relevant output excerpt can help explain the issue; remove private information before sharing.

For example: “I asked the lead to take over an existing project. It wrote another plan but did not resume unfinished work. I would prefer it to recover the continuation point, finish that work, and then propose changes.” This is an illustrative feedback scenario.

[View public GitHub discussions](https://github.com/aidesign996/ai-practice/discussions/1) · [Leave a comment in the shared thread](https://aidesign996.github.io/ai-practice/article-team-leader.html#comments)

The website's English, Traditional Chinese, and Simplified Chinese editions use the same discussion mapping. Comments remain public in their original language. I will use real situations to review the method and describe completed changes in future release notes.

---

The Team Leader Skill uses the [MIT License](team-leader/LICENSE), credited to AI Design 996. Article text and illustrations are separate. [Design references](https://github.com/aidesign996/ai-practice/blob/main/SOURCES.md)
