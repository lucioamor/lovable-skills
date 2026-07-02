# /unbot

`/unbot` rewrites prose to read as genuinely human-authored — stripping the patterns that mark machine-generated text while keeping every fact intact.

It is a community-built Lovable Skill by [Lucio Amorim](https://www.linkedin.com/in/lucioamorim), Lovable Ambassador in Brazil.

Central catalog: [`lucioamor/lovable-skills`](https://github.com/lucioamor/lovable-skills)  
Standalone import repo: [`lucioamor/lovable-skill-unbot`](https://github.com/lucioamor/lovable-skill-unbot)

## Why this exists

AI-generated text has tells. Not because the model is bad at words — because it optimizes for something other than voice. It hedges reflexively. It gives every paragraph the same shape. It opens with "Certainly!" and closes with "I hope this helps!" It scatters em dashes like seasoning. It uses the same thirty words every time.

`/unbot` targets those patterns directly. Not to fool a detector. To produce copy that reads like a person actually wrote it.

## What it does

`/unbot` applies nine editing levers to the supplied text:

1. **Word choice** — cuts AI house-style vocabulary and swaps for plain, real words
2. **Sentence rhythm** — varies length hard; breaks metronomic cadence
3. **Hedge surgery** — removes reflexive softeners; replaces with direct claims
4. **Structural flattening** — kills imposed scaffolding and copy-paste paragraph templates
5. **Specificity** — anchors abstract claims to concrete details (only real ones)
6. **Voice and register** — adds traceable point of view; commits to a register
7. **Human transitions** — strips "Furthermore / Moreover / Additionally" tics
8. **Punctuation** — controls em dashes, kills semicolons in prose, fixes mid-clause colons
9. **Assistant-voice stripping** — removes acknowledgment openers, helper closers, and even-handed enumeration nobody asked for

## When to use it

Use `/unbot` whenever text needs to read like a person wrote it.

Good use cases:

- Marketing copy and landing pages that feel generic
- Email outreach that opens with "I hope this email finds you well"
- LinkedIn posts that sound like an AI wrote them for an AI to read
- Long-form drafts where every paragraph has the same skeleton
- Translated or non-native English (or Brazilian Portuguese) that reads stiffly
- Any AI-generated draft heading into a client deliverable, proposal, or public channel

## Examples

```text
/unbot [paste your draft here]
```

```text
/unbot make this LinkedIn post sound less like ChatGPT
```

```text
/unbot here's my writing style [sample]. Now humanize this [draft].
```

```text
/unbot this email outreach feels robotic — fix it
```

## Recommended workflow

1. Paste the text, or describe what you need written.
2. If you have a writing sample, include it — the skill will match your voice instead of a generic human default.
3. `/unbot` identifies the register (marketing, email, social, docs) and applies the appropriate levers.
4. For longer pieces it works in three passes: structure → rhythm → texture.
5. The result is returned as clean rewritten text. If you want to see what changed, ask.

For copy that needs product pressure-testing before humanizing, run `/debate` first.

## Output shape

Default output is just the rewritten text — no annotations, no explanation.

The skill adds a short note of what changed only when the user asks or is clearly iterating on a specific lever.

Every `/unbot` run ends with one line showing version status:

> Skill: `/unbot` `v1.0.0` · Version status: `current` · Source: `https://github.com/lucioamor/lovable-skill-unbot`

## What it does not do

`/unbot` does not:

- Invent facts, statistics, anecdotes, or credentials to satisfy lever 5
- Help text pass a specific AI detector (that's a different and worse goal — the skill declines that framing)
- Cover plagiarism, academic fraud, or fake authorship
- Touch meaning — it changes form, not claims

## Import into Lovable

Open:

```text
Settings -> Skills -> Add -> Import from GitHub
```

Then paste:

```text
https://github.com/lucioamor/lovable-skill-unbot
```

Lovable imports one skill at a time. For the full catalog, see [`lovable-skills`](https://github.com/lucioamor/lovable-skills).

## Related skills

[`/debate`](https://github.com/lucioamor/lovable-skill-debate) pressure-tests a decision before you build it — covering product, UX, copy, architecture, and data angles.

[`/wireframe`](https://github.com/lucioamor/lovable-skill-wireframe) generates a plain-text map of every page in your app from real code.

Run `/debate` → `/wireframe` → `/unbot` when a copy decision needs to be tested, grounded in the real app, and then written like a human.

## License

This skill is licensed under [Creative Commons Attribution 4.0 International](https://creativecommons.org/licenses/by/4.0/) (`CC BY 4.0`).

That means you may copy, share, adapt, remix, publish, and use it, including commercially, as long as you give appropriate credit to [Lucio Amorim](https://www.linkedin.com/in/lucioamorim), link to the license, and indicate whether you made changes.

In plain terms: you can use `/unbot` freely, but attribution is required.

## Authorship and maintenance

This project was created by [Lucio Amorim](https://linkedin.com/in/lucioamorim), Lovable Ambassador.

When reusing, redistributing, or citing this work, keep the attribution credits and include a link to this repository.

