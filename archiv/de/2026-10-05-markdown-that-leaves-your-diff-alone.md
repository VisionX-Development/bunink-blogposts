---
title: Markdown, das deinen Diff in Ruhe lässt
date: 2026-10-05
description: Was der Editor von bun.ink zeigt, was in der Datei steht und warum eine fremde Datei nach dem Speichern Zeichen für Zeichen gleich bleibt – bis auf den Satz, den du geändert hast.
---

Wer Texte in einem Git-Repository pflegt, kennt das Problem: Du änderst in einem fremden README einen einzigen Satz, und der Commit zeigt dreissig geänderte Zeilen. Der Editor hat Listen neu eingerückt, Sternchen escaped, eine Tabelle neu ausgerichtet. Der eine Satz, um den es ging, geht im Diff unter.

[bun.ink](https://bun.ink) ist ein Schreibeditor für Markdown mit GitHub dahinter, und er folgt einer einfachen Regel: **Was du nicht anfasst, bleibt Zeichen für Zeichen, wie es in der Datei steht.**

## Was du siehst und was gespeichert wird

Im Editor siehst du formatierten Text, gespeichert wird Markdown. Formatieren kannst du auf drei Wegen:

- **Beim Tippen:** `#` und ein Leerzeichen am Zeilenanfang machen eine Überschrift, `-` eine Aufzählung, `1.` eine nummerierte Liste, `>` ein Zitat, Sternchen um ein Wort machen es kursiv oder fett.
- **Mit dem Format-Menü** in fünf Gruppen: **Text**, **Absatz**, **Blöcke**, **Dokument** (Metadaten und Notizen, die in keiner Vorschau erscheinen) und **Darstellung** (alles, was nur die Ansicht ändert, nie die Datei).
- **Mit der Formatierungs-Bubble**, die beim Markieren erscheint und deren Befehle du in den Einstellungen wählst.

Unterstreichen gibt es nicht, weil Markdown es nicht kennt. Wie die Datei genau aussieht, zeigt **Format → Darstellung → Markdown-Quelltext**.

## Drei Arten, eine Zeile zu beenden

Markdown kennt drei Zeilenenden mit verschiedener Bedeutung (CommonMark-Spezifikation, [Abschnitte 6.7 und 6.8](https://spec.commonmark.org/0.31.2/#hard-line-breaks)):

| In der Datei | Bedeutung | Im Editor |
|---|---|---|
| eine Leerzeile | neuer Absatz | Enter |
| zwei Leerzeichen oder `\` vor dem Zeilenende | neue Zeile im selben Absatz | Shift+Enter |
| ein einfaches Zeilenende | weicher Umbruch, gilt als Leerzeichen | lässt sich nicht tippen |

Der weiche Umbruch macht Diffs lesbar. Viele schreiben in Doku unter Git jeden Satz auf eine eigene Zeile – die Konvention heisst [Semantic Line Breaks](https://sembr.org/). Ändert sich ein Satz, zeigt der Diff genau diese eine Zeile. Im Editor ist ein weicher Umbruch ein Leerzeichen, der Absatz fliesst wie beim Leser. Beim Speichern kommt jedes Zeilenende so zurück, wie es in der Datei stand.

Markdown-Zeichen sind im Editor gewöhnlicher Text: Zwei getippte Leerzeichen bleiben zwei Leerzeichen. Einen Umbruch im Absatz machst du mit Shift+Enter. **Format → Darstellung → Zeilenumbrüche anzeigen** zeigt, wie die Formatierungszeichen in Word, **¶** am Absatzende, **↵** bei einem harten und **↩** bei einem weichen Umbruch.

## Was bun.ink an einer fremden Datei nicht anfasst

Öffnest und speicherst du eine Markdown-Datei, bleibt alles, was du nicht bearbeitest, wie es ist:

- **Sonderzeichen:** `a < b`, `snake_case`, `[x]` und Entities wie `&copy;` stehen danach genauso in der Datei.
- **Abstände und Schreibweisen:** mehrere Leerzeilen, `****` als Trennlinie, `>Zitat` ohne Leerzeichen, eingerückter Code.
- **Listen und Tabellen:** Einrückung, `*` oder `-`, `_betont_`, die Ausrichtung jeder Tabellenspalte.
- **Bilder und Referenz-Links:** `![Screenshot](docs/bild.png)` und die Zeilen `[name]: https://…` am Dateiende.
- **HTML:** das zentrierte Logo im README, aufklappbare `<details>`-Abschnitte, `<kbd>` und `<sup>`.
- **Front Matter und Kommentare:** der Block am Dateianfang und ausgeblendete TODOs.

Dahinter steht eine Regel: **Beim Laden merkt sich jeder Block seinen Quelltext und den Abstand zum vorigen Block. Solange sein Inhalt derselbe ist, schreibt bun.ink genau das zurück.** Änderst du einen Absatz, eine Liste oder eine Tabelle, wird nur dieser eine Block neu geschrieben. HTML erscheint im Editor als Quelltext, ein Bild als kleines Zeichen mit seinem Alt-Text.

Geprüft ist das an echten Dateien: an allen 66 Markdown-Dateien im Repository von bun.ink, allen 29 des [Handbuchs](https://github.com/VisionX-Development/writing-with-bunink) und an 811 fremden Markdown-Dateien aus den Abhängigkeiten von bun.ink – READMEs mit Badges, Bildern und HTML, Changelogs, Dokumentation. Jede kommt nach Öffnen und Speichern Zeichen für Zeichen unverändert zurück.

## Tabellen und Code

Eine neue Tabelle legst du mit **Format → Blöcke → Tabelle einfügen** an. Tab springt von Zelle zu Zelle und hängt hinter der letzten eine Zeile an. Steht der Cursor in einer Tabelle, erscheint darüber eine Leiste mit **+ Zeile**, **+ Spalte**, **− Zeile**, **− Spalte** und **×** zum Entfernen. Gespeichert wird eine gewöhnliche GFM-Tabelle.

**Inline-Code** steht mitten im Satz, zwischen zwei Backticks. **Code-Blöcke** stehen für sich, zwischen drei Backticks, auf Wunsch mit einer Sprache wie `python`. Beide sind im Editor sichtbar vom Text abgesetzt.

Metadaten und Notizen stehen in der Datei, erscheinen aber in keiner Vorschau. Wie beide funktionieren, beschreibt der Artikel [Metadaten und Notizen in Markdown](/blog/metadata-and-notes-in-markdown).

## Einfügen

Text aus einer E-Mail oder einem PDF ist oft auf eine feste Breite umbrochen. bun.ink erkennt das an der Form und fügt die Zeilen wieder zu Absätzen zusammen. Im Zweifel lässt es sie, wie sie sind: Ein Absatz zu viel ist schnell gelöscht, ein verlorener ist Arbeit. Snippets mit Formatierung werden formatiert eingesetzt: `**wichtig**` wird fett.

## Was (noch) nicht geht

- **Ein Block, den du bearbeitest, bekommt die Form des Serialisierers.** Änderst du ein Wort in einem Absatz mit `Tom & Jerry`, steht danach `Tom &amp; Jerry` in der Datei. Auf GitHub sieht es gleich aus, und im Diff ist dieser Absatz ohnehin geändert.
- **Eingefügtes Markdown** wird nicht als Formatierung übernommen: `## Überschrift` aus der Antwort eines KI-Agenten landet als Text im Editor.
- **Bilder** lassen sich nicht hochladen. Eingebundene Bilder bleiben erhalten und erscheinen auf GitHub und im Blog.

## Mehr dazu

Das Format-Menü, die Tabellen-Leiste und die Zeilenumbrüche beschreibt das [Handbuch im Kapitel «Der Editor»](https://github.com/VisionX-Development/writing-with-bunink/blob/main/de/03-der-editor.md), die Tastenkürzel der Artikel [Der TipTap-Editor in bun.ink](/blog/tiptap-editor-hidden-features).
