---
title: Proving Your Work – What the AI Watermark Doesn't Tell You
date: 2026-09-20
description: Since this summer, AI-generated texts have carried an invisible watermark — even when all that happened was a spell check. Why this leads to false accusations, and how your commit history proves that a text is yours, sentence by sentence.
sourceHash: a8abab2153bb0d25987e55447e4ce97bb33200aff9d37b4da34fd136efe31d9e
---

A while back we described here how AI can be used as a
[controlled tool](/blog/ai-controlled-writing-partner): with clear
rules and an agent that checks and suggests, while we as authors make the decisions.

This article is about a question that arises regardless: how do you prove that a text is your
work?

How someone deals with AI is a personal decision, and this article won't make it for anyone.  
Without passing judgement, and in rough and simplified terms, there are three camps: the first camp are those who never use AI; the second camp are those who have AI produce everything — whole scenes, chapters and books; the third group sits exactly between the first and second camp — these authors write every sentence themselves but use AI tools for spell-checking, revision or style analysis.

When it comes to the question of proof, one's attitude towards AI matters surprisingly little. Because the answer doesn't lie in the finished text. It lies in how it came about — more precisely, in the process of its creation. And that process is exactly what the versioning of a text records, and in bun.ink it happens without any extra work.

## The new problem: proving a negative

Anyone who delivers a text increasingly has to be able to prove something that nobody had to prove until recently: that they wrote it themselves and not a machine. Publishers want guarantees, editorial offices write corresponding clauses into contracts. The tools used to check this are still of little use today: AI detectors guess based on surface features and are regularly wrong — Moby-Dick, Herman Melville's 1851 classic, was recently flagged by an AI detector as having been written by an AI.

The core problem: the line between human and machine in text production is becoming ever blurrier. A text on its own is, first of all, an open result. The difference between human and machine lies in how it came about — and that is normally gone the moment the file is saved. Machine-generated text, on the other hand, almost never carries information about its own origin.

## Your own text, someone else's tools

So what happens to authors who write every sentence themselves but use a spelling or
grammar checker or a digital editing tool? What happens to authors who use excerpts from an AI agent's research?

All of these tools have long been using language models under the hood, and you often can't tell from the outside. Someone who accepts a grammar correction doesn't feel like they're writing with an AI. And yet, at some point, a machine has been over the text. And since this summer, that has become a problem.

## The watermark is no longer a distant prospect

Since the summer of 2026, the major providers have been embedding an invisible watermark in the text their models generate. At Anthropic, some models have carried it since 2 August 2026, with the rest due to follow by 2 December 2026. It can't be switched off. Behind this stand the
transparency obligations of European AI law. Other providers will have to go the same way.

What matters is where this marking shows up: **every tool that uses such a model in the background leaves it behind** — including the spell checker. And the watermark is a statistical property of the text that sits in the words themselves. It can't simply be removed. It survives copying, pasting, reformatting — and only disappears once the passage is completely rewritten.

## What a watermark says — and what it doesn't

For the group that "only" uses AI tools, this is a problem. The marking is very crude. It proves that a model was involved — but not that it wrote the
text. Anthropic says so clearly itself: it does not distinguish between
written, revised, translated and summarised. Someone who has their own text proofread gets the same marking as someone who had a whole chapter or book generated. In the eyes of an outside reader who doesn't know and can't trace how the text came about, groups 2 (AI only) and 3 (AI tools) are now treated as one and the same.

On top of that comes the real annoyance: **you can't check it yourself.** Detection is so far
only available to authorised bodies — authorities, media, research. There is no public tool with
which you could refute an accusation.

From this follows the sentence this article revolves around: if someone accuses you of your text being "from
the AI", you don't refute that by pointing at the finished text. Your proof is not the
result. In future, your only possible proof will be much more the path that led there.

