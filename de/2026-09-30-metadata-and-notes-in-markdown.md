---
title: Metadaten und Notizen – was in einer Markdown-Datei ausser dem Text steckt
date: 2026-09-30
description: Frontmatter für Titel und Status am Dateianfang, Notizen als Merkzettel an einer Textstelle. Wie beides in bun.ink funktioniert, wo es gespeichert wird und wer es sieht.
---

Eine Markdown-Datei ist Text. Aber nicht nur: Oft soll sie auch sagen, wie sie heisst, in welchem Stadium sie ist oder was an einer Stelle noch fehlt. [bun.ink](http://bun.ink) kennt dafür zwei Werkzeuge, die beide in der Datei selbst leben – **Metadaten** und **Notizen**.

## Kurz: der Unterschied

**Metadaten** (Frontmatter)

- stehen ganz oben in der Datei, genau ein Block
- sagen etwas über das ganze Dokument: Titel, Status, Datum
- sind für Programme gedacht: Website, Inhaltsverzeichnis, KI-Agent usw.
- erscheinen auf GitHub als Tabelle über dem Text
- einfügen mit **Format → Dokument → Metadaten einfügen**

**Notizen**

- stehen an beliebiger Stelle im Text, beliebig viele
- sagen etwas über eine bestimmte Textstelle
- sind für dich gedacht, beim Schreiben
- sind auf GitHub unsichtbar, stehen nur in den Rohdaten der datei
- einfügen mit **Format → Dokument → Notiz einfügen** oder einen von dir gewählten Shortcut-Tastenkürzel

## Metadaten: der Block am Anfang

Frontmatter ist ein Block zwischen zwei Zeilen mit drei Bindestrichen, ganz am Anfang der Datei:

```markdown
---
title: Das zweite Kapitel
status: draft
---
```

Website-Generatoren wie Hugo, Jekyll oder Astro lesen daraus Titel und Datum, unser eigenes [Handbuch](https://github.com/VisionX-Development/writing-with-bunink) seine Kapitelnummer und den Status. Welche Felder du brauchst, bestimmt das Programm, das die Datei weiterverarbeitet.

In [bun.ink](http://bun.ink) ist der Block ein eigener Kasten mit der Beschriftung **Metadaten**. Er landet immer am Dateianfang, egal wo der Cursor steht, und es gibt nie mehr als einen – Programme lesen ohnehin nur den ersten. Ein **×** entfernt ihn wieder. Und weil drei selbst getippte Bindestriche mitten im Text eine Trennlinie sind, legst du Metadaten immer über das Menü an.

Das Wichtigste passiert unsichtbar: [bun.ink](http://bun.ink) speichert den Block Zeichen für Zeichen zurück. Wer eine Datei aus einem bestehenden Repository öffnet, findet nach dem Speichern dasselbe Frontmatter vor – keine verrutschten Leerzeilen, keine eingefügten Backslashes.

## Notizen: der Merkzettel an der Textstelle

„Quelle nachtragen.“ „Dialog wirkt hölzern.“ „Mit Kapitel 4 abgleichen.“ Solche Anmerkungen gehören an eine Stelle, aber nicht in den Text. Genau dafür gibt es Notizen.

Setz den Cursor in einen Absatz und wähle **Format → Dokument → Notiz einfügen**, oder drück **Ctrl+N bzw. leg ein eigenes Tastenkürzel dafür fest**. Die Notiz erscheint als farbige Karte direkt hinter dem Absatz – nie mitten darin – und du schreibst los. Das Tastenkürzel lässt sich in den Einstellungen unter **Editor** ändern oder abschalten. Unter Windows und Linux solltest du das tun: dort behält der Browser das Kürzel Strg+N für ein neues Fenster.

In der Datei steht die Notiz als HTML-Kommentar mit einer Kennung:

```markdown
Anna stand am Fenster und zählte die Züge.

<!-- bun.ink:note
Wie viele Züge fahren nachts wirklich? Fahrplan prüfen.
-->
```

### Diese Form hat drei Vorteile:

- **Sie ist überall unsichtbar**, wo die Datei angezeigt wird: in der GitHub-Vorschau, auf einer Website, in anderen Markdown-Programmen.
- **Sie reist mit dem Text.** Die Notiz wird mit dem Dokument gespeichert, landet im selben Commit und bleibt an ihrer Stelle, wenn du drumherum schreibst. Kein zweiter Speicherort, der verloren gehen könnte.
- **Sie zählt nicht als Text.** Wortzählung und Schreibstatistik lassen Notizen aus; die Suche findet sie trotzdem – praktisch, um alle offenen „Quelle nachtragen“ eines Projekts wiederzufinden.

## Eine Warnung: unsichtbar heisst nicht geheim

Eine Notiz ist in der fertigen Ansicht verborgen, in der Datei aber lesbar. Wer die Rohdatei, einen Commit oder einen Vergleich ansieht, sieht auch sie. In einem öffentlichen Repository sind deine Notizen öffentlich, und ein Lektorat im selben Repository liest sie mit. Was niemand sehen darf, gehört nicht in eine Notiz. Für Anmerkungen, die tatsächlich an jemand anderen gehen, gibt es den [Review über Pull Requests](/blog/reviews-as-pull-requests): Dort stehen Kommentare auf GitHub am Pull Request, nicht im Text. Notizen sind dein eigener Merkzettel.

## Übrigens: fremde Kommentare bleiben stehen

Viele Dateien in Docs-Repositories bringen schon HTML-Kommentare mit – ausgeblendete TODOs, Anweisungen für Prüfprogramme. [bun.ink](http://bun.ink) zeigt sie im Editor grau an und speichert sie unverändert zurück. Das klingt selbstverständlich, andere Schreibeditoren verlieren solche Kommentare beim Speichern einfach.

Wie alles im Detail funktioniert, steht im Handbuch im Kapitel [Metadaten und Notizen](https://github.com/VisionX-Development/writing-with-bunink/blob/main/de/11-metadaten-und-notizen.md).
