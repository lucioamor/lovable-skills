# jevify — /jevify and /jevify migrate

The Lovable skill of the [jevify project](https://github.com/lucioamor/jevify). `/jevify` audits runtime AI calls in a Lovable project, classifies them as generation, structured decisions, deterministic code, retrieval, human review, or unknown, and proposes candidates for JEV in a report returned in chat. `/jevify migrate <finding>` moves one approved candidate to JEV, starting in shadow mode.

## Import into Lovable

Open **Settings → Skills → Add → Import from GitHub** and paste:

```text
https://github.com/lucioamor/lovable-skill-jevify
```

Run `/jevify` in your project. It inventories the call-sites, proposes Choice/Score/Noul primitives where appropriate, and identifies risks and next steps. It does not modify code or reduce Lovable build credits. Expected effects need validation; savings are not guaranteed.

Then run `/jevify migrate <finding>` on one candidate. It explains the plan, changes code only after you approve it, adds the JEV decision next to the existing AI call behind an `off | shadow | on` flag that starts in `shadow`, and never removes the existing path. The API key goes into a Lovable Cloud secret, never the frontend.

## Optional: jevify MCP connector

Open **Connectors**, add a custom MCP server with the URL `https://jevify.lovable.app/mcp`, and sign in. With it, the skill runs in MCP mode: the jevify service classifies call-sites and keeps reports private under your account. The skill asks before sending files and never sends `.env` files or credentials. Without it, the skill runs locally and nothing is sent to the service.

## Sources and version

- Version: `v1.2.0`.
- Canonical source: [lovable-skills/skills/jevify](https://github.com/lucioamor/lovable-skills/tree/main/skills/jevify).
- Import repository: [lovable-skill-jevify](https://github.com/lucioamor/lovable-skill-jevify).
- Full project, Claude Code variant, and report template: [jevify](https://github.com/lucioamor/jevify).

The skill reports whether its version is current, an update is available, or the version check could not be verified. Re-import the repository to update.

jevify is the project; `/jevify` is its diagnostic entry point and `/jevify migrate` its migration step. The project repository contains the skill variants, installation instructions, and report template. The audit needs no JEV API key; a migration needs one, kept server-side.

## Authorship and maintenance

This project was created by [Lucio Amorim](https://linkedin.com/in/lucioamorim), Lovable Ambassador.

When reusing, redistributing, or citing this work, keep the attribution credits and include a link to this repository.

## License

This skill is licensed under [Creative Commons Attribution 4.0 International](https://creativecommons.org/licenses/by/4.0/) (`CC BY 4.0`). Keep attribution, link to the license, and indicate changes when sharing adaptations. The full license is included in the import repository and the canonical skill folder.

## Documentation convention

Always write **jevify** in lowercase. Keep public repository documentation and GitHub descriptions in English.
