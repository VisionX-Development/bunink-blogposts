---
title: Why Your Writing Deserves a Repository — and What bun.ink Does With It
date: 2026-07-15
description: The story behind bun.ink and how it works under the hood – Markdown in your own GitHub repository, commits as deliberate versions, and revisions from people or AI agents that you decide on passage by passage.
sourceHash: a019742fe58605b6ddd9cd5fa5d8b41583f8b84126cef6069a30df1a9f6f1683
---

bun.ink grew out of a simple observation: the most powerful tools for versioning and collaborating on text have existed for ages. They're called Git and GitHub, and developers have been using them for decades — but anyone who wanted to use them for their own writing had to live in the terminal. Writing apps, on the other hand, feel wonderful, yet treat a text's history as an afterthought: only the current state ever exists, and everything before it is either gone or buried in duplicates and "Versions" menus.

bun.ink closes exactly that gap: a writing app in the browser that feels like a modern editor — and that versions your texts as Markdown in a GitHub repository. No terminal, no prior Git knowledge required.

## Writing app up front, repository behind

In bun.ink you write like you would in any good writing app: a focused editor, formatting, [text snippets](/blog/text-snippets-for-fast-writing), [writing statistics](/blog/writing-statistics-that-motivate). The difference lies underneath:

- **The file is Markdown, and it belongs to you.** What gets saved isn't some proprietary format, but exactly the `.md` file that sits in your repository. If you stop using bun.ink, you still have your texts — on GitHub and as a ZIP export.
- **A commit is a deliberate version.** Saving secures your current state in bun.ink, with a version history for each document. Whatever you want to put on record becomes a commit with a message in your repository. Branches are versions of your text: you can try out a radical rewrite on its own branch while the main version stays untouched. We explain the whole process in [Using GitHub the right way](/blog/using-github-with-bun-ink).
- **The history is readable.** In the [Commit Browser](/blog/browsing-your-commit-history) you can compare any two states — two commits, or a commit against your current text — as text, not as diff syntax.
- **Everything runs in the browser**, [including on your phone](/blog/using-bun-ink-on-mobile). bun.ink itself runs in Frankfurt; whatever you push to GitHub lives in your GitHub account.

If terms like commit, branch and merge don't mean anything to you yet: in [Git and GitHub made simple](/blog/git-and-github-for-writers) we've written them up calmly and without programmer jargon. Here, we want to talk about why we built all of this in the first place.

## The real reason: your texts become AI-ready

Beyond versioning, there's a second, more current reason why texts belong in a repository: **AI agents work on repositories today.**

Tools like Claude Code or GitHub Copilot can read an entire repository, propose changes and hand them back as a pull request. If your texts live in GitHub, that suddenly applies to your book manuscript, your documentation or your collection of articles too:

- An agent reads your whole manuscript and checks for consistency across every chapter.
- Its revision — or the one from your editor — arrives as a pull request. bun.ink shows it to you **passage by passage**: accept, reject, or put your own wording up against it. Anything you reject goes back to the pull request as a commit, and nothing is merged until every passage has been decided. What that looks like day to day is described in [The Editor Comes to the Text](/blog/reviews-as-pull-requests).
- None of this ever overwrites your text. You remain the author; the agent makes suggestions.

A Word document can't do that. A repository can. bun.ink makes the repository usable for writers. How to put an agent to work with clear rules and an `AGENTS.md` without giving up control is covered in [AI as a Controlled Writing Partner](/blog/ai-controlled-writing-partner).

Since August 2026, there's one more reason. Anthropic marks text from new Claude models worldwide with an invisible watermark — prompted by the transparency obligations under Article 50 of the EU AI Act. The marking doesn't distinguish between a model writing a whole paragraph and a model merely adding commas. It tells you *that* a model was involved, not *who* did the writing. Only the process of creation shows that: a commit history in which a chapter grows in small steps over weeks. More on this in [Proving Your Work](/blog/proving-you-wrote-it-yourself).

## Under the hood

For everyone who wants to know what they're getting into:

- **Markdown is the single source.** The editor (TipTap on ProseMirror) reads Markdown and writes Markdown. Frontmatter, HTML comments, tables and hard-wrapped paragraphs come back byte for byte when you save, and simply opening a file changes nothing. Anyone opening an existing docs repository won't be greeted by a diff full of blank lines and backslashes. Notes attached to a passage live in the file as `<!-- bun.ink:note -->` and are invisible in every other view — see [Metadata and Notes](/blog/metadata-and-notes-in-markdown).
- **Two storage locations, cleanly separated.** The main version lives in bun.ink, with a version history. A branch runs in your browser and is saved as a commit directly to the GitHub branch — never into the bun.ink database.
- **GitHub via the REST API.** bun.ink talks to GitHub as an OAuth app, and you can connect several accounts per person. Access tokens are stored encrypted with AES-256-GCM on the server, never in the browser.
- **Encryption in two layers.** Content is stored server-side in the database, encrypted with AES-256-GCM. For texts nobody should be able to read, there are high-privacy folders and projects: encryption happens in the browser, the key is derived from your passphrase using Argon2id, and there's a recovery key. We can't read that content, and it never goes to GitHub. Details in [How bun.ink protects your texts](/blog/how-bun-ink-protects-your-texts).
- **Built with** SvelteKit and Svelte 5; accounts and data with Appwrite in Frankfurt.

## Who we build for

bun.ink is for people who write and whose texts matter enough to them to deserve real versioning: technical writers and documentation teams, developers with writing projects, Markdown fans — and anyone curious about what happens when you entrust a manuscript to an AI agent without giving up control.

You can [try bun.ink free for 14 days](/signup) — no credit card required. And because everything is Markdown in your own GitHub repository, your texts belong to you on day 1 just as much as on day 1000.
