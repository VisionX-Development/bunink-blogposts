---
title: Proving Your Work — What the AI Watermark Doesn't Tell You
date: 2026-09-20
description: Since August 2026, Anthropic has been tagging text from new Claude models with an invisible watermark — whether the model wrote the text or merely corrected it. Why this leads to false accusations, and how your commit history proves that a text is yours, sentence by sentence.
sourceHash: b383ed647f396126b189f4b08c8325ba289141a1e90e54c5701af9ce474ed196
---

A while back we described here how an AI can be used as a [controlled tool](/blog/ai-controlled-writing-partner): with clear rules and an agent that checks and suggests, while we as authors make the decisions.

This article is about a question that arises regardless: how do you prove that a text is your own work?

How someone deals with AI is a personal decision, and this article won't make it for anyone. Without any judgement, and painting with a very broad brush, there are three camps: the first camp are those who never use AI; the second camp are those who have AI produce everything — entire scenes, chapters and books; the third group sits exactly between the first and the second, writing every sentence themselves but using AI tools for spellchecking, revision or style analysis.

When it comes to the question of proof, your attitude towards AI matters surprisingly little. Because the answer doesn't lie in the finished text. It lies in how the text came about — in the writing process itself. And that process is exactly what versioning a text captures, and in bun.ink it happens without any extra effort.

## The new problem: proving a negative

