---
title: The TipTap Editor in bun.ink – Write More Calmly, Format Faster, Save Safely
date: 2026-06-23
description: "A look at the less obvious features of the TipTap editor in bun.ink: zen mode, stealth key, Markdown formatting, shortcuts, and how local cloud storage works together with GitHub branches."
sourceHash: f9204a9293be95d76c70a88d71eafcfa1ac90813421267e111cccde3723d6e9d
---

A good editor should be as unobtrusive as possible while you write. It should be there when you need it – and disappear the moment you want to focus on your text. That's exactly why bun.ink relies on the **TipTap editor**: a modern writing surface that can feel calm, yet offers a surprising number of possibilities beneath the surface.

Many of these features don't shout for attention. They're more like small levers at your desk: once you've discovered them, they make writing faster, more focused and more secure. This post shows you the most important ones.

## Zen mode – just you and the text

**Zen mode** is the quietest writing environment in bun.ink. When you're working in `/writer`, you can toggle it on and off with a shortcut. Which key combination is used for this is something you define yourself in the settings: open **Settings** and then the **Editor** section. There you'll find all the shortcuts bun.ink provides for the editor, or will add in the future.

Zen mode is deliberately not about lots of buttons, menus or distractions. Essentially, there are only two things you can adjust there:

- the **font size**
- the **text transparency**

These settings are saved so that your quiet writing environment looks exactly the way you need it next time. Zen mode isn't meant to be anything more than that. It's not a second, more complicated editor, but a room for writing.

## The stealth key – when your text needs to vanish for a moment

One special feature in zen mode is the **stealth key**. It, too, can be assigned its own key in the editor settings.

With this key you can quickly toggle the text transparency between two states:

- **100 percent transparency** – the text is invisible
- **50 percent transparency** – the text is semi-transparent

In this form, it only works in zen mode. The idea behind it is simple: if someone takes a curious look at your screen, you can make the text visually disappear with a single keystroke. The window then looks almost empty. That's handy for private notes, unfinished drafts, or simply for moments when your text is nobody else's business yet.

And yes: if nosy bosses come to mind here, that's of course meant with a wink.

## Formatting with the T button

You can reach the most important formatting options via the **T button**. It opens the editor's format menu. There you'll find the basic functions you need regularly while writing: headings, lists, emphasis, quotes and similar basic formats.

In addition, there's what's known as a **bubble field**. It appears automatically when you select a passage of text. Instead of first opening a large menu, you can apply individual basic functions directly to your selection. That's especially handy when revising and you quickly want to bold a word, italicise a passage, or turn a section into a quote.

One important point: the TipTap editor in bun.ink creates **Markdown documents**. Markdown is a simple notation in which formatting is described using certain characters. So you're not writing in a heavy layout format, but in a clear text format that's easy to save, export and version.

## A short Markdown overview

Markdown works with a few easily readable characters. Some typical examples:

- `# Überschrift 1` becomes a large heading.
- `## Überschrift 2` becomes a subheading.
- `**fetter Text**` becomes **bold text**.
- `*kursiver Text*` becomes _italic text_.
- `- Listenpunkt` creates a bulleted list.
- `1. Listenpunkt` creates a numbered list.
- `> Zitat` creates a quote block.
- `` `Code` `` marks a short code or monospace expression.

Not every visual formatting option has its own simple character in classic Markdown. **Underlining**, for example, isn't one of the standard formats that Markdown covers with such symbols. That's why certain functions may deliberately not behave the way they would in a classic word processor.

What's more, the Markdown characters shouldn't get in your way while writing. In the actual `.md` file, the document is provided as Markdown. In certain exports, for instance as `.txt`, the formatting characters can become visible, because what's output there is the plain text including its Markdown notation.

## Shortcuts: write faster, click less

TipTap already comes with a range of sensible default shortcuts. Which of them are available in bun.ink depends on which editor functions are actively integrated. The best-known key combinations from the TipTap world are:

- **Copy:** `Strg + C` on Windows/Linux, `Cmd + C` on macOS
- **Cut:** `Strg + X` or `Cmd + X`
- **Paste:** `Strg + V` or `Cmd + V`
- **Paste without formatting:** `Strg + Shift + V` or `Cmd + Shift + V`
- **Undo:** `Strg + Z` or `Cmd + Z`
- **Redo:** `Strg + Shift + Z` or `Cmd + Shift + Z`
- **Bold:** `Strg + B` or `Cmd + B`
- **Italic:** `Strg + I` or `Cmd + I`
- **Strikethrough:** `Strg + Shift + S` or `Cmd + Shift + S`
- **Normal paragraph:** `Strg + Alt + 0` or `Cmd + Alt + 0`
- **Headings:** `Strg + Alt + 1` to `Strg + Alt + 6` or `Cmd + Alt + 1` to `Cmd + Alt + 6`
- **Numbered list:** `Strg + Shift + 7` or `Cmd + Shift + 7`
- **Bulleted list:** `Strg + Shift + 8` or `Cmd + Shift + 8`
- **Select all:** `Strg + A` or `Cmd + A`

