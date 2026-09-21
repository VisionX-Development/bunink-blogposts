---
title: Why texts deserve a repository – and what bun.ink makes of it
date: 2026-07-15
description: The story behind bun.ink – why texts deserve a repository, what that has to do with AI agents, and what a writing workflow looks like where no version is ever lost.
sourceHash: 07989b0ec8e517de51e8923c21b65498a005139a23099eb7c90e2e722d6a75da
---

bun.ink grew out of a simple observation: the most powerful tools for versioning and collaborating on texts have existed for a long time. They're called Git and GitHub, and developers have been working with them for decades – but anyone who wanted to use them for their writing had to live in the terminal. Writing apps, on the other hand, feel wonderful but treat the history of a text as an afterthought: only the current state ever exists, and everything before it is gone or buried in duplicates and "versions" menus.

bun.ink closes exactly this gap: a writing app in the browser that feels like a modern editor – and versions your texts as Markdown in a GitHub repository. No terminal, no prior Git knowledge required.

## A writing app up front, a repository underneath

In bun.ink you write like in any good writing app: a focused editor, formatting, [text snippets](/blog/text-snippets-for-fast-writing), [writing statistics](/blog/writing-statistics-that-motivate). The difference lies underneath:

- **Every document is Markdown** – an open format that belongs to you. No lock-in, no proprietary file format.
- **Saving creates commits, branches are versions of your text** – every saved draft is preserved, and you try out radical revisions on a separate branch while your main version stays untouched. We explain the full workflow in [Using GitHub with bun.ink](/blog/using-github-with-bun-ink).
- **Everything runs in the browser**, [including on your phone](/blog/using-bun-ink-on-mobile), and your data is stored in Europe.

If terms like commit, branch and merge don't mean anything to you yet: in [Git and GitHub made simple](/blog/git-and-github-for-writers) we've written them up calmly and without programmer vocabulary. Here, we want to focus on why we built all of this in the first place.

## The real reason: your texts become AI-ready

Beyond versioning, there is a second, more current reason why texts belong in a repository: **AI agents work on repositories today.**

Tools like Claude Code or GitHub Copilot can read an entire repository, propose changes and return them as a pull request. If your texts live in GitHub, this suddenly applies to your book manuscript, your documentation or your article collection too:

- An agent reads your entire manuscript and checks consistency across all chapters.
- A revision lands on its own branch – you compare it line by line with your version and adopt only what convinces you.
- None of this ever overwrites your text. You remain the author; the agent makes suggestions.

A Word document can't do that. A repository can. bun.ink makes the repository usable for writers. For how to use an agent with clear rules and an `AGENTS.md` without giving up control, see [AI as a controlled writing partner](/blog/ai-controlled-writing-partner).

## Who we're building for

bun.ink is for people who write and whose texts matter enough to them to deserve real versioning: technical writers and documentation teams, developers with writing projects, Markdown fans – and everyone curious about what happens when you entrust a manuscript to an AI agent without giving up control.

You can [try bun.ink free for 14 days](/signup) – no credit card required. And because everything is Markdown in your own GitHub repository, your texts belong to you on day 1 just as much as on day 1000.
