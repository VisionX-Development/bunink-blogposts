---
title: Proving Your Work — What the AI Watermark Doesn't Tell You
date: 2026-09-20
description: Since this summer, AI-generated text has carried an invisible watermark — even when all that touched it was the spelling checker. Why that leads to false accusations, and how your commit history proves a text came from you, sentence by sentence.
sourceHash: 78cbfa63a5bc3862c0289fd8ed1adf1886af0ea762c2d51ce9438fe5d03da834
---

A while ago we described here how AI can be used as a
[controlled writing partner](/blog/ai-controlled-writing-partner): with clear rules and an agent
that checks and suggests while the human decides.

This one is about a question that arises regardless: how do you show that a text is your work?

How someone handles AI is a personal decision this article won't make for anyone. Some have scenes
suggested to them and drafts reviewed. Some want none of it — out of conviction, or because a
contract rules it out. Most sit somewhere in between without having thought about it: they write
every sentence themselves and run the spell checker.

For the question of proof, that stance matters surprisingly little. The answer is never in the
finished text but in how it came to be — and that is exactly what the version control bun.ink
brings along keeps hold of.

## The new problem: proving a negative

Anyone handing in a text increasingly has to show something nobody had to show until recently: that
they wrote it themselves. Publishers ask for assurances, newsrooms add contract clauses. The tools
used to verify this are poor: AI detectors guess from surface features and get it wrong regularly —
even for people who simply write cleanly.

The core problem: who wrote a text isn't visible in the finished text. A finished text is a result,
and results look alike no matter how they came about. The difference is in how the text came to
be — and that's normally gone the moment the file is saved. Machine-generated text does carry a
mark these days; but it doesn't answer this particular question — more on that in a moment.

## The third group: your own text, someone else's tools

Of the three stances from the beginning, one gets talked about the least although it's probably the
most common: people who write every sentence themselves but use a spelling or grammar checker, or
a digital copy-editor.

You can't tell that these tools run language models under the hood. Anyone accepting a grammar
correction doesn't feel like they're writing with an AI — and they're right about that. And yet, at
one point, a machine passed over the text. That is exactly what has become a problem since this
summer.

## The watermark isn't a future problem

Since the summer of 2026, the major providers have put an invisible watermark into the text their
models generate. At Anthropic it's carried by every model released on or after 2 August 2026; the
older ones were to follow by 2 December 2026. It can't be switched off. Behind it are the
transparency obligations of European AI law, and other providers are going the same way.

What matters is where this mark turns up: **every tool that uses such a model under the hood leaves
it behind** — including the spelling checker. And it's tough: it doesn't sit in a file property but
in the word choice itself. It survives copying, pasting and reformatting, and only disappears once
a passage is rewritten from scratch.

## What a watermark says — and what it doesn't

This is where it gets uncomfortable for the third group, for a reason that has nothing to do with
bad technology: the mark is coarse. It shows a model was involved — not that it wrote the text.
Anthropic says so itself: it doesn't distinguish between written, revised, translated and
summarised. Have your own text proofread and you get the same mark as someone who had a whole
chapter generated.

On top of that: **you can't check it yourself.** Detection is open only to authorised bodies —
government agencies, media, research. There is no public tool to refute an accusation with.

Which gives us the sentence this article turns on: if someone tells you your text is "from the AI",
you don't refute it by pointing at the finished text. Your proof isn't the result. It's the path
that led there.

