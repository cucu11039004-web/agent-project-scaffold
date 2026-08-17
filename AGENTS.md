# &lt;项目名&gt; 项目说明（供 AI agent 使用）

> 本文件是本项目给所有 AI 编码 agent（Codex / Claude Code / Copilot 等）的**持久化记忆
> 与操作约定**，随项目进 git。`CLAUDE.md` 是指向本文件的软链，Claude Code 读到的即本文件。
>
> ——以下为脚手架骨架，占位小节请按真实项目替换。——

## 文档索引（去哪找什么）
- **术语表（glossary）**：仓库根 `CONTEXT.md`，全项目唯一一份（只放术语定义，不放
  实现/spec/进度）。grill-with-docs / domain-modeling 维护术语时写它。
- **架构决策（ADR）**：系统级放 `docs/adr/NNNN-*.md`；某上下文专属的可就近放
  `<ctx>/docs/adr/`。只追加不回改，见 `docs/adr/README.md`。
- **待办与进度**：仓库根 `TODO.md`（已完成 / 进行中 / 待办 / 以后，轻量清单）。稳定事实：本文件。
- **规划→执行交接**：规划者（Claude Code `/plan` + grill-me / grill-with-docs）形成初稿就
  落盘仓库根 `PLAN.md` 并标**状态**（草稿 / 评审中 / 定稿）；修改和给其他 agent 评审都直接
  在 `PLAN.md` 上进行，git 历史自动留痕。执行者只执行状态为**定稿**的计划，完成后回写
  `TODO.md` 并把 `PLAN.md` 清空回模板；**不做手工归档**，`git log -- PLAN.md` 即历史。
  跨会话上下文可用 handoff skill 生成背景文档（落 OS 临时目录），以路径引用 `PLAN.md`。
- **依赖的 skills**：见 `SKILLS.md`。

## 项目概览
&lt;一句话说明项目是什么；仓库结构；核心模块及其职责。替换本段。&gt;

## 关键约定（勿随意改）
&lt;列出与正确性强相关、不能随意改的约定/不变量。替换本段。&gt;

## 运行与自测（完整命令见 README）
&lt;关键脚本、环境、自测子命令名；具体命令放 README。替换本段。&gt;

## 计划与待办的真相源（agent 必读）
- **待办与进度的轻量真相源是 `TODO.md`**（仓库根，进 git）：已完成 / 进行中 / 待办 / 以后，
  需要了解"现在/接下来做什么"先读它。**决策理由**归 `docs/adr/`、**术语**归根
  `CONTEXT.md`、**稳定事实**归本文件——三类都不塞进 `TODO.md`，避免它长成臃肿路线图。
- 各 agent 自己 session 内的私有计划文件（如 Copilot 的 session `plan.md`）只是**临时执行笔记**，
  **不进 git、以 `TODO.md` 为准**；干完一段收尾时，把有效的进展**同步回 `TODO.md`**，
  然后临时笔记即可丢弃。任何时候若两者冲突，以 `TODO.md` 为准，只往 `TODO.md` 一个方向同步。
- **本文件（AGENTS.md）与 TODO.md 的分工**：AGENTS.md 记录**稳定事实**（架构、约定、红线、
  索引），**只在这些事实本身变化时才更新**；**日常进展/待办状态一律不写进本文件**，只进 `TODO.md`。
  一句话：TODO 记"在做什么/做到哪"，AGENTS 记"项目是什么、怎么在里面干活"。
