---
name: quiz-gated-learning-project
description: Create and run stateful beginner learning projects with one micro-topic at a time, a quiz gate before advancement, and durable README/ROADMAP/STATE artifacts. Use when a user asks to learn a topic from zero knowledge, turn source material into a guided learning project, continue a long-running study path, verify understanding before moving on, or keep learning state across sessions.
---

# Quiz Gated Learning Project

## Overview

Use this skill to turn learning into a small governed project instead of an ad hoc explanation thread.

The core rule is simple: teach one smallest useful concept, check understanding, and advance only after the learner passes the gate or explicitly says they understand.

## Workflow

1. Clarify the learning target.
   - Identify topic, starting level, desired outcome, available source material, language, and time horizon.
   - If the learner says "from zero", assume no prior vocabulary.
2. Separate source analysis from learning state.
   - If the user provides a PDF, article, repo, transcript, or notes, first summarize it as source analysis.
   - Do not mix the source analysis into the project state file.
3. Create or update the learning project artifacts.
   - `README.md`: project purpose, learning rules, artifact index.
   - `ROADMAP.md`: staged path with micro-topics and locked/unlocked status.
   - `STATE.md`: current topic, quiz status, misunderstandings, next action.
4. Teach exactly one micro-topic.
   - Keep the explanation beginner-safe.
   - Prefer concrete examples and contrast pairs.
   - Avoid jumping ahead to later vocabulary unless it is unavoidable.
5. Ask a quiz gate.
   - Use a short question that tests the core idea, not memorized phrasing.
   - Stop after asking the quiz; wait for the learner's answer.
6. Evaluate the answer before advancing.
   - If correct, mark the micro-topic as passed and unlock the next item.
   - If partially correct, repair only the missing idea and ask a smaller follow-up.
   - If incorrect, keep the same topic current and record the misconception.
7. Preserve continuity.
   - Update `STATE.md` after each gate decision or stable checkpoint.
   - When resuming, read `STATE.md` first, then `ROADMAP.md`, then any source analysis only if needed.

## Artifact Contract

Use these files for durable projects:

- `README.md`: why this project exists and how the learner wants to study.
- `ROADMAP.md`: ordered learning path with each micro-topic as a checkable unit.
- `STATE.md`: current checkpoint and the next quiz or lesson.
- `source-analysis.md` or `analysis/`: optional source-material notes, kept separate from teaching progress.
- `lessons/`: optional completed lesson notes, used only when the user wants durable lesson pages.

For exact templates, read `references/artifact-templates.md`.

## Teaching Rules

- Treat "I am a beginner" as a strict constraint.
- Teach one smallest knowledge point at a time.
- Ask before expanding into a new concept.
- Do not mark progress based on exposure; mark it only after a quiz gate or explicit understanding.
- Keep practice/action progress separate from conceptual understanding.
- Prefer the learner's language for explanations and artifacts.
- If the learner is tired or confused, shrink the current concept instead of moving on.

## Quiz Gate Rules

Use a quiz when:

- finishing a micro-topic
- resuming from an old checkpoint
- the learner says they understand but the concept is foundational
- the next topic depends on the current one

Good quiz forms:

- true/false plus why
- choose between two explanations
- explain in the learner's own words
- identify the misconception in a short example
- predict what happens in a tiny scenario

Avoid:

- multi-part exams
- questions that require later concepts
- moving on before evaluating the answer
- turning every quiz into a long lecture

## References

- Artifact templates: `references/artifact-templates.md`
- Example project scaffold: `examples/llm-training-beginner-project.md`
