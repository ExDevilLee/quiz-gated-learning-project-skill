# Artifact Templates

Use these templates when creating a quiz-gated learning project. Keep them small and adapt names to the user's domain.

## README.md

```md
# <Topic> Learning Project

## Goal

<What the learner wants to understand or become able to do.>

## Learning Contract

- Start from: <zero knowledge / beginner / known prerequisites>.
- Teach one micro-topic at a time.
- Ask a quiz before moving to the next topic.
- Advance only after the learner passes the gate or explicitly says they understand.
- Keep source analysis separate from learning progress.

## Artifacts

- `ROADMAP.md`: staged path and micro-topics.
- `STATE.md`: current checkpoint and next action.
- `source-analysis.md`: optional source-material analysis.
- `lessons/`: optional durable lesson notes.
```

## ROADMAP.md

```md
# Roadmap

Status values:

- `locked`: not ready yet
- `current`: active micro-topic
- `quiz`: explanation done, waiting for learner answer
- `passed`: learner passed the gate
- `review`: learner needs repair or repetition

## Stage 1: Foundations

| ID | Micro-topic | Status | Gate |
| --- | --- | --- | --- |
| L01-01 | <Smallest first concept> | current | <Quiz prompt> |
| L01-02 | <Next concept> | locked | <Gate depends on L01-01> |

## Stage 2: Application

| ID | Micro-topic | Status | Gate |
| --- | --- | --- | --- |
| L02-01 | <First practical concept> | locked | <Quiz prompt> |
```

## STATE.md

```md
# Learning State

## Current Topic

- ID: <L01-01>
- Title: <Smallest first concept>
- Status: <current / quiz / passed / review>

## Last Explanation

<One or two sentence summary of what was taught.>

## Current Quiz Gate

<The exact question currently waiting for the learner, if any.>

## Learner Answer

<Latest answer or empty if waiting.>

## Gate Decision

- Result: <waiting / passed / repair-needed>
- Reason: <short explanation>

## Misconceptions To Repair

- <Misconception or empty>

## Next Action

<Ask learner to answer / repair concept / unlock next micro-topic.>

## Completed Gates

- <L01-01>: <date or checkpoint label>
```

## source-analysis.md

```md
# Source Analysis

## Source

- Path or URL:
- Date reviewed:
- Scope:

## Useful Learning Material

- <Key idea that should become a micro-topic>

## Not For Beginner Path Yet

- <Advanced idea to postpone>

## Roadmap Implications

- <How this source changes the learning path>
```
