# Lucio's Lovable Skills

A collection of reusable Lovable Skills by [Lucio Amorim](https://www.linkedin.com/in/lucioamorim), Lovable Ambassador in Brazil.

These are skills I built and use to make Lovable projects easier to review, understand, and improve — whether you are working alone, with a team, or with other AI tools.

## What is a Skill?

A Skill is a saved set of instructions that Lovable can follow on command. Think of it like teaching Lovable a new trick: instead of typing the same long prompt every time, you just type the skill name and it knows exactly what to do.

Skills are different from Project Knowledge. Project Knowledge stores facts your app should remember. Skills store processes your app should run consistently.

## Available skills

| Skill | What it does |
| --- | --- |
| `/wireframe` | Reads your entire app and writes a plain-text document with every page's real layout, text, buttons, filters, and interactive elements. Great for sharing context with other AI tools or reviewers. |
| `/debate` | Brings in a panel of opposing specialists to pressure-test a decision before you build it — covering product, design, copy, technical, and data angles. |

All skills are available at: [lucioamor/lovable-skills](https://github.com/lucioamor/lovable-skills)

## How to add a skill to Lovable

Open Lovable and go to:

```text
Settings → Skills → Add → Import from GitHub
```

Paste the link for the skill you want:

```text
https://github.com/lucioamor/lovable-skill-wireframe
https://github.com/lucioamor/lovable-skill-debate
```

Lovable imports one skill at a time. You can add both.

Do not paste this catalog page URL. Use the individual skill links above.

## Recommended workflow

Run `/wireframe` first to get a clear picture of what your app currently looks like.

Then run `/debate` when the next decision is not obvious, or when you want to find blind spots before committing.

Example:

```text
/wireframe
```

Then:

```text
/debate based on WIREFRAME.md, why does the sign-up flow feel confusing?
```

This works especially well when switching between Lovable and external AI tools like ChatGPT, Claude, Gemini, or Grok — or when sharing context with a reviewer, client, or teammate.

## Skill details

### `/wireframe`

Maps the active page (or home page if unknown):

```text
/wireframe
```

Maps one specific page:

```text
/wireframe dashboard
```

Maps every page in the app into a single file:

```text
/wireframe all
```

`/wireframe` reads the active page and writes a `WIREFRAME-{page}.md` file with every word of visible text, every button, every link, and every interactive element like filters and dropdowns. Use `/wireframe all` to map the full app into a single `WIREFRAME.md`.

When a page has very large tables or long blocks of text, the skill creates an abbreviated version and tells you the best format for reviewing the full data.

It does not design new screens, write placeholder text, judge the design, or make any changes to the app.

Full instructions: [`skills/wireframe/SKILL.md`](./skills/wireframe/SKILL.md)  
Skill README: [`skills/wireframe/README.md`](./skills/wireframe/README.md)  
Example output: [`examples/WIREFRAME-nxlv.md`](./examples/WIREFRAME-nxlv.md)

### `/debate`

```text
/debate [topic or question]
```

`/debate` pressure-tests a decision before you build it. It convenes specialists who argue opposing sides across different domains:

- convergent (one right answer matters) for technical architecture, security, data, and performance
- divergent (creative tension is useful) for design, copy, branding, and positioning
- mixed for user experience, where vision may differ but clarity and user protection still matter

It does not implement anything. It ends with trade-offs, a decision matrix, and a recommendation.

Full instructions: [`skills/debate/SKILL.md`](./skills/debate/SKILL.md)  
Skill README: [`skills/debate/README.md`](./skills/debate/README.md)

## Repositories

| Repository | Purpose |
| --- | --- |
| [`lucioamor/lovable-skills`](https://github.com/lucioamor/lovable-skills) | Central home for all skills. Start here. |
| [`lucioamor/lovable-skill-wireframe`](https://github.com/lucioamor/lovable-skill-wireframe) | Import-ready `/wireframe` skill. |
| [`lucioamor/lovable-skill-debate`](https://github.com/lucioamor/lovable-skill-debate) | Import-ready `/debate` skill. |

## Versioning

Each skill tracks its own version. When you run a skill, it tells you the installed version and checks whether an update is available in its source repository.

Version status will show as:

- **current** — you have the latest version
- **update available** — a newer version exists; re-import the skill to update
- **unverified** — the check could not reach the source

Current published versions:

| Skill | Version | Check for updates |
| --- | --- | --- |
| `/wireframe` | `v1.1.0` | [`lovable-skill-wireframe`](https://github.com/lucioamor/lovable-skill-wireframe) |
| `/debate` | `v1.0.0` | [`lovable-skill-debate`](https://github.com/lucioamor/lovable-skill-debate) |

If a skill shows an older version, re-import its repository in Lovable to update it.

Maintainer workflow: [`MAINTENANCE.md`](./MAINTENANCE.md)

## About the author

Created and maintained by [Lucio Amorim](https://www.linkedin.com/in/lucioamorim), Lovable Ambassador in Brazil.

These skills are practical infrastructure for builders who use Lovable seriously: not just to generate apps, but to review them, move context between tools, pressure-test decisions, and make better product choices faster.

## License

[MIT](./LICENSE)

---

## How these skills are built (technical reference)

This section is for developers, contributors, or curious readers who want to understand how the skill system works under the hood.

### What a Skill is, technically

A Lovable Skill is a Markdown file (`SKILL.md`) with a YAML frontmatter block at the top and a set of instructions written in plain English below it. Lovable reads the frontmatter to register the skill's name and a short description, and reads the instructions to know how to behave when the skill is triggered.

Example frontmatter:

```yaml
---
name: wireframe
description: Run /wireframe to read your app and write WIREFRAME.md...
---
```

The instructions below the frontmatter are written so that an AI can follow them reliably: they define the trigger, the workflow steps, the output format, and any edge-case rules.

### Repository structure

This catalog repository stores the authoritative source for each skill:

```text
lovable-skills/
├── skills/
│   ├── wireframe/
│   │   ├── SKILL.md       ← authoritative skill instructions
│   │   ├── README.md      ← user-facing documentation
│   │   └── VERSION.md     ← current version
│   └── debate/
│       ├── SKILL.md
│       ├── README.md
│       └── VERSION.md
├── examples/              ← sample output files
├── MAINTENANCE.md         ← maintainer workflow
└── SKILL_METADATA.md      ← description contract
```

### Standalone import repositories

Lovable's import tool requires a GitHub repository with a `SKILL.md` at the root. Because of this, each skill also lives in its own standalone repository:

- [`lucioamor/lovable-skill-wireframe`](https://github.com/lucioamor/lovable-skill-wireframe)
- [`lucioamor/lovable-skill-debate`](https://github.com/lucioamor/lovable-skill-debate)

These standalone repositories are export targets, not editing targets. The canonical source lives in `skills/<skill-name>/SKILL.md` in this catalog. When a skill is updated here, the corresponding standalone repository should be synced.

The export contract is documented in [`MAINTENANCE.md`](./MAINTENANCE.md).

### Versioning convention

Each skill follows simple semantic versioning (`v1.0.0`). The version is stored in `VERSION.md` inside the skill folder and referenced inside `SKILL.md`. When a skill runs, it compares its installed version against the standalone repository's `VERSION.md` to report whether an update is available.

### How to add a new skill

1. Create `skills/<new-skill>/SKILL.md` with valid frontmatter and instructions.
2. Create `skills/<new-skill>/VERSION.md` starting at `v1.0.0`.
3. Create `skills/<new-skill>/README.md` for user-facing documentation.
4. Update `README.md` (this file) and `SKILL_METADATA.md`.
5. Create a new standalone import repository and sync the files there.
6. Add the new repository link to the Repositories table above.
