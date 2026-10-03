---
title: Warum Texte ein Repository verdienen – und was bun.ink daraus macht
date: 2026-07-15
description: Die Geschichte hinter bun.ink und wie es unter der Haube funktioniert – Markdown im eigenen GitHub-Repository, Commits als bewusste Fassungen und Überarbeitungen von Menschen oder KI-Agenten, die du Stelle für Stelle entscheidest.
---

bun.ink ist aus einer einfachen Beobachtung entstanden: Die mächtigsten Werkzeuge für Versionierung und Zusammenarbeit an Texten gibt es längst. Sie heissen Git und GitHub, und Entwickler arbeiten seit Jahrzehnten damit – aber wer sie für seine Texte nutzen wollte, musste bisher im Terminal leben. Schreib-Apps wiederum fühlen sich wunderbar an, behandeln die Geschichte eines Textes aber als Nebensache: Es existiert immer nur der aktuelle Stand, alles davor ist weg oder vergraben in Duplikaten und „Versionen"-Menüs.

bun.ink schliesst genau diese Lücke: eine Schreib-App im Browser, die sich anfühlt wie ein moderner Editor – und deine Texte als Markdown in einem GitHub-Repository versioniert. Ohne Terminal, ohne Git-Vorwissen.

## Schreib-App vorne, Repository hinten

In bun.ink schreibst du wie in jeder guten Schreib-App: fokussierter Editor, Formatierung, [Textschnipsel](/blog/text-snippets-for-fast-writing), [Schreibstatistiken](/blog/writing-statistics-that-motivate). Der Unterschied liegt darunter:

- **Die Datei ist Markdown, und sie gehört dir.** Gespeichert wird kein eigenes Format, sondern genau die `.md`-Datei, die in deinem Repository liegt. Wer bun.ink nicht mehr nutzt, hat seine Texte trotzdem – auf GitHub und als ZIP-Export.
- **Ein Commit ist eine bewusste Fassung.** Speichern sichert deinen Stand in bun.ink, mit einem Versionsverlauf pro Dokument. Was du festhalten willst, wird ein Commit mit Nachricht in deinem Repository. Branches sind Textfassungen: Eine radikale Überarbeitung probierst du auf einem eigenen Zweig aus, während die Hauptfassung unberührt bleibt. Den Ablauf erklären wir in [GitHub richtig nutzen](/blog/using-github-with-bun-ink).
- **Die Geschichte ist lesbar.** Im [Commit-Browser](/blog/browsing-your-commit-history) vergleichst du zwei beliebige Stände – zwei Commits oder einen Commit mit deinem aktuellen Text – als Text und nicht als Diff-Syntax.
- **Alles läuft im Browser**, [auch auf dem Smartphone](/blog/using-bun-ink-on-mobile). bun.ink selbst läuft in Frankfurt; was du nach GitHub pushst, liegt in deinem GitHub-Konto.

Falls dir Begriffe wie Commit, Branch und Merge noch nichts sagen: In [Git und GitHub einfach erklärt](/blog/git-and-github-for-writers) haben wir sie in Ruhe und ohne Programmierer-Vokabular aufgeschrieben. Hier soll es um die Frage gehen, warum wir das Ganze überhaupt gebaut haben.

## Der eigentliche Grund: deine Texte werden AI-ready

Es gibt neben der Versionierung einen zweiten, aktuelleren Grund, warum Texte in ein Repository gehören: **AI-Agenten arbeiten heute auf Repositories.**

Werkzeuge wie Claude Code oder GitHub Copilot können ein komplettes Repository lesen, Änderungen vorschlagen und als Pull Request zurückgeben. Wenn deine Texte in GitHub liegen, gilt das plötzlich auch für dein Buchmanuskript, deine Dokumentation oder deine Artikelsammlung:

