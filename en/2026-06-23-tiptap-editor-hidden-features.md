---
title: The TipTap Editor in bun.ink – Write More Calmly, Format Faster, Save Safely
date: 2026-06-23
description: "A look at the less obvious features of the TipTap editor in bun.ink: Zen mode, panic button, Markdown formatting, shortcuts, and how local cloud storage works together with GitHub branches."
sourceHash: a29c7a143b02d35b99ae2857033e7302b27ec6fe8b1b9ed131b6bd7da9b23cec
---

A good editor should stay out of the way while you write. It should be there when you need it – and disappear the moment you want to focus on your text. That's exactly why bun.ink uses the **TipTap editor**: a modern writing surface that can feel calm, yet offers a surprising number of possibilities beneath the surface.

Many of these features don't clamour for attention. They're more like small levers on your desk: once discovered, they make writing faster, more focused and more secure. This post shows you the most important ones.

## Zen mode – just you and the text

**Zen mode** is the quietest writing environment in bun.ink. When you're working in `/writer`, you can switch it on and off with a shortcut. You decide which key combination to use yourself in the settings: open **Settings** and then the **Editor** section. Under **Shortcuts** you'll find all of bun.ink's keyboard shortcuts, including **Zen mode**.

Zen mode deliberately isn't about lots of buttons, menus or distractions. Essentially, there are only three things you can adjust there:

- the **Text size**
- the **Transparency** of the text
- **Keep current line centered** – the line you're writing on stays in the middle of the screen, and the text scrolls beneath it

These settings are saved so that your calm writing environment looks exactly the way you need it next time. Zen mode isn't meant to be any more than that. It isn't a second, complicated editor – it's a space for writing.

## The stealth key – when the text needs to vanish for a moment

A special feature in Zen mode is the **stealth key**. You also define it in the settings under **Editor**, in the **Shortcuts** section under **Stealth mode**.

This key quickly toggles the text between two states:

- **invisible** – the text is hidden
- **semi-visible** – 50 per cent by default; you set how strong under **Visibility when shown** in the settings

In this form, it only works in Zen mode. The idea behind it is simple: if someone glances curiously at your screen, you can make the text visually disappear at the press of a key. The window then looks almost empty. That's handy for private notes, unfinished drafts, or simply for moments when your text is nobody else's business yet.

And yes: if nosy bosses come to mind here, that's meant with a wink, of course.

## Formatting with the format button

You reach all formatting via the **Format** button in the toolbar – the little T. It opens the editor's format menu, sorted into four groups:

- **Text** – bold, italic, strikethrough, inline code
- **Paragraph** – headings, lists, quote and code block
- **Display** – a line break without a new paragraph, the line spacing, and the **Markdown source**, which shows you the document exactly as it's saved
- **Document** – insert metadata and notes, plus **Show line breaks**, in case a line breaks in the middle of a paragraph

