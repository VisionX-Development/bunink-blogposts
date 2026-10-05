---
title: Markdown, das deinen Diff in Ruhe lässt
date: 2026-10-05
description: Was der Editor von bun.ink zeigt, was in der Datei steht und warum eine fremde Datei nach dem Speichern genau so aussieht wie vorher – bis auf den Satz, den du geändert hast.
---

Wer Texte in einem Git-Repository pflegt, kennt das: Du änderst in einem fremden README einen einzigen Satz, und der Commit zeigt dreissig geänderte Zeilen. Der Editor hat Listen neu eingerückt, Sternchen escaped, eine Tabelle neu ausgerichtet. Der eine Satz, um den es ging, ist im Diff kaum noch zu finden.

[bun.ink](https://bun.ink) ist ein Schreibeditor für Markdown mit GitHub dahinter. Dieser Artikel erklärt, wie Markdown im Editor aussieht, was davon in der Datei landet – und welche Regel dahinter steht: **Was du nicht anfasst, bleibt Zeichen für Zeichen, wie es war.**

## Was du siehst und was gespeichert wird

Im Editor siehst du formatierten Text: Überschriften, fette Wörter, Listen. Gespeichert wird Markdown, also Text, in dem die Formatierung durch Zeichen ausgedrückt wird. Zum Formatieren hast du drei Wege:

- **Beim Tippen:** `#` und ein Leerzeichen am Zeilenanfang machen eine Überschrift, `-` eine Aufzählung, `1.` eine nummerierte Liste, `>` ein Zitat. Sternchen um ein Wort machen es kursiv, doppelte fett.
- **Das Format-Menü** in der Werkzeugleiste, in fünf Gruppen: **Text** (Fett, Kursiv, Durchgestrichen, Inline-Code), **Absatz** (Überschriften, Listen, Zeilenumbruch), **Blöcke** (Zitat, Code-Block, Tabelle), **Dokument** (Metadaten und Notizen, die in keiner Vorschau erscheinen) und **Darstellung** (alles, was nur die Ansicht ändert, nie die Datei).
- **Die Formatierungs-Bubble**, die erscheint, sobald du Text markierst. Welche Befehle sie anbietet, stellst du in den Einstellungen ein.

Unterstreichen gibt es nicht. Markdown kennt es nicht, und bun.ink bietet nichts an, was beim Speichern wieder verloren ginge. Wie die Datei genau aussieht, zeigt dir jederzeit **Format → Darstellung → Markdown-Quelltext**.

## Drei Arten, eine Zeile zu beenden

Hier liegt die häufigste Überraschung, und an ihr lässt sich das Prinzip am besten zeigen. Markdown kennt drei Zeilenenden, und sie bedeuten Verschiedenes (CommonMark-Spezifikation, [Abschnitte 6.7 und 6.8](https://spec.commonmark.org/0.31.2/#hard-line-breaks)):

| In der Datei | Bedeutung | Im Editor |
|---|---|---|
| eine Leerzeile | neuer Absatz | Enter |
| zwei Leerzeichen oder `\` vor dem Zeilenende | harter Umbruch: neue Zeile im selben Absatz | Shift+Enter |
| ein einfaches Zeilenende | weicher Umbruch: gilt als Leerzeichen | lässt sich nicht tippen |

Der weiche Umbruch ist der interessante. Auf GitHub, im Blog und in jedem Export läuft der Absatz einfach weiter, als stünde dort ein Leerzeichen. Warum schreibt man ihn dann überhaupt? Weil er Diffs lesbar macht. Viele, die Doku unter Git pflegen, schreiben jeden Satz auf eine eigene Zeile, eine Konvention namens [Semantic Line Breaks](https://sembr.org/). Ändert sich ein Satz, zeigt der Diff genau diese eine Zeile statt des ganzen Absatzes.

Im Editor ist ein weicher Umbruch deshalb ein Leerzeichen, und der Absatz fliesst, wie ihn später auch der Leser sieht. Beim Speichern kommt aber jedes Zeilenende genau so zurück, wie es in der Datei stand. Ein Repository, das einen Satz pro Zeile schreibt, behält diese Form.

Das war nicht immer so. Früher zeigte der Editor einen weichen Umbruch als echte Zeilenschaltung, und wer daneben tippte, machte daraus unbemerkt harte Umbrüche. In zwei Artikeln dieses Blogs standen danach mitten im Absatz Zeilen mit fünf Wörtern. Wir haben es am eigenen Blog bemerkt, nicht an einem Testfall.

Zwei Dinge helfen dir, den Überblick zu behalten:

- **Markdown-Zeichen sind im Editor gewöhnlicher Text.** Tippst du zwei Leerzeichen und Enter, bekommst du zwei Leerzeichen und einen neuen Absatz, keinen harten Umbruch. Den machst du mit Shift+Enter, die Markdown-Zeichen dafür schreibt bun.ink selbst.
- **Format → Darstellung → Zeilenumbrüche anzeigen** macht alles sichtbar, wie die Formatierungszeichen in Word: **¶** am Ende jedes Absatzes, **↵** bei einem harten und **↩** bei einem weichen Umbruch. Bricht eine Zeile mitten im Absatz um, obwohl rechts noch Platz wäre, siehst du so sofort, woran es liegt.

## Was bun.ink an einer fremden Datei nicht anfasst

Der Markdown-Serialisierer, auf dem der Editor aufbaut, schreibt Text in eine eigene, «sichere» Form. Das ist praktisch, solange nur bun.ink die Datei je sieht. Für eine Datei aus einem fremden Repository ist es ein Problem: Jede dieser Umformungen landet im nächsten Commit. Im Einzelnen hiess das, wenn man irgendwo einen Satz änderte und speicherte:

- **Sonderzeichen:** aus `a < b` wurde `a &lt; b`, aus `snake_case` wurde `snake\_case`, aus `&copy;` wurde `&amp;copy;`. Auf GitHub stand danach «&copy;» statt «©».
- **Abstände und Schreibweisen:** mehrere Leerzeilen wurden zu einer, `****` wurde `---`, `>Zitat` wurde `> Zitat`, eingerückter Code wurde ein Block mit Backticks.
- **Listen und Tabellen:** Fortsetzungszeilen wurden neu eingerückt, aus `_betont_` wurde `*betont*`, Tabellen wurden neu ausgerichtet oder verschwanden ganz.
- **Bilder:** von `![Screenshot](docs/bild.png)` blieb nur das Wort «Screenshot».
- **Referenz-Links:** die Zeilen `[name]: https://…` am Dateiende fehlten, und jeder Link, der darauf zeigte, ging ins Leere.
- **HTML:** das zentrierte Logo im README (`<div align="center"><img …></div>`) war weg, ein aufklappbarer `<details>`-Abschnitt wurde Fliesstext, aus `<kbd>Ctrl</kbd>` wurde «Ctrl».
- **Front Matter und Kommentare:** der Block am Dateianfang wurde als Markdown gelesen, ausgeblendete TODOs und Lint-Anweisungen verschwanden.

All das ist behoben, und zwar nach einer gemeinsamen Regel: **Beim Laden merkt sich jeder Block seinen Quelltext und den Abstand zum vorigen Block. Solange sein Inhalt derselbe ist, schreibt bun.ink genau das zurück.** Erst wenn du einen Absatz, eine Liste oder eine Tabelle änderst, wird dieser eine Block neu geschrieben. HTML und Bilder erscheinen im Editor als Quelltext beziehungsweise als kleines Zeichen mit dem Alt-Text; du siehst und bearbeitest sie so, wie sie in der Datei stehen, und den Text zwischen zwei Tags, etwa in `<kbd>Ctrl</kbd>`, wie jeden anderen Text.

Geprüft haben wir das an echten Dateien statt an Beispielen: an allen 66 Markdown-Dateien im Repository von bun.ink, allen 29 des [Handbuchs](https://github.com/VisionX-Development/writing-with-bunink) und – weil unsere eigenen Dateien zu gleichförmig sind – an 811 fremden Markdown-Dateien aus den Abhängigkeiten von bun.ink: READMEs mit Badges, Bildern und HTML, Changelogs, Dokumentation. Jede einzelne kommt nach Öffnen und Speichern Zeichen für Zeichen unverändert zurück. Vorher war es nur gut die Hälfte der READMEs.

## Tabellen

Tabellen aus anderen Dateien bleiben, wie sie sind, solange du sie nicht änderst. Eine neue legst du mit **Format → Blöcke → Tabelle einfügen** an: drei Spalten, eine Kopfzeile, zwei Zeilen, hinter dem Absatz am Cursor. Mit Tab springst du von Zelle zu Zelle, hinter der letzten Zelle entsteht eine neue Zeile. Steht der Cursor in einer Tabelle, erscheint darüber eine schlichte Leiste mit **+ Zeile**, **+ Spalte**, **− Zeile**, **− Spalte** und **×** zum Entfernen. Gespeichert wird eine gewöhnliche GFM-Tabelle, die GitHub und jeder andere Renderer darstellen. Zellen verbinden kannst du nicht, Markdown kennt keine verbundenen Zellen.

## Code und was nicht in die Vorschau gehört

**Inline-Code** steht mitten im Satz, für Dateinamen, Befehle und Werte, mit einem Backtick davor und dahinter. **Code-Blöcke** stehen für sich, über mehrere Zeilen, zwischen drei Backticks, auf Wunsch mit einer Sprache wie `python`. Der Editor setzt beide sichtbar vom Text ab, den Code-Block mit Rahmen und der Sprache als Label.

Zwei Dinge stehen in der Datei, erscheinen aber in keiner Vorschau: **Metadaten** (das Front Matter am Dateianfang) und **Notizen**, Merkzettel an einer Textstelle, gespeichert als HTML-Kommentar. Wie beide funktionieren, beschreibt der Artikel [Metadaten und Notizen in Markdown](/blog/metadata-and-notes-in-markdown).

## Einfügen

Text, den du aus einer E-Mail oder einem PDF einfügst, ist oft auf eine feste Breite umbrochen, jede Zeile endet nach etwa 80 Zeichen. Früher wurde daraus Zeile für Zeile ein eigener Absatz. Heute erkennt bun.ink solchen Text an seiner Form und zieht die Zeilen wieder zu Absätzen zusammen. Im Zweifel lässt es sie, wie sie sind: Ein Absatz zu viel ist schnell gelöscht, ein verlorener ist Arbeit.

Auch Textbausteine (Snippets) mit Formatierung werden richtig eingesetzt: Ein Snippet mit `**wichtig**` wird fett, statt die Sternchen in den Text zu schreiben.

## Was (noch) nicht geht

Damit du weisst, worauf du dich verlassen kannst:

- **Ein Block, den du bearbeitest, bekommt die Form des Serialisierers.** Änderst du in einem Absatz mit `Tom & Jerry` ein Wort, steht danach `Tom &amp; Jerry` in der Datei. Auf GitHub sieht es gleich aus, und im Diff ist dieser Absatz ohnehin geändert – die anderen bleiben unberührt.
- **Eingefügtes Markdown** wird noch nicht als Formatierung übernommen. Wenn du Text mit `## Überschrift` oder `**fett**` einfügst, etwa aus der Antwort eines KI-Agenten, landen die Zeichen als Text im Editor.
- **Bilder** lassen sich noch nicht hochladen. Bilder, die eine Datei bereits einbindet, bleiben erhalten; dargestellt werden sie erst auf GitHub und im Blog.

## Mehr dazu

Alle Einträge des Format-Menüs, die Tabellen-Leiste und die Zeilenumbrüche beschreibt das [Handbuch im Kapitel «Der Editor»](https://github.com/VisionX-Development/writing-with-bunink/blob/main/de/03-der-editor.md). Die versteckten Funktionen und Tastenkürzel des Editors stehen im Artikel [Der TipTap-Editor in bun.ink](/blog/tiptap-editor-hidden-features).
