---
title: Warum Texte ein Repository verdienen – und was bun.ink daraus macht
date: 2026-07-15
description: Die Geschichte hinter bun.ink – warum Texte ein Repository verdienen, was das mit AI-Agenten zu tun hat und wie ein Schreib-Workflow aussieht, bei dem keine Version mehr verloren geht.
---

bun.ink ist aus einer einfachen Beobachtung entstanden: Die mächtigsten Werkzeuge für Versionierung und Zusammenarbeit an Texten gibt es längst. Sie heissen Git und GitHub, und Entwickler arbeiten seit Jahrzehnten damit – aber wer sie für seine Texte nutzen wollte, musste bisher im Terminal leben. Schreib-Apps wiederum fühlen sich wunderbar an, behandeln die Geschichte eines Textes aber als Nebensache: Es existiert immer nur der aktuelle Stand, alles davor ist weg oder vergraben in Duplikaten und „Versionen"-Menüs.

bun.ink schliesst genau diese Lücke: eine Schreib-App im Browser, die sich anfühlt wie ein moderner Editor – und deine Texte als Markdown in einem GitHub-Repository versioniert. Ohne Terminal, ohne Git-Vorwissen.

## Schreib-App vorne, Repository hinten

In bun.ink schreibst du wie in jeder guten Schreib-App: fokussierter Editor, Formatierung, [Textschnipsel](/blog/text-snippets-for-fast-writing), [Schreibstatistiken](/blog/writing-statistics-that-motivate). Der Unterschied liegt darunter:

- **Jedes Dokument ist Markdown** – ein offenes Format, das dir gehört. Kein Lock-in, kein proprietäres Dateiformat.
- **Speichern erzeugt Commits, Branches sind Textfassungen** – jede gesicherte Fassung bleibt erhalten, und radikale Überarbeitungen probierst du auf einem eigenen Zweig aus, während die Hauptfassung unberührt bleibt. Den kompletten Workflow dazu erklären wir in [GitHub richtig nutzen](/blog/using-github-with-bun-ink).
- **Alles läuft im Browser**, [auch auf dem Smartphone](/blog/using-bun-ink-on-mobile), und deine Daten liegen in Europa.

Falls dir Begriffe wie Commit, Branch und Merge noch nichts sagen: In [Git und GitHub einfach erklärt](/blog/git-and-github-for-writers) haben wir sie in Ruhe und ohne Programmierer-Vokabular aufgeschrieben. Hier soll es um die Frage gehen, warum wir das Ganze überhaupt gebaut haben.

## Der eigentliche Grund: deine Texte werden AI-ready

Es gibt neben der Versionierung einen zweiten, aktuelleren Grund, warum Texte in ein Repository gehören: **AI-Agenten arbeiten heute auf Repositories.**

Werkzeuge wie Claude Code oder GitHub Copilot können ein komplettes Repository lesen, Änderungen vorschlagen und als Pull Request zurückgeben. Wenn deine Texte in GitHub liegen, gilt das plötzlich auch für dein Buchmanuskript, deine Dokumentation oder deine Artikelsammlung:

- Ein Agent liest dein ganzes Manuskript und prüft Konsistenz über alle Kapitel hinweg.
- Eine Überarbeitung landet als eigener Branch – du vergleichst sie Zeile für Zeile mit deiner Fassung und übernimmst nur, was dich überzeugt.
- Nichts davon überschreibt jemals deinen Text. Du bleibst die Autorin oder der Autor, der Agent macht Vorschläge.

Ein Word-Dokument kann das nicht. Ein Repository schon. bun.ink macht das Repository für Schreibende benutzbar. Wie du einen Agenten mit klaren Regeln und einer `AGENTS.md` einsetzt, ohne die Kontrolle abzugeben, zeigt der Artikel [KI als kontrollierter Schreibpartner](/blog/ai-controlled-writing-partner).

## Für wen wir bauen

bun.ink ist für Menschen, die schreiben und denen ihre Texte wichtig genug für echte Versionierung sind: Technical Writer und Dokumentations-Teams, Entwickler mit Schreibprojekten, Markdown-Fans – und alle, die neugierig sind, was passiert, wenn man einem AI-Agenten ein Manuskript anvertraut, ohne die Kontrolle abzugeben.

Du kannst bun.ink [14 Tage kostenlos testen](/signup) – ohne Kreditkarte. Und weil alles Markdown in deinem eigenen GitHub-Repository ist, gehören dir deine Texte an Tag 1 genauso wie an Tag 1000.
