---
title: How bun.ink protects your texts – encryption explained simply
date: 2026-07-28
description: What happens to your texts before they're saved — server-side encryption for all documents, the high-privacy folder and the high-privacy project for your diary, and what you're responsible for yourself in all of this.
sourceHash: aa11674f2512781e1b6228f679fc4a2352c310429c6ea52d9276bc4c38d00646
---

A text is a personal thing. A half-finished chapter, research with sources no one is supposed to know about, a diary entry from a bad day — this isn't just any old data. That's why the question "Who can actually read this?" isn't a technical footnote for a writing app, but a question of trust.

This article answers it as precisely as possible — without jargon, but also without promises we can't keep.

## Two layers — one for everyone, one for your diary

bun.ink protects content on two levels, and it's important to keep them apart:

- **Layer 1 — server-side encryption.** Applies to every document, without you having to do or configure anything. Your texts don't sit in the database as readable plain text.
- **Layer 2 — the high-privacy folder or a high-privacy project.** A special type of folder or project that you create yourself. Its contents are encrypted **in your browser**. No one but you can read them — not even us.

Layer 1 is convenience without compromise. Layer 2 is maximum protection at a price you should be aware of. We'll explain both here, one after the other.

## First, briefly — what encryption actually does

Imagine a text that runs through a machine and comes out the other side as an unreadable jumble of characters. The machine needs a **key** to do this — a long, random number. With the same key, the jumble runs back into the original text. Without the key, it's practically impossible to reconstruct; not a puzzle you can solve with patience, but a calculation that even huge data centres couldn't crack within several human lifetimes.

For this, bun.ink uses **AES-256-GCM**, the standard method that banks, government agencies and HTTPS connections rely on too. Two of its properties are practically relevant for you:

- **Every save uses a fresh random value.** The same text saved twice produces two completely different jumbles of characters. So the stored data gives no clue that two documents contain the same content.
- **Every encrypted text carries a seal.** If someone alters the stored data by even a single character, the text can no longer be decrypted — the tampering is detected immediately, rather than silently delivering a corrupted text.

On top of that: **a separate key for each type of data.** Document contents, GitHub access tokens and backups each have their own. Whoever had one couldn't do anything with the other data. The keys never live in the program code and never in your repository, but exclusively in the server's configuration and in a password manager.

## Layer 1 — your texts don't sit in the database as plain text

When you save, your text goes into the database encrypted. The server encrypts it right before writing and decrypts it again after reading — in between, it's just a jumble of characters in the database. The same applies to saved versions (the snapshots of your text's history) and to your text snippets.

You won't notice **any** of this. Full-text search, version comparisons, conflict handling, GitHub sync: everything works exactly as before and without any noticeable delay — encryption of this kind operates in the range of milliseconds, not seconds.

What this protects you against:

- **A database leak.** Whoever gains access to the database has a jumble of characters, not texts.
- **A stolen or lost backup.** Backups contain the same encrypted data — and are additionally encrypted themselves.
- **Access via the database console.** Even someone poking around in there — today or as a future team member — won't see your content.

And now for the honest part, because this point determines whether you need Layer 2:

- **Layer 1 is not "no one can read it."** The server needs the key to show you your text in the editor. Whoever has access to the server configuration — that is, us as the operator — technically has access to the key as well. We don't do this, but encryption alone doesn't prevent it. This is precisely the gap that Layer 2 closes.
- **GitHub deliberately stays readable.** "Git for Writers" depends on your repository holding real, readable Markdown files — there you can open them on any device, and there [AI agents](/blog/ai-controlled-writing-partner) can work with them. An encrypted jumble of characters in the repo would be useless. So the encryption protects our database, not your GitHub account; your repository is governed by the access rights you set on GitHub itself (a private repository stays private).
- **Names and numbers stay visible.** Document, project and folder names, timestamps, version numbers and the approximate text length are not encrypted — they're needed so that lists, sorting and the tree view work. So don't name a folder after the secret it contains.

## Layer 2 — the high-privacy folder or a high-privacy project

For a diary, for confidential sources, for texts no one should ever see, there are two variants of **high privacy**. The difference from Layer 1 sounds small but is fundamental: here, encryption doesn't happen on the server but **in your browser** — before anything ever reaches our data centre. All that arrives at the server and in the database is a jumble of characters for which no key exists there.

When you create it, you choose how large the protected area should be:

- **High-privacy folder.** Protects exactly this one folder (and its subfolders) within an otherwise normal project. The rest of the project remains fully usable — including GitHub sync, which simply skips the encrypted documents.
- **High-privacy project.** Automatically protects the entire project, including documents that sit directly in the project and aren't inside any folder. In return, such a project can't be linked to GitHub at all — there'd be nothing syncable in it.

Cryptographically, both are identical: the same algorithm, the same process, the same rules. But a project and its folders can't be mixed — within a high-privacy project you can't create an additional high-privacy folder, that would be a key within a key. Everything described below for the "high-privacy folder" therefore applies unchanged to the high-privacy project as well.

This is true end-to-end encryption. We can't read this content, can't search it, can't restore it and can't hand it over to anyone — not even from backups, because there sits the same unreadable material.

Here's how it works, in simple terms:

