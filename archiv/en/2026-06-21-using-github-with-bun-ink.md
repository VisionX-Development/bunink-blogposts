---
title: Using GitHub the right way – the versioning workflow in bun.ink
date: 2026-06-21
description: From a free GitHub account to your first repository and on to the complete branch, commit and sync workflow in bun.ink – explained step by step, without the jargon.
sourceHash: 444f96e910a66407d3b96f93eb53400faf51df411b960eab28e653f55ad92e8c
---

In [Git and GitHub made simple – version control for writers](/blog/git-and-github-for-writers), we tackled the big question: what are Git and GitHub, and why are these tools so useful for writers in particular? This post picks up exactly where that one left off and gets practical. It's no longer about the what, but about the how: the hands-on workflow for versioning your documents via GitHub – straight from bun.ink.

If terms like repository, branch or commit still don't mean much to you, it's best to read the previous article first. Here we assume you have a rough idea of them, and we'll walk you through the process step by step.

## A free GitHub account is all you need

For this kind of version control you'll need a GitHub account – and that's free. You don't have to provide payment details, enter a credit card or sign up for a paid plan. A regular, free account is entirely sufficient for the workflow described here.

Here's how to get started in just a few minutes:

1. Go to [github.com](https://github.com) and click **Sign up**.
2. Enter an email address, a password and a username.
3. Confirm your email address using the link GitHub sends you.
4. Done – you now have a free GitHub account.

That's all you need to begin. The first repository comes next.

## Creating your first repository

A **repository** is the place where GitHub stores your files and their version history. Think of it as a project folder with a built-in memory: it remembers every saved version.

One thing that helps to understand: in bun.ink, a repository sits at the same level as a **Project**. All the documents belonging to one writing project go into exactly one repository. You can create as many repositories as you like – one per book, per article series or per client, for example – but the documents of a single, coherent project are best kept together in one repository.

Here's how to create your first repository on GitHub:

1. Click the **+** in the top right, then **New repository**.
2. Give the repository a **name**.
3. Choose its visibility (more on that in a moment).
4. Click **Create repository**.

There are a few rules for the name: letters, numbers, hyphens, underscores and dots are allowed. Spaces are not – so instead of `My Novel` you'd write something like `my-novel`. The name has to be unique within your account.

## Private or public? Choose private

When creating a repository you decide whether it's **private** or **public**. This difference matters:

- **Public** means anyone on the internet can see the contents.
- **Private** means only you (and people you explicitly invite) can see them.

bun.ink displays both kinds and can work with either. But be clear about the difference: a public repository is visible to everyone, a private one only to you. For your own writing, the clear recommendation is therefore: **private**. That way your work stays protected until you actively decide to share something.

## What GitHub feels like on its own – and why bun.ink makes it easier

Through the **GitHub dashboard** in your browser you can in principle view and even edit every file that's synced with GitHub. At first glance, though, it feels cumbersome, because GitHub comes from the programming world and brings a few technical quirks with it.

Folders are a good example. On GitHub you can't simply "create a new folder". Folders there are so-called **paths**, which only come into being through a file. So if you want to create a folder, here's how:

1. Click **Add file**, then **Create new file**.
2. In the name field, enter a path – for example `docs/myfile.md`.
3. The `/` in the name tells GitHub to automatically create the `docs` folder and put the file inside it.

You can't create an **empty** folder on GitHub – a folder only exists as long as there's at least one file in it.

Branching projects is possible on GitHub too: there's a main trunk (usually called `main` or `master`), and you can create as many side branches – **branches** – as you like, each of which you have to name.

Editing via bun.ink is deliberately more intuitive and simpler. We're well aware that not every single Git capability is represented in bun.ink – that's by design. For instance, while editing a branch in bun.ink you can't create new folders or documents. New folders have to be created on the main trunk (`main`) first; after that they can be edited on the side branches as well. What might look like a limitation at first actually makes the workflow considerably easier, because the project structure stays stable and clear across all branches.

## Getting started in bun.ink: linking a project and a repository

For bun.ink to work together with GitHub, there needs to be a connection between a **Project** in bun.ink and a **repository** on GitHub. You start in the editor, in the sidebar under **Files**:

- Select an existing project **or** create a new one.
- Alternatively, you can open an existing GitHub repository directly as a new project.

You trigger the link itself via the **Link repository** button. bun.ink then asks whether you want to **open the repository as a new project** or **link it to the currently open project**. After that, bun.ink lists all your repositories – public and private alike – and you pick the right one.

### A one-time step: granting access via the OAuth app

For the exchange between bun.ink and GitHub to work, a one-time authorisation is required. bun.ink is built by the development company **VisionX Development**, and a so-called **OAuth app** runs through their GitHub account. This app needs your permission to access your GitHub account so that bun.ink can communicate with your repositories on your behalf – that is, read and write files.

The first time you connect, you'll therefore be taken to GitHub to confirm the access. This is a normal, transparent process: you can see which permissions are being granted, and you can revoke that authorisation at any time – in your GitHub settings or directly in bun.ink under **Settings** → **GitHub**, where you can also disconnect a linked account.

## The bun.ink workflow at a glance

Once a project is linked to a repository, you can version your work conveniently from within bun.ink. Here are the most important building blocks – deliberately kept simple.

### Saving and committing

When you save changes, bun.ink asks where they should go. When pushing to GitHub, you enter a **Commit message**. A commit is nothing more than a deliberately set save point with a short description of what you've changed. So you don't have to think about it every time, bun.ink suggests the **current date and time** as the default message (in the format `21.06.2026 14:30`). You can simply accept that suggestion or replace it with something more meaningful, such as "Revised chapter 2".

### Pushing

**Pushing** means uploading your committed changes from bun.ink to GitHub. Only after the push have they arrived in your repository and become part of the version history. When saving, you have several options: push to the current branch, create a new branch and push there, or just save locally for now without pushing.

### Creating and editing branches

A **branch** is a side branch of your project where you can try something out without changing the main trunk. In bun.ink you create a branch in a couple of clicks and give it a name. While you're working on a branch, bun.ink makes that clear with a **Branch mode** indicator.

One important point: changes on a branch do **not** end up in the bun.ink database, because only the main trunk is stored there. Branch states belong on GitHub. So when saving on a branch, you choose whether to commit and push to GitHub – or whether you'd also like to save the current state as a bun.ink version. And as mentioned above: new folders and documents are only created on the main trunk, not on a branch.

### Merging

**Merging** means bringing a branch's changes back into the main trunk. Once your side branch is finished and you're happy with the result, you combine it with the main trunk via **Merge into main**. bun.ink makes sure the branch has been cleanly saved to GitHub beforehand; if not, you'll be asked to take care of that first.

### Seeing and syncing changes

The **Changes** area shows you what needs doing: your own changes that haven't been pushed yet on the one hand, and incoming changes from GitHub on the other. The diff view lets you see the difference from the GitHub state at any time.

The **sync logic** is kept deliberately simple: if GitHub has new changes, bun.ink asks you to sync first before pushing again. Incoming changes are applied automatically as long as they don't overlap with your own. Where the same file has been changed both locally and on GitHub, a **Conflict** arises – and you resolve it quite deliberately, file by file: take the GitHub version, keep your own version, or preserve both as separate files. That way no changes are lost without you noticing.

## What's been added since

The workflow above is the core. Since this article was written, a few more building blocks have been added:

- **Multiple GitHub accounts.** You can connect more than one account, for example a personal one and one for work. Each project remembers which account it uses to talk to GitHub. You can connect and disconnect accounts under **Settings** → **GitHub**.
- **Leafing through your history.** The Commit Browser lives in the **Changes** area: you pick two states – two commits, or a commit and your current text – and see the differences as text. More on this in [The Commit Browser](/blog/browsing-your-commit-history).
- **Reviews as a pull request.** An editor or an AI agent works on a separate branch, and you decide passage by passage what makes it into your text. How that works is described in [The Editor Comes to the Text](/blog/reviews-as-pull-requests).

## The focus stays on the writing

Behind the scenes, GitHub brings powerful version control – with all its technical possibilities, but also with a few hurdles. bun.ink takes exactly those hurdles off your hands: you work in a tidy writing environment, and versioning, branching, merging and syncing happen through clear, simple steps.

That gives you the security of professional version control without its complexity – and the focus stays where it belongs: on the writing.
