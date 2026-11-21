---
title: Git and GitHub made simple – version control for writers
date: 2026-06-18
description: What Git and GitHub actually are, in plain language – and why these tools from the programming world turn out to be surprisingly useful for writers.
sourceHash: 31bbfa11d821afcf73b230116a8bf83f98ebc4943c27dc97b6d404b3223bbc3e
---

If you've ever worked on a longer text – a novel, a piece of reporting, a non-fiction book – you know the feeling: you've rewritten a paragraph three times, yesterday there was a version you liked better, but you saved over it long ago. Or you have `manuscript_final_v3_really_final.docx` sitting next to six similarly named files and you no longer know which one is current.

There has long been a tool for exactly this problem – it just used to come almost exclusively from the world of programming. It's called **Git**. In bun.ink we've built it in so that you can use it without writing a single line of code. This article explains, calmly, what it's all about.

## What is version control?

Imagine your text had a perfect memory. Every time you said "right, this state matters to me," it would take a snapshot. Weeks later you could look at any of those snapshots again, compare what had changed, and return to an earlier state if you needed to – without anything getting lost.

That is **version control**: a seamless, ordered history of your text. Not twelve files with cryptic names, but _one_ document with a timeline.

## Git – the memory

**Git** is the program that keeps this history. It runs in the background and remembers every version you deliberately save. Three terms come up again and again:

- **Commit** – a single snapshot. When you make a commit, you're essentially saying: "Please hold on to this state forever." Each commit gets a short note so you'll know later what you changed – for example, _"shortened chapter 3."_
- **Repository** (or _repo_ for short) – the folder that holds your project together with its entire history. A repository is simply your book _plus_ the memory of every version.
- **Branch** – a parallel storyline. More on that in a moment.

One important point: Git never throws anything away. Even if you delete a whole paragraph and save – it stays findable in the history.

## Branch and merge – experiment boldly, without fear

Probably the most useful idea for writers is the **branch**.

Say your manuscript is in solid shape, but you find yourself wondering: _What if I told the story in the present tense instead of the past?_ A big change. You want to try it without putting your good version at risk.

With a branch you create a side strand for this – a working copy in which you experiment freely. Your main strand (usually called **main**) stays untouched. If you don't like the experiment, you discard the branch and nothing has happened. If you do like it, you bring both strands back together. This bringing-together is called a **merge**.

Here's an image for it: your text is a river. A branch is a side channel you dig to test a different route. The **merge** is the point where you let the side channel flow back into the main river.

## So why GitHub on top of that?

Git runs on your device. **GitHub** is an online service that keeps your repositories safely stored on the internet. You gain three things from it:

1. **Backup** – your text and its entire history sit protected in the cloud. If you lose your laptop, the work isn't gone.
2. **Available anywhere** – you pick up in the morning at your desk where you left off in the evening on the sofa.
3. **Collaboration** – an editor or a co-author can work on a branch of their own, and you bring your versions together in an orderly way.

In short: **Git** is the memory, **GitHub** is the safe, shared place where that memory lives.

## Why this matters for writers

These tools were built for software – but the problem they solve is, at heart, a writing problem: _How do I keep track of a text that's constantly changing, and how do I try new things without losing the good ones?_

- You can **cut radically**, because you know the deleted material isn't lost.
- You can write **two endings** for your story and compare them side by side.
- You can see **in black and white** what changed between two versions.
- You never have to fear saving again.

In bun.ink, all of this happens in the background. You write as usual – version control is simply there when you need it. You don't have to install Git or learn any commands. Terms like _commit_, _branch_, and _merge_ show up in the right places, and now you know what they mean.

In future articles we'll take a closer look at individual features. Until then: write boldly – your text no longer forgets a thing.
