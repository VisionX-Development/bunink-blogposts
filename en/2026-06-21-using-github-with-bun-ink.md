---
title: Using GitHub the right way – the versioning workflow in bun.ink
date: 2026-06-21
description: From a free GitHub account to your first repository to the complete branch, commit, and sync workflow in bun.ink – explained step by step and without jargon.
sourceHash: d2a5dee2dd91232aca224b73a160827ec4192b0deba08c9bb27959112d39108c
---

The article [Git and GitHub made simple – version control for writers](/blog/git-and-github-for-writers) tackled the big question: what are Git and GitHub anyway, and why are these tools useful precisely for writers? This post picks up right there and gets concrete. It is no longer about the what, but about the how: the practical workflow you use to version your documents through GitHub – straight from bun.ink.

If terms like repository, branch, or commit still mean nothing to you, it is best to read the previous article first. Here we assume you have a rough idea of them, and we will walk you through the path step by step.

## A free GitHub account is enough

For this kind of version control you need a GitHub account – and it is free. You do not have to store any payment details, provide a credit card, or sign up for a paid plan. A normal, free account is completely sufficient for the workflow described here.

Here is how to get started in just a few minutes:

1. Open [github.com](https://github.com) and click **Sign up**.
2. Enter an email address, a password, and a username.
3. Confirm your email address via the link GitHub sends you.
4. Done – you have a free GitHub account.

That is all you need to begin. The first repository comes next.

## Creating your first repository

A **repository** is the place where GitHub stores your files and their version history. Think of it as a project folder with a built-in memory: it remembers every saved version.

Important for understanding: a repository has the same rank in bun.ink as a **project**. All the documents of a writing project belong in exactly one repository. You can create as many repositories as you like – for example one per book, per article series, or per client – but the documents that belong to one project sensibly stay together in a single repository.

Here is how to create your first repository on GitHub:

1. Click the **+** in the top right and then **New repository**.
2. Give the repository a **name** (more on this in a moment).
3. Choose the visibility (more on this shortly).
4. Click **Create repository**.

There are a few rules to follow for the name: letters, digits, hyphens, underscores, and dots are allowed. Spaces are not allowed – so instead of `My Novel` you would write something like `my-novel`. The name must be unique within your account.

## Private or public? Choose private

When creating it, you decide whether the repository is **private** or **public**. This difference matters:

- **Public** means: anyone on the internet can see the contents.
- **Private** means: only you (and explicitly invited people) can see the contents.

bun.ink displays both kinds and can work with both. But be clear about the difference: a public repository is visible to everyone, a private one only to you. For your own texts, the clear recommendation is therefore: **private**. That way your work stays protected until you actively decide to share something.

## What GitHub itself feels like – and why bun.ink makes it easier

Through the **GitHub dashboard** in the browser you can, in principle, view and even edit all the files that are synced with GitHub. At first glance, though, this feels cumbersome, because GitHub comes from the programming world and brings along a few technical quirks.

Folders are a good example. On GitHub you cannot simply "create a new folder." There, folders are so-called **paths** that only come into being through a file. So if you want to create a folder, you go about it like this:

1. Click **Add file** and then **Create new file**.
2. In the name field, enter a path, for example `docs/myfile.md`.
3. With the `/` in the name, GitHub automatically creates the `docs` folder and places the file inside it.

You cannot create an **empty** folder on GitHub – a folder only exists as long as at least one file is in it.

Branching projects is also possible on GitHub: there is a main trunk (usually called `main` or `master`), and you can create any number of side branches – **branches** – each of which you have to name.

Editing through bun.ink is deliberately more intuitive and simpler. In doing so, we are aware that not every single capability of Git is reflected in bun.ink – and that is intentional. For instance, while editing a branch in bun.ink you cannot create new folders or documents. New folders must first be created on the main trunk (`main`); after that they can also be edited on the side branches. What may at first seem like a restriction makes the workflow considerably easier, because the project structure stays stable and clear across all branches.

## Getting started in bun.ink: linking a project and a repository

For bun.ink to work together with GitHub, it needs a connection between a **project** in bun.ink and a **repository** on GitHub. You make the start in the editor in the sidebar under **Files**:

- Select an existing project **or** create a new project.
- Alternatively, you can open an existing GitHub repository directly as a new project.

You trigger the linking itself via the **Link repository** button. bun.ink then asks whether you want to **open the repository as a new project** or **link it with the currently open project**. After that, bun.ink lists all your repositories – public as well as private – and you pick the right one.

### One-time step: granting access via the OAuth app

For the exchange between bun.ink and GitHub to work, a one-time authorization is required. Behind bun.ink stands the development company **VisionX Development**, and a so-called **OAuth app** runs through its GitHub account. This app needs your permission to access your GitHub account so that bun.ink can communicate with your repositories on your behalf – that is, read and write files.

When you connect for the first time, you are therefore taken to GitHub and confirm the access there. This is a normal, transparent process: you can see which permissions are granted, and you can revoke this authorization at any time – in your GitHub settings or directly in bun.ink's account area, where you can also disconnect the GitHub account again.

## The workflow in bun.ink at a glance

As soon as a project is linked with a repository, you can version comfortably from within bun.ink. Here are the most important building blocks – kept deliberately simple.

### Saving and committing

When you save changes, bun.ink asks where they should go. When pushing to GitHub, you enter a **commit message**. A commit is nothing more than a deliberately set save point with a short description of what you changed. So that you do not have to think about it every time, bun.ink suggests the **current date and time** as the message by default (in the format `21.06.2026 14:30`). You can simply accept this suggestion or replace it with a meaningful description, such as "Revised chapter 2."

### Pushing

**Pushing** means uploading your committed changes from bun.ink to GitHub. Only after the push have they arrived in your repository and become part of the version history. When saving, you have several options for this: push on the current branch, create a new branch and push there, or save only locally for now without pushing.

### Creating and editing branches

A **branch** is a side branch of your project on which you can try things out without changing the main trunk. In bun.ink you create a branch with a few clicks and give it a name. While you are on a branch, bun.ink clearly indicates this with a **branch mode** notice.

One important point: changes on a branch do **not** end up in the bun.ink database, because only the main trunk is stored there. Branch states belong on GitHub. When saving on a branch, you therefore choose whether to commit and push to GitHub – or whether you additionally want to keep the current state as a bun.ink version. And as mentioned above: you create new folders and documents only on the main trunk, not on a branch.

### Merging

**Merging** means bringing the changes of a branch back into the main trunk. When your side branch is finished and you are happy with the result, you combine it with the main trunk via **Merge into main**. bun.ink makes sure the branch has been cleanly saved to GitHub beforehand; otherwise you are asked to take care of that first.

### Seeing and syncing changes

In the **Changes** area, bun.ink shows you what needs doing: your own changes that have not yet been pushed on the one hand, and incoming changes from GitHub on the other. Through the diff view you can look at the difference from the GitHub state at any time.

The **sync logic** is kept simple in concept: if GitHub has new changes, bun.ink asks you to sync first before you push again. Incoming changes are applied automatically, as long as they do not overlap with your own. Where the same file was changed both locally and on GitHub, a **conflict** arises – and you resolve it quite deliberately, per file: take the GitHub version, keep your own version, or keep both as separate files. That way no changes are lost unnoticed.

## The focus stays on writing

Behind the scenes, GitHub brings along powerful version control – with all its technical possibilities, but also with a few hurdles. bun.ink takes exactly those hurdles off your shoulders: you work in a tidy writing environment, and versioning, branching, merging, and syncing happen through clear, simple steps.

That gives you the safety of professional version control without its complexity – and the focus stays where it belongs: on writing.
