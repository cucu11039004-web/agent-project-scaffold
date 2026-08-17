# agent-project-scaffold

面向 AI 编码 agent（Claude Code / Copilot / Codex 等）协作的**项目文档脚手架**。
它把一套"人 + 多 agent 协作"的文档结构固化下来，方便新项目直接复用。

## 这套脚手架解决什么

让多个 AI agent 在同一项目里协作时，有稳定、单一的"去哪找什么、怎么干活"的约定：

- **稳定事实与操作约定** → `AGENTS.md`（`CLAUDE.md` 软链指向它）
- **上下文划分（多限界上下文）** → `CONTEXT-MAP.md` + 各上下文就近的 `CONTEXT.md`
- **架构决策** → `docs/adr/`（只追加不回改）
- **待办与进度** → `TODO.md`（轻量清单）
- **规划→执行交接** → `docs/plan/current.md`（规划者写、执行者读、完成后归档）
- **依赖的 skills** → `SKILLS.md`

## 分支模型

- `main`：**领域无关的空壳基座**。所有文件都是通用骨架 + 占位，任何项目都能套。
- `robot-il`：从 `main` 派生的**机器人模仿学习**风味分支，预置 dataset/training/
  inference/ops 上下文、真机安全红线等（内容抽象化，用占位名）。
- 未来其他领域（web / research…）各从 `main` 再开分支。

通用改进只改 `main`，再单向 `merge` 进各风味分支；已经用它开出去的真实项目不回流。

## 怎么用

1. 选一个贴近的分支（通用就 `main`，机器人模仿学习就 `robot-il`）。
2. 克隆/复制其文件到你的新项目，按各文件里的占位提示替换成真实内容。
3. 按 `SKILLS.md` 装好依赖的 skills，即可开始用 grill / handoff / plan 等流程。
