---
title: The Editor Comes to the Text — Reviews as a Pull Request
date: 2026-09-12
description: How someone else can revise your text without ever touching it — and how, in the end, you decide passage by passage what makes it into your manuscript.
sourceHash: 99d21656c6100cdc098bb86a6e87282b697ddb3adbcfcbc42bc52efaddc18d60
---

There's this folder. `kapitel-3.docx`, `kapitel-3-lektorat.docx`,
`kapitel-3-lektorat-final.docx`, `kapitel-3-lektorat-final-KORR.docx`. Somewhere in there is the
version that counts. After the third round, nobody knows for sure which one it is, and the note
that was in the margin of page 14 got lost when it was copied over.

bun.ink turns this into something else: a **review**. Someone reads your text, marks passages,
suggests new wording — and your text stays untouched until you've decided, passage by passage,
what you want to take from it. In the end there's no second file. There's your text, and it says
what you wanted it to say.

## The difference: nobody writes in your manuscript

This is where this feature differs from a shared file. When your editor starts a review, they
get their own copy of your text — in Git this is called a branch, an offshoot, as described in
[Using GitHub the right way](/blog/using-github-with-bun-ink). Everything that happens there stays
there: rewordings, deletions, notes.

Your version notices none of it. You can keep writing while someone else reads. Only when the
review is finished and sent does it come knocking — and even then nothing in your text changes
as long as you don't accept something yourself.

That's the real reversal. In a shared document, someone else's change is simply there and you
have to undo it if you don't want it. Here it's a suggestion waiting for you to accept it.

One requirement, right up front: the text to be revised must itself already be on a branch — say
`kapitel-3` — and not on your project's main version. The review needs a target that can be
merged later, and the main version is deliberately off-limits for that. Creating a branch is one
click, nothing more.

## How a review comes about

From the perspective of the person doing the reviewing, the beginning is unspectacular: they open
your project, switch to your text, and start the review. bun.ink explains in one sentence what's
about to happen — the review gets its own branch alongside yours, that's where the work
happens, and its suggestion is offered to you later.

After that, the work is done in the perfectly ordinary way in the editor. Rearranging sentences,
cutting, deleting — just like any other text. For the person reviewing, it feels like editing your
text. In fact they're editing their copy.

That copy then becomes **suggestions**. bun.ink shows your text and the revised version side by
side, with all the differences highlighted — as readable text, not as code. The person reviewing
goes through the changed passages and turns each one they want to put to you into a suggestion:
this is the passage, this is the new wording, and — if they like — why. That reasoning is what
you read later, before you decide.

It also works without new wording. Sometimes a note doesn't want to change anything at all, it
just wants to say something: "This comes too early," "The name is wrong here." Such notes hang at
their spot in the text and get lost just as little as a suggestion does. And for anything that can't be
pinned to a specific spot — about structure, about tone — there are notes on the whole text.

Up to this point nothing is on its way yet. Every suggestion can still be reworded or withdrawn;
if it's withdrawn, the change in the text disappears too, so that nothing quietly remains for
which there's no longer a suggestion. And if the text under a suggestion has since changed,
bun.ink says so clearly before anything is sent.

The review in progress stays on the device of the person reviewing, even if they close the
window or continue tomorrow. Only logging out clears it away — bun.ink warns about that — and
whatever has already been saved as text is safe anyway. Everything is sent at once, as a **pull
request**. That's nothing more than the form in which GitHub carries such a request: "Here's a
suggestion for your text, take a look."

If something is added later, no second process is created for it. Each text has exactly one
review, and further rounds attach to the same one — a conversation, not a stack of
conversations.

## What arrives on your end

A notice appears on your end: there's a review for your text. From there you have two paths, and
you can mix them.

The first path leads through your document. Alongside your text, the suggestions that concern it
appear: the marked passage, the proposed wording, the reasoning, and who wrote it. You jump to the
spot, read it in context, and accept the suggestion — or leave it.

Whatever you accept is immediately in your document. Not "requested," not "will be worked in at the
next step" — it's there, and you can keep writing on it. To notes that only wanted to say
something you can reply directly; the reply appears at the editor's end at exactly the spot it was
about.

