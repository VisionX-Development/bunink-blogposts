---
title: How bun.ink Protects Your Texts – Encryption Explained Simply
date: 2026-07-28
description: What happens to your texts before they're saved — server-side encryption for all documents, the high-privacy folder and the high-privacy project for your diary, and what you're responsible for yourself.
sourceHash: 02533f86be3f2766e55be359e004b70a66032ec5e7262a66f143e00dea62ffb6
---

A text is a personal thing. A half-finished chapter, research with sources nobody is supposed to know about, a diary entry from a bad day — that isn't just arbitrary data. Which is why the question "who can actually read this?" isn't a technical footnote for a writing app. It's a question of trust.

This article answers it as precisely as possible — without jargon, but also without promises we can't keep.

## Two layers — one for everything, one for your diary

bun.ink protects content on two levels, and it's important to keep them apart:

- **Layer 1 — server-side encryption.** Applies to every document, without you having to do or configure anything. Your texts don't sit in the database as readable plain text.
- **Layer 2 — the high-privacy folder or a high-privacy project.** A special type of folder or project that you create yourself. Its contents are encrypted **in your browser**. Nobody but you can read them — not even us.

Layer 1 is convenience without compromise. Layer 2 is maximum protection at a price you should know about. We'll explain both, one after the other.

## First, briefly — what encryption actually does

Picture a text running through a machine and coming out the other side as an unreadable jumble of characters. The machine needs a **key** to do this — a long, random number. With that same key, the jumble runs back through and becomes the original text again. Without the key, it's effectively impossible to reconstruct; it's not a puzzle you can crack with patience, but a computation that wouldn't finish within human lifetimes even in enormous data centres.

bun.ink uses **AES-256-GCM** for this, the standard method also used by banks, government agencies and HTTPS connections. Two of its properties matter to you in practice:

- **Every save uses a fresh random value.** The same text saved twice produces two completely different jumbles of characters. So the stored data gives no indication that two documents have the same content.
- **Every encrypted text carries a seal.** If someone alters the stored data by even a single character, the text can no longer be decrypted — the tampering is immediately obvious, instead of a corrupted text being quietly handed back.

There's another rule: **a separate key for every kind of data.** Document contents, GitHub access tokens and backups each have their own. Anyone holding one of them could do nothing with the other data. The keys never live in the program code and never in your repository, only in the server configuration and in a password manager.

## Layer 1 — your texts don't sit in the database as plain text

When you save, your text goes into the database encrypted. The server encrypts it right before writing and decrypts it again after reading — in between, it's nothing but a jumble of characters in the database. The same goes for saved versions (the snapshots of your text's history) and for your snippets.

You notice **nothing** of this. Full-text search, version comparison, conflict handling, GitHub sync: everything works exactly as before and without any noticeable delay — encryption of this kind operates in milliseconds, not seconds.

What this protects you against:

- **A database leak.** Anyone who gains access to the database gets a jumble of characters, not texts.
- **A stolen or lost backup.** Backups contain the same encrypted data — and are additionally encrypted themselves.
- **Access via the database console.** Even someone poking around there — today, or as a future team member — won't see your content.

And now the honest part, because this point decides whether you need layer 2:

- **Layer 1 is not "nobody can read it".** The server needs the key in order to show you your text in the editor. Anyone with access to the server configuration — that is, us as the operators — therefore technically has access to the key as well. We don't do that, but the encryption alone doesn't prevent it. That's exactly the gap layer 2 closes.
- **GitHub stays readable on purpose.** "Git for writers" depends on your repository holding real, readable Markdown files — that's where you can open them on any device, and that's where [AI agents](/blog/ai-controlled-writing-partner) can work with them. An encrypted jumble of characters in the repo would be useless. So the encryption protects our database, not your GitHub account; for your repository, the access rights you set on GitHub yourself apply (a private repository stays private).
- **Names and numbers remain visible.** Document, project and folder names, timestamps, version counts and the approximate text length are not encrypted — they're needed for lists, sorting and the tree view to work. So don't name a folder after the secret it contains.

## Layer 2 — the high-privacy folder or a high-privacy project

For a diary, for confidential sources, for texts nobody should see, there are two **high-privacy** variants. The difference from layer 1 sounds small but is fundamental: here, encryption doesn't happen on the server but **in your browser** — before anything reaches our data centre. All that arrives at the server and in the database is a jumble of characters for which no key exists there.

You choose how large the protected area should be when you create it:

- **High-privacy folder.** Protects exactly this one folder (and its subfolders) within an otherwise normal project. The rest of the project remains fully usable — including GitHub sync, which simply skips the encrypted documents.
- **High-privacy project.** Automatically protects the entire project, including documents that sit directly in the project rather than in any folder. In return, such a project can't be linked to GitHub at all — there'd be nothing in it to sync.

Cryptographically, the two are identical: same algorithm, same process, same rules. But a project and its folders can't be mixed — you can't create an additional high-privacy folder inside a high-privacy project, that would be a key within a key. Everything described below for the "high-privacy folder" therefore applies unchanged to the high-privacy project as well.

This is genuine end-to-end encryption. We can't read this content, can't search it, can't restore it and can't hand it over to anyone — not even from backups, because what's stored there is equally unreadable.

Here's how it works, in plain words:

1. When you create it, your browser generates a random **folder key**. All documents in this folder are encrypted and decrypted with it.
2. You choose a **passphrase**. From it, the browser derives a second key that locks the folder key away as if in a safe. Only this locked safe is stored — the passphrase itself never leaves your browser and is never stored anywhere.
3. This derivation is deliberately **computationally expensive** (Argon2id, a method designed specifically against password-guessing attacks). An attacker wanting to try millions of passphrases has to spend significant computing time and memory on every single attempt. For you, unlocking takes less than a second.
4. After creation, bun.ink shows you a **recovery key** — **once**. This is the folder key itself, in text form. It opens the folder even if you've forgotten the passphrase.
5. When you open a document, bun.ink asks for the passphrase (or the recovery key). After that you carry on as normal: editor, local search, word count. When you save, your browser encrypts again.
6. The unlocked key lives **only in the memory** of this browser session — never in a cookie, never in local storage. Reloading or logging out automatically locks the folder again.

Incidentally, a wrong passphrase is reliably detected without any password having to be stored anywhere: the safe simply won't open with it, and the seal on the encrypted data raises the alarm.

## Your responsibility — and it's real

End-to-end encryption means: the protection is in your hands, because the key is in your hands. Which leads to the most important sentence in this article:

> **If you lose both your passphrase _and_ your recovery key, the contents of that folder or project are gone for good.**

For good means exactly that. There's no "reset password", no support route, no emergency key and no restore from backup. We have nothing we could help with — and that is precisely the point. A back door for us would be a back door for everyone else too. With a high-privacy project the stakes are potentially higher than with a single folder, because the entire project content is affected in one go.

So, before you write the first sentence into such a folder or project:

- **Passphrase into the password manager**, right away and not "later". It's not your bun.ink password, but an additional, separate passphrase.
- **Save the recovery key** while it's on screen — password manager, encrypted note, or printed out and kept somewhere you'd keep identity documents. It's only shown once.
- **Two places instead of one.** The passphrase and the recovery key are each other's backup. Store them so that a single lost device doesn't take both with it.
- **Practise once.** Reload the page and unlock the folder again — ideally once with the passphrase and once with the recovery key. That way you know both really work, while the folder is still empty.

You can change the passphrase at any time later (via the folder's context menu). The folder key stays the same, nothing needs re-encrypting — and your recovery key remains valid, because it's tied to the folder key, not to the passphrase.

## What high privacy costs

Because the server can't read this content, it can't do anything with it either. That's not a missing feature but the logical consequence — though you should know about it before you create one. The following points apply equally to folders and projects:

- **No GitHub.** Documents in high-privacy folders are never synced to GitHub; they appear in no push, no pull and no commit, while the rest of the project remains linkable. A high-privacy **project** can't be linked to GitHub in the first place — there's nothing unencrypted in it that could be synced. So Git-based versioning, branches and working with AI agents aren't available for these texts.
- **Search only locally and only when unlocked.** Project-wide search can't search encrypted documents. If the folder is unlocked, bun.ink searches locally in your browser as well; if it's locked, those documents are skipped.
- **No version preview and no comparison.** Versions are saved — encrypted and secure — but preview and line-by-line comparison are currently disabled for these documents.
- **Locked again after every reload.** There is deliberately no local cache and no restoring of open tabs for these documents, so that no plain text is left behind on the device. So you enter the passphrase once per session.
- **In a save conflict, reloading wins.** If you've changed the same text in two windows at once, the server can't compare the versions. Instead of merging, it's a case of: reload, unlock, carry on.
- **The decision is final.** A folder or project is either high-privacy or normal from the very beginning. Encryption can't be switched on or off afterwards, and documents can't be moved between the encrypted and the normal area — the key wouldn't fit at the destination. If you want to switch, you copy the text by hand into a newly created folder or a newly created project. Subfolders are allowed and inherit the protection; a high-privacy folder inside a high-privacy project, on the other hand, isn't possible — a project is either fully protected or not at all.
- **Names and sizes remain visible.** As in layer 1, folder and document names, timestamps, version counts and word counts are not encrypted. Only the content is.
- **Your device remains your job.** Encryption in the browser doesn't help against a machine with malware or an unattended, unlocked laptop. While you're writing, the text is inevitably readable — on your screen.

## What we recommend

For most projects — book manuscript, articles, documentation — the normal folder is the right place. Your content is stored encrypted there, and you keep everything that makes bun.ink strong: [versioning via GitHub](/blog/using-github-with-bun-ink), comparisons, branches, [AI support](/blog/ai-controlled-writing-partner).

Use high privacy deliberately and selectively, for the things that really are nobody else's business: a diary, therapy notes, protected sources, very personal drafts. For occasional private content alongside an otherwise normal project, a single "Diary" **folder** is usually enough. If, on the other hand, you consistently write everything in a self-contained, thoroughly private context — a personal diary project with many documents, say, or notes from therapy — a dedicated **high-privacy project** is often the tidier choice, because then documents sitting directly in the project are automatically protected too. In both cases the rule is: don't encrypt everything, encrypt the right thing.

And quite apart from which folder you write in: your texts are stored in Europe, they're stored encrypted, they're backed up daily — and they stay yours. As Markdown, in an open format, exportable at any time. That's exactly [why we built bun.ink](/blog/why-bun-ink-exists).
