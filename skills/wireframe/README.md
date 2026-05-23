# /wireframe

`/wireframe` reads a Lovable app's real codebase and writes a dense `WIREFRAME.md` file that another model, reviewer, or agent can understand without rendering the app.

It is part of the central [`lovable-skills`](https://github.com/lucioamor/lovable-skills) catalog. The importable standalone repository is [`lovable-skill-wireframe`](https://github.com/lucioamor/lovable-skill-wireframe).

## What it does

`/wireframe` turns the app that already exists into plain-text product context:

- route map
- global chrome such as header, footer, navigation, dialogs, and modals
- page-by-page ASCII layout
- exact visible copy from JSX, locale files, or constants
- buttons, links, CTAs, forms, and microcopy
- auth, role, loading, empty, and error states when visible in code
- component names and file paths
- visible Supabase schema summary when present

The output is designed for LLM handoff. It is not a screenshot, not raw HTML, and not a design mockup. It is compact markdown that can be pasted into another model or reviewed asynchronously.

## When to use it

Use `/wireframe` when you want a faithful textual snapshot of the current app:

- getting a second opinion on UX or copy
- asking another LLM to critique a page without sending screenshots
- giving an agent context before a redesign
- documenting what routes and screens actually exist
- reducing tokens when moving app context between tools
- preparing context for `/debate`

Example:

```text
/wireframe
```

Generates `WIREFRAME.md` for all routes registered in the app router.

Example:

```text
/wireframe /dashboard
```

Generates or updates the wireframe for only `/dashboard`, if that route exists.

## Example flow

1. Run `/wireframe`.
2. Lovable reads the router, pages, imported components, global chrome, and visible schema.
3. The skill writes `WIREFRAME.md`.
4. You send that file to another LLM, teammate, or reviewer.
5. You use the critique to decide what to change.

A common follow-up is:

```text
/debate based on WIREFRAME.md, why does the onboarding flow feel unclear?
```

## What it does not do

`/wireframe` does not:

- invent screens that are not in the router
- write placeholder copy
- design a new UI
- judge whether the current UI is good
- implement changes
- replace product specs or human design review

If something is dynamic, it marks the source instead of guessing the final value.

## How it behaves

The skill first locates the app router, then follows each route into its page component and imported child components. It extracts real user-facing strings and records the top-to-bottom render order.

If `WIREFRAME.md` already exists, it asks whether to overwrite it or save a timestamped version. In single-route mode, overwrite updates only that route section when possible.

Every run includes the installed skill version and checks whether the standalone source repo appears current.

## Related skills

- [`/debate`](../debate/README.md) runs a structured panel of opposing experts for product, UX, copy, architecture, performance, data, or security decisions.

Use `/wireframe` first when the debate needs a grounded map of the current app.
