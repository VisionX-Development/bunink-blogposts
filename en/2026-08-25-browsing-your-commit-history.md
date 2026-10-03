---
title: The Commit Browser – Browsing Your Text's History Across Every Commit
date: 2026-08-25
description: How the new commit browser in the Changes tab works — browse a branch's entire commit history, pick any two snapshots to compare, and understand how this differs from the familiar local comparison.
sourceHash: 877260e54dc9df6abd6684ef4ae55f39924d89fc49b5be1a5eecb46ff872365e
---

In [Using GitHub the right way – the versioning workflow in bun.ink](/blog/using-github-with-bun-ink), we covered saving, pushing, branches and merging. One piece was still missing: how do you look at what has changed in a document across many commits – not just since you last saved, but since the very first commit? That's exactly what the new **commit browser** in the Changes tab is for.

## What the commit browser is good for

The Changes tab normally shows you what has changed since your last save point – a single, close-up comparison. But if you've linked your project to a GitHub repository, there's much more in there: the complete commit history of your branch. Every commit is a save point with its own message and its own timestamp.

The commit browser makes that history usable. You pick two states from the list – say, the very first commit of your branch and the most recent one – and the changes panel shows you exactly what happened to the document in between. That way you can follow the development of a chapter over weeks, instead of only seeing the last step.

## Where to find it

In the Writer, open the **Changes** tab in the sidebar. Below the list of changed documents you'll find a new section called **Commits**.

The section only appears when everything lines up:

- Your GitHub account is connected to bun.ink.
- The current project is linked to a repository.
- It isn't a high-privacy project. Those projects deliberately stay on your device only, and therefore have no GitHub history.
- Your 14-day trial is still running, or you have a subscription.

If one of these conditions is missing, the section either stays hidden altogether or shows you a short line explaining why. Nothing looks like an error when all that's really missing is a prerequisite.

## Two states: A and B

Every commit in the list carries two small toggles, **A** and **B**. They determine what gets compared:

- **A** is always the left-hand, older side. A is always an actual commit – never the unfinished text you currently have open.
- **B** is the right-hand, newer side. B can be a commit, or the special entry **Working draft**: your current text in the editor exactly as it stands right now, even if you haven't saved or pushed it yet.

If you click a side that's already selected on the other side, the two sides simply swap places – the comparison is never empty. Using the section header, you can swap A and B with a single click, or reset the selection to its default.

## The default: first commit against the most recent one

When you open the commit browser, a sensible selection has already been made: **A is the first commit of your branch, B is the most recent one**. That's the case you'll want most of the time – the whole journey from where the branch began to where it stands today. So you don't have to set anything up to get that big-picture view; but you can change the selection to any two other commits at any time.

If you're working on the main branch (`main`), there's no branch point – there, the oldest loaded commit simply takes the place of the branch start.

## What exactly gets compared

The comparison always refers to the document you currently have open – not to the whole project. That keeps the view fast and clear, even with a long history. An overview of all the files a commit has changed is planned for later.

A few honest edge cases you might run into:

- If the document didn't exist yet in the older commit, the view shows it as "fully added" – not an error, just a normal result.
- If a file was renamed between A and B, the commit browser doesn't yet recognise it as the same file. That's deliberate, rather than displaying an uncertain guess.
- If a selected commit disappears – after a force push, for example – bun.ink reloads the list and lets you know.

## The difference from the local comparison

This is the most important point for understanding where the commit browser fits in. The Changes tab already offered several kinds of comparison, and they answer different questions:

- **Local comparison** (the default): puts your last saved state next to your current state in the editor. That's always just **one** step, and always the very next one – "what have I changed since a moment ago?"
- **GitHub comparison**: puts the saved main state next to your current state – or, in branch mode, the main state next to your branch.
- **Version comparison**: puts a single saved version you've selected next to your current state.
- **Commit comparison** (new, the commit browser): puts **two freely chosen points from the entire commit history** next to each other – not just the last step, but any stretch in between. Commit three against commit seventeen, the first commit against today's state, two months of work in a single diff.

In short: the local comparison only ever looks at the next step. The commit browser opens up the whole timeline and lets you choose which section of it you want to see.

## Viewing only – for now

In this first version, the commit browser is deliberately for viewing only. There's no "restore this state" directly from the comparison. Restoring individual versions already exists elsewhere – for commits it will come later, with its own carefully thought-out rules for branches.

## A tool for the big picture, not for everyday use

For most save points, the familiar local comparison is perfectly sufficient. The commit browser is meant for those moments when you want to look back: how has this chapter developed since the first draft? What happened between two important milestones? The answer is now just two clicks away – without you having to open GitHub yourself.
