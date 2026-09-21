---
title: The TipTap Editor in bun.ink – Write More Calmly, Format Faster, Save Safely
date: 2026-06-23
description: 'A look at the less obvious features of the TipTap editor in bun.ink: Zen mode, the stealth key, Markdown formatting, shortcuts, and the interplay between local cloud storage and GitHub branches.'
sourceHash: f9204a9293be95d76c70a88d71eafcfa1ac90813421267e111cccde3723d6e9d
---

A good editor should barely make itself noticed while you write. It should be there when you need it – and disappear the moment you want to focus on your text. That's exactly why bun.ink relies on the **TipTap editor**: a modern writing surface that can feel calm, yet offers a surprising range of possibilities beneath the surface.

Many of these features don't get loudly in the way. They're more like small levers at your desk: once discovered, they make writing faster, more focused, and safer. This post walks you through the most important ones.

## Zen mode – just you and the text

**Zen mode** is the calmest writing environment in bun.ink. When you work under `/writer`, you can toggle it on and off with a shortcut. Which key combination you use for this is up to you: open **Settings** and then the **Editor** section. There you'll find all the shortcuts that bun.ink provides for the editor – or will add in the future.

Zen mode is deliberately not about lots of buttons, menus, or distractions. At its core, there are only two things you can adjust:

- the **font size**
- the **text transparency**

These settings are saved so that your calm writing environment looks the way you need it the next time around. Zen mode isn't meant to be anything more than that. It's not a second, complicated editor, but simply a space to write.

## The stealth key – when the text should briefly disappear

A special feature within Zen mode is the **stealth key**. It too can be assigned its own key in the editor settings.

With this key, you quickly toggle the text transparency between two states:

- **100 percent transparency** – the text is not visible
- **50 percent transparency** – the text is half-transparent and visible

In this form, it only works in Zen mode. The idea behind it is simple: if someone glances curiously at your screen, you can make the text visually vanish with a single keystroke. The window then looks almost empty. This comes in handy for private notes, unfinished drafts, or simply for moments when your text is nobody else's business just yet.

And yes: if you happen to think of nosy bosses here, that's meant with a wink, of course.

## Formatting with the T button

You reach the most important formatting options through the **T button**. It opens the editor's format menu. There you'll find the basic functions you regularly need while writing: headings, lists, emphasis, quotes, and similar basic formats.

There's also a so-called **bubble field**. It appears automatically when you select a passage of text. Instead of first opening a large menu, you can apply individual basic functions directly to your selection. This is especially handy when, while revising, you quickly want to make a word bold, mark a passage in italics, or highlight a section as a quote.

One important point: the TipTap editor in bun.ink creates **Markdown documents**. Markdown is a simple notation in which formatting is described using specific characters. So you're not writing in a heavy layout format, but in a clear text format that's easy to save, export, and version.

## A quick Markdown overview

Markdown works with a few, easily readable characters. Some typical examples:

- `# Heading 1` becomes a large heading.
- `## Heading 2` becomes a subheading.
- `**bold text**` becomes **bold text**.
- `*italic text*` becomes _italic text_.
- `- List item` creates a bulleted list.
- `1. List item` creates a numbered list.
- `> Quote` creates a quote block.
- `` `Code` `` marks a short code or monospace expression.

Not every visual formatting has its own simple character in classic Markdown. **Underlining**, for example, isn't among the standard formats that Markdown covers with such symbols. That's why certain functions may deliberately not work the way they would in a classic word processor.

Another thing to keep in mind: the Markdown characters aren't meant to disturb you while writing. In the actual `.md` file, the document is provided as Markdown. In certain exports, such as `.txt`, the formatting characters may become visible, because there the plain text is output including its Markdown notation.

## Shortcuts: write faster, click less

TipTap already comes with a range of useful default shortcuts. Which of them are available in bun.ink depends on which editor functions are actively enabled. The most important known key combinations from the TipTap world are:

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
- **Select all:** `Ctrl + A` or `Cmd + A`

But bun.ink doesn't stop at the standard functions. The app places particular emphasis on its own shortcuts, developed specifically for a comfortable writing experience. Many of these you can enable, disable, or assign to your own key combination in the settings. This includes, for example, the already-mentioned shortcut for the stealth key.

More practical keyboard functions are planned. The goal is clear: you should have to reach for the mouse as rarely as possible while writing. Navigation, focus, formatting, and workflow should all be accessible directly from the keyboard.

