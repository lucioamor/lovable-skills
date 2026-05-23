# /wireframe

`/wireframe` turns a real Lovable app into a compact `WIREFRAME.md` file that another LLM, reviewer, teammate, or agent can understand without rendering the app.

It is a community-built Lovable Skill by [Lucio Amorim](https://www.linkedin.com/in/lucioamorim), Lovable Ambassador in Brazil.

Central catalog: [`lucioamor/lovable-skills`](https://github.com/lucioamor/lovable-skills)  
Standalone import repo: [`lucioamor/lovable-skill-wireframe`](https://github.com/lucioamor/lovable-skill-wireframe)

## Why this exists

Most builders eventually need to move app context outside the original Lovable project.

Screenshots are heavy and shallow. Raw HTML is noisy. Copying code into another model often gives too much implementation detail and too little product structure.

`/wireframe` creates the missing abstraction layer: a plain-text map of what the app actually renders.

That makes it easier to ask another model for UX critique, copy review, layout feedback, onboarding diagnosis, or product direction without wasting tokens on screenshots, markup, or vague explanations.

## What it generates

`/wireframe` reads the current Lovable codebase and writes a `WIREFRAME.md` file with:

- route map
- global chrome such as header, footer, navigation, dialogs, and modals
- page-by-page ASCII layout
- visible copy from JSX, locale files, or constants
- buttons, links, CTAs, forms, labels, and microcopy
- auth, role, loading, empty, and error states when visible in code
- component names and file paths
- visible Supabase schema summary when present

The output is designed for LLM handoff. It is not a screenshot, not raw HTML, and not a design mockup. It is dense markdown that travels well across ChatGPT, Claude, Gemini, Grok, agents, reviewers, and async critique workflows.

## When to use it

Use `/wireframe` when you need a faithful textual snapshot of the app that exists now.

Good use cases:

- getting a second opinion on UX or copy
- sending app context to another LLM without screenshots
- giving an agent layout and route context before a redesign
- documenting which routes and screens actually exist
- reducing token cost when moving app context between tools
- preparing structured context for `/debate`
- creating a reviewable artifact before a product or design pass

## Commands

Generate a full-app wireframe:

```text
/wireframe
```

Generate or update one route only:

```text
/wireframe /dashboard
```

The route-specific command updates only the matching route section when possible.

## Recommended workflow

1. Run `/wireframe`.
2. Lovable reads the router, page components, imported child components, global chrome, and visible schema.
3. The skill writes `WIREFRAME.md`.
4. Send that file to another LLM, reviewer, or agent.
5. Use the critique to decide what should change.
6. If the decision is non-obvious, run `/debate` against the wireframe.

Example follow-up:

```text
/debate based on WIREFRAME.md, why does the onboarding flow feel unclear?
```

## What it does not do

`/wireframe` does not:

- invent screens that are not in the router
- write placeholder copy
- redesign the UI
- judge whether the UI is good
- implement changes
- replace product specs, analytics, or human design review

If a value is dynamic, the skill marks the source instead of guessing the final rendered value.

## How it behaves

The skill first locates the app router, then follows each route into its page component and imported child components. It extracts real user-facing strings and records the top-to-bottom render order.

If `WIREFRAME.md` already exists, it asks whether to overwrite it or save a timestamped version. In single-route mode, overwrite updates only that route section when possible.

Every run includes the installed skill version and checks whether the standalone source repo appears current.

## Import into Lovable

Open:

```text
Settings -> Skills -> Add -> Import from GitHub
```

Then paste:

```text
https://github.com/lucioamor/lovable-skill-wireframe
```

Lovable imports one skill at a time. For the full catalog, see [`lovable-skills`](https://github.com/lucioamor/lovable-skills).

## Related skill

[`/debate`](https://github.com/lucioamor/lovable-skill-debate) runs a structured panel of opposing experts for product, UX, copy, architecture, performance, data, and security decisions.

Use `/wireframe` first when the debate needs a grounded map of routes, copy, layout, and component structure.

## Author

Created and maintained by [Lucio Amorim](https://www.linkedin.com/in/lucioamorim), Lovable Ambassador in Brazil.

This is a community-built skill intended to make Lovable workflows more structured, portable, and reviewable.
