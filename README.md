# Lovable Skills — by Lucio Amorim

Reusable skills for [Lovable](https://lovable.dev). Drop them into any project's `.lovable/skills/` folder and use the commands in chat.

## Installed skills

### `/wireframe` — Codebase → WIREFRAME.md

Reads the actual codebase (routes, components, exact copy, CTAs, layouts, and Supabase schema) and generates a dense, LLM-readable wireframe in markdown.

**Usage:**

- `/wireframe` — generate wireframe for **all** routes
- `/wireframe /route` — generate wireframe for a **single** route (e.g. `/wireframe /dashboard`)

**Output:** writes to `WIREFRAME.md` at project root. If the file already exists, Lovable will ask whether to **overwrite** or save as a timestamped version (`WIREFRAME-YYYY-MM-DD_HH-MM.md`).

See [`skills/wireframe.md`](./skills/wireframe.md) for the full spec.

## Installation

1. Copy the skill file into your Lovable project:

   ```
   your-project/
   └── .lovable/
       ├── README.md          ← (optional) note that skills are installed
       └── skills/
           └── wireframe.md   ← copy this file
   ```

2. Use the command in Lovable's chat: type `/wireframe`

## Example output

See [`examples/WIREFRAME-nxlv.md`](./examples/WIREFRAME-nxlv.md) for a real-world example generated from the [NXLV.AI](https://be.nxlv.ai) codebase.

## License

[MIT](./LICENSE)