Anthropic explains the current state of the watermark in its
[help article on marking AI-generated content](https://support.claude.com/en/articles/16266773-how-claude-marks-ai-generated-content).

## What a version history contains besides the text

And this is exactly where versioning happens to do something it was never actually designed for in the past. When you work in
bun.ink, you don't save a file that overwrites itself; you create
save points — commits that record what the text looked like, when that was and what you noted
down. What commits, branches and repositories mean is explained in
[Git and GitHub made simple](/blog/git-and-github-for-writers).

This creates a second "story" alongside your text, one nobody deliberately writes: the story of how it came to be. When the first paragraph appeared, which sentence stood unchanged for three weeks, where you discarded a scene and later picked it up differently. This second layer is
the proof of your work — and it comes into being on the side, while you simply get on with writing.

## The timeline: when each sentence came into being

In the Writer you can read this history too. In the Changes tab there's the **Commit Browser**: a
list of all save points, each with a timestamp and a message. You pick two states — say the
first commit and today's — and see every change on a branch highlighted in between. Described in detail
in [The Commit Browser](/blog/browsing-your-commit-history).

So if someone asks you whether chapter 7 is really yours, you don't have to protest. You can  
show the forty save points it grew out of.

## Why micro-steps are more convincing than a finished chapter

The real proof doesn't lie in a single commit, but in the **shape** of the history.
Human writing is crooked: one paragraph grows over a week in seven steps, another
appears in twenty minutes and is cut in half the next day. There are days with four hundred words
and days with forty, sentences that get rearranged three times, deletions, pauses, returns.

That's exactly what a grown commit history contains — and exactly what's missing when a chapter shows up in
a single step: complete, without a single revision afterwards. A text that comes into being
this way was either created elsewhere or generated. Both look different from
a text that a human has worked on.

The smaller your saves, the denser this evidence becomes. With bun.ink that's no longer extra effort;
it's the way of working that helps you go back anyway.

## Before and after: what the history reveals about the tool

For the third group this becomes very concrete. Your history contains the paragraph **before** the
tool touched it: Tuesday evening's commit shows your version, Wednesday morning's
shows what the correction made of it. In between lies a comparison anyone can read —
a comma, two words swapped around. And yes, making mistakes, e.g. spelling mistakes, is very useful here, even if it's easy for an AI to find and correct them.  
 And yes, making mistakes, e.g. spelling mistakes, is very useful here, even if it's easy for an AI to find and correct them.

This shifts the question from "is there machine in there?" to "what exactly did it do?". You
don't prove that no tool was ever involved — since this summer you can't do that
anyway. You prove authorship: that the text is yours and that a tool touched it at the edges,
not in substance.

In practice that means: **one commit before using the tool, one commit after.** Ten seconds of effort —
and the line between your work and the correction is permanently documented. Because the
marking can't be washed out and you can't check it yourself, your history is the
only piece of evidence that belongs to you.

## Statistics make it visible

What's in the history can also be looked at rather than read. The
[writing statistics](/blog/writing-statistics-that-motivate) in the Writer show your work as numbers
and pictures: words per day and week, active writing time, a heatmap over twelve months. For
projects with a repository, commit activity is added on top.

A year of writing looks in there like a year of writing just does: uneven, with gaps and dense phases before deadlines — not like three afternoons in which a book appeared.  
The statistics count you, not your text: word counts and times are recorded, no  
content.

## GitHub as an impartial witness

Up to this point everything sits with you — and anything that sits with you could, in case of doubt, have been staged by you. The final step turns it into something that holds up: if your project is linked to GitHub,
your commits end up with a third party that has nothing to do with your text. How that
works is described in [Using GitHub the right way](/blog/using-github-with-bun-ink).

A timestamp you set yourself is a claim. A timestamp on the GitHub server is more like proof. You grant access as coarsely or finely as you like — invite one person, open up the repository, or export the commit list. "I wrote this myself" becomes "here are the 312 steps, with dates and the content of the corresponding changes".

Of course, a grown commit history is not forensic proof. With enough  
effort it could be staged, including by an AI agent. What versioning achieves is more modest but useful nonetheless: it  
shifts the question from "does the text look human?" to "is there a coherent trail of work that grew over weeks?". That's the better question, and this is how you can answer it.

## And what about the security of your texts?

In connection with the well-known large language models, another question unfortunately always comes up: *does my manuscript end up in some training data set somewhere?* At  
bun.ink the answer is short. The app sends your texts neither to a language model nor to anyone else unless you want it to. In the [bun.ink](http://bun.ink)  
database, text entries are not stored as readable plain text but encrypted. How that works in detail is described in [How bun.ink protects your texts](/blog/how-bun-ink-protects-your-texts).

Using versioning via GitHub — in the sense described above — is something you have to explicitly agree to. Of course you can also use [bun.ink](http://bun.ink) without GitHub. The High Privacy folder in particular can only be used without GitHub. Nobody else can then read or change your texts. But the advantage of absolute privacy comes with the disadvantage of missing version control — and, in case of doubt, the loss of proof of the work you've done.

## What you can do to document your work

If this kind of proof matters to you, a few habits are worth building:

- **Start early.** The history begins with the first commit, not with the finished manuscript.
- **Save small.** Better five commits in one afternoon than one at the end of the month.
- **Write honest messages.** "Dialogue shortened, flashback cut" says more than "Update".
- **Leave the detours in.** Discarded versions are not a flaw, they are the evidence.
- **Frame your tools.** Save once before and once after every pass through a correction tool.
- **Keep the agent separate.** Larger AI work belongs on its own branch and under the agent's own account — that distinction is half the proof.
- **Revisions, even when working alone.** What you discarded stays documented along with the reasoning — how that works is described in [The Editor Comes to the Text](/blog/reviews-as-pull-requests).

## Finally: an open book, in both directions

A fair warning at the end: what's described here as proof works in both  
directions. A version history that shows a chapter grew in forty steps  
equally shows that another one stood there finished in a single step. Anyone working with AI leaves  
a recognisable trail in the history — but since this summer there's an additional one in the text itself.

For most people that's not a problem: whoever discloses their tools has nothing to hide, and a
well-kept repository even shows what was suggested and what was accepted — exactly the
idea behind the article on the [controlled writing partner](/blog/ai-controlled-writing-partner).

Because that's the price and the value of one and the same thing: with bun.ink, the process behind a  
text is a proverbial open book. Those who write every line themselves find in it the proof they will come to depend on. Those who only have their work corrected find the difference between "a machine was involved" and "here's what it did". Those who work with AI learn the truth about their way of working. The one thing the writing process no longer is, is invisible.
