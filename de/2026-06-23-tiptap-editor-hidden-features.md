---
title: Der TipTap-Editor in bun.ink – ruhiger schreiben, schneller formatieren, sicher speichern
date: 2026-06-23
description: 'Ein Blick auf die weniger offensichtlichen Funktionen des TipTap-Editors in bun.ink: Zen-Modus, Stealth-Taste, Markdown-Formatierung, Shortcuts und das Zusammenspiel von lokalem Cloud-Speicher und GitHub-Branches.'
---

Ein guter Editor sollte beim Schreiben möglichst wenig auffallen. Er soll da sein, wenn du ihn brauchst – und verschwinden, sobald du dich auf deinen Text konzentrieren willst. Genau deshalb setzt bun.ink auf den **TipTap-Editor**: eine moderne Schreibfläche, die sich ruhig anfühlen kann, aber unter der Oberfläche erstaunlich viele Möglichkeiten bietet.

Viele dieser Funktionen liegen nicht laut im Weg. Sie sind eher wie kleine Hebel am Schreibtisch: einmal entdeckt, machen sie das Schreiben schneller, konzentrierter und sicherer. Dieser Beitrag zeigt dir die wichtigsten davon.

## Der Zen-Modus – nur du und der Text

Der **Zen-Modus** ist die ruhigste Schreibumgebung in bun.ink. Wenn du unter `/writer` arbeitest, kannst du ihn per Shortcut ein- und ausschalten. Welche Tastenkombination dafür verwendet wird, legst du in den Einstellungen selbst fest: Öffne dafür **Einstellungen** und dann den Bereich **Editor**. Im Abschnitt **Shortcuts** stehen alle Tastenkürzel von bun.ink, darunter **Zen-Modus**.

Im Zen-Modus geht es bewusst nicht um viele Knöpfe, Menüs oder Ablenkungen. Du kannst dort im Kern nur drei Dinge anpassen:

- die **Textgröße**
- die **Transparenz** der Schrift
- **Aktuelle Zeile zentriert halten** – die Zeile, an der du schreibst, bleibt in der Mitte des Bildschirms, und der Text läuft unter ihr durch

Diese Einstellungen werden gespeichert, damit deine ruhige Schreibumgebung beim nächsten Mal wieder so aussieht, wie du sie brauchst. Mehr soll der Zen-Modus gar nicht sein. Er ist kein zweiter, komplizierter Editor, sondern ein Raum zum Schreiben.

## Die Stealth-Taste – wenn der Text kurz verschwinden soll

Eine besondere Funktion im Zen-Modus ist die **Stealth-Taste**. Auch sie legst du in den Einstellungen unter **Editor** fest, im Abschnitt **Shortcuts** bei **Stealth-Modus**.

Mit dieser Taste schaltest du die Schrift schnell zwischen zwei Zuständen um:

- **unsichtbar** – der Text ist ausgeblendet
- **halb sichtbar** – standardmässig zu 50 Prozent; wie stark, stellst du in den Einstellungen unter **Sichtbarkeit beim Einblenden** ein

Das funktioniert in dieser Form nur im Zen-Modus. Der Gedanke dahinter ist einfach: Wenn jemand neugierig auf deinen Bildschirm schaut, kannst du den Text mit einem Tastendruck optisch verschwinden lassen. Dann wirkt das Fenster fast leer. Praktisch ist das für private Notizen, unfertige Entwürfe oder schlicht für Momente, in denen dein Text noch niemanden etwas angeht.

Und ja: Wenn man dabei an neugierige Chefs denkt, ist das natürlich eher mit einem Augenzwinkern gemeint.

## Formatieren mit dem Format-Knopf

Alle Formatierungen erreichst du über den **Format**-Knopf in der Werkzeugleiste, das kleine T. Er öffnet das Format-Menü des Editors, sortiert in vier Gruppen:

- **Text** – Fett, Kursiv, Durchgestrichen, Inline-Code
- **Absatz** – Überschriften, Listen, Zitat und Code-Block
- **Darstellung** – ein Zeilenumbruch ohne neuen Absatz, der Zeilenabstand und der **Markdown-Quelltext**, der dir das Dokument genau so zeigt, wie es gespeichert wird
- **Dokument** – Metadaten und Notizen einfügen und **Zeilenumbrüche anzeigen**, falls eine Zeile mitten im Absatz umbricht