## Hidden navigation: the keyboard as a writing tool

Shortcuts aren't just abbreviations for menu items. They change how writing feels. When you move paragraphs, set headings, open lists, or switch to Zen mode without falling out of your writing flow, your mind stays more firmly within the text.

This is exactly where one of the editor's quiet strengths lies: many navigation and editing functions seem unspectacular, yet over a long writing day they save you many small interruptions. This makes a real difference, especially with longer manuscripts, notes, or blog articles.

## Saving: local, deliberate, and with GitHub branches

Saving is worth a closer look too – above all because different approaches can feel right in the editor depending on your working mode. In normal writing mode, your current state lands in bun.ink's local cloud database as soon as you press **Save**.

If, on the other hand, you're working on a **GitHub branch**, the state first goes to GitHub – commit and push, not the cloud database. Which saving options you have at which moment, and how branches, merges, and conflicts work in detail, is explained in the article [Using GitHub properly – the versioning workflow in bun.ink](/blog/using-github-with-bun-ink). Here we focus only on the editor perspective: in **branch mode**, the **History** tab is not available, because branch states are stored on GitHub rather than in bun.ink's cloud database.

## Local versions – snapshots without any GitHub

Not everyone wants to or can use a GitHub account. For exactly this case, bun.ink – like other writing apps – offers **local versions**: small snapshots of a document that you can create yourself at any time. They work independently of GitHub.

You'll find them in the sidebar under the **History** tab. There you can:

- create a new snapshot of your current state with **Save version**,
- **compare a saved version with your current text in the editor**,
- **restore** an earlier version – your current text is saved as a new version first, so nothing gets lost.

In addition, bun.ink creates **automatic versions** in the background – entirely on its own. This happens gently and only when it's worthwhile: typically when you're taking a short writing break, something has noticeably changed since the last snapshot, and enough time has passed since the last automatic version (on the order of about ten minutes). This creates a safety net along the way in case you ever forget to save a version yourself. In the history, such entries are marked as **Automatic**, while manually created ones are marked as **Manual**.

The number of manually created versions is deliberately limited: you can save **up to ten versions** per document. Once this limit is reached, you simply delete a version you no longer need to make room for a new one. **Automatic versions don't count toward this limit** and are never blocked – they are an additional safety net, not a substitute for deliberately saving important states.

One note: the history always refers to the main state of your document. It's not available in branch mode – branch states belong on GitHub (see [GitHub workflow](/blog/using-github-with-bun-ink)).

This way, even without GitHub, you get a simple, traceable version history right inside bun.ink.

## What happens when you close, log out, or auto-log out?

An editor doesn't just need to be able to save. It also needs to warn you when you're about to lose unsaved work.

If you close a tab or want to log out even though new changes have been made since your last save, bun.ink should alert you. The editor recognizes that the current content hasn't been saved yet and gives you the option to save first or to deliberately continue the action.

Similarly important is the **auto-logout function**. When it's enabled, it protects your account by automatically logging you out after a certain period of inactivity. So that nothing gets lost in the process, bun.ink automatically saves all open changes to your account's local cloud storage before the automatic logout – otherwise these changes would be lost at logout. A GitHub push does not happen, however. You can turn the auto-logout function on and off under **Settings** in the **Security** section.

Even so, it makes sense to save manually on a regular basis, especially during longer writing sessions – above all when you're working on a GitHub branch and your changes only truly land there through a commit and push.

This is precisely where a clear rule of thumb applies: **on a GitHub branch, only the commit and push to GitHub truly saves your work.** Until then, branch changes exist solely locally in that browser. In the event of a logout, a browser crash, or an accidentally closed tab, only the already **pushed** states of a branch are secured – anything not yet pushed can be lost. So push more often than you think you need to: there's practically no such thing as pushing too much.

## An editor that quietly thinks along

The TipTap editor in bun.ink isn't just a text field. It combines a pared-down writing surface with Markdown, shortcuts, Zen mode, the stealth function, local versions, and a saving model that supports both local cloud texts and GitHub branches.

It works best when you think of it not as a toolbox full of buttons, but as a writing space with a few well-placed switches. Some of them you'll use every day. Others you'll only need in particular moments. But they're there – hidden enough not to disturb you, and close enough to protect your writing flow.
