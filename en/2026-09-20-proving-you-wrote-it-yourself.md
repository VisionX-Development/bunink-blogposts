---
title: Proving Your Work – What the AI Watermark Doesn't Tell You
date: 2026-09-20
description: Since August 2026, Anthropic has been tagging text from new Claude models with an invisible watermark — whether the model wrote the piece or merely proofread it. Why that leads to false accusations, and how your commit history proves a text is yours, sentence by sentence.
sourceHash: a21d7d4f02a5f09dd1eac02eba83426119f52aa56f9b3f6bbe317481c1577b29
---

A while ago we described here how an AI can be used as a [controlled tool](/blog/ai-controlled-writing-partner): with clear rules and an agent that checks and suggests, while we as authors make the decisions.

This article is about a question that arises regardless: how do you prove that a text is your own work?

How someone deals with AI is a personal decision, and this article won't make it for anyone. Without any judgement, and broadly and simply put, there are three camps: the first camp consists of those who never use AI; the second camp are those who have AI produce everything — whole scenes, chapters and books; the third group sits exactly between the first and the second — these authors write every sentence themselves, but use AI tools for spell-checking, revision or style analysis.

When it comes to the question of proof, one's stance on AI matters surprisingly little. Because the answer doesn't lie in the finished text. It lies in how the text came about — in the process of its creation. And it is precisely this process that a text's version history records, and in bun.ink that happens without any extra effort.

## The new problem: proving a negative

