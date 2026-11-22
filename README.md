# AI 项目设计与学习

`project-learning-workflow` 是一个 Codex Skill，面向想用 AI 做项目、同时学会自己做判断的人。它适合只有初步想法的新人，也适合已经有项目、想明确下一项功能或做交付验收的人。

你可以和 AI 一起说清项目要解决的问题，把路线拆成能亲手试用的小成果，再用验收结果决定下一步。代码原理按当前任务和你的兴趣讲解。

## 安装

把仓库克隆到个人 Skill 目录，让 `SKILL.md` 位于 `project-learning-workflow` 文件夹的根目录。

Windows PowerShell

```powershell
$projectSkillPath = Join-Path $HOME '.agents/skills/project-learning-workflow'
git clone https://github.com/ljx1234452/project-learning-workflow.git "$projectSkillPath"
```

macOS 或 Linux

```bash
git clone https://github.com/ljx1234452/project-learning-workflow.git "$HOME/.agents/skills/project-learning-workflow"
```

如果只想在一个项目里使用，也可以把仓库放到该项目的 `.agents/skills/project-learning-workflow`。安装后，在 Codex 打开一个任务并输入下方的调用语。[Codex 技能安装说明](https://developers.openai.com/api/reference/cli)

## 在 Codex 中使用

**只有初步想法**

```text
用 $project-learning-workflow 帮我梳理一个社区活动小工具。我还没想清楚第一版应该先解决报名还是签到。
```

**已经知道这轮要做什么**

```text
用 $project-learning-workflow 给已有的资料整理工具写一份小任务 PRD。这轮要把当前筛选结果按界面顺序导出为 CSV，表头为「文件名」和「标签」。我先审查 PRD。
```

## 六步流程

| 步骤 | 这一轮得到什么 |
| --- | --- |
| 1. 明确项目目标 | 说清谁会用、要解决什么问题、首版做到哪。有相近的开源案例时，先看实际使用流程，再选值得借鉴的设计。 |
| 2. 制定整体路线 | 按用户能试用的成果排里程碑，细化最近一轮，后续保留方向。考虑改编开源项目时，核对许可、适配度和改动成本。 |
| 3. 写小任务 PRD | 拿到一份可独立交接的需求说明，包含背景与目标、本轮范围、交付物、可操作的验收标准和开工所需信息。 |
| 4. 执行、试用与修改 | PRD 审查通过后，可带到新任务执行。AI 自测后交付成果、试用步骤和验证结果，你亲手试用并确认。 |
| 5. 整合成果，更新路线 | 回到主任务检查新成果能否接入已有流程，记录遗留问题，再选下一个小目标。 |
| 6. 评测与交付准备 | 用真实场景和可测量的指标验收核心目标，按需要准备演示、内部交接或上线。 |

可以从项目当前所在的步骤开始。主任务保留目标、路线和进度，执行任务按已审查的 PRD 推进。用户验收后，把成果位置、验证结果和遗留问题带回主任务。

## 仓库结构

- [`SKILL.md`](SKILL.md) 定义工作流程和小任务 PRD 的结构。
- [`agents/openai.yaml`](agents/openai.yaml) 设置 Codex 中的显示名称、简介和默认调用语。