There's also the **Formatting bubble**. It appears automatically when you select a passage of text. Instead of opening the menu first, you apply individual formats directly to the selection – handy when you're revising and want to quickly bold a word or italicise a phrase. Which formats the bubble offers is up to you: set it in the settings under **Editor** at **Formatting bubble**. Every entry is explained in the [manual, in the chapter “The Editor”](https://github.com/VisionX-Development/writing-with-bunink/blob/main/en/03-the-editor.md).

One thing is important: the TipTap editor in bun.ink creates **Markdown documents**. Markdown is a simple notation in which formatting is described using certain characters. So you're not writing in a heavy layout format, but in a clear text format that's easy to save, export and version.

## A quick Markdown overview

Markdown works with just a few, easily readable characters. Some typical examples:

- `# Heading 1` becomes a large heading.
- `## Heading 2` becomes a subheading.
- `**bold text**` becomes **bold text**.
- `*italic text*` becomes _italic text_.
- `- list item` creates a bulleted list.
- `1. list item` creates a numbered list.
- `> quote` creates a quote block.
- `` `code` `` marks a short code or monospace expression.
- `` ``` `` at the start of a line, followed by a language such as `python`, begins a code block.

Not every visual formatting has its own simple character in classic Markdown. **Underlining**, for example, isn't one of the standard formats that Markdown covers with such symbols. That's why certain functions may deliberately not work the way they do in a classic word processor.

Another point: the Markdown characters shouldn't get in your way while writing. In the actual `.md` file, the document is provided as Markdown. In certain exports, such as `.txt`, the format characters can become visible, because there the plain text is output including its Markdown notation. You can always see exactly what the file looks like via **Format → Display → Markdown source**. And what else a Markdown file can contain besides the text is described in [Metadata and Notes](/blog/metadata-and-notes-in-markdown).

## Shortcuts: write faster, click less

TipTap already comes with a range of sensible default shortcuts. Which of them are available in bun.ink depends on which editor features are actively integrated. The best-known key combinations from the TipTap world are:

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

But bun.ink doesn't stop at the standard functions. There are also its own shortcuts, all in one place: in the settings under **Editor**, in the **Shortcuts** section. There you'll find **Insert note** (`Ctrl + N` by default, and the Control key on the Mac as well), **Save** (`Ctrl + S` or `Cmd + S`), **Stealth mode** and **Zen mode**. You can assign your own key combination to each shortcut.

The goal is clear: you should have to reach for the mouse as rarely as possible while writing. Navigation, focus, formatting and workflow should all be accessible directly from the keyboard.

## Hidden navigation: the keyboard as a writing tool

Shortcuts aren't just abbreviations for menu items. They change how writing feels. When you move paragraphs, set headings, open lists or switch to Zen mode without dropping out of your writing flow, your mind stays more firmly in the text.

This is where one of the editor's quiet strengths lies: many navigation and editing functions seem unspectacular, but over a long day of writing they save you a great many small interruptions. That makes a difference especially with longer manuscripts, notes or blog articles.

## Saving: locally, deliberately and with GitHub branches

Saving is worth a closer look too – above all because different paths feel right in the editor depending on your working mode. In normal writing mode, your current state goes into bun.ink's local cloud database as soon as you press **Save**.

If you're working on a **GitHub branch**, on the other hand, your state belongs on GitHub first – commit and push, not the cloud database. Which saving options you have at which moment, and how branches, merges and conflicts work in detail, is explained in the article [Using GitHub the right way – the versioning workflow in bun.ink](/blog/using-github-with-bun-ink). Here it's only about the editor's perspective: in **Branch mode**, the **History** tab isn't available, because branch states don't live in bun.ink's cloud database but on GitHub.

## Local versions – snapshots entirely without GitHub

Not everyone wants to or can use a GitHub account. For exactly this case, bun.ink offers – as other writing apps do – **local versions**: small snapshots of a document that you can create yourself at any time. They work independently of GitHub.

You'll find them in the sidebar in the **History** tab. There you can:

- create a new snapshot of your current state with **Save version**,
- **compare** a saved version **in the editor with your current text**,
- **restore** an earlier version – your current text is saved as a new version first, so nothing is lost.

In addition, bun.ink creates **automatic versions** in the background – without any action on your part. This happens gently and only when it's worthwhile: typically when you're taking a short writing break, when something has noticeably changed since the last snapshot, and when enough time has passed since the last automatic version (on the order of about ten minutes). That creates a safety net along the way, in case you forget to save a version yourself. In the history, such entries are marked as **Auto**, and ones you created yourself as **Manual**.

The number of manually created versions is deliberately limited: you can save **up to ten versions** per document. Once you reach that limit, simply delete a version you no longer need to make room for a new one. **Automatic versions don't count towards this** and are never blocked – they're an additional safety net, not a substitute for deliberately saving important states.

One note: the history always refers to the main state of your document. It isn't available in branch mode – branch states belong on GitHub (see [GitHub workflow](/blog/using-github-with-bun-ink)).

This way you get a simple, traceable version history directly in bun.ink, even without GitHub.

## What happens when you close, log out or trigger a security logout?

An editor doesn't just need to be able to save. It also has to warn you when you're about to lose unsaved work.

If you close a tab or want to log out even though new changes have been made since the last save, bun.ink should point that out to you. The editor recognises that the current content hasn't been saved yet and gives you the chance to save first or to deliberately continue with the action.

The **Security logout** is just as important. When it's enabled, it protects your account by automatically logging you out after a certain period of inactivity. So that nothing is lost in the process, bun.ink automatically saves all open changes to your account's local cloud storage before the automatic logout – otherwise those changes would be lost on logout. A GitHub push does not happen, though. You switch the security logout on and off under **Settings** in the **Security** section, where you also choose the period of inactivity.

Even so, it makes sense to save manually on a regular basis, especially during longer writing sessions – and particularly when you're working on a GitHub branch, where your changes only really arrive there via commit and push.

There's a clear rule of thumb here: **On a GitHub branch, only Save to branch – that is, commit and push to GitHub – really secures your work.** Until then, branch changes exist solely locally in this browser. If you log out, your browser crashes or you accidentally close the tab, only the states of a branch that have already been **pushed** are safe – anything not yet pushed can be lost. So push more often than you think you need to: it's practically impossible to push too much.

## An editor that quietly thinks along

The TipTap editor in bun.ink isn't just a text field. It combines a pared-back writing surface with Markdown, a tidy format menu, shortcuts, Zen mode, the stealth function, local versions and a saving model that supports both local cloud texts and GitHub branches.

It works best when you think of it not as a toolbox full of buttons, but as a writing space with a few well-placed switches. Some of them you'll use every day. Others you'll only need in particular moments. But they're there – hidden enough not to disturb you, and close enough to protect your writing flow.
