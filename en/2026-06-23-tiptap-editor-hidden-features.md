---
title: The TipTap Editor in bun.ink – Write More Calmly, Format Faster, Save Safely
date: 2026-06-23
description: "A look at the less obvious features of the TipTap editor in bun.ink: zen mode, panic button, Markdown formatting, shortcuts, and how local cloud storage and GitHub branches work together."
sourceHash: 2ac620e278cff5d3fbc7807748fa82298d3241510546bd310a735d2f0912f7c0
---

A good editor should stay out of the way while you write. It should be there when you need it — and disappear the moment you want to focus on your text. That's exactly why bun.ink uses the **TipTap editor**: a modern writing surface that can feel perfectly calm, yet offers a surprising number of possibilities beneath the surface.

Many of these features don't clamour for attention. They're more like small levers on your desk: once you've found them, they make writing faster, more focused and more secure. This post shows you the most important ones.

## Zen mode — just you and the text

**Zen mode** is the quietest writing environment in bun.ink. When you're working under `/writer`, you can toggle it on and off with a shortcut. Which key combination that is, you decide yourself in the settings: open **Settings** and then the **Editor** section. Under **Shortcuts** you'll find all of bun.ink's keyboard shortcuts, including **Zen mode**.

Zen mode is deliberately not about lots of buttons, menus or distractions. There are essentially only three things you can adjust there:

- the **Text size**
- the **Transparency** of the type
- **Keep current line centered** — the line you're writing on stays in the middle of the screen, and the text scrolls beneath it

These settings are saved, so that your quiet writing environment looks the way you need it again next time. Zen mode isn't meant to be anything more than that. It's not a second, complicated editor, but a space for writing.

## The stealth key — when the text needs to vanish for a moment

A special feature in Zen mode is the **stealth key**. You also define it in the settings under **Editor**, in the **Shortcuts** section under **Stealth mode**.

This key quickly switches the type between two states:

- **invisible** — the text is hidden
- **semi-visible** — 50 percent by default; you set the level in the settings under **Visibility when shown**

In this form it only works in Zen mode. The idea behind it is simple: if someone glances curiously at your screen, you can make the text visually disappear with a single keystroke. The window then looks almost empty. That's handy for private notes, unfinished drafts, or simply for moments when your text is nobody else's business yet.

And yes: if nosy bosses come to mind here, that's of course meant with a wink.

## Formatting with the format button

All formatting is available via the **Format** button in the toolbar — the little T. It opens the editor's format menu, sorted into four groups:

- **Text** — bold, italic, strikethrough, inline code
- **Paragraph** — headings, lists, quote and code block
- **Display** — a line break without a new paragraph, the line spacing and the **Markdown source**, which shows you the document exactly as it is saved
- **Document** — insert metadata and notes, and **Show line breaks**, in case a line breaks in the middle of a paragraph