- Ein Agent liest dein ganzes Manuskript und prüft Konsistenz über alle Kapitel hinweg.
- Seine Überarbeitung – oder die deines Lektorats – kommt als Pull Request. bun.ink zeigt sie dir **Stelle für Stelle**: übernehmen, verwerfen oder eine eigene Fassung dagegensetzen. Verworfenes geht als Commit an den Pull Request zurück, und gemergt wird erst, wenn über jede Stelle entschieden ist. Wie das im Alltag aussieht, steht in [Das Lektorat kommt zum Text](/blog/reviews-as-pull-requests).
- Nichts davon überschreibt jemals deinen Text. Du bleibst die Autorin oder der Autor, der Agent macht Vorschläge.

Ein Word-Dokument kann das nicht. Ein Repository schon. bun.ink macht das Repository für Schreibende benutzbar. Wie du einen Agenten mit klaren Regeln und einer `AGENTS.md` einsetzt, ohne die Kontrolle abzugeben, zeigt der Artikel [KI als kontrollierter Schreibpartner](/blog/ai-controlled-writing-partner).

Seit August 2026 gibt es dafür noch einen Grund. Anthropic versieht Text neuer Claude-Modelle mit einem unsichtbaren Wasserzeichen – Teil der Transparenzpflichten nach Artikel 50 des EU AI Act. Die Markierung unterscheidet nicht, ob ein Modell einen Absatz geschrieben oder nur Kommas gesetzt hat. Sie sagt, *dass* ein Modell beteiligt war, nicht, *wer* geschrieben hat. Das zeigt nur die Entstehung: eine Commit-Historie, in der ein Kapitel über Wochen in kleinen Schritten wächst. Mehr dazu in [Deine Arbeit beweisen](/blog/proving-you-wrote-it-yourself).

## Unter der Haube

Für alle, die wissen wollen, worauf sie sich einlassen:

- **Markdown ist die einzige Quelle.** Der Editor (TipTap auf ProseMirror) liest Markdown und schreibt Markdown. Frontmatter, HTML-Kommentare, Tabellen und fest umbrochene Absätze kommen beim Speichern Byte für Byte zurück, und das blosse Öffnen ändert keine Datei. Wer ein bestehendes Docs-Repository öffnet, bekommt keinen Vergleich voller Leerzeilen und Backslashes. Notizen an eine Textstelle stehen als `<!-- bun.ink:note -->` in der Datei und sind in jeder anderen Ansicht unsichtbar – siehe [Metadaten und Notizen](/blog/metadata-and-notes-in-markdown).
- **Zwei Speicherorte, klar getrennt.** Der Hauptstand liegt in bun.ink, mit Versionsverlauf. Ein Branch läuft in deinem Browser und wird als Commit direkt auf den GitHub-Branch gespeichert – nie in die bun.ink-Datenbank.
- **GitHub über die REST-API.** bun.ink spricht als OAuth-App mit GitHub, mehrere Konten pro Person sind möglich. Die Zugangstoken liegen mit AES-256-GCM verschlüsselt auf dem Server, nie im Browser.
- **Verschlüsselung in zwei Schichten.** Inhalte liegen serverseitig mit AES-256-GCM verschlüsselt in der Datenbank. Für Texte, die niemand lesen soll, gibt es High-Privacy-Ordner und -Projekte: Verschlüsselt wird im Browser, der Schlüssel entsteht aus deiner Passphrase per Argon2id, und es gibt einen Wiederherstellungsschlüssel. Diese Inhalte können wir nicht lesen, und sie gehen nie zu GitHub. Details in [Wie bun.ink deine Texte schützt](/blog/how-bun-ink-protects-your-texts).
- **Gebaut mit** SvelteKit und Svelte 5; Konten und Daten bei Appwrite in Frankfurt.

## Für wen wir bauen

bun.ink ist für Menschen, die schreiben und denen ihre Texte wichtig genug für echte Versionierung sind: Technical Writer und Dokumentations-Teams, Entwickler mit Schreibprojekten, Markdown-Fans – und alle, die neugierig sind, was passiert, wenn man einem AI-Agenten ein Manuskript anvertraut, ohne die Kontrolle abzugeben.

Du kannst bun.ink [14 Tage kostenlos testen](/signup) – ohne Kreditkarte. Und weil alles Markdown in deinem eigenen GitHub-Repository ist, gehören dir deine Texte an Tag 1 genauso wie an Tag 1000.
