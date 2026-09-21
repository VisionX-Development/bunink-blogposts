---
title: Writing Faster with Short Text Snippets
date: 2026-06-20
description: How text snippets in bun.ink insert frequent words and phrases with just a few characters — and how jump marks make text blocks even more flexible.
sourceHash: b34761b8b2ef38073e51cc2d6b6720ab3d2c91bbeee71b5d53b6d793c92299fc
---

Some words appear in a text again and again. Some are long, unfamiliar, or simply annoying to type. This is exactly where **text snippets** help: short character shortcuts that bun.ink automatically replaces in the editor with a predefined text.

The principle is simple. Instead of typing out `Supercalifragilisticexpialidocious` every time, a shortcut like `sfd` can be enough. As soon as the shortcut is entered and triggered in the editor, the full word appears. That saves time and also prevents typos in terms, names, technical words, or recurring phrases.

## Words, names, and fixed phrases

Text snippets are especially useful for anything that comes up often:

- difficult foreign words
- character or place names
- technical terms
- greetings and signatures
- recurring sentence openings or paragraphs

A shortcut should be short, but easy to remember. For a long technical term, it might be an abbreviation; for a character, perhaps the initials; for a standard phrase, a small pattern. The important part is that the writing flow stays intact. The text block appears exactly where you need it.

## Jump marks for flexible blocks

Text snippets become even more flexible with **jump marks**. They make text blocks adaptable because an inserted snippet no longer has to be completely fixed.

In the editor settings, a character sequence such as `{}` can be configured as a jump mark. This marker can then be used directly inside text snippets. Default text may also be placed between the braces.

A text block could look like this:

```text
The wind blows strongly {through the house}.
```

The shortcut for it could be `wb`. When the text block is inserted, the sentence appears in the editor, and the section `through the house` is selected. The cursor jumps to the next jump mark with the Tab key. If you press Tab again, the default text stays in place — just without the `{}` marker. If you start typing instead, the new text replaces the selected section.

That turns the same block into a different sentence very quickly:

```text
The wind blows strongly through the hair.
```

## Small blocks, less friction

Text snippets are not a large automation that takes over the writing. They are more like a small tool against repetition and friction. Long words, fixed phrases, and variable sentence parts can be inserted with just a few characters.

That is valuable in writing: attention stays on the sentence, not on the mechanics of typing.
