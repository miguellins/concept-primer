# Concept Primer

Build intuition for complex concepts before asking the learner to prove mastery.

`concept-primer` is a Codex skill for teaching technical, theoretical, mathematical, and architectural ideas from the ground up. It starts with the practical problem a concept solves, anchors the idea in a familiar analogy, then gradually maps that intuition back to real mechanics.

> [!NOTE]
> This skill is designed for first-pass understanding. Once the learner can explain the baseline mechanics, pair it with a Feynman-style understanding check to expose weak spots.

## Why use it?

Complex ideas often become harder because the explanation starts with formal vocabulary too early. This skill flips the order:

- Start with the headache the concept solves.
- Use a mundane analogy to make the shape of the idea visible.
- Translate the analogy into exactly a few real moving parts.
- Add mechanics only after the learner has a mental model.
- End with a predictive intuition check instead of a definition quiz.

## How it works

The teaching flow is intentionally layered:

| Phase | Goal |
| --- | --- |
| 1. Villain and Hero | Explain the problem before defining the concept. |
| 2. Anchor Analogy | Map the idea into a familiar system such as traffic, cooking, plumbing, libraries, or shipping docks. |
| 3. Blueprint | Translate the analogy back into three main technical moving parts where possible. |
| 4. Mechanics | Show how the parts interact with a concrete example, tiny diagram, pseudocode, or scenario. |
| 5. Intuition Check | Ask a low-stakes predictive question that tests the learner's model. |

## Example prompts

```text
Use $concept-primer to teach me event sourcing from scratch.
```

```text
Use $concept-primer to explain eigenvectors. I remember basic matrix multiplication but not much else.
```

```text
Use $concept-primer to give me a baseline mental model for Kubernetes controllers.
```

## When to use it

Use this skill when the learner:

- Feels confused by a concept and needs a simple starting model.
- Is encountering a new architecture, algorithm, theory, or math topic.
- Needs an explanation before a formal quiz or Feynman check.
- Benefits from analogies, diagrams, small examples, and scaffolded complexity.

## Teaching style

`concept-primer` keeps lessons compact and interactive. It avoids textbook-style walls of text, defines new terms immediately, and asks brief pulse checks before going deeper when the learner is actively participating.

When the learner struggles, the skill repairs the mental model using the same analogy instead of treating the answer as a failure.

## Package contents

```text
.
├── SKILL.md
└── agents/
    └── openai.yaml
```

- `SKILL.md` contains the teaching rules, workflow, response patterns, and handoff guidance.
- `agents/openai.yaml` defines the display name, short description, and default prompt for agent interfaces.

## Quick start

Install or keep this directory in your Codex skills path, then invoke it by name:

```text
$concept-primer
```

For best results, name the concept and mention any relevant background:

```text
Use $concept-primer to teach me CQRS. I already know basic REST APIs and relational databases.
```
