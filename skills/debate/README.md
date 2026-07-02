# /debate

`/debate` runs a structured expert panel with opposing schools of thought, then ends with a decision matrix and a clear read.

It is a community-built Lovable Skill by [Lucio Amorim](https://www.linkedin.com/in/lucioamorim), Lovable Ambassador in Brazil.

Central catalog: [`lucioamor/lovable-skills`](https://github.com/lucioamor/lovable-skills)  
Standalone import repo: [`lucioamor/lovable-skill-debate`](https://github.com/lucioamor/lovable-skill-debate)

## Why this exists

Builders usually make bad decisions in two moments:

1. when they do not know what direction to take
2. when they are too confident they already do

`/debate` is built for both.

It turns uncertainty into structured disagreement. Instead of asking one model for one confident answer, it casts experts with conflicting priors and forces the trade-offs into the open.

The point is not theater. The point is to make premature consensus harder.

## What it does

`/debate` creates a small panel of specialists who should disagree.

Depending on the problem, the panel may include perspectives such as:

- conservative vs. experimental
- minimalist vs. trend-sensitive
- frictionless vs. deliberate-friction
- pragmatic architecture vs. clean-boundary architecture
- profiler-first performance vs. payload minimization
- trust-led copy vs. conversion-led copy
- growth-oriented onboarding vs. user-protection onboarding
- implementation speed vs. long-term maintainability

A panel that agrees too quickly has failed. The skill is designed to expose the strongest version of each serious option before recommending what to do next.

## When to use it

Use `/debate` when a decision is important enough to pressure-test before implementation.

Good use cases:

- UX direction when something feels off
- copy when every version sounds equally fine
- architecture when "good enough" might hide future cost
- onboarding flows
- AI feature behavior
- pricing or GTM positioning
- security, auth, and data access decisions
- performance trade-offs
- product scope decisions
- positioning choices where taste may be masking strategy

## Examples

```text
/debate the pricing page feels generic and I don't know why
```

```text
/debate is it okay to keep this auth check on the client?
```

```text
/debate should onboarding be shorter, or should we add one more qualifying step?
```

```text
/debate based on WIREFRAME.md, where is the dashboard losing clarity?
```

## Recommended workflow

1. Invoke `/debate` with a question, concern, or decision.
2. The skill infers the domain and the right posture.
3. It casts a panel of opposing experts.
4. If the question depends on existing code, it reads the relevant files first.
5. The experts argue the trade-offs.
6. The response ends with a decision matrix and "the read".
7. For architecture, security, data, or high-impact product decisions, it may save a trace file.

For product or UX decisions based on an existing app, run `/wireframe` first and debate from the generated `WIREFRAME.md`.

## Output shape

Every serious debate ends with:

- strongest options still standing
- what each option wins
- what each option loses
- risk
- effort
- best-fit scenario
- the read: a short explanation of the real trade-off

The result should be actionable. You should leave knowing what to do, what to avoid, and what assumption matters most.

## How it behaves by domain

The skill changes posture depending on the type of problem.

For architecture, security, data, stack, and integrations, it converges on the safest defensible path.

For performance, it converges around what measurement would likely show and what should be tested first.

For UI, copy, branding, and positioning, it preserves divergent strong directions instead of pretending there is one objective answer.

For UX, it diverges on product vision but converges on accessibility, user protection, and clarity constraints.

When the question mentions an existing screen, flow, schema, or implementation, the skill inspects relevant files before judging. If it cannot find them, it says so and continues as a conceptual review.

## What it does not do

`/debate` does not:

- implement code
- rewrite copy directly unless example wording is needed
- force consensus on subjective design questions
- treat architecture or security as taste
- replace measurement for performance issues
- keep asking clarifying questions until the user does the framing work

If the prompt is vague, it asks at most once and then proceeds with its best diagnosis.

## Import into Lovable

Open:

```text
Settings -> Skills -> Add -> Import from GitHub
```

Then paste:

```text
https://github.com/lucioamor/lovable-skill-debate
```

Lovable imports one skill at a time. For the full catalog, see [`lovable-skills`](https://github.com/lucioamor/lovable-skills).

## Related skill

[`/wireframe`](https://github.com/lucioamor/lovable-skill-wireframe) generates a plain-text `WIREFRAME.md` from the real app.

Use `/wireframe` first when `/debate` needs a complete map of routes, copy, layout, and component structure.

## License

This skill is licensed under [Creative Commons Attribution 4.0 International](https://creativecommons.org/licenses/by/4.0/) (`CC BY 4.0`).

That means you may copy, share, adapt, remix, publish, and use it, including commercially, as long as you give appropriate credit to [Lucio Amorim](https://www.linkedin.com/in/lucioamorim), link to the license, and indicate whether you made changes.

In plain terms: you can use `/debate` freely, but attribution is required.

## Authorship and maintenance

This project was created by [Lucio Amorim](https://linkedin.com/in/lucioamorim), Lovable Ambassador.

When reusing, redistributing, or citing this work, keep the attribution credits and include a link to this repository.

