---
title: AI as a Controlled Writing Partner – Creating Texts with Agents and Clear Rules
date: 2026-06-19
description: How authors can use AI to write, review, and revise — without giving up control over style, content, and decisions.
sourceHash: 7dbbaba0177e9952bbfd00948070e810cf14ac790081a70e39a4df1f2c2b0812
---

Artificial intelligence can now craft paragraphs, suggest scenes, imitate character voices, and revise entire drafts. That sounds like a grand promise — and sometimes like a threat: _Is the human even still writing?_

The more interesting answer is: yes, as long as the AI is understood not as a replacement but as a **controlled writing partner**. An agent can sort ideas, find weak spots, and offer alternatives. But the direction, the rules, and the final decision remain with the author.

## AI doesn't write in a vacuum

A AI agent is especially helpful when it knows what to look out for. Without context, it works from general patterns: it recognizes what "usually" sounds good, which structures tend to work, and which phrasings are likely to fit. For a specific novel, essay, or blog post, that often isn't enough.

Texts have their own laws. A novel may be told consistently in the first person. A character may deliberately speak in short, hard sentences. A nonfiction piece may have a calm, explanatory voice. If the AI doesn't know these rules, it might "improve" something that wasn't meant to be improved at all.

That's why context becomes crucial: the more precisely the agent knows the intention behind a text, the more useful its support can be.

## What an AGENTS.md can do

A simple Markdown file can play a surprisingly large role here. In many working environments, you can place a file like `AGENTS.md` or `agents.md` in your project. It contains instructions, background information, and rules that an AI agent should take into account as it works.

For a literary project, such a file might, for example, note:

- **Narrative perspective:** close third person, near the protagonist
- **Tense:** past tense, no shifts into the present
- **Style:** terse, vivid, no ironic narratorial commentary
- **Character knowledge:** the protagonist doesn't know who wrote the letter until chapter 12
- **Storyline:** central turning points, key relationships, open secrets
- **Taboos:** no modern idioms, no omniscient explanation, no resolution before the finale

This turns the Markdown file into a kind of working brief. It doesn't replace the manuscript or the creative decision. But it gives the agent a framework within which to check, comment, and make suggestions.

## When the agent has access to the project

This becomes especially interesting when an agent is connected directly to a GitHub repository or another project folder. Then it sees not just the single excerpt you paste into a chat window, but can also read accompanying files: notes, character sheets, chapter plans, research texts, or indeed an `AGENTS.md`. We describe the concrete workflow for linking a project with GitHub in [Using GitHub with bun.ink – the versioning workflow](/blog/using-github-with-bun-ink).

That changes how you collaborate. Instead of explaining the situation from scratch each time, the agent can take recurring project rules into account. It can ask: _Does this scene still match the established narrative perspective?_ Or: _Does this piece of information contradict the storyline so far?_

For authors, this means the AI doesn't get smarter because it "magically" understands what you mean. It becomes more helpful because it has better working materials.

## Style analysis instead of automatic rewriting

A controlled approach often doesn't begin with the request "Make this sound nicer." Far more helpful is the request: "Analyze this text against my rules."

The agent can then work like an attentive editor and offer pointers:

- Where does the narrative perspective shift unintentionally?
- Where does the text slip from past tense into present?
- Which sentences don't sound like the established character voice?
- Where does the narrator explain too much, when the scene could show it instead?
- Which terms don't fit the period, the setting, or the tone of the novel?

The distinction matters: the AI doesn't change the text unbidden. It flags passages, explains its reasoning, and makes suggestions. The decision whether to change anything stays with the human.

## Spotting logical errors and blind spots

Beyond questions of style, an agent can also watch for contradictions in content — especially when the rough plot is described in a project file. If it says there that a character only learns of a secret in the final third, the agent can check earlier chapters to see whether they accidentally already assume that knowledge.

Such checks are no guarantee. An AI can weigh connections wrongly or miss something. But it can serve as a second layer of attention. Sometimes it catches inconsistencies that have become invisible on repeated reading, because the author has long since completed the story in their own head.

Typical requests to the agent might be:

- "Check chapter 4 for contradictions with the storyline in `AGENTS.md`."
- "List every passage where the protagonist seems to know more than they should at that point."
- "Look for tense shifts and briefly explain why they stand out."
- "Suggest alternatives for this scene without changing the perspective."

The result is a dialogue resembling an editorial conversation: the agent doesn't deliver final verdicts but provides observations and possible paths forward.

## The human remains the authority

With literary texts in particular, control is decisive. An AI can phrase things very convincingly, but it doesn't automatically grasp a text's inner necessity. Sometimes a break is intentional. Sometimes a sentence is meant to stay awkward. Sometimes a repetition isn't a mistake but a rhythm.

That's why the agent shouldn't present itself as an authority, but as a tool with a clear task. The best results come when authors specify precisely on which level the AI should help:

1. **Observe:** check style, perspective, tense, or logic.
2. **Explain:** justify and contextualize anything that stands out.
3. **Suggest:** offer several alternatives.
4. **Implement:** make changes only after explicit approval.

This order protects your text. It prevents an AI from turning an idiosyncratic manuscript into a smooth, average one.

## Writing with memory and rules

Combined with version control, this approach becomes even stronger. When a project lives in a repository, changes remain traceable – you can see which suggestions were adopted and which version existed before. What commits, branches and repository mean in detail is covered in [Git and GitHub made simple](/blog/git-and-github-for-writers); the practical workflow in bun.ink is shown in [Using GitHub with bun.ink](/blog/using-github-with-bun-ink).

An `AGENTS.md` provides the rules. The repository preserves the history. The agent helps with checking and revising. Together they create a way of working in which AI doesn't quietly take over but visibly contributes.

That may be the most important idea: AI-assisted text creation doesn't have to mean a text becomes less personal. Used well, it can even help protect your own intentions more clearly — because style, perspective, and plot no longer live only in the author's head, but stand in the project as checkable rules.

The future of writing therefore doesn't lie in the press of a button that produces a finished book. It lies in tools that read along attentively, ask smart questions, and offer alternatives — while the human decides what voice the text should ultimately have.
