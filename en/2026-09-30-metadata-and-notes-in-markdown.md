---
title: Metadata and Notes — What's in a Markdown File Besides the Text
date: 2026-09-30
description: Front matter for title and status at the top of the file, notes as reminders attached to a specific spot in the text. How both work in bun.ink, where they're stored, and who sees them.
sourceHash: d0599bef334ebda6caebeb4b8150b7cb4fc79a5ef87ef416d465ad66effd772a
---

A Markdown file is text. But not only that: often it also needs to say what it's called, what stage it's at, or what's still missing in a particular spot. [bun.ink](http://bun.ink) has two tools for this, and both live inside the file itself – **metadata** and **notes**.

## In short: the difference

**Metadata** (frontmatter)

- sits at the very top of the file, exactly one block
- says something about the whole document: title, status, date
- is meant for programs: website, table of contents, AI agent, and so on
- appears on GitHub as a table above the text
- insert it with **Format → Document → Insert Metadata**

**Notes**

- sit anywhere in the text, as many as you like
- say something about a specific passage
- are meant for you, while you write
- are invisible on GitHub, they only appear in the file's raw data
- insert them with **Format → Document → Insert Note** or a keyboard shortcut of your choosing

## Metadata: the block at the beginning

Frontmatter is a block between two lines of three hyphens, right at the start of the file:

```markdown
---
title: Das zweite Kapitel
status: draft
---
```

Website generators like Hugo, Jekyll or Astro read the title and date from it; our own [handbook](https://github.com/VisionX-Development/writing-with-bunink) reads its chapter number and status. Which fields you need depends on the program that processes the file.

In [bun.ink](http://bun.ink), the block is a box of its own labelled **Metadata**. It always ends up at the top of the file, no matter where the cursor is, and there is never more than one – programs only read the first one anyway. An **×** removes it again. And because three hyphens typed by hand in the middle of the text make a horizontal rule, you always create metadata through the menu.

The most important part happens invisibly: [bun.ink](http://bun.ink) writes the block back character for character. If you open a file from an existing repository, you'll find exactly the same frontmatter after saving – no shifted blank lines, no inserted backslashes.

## Notes: the sticky note on the passage

"Add the source." "The dialogue feels wooden." "Cross-check with chapter 4." Comments like these belong in a specific place, but not in the text. That's exactly what notes are for.

Put the cursor in a paragraph and choose **Format → Document → Insert Note**, or press **Ctrl+N, or set your own keyboard shortcut for it**. The note appears as a coloured card directly after the paragraph – never in the middle of it – and you can start writing. The shortcut can be changed or switched off in the settings under **Editor**. On Windows and Linux you should do that: there, the browser keeps Ctrl+N for opening a new window.

In the file, the note appears as an HTML comment with an identifier:

```markdown
Anna stand am Fenster und zählte die Züge.

<!-- bun.ink:note
Wie viele Züge fahren nachts wirklich? Fahrplan prüfen.
-->
```

### This form has three advantages:

- **It's invisible everywhere** the file is displayed: in the GitHub preview, on a website, in other Markdown programs.
- **It travels with the text.** The note is saved with the document, ends up in the same commit and stays where it is while you write around it. No second storage location that could get lost.
- **It doesn't count as text.** Word counts and writing statistics leave notes out; the search still finds them – handy for tracking down every outstanding "add the source" in a project.

## A word of warning: invisible doesn't mean secret

A note is hidden in the rendered view, but readable in the file. Anyone looking at the raw file, a commit or a diff will see it too. In a public repository your notes are public, and an editor working in the same repository reads along. Anything nobody is allowed to see does not belong in a note. For comments that are genuinely meant for someone else, there's [review via pull requests](/blog/reviews-as-pull-requests): there, comments live on GitHub at the pull request, not in the text. Notes are your own sticky notes.

## By the way: other people's comments stay put

Many files in docs repositories already come with HTML comments – hidden TODOs, instructions for linting tools. [bun.ink](http://bun.ink) shows them in grey in the editor and writes them back unchanged. That may sound obvious, but other writing editors simply lose such comments when saving.

How it all works in detail is described in the handbook chapter [Metadata and Notes](https://github.com/VisionX-Development/writing-with-bunink/blob/main/en/11-metadata-and-notes.md).
