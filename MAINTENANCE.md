# Maintenance

This repo is the source catalog for the Lovable skills. Standalone import repos are generated or synced from this repo; they are not the place to author skill behavior.

## Source of truth

The main file for each skill is:

```text
skills/<skill>/SKILL.md
```

Examples:

```text
skills/wireframe/SKILL.md
skills/debate/SKILL.md
```

Edit those files first. Treat any root `SKILL.md` in a standalone import repo as exported output.

## Update flow

1. Edit `skills/<skill>/SKILL.md`.
2. If behavior, output shape, metadata, or compatibility changed, bump `skills/<skill>/VERSION.md`.
3. If public usage changed, update `skills/<skill>/README.md`.
4. If the root catalog changed, update `README.md`.
5. Run the export workflow once it exists.
6. Sync the generated standalone output to the matching import repo.

The standalone import repos should receive only import-ready skill files, such as:

```text
SKILL.md
VERSION.md
README.md
LICENSE
```

## What not to export

Do not export maintainer-only files to standalone skill import repos:

```text
MAINTENANCE.md
SKILL_METADATA.md
scripts/
exports/
examples/
*.rewritten.md
```

Those files can live in this central catalog repo, including on GitHub. They should not be copied into the standalone import repos because Lovable users importing a single skill do not need catalog maintenance instructions.

## Export contract

An export workflow should:

- read from `skills/*`
- write import-ready standalone folders
- preserve each skill's root `SKILL.md`
- include `VERSION.md`
- include the skill README when useful for the standalone repo
- exclude maintainer-only catalog files
- fail if `SKILL.md` and `VERSION.md` disagree on the version
- fail if frontmatter is missing `name` or `description`
- fail if the description violates the contract in `SKILL_METADATA.md`

The export output is a sync artifact. If a generated file needs a manual edit, make that edit in `skills/<skill>/...` and export again.
