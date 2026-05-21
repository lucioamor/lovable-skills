# Lovable Skills

Reusable skills by Lucio Amorim for [Lovable](https://lovable.dev).

This repository keeps more than one skill. Each skill lives in its own folder under `skills/`, with the `SKILL.md` file that Lovable imports directly inside that folder.

## Available skills

| Skill | What it does | Import |
| --- | --- | --- |
| `/wireframe` | Reads the current codebase and writes a dense `WIREFRAME.md` from real routes, components, copy, CTAs, layouts, and visible Supabase schema. | [Import folder](https://github.com/lucioamor/lovable-skills/tree/main/skills/wireframe) |
| `/debate` | Runs an advisory expert panel with opposing views for product, UI, UX, copy, architecture, performance, data, or security decisions. | [Import folder](https://github.com/lucioamor/lovable-skills/tree/main/skills/debate) |

## Import into Lovable

1. Open `Settings -> Skills -> Add -> Import from GitHub`.
2. Paste the GitHub folder URL for the skill you want:

```text
https://github.com/lucioamor/lovable-skills/tree/main/skills/wireframe
https://github.com/lucioamor/lovable-skills/tree/main/skills/debate
```

Lovable imports one skill at a time. Because this repository contains multiple skills, use the folder URL for the chosen skill instead of the repository root.

## Skill details

### `/wireframe`

Use `/wireframe` to generate a wireframe for all routes, or `/wireframe /route` to focus on one route such as `/dashboard`.

The skill writes `WIREFRAME.md` at the project root. If that file already exists, it asks whether to overwrite it or save a timestamped version such as `WIREFRAME-YYYY-MM-DD_HH-MM.md`.

Full instructions: [`skills/wireframe/SKILL.md`](./skills/wireframe/SKILL.md)

Example output: [`examples/WIREFRAME-nxlv.md`](./examples/WIREFRAME-nxlv.md)

### `/debate`

Use `/debate` when you want a decision discussed before implementation. The skill casts specialists with real disagreement, produces the trade-offs, and ends with a decision matrix and a clear read.

Full instructions: [`skills/debate/SKILL.md`](./skills/debate/SKILL.md)

## Repository shape

```text
skills/
|-- debate/
|   `-- SKILL.md
`-- wireframe/
    `-- SKILL.md
```

That layout follows Lovable's multi-skill GitHub import shape: the linked skill directory must contain `SKILL.md` directly.

## License

[MIT](./LICENSE)