But bun.ink doesn't stop at the standard functions. The app places particular value on its own shortcuts, developed specifically for a comfortable writing experience. Many of them can be enabled, disabled or assigned your own key combination in the settings. That includes the stealth key shortcut already mentioned.

More practical keyboard functions are planned. The goal is clear: you should have to reach for the mouse as rarely as possible while writing. Navigation, focus, formatting and workflow should all be accessible directly from the keyboard.

## Hidden navigation: the keyboard as a writing tool

Shortcuts aren't just abbreviations for menu items. They change how writing feels. When you move paragraphs, set headings, start lists or switch to zen mode without falling out of your writing flow, your mind stays more firmly in the text.

That's precisely where one of the editor's quiet strengths lies: many navigation and editing functions seem unspectacular, yet over a long day of writing they save you a lot of small interruptions. With longer manuscripts, notes or blog articles in particular, that makes a difference.

## Saving: locally, deliberately and with GitHub branches

Saving is also worth a closer look – especially because different paths feel right in the editor depending on which mode you're working in. In normal writing mode, your current state goes into bun.ink's local cloud database as soon as you press **Save**.

If, on the other hand, you're working on a **GitHub branch**, that state belongs on GitHub first – commit and push, not the cloud database. Which saving options you have at which moment, and how branches, merges and conflicts work in detail, is explained in the article [Using GitHub the right way – the versioning workflow in bun.ink](/blog/using-github-with-bun-ink). Here we're only looking at the editor's perspective: in **branch mode**, the **History** tab isn't available, because branch states live on GitHub rather than in bun.ink's cloud database.

## Local versions – snapshots entirely without GitHub

Not everyone wants to or can use a GitHub account. For exactly that case, bun.ink offers – like other writing apps – **local versions**: small snapshots of a document that you can create yourself at any time. They work independently of GitHub.

You'll find them in the sidebar under the **History** tab. There you can:

- create a new snapshot of your current state with **Save version**,
- **compare** a saved version **with your current text in the editor**,
- **restore** an earlier version – your current text is saved as a new version first, so nothing is lost.

In addition, bun.ink creates **automatic versions** in the background – entirely without you doing anything. This happens gently and only when it's worthwhile: typically when you're taking a short writing break, when something has noticeably changed since the last snapshot, and when enough time has passed since the last automatic version (on the order of about ten minutes). That creates a safety net along the way, in case you forget to save a version yourself. In the history, such entries are labelled **Automatic**, and manually created ones **Manual**.

The number of manually created versions is deliberately limited: you can save **up to ten versions** per document. Once that limit is reached, you simply delete a version you no longer need to make room for a new one. **Automatic versions don't count towards this** and are never blocked – they're an additional safety net, not a substitute for deliberately saving important states.

One note: the history always refers to the main state of your document. In branch mode it isn't available – branch states belong on GitHub (see [GitHub workflow](/blog/using-github-with-bun-ink)).

So even without GitHub, you get a simple, traceable version history directly in bun.ink.

## What happens when you close, log out, or get auto-logged out?

An editor doesn't just need to be able to save. It also needs to warn you when you're about to lose unsaved work.

If you close a tab or want to log out even though new changes have been made since the last save, bun.ink should point this out to you. The editor recognises that the current content hasn't been saved yet and gives you the chance to save first or deliberately continue with the action.

The **auto-logout function** is similarly important. When it's enabled, it protects your account by automatically logging you out after a certain period of inactivity. So that nothing is lost in the process, bun.ink automatically saves all open changes to your account's local cloud storage before the automatic logout – otherwise those changes would be lost when you're logged out. A GitHub push, however, doesn't happen. You can switch the auto-logout function on and off under **Settings** in the **Security** section.

Even so, it makes sense to save manually at regular intervals, especially during longer writing sessions – and particularly when you're working on a GitHub branch, where your changes only really arrive there via commit and push.

This is exactly where a clear rule of thumb applies: **on a GitHub branch, only committing and pushing to GitHub truly saves your work.** Until then, branch changes exist only locally in that browser. In the event of a logout, a browser crash or an accidentally closed tab, only the states of a branch that have already been **pushed** are safe – anything not yet pushed can be lost. So go ahead and push more often than you think you need to: pushing too much is practically impossible.

## An editor that quietly thinks along

The TipTap editor in bun.ink isn't just a text field. It combines a pared-down writing surface with Markdown, shortcuts, zen mode, the stealth function, local versions and a saving model that supports both local cloud texts and GitHub branches.

It works best when you think of it not as a toolbox full of buttons, but as a writing space with a few well-placed switches. Some of them you'll use every day. Others you'll only need in special moments. But they're there – hidden enough not to disturb you, and close enough to protect your writing flow.
