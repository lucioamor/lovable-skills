# /debate

`/debate` runs a structured expert panel with opposing schools of thought, then ends with a decision matrix and a clear read.

It is part of the central [`lovable-skills`](https://github.com/lucioamor/lovable-skills) catalog. The importable standalone repository is [`lovable-skill-debate`](https://github.com/lucioamor/lovable-skill-debate).

## What it does

`/debate` is for moments where builders make bad calls:

- when they do not know what direction to take
- when they are too confident they already do

The skill casts specialists who should disagree. For example:

- conservative vs. experimental
- minimalist vs. trend-sensitive
- frictionless vs. deliberate-friction
- pragmatic architecture vs. clean-boundary architecture
- profiler-first performance vs. payload minimization
- trust-led copy vs. conversion-led copy

The disagreement is the point. A panel that agrees too quickly has failed.

## When to use it

Use `/debate` when you want to pressure-test a decision before implementation:

- UX direction when something feels off
- copy when every version sounds equally fine
- architecture when "good enough" might hide future cost
- onboarding flows
- AI feature behavior
- pricing or GTM positioning
- security, auth, and data access decisions
- performance trade-offs

Example:

```text
/debate the pricing page feels generic and I don't know why
```

Example:

```text
/debate is it okay to keep this auth check on the client?
```

Example:

```text
/debate should onboarding be shorter, or should we add one more qualifying step?
```

## Example flow

1. You invoke `/debate` with a question or rough concern.
2. The skill infers the domain and desired posture.
3. It casts a small panel of opposing experts.
4. If the question depends on existing code, it reads the relevant files first.
5. The experts argue the trade-offs.
6. The response ends with a decision matrix and "the read".
7. For architecture, security, data, or high-impact product decisions, it may save a trace file.

## Output shape

Every serious debate ends with:

- the strongest options still standing
- what each option wins
- what each option loses
- risk
- effort
- best-fit scenario
- a short read explaining the real trade-off

The goal is not expert theater. The goal is a decision you can act on.

## What it does not do

`/debate` does not:

- implement code
- rewrite copy directly unless the debate calls for example wording
- force consensus on subjective design questions
- make risky architecture or security calls look like taste
- replace measurement for performance issues
- keep asking clarifying questions until the user does the framing work

If the prompt is vague, it asks at most once and then proceeds with its best diagnosis.

## How it behaves

The skill changes posture by domain:

- architecture, security, data, stack, integrations: converge on the safest defensible path
- performance: converge around what measurement would likely show
- UI, copy, branding, positioning: preserve divergent strong directions
- UX: diverge on vision, converge on accessibility and user-protection constraints

When the question mentions an existing screen, flow, schema, or implementation, the skill inspects relevant files before judging. If it cannot find them, it says so and continues as a conceptual review.

Every run includes the installed skill version and checks whether the standalone source repo appears current.

## Related skills

- [`/wireframe`](../wireframe/README.md) generates a plain-text `WIREFRAME.md` from the real app.

Use `/wireframe` first when `/debate` needs a complete map of routes, copy, layout, and component structure.
