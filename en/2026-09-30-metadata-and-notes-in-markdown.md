---
title: Metadata and Notes – What's Inside a Markdown File Besides the Text
date: 2026-09-30
description: Front matter for title and status at the top of the file, notes as reminders attached to a specific spot in the text. How both work in bun.ink, where they're stored and who sees them.
sourceHash: 8295120e8bc7b21aceef89d73a67dac8bf453a149996f73242330e97562c4146
---

A Markdown file is text. But not only that: often it also needs to say what it's called, what stage it's at, or what's still missing in a particular spot. [bun.ink](http://bun.ink) has two tools for this, and both live inside the file itself — **Metadata** and **notes**.

## In short: the difference

**Metadata** (frontmatter)

- sits at the very top of the file, exactly one block
- says something about the whole document: title, status, date
- is meant for programs: website, table of contents, AI agent, and so on
- appears on GitHub as a table above the text
- insert it with **Format → Document → Insert Metadata**

**Notes**

- sit anywhere in the text, as many as you like
- say something about one particular passage
- are meant for you, while you write
- are invisible on GitHub, appearing only in the file's raw data
- insert one with **Format → Document → Insert Note** or a keyboard shortcut of your choosing

## Metadata: the block at the start

Frontmatter is a block between two lines of three hyphens, right at the beginning of the file:

```markdown
---
title: Das zweite Kapitel
status: draft
---
```

Website generators like Hugo, Jekyll or Astro read the title and date from it; our own [handbook](https://github.com/VisionX-Development/writing-with-bunink) reads its chapter number and status. Which fields you need is decided by the program that processes the file further.

In [bun.ink](http://bun.ink), the block appears as its own box labelled **Metadata**. It always ends up at the start of the file, no matter where your cursor is, and there's never more than one — programs only read the first one anyway. An **×** removes it again. And because three hyphens typed by hand in the middle of the text make a horizontal rule, you always create metadata through the menu.

The most important part happens invisibly: [bun.ink](http://bun.ink) writes the block back character for character. Open a file from an existing repository and, after saving, you'll find exactly the same frontmatter — no shifted blank lines, no inserted backslashes.

## Notes: the sticky note on the passage

"Add the source." "Dialogue feels wooden." "Cross-check with Chapter 4." Remarks like these belong in a particular spot, but not in the text. That's exactly what notes are for.

Place the cursor in a paragraph and choose **Format → Document → Insert Note**, or press **Ctrl+N — or set your own keyboard shortcut for it**. The note appears as a coloured card directly after the paragraph — never inside it — and you start writing. The shortcut can be changed or switched off in the settings under **Editor**. On Windows and Linux you should do that: there, the browser keeps Ctrl+N for opening a new window.

In the file, the note appears as an HTML comment with an identifier:

```markdown
Anna stand am Fenster und zählte die Züge.

<!-- bun.ink:note
Wie viele Züge fahren nachts wirklich? Fahrplan prüfen.
-->
```

### This form has three advantages:

- **It's invisible everywhere** the file is displayed: in the GitHub preview, on a website, in other Markdown programs.
- **It travels with the text.** The note is saved with the document, goes into the same commit and stays where it is as you write around it. No second storage location that could go missing.
- **It doesn't count as text.** Word counts and writing statistics leave notes out; the search still finds them — handy for tracking down every outstanding "add the source" in a project.

## A word of warning: invisible doesn't mean secret

A note is hidden in the rendered view, but readable in the file. Anyone looking at the raw file, a commit or a diff will see it too. In a public repository your notes are public, and an editor working in the same repository reads along. Anything nobody is allowed to see does not belong in a note. For remarks that really are meant for someone else, there's the [review via pull requests](/blog/reviews-as-pull-requests): there, comments live on GitHub at the pull request, not in the text. Notes are your own sticky notes.

## By the way: other people's comments stay put

Many files in docs repositories already come with HTML comments — hidden TODOs, instructions for validation tools. [bun.ink](http://bun.ink) shows them in grey in the editor and writes them back unchanged. That sounds obvious, but other writing editors simply lose such comments when saving.

For a detailed look at how it all works, see the handbook chapter [Metadata and Notes](https://github.com/VisionX-Development/writing-with-bunink/blob/main/en/11-metadata-and-notes.md).
