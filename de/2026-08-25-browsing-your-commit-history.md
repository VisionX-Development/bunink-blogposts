---
title: Der Commit-Browser – deine Textgeschichte in der Commit-Historie durchsuchen
date: 2026-08-25
description: Wie der neue Commit-Browser im Changes-Tab funktioniert – die ganze Commit-Historie eines Branches durchsuchen, zwei Stände frei wählen und verstehen, worin sich das vom gewohnten lokalen Vergleich unterscheidet.
---

Im Artikel [GitHub richtig nutzen – der Versionierungs-Workflow in bun.ink](/blog/using-github-with-bun-ink) ging es um Speichern, Pushen, Branches und Mergen. Ein Baustein hat dort noch gefehlt: Wie schaust du dir an, was sich über viele Commits hinweg an einem Dokument verändert hat – nicht nur seit dem letzten Speichern, sondern seit dem allerersten Commit? Genau dafür gibt es jetzt den **Commit-Browser** im Changes-Tab.

## Wozu der Commit-Browser gut ist

Der Changes-Tab zeigt dir normalerweise, was sich seit deinem letzten Speicherpunkt verändert hat – ein einzelner, naher Vergleich. Hast du dein Projekt mit einem GitHub-Repository verknüpft, steckt darin aber viel mehr: die komplette Commit-Historie deines Branches. Jeder Commit ist ein Speicherpunkt mit eigener Nachricht und eigenem Zeitstempel.

Der Commit-Browser macht diese Historie nutzbar. Du wählst zwei Stände aus der Liste – zum Beispiel den allerersten Commit deines Branches und den aktuellsten – und siehst im Änderungsfenster genau, was sich dazwischen am Dokument getan hat. So verfolgst du die Entwicklung eines Kapitels über Wochen, statt nur den letzten Schritt zu sehen.

## Wo du ihn findest

Im Writer öffnest du in der Seitenleiste den Tab **Änderungen**. Unter der Liste der geänderten Dokumente erscheint dort ein neuer Abschnitt namens **Commits**.

Der Abschnitt erscheint nur, wenn alles zusammenpasst:

- Dein GitHub-Konto ist mit bun.ink verbunden.
- Das aktuelle Projekt ist mit einem Repository verknüpft.
- Es ist kein High-Privacy-Projekt. Solche Projekte bleiben bewusst nur auf deinem Gerät und haben deshalb keine GitHub-Historie.
- Du hast ein aktives Pro-Abo oder eine laufende Testphase – das Durchsuchen der Commits gehört zu den Pro-Funktionen.

Fehlt eine dieser Voraussetzungen, bleibt der Abschnitt entweder ganz weg oder zeigt dir in einer kurzen Zeile, woran es liegt. Nichts wirkt wie ein Fehler, wenn eigentlich nur eine Bedingung fehlt.

## Zwei Stände: A und B

Jeder Commit in der Liste trägt zwei kleine Schalter, **A** und **B**. Damit legst du fest, was miteinander verglichen wird:

- **A** ist immer die linke, ältere Seite. A ist immer ein echter Commit – nie dein gerade offener, unfertiger Text.
- **B** ist die rechte, neuere Seite. B kann ein Commit sein, oder der besondere Eintrag **Arbeitsstand**: dein aktueller Text im Editor, so wie er gerade dasteht, auch wenn du ihn noch nicht gespeichert oder gepusht hast.

Klickst du auf eine Seite, die schon auf der jeweils anderen Seite ausgewählt ist, tauschen die beiden Seiten einfach die Plätze – der Vergleich wird nie leer. Über die Kopfzeile des Abschnitts kannst du A und B mit einem Klick vertauschen oder die Auswahl auf die Voreinstellung zurücksetzen.

## Die Voreinstellung: erster Commit gegen den aktuellsten

