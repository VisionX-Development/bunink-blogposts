---
title: Warum Texte ein Repository verdienen – und was bun.ink daraus macht
date: 2026-07-15
description: Die Geschichte hinter bun.ink und wie es unter der Haube funktioniert.
update: 2026-11-22
---

bun.ink ist aus einer einfachen Beobachtung heraus entstanden: Die mächtigsten Werkzeuge für Versionierung und Zusammenarbeit an Texten gibt es bereits. Sie heissen Git und GitHub, und Entwickler arbeiten seit Jahrzehnten damit – aber wer sie für seine Texte nutzen wollte, musste diese zusätzlich vom Terminal aus bearbeiten. Schreib-Apps wiederum fühlen sich wunderbar an, behandeln die Geschichte eines Textes aber als Nebensache: Es existiert immer nur der aktuelle Stand, alles davor ist weg oder vergraben in Duplikaten und „Versionen"-Menüs.

bun.ink schliesst diese Lücke: eine Schreib-App im Browser, die sich anfühlt wie ein moderner Editor – und deine Texte als Markdown bereits in der App versioniert. Das Versionierungssystem ist selbst programmiert aber an dem bekannten System von Git angelehnt. So können wir beides garantieren: ein funktionierendes Versionssystem und die sichere Verschlüsselung und Speicherung deiner Texte auf einem europäischen Server. Danebern können Dokumente und ganze Projekte auch auf einem lokalen Computer gespeichert und synchronisiert werden. Eine Verknüfung zu einem GitHub-Repository ist optional.

## Schreib-App vorne, Versionskontrolle hinten

In bun.ink schreibst du wie in jeder guten Schreib-App: fokussierter Editor, Formatierung, [Textschnipsel](/blog/text-snippets-for-fast-writing), [Schreibstatistiken](/blog/writing-statistics-that-motivate). Der Unterschied liegt darunter:

- **Die Datei ist Markdown, und sie gehört dir.** Gespeichert wird kein eigenes Format, sondern genau die `.md`-Datei, die in deinem Projekt liegt. Wer bun.ink nicht mehr nutzen möchte, hat seine Texte trotzdem – jederzeit als ZIP-Export.
- **Lege Meilentein an für eine Änderung oder neue Fassung.** Speichern sichert einen neuen Stand auf diesem Meilenstein in bun.ink.
- **Die Geschichte ist lesbar.** Der Verlauf dieser Meilensteine ist im Verlaufs- Tab jederzeit sichtbar. Zwei beliebige Meilensteine können hier in einem Diff- Editor mit einander verglichen werden. 
- **Alles läuft im Browser**, [auch auf dem Smartphone](/blog/using-bun-ink-on-mobile). [bun.ink](http://bun.ink) kann als Progressive Web App geladen werden. bun.ink's Server stehen in Frankfurt;

## Ein weiterer Grund: der Arbeitsverlauf deiner Texte ist klar nachvollziehbar

Neben der Erleichterung beim Schreibprozess bietet Versionierung einen weiteren ganz aktuellen Vorteil.

Seit August 2026 sind z.B. Anthropics neuere Claude-Modelle weltweit mit einem unsichtbaren Wasserzeichen ausgestattet – angestossen durch die Transparenzpflichten nach Artikel 50 des EU AI Act. Die Markierung unterscheidet nicht, ob ein Modell einen Absatz geschrieben oder nur Kommas gesetzt hat oder ggf. nur eine Rechtschreibprüfung durchgeführt wurde. Sie sagt, *dass* ein Modell an einem Text beteiligt war. Verlager verlangen bereits jetzt Nachweise, dass ein Text ohne KI geschrieben wurde. Die Beweispflicht liegt damit beim Autor. Ohne eine Versions- Geschicht ist dies so gut wie unmöglich. Allerdings, mit Versionsgegeschichte kann er seinen gesamten Schaffensprozess minutiös nachweisen, auch wenn er vielleicht ein Programm zur Rechtschreibkorrektur verwendet hat. 

## Unter der Haube

Für alle, die wissen wollen, worauf sie sich einlassen:

- **Markdown ist die einzige Quelle.** Der Editor (TipTap auf ProseMirror) liest Markdown und schreibt Markdown. Frontmatter, HTML-Kommentare, Tabellen und fest umbrochene Absätze kommen beim Speichern Byte für Byte zurück, und das blosse Öffnen ändert keine Datei. Wer ein bestehendes Docs-Projekt öffnet, bekommt keinen Vergleich voller Leerzeilen und Backslashes. Notizen an eine Textstelle stehen als `<!-- bun.ink:note -->` in der Datei und sind in jeder anderen Ansicht unsichtbar – siehe [Metadaten und Notizen](/blog/metadata-and-notes-in-markdown).
- **Zwei Speicherorte.** Der Hauptstand liegt sicher verschlüsselt auf einem europäischen Server in bun.ink, hierauf kann von allen Geräten die einen Browser installiert haben zugegriffen werden, auch eine . Es gibt aber auch die Möglichkeit ein Projekt lokal auf einem Computer zu speichern und zu synchronisieren. 
- **Verschlüsselung in zwei Schichten.** Inhalte liegen serverseitig mit AES-256-GCM verschlüsselt in der Datenbank. Für Texte, die niemand lesen soll, gibt es **High-Privacy-Ordner und -Projekte**: Verschlüsselt wird im Browser, der Schlüssel entsteht aus deiner Passphrase per Argon2id, und es gibt einen Wiederherstellungsschlüssel. Diese Inhalte können wir nicht lesen, und sie gehen nie zu GitHub. Details in [Wie bun.ink deine Texte schützt](/blog/how-bun-ink-protects-your-texts).
- **Gebaut mit** SvelteKit und Svelte 5; Konten und Daten bei Appwrite in Frankfurt.

## Für wen wir bauen

bun.ink ist für Menschen, die schreiben und denen ihre Texte wichtig genug für echte Versionierung sind: Technical Writer und Dokumentations-Teams, Entwickler mit Schreibprojekten, Markdown-Fans – und alle, die neugierig sind, was passiert, wenn man einem AI-Agenten ein Manuskript anvertraut, ohne die Kontrolle abzugeben.

Du kannst bun.ink [14 Tage kostenlos testen](/signup) – ohne Kreditkarte. Und weil alles Markdown in deinem eigenen GitHub-Repository ist, gehören dir deine Texte an Tag 1 genauso wie an Tag 1000.
