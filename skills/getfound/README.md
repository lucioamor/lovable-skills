# /getfound

`/getfound` makes a Lovable site easier for search engines and AI systems to find, understand and cite — working only on what Lovable's native SEO & AI search review does not already cover.

It is a community-built Lovable Skill by [Lucio Amorim](https://www.linkedin.com/in/lucioamorim), Lovable Ambassador in Brazil.

Central catalog: [`lucioamor/lovable-skills`](https://github.com/lucioamor/lovable-skills)  
Standalone import repo: [`lucioamor/lovable-skill-getfound`](https://github.com/lucioamor/lovable-skill-getfound)

## Import into Lovable

**Settings → Skills → Add → Import from GitHub**, then paste:

```text
https://github.com/lucioamor/lovable-skill-getfound
```

Re-import to update.

## Why this exists

Lovable's native review already handles traditional technical SEO: titles, descriptions, canonicals, Open Graph, headings, robots.txt, sitemap, viewport, basic JSON-LD, pre-rendering and automatic Markdown for AI crawlers. Running another generic SEO audit on top of that only repeats it.

`/getfound` covers the gap:

- **Entity identity** — a canonical entity home, stable `@id`, correct `sameAs`, `knowsAbout`, `worksFor`, `alumniOf` and external-node consistency.
- **Claim evidence** — a ledger of the claims that matter, with sources and dates; unsupported superlatives rewritten as verifiable facts.
- **Access by consumer** — what verified crawlers, unverified agents and `Accept: text/markdown` requests actually receive; host canonicalization; an intentional AI-crawler policy by purpose (search vs training vs user-initiated).
- **Markdown fidelity** — duplicated marquees, carousels and mobile/desktop copies that pollute extraction.
- **Bilingual parity** — crawlable URLs per language, hreflang, and the same facts in EN and PT-BR.
- **Agent files** — integrity of `llms.txt`, `llms-full.txt`, Markdown twins and `.well-known/agent-skills/` when they exist or are justified.
- **Real outcomes** — a reproducible protocol to check what ChatGPT, Perplexity, Claude, Gemini/AI Mode and Copilot say and cite.

## Commands

```text
/getfound
```

Audits the current project and applies, in the same run, the fixes that are local, reversible, complementary to the native review and backed by evidence. Everything else comes back as a prioritized backlog.

```text
/getfound https://your-domain.example
```

Scopes the run to a published site.

```text
/getfound audit
```

Report only. Never edits the app.

```text
/getfound compare
```

Repeats equivalent observations against an earlier baseline.

## What it does not do

- Publish, change domain/DNS/WAF settings, submit to indexers or edit external profiles — these come back as off-site tasks with exact steps.
- Invent facts, credentials, dates or endorsements to fill schema or copy.
- Re-audit what the native review already checks and passes.
- Promise rankings, citations or traffic, or produce a numeric "GEO score".
- Simulate AI engine results. When engines cannot be queried from inside Lovable, it hands you a ready-to-run measurement protocol.

## Recommended workflow

1. Run Lovable's **SEO & AI search review** and fix native findings with **Try to fix**.
2. Run `/getfound`.
3. Answer any fact questions it raises, then publish.
4. Re-run the native review and the acceptance tests from the report.
5. After recrawl, run the measurement protocol and `/getfound compare`.

## Package

- [SKILL.md](./SKILL.md) — complete instructions used by Lovable.
- [VERSION.md](./VERSION.md) — version and release status.
- License: [CC BY 4.0](https://github.com/lucioamor/lovable-skills/blob/main/LICENSE).

The canonical source lives in the central catalog at `skills/getfound/`; the standalone repo is synced from it. Edit the catalog, not the standalone repo.

## Authorship and maintenance

This project was created by [Lucio Amorim](https://linkedin.com/in/lucioamorim), Lovable Ambassador.

When reusing, redistributing, or citing this work, keep the attribution credits and include a link to [this repository](https://github.com/lucioamor/lovable-skills).
