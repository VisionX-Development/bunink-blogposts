---
title: Git und GitHub einfach erklärt – Versionskontrolle für Autoren
date: 2026-06-18
description: Was Git und GitHub eigentlich sind, in verständlicher Sprache – und warum diese Werkzeuge aus der Programmierwelt gerade für Autorinnen und Autoren überraschend nützlich sind.
update: 2026-11-20
---

**Git bzw. GitHub** sind Werkzeuge der Versionskontrolle aus der Welt der Programmierung. Es ist optional in [bun.ink](http://bun.ink) verfügbar. Warum? Als Entwickler von bun.ink und Autoren habe wir uns schon immer einen Schreib- Editor gewünscht, der Texte versioniert wie **Git** es tut. 

**MERKE: [bun.ink beinhaltet bereits ein Git ähnliches](http://bun.ink) Versionssystem das ohne jeglichen zusätzlichen Aufwand funktioniert.** 

Für alle die technisch interessiert sind haben wir in [bun.ink](http://bun.ink) aber optional eine GitHub Integration eingebaut. Diese funktioniert ohne den Terminal benutzen zu müssen und kann Text- Datein mit GitHub synchronisieren. Dieser Beitrag erklärt in Ruhe, worum es geht. Es liefert den technischen Hintergrund, für alle die, die es interessiert.

## Was ist Versionskontrolle?

Stell dir vor, dein Text hätte ein perfektes Gedächtnis. Jedes Mal, wenn du sagst „so, dieser Stand ist mir wichtig", legt er einen Schnappschuss an. Wochen später kannst du jeden dieser Schnappschüsse wieder ansehen, vergleichen, was sich verändert hat, und bei Bedarf zu einem früheren Stand zurückkehren – ohne dass irgendetwas verloren geht.

Das ist **Versionskontrolle**: eine lückenlose, geordnete Geschichte deines Textes. Nicht zwölf Dateien mit kryptischen Namen, sondern _ein_ Dokument mit einer Zeitleiste.

## Git – das Gedächtnis

**Git** ist das Programm, das diese Geschichte führt. Es läuft im Hintergrund und merkt sich jede Fassung, die du bewusst sicherst. Drei Begriffe begegnen dir dabei immer wieder:

- **Commit** – ein einzelner Schnappschuss. Wenn du einen Commit machst, sagst du im Grunde: „Diesen Stand bitte für die Ewigkeit festhalten." Jeder Commit bekommt eine kurze Notiz, damit du später weisst, was du geändert hast – zum Beispiel _„Kapitel 3 gekürzt"_.
- **Repository** (kurz _Repo_) – die Sammelmappe, in der dein Projekt mit seiner gesamten Geschichte liegt. Ein Repository ist einfach dein Buch _plus_ das Gedächtnis aller Fassungen.
- **Branch** – ein paralleler Erzählstrang. Dazu gleich mehr.

Wichtig: Git wirft nie etwas weg. Selbst wenn du einen ganzen Absatz löschst und sicherst – in der Geschichte bleibt er auffindbar.

## Branch und Merge – mutig ausprobieren, ohne Angst

Der wahrscheinlich nützlichste Gedanke für Schreibende ist der **Branch** (gesprochen „Bräntsch", englisch für _Zweig_ oder _Ast_).

Angenommen, dein Manuskript steht solide da, aber du fragst dich: _Was, wenn ich die Geschichte in der Gegenwart statt in der Vergangenheit erzähle?_ Eine grosse Änderung. Du willst sie ausprobieren, ohne deine gute Fassung zu gefährden.

Mit einem Branch legst du dafür einen Seitenstrang an – eine Arbeitskopie, in der du frei experimentierst. Dein Hauptstrang (üblicherweise **main** genannt) bleibt unangetastet. Gefällt dir das Experiment nicht, verwirfst du den Branch, und nichts ist passiert. Gefällt es dir, führst du beide Stränge wieder zusammen. Dieses Zusammenführen heisst **Merge**.

Ein Bild dafür: Dein Text ist ein Fluss. Ein Branch ist ein Seitenarm, den du gräbst, um eine andere Route zu testen. Der **Merge** ist die Stelle, an der du den Seitenarm wieder in den Hauptfluss münden lässt.

## Wozu dann noch GitHub?

Git läuft auf einem Gerät lokal. **GitHub** ist ein Dienst im Internet, der deine Repositories sicher **online** aufbewahrt. Drei Dinge gewinnst du damit:

1. **Sicherung** – dein Text und seine ganze Geschichte liegen geschützt in der **GitHub- Cloud**. Geht dein Laptop verloren, ist die Arbeit nicht weg.
2. **Überall verfügbar** – du schreibst morgens am Schreibtisch weiter, wo du abends am Sofa aufgehört hast.
3. **Zusammenarbeit** – ein Lektor oder eine Mitautorin kann an einem eigenen Branch arbeiten, und ihr führt eure Fassungen geordnet zusammen.

Kurz gesagt: **Git** ist das Gedächtnis, **GitHub** ist der sichere, geteilte Ort, an dem dieses Gedächtnis lebt.

## Warum das für Autorinnen und Autoren zählt

Diese Werkzeuge wurden für Software gebaut – aber das Problem, das sie lösen, ist zutiefst ein Schreibproblem: _Wie behalte ich den Überblick über einen Text, der sich ständig verändert, und wie probiere ich Neues aus, ohne Gutes zu verlieren?_

- Du kannst **radikal kürzen**, weil du weisst: Das Gestrichene ist nicht verloren.
- Du kannst **zwei Enden** für deine Geschichte schreiben und sie nebeneinander vergleichen.
- Du siehst **schwarz auf weiss**, was sich zwischen zwei Fassungen verändert hat.
- Du hast nie wieder Angst vor dem Speichern.

In bun.ink passiert all das im Hintergrund. Du schreibst wie gewohnt – die Versionskontrolle ist einfach da, wenn du sie brauchst. Du musst weder Git installieren noch Befehle lernen. Begriffe wie _Commit_, _Branch_ und _Merge_ tauchen an den richtigen Stellen auf, und jetzt weisst du, was sie bedeuten.

**MERKE: das [bun.ink](http://bun.ink) eigene Versionskontrollsystem ist dem Versionskontrollsystem von Git nachempfunden! Bereits mit der Versionskontrolle von [bun.ink](http://bun.ink) hast du alles was du brauchst! Die Verknüpfung mit einem GitHub- Repository ist optional und macht nur Sinn wenn du deine Datein explizit mit GitHub synchronisieren möchtest, z.B. wenn du mit anderen Autoren zusammen an deinen Datein arbeiten möchtest.** 

In kommenden Beiträgen schauen wir uns einzelne Funktionen zur Versionskontrolle genauer an. Bis dahin: Schreib mutig – dein Text vergisst nichts mehr.
