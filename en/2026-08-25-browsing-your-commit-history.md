---
title: The Commit Browser – Browsing Your Text's History Across Every Commit
date: 2026-08-25
description: How the new commit browser in the Changes tab works — search through a branch's entire commit history, freely pick any two states, and understand how this differs from the familiar local comparison.
sourceHash: 1b62983a7f519ee017ea61340c68a49dfa8795643f0d8dc48b7eee1157dcaff4
---

The article [Using GitHub the right way – the versioning workflow in bun.ink](/blog/using-github-with-bun-ink) covered saving, pushing, branches, and merging. But one piece was still missing: how do you look at what has changed in a document across many commits – not just since your last save, but since the very first commit? That's exactly what the new **commit browser** in the Changes tab is for.

## What the commit browser is good for

The Changes tab normally shows you what's changed since your last save point – a single, close-up comparison. But if you've linked your project to a GitHub repository, there's a lot more in there: the complete commit history of your branch. Every commit is a save point with its own message and its own timestamp.

The commit browser makes that history usable. You pick two states from the list – say, the very first commit of your branch and the most recent one – and the changes window shows you exactly what happened to the document in between. That way you can follow the development of a chapter over weeks, instead of only seeing the last step.

## Where to find it

In the writer, open the **Changes** tab in the sidebar. Below the list of changed documents, a new section called **Commits** appears there.

The section only shows up when everything lines up:

- Your GitHub account is connected to bun.ink.
- The current project is linked to a repository.
- It's not a high-privacy project. Projects like that deliberately stay on your device only, so they have no GitHub history.
- You have an active Pro subscription or an ongoing trial – browsing commits is one of the Pro features.

If any of these requirements is missing, the section either stays hidden entirely or shows you a short line explaining why. Nothing looks like an error when really it's just a missing condition.

## Two states: A and B

Every commit in the list carries two little toggles, **A** and **B**. With them you decide what gets compared:

- **A** is always the left, older side. A is always a real commit – never your currently open, unfinished text.
- **B** is the right, newer side. B can be a commit, or the special entry **Working state**: your current text in the editor, exactly as it stands right now, even if you haven't saved or pushed it yet.

If you click on a side that's already selected on the other side, the two sides simply swap places – the comparison is never left empty. Using the section header, you can swap A and B with a single click, or reset the selection to the default.

## The default: first commit against the most recent one

When you open the commit browser, a sensible selection is already in place: **A is the first commit of your branch, B is the most recent one**. That's exactly the case that matters most of the time – the whole journey from where the branch started to where it stands today. So you don't have to set anything up to get this big-picture view; but you can change the selection to any two other commits at any time.

If you're working on the main branch (`main`), there's no branching-off point – there, the oldest loaded commit simply takes the place of the branch start.

## What exactly gets compared

The comparison always refers to the document you currently have open – not the whole project. That keeps the view fast and clear, even with a long history. An overview of all the files a commit changed is planned for later.

A few honest edge cases you might run into:

- If the document didn't exist yet in the older commit, the view shows that as "fully added" – not an error, just a normal result.
- If a file was renamed between A and B, the commit browser doesn't yet recognize it as the same file. That's intentional, rather than showing an uncertain guess.
- If a selected commit disappears – after a force push, for example – bun.ink reloads the list and lets you know.

## The difference from the local comparison

This is the most important point for placing the commit browser correctly. The Changes tab already offered several kinds of comparisons before, and they answer different questions:

- **Local comparison** (the default): puts your most recently saved state next to your current state in the editor. That's always just **one** step, and always the very nearest one – "what have I changed since a moment ago?"
- **GitHub comparison**: puts the saved main state next to your current state – or, in branch mode, the main state next to your branch.
- **Version comparison**: puts a single saved version you've chosen next to your current state.
- **Commit comparison** (new, the commit browser): puts **two freely chosen points from the entire commit history** next to each other – not just the last step, but any stretch in between. Commit three against commit seventeen, the first commit against today's state, two months of work in a single diff.

In short: the local comparison always looks only at the next step. The commit browser opens up the whole timeline and lets you choose which slice of it you want to see.

## Viewing only – for now

In this first version, the commit browser is deliberately for viewing only. There's no "restore this state" directly from the comparison. Restoring individual versions already exists elsewhere – for commits, that will come later, with its own carefully thought-out rules for branches.

## A tool for the big picture, not for everyday work

For most save points, the familiar local comparison is entirely enough. The commit browser is meant for those moments when you want to look back: how has this chapter developed since the first draft? What happened between two important milestones? The answer is now just two clicks away – without you having to open GitHub yourself.
