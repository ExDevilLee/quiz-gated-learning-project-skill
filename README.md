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

如果你的 Agent / CLI 支持 `skills add`：

```bash
npx skills add ExDevilLee/quiz-gated-learning-project-skill
```

也可以指定 Skill 目录：

```bash
npx skills add ExDevilLee/quiz-gated-learning-project-skill/skills/quiz-gated-learning-project
```

如果使用 Codex Marketplace CLI：

```bash
npx codex-marketplace add ExDevilLee/quiz-gated-learning-project-skill/skills/quiz-gated-learning-project --skill
```

## 其他 LLM Agent 怎么用

这个仓库不是 Codex 专用。核心工作流写在普通 Markdown 文件里：

- `skills/quiz-gated-learning-project/SKILL.md`：主规则，任何 LLM Agent 都可以直接读取。
- `skills/quiz-gated-learning-project/references/artifact-templates.md`：`README.md` / `ROADMAP.md` / `STATE.md` 模板。
- `skills/quiz-gated-learning-project/examples/llm-training-beginner-project.md`：最小示例。
- `skills/quiz-gated-learning-project/agents/openai.yaml`：OpenAI / Codex 相关 UI metadata，可选，不是运行必需。

如果你的 Agent 不支持 `npx skills add`，可以直接把这段话给它：

```text
Read skills/quiz-gated-learning-project/SKILL.md in this repository and follow it as the learning workflow. Load skills/quiz-gated-learning-project/references/artifact-templates.md only when you need to create project files. Use skills/quiz-gated-learning-project/examples/llm-training-beginner-project.md as a style reference if needed.
```

## 示例 Prompt

```text
使用 $quiz-gated-learning-project，把这个主题变成一个适合初学者的学习项目。我对这个主题是 0 知识点小白。每次只讲一个最小知识点，讲完后先考我一下，确认我理解了再继续。
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
