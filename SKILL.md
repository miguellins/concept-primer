---
name: concept-primer
description: Teach a complex technical, theoretical, mathematical, or architectural concept from scratch using problem-first framing, upfront analogies, scaffolded complexity, and low-stakes intuition checks before formal testing. Use when the user wants to learn a new topic, feels confused, needs a baseline mental model, asks for a primer, or should build understanding before using a Feynman-style check.
---

# Concept Primer

## Purpose

Build an intuitive baseline mental model before testing begins. Explain why the concept exists, anchor it in a familiar real-world analogy, then reveal technical detail gradually.

## Teaching Rules

- Start with the problem the concept solves before defining the concept.
- Use a mundane analogy early, such as traffic, cooking, plumbing, a library, a shipping dock, a restaurant kitchen, or a post office.
- Keep explanations bite-sized. Do not deliver a textbook-style wall of text.
- Reveal complexity in layers: problem, analogy, blueprint, mechanics, intuition check.
- Prefer visual, concrete language over abstract terminology.
- Ask one low-stakes pulse check at the end of each phase before going deeper when the user is actively learning interactively.
- Use elaborative interrogation: ask brief why/predict questions that make the learner reason about design tradeoffs.
- Do not grade harshly. If the user is wrong or unsure, repair the mental model and continue.
- When the user indicates the baseline mechanics make sense, suggest switching to `feynman-understanding-check` if that skill is available or was requested.

## Workflow

### 1. Identify the Target

If the topic is missing, ask what concept the user wants to learn. If useful, ask for adjacent knowledge in one short question, such as whether they already know a prerequisite or where they encountered the topic.

If the user already named the concept, begin without extra questioning unless context would materially change the explanation.

### 2. Phase 1: The Villain and the Hero

Explain the headache that existed before the concept:

- What problem, limitation, confusion, or inefficiency appears without it?
- Why does that problem matter in practice?
- In two sentences, how does the concept act as the solution?

Avoid formal definitions until this problem frame is clear.

### 3. Phase 2: The Anchor Analogy

Choose one familiar analogy and map the concept entirely inside that world before introducing technical vocabulary.

Use this shape:

```text
Think of [Topic] like a [mundane system]. In this world:
- [Analogy part] handles...
- [Analogy part] decides...
- [Analogy part] prevents...
```

Keep the analogy useful but bounded. Mention where it stops fitting if the mismatch could mislead the learner.

### 4. Phase 3: The Blueprint

Translate the analogy into the real concept with exactly three main moving parts when possible.

Use this shape:

```text
Now map that back to the real thing:
- [Analogy component] -> [Technical term]
- [Analogy component] -> [Technical term]
- [Analogy component] -> [Technical term]
```

Then describe the workflow in 3 to 5 steps. Keep terminology light and define new terms immediately.

### 5. Phase 4: The Mechanics

Only after the blueprint is clear, explain how the parts actually interact.

For technical topics, include a minimal concrete example, pseudocode, small diagram in text, or short scenario when it would clarify the flow. For math-heavy topics, use a tiny numeric example before general notation. For architecture topics, describe the request/data path and ownership boundaries.

### 6. Phase 5: Intuition Check

Ask one predictive scenario question rather than a definition quiz.

Examples:

```text
If we removed [Component B], what do you think would break first?
```

```text
If this system suddenly had 100 times more traffic/data/inputs, where would the bottleneck likely appear?
```

```text
Why do you think the designers chose [X] instead of the simpler [Y]?
```

If the user answers well, briefly confirm the intuition and offer a deeper layer or a Feynman-style check. If not, explain the missing link using the same analogy, then ask a simpler version.

## Response Patterns

When starting from no topic:

```text
What concept are we tackling, and what background do you already have around it?
```

When starting a primer:

```text
Before we define [Topic], look at the headache it solves: [problem]. Without it, [consequence]. [Topic] exists to [solution].
```

When anchoring:

```text
Think of [Topic] like a [analogy]. In this world, [part] is responsible for [role], while [part] keeps [constraint] from becoming a mess.
```

When checking intuition:

```text
Quick intuition check: if [scenario happens], what do you think breaks or slows down first?
```

## Handoff

When the learner says the baseline mechanics make sense, transition from teaching to testing:

```text
You have the basic model now. The next useful step is a Feynman check: explain it back in plain language, then we will find the weak spots.
```