Öffnest du den Commit-Browser, ist schon eine sinnvolle Auswahl getroffen: **A ist der erste Commit deines Branches, B ist der aktuellste**. Genau das ist der Fall, um den es meistens geht – der ganze Weg von dort, wo der Branch angefangen hat, bis zu dem, wo er heute steht. Du musst also nichts einstellen, um diesen grossen Überblick zu sehen; du kannst die Auswahl aber jederzeit auf zwei beliebige andere Commits ändern.

Bist du auf dem Hauptast (`main`) unterwegs, gibt es keinen Abzweigpunkt – dort tritt einfach der älteste geladene Commit an die Stelle des Branch-Starts.

## Was genau verglichen wird

Der Vergleich bezieht sich immer auf das Dokument, das du gerade geöffnet hast – nicht auf das ganze Projekt. Das hält die Ansicht schnell und übersichtlich, auch bei einer langen Historie. Eine Übersicht über alle Dateien, die ein Commit verändert hat, ist für später geplant.

Ein paar ehrliche Randfälle, die dir begegnen können:

- Gab es das Dokument im älteren Commit noch gar nicht, zeigt die Ansicht das als „vollständig hinzugefügt" – kein Fehler, sondern ein normales Ergebnis.
- Wurde eine Datei zwischen A und B umbenannt, erkennt der Commit-Browser das noch nicht als dieselbe Datei. Das ist bewusst so gehalten, statt eine unsichere Vermutung anzuzeigen.
- Verschwindet ein ausgewählter Commit – etwa nach einem force-push –, lädt bun.ink die Liste neu und weist dich darauf hin.

## Der Unterschied zum lokalen Vergleich

Das ist der wichtigste Punkt, um den Commit-Browser richtig einzuordnen. Im Changes-Tab gab es schon vorher mehrere Arten von Vergleichen, und sie beantworten unterschiedliche Fragen:

- **Lokaler Vergleich** (die Voreinstellung): stellt deinen zuletzt gespeicherten Stand deinem aktuellen Stand im Editor gegenüber. Das ist immer nur **ein** Schritt, und immer der allernächste – „was habe ich seit eben verändert?"
- **GitHub-Vergleich**: stellt den gespeicherten Hauptstand deinem aktuellen Stand gegenüber – oder, im Branch-Modus, den Hauptstand deinem Branch.
- **Versions-Vergleich**: stellt eine einzelne, von dir ausgewählte gespeicherte Version deinem aktuellen Stand gegenüber.
- **Commit-Vergleich** (neu, der Commit-Browser): stellt **zwei frei wählbare Punkte aus der gesamten Commit-Historie** gegenüber – nicht nur den letzten Schritt, sondern jeden beliebigen Abschnitt dazwischen. Commit drei gegen Commit siebzehn, der erste Commit gegen den heutigen Stand, zwei Monate Arbeit in einem einzigen Diff.

Kurz gesagt: Der lokale Vergleich schaut immer nur auf den nächsten Schritt. Der Commit-Browser öffnet dir die ganze Zeitachse und lässt dich selbst wählen, welchen Ausschnitt daraus du sehen willst.

## Nur zum Anschauen – noch

Der Commit-Browser ist in dieser ersten Version bewusst nur zum Betrachten da. Es gibt kein „diesen Stand wiederherstellen" direkt aus dem Vergleich heraus. Das Wiederherstellen einzelner Versionen gibt es an anderer Stelle bereits – für Commits kommt das später, mit eigenen, sauber durchdachten Regeln für Branches.

## Ein Werkzeug für den Überblick, nicht für den Alltag

Für die meisten Speicherpunkte reicht der gewohnte, lokale Vergleich völlig aus. Der Commit-Browser ist für die Momente gedacht, in denen du zurückblicken willst: Wie hat sich dieses Kapitel seit dem ersten Entwurf entwickelt? Was ist zwischen zwei wichtigen Etappen passiert? Die Antwort liegt jetzt nur zwei Klicks entfernt – ohne dass du GitHub selbst öffnen musst.
