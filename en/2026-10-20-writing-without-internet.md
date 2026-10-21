---
title: Writing Offline — With Text That Doesn't Get Lost
date: 2026-10-20
description: How bun.ink keeps working on the train, in a holiday cottage or on a plane, what works offline, what doesn't, and what happens to your text when the connection comes back.
sourceHash: 2a479f0cbdff96eda09bc692524ae65147023e1ca3d86540003467a95e89e06b
---

The best writing hours often happen where the network ends: on the train, in a holiday cottage, on a plane. That's usually where a browser-based writing app gives up – the page won't load, and whatever you typed before the dead zone is stuck somewhere between tab and server.

[bun.ink](https://bun.ink) is a writing editor for Markdown, with your own GitHub repository behind it if you want one. As of this week, it keeps working without a connection too – for a few days at a time, in the browser tab, as an installed app on your computer and on your iPhone. The principle behind it: **what you write stays on your device until the server has it safely – and nothing is silently overwritten.**

## Preparing, once

Only what's already on your device is available offline. There are two ways to get it there:

- **By hand:** right-click a project in the sidebar (long-press on a phone) and choose **Available offline**. A small cloud next to the project name shows that it's ready.
- **Automatically:** under **Settings → Account → Offline on this device**, turn on **Make opened projects available offline automatically**. From then on, every project you open on this device comes along by itself.

The automatic option is deliberately a per-device switch rather than simply always on. The copy sits readable in the browser's storage. On your own laptop that's exactly right; on the computer in the library it isn't.

After that there's nothing more to do. As long as you're online, bun.ink keeps the copy up to date: when you open the project, after every save, and whenever you create a folder or rename something in it.

On iPhone and iPad there's one peculiarity: iOS may delete a browser tab's data after a few days without use. So add bun.ink as an app via **Share → Add to Home Screen** and make the project available offline **there**. The app has its own, protected storage.

## When the network drops out

You'll barely notice. If the connection disappears while you're writing in a project that's available offline, you simply keep writing. All other projects can only be read and exported until the connection returns. That way no text you didn't want to leave behind stays on someone else's computer. If you open bun.ink with no network, it loads the editor from the copy on your device, with the note **Offline — you are working on the copy stored on this device.**

Offline you can:

- edit, close and reopen existing documents,
- create, rename, move, export and delete new documents,
- unlock high-privacy areas with your passphrase and write in them,
- search within the project and use snippets.

You can see at a glance what has been changed offline: the dot on the tab stays red, and in the explorer a small cloud appears next to the document. It means: **saved only on this device so far.** You don't need to save anything yourself – bun.ink continuously stores every state on the device, even if you close the window.

Everything that needs the server waits: GitHub, the version history, the view of changes, creating projects and folders, renaming or deleting existing documents. Clicking one of them says **Not available offline**, and you stay in the editor. The same goes for links to pages such as the settings or the blog. Offline, they no longer lead nowhere.

## Back online

When the connection returns, bun.ink uploads your changes. If you had the app open without a network, a note says **You're back online**, and **Continue online** brings back the normal editor. The switch happens on a click on purpose, so it doesn't interrupt you mid-sentence. After that, clouds and red dots disappear, and bun.ink reports how many offline changes were uploaded.

It gets interesting when you've edited the same document on a second device in the meantime. In that case bun.ink overwrites nothing. It shows the dialog **Document was saved elsewhere**:

- **Save local version** files your offline draft as a version in the history. The document then carries the newer state from the other device, and you can restore your version at any time.
- **Overwrite anyway** takes your offline draft as the new state.

With high-privacy documents, the text only ever leaves the device encrypted anyway. That's why bun.ink can upload it even when the area is locked. You only need to unlock it to compare in the event of a conflict, because only plain text can be compared. Until then, your text stays on the device.

## Fourteen days

A device may write offline for fourteen days after its last contact with the server. The deadline renews itself with every online contact; in the final four days a note reminds you of it. If it expires, you can still read and export, you just can't edit any more until the device has been online once. What you've written stays on the device in the meantime. The deadline is signed by the server – it can't be extended in storage or by putting the clock back.

## What you should know

- **Clearing browser data clears the copy too.** As long as **Changes waiting to upload** is showing, don't delete any website data. Afterwards everything is on the server.
- **Signing out tidies up.** The copies and anything still waiting are deleted from the device – bun.ink warns you beforehand if something is still pending. The automatic logout after inactivity pauses while you're offline, so you can't lock yourself out.
- **Signing in needs a connection.** If you're signed out, all you'll see offline is a notice. As soon as the network is back, you're taken to the sign-in page automatically.

Exactly what is stored on your device is described in the [privacy policy](/privacy) under "Offline copies on your device".

## More on this

Step by step, with all the special cases, it's covered in the [handbook chapter "Writing Offline"](https://github.com/VisionX-Development/writing-with-bunink/blob/main/en/12-writing-without-internet.md). How bun.ink encrypts high-privacy areas and protects your texts in general is described in the article [How bun.ink protects your texts](/blog/how-bun-ink-protects-your-texts). How to use bun.ink on your phone is covered in [Using bun.ink on a Mobile Device](/blog/using-bun-ink-on-mobile).
