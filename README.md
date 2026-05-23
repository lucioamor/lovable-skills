# Lovable Skills

Reusable Lovable Skills by [Lucio Amorim](https://www.linkedin.com/in/lucioamorim), Lovable Ambassador in Brazil.

This repository is the central catalog and working source for skills I use to make Lovable projects easier to inspect, critique, and improve across LLMs, agents, reviewers, and product workflows.

For the easiest Lovable import, use the standalone GitHub repository for the specific skill you want. Each standalone repository exposes a single `SKILL.md` at its root.

## Why this repo exists

Lovable Skills turn repeated prompts into reusable canonical instructions.

Project Knowledge is for facts a project should remember. Skills are for processes a project should run in a consistent way.

That distinction matters. As Lovable projects become more complex, the bottleneck is often not whether the app can be built. The bottleneck is whether builders can create a repeatable workflow for review, critique, context transfer, and decision-making.

This repo packages two of those workflows:

- `/wireframe` compresses the real app surface into portable product context.
- `/debate` pressure-tests important product, UX, copy, and technical decisions before implementation.

Together, they create a simple loop:

```text
extract the app -> critique the decision -> implement with clearer judgment
```

## Available skills

| Skill | What it does | Import |
| --- | --- | --- |
| `/wireframe` | Reads the current Lovable codebase and writes a dense `WIREFRAME.md` from real routes, components, copy, CTAs, layouts, states, and visible Supabase schema. | [`lovable-skill-wireframe`](https://github.com/lucioamor/lovable-skill-wireframe) |
| `/debate` | Runs a structured expert panel with opposing viewpoints for product, UI, UX, copy, architecture, performance, data, security, and GTM decisions. | [`lovable-skill-debate`](https://github.com/lucioamor/lovable-skill-debate) |

## Recommended workflow

Use `/wireframe` when you need a grounded map of what the app currently is.

Then use `/debate` when the next decision is not obvious, or when the obvious decision may be hiding a blind spot.

Example:

```text
/wireframe
```

Then:

```text
/debate based on WIREFRAME.md, why does the onboarding flow feel unclear?
```

This is especially useful when moving between Lovable and external LLMs such as ChatGPT, Claude, Gemini, or Grok, or when handing context to an async reviewer, agent, teammate, or client.

## Import into Lovable

Open:

```text
Settings -> Skills -> Add -> Import from GitHub
```

Paste the standalone repository URL for the skill you want:

```text
https://github.com/lucioamor/lovable-skill-wireframe
https://github.com/lucioamor/lovable-skill-debate
```

Lovable imports one skill at a time.

Do not paste this catalog repository URL into the importer. Use the standalone repositories above.

## Skill details

### `/wireframe`

`/wireframe` generates a `WIREFRAME.md` file from the current app.

Use it for all routes:

```text
/wireframe
```

Use it for one route:

```text
/wireframe /dashboard
```

It reads real routes, page components, imported components, visible UI copy, auth states, loading states, empty states, error states, and visible Supabase schema. It then compresses the app into plain markdown that can be shared across LLMs and review workflows.

It does not design new screens, invent missing copy, judge the UI, or infer pages that are not present in the router.

Full instructions: [`skills/wireframe/SKILL.md`](./skills/wireframe/SKILL.md)  
Skill README: [`skills/wireframe/README.md`](./skills/wireframe/README.md)  
Example output: [`examples/WIREFRAME-nxlv.md`](./examples/WIREFRAME-nxlv.md)

### `/debate`

`/debate` pressure-tests a decision before implementation.

Use it when you are stuck and do not know what to ask. Also use it when you are already confident and want the blind spots surfaced before committing.

The skill changes posture by domain:

- convergent for architecture, security, data, integrations, and performance
- divergent for UI, copy, branding, and positioning
- mixed for UX, where vision may diverge but clarity and user-protection constraints still matter

It does not implement the decision. It ends at analysis, trade-offs, decision matrix, the read, and sometimes a saved trace.

Full instructions: [`skills/debate/SKILL.md`](./skills/debate/SKILL.md)  
Skill README: [`skills/debate/README.md`](./skills/debate/README.md)

## Repositories

| Repository | Purpose |
| --- | --- |
| [`lucioamor/lovable-skill-wireframe`](https://github.com/lucioamor/lovable-skill-wireframe) | Importable `/wireframe` skill with `SKILL.md` at the repository root. |
| [`lucioamor/lovable-skill-debate`](https://github.com/lucioamor/lovable-skill-debate) | Importable `/debate` skill with `SKILL.md` at the repository root. |
| [`lucioamor/lovable-skills`](https://github.com/lucioamor/lovable-skills) | Central catalog and working source for all skills. |

## Versioning

Each skill identifies its source repository and version inside its own instructions.

When a skill runs, its response includes the installed version, tries to compare it with the standalone repo version, and labels the status as:

- current
- update available
- unverified

Current published versions:

| Skill | Version | Latest source |
| --- | --- | --- |
| `/wireframe` | `v1.0.0` | [`lovable-skill-wireframe/VERSION.md`](https://github.com/lucioamor/lovable-skill-wireframe/blob/main/VERSION.md) |
| `/debate` | `v1.0.0` | [`lovable-skill-debate/VERSION.md`](https://github.com/lucioamor/lovable-skill-debate/blob/main/VERSION.md) |

If a running skill shows an older version than its standalone repo, import that standalone repo again in Lovable to update it.

## Catalog shape

```text
skills/
|-- debate/
|   |-- README.md
|   `-- SKILL.md
`-- wireframe/
    |-- README.md
    `-- SKILL.md
```

The folders above keep the central source organized. The standalone repositories are the recommended import path because each one exposes a single root `SKILL.md`.

## About the author

Created and maintained by [Lucio Amorim](https://www.linkedin.com/in/lucioamorim), Lovable Ambassador in Brazil.

I share these skills as practical infrastructure for builders who use Lovable seriously: not just to generate apps, but to review them, move context across tools, pressure-test decisions, and make better product calls faster.

## License

[MIT](./LICENSE)
