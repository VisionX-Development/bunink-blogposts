---
title: Writing Without the Internet – With Text That Doesn't Get Lost
date: 2026-10-20
description: How bun.ink keeps working on the train, in a holiday cottage or on a plane, what you can do offline, what you can't, and what happens to your text when the connection comes back.
sourceHash: a35c09eef6a525c9566a77a55baab0b85ca2186db7c97e46ac602cf8ac549e87
---

The best writing hours often happen where the network ends: on the train, in a holiday cottage, on a plane. A writing app in the browser is usually done for at that point – the page won't load, and whatever you typed before the dead zone is stuck somewhere between tab and server.

[bun.ink](https://bun.ink) is a writing editor for Markdown, with your own GitHub repository behind it if you want one. As of this week it keeps running without a connection too, for a few days at a time, in the browser tab, as an installed app on your computer and on your iPhone. The rule behind it: **what you write stays on your device until the server has it safely – and nothing is overwritten silently.**

## Preparing, once

Offline only gives you what was already on the device. There are two ways to get it there:

- **By hand:** right-click a project in the sidebar (long-press on your phone) and choose **Available offline**. A small cloud next to the project name shows that it's ready.
- **Automatically:** under **Settings → Account → Offline on this device**, turn on **Make opened projects available offline automatically**. Every project you open on this device then comes along by itself.

The automatic option is deliberately a per-device switch rather than simply always on. The copy sits readable in the browser's storage. On your own laptop that's exactly right; on a computer in the library it isn't.

After that there's nothing left to do. As long as you're online, bun.ink keeps the copy up to date: when you open a document, after every save, and when you create a folder or rename something in the project.

On iPhone and iPad there's one peculiarity: iOS can delete a browser tab's data after a few days without use. So add bun.ink via **Share → Add to Home Screen** as an app and make the project available offline **there**. The app has its own, protected storage.

## When the network drops out

You'll barely notice. If the connection disappears while you're writing, you simply keep writing. If you open bun.ink without a network, it loads the editor from the copy on your device, with the note **Offline — you are working on the copy stored on this device.**

Offline you can:

- edit, close and reopen existing documents,
- create new documents, rename, move, export and delete them again,
- unlock high-privacy areas with your passphrase and write in them,
- search within the project and use snippets.

You can see at a glance what has been changed offline: the dot on the tab stays red, and in the explorer a small cloud appears next to the document. It means: **saved only on this device so far.** You don't need to back anything up – bun.ink continuously stores every state on the device, even if you close the window.

Everything that needs the server waits: GitHub, the version history, the view of changes, creating projects and folders, renaming or deleting existing documents. Clicking one of them says **Not available offline**, and you stay in the editor. The same goes for links to pages such as the settings or the blog. Offline they no longer lead nowhere.

## Back online

When the connection returns, bun.ink uploads your changes. If you had the app open without a network, a note says **You're back online**, and **Continue online** brings up the normal editor. The switch happens deliberately on a click, so it doesn't interrupt you mid-sentence. After that the clouds and red dots disappear, and bun.ink reports how many offline changes were uploaded.

It gets interesting when you've changed the same document on a second device in the meantime. In that case bun.ink overwrites nothing. It shows the dialogue **Document was saved elsewhere**:

- **Save local version** puts your offline version into the history as a version. The document then carries the newer state from the other device, and you can restore your version at any time.
- **Overwrite anyway** takes your offline version as the new state.

With high-privacy documents, the text only ever leaves the device encrypted anyway. That's why bun.ink can upload it even when the area is locked. You only need to unlock it to compare in the event of a conflict, because only plain text can be compared. Until then your text stays on the device.

## Fourteen days

A device may write offline for fourteen days after its last contact with the server. The deadline renews itself with every online contact, and during the last four days a note reminds you of it. If it expires, you can still read and export, you just can't edit any more until the device has been online once. What you've written stays on the device in the meantime. The deadline is signed by the server; it can't be extended in storage, nor by setting the clock back.

## What you should know

- **Clearing browser data also clears the copy.** As long as **Changes waiting to upload** is showing, don't delete any website data. After that, everything is on the server.
- **Signing out tidies up.** The copies and anything still waiting are deleted from the device – bun.ink warns you beforehand if something is still pending. The automatic logout after inactivity is paused offline, so you don't lock yourself out.
- **Signing in needs a connection.** If you're signed out, offline you'll only see a note. As soon as the network is back, it goes to the sign-in page by itself.

Exactly what is stored on your device is described in the [privacy policy](/privacy) under "Offline copies on your device".

## More on this

Step by step, with all the special cases, it's in the [handbook, chapter "Writing without an internet connection"](https://github.com/VisionX-Development/writing-with-bunink/blob/main/en/12-writing-without-internet.md). How bun.ink encrypts high-privacy areas and otherwise protects your texts is described in the article [How bun.ink protects your texts](/blog/how-bun-ink-protects-your-texts). How to use bun.ink on your phone is covered in [Using bun.ink on a Mobile Device](/blog/using-bun-ink-on-mobile).