Anyone who delivers a text increasingly has to be able to prove something that nobody had to prove until recently: that they wrote it themselves and not a machine. Publishers ask for assurances, editorial offices add corresponding clauses to contracts. The tools used for checking are still of little use today: AI detectors guess based on surface features and are regularly wrong — in a [test by Markus Brinsa](https://brinsa.com/moby-dick-failed-the-ai-test-or-the-test-failed-moby-dick), the detector Pangram classified roughly 44 percent of Moby-Dick, Herman Melville's 1851 classic, as AI-generated text.

The core problem: the line between human and machine in text creation is becoming ever blurrier. A text on its own is, first of all, an open-ended result. The difference between human and machine lies in how it came about — and that normally vanishes the moment the file is saved. Machine-generated text, on the other hand, almost never carries any information about its origin.

## Your own text, someone else's tools

So what happens to authors who write every sentence themselves but use a spelling or grammar checker or a digital editing tool? What happens to authors who use excerpts from an AI agent's research?

All of these tools have long been using language models under the hood, often without that being at all obvious. Accepting a grammar correction doesn't feel like writing with an AI. Nevertheless, at some point a machine has passed over the text. And since this summer, that has become a problem.

## The watermark isn't a distant prospect

Since 2 August 2026, Anthropic has been adding an invisible watermark to text from new Claude models — [according to the company](https://www.anthropic.com/news/claude-text-watermark) worldwide, because the marking can't reliably be restricted to one region. It will be retrofitted to older models over the coming months; the AI Act sets a deadline of 2 December 2026 for this in [Article 111(4)](https://ai-act-service-desk.ec.europa.eu/en/ai-act/article-111). Behind it stands the code of practice on Article 50 of the EU AI Act, which Anthropic has signed — other providers will have to go the same way.

What matters is where this marking shows up: **any tool that uses a marking model in the background can leave it behind** — including the spell-checker. The watermark is embedded in the choice of words itself. According to Anthropic, it survives light editing and copying; only when every single word is replaced does it disappear. Even a translation by Claude carries it.

## What a watermark says — and what it doesn't

For the group that "only" uses AI tools, that's a problem. The marking is very coarse. It shows that a model was involved — but not that it wrote the text. Anthropic says this clearly itself: it doesn't distinguish between written, revised, translated and summarised. Anyone who has their own text proofread gets the same marking as someone who had an entire chapter or book generated. In the eyes of an outside reader who doesn't know — or can't retrace — how the text came about, groups 2 (AI only) and 3 (AI tools) are now treated as the same.

On top of that comes the real annoyance: **you can't check it yourself.** Detection is so far only available to authorised bodies — authorities, media, researchers. There is no public tool with which you could refute an accusation.

Which leads to the sentence this article revolves around: if someone accuses you of your text being "AI-written", you won't disprove it by pointing at the finished text. Your proof isn't the result. In future, your only possible proof will much more likely be the path that led to it.

Anthropic explains the current state of the watermark in its [help article on marking AI-generated content](https://support.claude.com/en/articles/16266773-how-claude-marks-ai-generated-content), and how it works technically in [How Claude's text watermarking works](https://www.anthropic.com/news/claude-text-watermark).

## What's in a version history besides the text

This is exactly where version control happens to do something it was never actually intended for in the past. When you work in bun.ink, you don't save a file that overwrites itself; you create save points — commits that record what the text looked like, when that was, and what you noted down. What commits, branches and repositories mean is explained in [Git and GitHub made simple](/blog/git-and-github-for-writers).

As a result, a second "story" grows alongside your text, one that nobody writes deliberately: the story of how it came about. When the first paragraph appeared, which sentence stood unchanged for three weeks, where you discarded a scene and later picked it up again differently. This second layer is the proof of your work — and it emerges on the side, while you simply get on with writing.

## The timeline: when each sentence came into being

In the Writer, you can also read this history. The Changes tab contains the **Commit Browser**: a list of all save points, each with a timestamp and a message. You pick two versions — say the first commit and today's — and see every change between them highlighted. Described in detail in [The Commit Browser](/blog/browsing-your-commit-history).

So if someone asks you whether Chapter 7 is really yours, you don't have to protest. You can show the forty save points it grew out of.

## Why micro-steps are more convincing than a finished chapter

The real proof doesn't lie in a single commit, but in the **shape** of the history. Human writing is crooked: one paragraph grows over a week in seven steps, another comes together in twenty minutes and is cut in half the next day. There are days with four hundred words and days with forty, sentences that get rearranged three times, deletions, pauses, returns.

That's exactly what a grown commit history shows — and exactly what's missing when a chapter appears in a single step: complete, without a single revision afterwards. A text that comes about this way was either created somewhere else or generated. Either one looks different from a text that a human has worked on.

The smaller your save steps, the denser this record becomes. With bun.ink that's no extra effort — it's the way of working that helps you go back anyway.

## Before and after: what the history reveals about the tool

For the third group this gets very concrete. Your history contains the paragraph **before** the tool touched it: Tuesday evening's commit shows your version, Wednesday morning's shows what the correction made of it. Between them lies a comparison anyone can read — a comma, two words swapped around. And yes, making mistakes, spelling errors for example, is very useful here, even though it's easy for an AI to find and correct them.

That shifts the question from "is there machine in here?" to "what exactly did it do?". You're not proving that no tool was ever involved — since this summer, you can't do that anyway. You're proving authorship: that the text is yours and that a tool touched it at the edges, not in substance.

In practice that means: **one commit before using the tool, one commit after.** Ten seconds of effort — and the line between your work and the correction is permanently documented. Because you can't check the marking yourself, your history is the only evidence that belongs to you.

## The statistics make it visible

What's in the history can also be viewed rather than read. The [writing statistics](/blog/writing-statistics-that-motivate) in the Writer show your work as numbers and images: words per day and week, active writing time, a heatmap over twelve months. For projects with a repository, commit activity is added.

A year of writing looks there the way a year of writing simply looks: uneven, with gaps and dense phases before deadlines — not like three afternoons that produced a book. The statistics count you, not your text: word counts and times are recorded, not content.

## GitHub as an uninvolved witness

Up to this point everything sits with you — and anything that sits with you could, in case of doubt, have been staged by you. The final step turns it into something solid: if your project is linked to GitHub, your commits end up with a third party that has nothing to do with your text. How that works is explained in [Using GitHub the right way](/blog/using-github-with-bun-ink).

A timestamp you set yourself is a claim. A timestamp on the GitHub server is more like evidence. You grant access as broadly or narrowly as you like — invite one person, open the repository, or export the commit list. "I wrote this myself" becomes "here are the 312 steps, with dates and the content of the corresponding changes".

Of course a grown commit history isn't forensic proof. With enough effort it could be staged, including by an AI agent. What version control achieves is more modest, but still useful: it shifts the question from "does the text look human?" to "is there a coherent trail of work that grew over weeks?". That's the better question, and it can be answered this way.

## And the security of your texts?

In connection with the well-known large language models, another question unfortunately always comes up: *does my manuscript end up in some training dataset somewhere?* With bun.ink, the answer is short. The app sends your texts neither to a language model nor to anyone else, unless you want it to. In the bun.ink database, text entries are not stored as readable plain text but encrypted. How that works in detail is explained in [How bun.ink protects your texts](/blog/how-bun-ink-protects-your-texts).

Versioning via GitHub, as described above, requires your explicit consent. Of course you can also use [bun.ink](http://bun.ink) without GitHub. A high-privacy folder or project in particular can only be used without GitHub. Nobody else can then read or change your texts. But the benefit of absolute privacy comes with a drawback: there's no versioning via GitHub — and therefore, in case of doubt, no proof of your work.

## What you can do to document your work

If this kind of proof matters to you, a few habits are worth building:

- **Start early.** The history begins with the first commit, not with the finished manuscript.
- **Save in small steps.** Five commits in one afternoon are better than one at the end of the month.
- **Write honest messages.** "Dialogue shortened, flashback removed" says more than "Update".
- **Leave the detours in.** Discarded versions aren't a flaw, they're the proof.
- **Frame your tools.** Save once before and once after each pass through a correction tool.
- **Keep the agent separate.** Larger AI work belongs on its own branch and under the agent's own account — that distinction is half the evidence.
- **Revise through pull requests, even on your own.** What you discarded stays documented along with the reasoning — how that works is explained in [The Editor Comes to the Text](/blog/reviews-as-pull-requests).

## Finally: an open book, in both directions

A fair warning at the end: what's described here as evidence works in both directions. A version history that shows a chapter grew in forty steps equally shows that another one stood complete after a single step. Anyone working with AI leaves a recognisable trail in the history — but with models like Claude, since this summer there's additionally one in the text itself.

For most people that's not a problem: anyone who discloses their tools has nothing to hide, and a well-kept repository even shows what was suggested and what was adopted — exactly the idea behind the article on the [controlled writing partner](/blog/ai-controlled-writing-partner).

Because that's the price and the value of one and the same thing: with bun.ink, the creation process of a text is a proverbial open book. Anyone who writes every line themselves will find in it the proof they'll depend on in future. Anyone who only has their text corrected will find in it the difference between "a machine was involved" and "here's what it did". Anyone working with AI will learn the truth about their own way of working. The one thing the writing process no longer is: invisible.
