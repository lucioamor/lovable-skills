# JEVify Diagnostics — /jevify

The basic read-only diagnostic skill of the [JEVify project](https://github.com/lucioamor/jevify). Audits runtime AI calls in a Lovable project, classifies them as generation, structured decisions, deterministic code, retrieval, human review, or unknown, and proposes candidates for JEV in a report returned in chat.

## Import into Lovable

Open **Settings → Skills → Add → Import from GitHub** and paste:

```text
https://github.com/lucioamor/lovable-skill-jevify
```

Run `/jevify` in your project. It inventories the call-sites, proposes Choice/Score/Noul primitives where appropriate, and identifies risks and next steps. It does not modify code or reduce Lovable build credits. Expected effects need validation; savings are not guaranteed.

## Sources and version

- Version: `v1.1.0`.
- Canonical source: [lovable-skills/skills/jevify](https://github.com/lucioamor/lovable-skills/tree/main/skills/jevify).
- Import repository: [lovable-skill-jevify](https://github.com/lucioamor/lovable-skill-jevify).
- Full project, Claude Code variant, and report template: [jevify](https://github.com/lucioamor/jevify).

The skill reports whether its version is current, an update is available, or the version check could not be verified. Re-import the repository to update.

JEVify is the project; `/jevify` is its diagnostic entry point. The project repository contains the skill variants, installation instructions, and report template. Implementation and validation are separate follow-ups; there is no migration skill or executable JEV integration in this release. The diagnostic skill needs no JEV API key.

## Authorship and maintenance

This project was created by [Lucio Amorim](https://linkedin.com/in/lucioamorim), Lovable Ambassador.

When reusing, redistributing, or citing this work, keep the attribution credits and include a link to this repository.

## License

This skill is licensed under [Creative Commons Attribution 4.0 International](https://creativecommons.org/licenses/by/4.0/) (`CC BY 4.0`). Keep attribution, link to the license, and indicate changes when sharing adaptations. The full license is included in the import repository and the canonical skill folder.
