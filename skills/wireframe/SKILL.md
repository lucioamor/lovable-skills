---
name: wireframe
description: Run /wireframe to read the real codebase and write WIREFRAME.md from routes, components, UI copy, layout, auth states, and visible Supabase schema. Add a route after the command to cover one page only; never invent screens or copy.
---

# /wireframe - Codebase to Wireframe

## Skill identity

- Version: `v1.0.0`
- Source repo: `https://github.com/lucioamor/lovable-skill-wireframe`
- Central catalog: `https://github.com/lucioamor/lovable-skills`
- Related skill: `/debate` (`https://github.com/lucioamor/lovable-skill-debate`) pressure-tests product, UX, copy, architecture, performance, data, or security decisions. Use `/wireframe` first when `/debate` needs a grounded map of the current app.
- Latest check: before the final user-facing response, compare this version with the current `VERSION.md` in the source repo when that source is reachable.

After every `/wireframe` run, include one compact line in the user-facing result with the version status:

> Skill: `/wireframe` `v1.0.0` · Version status: `{current | update available | unverified}` · Source: `https://github.com/lucioamor/lovable-skill-wireframe`

Use `current` only when the source repo version matches this installed version. Use `update available` when the source repo version differs. Use `unverified` when the source repo version cannot be checked.

When the user types `/wireframe` or `/wireframe /some-route`, generate a markdown wireframe by reading the real codebase. Do not invent copy, do not use lorem ipsum, do not use placeholders.

## Command variants

- `/wireframe` -> generate wireframe for **ALL** routes registered in the app router (e.g. `src/App.tsx`).
- `/wireframe /route` -> generate wireframe **only** for the matching route (e.g. `/wireframe /dashboard` -> only `/dashboard`).

If the requested route does not exist in the router, stop and tell the user which routes are available.

## Workflow

1. **Locate the router** (typically `src/App.tsx` or wherever `<Routes>` lives). Build the route map.
2. **Read each page component** referenced by the route, then follow imports into its section/child components. Read enough to extract:
   - Exact headings, subheadings, body text, button labels, link labels, microcopy.
   - Section order as rendered top-to-bottom (mirror JSX order).
   - Conditional rendering (auth gates, role gates, loading/empty/error states).
   - File path of each named component for reference.
3. **Read global chrome once** (Header, Footer, global Nav, global Modals/Dialogs). Document them in their own section, not per page.
4. **If a Supabase schema is present** (e.g. `src/integrations/supabase/types.ts` or `supabase/migrations/*`), include a compact data model summary: table name, key columns, RLS posture if visible.
5. **Compose the markdown** following the Output Format below.
6. **Write the file** following the File Output Logic below.

## File Output Logic

- Target path: `WIREFRAME.md` at project root.
- If `WIREFRAME.md` does **not** exist -> create it.
- If `WIREFRAME.md` **does** exist -> ask the user, verbatim:
  > WIREFRAME.md ja existe. Deseja fazer **overwrite** ou salvar como nova versao (**WIREFRAME-YYYY-MM-DD_HH-MM.md**)?
  Then act on their answer:
  - "overwrite" -> overwrite `WIREFRAME.md`.
  - "nova versao" / "new version" -> write to `WIREFRAME-YYYY-MM-DD_HH-MM.md` using the current local date/time (24h).
- For single-route mode (`/wireframe /route`) on an existing `WIREFRAME.md`, still ask. If user picks overwrite, replace only that route's section and preserve the rest; if new version, write a fresh file containing just that route plus global chrome.

## Output Format

````markdown
# {Project Name} - Wireframe

> Generated from codebase on {YYYY-MM-DD}. Reflects current code.

## 0. Route Map

| Route | Page Component | Auth | Notes |
|-------|----------------|------|-------|
| `/`   | `Index` (`src/pages/Index.tsx`) | Public | ... |

## 1. Global Chrome

### Header - `<Header>` (`src/components/Header.tsx`)
ASCII box + exact links/labels.

### Footer - `<Footer>` (`...`)
ASCII box + exact copy.

### Global Modals (e.g. ContactDialog, AuthModal)
Trigger sources + exact field labels + submit destination.

## 2. Pages

### 2.1 `/` - Index
ASCII layout box mirroring top-to-bottom section order:

```
+----------------------------------+
| HERO                             |
|   H1: "<exact copy>"             |
|   Sub: "<exact copy>"            |
|   [Button: <exact label>]        |
+----------------------------------+
| SECTION 2 ...                    |
+----------------------------------+
```

For each section list:
- Component name + file path
- Exact heading / body / button copy
- Conditional/auth states ("Signed-out: ..., Signed-in: ...")

(repeat per route)

## 3. Data Model (if Supabase present)

| Table | Key Columns | RLS |
|-------|-------------|-----|
| ...   | ...         | ... |

## 4. Cross-Cutting Rules

- i18n, auth, roles, animation, routing patterns observed in code.
````

## Format Rules (must follow)

- **Real copy only.** Pull strings directly from JSX, i18n locale files, or constants. Never paraphrase user-facing text.
- **ASCII boxes reflect true visual order** (top-to-bottom as rendered, not import order).
- **Dense but scannable.** Tables for route maps and data models; ASCII boxes + bullet lists for sections.
- **Name every component** with its file path so a future LLM can jump straight to the source.
- **No placeholders, no "TBD", no lorem ipsum.** If a string is dynamic, mark it `{dynamic: <source>}`.
- **i18n projects:** prefer the EN locale unless the project is single-language PT-BR; note the other language exists.
- **Skip dev-only routes** (Storybook, test harnesses) unless the user asked for them.

## After Writing

Tell the user: file path written, route count covered, and (if applicable) which sections were skipped and why.
