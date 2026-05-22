# Lovable Skills

Reusable skills by Lucio Amorim for [Lovable](https://lovable.dev).

This repository is the catalog and working source for Lucio Amorim's Lovable skills.

For the easiest Lovable import, use the standalone GitHub repository for the skill you want. Each standalone repository has a single `SKILL.md` at its root.

Each skill identifies its source repository and version inside its own instructions. When a skill runs, its response includes the installed version, tries to compare it with the repo version, and labels the status as current, update available, or unverified.

## Available skills

| Skill | What it does | Import |
| --- | --- | --- |
| `/wireframe` | Reads the current codebase and writes a dense `WIREFRAME.md` from real routes, components, copy, CTAs, layouts, and visible Supabase schema. | [Import repo](https://github.com/lucioamor/lovable-skill-wireframe) |
| `/debate` | Runs an advisory expert panel with opposing views for product, UI, UX, copy, architecture, performance, data, or security decisions. | [Import repo](https://github.com/lucioamor/lovable-skill-debate) |

## Import into Lovable

1. Open `Settings -> Skills -> Add -> Import from GitHub`.
2. Paste the standalone repository URL for the skill you want:

```text
https://github.com/lucioamor/lovable-skill-wireframe
https://github.com/lucioamor/lovable-skill-debate
```

Lovable imports one skill at a time. Do not paste this catalog repository URL into the importer.

## Skill details

### `/wireframe`

Use `/wireframe` to generate a wireframe for all routes, or `/wireframe /route` to focus on one route such as `/dashboard`.

The skill writes `WIREFRAME.md` at the project root. If that file already exists, it asks whether to overwrite it or save a timestamped version such as `WIREFRAME-YYYY-MM-DD_HH-MM.md`.

Full instructions: [`skills/wireframe/SKILL.md`](./skills/wireframe/SKILL.md)

Example output: [`examples/WIREFRAME-nxlv.md`](./examples/WIREFRAME-nxlv.md)

### `/debate`

Use `/debate` when you want a decision discussed before implementation. The skill casts specialists with real disagreement, produces the trade-offs, and ends with a decision matrix and a clear read.

Full instructions: [`skills/debate/SKILL.md`](./skills/debate/SKILL.md)

## Repositories

| Repository | Purpose |
| --- | --- |
| [`lucioamor/lovable-skill-wireframe`](https://github.com/lucioamor/lovable-skill-wireframe) | Importable `/wireframe` skill with `SKILL.md` at the repository root. |
| [`lucioamor/lovable-skill-debate`](https://github.com/lucioamor/lovable-skill-debate) | Importable `/debate` skill with `SKILL.md` at the repository root. |
| [`lucioamor/lovable-skills`](https://github.com/lucioamor/lovable-skills) | Central catalog and working source for the skills. |

## Versions

Current published versions:

| Skill | Version | Latest source |
| --- | --- | --- |
| `/wireframe` | `v1.0.0` | [`lovable-skill-wireframe/VERSION.md`](https://github.com/lucioamor/lovable-skill-wireframe/blob/main/VERSION.md) |
| `/debate` | `v1.0.0` | [`lovable-skill-debate/VERSION.md`](https://github.com/lucioamor/lovable-skill-debate/blob/main/VERSION.md) |

If a running skill shows an older version than its standalone repo, import that repo again in Lovable to update it.

## Catalog shape

```text
skills/
|-- debate/
|   `-- SKILL.md
`-- wireframe/
    `-- SKILL.md
```

The folders above keep the central source organized. The standalone repositories are the recommended import path because each one exposes a single root `SKILL.md`.

## License

[MIT](./LICENSE)
