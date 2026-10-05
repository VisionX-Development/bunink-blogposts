---
title: Markdown That Leaves Your Diff Alone
date: 2026-10-05
description: What the bun.ink editor shows you, what's actually in the file, and why someone else's file stays character-for-character identical after you save it — apart from the sentence you changed.
sourceHash: 8bc30ef94fe5d13d69c03d632fe0c08e0ebf780102cef23961985454dfe09562
---

If you maintain text in a Git repository, you know the problem: you change a single sentence in someone else's README, and the commit shows thirty changed lines. The editor has re-indented lists, escaped asterisks, realigned a table. The one sentence you actually cared about disappears in the diff.

[bun.ink](https://bun.ink) is a writing editor for Markdown with GitHub behind it, and it follows one simple rule: **whatever you don't touch stays exactly as it is in the file, character for character.**

## What you see and what gets saved

In the editor you see formatted text; what gets saved is Markdown. There are three ways to format:

- **While typing:** `#` and a space at the start of a line makes a heading, `-` a bullet list, `1.` a numbered list, `>` a quote, asterisks around a word make it italic or bold.
- **With the format menu** in five groups: **Text**, **Paragraph**, **Blocks**, **Document** (metadata and notes that appear in no preview) and **Display** (everything that only changes the view, never the file).
- **With the formatting bubble** that appears when you select text and whose commands you choose in the settings.

There is no underline, because Markdown doesn't have one. To see exactly what the file looks like, use **Format → Display → Markdown source**.

## Three ways to end a line

Markdown has three line endings with different meanings (CommonMark specification, [sections 6.7 and 6.8](https://spec.commonmark.org/0.31.2/#hard-line-breaks)):

| In the file | Meaning | In the editor |
|---|---|---|
| a blank line | new paragraph | Enter |
| two spaces or `\` before the line ending | new line in the same paragraph | Shift+Enter |
| a plain line ending | soft break, counts as a space | can't be typed |

The soft break is what makes diffs readable. Many people writing documentation under Git put each sentence on its own line – the convention is called [Semantic Line Breaks](https://sembr.org/). If a sentence changes, the diff shows exactly that one line. In the editor a soft break is a space, and the paragraph flows the way the reader will see it. When you save, every line ending comes back just as it was in the file.

Markdown characters are ordinary text in the editor: two typed spaces stay two spaces. To break a line within a paragraph, use Shift+Enter. **Format → Display → Show line breaks** shows them the way formatting marks work in Word: **¶** at the end of a paragraph, **↵** for a hard break and **↩** for a soft one.

## What bun.ink leaves untouched in someone else's file

When you open and save a Markdown file, everything you don't edit stays as it is:

- **Special characters:** `a < b`, `snake_case`, `[x]` and entities like `&copy;` are still in the file exactly as before.
- **Spacing and spelling variants:** several blank lines, `****` as a horizontal rule, `>Zitat` without a space, indented code.
- **Lists and tables:** indentation, `*` or `-`, `_emphasis_`, the alignment of every table column.
- **Images and reference links:** `![Screenshot](docs/bild.png)` and the `[name]: https://…` lines at the end of the file.
- **HTML:** the centred logo in the README, collapsible `<details>` sections, `<kbd>` and `<sup>`.
- **Front matter and comments:** the block at the top of the file and hidden TODOs.

There's one rule behind this: **when loading, every block remembers its own source text and the spacing to the previous block. As long as its content is unchanged, bun.ink writes exactly that back.** If you change a paragraph, a list or a table, only that one block is rewritten. HTML appears in the editor as source text, an image as a small marker with its alt text.

This has been verified against real files: all 66 Markdown files in the bun.ink repository, all 29 in the [handbook](https://github.com/VisionX-Development/writing-with-bunink), and 811 third-party Markdown files from bun.ink's dependencies – READMEs with badges, images and HTML, changelogs, documentation. Every one of them comes back character for character unchanged after opening and saving.

## Tables and code

You create a new table with **Format → Blocks → Insert table**. Tab moves from cell to cell and adds a row after the last one. When the cursor is inside a table, a bar appears above it with **+ Row**, **+ Column**, **− Row**, **− Column** and **×** to remove it. What gets saved is an ordinary GFM table.

**Inline code** sits in the middle of a sentence, between two backticks. **Code blocks** stand on their own, between three backticks, optionally with a language such as `python`. Both are visibly set apart from the text in the editor.

Metadata and notes are stored in the file but appear in no preview. How both work is described in the article [Metadata and Notes in Markdown](/blog/metadata-and-notes-in-markdown).

## Pasting

Text from an email or a PDF is often wrapped to a fixed width. bun.ink recognises this by its shape and joins the lines back into paragraphs. When in doubt, it leaves them as they are: one paragraph too many is quickly deleted, a lost one means work. Snippets with formatting are pasted with their formatting: `**important**` becomes bold.

## What doesn't work (yet)

- **A block you edit takes on the form of the serialiser.** If you change a word in a paragraph containing `Tom & Jerry`, the file will then read `Tom &amp; Jerry`. On GitHub it looks the same, and in the diff that paragraph has changed anyway.
- **Pasted Markdown** is not taken over as formatting: `## Heading` from an AI agent's reply ends up as plain text in the editor.
- **Images** can't be uploaded. Embedded images are preserved and show up on GitHub and in the blog.

## More on this

The format menu, the table bar and line breaks are described in the [handbook chapter “The Editor”](https://github.com/VisionX-Development/writing-with-bunink/blob/main/en/03-the-editor.md), the keyboard shortcuts in the article [The TipTap Editor in bun.ink](/blog/tiptap-editor-hidden-features).
