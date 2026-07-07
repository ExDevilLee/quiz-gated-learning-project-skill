# Quiz-Gated Learning Project Skill

为初学者创建可续做的学习项目：每次只推进一个最小知识点，并在进入下一点前通过 quiz gate 检查理解。

English version: [README-EN.md](README-EN.md)

## 为什么需要这个 Skill

Agent 教学很容易变成长篇解释：当下看起来有帮助，但下一次很难恢复，也不确定学习者是否真的理解。

这个 Skill 把学习过程变成一个小型项目：

- `README.md` 记录学习契约
- `ROADMAP.md` 拆分阶段和最小知识点
- `STATE.md` 保存当前学习检查点
- 每次推进前都有 quiz gate
- source analysis 和 learning progress 分开保存

它适合这类请求：

- “把我当成 0 知识点小白。”
- “每次只讲一个最小知识点。”
- “讲完以后考我一下，确认我真的理解。”
- “把这篇 PDF / 文章 / 仓库变成学习路线。”
- “从上次停止的地方继续。”

## 安装

```bash
npx skills add ExDevilLee/quiz-gated-learning-project-skill
```

## 示例 Prompt

```text
Use $quiz-gated-learning-project to turn this topic into a beginner learning project. I know nothing about it. Teach one smallest concept, then quiz me before moving on.
```

## 产出结构

```text
learning-project/
  README.md
  ROADMAP.md
  STATE.md
  source-analysis.md    # optional
  lessons/              # optional
```

## 当前状态

第一版公开参考 Skill。这个工作流来自一个真实的长期初学者学习项目：学习进度不靠“看过了”推进，而靠明确理解和 quiz gate 推进。
