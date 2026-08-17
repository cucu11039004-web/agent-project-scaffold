# SKILLS — 本脚手架依赖的 agent skills

本文档体系（CONTEXT / ADR / TODO / plan 交接、grill 拷打）假设装了下面这几个 skill。
用 [skills CLI](https://skills.sh/) 安装。

## 假设依赖的 skills

| skill | 用途 |
|---|---|
| `grill-me` | 关起门拷打一个方案/设计，逼清思路（不落盘） |
| `grill-with-docs` | 拷打 + 顺手沉淀：术语进各上下文 `CONTEXT.md`、决策进 `docs/adr/` |
| `domain-modeling` | 维护领域术语表与 ADR（被 grill-with-docs 调用） |
| `handoff` | 把当前会话压缩成交接文档，供另一个 agent 接手 |
| `find-skills` | 到 skills 生态里发现/安装更多 skill |

## 安装

这些 skill 来自一个 git 仓库，用 skills CLI 从该仓库安装（示例）：

```bash
# 安装到全局，供各 agent 使用
npx skills add git@github.com:<your-org>/<your-skills-repo>.git -g
# 只装其中若干个：
npx skills add git@github.com:<your-org>/<your-skills-repo>.git -g -s grill-me grill-with-docs domain-modeling handoff
```

查看已安装：`npx skills ls -g`。
把 `<your-org>/<your-skills-repo>` 换成你自己维护 skills 的仓库地址。