Zusätzlich gibt es die **Formatierungs-Bubble**. Sie erscheint automatisch, wenn du eine Textstelle markierst. Statt erst das Menü zu öffnen, wendest du dort einzelne Formate direkt auf die Auswahl an – praktisch, wenn du beim Überarbeiten schnell ein Wort fett setzen oder eine Stelle kursiv markieren willst. Welche Formate die Bubble anbietet, bestimmst du in den Einstellungen unter **Editor** bei **Formatierungs-Bubble**. Jeden Eintrag erklärt das [Handbuch im Kapitel «Der Editor»](https://github.com/VisionX-Development/writing-with-bunink/blob/main/de/03-der-editor.md).

Wichtig ist: Der TipTap-Editor in bun.ink erstellt **Markdown-Dokumente**. Markdown ist eine einfache Schreibweise, bei der Formatierungen durch bestimmte Zeichen beschrieben werden. Du schreibst also nicht in einem schweren Layout-Format, sondern in einem klaren Textformat, das sich gut speichern, exportieren und versionieren lässt.

## Eine kurze Markdown-Übersicht

Markdown arbeitet mit wenigen, gut lesbaren Zeichen. Einige typische Beispiele:

- `# Überschrift 1` wird zu einer grossen Überschrift.
- `## Überschrift 2` wird zu einer Unterüberschrift.
- `**fetter Text**` wird zu **fettem Text**.
- `*kursiver Text*` wird zu _kursivem Text_.
- `- Listenpunkt` erzeugt eine Aufzählung.
- `1. Listenpunkt` erzeugt eine nummerierte Liste.
- `> Zitat` erzeugt einen Zitatblock.
- `` `Code` `` markiert einen kurzen Code- oder Monospace-Ausdruck.
- `` ``` `` am Zeilenanfang, gefolgt von einer Sprache wie `python`, beginnt einen Code-Block.

Nicht jede optische Formatierung hat in klassischem Markdown ein eigenes, einfaches Zeichen. **Unterstreichen** gehört zum Beispiel nicht zu den Standardformatierungen, die Markdown über solche Symbole abdeckt. Deshalb kann es sein, dass bestimmte Funktionen bewusst nicht wie in einer klassischen Textverarbeitung funktionieren.

Ausserdem gilt: Die Markdown-Zeichen sollen dich beim Schreiben nicht stören. In der eigentlichen `.md`-Datei wird das Dokument als Markdown bereitgestellt. In bestimmten Exporten, etwa als `.txt`, können die Formatzeichen sichtbar werden, weil dort der reine Text inklusive seiner Markdown-Schreibweise ausgegeben wird. Wie die Datei genau aussieht, zeigt dir jederzeit **Format → Darstellung → Markdown-Quelltext**. Und was in einer Markdown-Datei ausser dem Text noch stehen kann, beschreibt [Metadaten und Notizen](/blog/metadata-and-notes-in-markdown).

## Shortcuts: schneller schreiben, weniger klicken

TipTap bringt bereits eine Reihe sinnvoller Standard-Shortcuts mit. Welche davon in bun.ink verfügbar sind, hängt davon ab, welche Editor-Funktionen aktiv eingebunden sind. Die wichtigsten bekannten Tastenkombinationen aus der TipTap-Welt sind:

- **Kopieren:** `Strg + C` unter Windows/Linux, `Cmd + C` auf macOS
- **Ausschneiden:** `Strg + X` bzw. `Cmd + X`
- **Einfügen:** `Strg + V` bzw. `Cmd + V`
- **Ohne Formatierung einfügen:** `Strg + Shift + V` bzw. `Cmd + Shift + V`
- **Rückgängig:** `Strg + Z` bzw. `Cmd + Z`
- **Wiederholen:** `Strg + Shift + Z` bzw. `Cmd + Shift + Z`
- **Fett:** `Strg + B` bzw. `Cmd + B`
- **Kursiv:** `Strg + I` bzw. `Cmd + I`
- **Durchgestrichen:** `Strg + Shift + S` bzw. `Cmd + Shift + S`
- **Normaler Absatz:** `Strg + Alt + 0` bzw. `Cmd + Alt + 0`
- **Überschriften:** `Strg + Alt + 1` bis `Strg + Alt + 6` bzw. `Cmd + Alt + 1` bis `Cmd + Alt + 6`
- **Nummerierte Liste:** `Strg + Shift + 7` bzw. `Cmd + Shift + 7`
- **Aufzählung:** `Strg + Shift + 8` bzw. `Cmd + Shift + 8`
- **Zeilenumbruch im selben Absatz:** `Shift + Enter`
- **Alles auswählen:** `Strg + A` bzw. `Cmd + A`

bun.ink bleibt aber nicht bei den Standardfunktionen stehen. Dazu kommen eigene Shortcuts, alle an einer Stelle: in den Einstellungen unter **Editor** im Abschnitt **Shortcuts**. Dort stehen **Notiz einfügen** (standardmässig `Ctrl + N`, auch auf dem Mac die Control-Taste), **Speichern** (`Strg + S` bzw. `Cmd + S`), **Stealth-Modus** und **Zen-Modus**. Jedes Kürzel kannst du mit einer eigenen Tastenkombination belegen.

Das Ziel ist klar: Du sollst beim Schreiben möglichst selten zur Maus greifen müssen. Navigation, Fokus, Formatierung und Arbeitsfluss sollen direkt über die Tastatur erreichbar sein.

## Versteckte Navigation: die Tastatur als Schreibwerkzeug

Shortcuts sind nicht nur Abkürzungen für Menüpunkte. Sie verändern, wie sich Schreiben anfühlt. Wenn du Absätze verschiebst, Überschriften setzt, Listen öffnest oder in den Zen-Modus wechselst, ohne aus dem Schreibfluss zu fallen, bleibt dein Kopf stärker im Text.

Genau hier liegt eine der stillen Stärken des Editors: Viele Navigations- und Bearbeitungsfunktionen wirken unspektakulär, sparen aber über einen langen Schreibtag hinweg viele kleine Unterbrechungen. Besonders bei längeren Manuskripten, Notizen oder Blogartikeln macht das einen Unterschied.

## Speichern: lokal, bewusst und mit GitHub-Branches

Auch beim Speichern lohnt sich ein genauer Blick – vor allem, weil sich im Editor je nach Arbeitsmodus unterschiedliche Wege anfühlen. Im normalen Schreibmodus landet dein aktueller Stand in der lokalen Cloud-Datenbank von bun.ink, sobald du **Speichern** drückst.

Arbeitest du dagegen auf einem **GitHub-Branch**, gehört der Stand zunächst nach GitHub – Commit und Push, nicht die Cloud-Datenbank. Welche Speicheroptionen du in welchem Moment hast und wie Branches, Merges und Konflikte im Detail funktionieren, erklärt der Artikel [GitHub richtig nutzen – der Versionierungs-Workflow in bun.ink](/blog/using-github-with-bun-ink). Hier geht es nur um die Editor-Perspektive: Im **Branch-Modus** ist der Tab **Verlauf** nicht verfügbar, weil Branch-Stände nicht in der Cloud-Datenbank von bun.ink, sondern auf GitHub liegen.

## Lokale Versionen – Snapshots ganz ohne GitHub

Nicht jede und jeder möchte oder kann ein GitHub-Konto nutzen. Für genau diesen Fall bietet bun.ink – wie andere Schreib-Apps auch – **lokale Versionen**: kleine Schnappschüsse (Snapshots) eines Dokuments, die du jederzeit selbst anlegen kannst. Sie funktionieren unabhängig von GitHub.

Du findest sie in der Seitenleiste im Tab **Verlauf**. Dort kannst du:

- mit **Version speichern** einen neuen Snapshot deines aktuellen Standes anlegen,
- eine gespeicherte Version **im Editor mit deinem aktuellen Text vergleichen**,
- eine frühere Version **wiederherstellen** – dein aktueller Text wird dabei zuerst als neue Version gesichert, es geht also nichts verloren.

Zusätzlich legt bun.ink im Hintergrund **automatische Versionen** an – ganz ohne dein Zutun. Das geschieht behutsam und nur, wenn es sich lohnt: typischerweise dann, wenn du gerade eine kurze Schreibpause machst, sich seit dem letzten Snapshot spürbar etwas geändert hat und seit der letzten automatischen Version genügend Zeit vergangen ist (in der Grössenordnung von etwa zehn Minuten). So entsteht nebenbei ein Sicherheitsnetz, falls du einmal vergisst, selbst eine Version zu speichern. Im Verlauf sind solche Einträge als **Automatisch** gekennzeichnet, manuell angelegte als **Manuell**.

Die Zahl der manuell angelegten Versionen ist bewusst begrenzt: Pro Dokument kannst du **bis zu zehn Versionen** speichern. Ist diese Grenze erreicht, löschst du einfach eine nicht mehr benötigte Version, um wieder Platz für eine neue zu schaffen. **Automatische Versionen zählen dabei nicht mit** und werden nie blockiert – sie sind ein zusätzliches Sicherheitsnetz und kein Ersatz für das bewusste Speichern wichtiger Stände.

Ein Hinweis: Der Verlauf bezieht sich immer auf den Hauptstand deines Dokuments. Im Branch-Modus ist er nicht verfügbar – Branch-Stände gehören nach GitHub (siehe [GitHub-Workflow](/blog/using-github-with-bun-ink)).

So bekommst du auch ohne GitHub eine einfache, nachvollziehbare Versionsgeschichte direkt in bun.ink.

## Was passiert beim Schliessen, Ausloggen oder Sicherheits-Logout?

Ein Editor muss nicht nur speichern können. Er muss dich auch warnen, wenn du im Begriff bist, ungesicherte Arbeit zu verlieren.

Wenn du einen Tab schliesst oder dich ausloggen möchtest, obwohl seit dem letzten Speichern neue Änderungen entstanden sind, sollte bun.ink dich darauf aufmerksam machen. Der Editor erkennt, dass der aktuelle Inhalt noch nicht gesichert wurde, und gibt dir die Möglichkeit, vorher zu speichern oder die Aktion bewusst fortzusetzen.

Ähnlich wichtig ist der **Sicherheits-Logout**. Wenn sie aktiviert ist, schützt sie dein Konto, indem sie dich nach einer bestimmten Zeit der Inaktivität automatisch abmeldet. Damit dabei nichts verloren geht, sichert bun.ink vor dem automatischen Logout alle offenen Änderungen automatisch im lokalen Cloud-Speicher deines Kontos – andernfalls gingen diese Änderungen beim Logout verloren. Ein GitHub-Push passiert dabei allerdings nicht. Den Sicherheits-Logout schaltest du unter **Einstellungen** im Bereich **Sicherheit** ein und aus und wählst dort auch die Zeit ohne Aktivität.

Trotzdem ist es sinnvoll, gerade bei längeren Schreibphasen regelmässig manuell zu speichern – besonders dann, wenn du auf einem GitHub-Branch arbeitest und deine Änderungen erst durch Commit und Push wirklich dort landen.

Genau hier gilt eine klare Faustregel: **Auf einem GitHub-Branch sichert erst Auf Branch speichern – also Commit und Push nach GitHub – deine Arbeit wirklich.** Bis dahin liegen Branch-Änderungen ausschliesslich lokal in diesem Browser. Bei einem Logout, einem Browser-Absturz oder einem versehentlich geschlossenen Tab sind nur die bereits **gepushten** Stände eines Branches gesichert – alles, was noch nicht gepusht wurde, kann verloren gehen. Pushe deshalb ruhig öfter, als du denkst: Zu viel pushen geht praktisch nicht.

## Ein Editor, der leise mitdenkt

Der TipTap-Editor in bun.ink ist nicht einfach nur ein Textfeld. Er verbindet eine reduzierte Schreiboberfläche mit Markdown, einem aufgeräumten Format-Menü, Shortcuts, Zen-Modus, Stealth-Funktion, lokalen Versionen und einem Speichermodell, das sowohl lokale Cloud-Texte als auch GitHub-Branches unterstützt.

Am besten funktioniert er, wenn du ihn nicht als Werkzeugkasten voller Knöpfe verstehst, sondern als Schreibraum mit ein paar gut platzierten Schaltern. Manche davon wirst du täglich nutzen. Andere brauchst du nur in besonderen Momenten. Aber sie sind da – verborgen genug, um nicht zu stören, und nah genug, um deinen Schreibfluss zu schützen.
