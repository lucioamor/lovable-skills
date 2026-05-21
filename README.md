# Lovable Skills - by Lucio Amorim

Reusable skills for [Lovable](https://lovable.dev).

This repository contains multiple Lovable skills. Each importable skill has its own folder with a `SKILL.md` file directly inside it.

## Skills

### `/wireframe` - Codebase to WIREFRAME.md

Reads the actual codebase (routes, components, exact copy, CTAs, layouts, and Supabase schema) and generates a dense, LLM-readable wireframe in markdown.

**Usage:**

- `/wireframe` — generate wireframe for **all** routes
- `/wireframe /route` — generate wireframe for a **single** route (e.g. `/wireframe /dashboard`)

**Output:** writes to `WIREFRAME.md` at project root. If the file already exists, Lovable will ask whether to **overwrite** or save as a timestamped version (`WIREFRAME-YYYY-MM-DD_HH-MM.md`).

See [`skills/wireframe/SKILL.md`](./skills/wireframe/SKILL.md) for the full spec.

### `/debate` - Expert panel

Convenes specialists with opposing views to analyze UI, UX, copy, architecture, performance, or security decisions before implementation.

See [`skills/debate/SKILL.md`](./skills/debate/SKILL.md) for the full spec.

## Installation

### Import from GitHub

In Lovable, go to Settings -> Skills -> Add -> Import from GitHub and paste the folder URL for the skill you want.

```text
https://github.com/<owner>/<repo>/tree/main/skills/wireframe
https://github.com/<owner>/<repo>/tree/main/skills/debate
```

For repositories with multiple skills, Lovable expects the linked directory to contain `SKILL.md` directly.

### Upload ZIP

Zip one skill folder at a time so its `SKILL.md` is at the archive root or inside a single wrapping folder.

## Usage

Use the imported skill in Lovable's chat, for example `/wireframe` or `/debate`.

## Example output

See [`examples/WIREFRAME-nxlv.md`](./examples/WIREFRAME-nxlv.md) for a real-world example generated from the [NXLV.AI](https://be.nxlv.ai) codebase.

## License

[MIT](./LICENSE)