There's also the **Formatting bubble**. It appears automatically when you select a passage of text. Instead of opening the menu first, you apply individual formats directly to the selection — practical when you're revising and want to quickly bold a word or italicise a phrase. Which formats the bubble offers is up to you, in the settings under **Editor** at **Formatting bubble**. Every entry is explained in [the handbook chapter "The Editor"](https://github.com/VisionX-Development/writing-with-bunink/blob/main/en/03-the-editor.md).

One thing is important: the TipTap editor in bun.ink creates **Markdown documents**. Markdown is a simple notation in which formatting is described by particular characters. So you're not writing in a heavy layout format, but in a clear text format that's easy to save, export and version.

## A quick Markdown overview

Markdown works with a few, easily readable characters. Some typical examples:

- `# Heading 1` becomes a large heading.
- `## Heading 2` becomes a subheading.
- `**bold text**` becomes **bold text**.
- `*italic text*` becomes _italic text_.
- `- list item` creates a bulleted list.
- `1. list item` creates a numbered list.
- `> quote` creates a block quote.
- `` `code` `` marks a short code or monospace expression.
- `` ``` `` at the start of a line, followed by a language such as `python`, begins a code block.

Not every visual format has its own simple character in classic Markdown. **Underlining**, for example, is not among the standard formats that Markdown covers with such symbols. So it may be that certain functions deliberately don't work the way they would in a classic word processor.

What's more: the Markdown characters shouldn't get in your way while writing. In the actual `.md` file, the document is provided as Markdown. In certain exports, for instance as `.txt`, the format characters can become visible, because what's written out there is the plain text including its Markdown notation. You can see exactly what the file looks like at any time via **Format → Display → Markdown source**. And what a Markdown file can contain besides the text is described in [Metadata and Notes](/blog/metadata-and-notes-in-markdown).

## Shortcuts: write faster, click less

TipTap already comes with a range of sensible default shortcuts. Which of them are available in bun.ink depends on which editor functions are actively integrated. The best-known key combinations from the TipTap world are:

- **Copy:** `Ctrl + C` on Windows/Linux, `Cmd + C` on macOS
- **Cut:** `Ctrl + X` or `Cmd + X`
- **Paste:** `Ctrl + V` or `Cmd + V`
- **Paste without formatting:** `Ctrl + Shift + V` or `Cmd + Shift + V`
- **Undo:** `Ctrl + Z` or `Cmd + Z`
- **Redo:** `Ctrl + Shift + Z` or `Cmd + Shift + Z`
- **Bold:** `Ctrl + B` or `Cmd + B`
- **Italic:** `Ctrl + I` or `Cmd + I`
- **Strikethrough:** `Ctrl + Shift + S` or `Cmd + Shift + S`
- **Normal paragraph:** `Ctrl + Alt + 0` or `Cmd + Alt + 0`
- **Headings:** `Ctrl + Alt + 1` to `Ctrl + Alt + 6` or `Cmd + Alt + 1` to `Cmd + Alt + 6`
- **Numbered list:** `Ctrl + Shift + 7` or `Cmd + Shift + 7`
- **Bulleted list:** `Ctrl + Shift + 8` or `Cmd + Shift + 8`
- **Line break within the same paragraph:** `Shift + Enter`
- **Select all:** `Ctrl + A` or `Cmd + A`

But bun.ink doesn't stop at the standard functions. There are also its own shortcuts, all in one place: in the settings under **Editor** in the **Shortcuts** section. There you'll find **Insert note** (`Ctrl + N` by default, the Control key on the Mac too), **Save** (`Ctrl + S` or `Cmd + S`), **Stealth mode** and **Zen mode**. You can assign your own key combination to each of them.

The goal is clear: you should have to reach for the mouse as rarely as possible while writing. Navigation, focus, formatting and workflow should all be reachable straight from the keyboard.

## Hidden navigation: the keyboard as a writing tool

Shortcuts aren't just abbreviations for menu items. They change how writing feels. When you move paragraphs, set headings, open lists or switch into Zen mode without dropping out of the flow, your head stays more firmly in the text.

That's one of the editor's quiet strengths: many navigation and editing functions look unspectacular, but over a long day of writing they save a great many small interruptions. With longer manuscripts, notes or blog articles in particular, that makes a difference.

## Saving: local, deliberate and with GitHub branches

Saving is also worth a closer look — above all because, depending on the mode you're working in, the editor offers different routes. In normal writing mode, your current state goes into bun.ink's local cloud database as soon as you press **Save**.

If, on the other hand, you're working on a **GitHub branch**, the state belongs on GitHub first — commit and push, not the cloud database. Which save options you have at which moment, and how branches, merges and conflicts work in detail, is explained in the article [Using GitHub Properly — the Versioning Workflow in bun.ink](/blog/using-github-with-bun-ink). Here it's only about the editor's perspective: in **Branch mode** the **History** tab is not available, because branch states live on GitHub rather than in bun.ink's cloud database.

## Local versions — snapshots entirely without GitHub

Not everyone wants to — or can — use a GitHub account. For exactly this case, bun.ink offers, as other writing apps do, **local versions**: small snapshots of a document that you can create yourself at any time. They work independently of GitHub.

You'll find them in the sidebar under the **History** tab. There you can:

- create a new snapshot of your current state with **Save version**,
- **compare** a saved version **with your current text in the editor**,
- **restore** an earlier version — your current text is first secured as a new version, so nothing gets lost.

In addition, bun.ink creates **automatic versions** in the background, entirely without your involvement. This happens gently and only when it's worthwhile: typically when you're taking a short writing break, when something noticeable has changed since the last snapshot, and when enough time has passed since the last automatic version (on the order of about ten minutes). That way a safety net quietly builds up, in case you ever forget to save a version yourself. In the history, such entries are labelled **Automatic**, manually created ones **Manual**.

The number of manually created versions is deliberately limited: you can save **up to ten versions** per document. Once that limit is reached, you simply delete a version you no longer need to make room for a new one. **Automatic versions don't count towards this** and are never blocked — they're an extra safety net, not a substitute for deliberately saving important states.

One note: the history always refers to the main state of your document. In branch mode it isn't available — branch states belong on GitHub (see [GitHub workflow](/blog/using-github-with-bun-ink)).

So even without GitHub you get a simple, comprehensible version history directly in bun.ink.

## What happens when you close, log out, or the security logout kicks in?

An editor doesn't just need to be able to save. It also needs to warn you when you're about to lose unsaved work.

If you close a tab or want to log out although new changes have been made since the last save, bun.ink should point that out to you. The editor recognises that the current content hasn't been secured yet, and gives you the chance to save first or to deliberately continue.

Equally important is the **Security logout**. When it's enabled, it protects your account by logging you out automatically after a certain period of inactivity. So that nothing gets lost in the process, bun.ink automatically saves all open changes to your account's local cloud storage before the automatic logout — otherwise those changes would be lost at logout. A GitHub push, however, does not happen. You switch the security logout on and off under **Settings** in the **Security** section, where you also choose the period of inactivity.

Even so, it makes sense to save manually at regular intervals during longer writing sessions — especially when you're working on a GitHub branch and your changes only really arrive there via commit and push.

And here a clear rule of thumb applies: **on a GitHub branch, only Save to branch — that is, commit and push to GitHub — really secures your work.** Until then, branch changes exist solely locally in this browser. In the event of a logout, a browser crash or an accidentally closed tab, only the states of a branch that have already been **pushed** are safe — anything not yet pushed can be lost. So push more often than you think you need to: it's practically impossible to push too much.

## An editor that quietly thinks along

The TipTap editor in bun.ink isn't just a text field. It combines a pared-back writing surface with Markdown, a tidy format menu, shortcuts, Zen mode, the stealth function, local versions and a saving model that supports both local cloud texts and GitHub branches.

It works best when you think of it not as a toolbox full of buttons, but as a writing space with a few well-placed switches. Some of them you'll use every day. Others you'll only need in particular moments. But they're there — hidden enough not to disturb you, and close enough to protect your writing flow.
