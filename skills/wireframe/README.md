# /wireframe

`/wireframe` reads the active page of your Lovable app and creates a `WIREFRAME-{page}.md` file with that page's real text, layout, buttons, and interactive elements — written in plain language that anyone can read and share. Use `/wireframe all` to map every page into a single file.

It is a community-built Lovable Skill by [Lucio Amorim](https://www.linkedin.com/in/lucioamorim), Lovable Ambassador in Brazil.

All skills: [lucioamor/lovable-skills](https://github.com/lucioamor/lovable-skills)

## Why this exists

At some point, almost every builder needs to show someone else what their app looks like — a teammate, a client, a reviewer, or another AI tool.

Screenshots are hard to search through. Sending raw code is confusing. Describing the app from memory is unreliable.

`/wireframe` creates a plain-text document of what the app actually shows: every page, every button, every piece of text, and every interactive element like filters and dropdowns. That document is easy to read, easy to share, and easy to hand off to any AI tool without uploading screenshots or copying piles of code.

## What it creates

`/wireframe` reads your app and writes a `WIREFRAME.md` file with:

- a list of all pages in the app
- shared elements like the top bar, bottom bar, and pop-up dialogs
- a layout diagram for each page, in the order things appear on screen
- every word of real text: headings, descriptions, button labels, links, error messages, and small captions
- interactive elements like filters, dropdowns, date pickers, and tabs — including what each one does and what it looks like by default
- different states of each page: what shows when you are signed in, signed out, or when there is no data yet

When a page contains a very large table or a long block of text, the file shows an abbreviated version and tells you the best way to review the full data (usually exporting it as a spreadsheet or a data file).

## When to use it

Use `/wireframe` when you need an accurate, complete record of what your app shows right now.

Good situations:

- you want a second opinion on how your app looks or reads
- you need to explain your app to another AI tool without sending screenshots
- you are handing context to a designer, reviewer, or teammate
- you want to document your app before making big changes
- you are preparing to use `/debate` to think through a decision

## How to use it

Map the page you are currently looking at (or the home page if that cannot be determined):

```text
/wireframe
```

Map one specific page:

```text
/wireframe dashboard
```

Map every page in the app into a single file:

```text
/wireframe all
```

If the page you named does not exist, the skill will tell you which pages are available.

## Recommended workflow

1. Run `/wireframe`.
2. The skill reads the page and creates `WIREFRAME-{page-name}.md`.
3. Share that file with another AI tool, a reviewer, or a teammate.
4. Use their feedback to decide what to change.
5. If the decision is not obvious, run `/debate` to think it through.

Example follow-up:

```text
/debate based on WIREFRAME.md, why does the sign-up flow feel confusing?
```

## What it does not do

`/wireframe` does not:

- make up pages or text that are not in the app
- redesign anything
- say whether the design is good or bad
- make any changes to the app
- replace a real design review or user testing

## How to add it to Lovable

Open:

```text
Settings → Skills → Add → Import from GitHub
```

Then paste:

```text
https://github.com/lucioamor/lovable-skill-wireframe
```

For the full collection of skills, visit [lucioamor/lovable-skills](https://github.com/lucioamor/lovable-skills).

## Related skill

[`/debate`](https://github.com/lucioamor/lovable-skill-debate) brings in a panel of opposing specialists to pressure-test a decision before you build it — covering product, design, copy, technical, and data angles.

Use `/wireframe` first to give the debate a clear picture of what the app currently looks like.

## Author

Created and maintained by [Lucio Amorim](https://www.linkedin.com/in/lucioamorim), Lovable Ambassador in Brazil.

This is a community-built skill for builders who want their Lovable workflow to be more structured, easier to share, and easier to review.
