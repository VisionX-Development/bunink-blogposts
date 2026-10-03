---
title: Why Your Writing Deserves a Repository — and What bun.ink Does With It
date: 2026-07-15
description: The story behind bun.ink – why texts deserve a repository, what that has to do with AI agents, and what a writing workflow looks like when no version ever gets lost again.
sourceHash: 07989b0ec8e517de51e8923c21b65498a005139a23099eb7c90e2e722d6a75da
---

bun.ink grew out of a simple observation: the most powerful tools for versioning and collaborating on text have been around for ages. They're called Git and GitHub, and developers have been using them for decades — but anyone who wanted to use them for their own writing had to live in the terminal. Writing apps, on the other hand, feel wonderful, yet treat a text's history as an afterthought: only the current state ever exists, and everything before it is gone or buried in duplicates and "Versions" menus.

bun.ink closes exactly that gap: a writing app in the browser that feels like a modern editor — and versions your texts as Markdown in a GitHub repository. No terminal, no prior Git knowledge required.

## Writing app up front, repository behind the scenes

In bun.ink you write like you would in any good writing app: a focused editor, formatting, [text snippets](/blog/text-snippets-for-fast-writing), [writing statistics](/blog/writing-statistics-that-motivate). The difference lies underneath:

- **Every document is Markdown** – an open format that belongs to you. No lock-in, no proprietary file format.
- **Saving creates commits, branches are versions of your text** – every saved version is preserved, and you can try out radical rewrites on a branch of their own while the main version stays untouched. We explain the complete workflow in [Using GitHub the right way](/blog/using-github-with-bun-ink).
- **Everything runs in the browser**, [including on your smartphone](/blog/using-bun-ink-on-mobile), and your data is stored in Europe.

If terms like commit, branch and merge don't mean anything to you yet: in [Git and GitHub made simple](/blog/git-and-github-for-writers) we've written them up calmly and without programmer jargon. Here, we want to look at why we built all of this in the first place.

## The real reason: your texts become AI-ready

Beyond versioning, there's a second, more current reason why texts belong in a repository: **AI agents today work on repositories.**

Tools like Claude Code or GitHub Copilot can read an entire repository, suggest changes and hand them back as a pull request. If your texts live in GitHub, that suddenly applies to your book manuscript, your documentation or your collection of articles too:

- An agent reads your entire manuscript and checks for consistency across all chapters.
- A revision arrives as its own branch – you compare it line by line with your version and keep only what convinces you.
- None of it ever overwrites your text. You remain the author; the agent makes suggestions.

A Word document can't do that. A repository can. bun.ink makes the repository usable for people who write. How to put an agent to work with clear rules and an `AGENTS.md` without giving up control is shown in the article [AI as a Controlled Writing Partner](/blog/ai-controlled-writing-partner).

## Who we're building for

bun.ink is for people who write and whose texts matter enough to them to deserve real versioning: technical writers and documentation teams, developers with writing projects, Markdown fans — and anyone curious about what happens when you hand a manuscript to an AI agent without giving up control.

You can [try bun.ink free for 14 days](/signup) – no credit card required. And because everything is Markdown in your own GitHub repository, your texts belong to you on day 1 just as much as on day 1000.
