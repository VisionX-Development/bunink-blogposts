# Document structure

The anatomy of a single blog post file.

## File name

```
de/2026-06-18-git-and-github-for-writers.md
   │          │
   │          └─ slug: English, kebab-case — becomes the URL: bun.ink/blog/git-and-github-for-writers
   └──────────── publication date, YYYY-MM-DD
```

The slug is **English even though the post is German**: English is the primary, indexed market and the URL is shared by both languages. Lowercase letters, digits and hyphens only. The English file in `en/` has the **same name** — the name is what pairs the two languages, so it never changes once a post is published. A file that does not follow this pattern is reported by the sync and neither translated nor published.

## Front matter

Every file in `de/` starts with a front-matter block. The sync reads it, so a malformed block means the post is skipped.

```markdown
---
title: Git und GitHub für Autoren – eine Einführung
date: 2026-06-18
description: Was Commits, Branches und Repositories für Schreibende bedeuten.
---
```

| Field | Required | Purpose |
|---|---|---|
| `title` | yes | heading, index entry, `<title>` |
| `date` | yes (`YYYY-MM-DD`) | sorting (newest first) and display |
| `description` | recommended | teaser in the index and meta description |

Generated files in `en/` additionally carry `sourceHash`, a hash of the German file. It tells the sync whether the translation is still current. Do not edit it.

Keep the syntax flat — one `key: value` per line. Wrap a value in quotes when it contains `:` or starts with `#`. The parser is deliberately minimal; nested structures will not be read.

## Body

Plain Markdown, starting straight with the prose — the title comes from the front matter, so do not repeat it as a heading. `##` for sections a reader would scan for, `###` sparingly. Links to other posts are site-relative: `[kontrollierter Schreibpartner](/blog/ai-controlled-writing-partner)`.

### Conventions

- Addressed as "du"; the reader writes for a living and is not necessarily a developer.
- **UI labels in bold**: click **Speichern**. Use the German UI wording; the translation handles the English label.
- Paths, file names, commands and branch names in backticks.
- Explain a Git term the first time it appears in the post, then use it plainly.
- No release notes, no roadmap promises. A post describes what the app does today.

## Translation

The German file is translated verbatim in structure: headings, lists, emphasis and inline code are preserved; content inside code, URLs and paths is left untouched. A formatting mistake in the source is faithfully reproduced — proofread the German before it lands on `main`. Changing a German post after publication is fine: the sync notices the changed hash and re-translates. Editing `en/` by hand is not: the next sync of that post overwrites it.