Anthropic explains the current state of the watermark in its
[help article on how it marks AI-generated content](https://support.claude.com/en/articles/16266773-how-claude-marks-ai-generated-content).

## What a version history holds besides the text

This is where version control does something it actually does for entirely different reasons. When
you work in bun.ink, you're not saving a file that overwrites itself — you're creating save
points, commits, that record what the text looked like, when that was, and what you noted about it.
What commits, branches and repositories mean is explained in
[Git and GitHub made simple](/blog/git-and-github-for-writers).

This creates a second text alongside yours that nobody deliberately writes: the story of how it
came about. When the first paragraph existed, which sentence stood unchanged for weeks, where you
discarded a scene and picked it up later in a different form. That second layer is the proof — it
comes into being on the side, while you simply do your work.

## The timeline: when each sentence came to be

In the writer you can read this history too. The Changes tab has the **commit browser**: a list of
every save point, each with a timestamp and message. You pick two states — say, the first commit
and today's — and see every change between them highlighted. Described in full in
[The commit browser](/blog/browsing-your-commit-history).

So if someone asks whether chapter 7 is really yours, you don't have to insist. You can show the
forty save points it grew out of.

## Why micro-steps are more convincing than a finished chapter

The actual proof isn't in any single commit — it's in the **shape** of the history. Human writing is
crooked: one paragraph grows over a week in seven steps, another appears in twenty minutes and gets
cut in half the next day. There are days with four hundred words and days with forty, sentences
rearranged three times, deletions, pauses, returns.

That is exactly what a grown commit history contains — and exactly what's missing when a chapter
shows up in a single step, complete, without a single revision afterwards. A text that appears that
way either came from elsewhere or was generated. Both look different from work.

The smaller you save, the denser this record becomes. That's not extra effort for some reviewing
authority — it's the way of working that helps you go back anyway.

## Before and after: what the history reveals about the tool

For the third group this gets very concrete. Your history contains the paragraph **before** the
tool touched it: Tuesday evening's commit shows your version, Wednesday morning's shows what the
correction made of it. Between them lies a comparison anyone can read — a comma, two words swapped.

That shifts the question from "is there machine in here?" to "what exactly did it do?". You're not
proving no tool was ever involved — since this summer you can't do that anyway. You're proving
authorship: that the text is yours and the tool touched its edges, not its substance.

In practice: **one commit before the tool, one after.** Ten seconds of effort — and the line between
your work and the correction is documented for good. Because the mark can't be washed out and you
can't inspect it yourself, your history is the only record that belongs to you.

## The statistics make it visible

What's in the history can also be looked at rather than read. The
[writing statistics](/blog/writing-statistics-that-motivate) in the writer show your work as numbers
and pictures: words per day and week, active writing time, a twelve-month heatmap. Projects linked
to a repository add commit activity.

A year of writing work looks like a year of writing work: uneven, with holes and dense stretches
before deadlines — not like three afternoons on which a book appeared. The statistics count you, not
your text: what's recorded are word counts and times, not content.

## GitHub as a disinterested witness

Up to here everything sits with you — and anything that sits with you, you could have staged
yourself. The last step turns it into something that holds up: when your project is linked to
GitHub, your commits land with a third party that has nothing to do with your text. How to set that
up is in [Using GitHub the right way](/blog/using-github-with-bun-ink).

A timestamp you set yourself is a claim; one on someone else's server is a record. You grant access
as coarsely or finely as you like. "I wrote this myself" becomes "here are the 312 steps, with
dates".

## And what about the security of your texts?

One question from the beginning has stayed open: _does my manuscript end up in a training set
somewhere?_ With bun.ink the answer is short. The app doesn't send your texts to a language model,
and in the database they aren't stored as readable plain text but encrypted. How that works in
detail is in [How bun.ink protects your texts](/blog/how-bun-ink-protects-your-texts).

Your text doesn't go anywhere — not into a training set, not as plain text into a database. What
follows from that for your record, though, has a flip side.

## An honest caveat

It is this: you can't have both at once. A high-privacy project deliberately has no GitHub
history — maximum privacy and public verifiability rule each other out. bun.ink lets you decide
that per project.

And a second caveat: a history isn't forensic proof, and could in principle be staged. What version
control delivers is more modest and still useful: it shifts the question from "does this text look
human?" to "is there a coherent working trail that grew over weeks?" — the far better question, and
it can be answered.

## What you should do for it

If this record matters to you, a few habits pay off:

- **Start early.** The history begins with the first commit, not the finished manuscript.
- **Save small.** Five commits in an afternoon beat one at the end of the month.
- **Write honest messages.** "Trimmed the dialogue, cut the flashback" says more than "update".
- **Leave the detours in.** Discarded versions aren't a blemish — they're the evidence.
- **Frame your tools.** Save once before and once after every pass through a correction helper.
- **Keep the agent separate.** Larger AI work belongs on its own branch and account — that
  distinction is half the proof.
- **Review even on your own.** What you discarded stays documented with your reasoning — see
  [The editor comes to the text](/blog/reviews-as-pull-requests).

## Finally: an open book, in both directions

A fair warning to close: this works in both directions. A history that can show a chapter grew in
forty steps can just as easily show another stood there finished in one. Anyone working with AI
leaves a recognisable trail — and, since this summer, another one in the text itself.

For most people that's not a problem: if you're open about your tools you have nothing to hide, and
a well-kept repository even shows what was suggested and what was kept — exactly the idea in the
article about the [controlled writing partner](/blog/ai-controlled-writing-partner).

Because that's the price and the value of the same thing: with bun.ink the making of a text is a
literally open book. Anyone who writes every line themselves finds in it the proof they'll come to
depend on. Anyone who only lets it be corrected finds the difference between "there was a machine
involved" and "here's exactly what it did". And anyone working with AI finds the truth about how
they work. What the process no longer is, is invisible.