Anyone who delivers a text increasingly has to be able to prove something that nobody had to prove until recently: that they wrote it themselves and not a machine. Publishers ask for assurances, editorial departments add corresponding clauses to contracts. The tools used to check this are still pretty useless today: AI detectors guess on the basis of surface features and are regularly wrong — in a [test by Markus Brinsa](https://brinsa.com/moby-dick-failed-the-ai-test-or-the-test-failed-moby-dick), the detector Pangram classified around 44 percent of Moby-Dick, Herman Melville's 1851 classic, as AI text.

The core problem: the line between human and machine in text creation is getting blurrier all the time. A text on its own is an open-ended result. The difference between human and machine lies in how it came about — and that normally disappears the moment the file is saved. Machine-generated text, on the other hand, almost never carries information about its own origin.

## Your own text, someone else's tools

So what happens to authors who write every sentence themselves but use a spelling or grammar checker or a digital editing tool? What happens to authors who use excerpts from an AI agent's research?

All of these tools have long been using language models under the hood, and you often can't tell from the outside. If you accept a grammar correction, it doesn't feel like writing with an AI. All the same, at some point a machine has passed over the text. And since this summer, that has become a problem.

## The watermark is not a thing of the future

Since 2 August 2026, Anthropic has been adding an invisible watermark to text from new Claude models — [according to the company](https://www.anthropic.com/news/claude-text-watermark), worldwide, because the marking can't reliably be limited to one region. Older models will be retrofitted over the coming months; the AI Act sets a deadline of 2 December 2026 in [Article 111(4)](https://ai-act-service-desk.ec.europa.eu/en/ai-act/article-111). Behind this is the code of practice for Article 50 of the EU AI Act, which Anthropic has signed — other providers will have to follow the same path.

What matters is where this marking shows up: **any tool that uses a watermarking model in the background can leave it behind** — including your spellchecker. The watermark is embedded in the word choice itself. According to Anthropic, it survives light editing and copying; only when every single word is replaced does it disappear. A translation by Claude carries it too.

## What a watermark says — and what it doesn't

For the group that "only" uses AI tools, that's a problem. The marking is very crude. It proves that a model was involved — but not that it wrote the text. Anthropic says so clearly itself: it doesn't distinguish between written, revised, translated and summarised. Someone who has their own text proofread gets the same marking as someone who had an entire chapter or book generated. In the eyes of an outside reader who doesn't know or can't trace how the text came about, groups 2 (AI only) and 3 (AI tools) are now treated as one and the same.

On top of that comes the real annoyance: **you can't check it yourself.** So far, detection is only available to authorised bodies — authorities, media, research. There is no public tool you could use to refute an accusation.

Which brings us to the sentence this whole article revolves around: if someone accuses you of your text being "AI-written," you won't refute it by pointing at the finished text. Your proof isn't the result. In future, your only possible proof will be the path that led there.

Anthropic explains the current state of the watermark in its [help article on marking AI-generated content](https://support.claude.com/en/articles/16266773-how-claude-marks-ai-generated-content), and how it works technically in [How Claude's text watermarking works](https://www.anthropic.com/news/claude-text-watermark).

## What versioning records besides the text

This is exactly where versioning happens to do something it was never actually designed for in the past. When you work in bun.ink, you don't save a file that overwrites itself; you create save points — commits that record what the text looked like, when that was, and what you noted down. What commits, branches and repositories mean is explained in [Git and GitHub explained simply](/blog/git-and-github-for-writers).

Alongside your text, this creates a second "story" that nobody deliberately writes: the story of how it came to be. When the first paragraph appeared, which sentence stood unchanged for three weeks, where you discarded a scene and later picked it up again differently. This second layer is the proof of your work — and it comes into being on the side, while you simply get on with writing.

## The timeline: when each sentence came into being

In the Writer you can read this history too. The Changes tab contains the **commit browser**: a list of all save points, each with a timestamp and a message. You pick two states — say the first commit and today's — and see every change between them highlighted. Described in detail in [The Commit Browser](/blog/browsing-your-commit-history).

So if someone asks you whether chapter 7 is really yours, you don't have to protest your innocence. You can show the forty save points it grew out of.

## Why micro-steps are more convincing than a finished chapter

The real proof doesn't lie in any single commit, but in the **shape** of the history. Human writing is crooked: one paragraph grows over a week in seven steps, another appears in twenty minutes and is cut in half the next day. There are days with four hundred words and days with forty, sentences that get rearranged three times, deletions, pauses, returns.

That is exactly what a grown commit history contains — and exactly what's missing when a chapter shows up in a single step: complete, without a single revision afterwards. A text that appears that way either came into being somewhere else or was generated. Either looks different from a text that a human has worked on.

The smaller your save points, the denser this evidence becomes. With bun.ink that's no extra effort; it's the way of working that helps you go back anyway.

## Before and after: what the history reveals about the tool

For the third group this gets very concrete. Your history contains the paragraph **before** the tool touched it: Tuesday evening's commit shows your version, Wednesday morning's shows what the correction made of it. Between them lies a comparison anyone can read — a comma, two words swapped around. And yes, making mistakes, spelling errors for example, is very useful here, even if it's child's play for an AI to find and correct them.

That shifts the question from "is there machine in here?" to "what exactly did it do?" You're not proving that no tool was ever involved — since this summer you can't do that anyway. You're proving authorship: that the text is yours and that a tool touched its edges, not its substance.

In practice that means: **one commit before using the tool, one commit after.** Ten seconds of effort — and the line between your work and the correction is permanently documented. Because you can't check the marking yourself, your history is the only evidence that belongs to you.

## The statistics make it visible

What's contained in the history can also be looked at rather than read. The [writing statistics](/blog/writing-statistics-that-motivate) in the Writer show your work as numbers and images: words per day and week, active writing time, a heatmap across twelve months. For projects with a repository, commit activity is added.

A year of writing looks in there exactly like a year of writing looks: uneven, with gaps and dense phases before deadlines — not like three afternoons during which a book appeared. The statistics count you, not your text: word counts and times are recorded, no content.

## GitHub as an uninvolved witness

Up to this point everything sits with you — and anything that sits with you, you could in principle have staged yourself. The final step turns it into something robust: if your project is linked to GitHub, your commits end up with a third party that has nothing to do with your text. How that works is described in [Using GitHub the right way](/blog/using-github-with-bun-ink).

A timestamp you set yourself is a claim. A timestamp on GitHub's server is closer to evidence. You grant access as broadly or as narrowly as you like — invite one person, open the repository, or export the commit list. "I wrote this myself" becomes "here are the 312 steps, with dates and the content of each change."

Of course, a grown commit history is not forensic proof. With enough effort it could be staged, including by an AI agent. What versioning achieves is more modest, but still useful: it shifts the question from "does this text look human?" to "is there a coherent trail of work that grew over weeks?" That's the better question, and this is how you answer it.

## And the security of your texts?

In connection with the well-known large language models, another question unfortunately always comes up: *will my manuscript end up in some training dataset?* With bun.ink the answer is short. The app sends your texts neither to a language model nor to anyone else, unless you want it to. In the bun.ink database, text entries are not stored as readable plain text but encrypted. How that works in detail is described in [How bun.ink Protects Your Texts](/blog/how-bun-ink-protects-your-texts).

Versioning via GitHub, as described above, requires your explicit consent. You can of course also use [bun.ink](http://bun.ink) without GitHub. A high-privacy folder or project in particular can only be used without GitHub. No one else can then read or change your texts. But the advantage of absolute privacy comes with a drawback: you lose versioning via GitHub — and with it, if it ever comes to that, the proof of your work.

## What you can do to document your work

If this kind of proof matters to you, a few habits are worth developing:

- **Start early.** The history begins with the first commit, not with the finished manuscript.
- **Save in small steps.** Better five commits in one afternoon than one at the end of the month.
- **Write honest messages.** "Shortened dialogue, cut flashback" says more than "update".
- **Leave the detours in.** Discarded versions aren't a flaw, they're the evidence.
- **Frame your tools.** Save once before and once after every pass through a correction tool.
- **Keep the agent separate.** Larger AI work belongs on its own branch and under the agent's own account — that distinction is half the proof.
- **Revise in the open, even on your own.** What you discarded stays documented along with the reasoning — how that works is described in [Editing Comes to the Text](/blog/reviews-as-pull-requests).

## Finally: an open book, in both directions

A fair warning at the end: what's described here as evidence works in both directions. A version history that shows one chapter grew in forty steps shows just as clearly that another stood finished after a single step. Anyone working with AI leaves a recognisable trail in the history — and with models like Claude, since this summer, there's an additional one in the text itself.

For most people that's not a problem: if you're open about your tools, you have nothing to hide, and a well-kept repository even shows what was suggested and what was accepted — exactly the idea behind the article on the [controlled writing partner](/blog/ai-controlled-writing-partner).

Because that's the price and the value of one and the same thing: with bun.ink, the process behind a text is a proverbial open book. Anyone who writes every line themselves finds in it the proof they'll be relying on in future. Anyone who only has their work corrected finds the difference between "a machine was involved" and "here's exactly what it did." And anyone working with AI learns the truth about their own way of working. One thing the writing process no longer is: invisible.
