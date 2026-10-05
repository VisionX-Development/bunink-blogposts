---
title: Markdown that leaves your diff alone
date: 2026-10-05
description: What the bun.ink editor shows you, what's actually in the file, and why someone else's file looks exactly the same after you save it — apart from the sentence you changed.
sourceHash: 682f6c9bdd7721d26f35cecf44703e7d43feb3680f9844d92fb78bcb2eff1349
---

Anyone who maintains text in a Git repository knows the feeling: you change a single sentence in someone else's README, and the commit shows thirty changed lines. The editor has re-indented lists, escaped asterisks, realigned a table. The one sentence you actually cared about is almost impossible to find in the diff.

[bun.ink](https://bun.ink) is a writing editor for Markdown with GitHub behind it. This article explains what Markdown looks like in the editor, what of it ends up in the file – and the rule behind it all: **whatever you don't touch stays exactly as it was, character for character.**

## What you see and what gets saved

In the editor you see formatted text: headings, bold words, lists. What gets saved is Markdown – text in which formatting is expressed through characters. You have three ways to format:

- **As you type:** `#` followed by a space at the start of a line creates a heading, `-` a bullet list, `1.` a numbered list, `>` a quote. Asterisks around a word make it italic, double asterisks bold.
- **The format menu** in the toolbar, in five groups: **Text** (Bold, Italic, Strikethrough, Inline code), **Paragraph** (headings, lists, line break), **Blocks** (quote, code block, table), **Document** (metadata and notes, which appear in no preview) and **Display** (everything that only changes the view, never the file).
- **The formatting bubble**, which appears as soon as you select text. Which commands it offers is up to you in the settings.

There is no underline. Markdown doesn't have it, and bun.ink doesn't offer anything that would be lost again on saving. To see exactly what the file looks like, use **Format → Display → Markdown source** at any time.

## Three ways to end a line

This is where the most common surprise lies, and it's the best illustration of the principle. Markdown has three kinds of line endings, and they mean different things (CommonMark specification, [sections 6.7 and 6.8](https://spec.commonmark.org/0.31.2/#hard-line-breaks)):

| In the file | Meaning | In the editor |
|---|---|---|
| a blank line | new paragraph | Enter |
| two spaces or `\` before the line ending | hard break: new line within the same paragraph | Shift+Enter |
| a plain line ending | soft break: counts as a space | can't be typed |

The soft break is the interesting one. On GitHub, in the blog and in every export, the paragraph simply carries on as if there were a space there. So why write one at all? Because it makes diffs readable. Many people who maintain documentation under Git put every sentence on its own line, a convention called [Semantic Line Breaks](https://sembr.org/). When a sentence changes, the diff shows exactly that one line instead of the whole paragraph.

That's why a soft break is a space in the editor, and the paragraph flows just as the reader will later see it. On saving, though, every line ending comes back exactly as it was in the file. A repository that writes one sentence per line keeps that shape.

It wasn't always like this. The editor used to show a soft break as a real line break, and anyone typing next to it unknowingly turned it into a hard break. Two articles on this blog ended up with five-word lines in the middle of a paragraph. We noticed it on our own blog, not in a test case.

Two things help you keep track:

- **Markdown characters are ordinary text in the editor.** If you type two spaces and Enter, you get two spaces and a new paragraph, not a hard break. For that you use Shift+Enter, and bun.ink writes the Markdown characters itself.
- **Format → Display → Show line breaks** makes everything visible, like formatting marks in Word: **¶** at the end of every paragraph, **↵** for a hard break and **↩** for a soft one. If a line breaks in the middle of a paragraph even though there's still room to the right, you can see immediately why.

## What bun.ink doesn't touch in someone else's file

The Markdown serialiser the editor builds on writes text in its own "safe" form. That's handy as long as only bun.ink ever sees the file. For a file from someone else's repository it's a problem: every one of those transformations ends up in the next commit. In concrete terms, here's what happened when you changed a sentence somewhere and saved:

- **Special characters:** `a < b` became `a &lt; b`, `snake_case` became `snake\_case`, `&copy;` became `&amp;copy;`. On GitHub it then said "&copy;" instead of "©".
- **Spacing and notation:** several blank lines became one, `****` became `---`, `>Quote` became `> Quote`, indented code became a block with backticks.
- **Lists and tables:** continuation lines were re-indented, `_emphasis_` became `*emphasis*`, tables were realigned or vanished entirely.
- **Images:** of `![Screenshot](docs/bild.png)` only the word "Screenshot" remained.
- **Reference links:** the `[name]: https://…` lines at the end of the file were missing, and every link pointing to them led nowhere.
- **HTML:** the centred logo in the README (`<div align="center"><img …></div>`) was gone, a collapsible `<details>` section became body text, `<kbd>Ctrl</kbd>` became "Ctrl".
- **Front matter and comments:** the block at the start of the file was read as Markdown, hidden TODOs and lint directives disappeared.

All of this is fixed, and according to a single rule: **when a file is loaded, every block remembers its source text and the spacing from the previous block. As long as its content is the same, bun.ink writes exactly that back.** Only when you change a paragraph, a list or a table does that one block get rewritten. HTML and images appear in the editor as source text and as a small symbol with the alt text respectively; you see and edit them exactly as they appear in the file, and the text between two tags, as in `<kbd>Ctrl</kbd>`, like any other text.

We tested this on real files rather than examples: on all 66 Markdown files in the bun.ink repository, all 29 in the [handbook](https://github.com/VisionX-Development/writing-with-bunink), and – because our own files are too uniform – on 811 external Markdown files from bun.ink's dependencies: READMEs with badges, images and HTML, changelogs, documentation. Every single one comes back character for character unchanged after opening and saving. Before, it was only just over half of the READMEs.

## Tables

Tables from other files stay as they are as long as you don't change them. You create a new one with **Format → Blocks → Insert table**: three columns, a header row, two rows, after the paragraph at the cursor. Tab moves you from cell to cell, and past the last cell a new row appears. When the cursor is in a table, a plain bar appears above it with **+ Row**, **+ Column**, **− Row**, **− Column** and **×** to remove it. What gets saved is an ordinary GFM table that GitHub and every other renderer can display. You can't merge cells – Markdown has no merged cells.

## Code and what doesn't belong in the preview

**Inline code** sits in the middle of a sentence, for file names, commands and values, with a backtick before and after it. **Code blocks** stand on their own, across several lines, between three backticks, optionally with a language such as `python`. The editor sets both visibly apart from the text, the code block with a frame and the language as a label.

Two things live in the file but appear in no preview: **Metadata** (the front matter at the start of the file) and **notes**, reminders attached to a spot in the text and saved as an HTML comment. How both work is described in the article [Metadata and Notes in Markdown](/blog/metadata-and-notes-in-markdown).

## Pasting

Text you paste from an email or a PDF is often wrapped to a fixed width, with every line ending after about 80 characters. In the past, each line became its own paragraph. Today bun.ink recognises such text by its shape and pulls the lines back together into paragraphs. When in doubt, it leaves them as they are: one paragraph too many is quickly deleted, a lost one means work.

Snippets with formatting are also inserted correctly: a snippet containing `**important**` becomes bold instead of writing the asterisks into the text.

## What doesn't work (yet)

So you know what you can rely on:

- **A block you edit takes on the serialiser's form.** If you change a word in a paragraph containing `Tom & Jerry`, the file will then say `Tom &amp; Jerry`. It looks the same on GitHub, and in the diff that paragraph is marked as changed anyway – the others stay untouched.
- **Pasted Markdown** isn't yet picked up as formatting. If you paste text with `## Heading` or `**bold**`, for example from an AI agent's reply, the characters land in the editor as plain text.
- **Images** can't be uploaded yet. Images a file already embeds are preserved; they're only displayed on GitHub and in the blog.

## More on this

All the entries in the format menu, the table bar and the line breaks are described in the [handbook chapter "The Editor"](https://github.com/VisionX-Development/writing-with-bunink/blob/main/en/03-the-editor.md). The editor's hidden features and keyboard shortcuts are covered in the article [The TipTap Editor in bun.ink](/blog/tiptap-editor-hidden-features).