1. When you create it, your browser generates a random **folder key**. It's used to encrypt and decrypt all documents in this folder.
2. You choose a **passphrase**. From it, the browser computes a second key that locks the folder key away as if in a safe. Only this locked safe is stored — the passphrase itself never leaves your browser and is never saved anywhere.
3. This computation is deliberately **compute-intensive** (Argon2id, a method designed specifically against password-guessing attacks). An attacker wanting to try millions of passphrases has to spend noticeable computing time and memory on each attempt. For you, unlocking takes less than a second.
4. After creation, bun.ink shows you a **recovery key** — **once**. This is the folder key itself, in text form. It opens the folder even if you've forgotten the passphrase.
5. When you open a document, bun.ink asks for the passphrase (or the recovery key). After that, you keep working as normal: editor, local search, word count. When you save, your browser encrypts again.
6. The unlocked key lives **only in the working memory** of this browser session — never in a cookie, never in local storage. A reload or logout automatically locks the folder again.

Incidentally, a wrong passphrase is reliably detected without any password having to be stored anywhere: the safe simply won't open with it, and the seal on the encrypted data raises the alarm.

## Your responsibility — and it's real

End-to-end encryption means: the protection rests with you, because the key rests with you. From this follows the most important sentence in this article:

> **If you lose both the passphrase _and_ the recovery key, the contents of this folder or project are gone for good.**

For good really means for good. There is no "reset password," no support route, no emergency key and no recovery from backup. We have nothing we could help with — and that's exactly the point. A back door for us would be a back door for everyone else too. With a high-privacy project, this potentially weighs more heavily than with a single folder, because there the entire project's contents are affected in one stroke.

So, before you write the first sentence into such a folder or project:

- **Passphrase into the password manager**, right away and not "later." It's not your bun.ink password, but an additional, separate passphrase.
- **Save the recovery key** while it's shown — password manager, encrypted note, or printed out somewhere you'd keep identity documents. It's shown only once.
- **Two places, not one.** The passphrase and recovery key are each other's backup. Keep them so that a single lost device doesn't take both with it.
- **Practise once.** Reload the page and unlock the folder again — ideally once with the passphrase and once with the recovery key. That way you know both really work while the folder is still empty.

You can change the passphrase at any time later (via the folder's context menu). The folder key stays the same and nothing needs to be re-encrypted — and your recovery key remains valid, because it's tied to the folder key, not to the passphrase.

## What high privacy costs

Because the server can't read this content, it can't do anything with it either. This isn't a missing feature but the logical consequence — but you should know it before you create one. The following points apply equally to folders and projects:

- **No GitHub.** Documents from high-privacy folders are never synced to GitHub; they don't appear in any push, any pull or any commit, while the rest of the project remains linkable. A high-privacy **project** can't be linked to GitHub in the first place — there's nothing unencrypted in it that could be synced. So version control via Git, branches and working with AI agents are not available for these texts.
- **Search only locally and only when unlocked.** Project-wide search can't search encrypted documents. If the folder is unlocked, bun.ink searches along locally in your browser; if it's locked, these documents are skipped.
- **No version preview and no comparison.** Versions are saved — encrypted and secure — but preview and line-by-line comparison are currently disabled for these documents.
- **Locked again after every reload.** For these documents there is deliberately no local cache and no restoring of open tabs, so that no plain text is left behind on the device. So you enter the passphrase once per session.
- **On a save conflict, reloading wins.** If you've changed the same text in two windows in parallel, the server can't compare the versions. Instead of a merge, it's then: reload, unlock, keep working.
- **The decision is final.** A folder or project is either high-privacy or normal from the start. You can't switch the encryption on or off afterwards, and documents can't be moved between the encrypted and normal areas — the key wouldn't fit at the destination anymore. If you want to switch, you copy the text by hand into a newly created folder or a newly created project. Subfolders are allowed and inherit the protection; a high-privacy folder inside a high-privacy project, on the other hand, isn't possible — a project is either entirely protected or not at all.
- **Names and sizes stay visible.** As in Layer 1, folder and document names, timestamps, number of versions and word counts are not encrypted. Only the content is.
- **Your device remains your responsibility.** Encryption in the browser doesn't help against a computer with malware or an unattended, unlocked laptop. While you're writing, the text is inevitably readable — on your screen.

## What we recommend

For most projects — a book manuscript, articles, documentation — the normal folder is the right place. Your content is stored there encrypted, and you keep everything that makes bun.ink powerful: [version control via GitHub](/blog/using-github-with-bun-ink), comparisons, branches, [AI support](/blog/ai-controlled-writing-partner).

Use high privacy deliberately and selectively for what really concerns no one else: a diary, therapy notes, protected sources, deeply personal drafts. For occasional private content alongside an otherwise normal project, a single "Diary" **folder** is usually enough. But if you consistently write everything within its own, entirely private context — say a personal diary project with many documents, or notes from therapy — a dedicated **high-privacy project** is often the tidier choice, because then documents sitting directly in the project are automatically protected too. In both cases: don't encrypt everything, encrypt the right things.

And regardless of which folder you write in: your texts sit in Europe, they're stored encrypted, they're backed up daily — and they remain yours. As Markdown, in an open format, exportable at any time. That's exactly [why we built bun.ink](/blog/why-bun-ink-exists).
