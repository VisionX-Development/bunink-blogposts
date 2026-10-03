---
title: Metadata and Notes – What's Inside a Markdown File Besides the Text
date: 2026-09-30
description: Frontmatter for title and status at the top of the file, notes as reminders attached to a specific spot in the text. How both work in bun.ink, where they're stored and who can see them.
sourceHash: 8295120e8bc7b21aceef89d73a67dac8bf453a149996f73242330e97562c4146
---

A Markdown file is text. But it's more than that: often it also needs to say what it's called, what stage it's at, or what's still missing in a particular spot. [bun.ink](http://bun.ink) has two tools for this, and both live inside the file itself — **metadata** and **notes**.

## In short: the difference

**Metadata** (frontmatter)

- sits right at the top of the file, exactly one block
- says something about the whole document: title, status, date
- is meant for programs: website, table of contents, AI agent, and so on
- appears on GitHub as a table above the text
- insert it with **Format → Document → Insert metadata**

**Notes**

- can sit anywhere in the text, as many as you like
- say something about one particular passage
- are meant for you, while you write
- are invisible on GitHub; they only appear in the file's raw data
- insert them with **Format → Document → Insert note** or a keyboard shortcut of your choosing

## Metadata: the block at the beginning

Frontmatter is a block between two lines of three hyphens, right at the start of the file:

```markdown
---
title: Das zweite Kapitel
status: draft
---
```

Website generators such as Hugo, Jekyll or Astro read the title and date from it; our own [handbook](https://github.com/VisionX-Development/writing-with-bunink) reads its chapter number and status. Which fields you need is determined by whichever program processes the file further.

In [bun.ink](http://bun.ink), the block is a box of its own, labelled **Metadata**. It always ends up at the start of the file, no matter where the cursor is, and there's never more than one — programs only read the first one anyway. An **×** removes it again. And because three hyphens typed in the middle of the text make a horizontal rule, you always create metadata through the menu.

The most important part happens invisibly: [bun.ink](http://bun.ink) writes the block back character for character. Open a file from an existing repository, and after saving you'll find exactly the same frontmatter — no shifted blank lines, no inserted backslashes.

## Notes: the sticky note on the passage

"Add source." "Dialogue feels wooden." "Cross-check with chapter 4." Comments like these belong in a particular spot, but not in the text itself. That's exactly what notes are for.

Put the cursor in a paragraph and choose **Format → Document → Insert note**, or press **Ctrl+N — or set your own keyboard shortcut for it**. The note appears as a coloured card directly after the paragraph — never in the middle of it — and you start writing. The shortcut can be changed or switched off in the settings under **Editor**. On Windows and Linux you should do exactly that: there, the browser claims Ctrl+N for a new window.

In the file, the note appears as an HTML comment with an identifier:

```markdown
Anna stand am Fenster und zählte die Züge.

<!-- bun.ink:note
Wie viele Züge fahren nachts wirklich? Fahrplan prüfen.
-->
```

### This format has three advantages:

- **It's invisible everywhere** the file is displayed: in the GitHub preview, on a website, in other Markdown programs.
- **It travels with the text.** The note is saved with the document, ends up in the same commit, and stays where it is as you write around it. No second storage location that could go missing.
- **It doesn't count as text.** Word counts and writing statistics skip notes; search still finds them — handy for tracking down all the outstanding "add source" reminders in a project.

## A word of warning: invisible doesn't mean secret

A note is hidden in the rendered view, but readable in the file. Anyone looking at the raw file, a commit or a diff will see it too. In a public repository, your notes are public, and an editor working in the same repository reads along. Anything nobody is allowed to see doesn't belong in a note. For comments that really are meant for someone else, there's the [review via pull request](/blog/reviews-as-pull-requests): there, comments live on GitHub attached to the pull request, not in the text. Notes are your own private sticky notes.

## By the way: other people's comments stay put

Many files in docs repositories already come with HTML comments — hidden TODOs, instructions for linting tools. [bun.ink](http://bun.ink) shows them greyed out in the editor and writes them back unchanged. That may sound obvious, but other writing editors simply lose such comments when saving.

How it all works in detail is explained in the handbook chapter [Metadata and Notes](https://github.com/VisionX-Development/writing-with-bunink/blob/main/en/11-metadata-and-notes.md).
