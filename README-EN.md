# Quiz-Gated Learning Project Skill

Create beginner-friendly learning projects that advance one micro-topic at a time and require a quiz gate before moving on.

## Why This Skill Exists

Agent teaching often turns into long explanations that feel useful but leave no durable state. This skill turns learning into a small project with:

- `README.md` for the learning contract
- `ROADMAP.md` for staged micro-topics
- `STATE.md` for the current checkpoint
- a quiz gate before each advancement
- source analysis kept separate from learning progress

It is designed for learners who say things like:

- "Teach me from zero."
- "Only explain one small concept at a time."
- "Quiz me before we continue."
- "Turn this PDF/article/repo into a learning path."
- "Resume where we stopped last time."

## Install

If your agent or CLI supports `skills add`:

```bash
npx skills add ExDevilLee/quiz-gated-learning-project-skill
```

## Using It With Other LLM Agents

This repository is not Codex-only. The core workflow is plain Markdown:

- `SKILL.md`: the main rules; any LLM agent can read it directly.
- `references/artifact-templates.md`: templates for `README.md`, `ROADMAP.md`, and `STATE.md`.
- `examples/llm-training-beginner-project.md`: a minimal example.
- `agents/openai.yaml`: optional OpenAI / Codex UI metadata, not required to use the workflow.

If your agent does not support `npx skills add`, give it this instruction:

```text
Read SKILL.md in this repository and follow it as the learning workflow. Load references/artifact-templates.md only when you need to create project files. Use examples/llm-training-beginner-project.md as a style reference if needed.
```

## Example Prompt

```text
Use $quiz-gated-learning-project to turn this topic into a beginner learning project. I know nothing about it. Teach one smallest concept, then quiz me before moving on.
```

## What It Produces

```text
learning-project/
  README.md
  ROADMAP.md
  STATE.md
  source-analysis.md    # optional
  lessons/              # optional
```

## Status

First public reference version. The workflow was distilled from a real long-running beginner learning project where progress is gated by explicit understanding rather than passive exposure.
