---
title: Write Faster with Short Sentence Building Blocks
date: 2026-06-20
description: How text snippets in bun.ink insert common words and phrases with just a few keystrokes — and how jump markers make boilerplate text even more flexible.
sourceHash: fbb91625a0758e9b8ede582a2a0ec8efc4e2cd48cf38cd169f880c24e0fac446
---

Some words show up again and again in a text. Some are long, unfamiliar, or simply tedious to type. This is exactly where **text snippets** come in: short character abbreviations that bun.ink automatically replaces with a predefined text in the editor.

The principle is simple. Instead of spelling out `Supercalifragilisticexpialidocious` every time, an abbreviation like `sfd` can be enough. As soon as the abbreviation is typed in the editor and triggered, the full word appears. That not only saves time, it also prevents typos in terms, names, technical vocabulary, or recurring phrases.

## Words, names, and set phrases

Text snippets are especially well suited to anything that comes up often:

- difficult foreign words
- character or place names
- technical terms
- greetings and signatures
- recurring sentence openers or paragraphs

An abbreviation should be short but easy to remember. For a long technical term it might be an acronym, for a character perhaps their initials, for a standard phrase a small pattern. The only thing that matters is that your writing flow stays intact. The text block appears right where you need it.

## Jump marks for flexible building blocks

Text snippets become even more flexible with **Jump marks**. They make text blocks adaptable, because an inserted snippet no longer has to be entirely fixed.

In the editor settings you can, for example, define the character sequence `{}` as a jump mark. This marker can be used directly inside text snippets. You can also put default text between the brackets.

A text block might then look like this:

```text
Der Wind bläst kräftig {durch das Haus}.
```

The matching abbreviation could be `wb`. When the text block is inserted, the sentence appears in the editor with the section `durch das Haus` selected. Pressing Tab moves the cursor to the next jump mark. Press Tab again and the default text stays as it is — just without the `{}` markers. If instead you start typing right away, the new text replaces the selected section.

That way the same building block can quickly turn into a different sentence:

```text
Der Wind bläst kräftig durch die Haare.
```

## Small building blocks, less friction

Text snippets aren't some grand automation that writes the text for you. They're more of a small tool against repetition and friction. Long words, set phrases, and variable sentence parts can be inserted with just a few characters.

That's particularly valuable while writing: your attention stays on the sentence, not on the mechanics of typing.