### When a passage no longer fits

You kept writing while it was being read. The suggestion refers to a sentence that no longer
exists like that — or that now appears twice. bun.ink then doesn't guess, it says so: this passage
needs your decision.

You see both versions side by side — what's currently in your text and what was suggested — and
exactly the lines in question. You insert the suggestion, write your own version, or leave
everything as it is. Nothing is shifted around in the background.

This is deliberately the more inconvenient option. An automatically inserted suggestion that lands
a few lines off the mark only comes to light weeks later — if at all.

## The whole suggestion at once

The second path is the overview: all changed files placed side by side, your text on the left, the
review's version on the right. Where a change concerns only formatting — a sentence was italic
and is meant to be bold — bun.ink tells you so, instead of making you compare the same sentence
twice.

Here decisions aren't made by lines but by **passages** — connected stretches where something has
changed. For prose that's the right unit: a reworded sentence hangs on its neighbours, and taking
a single line from it produces a text nobody wrote. A suggestion that runs across two paragraphs
is therefore one passage and one decision, not two.

For each passage you have three answers:

- **Keep** — the change comes along when you accept the review as a whole at the end.
- **Discard** — the passage stays as it was on your side. With a reason, if you like.
- **Own wording** — neither one nor the other, but your third wording. It goes back to the editor
  as a counter-suggestion.

And just as in the document, here too you can accept a passage into your text right away. That even
applies to deletions, which are otherwise hard to "suggest": one decision, and the paragraph is
gone from your side.

### What's discarded goes back

Here something happens that doesn't exist on paper. Whatever you discard or answer with your own
version is written back onto the review's copy — with your reason attached, if you gave one. So
your editor sees which passages you didn't want and what you're suggesting instead.

The reason for this detour is simple: the alternative would be for you to quietly leave out the
unwanted passages. Then in the end there'd be a text that both sides consider agreed upon,
although nobody talked about half the changes. This way the coordination stays complete and can be
read back in both directions.

## In the end: accept or close

Two ways to finish a review.

**Accept everything at once.** In Git this is called merging: the review's copy is merged into
your text, and the copy disappears. bun.ink only allows this once every single passage has been
decided, and until then counts off for you how many are still open. Otherwise an unanswered
suggestion would travel along unseen, and that's the most dangerous kind of mistake: nothing goes
wrong, it just never gets noticed.

One case deserves its own sentence: if you've already accepted individual suggestions into your text
and saved them, GitHub sees two changes at that spot — yours and the review's — and can't know
they're the same. bun.ink knows, and resolves it for you: what you decided stands, the rest comes
from the review, and the merge goes through. No new process, no detour via GitHub.

**Accept individually, then close.** If you've already brought everything you wanted into
your text, passage by passage, no merge is needed anymore. You close the review, and your editor
automatically gets a report: which file, and how many of the suggested changes were accepted. No
process that vanishes without a word.

## What you need for this

Honestly, this is the least romantic section, but without it nothing works:

- **Both sides need their own GitHub account** and their own bun.ink account. There's no shared
  password and no guest access.
- **Access runs through GitHub**, not through bun.ink: you invite your editor as a collaborator on
  your repository, just as you'd give someone access to a shared folder. Anyone without access
  there won't even see your project in bun.ink.
- **An active subscription or an ongoing trial** on both sides.
- **Only someone with write access to the repository may merge.** Reading and suggesting works
  without it.

And one limitation you should be aware of: as long as you're working on a branch, your text isn't
in bun.ink but only in your browser — until you save it to GitHub. That applies while reviewing
just as it does otherwise. Save there earlier and more often than you're used to.

## Why it's worth the effort

Editing is a conversation about a text, and conversations fall apart when you conduct them through
file attachments. Someone writes a note, someone else transcribes it by hand, half of it gets lost
in the process and the rest suddenly ends up in the wrong place.

Here every note stays at its spot, every suggestion is a decision and not a fact, and in the end
you can read back who suggested what and who accepted what. Not because anyone is suspicious — but
because a text whose making you can read back is a text you can still agree on in half a year.
