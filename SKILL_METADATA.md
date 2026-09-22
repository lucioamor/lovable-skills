# Skill Metadata

This file records the internal metadata contract for skills in this catalog.
The `SKILL.md` frontmatter remains the source of truth; keep this record in sync when a skill is added or its description changes.

## Description contract

- Treat each `SKILL.md` frontmatter `description` as the pre-import popup copy.
- Write it as a short operating instruction so a new user knows what the skill does before importing it.
- Keep it under 300 characters.
- State the trigger or command, the core behavior, the main output, and any essential boundary.
- Apply this rule to every current and new skill.

## Current descriptions

| Skill | Description |
| --- | --- |
| `/jevify` | Run /jevify for a read-only diagnosis of runtime AI calls in a Lovable project. Distinguishes generation from structured decisions and proposes candidates for JEV. Returns a report in chat without changing code. Targets runtime AI cost, not build credits. |
| `/wireframe` | Run /wireframe to map the active page (or root if unknown) with every real title, button, and section label in screen order. Add a page name to pick a specific page. Add "all" to map the whole app. Never invent copy. |
| `/debate` | Run /debate to convene opposing specialists for a product, UI, UX, copy, architecture, performance, data, or security decision. It inspects relevant code when needed, argues trade-offs, ends with a decision matrix and read, and does not implement. |
| `/unbot` | Run /unbot to rewrite or generate prose so it reads as genuinely human-authored, not machine-generated. Applies nine editing levers — word choice, rhythm, hedges, structure, specificity, voice, transitions, punctuation, and assistant-voice stripping. Works across marketing, email, essays, social, and docs. Does not fabricate facts. |
