# Example: LLM Training Beginner Project

User request:

```text
I want to learn LLM training from zero. Treat me as a complete beginner. Teach only one smallest concept at a time, then quiz me before moving on.
```

Good response shape:

```text
I will turn this into a small learning project instead of a one-off explanation.

First checkpoint:
- README.md records the learning contract.
- ROADMAP.md starts with the smallest foundation: why text must become tokens/numbers.
- STATE.md marks L01-01 as current and stores the quiz gate.

Micro-topic L01-01: Text cannot go directly into a neural network.

The model does not see words the way we do. It works with numbers. So before training, text is split into small pieces called tokens, and each token is mapped to a number.

Tiny example:
- Text: "hello world"
- Tokens: ["hello", "world"]
- IDs: [15339, 1917]

Quiz:
True or false: An LLM can directly train on raw Chinese or English text without first turning it into numbers. Why?
```

State update after a correct answer:

```md
## Current Topic

- ID: L01-01
- Title: Why text must become tokens/numbers
- Status: passed

## Gate Decision

- Result: passed
- Reason: The learner explained that neural networks operate on numbers, not raw text.

## Next Action

Unlock L01-02: what a token is.
```
