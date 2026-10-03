---
title: AI as a Controlled Writing Partner – Creating Texts with Agents and Clear Rules
date: 2026-06-19
description: How writers can use AI for drafting, checking, and revising without surrendering control over style, content, and decisions.
sourceHash: 7d7a99fe5af3bff6fa51f9382c8b657eca1db41bb72417c5408ddca7bd660ede
---

Artificial intelligence can now draft paragraphs, suggest scenes, imitate character voices and rework entire versions of a text. That sounds like a big promise – and sometimes like a threat: _Is a human still doing the writing?_

The more interesting answer is: yes, as long as AI isn't seen as a replacement but as a **controlled writing partner**. An agent can sort ideas, spot weak points and offer alternatives. But the direction, the rules and the final decision stay with the author.

## AI doesn't write in a vacuum

An AI agent is especially helpful when it knows what to pay attention to. Without context, it works from general patterns: it recognises what "usually" sounds good, which structures tend to work and which phrasings are likely to fit. For a particular novel, essay or blog article, that often isn't enough.

Texts have their own laws. A novel may be told consistently in the first person. A character may deliberately speak in short, hard sentences. A non-fiction piece may have a calm, explanatory voice. If the AI doesn't know these rules, it may well "improve" something that was never meant to be improved.

That's why context becomes decisive: the more precisely the agent knows what intention lies behind a text, the more useful its support can be.

## What an AGENTS.md can do

A simple Markdown file can play a surprisingly large role here. In many working environments you can place a file such as `AGENTS.md` or `agents.md` in the project. It contains instructions, background information and rules that an AI agent should take into account as it works.

For a literary project, such a file might record, for example:

- **Narrative perspective:** third-person limited, close to the main character
- **Tense:** past tense, no switching into the present
- **Style:** terse, vivid, no ironic narrator's commentary
- **Character knowledge:** the main character doesn't know who wrote the letter until chapter 12
- **Storyline:** key turning points, important relationships, unresolved secrets
- **Taboos:** no modern idioms, no omniscient explanation, no resolution before the finale

This turns the Markdown file into a kind of working brief. It doesn't replace the manuscript, nor the creative decision. But it gives the agent a framework within which it can check, comment and make suggestions.

## When the agent has access to the project

This becomes particularly interesting when an agent is connected directly to a GitHub repository or another project folder. It then sees more than the single excerpt you paste into a chat window: it can also read the accompanying files – notes, character sheets, chapter outlines, research texts or indeed an `AGENTS.md`. We describe the concrete workflow for connecting a project to GitHub in [Using GitHub the right way – the versioning workflow in bun.ink](/blog/using-github-with-bun-ink).

That changes the collaboration. Instead of explaining what it's all about every single time, the agent can take recurring project rules into account. It can ask: _Does this scene still match the established narrative perspective?_ Or: _Does this piece of information contradict the storyline so far?_

For authors, this means the AI doesn't get smarter because it "magically" understands what you mean. It becomes more helpful because it's given better working material.

## Style analysis instead of automatic rewriting

Controlled use often doesn't begin with the request "make this sound nicer." A far more helpful question is: "Analyse this text against my rules."

The agent can then work like an attentive editor and point things out:

- Where does the narrative perspective shift unintentionally?
- Where does the text slip from past tense into present tense?
- Which sentences don't sound like the character voice you defined?
- Where does the narrator explain too much, when the scene could show it instead?
- Which terms don't fit the period, the milieu or the tone of the novel?

The difference matters: the AI doesn't change the text unasked. It flags passages, explains its reasoning and makes suggestions. Whether anything is actually changed remains a human decision.

## Finding logical errors and blind spots

Besides questions of style, an agent can also watch for contradictions in content – especially when the broad plot is described in a project file. If that file states that a character only learns of a secret in the final third, the agent can check earlier chapters for places where they inadvertently already assume that knowledge.

Such checks are no guarantee. An AI can misjudge the weight of a connection or miss something entirely. But it can serve as a second layer of attention. Sometimes it finds breaks that have become invisible on repeated reading, because the author has long since completed the story in their head.

Typical requests to the agent might be:

- "Check chapter 4 for contradictions with the storyline in `AGENTS.md`."
- "List every passage where the main character seems to know more than they should at this point."
- "Look for shifts in tense and briefly explain why they stand out."
- "Suggest alternatives for this scene without changing the perspective."

The result is a dialogue that resembles an editorial conversation: the agent doesn't pass final judgement, it offers observations and possible paths.

## The human remains the authority

With literary texts in particular, control is crucial. An AI can phrase things very persuasively, but it doesn't automatically grasp the inner necessity of a text. Sometimes a break is intentional. Sometimes a sentence is meant to stay awkward. Sometimes a repetition isn't a mistake but rhythm.

That's why the agent shouldn't present itself as an authority, but as a tool with a clear task. The best results come when authors specify precisely on which level the AI should help:

1. **Observe:** check style, perspective, tense or logic.
2. **Explain:** justify and contextualise anything that stands out.
3. **Suggest:** offer several alternatives.
4. **Implement:** only make changes once explicitly approved.

This order protects your own text. It stops an AI from turning an idiosyncratic manuscript into a smooth, average one.

## Writing with memory and rules

Combined with version control, this approach becomes even stronger. When a project lives in a repository, changes stay traceable – you can see which suggestions were adopted and what the previous version looked like. We've written up what commits, branches and repositories mean in detail in [Git and GitHub made simple](/blog/git-and-github-for-writers); for the practical workflow in bun.ink, see [Using GitHub the right way](/blog/using-github-with-bun-ink).

Ideally the agent works on a branch of its own and hands back its result as a pull request. In bun.ink you then go through it passage by passage – accept, discard, or put your own wording against it – just like a revision from a human editor. How that works is described in [The Editor Comes to the Text](/blog/reviews-as-pull-requests); how to set up an agent and give it a task is covered in the handbook chapter [AI Tools and Your Texts](https://github.com/VisionX-Development/writing-with-bunink/blob/main/en/08-ai-agents.md).

The `AGENTS.md` supplies the rules. The repository preserves the history. The agent helps with checking and revising. Together they create a way of working in which AI doesn't quietly take over, but visibly contributes.

That may be the most important idea here: AI-assisted writing doesn't have to mean a text becomes less personal. Used properly, it can even help you protect your own intentions more clearly – because style, perspective and plot no longer live only in the author's head, but exist as verifiable rules within the project.

The future of writing therefore doesn't lie in pressing a button that produces a finished book. It lies in tools that read along attentively, ask smart questions and offer alternatives – while the human decides what voice the text should have in the end.
