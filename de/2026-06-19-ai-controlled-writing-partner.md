---
title: KI als kontrollierter Schreibpartner – Texterstellung mit Agenten und klaren Regeln
date: 2026-06-19
description: Wie Autorinnen und Autoren KI beim Schreiben, Prüfen und Überarbeiten nutzen können, ohne die Kontrolle über Stil, Inhalt und Entscheidungen abzugeben.
---

Künstliche Intelligenz kann heute Absätze formulieren, Szenen vorschlagen, Figurenstimmen nachahmen und ganze Textfassungen überarbeiten. Das klingt nach einem grossen Versprechen – und manchmal auch nach einer Bedrohung: _Schreibt dann noch der Mensch?_

Die spannendere Antwort lautet: Ja, wenn die KI nicht als Ersatz verstanden wird, sondern als **kontrollierter Schreibpartner**. Ein Agent kann Ideen sortieren, Schwachstellen finden und Alternativen anbieten. Aber die Richtung, die Regeln und die letzte Entscheidung bleiben bei der Autorin oder beim Autor.

## KI schreibt nicht im luftleeren Raum

Ein KI-Agent ist besonders hilfreich, wenn er weiss, worauf er achten soll. Ohne Kontext arbeitet er mit allgemeinen Mustern: Er erkennt, was „normalerweise“ gut klingt, welche Struktur häufig funktioniert und welche Formulierungen wahrscheinlich passen. Für einen konkreten Roman, Essay oder Blogartikel reicht das oft nicht.

Texte haben eigene Gesetze. Ein Roman kann konsequent in der Ich-Perspektive erzählt sein. Eine Figur kann bewusst kurze, harte Sätze sprechen. Ein Sachtext kann eine ruhige, erklärende Stimme haben. Wenn die KI diese Regeln nicht kennt, verbessert sie vielleicht etwas, das gar nicht verbessert werden soll.

Darum wird der Kontext entscheidend: Je genauer der Agent weiss, welche Absicht hinter einem Text steht, desto nützlicher kann seine Unterstützung sein.

## Was eine AGENTS.md leisten kann

Eine einfache Markdown-Datei kann dabei eine erstaunlich grosse Rolle spielen. In vielen Arbeitsumgebungen lässt sich eine Datei wie `AGENTS.md` oder `agents.md` im Projekt ablegen. Darin stehen Anweisungen, Hintergrundinformationen und Regeln, die ein KI-Agent bei seiner Arbeit berücksichtigen soll.

Für ein literarisches Projekt könnte eine solche Datei zum Beispiel festhalten:

- **Erzählperspektive:** personale Perspektive, nah an der Hauptfigur
- **Zeitform:** Präteritum, keine Wechsel ins Präsens
- **Sprachstil:** knapp, bildhaft, ohne ironischen Erzählerkommentar
- **Figurenwissen:** Die Hauptfigur weiss bis Kapitel 12 nicht, wer den Brief geschrieben hat
- **Storyline:** zentrale Wendepunkte, wichtige Beziehungen, offene Geheimnisse
- **Tabus:** keine modernen Redewendungen, keine allwissende Erklärung, keine Auflösung vor dem Finale

Damit wird die Markdown-Datei zu einer Art Arbeitsbriefing. Sie ersetzt nicht das Manuskript und auch nicht die kreative Entscheidung. Aber sie gibt dem Agenten einen Rahmen, in dem er prüfen, kommentieren und Vorschläge machen kann.

## Wenn der Agent Zugriff auf das Projekt hat

Besonders interessant wird das, wenn ein Agent direkt mit einem GitHub-Repository oder einem anderen Projektordner verbunden ist. Dann sieht er nicht nur den einzelnen Ausschnitt, den man in ein Chatfenster kopiert, sondern kann auch begleitende Dateien lesen: Notizen, Figurenblätter, Kapitelpläne, Recherchetexte oder eben eine `AGENTS.md`. Den konkreten Workflow zum Verknüpfen eines Projekts mit GitHub beschreiben wir in [GitHub richtig nutzen – der Versionierungs-Workflow in bun.ink](/blog/using-github-with-bun-ink).

Das verändert die Zusammenarbeit. Statt jedes Mal neu zu erklären, worum es geht, kann der Agent wiederkehrende Projektregeln berücksichtigen. Er kann fragen: _Passt diese Szene noch zur festgelegten Erzählperspektive?_ Oder: _Widerspricht diese Information der bisherigen Storyline?_

Für Autorinnen und Autoren bedeutet das: Die KI wird nicht klüger, weil sie „magisch“ versteht, was gemeint ist. Sie wird hilfreicher, weil sie bessere Arbeitsunterlagen bekommt.

## Stil-Analyse statt automatischer Umschreibung

Ein kontrollierter Einsatz beginnt oft nicht mit der Frage: „Schreib das schöner.“ Viel hilfreicher ist die Frage: „Analysiere diesen Text anhand meiner Regeln.“

Der Agent kann dann wie ein aufmerksamer Lektor arbeiten und Hinweise geben:

- Wo wechselt die Erzählperspektive ungewollt?
- Wo rutscht der Text aus dem Präteritum ins Präsens?
- Welche Sätze klingen nicht nach der festgelegten Figurenstimme?
- Wo erklärt der Erzähler zu viel, obwohl die Szene es zeigen könnte?
- Welche Begriffe passen nicht zur Zeit, zum Milieu oder zum Ton des Romans?

Der Unterschied ist wichtig: Die KI verändert den Text nicht ungefragt. Sie markiert Stellen, begründet ihre Einschätzung und macht Vorschläge. Die Entscheidung, ob etwas geändert wird, bleibt beim Menschen.

## Logikfehler und blinde Flecken finden

Neben Stilfragen kann ein Agent auch auf inhaltliche Widersprüche achten – besonders dann, wenn die grobe Handlung in einer Projektdatei beschrieben ist. Wenn dort steht, dass eine Figur erst im letzten Drittel von einem Geheimnis erfährt, kann der Agent frühere Kapitel darauf prüfen, ob sie dieses Wissen versehentlich schon voraussetzen.

Solche Prüfungen sind keine Garantie. Eine KI kann Zusammenhänge falsch gewichten oder etwas übersehen. Aber sie kann als zweite Aufmerksamkeitsebene dienen. Sie findet manchmal Brüche, die beim wiederholten Lesen unsichtbar geworden sind, weil die Autorin oder der Autor die Geschichte längst im Kopf vervollständigt.

Typische Fragen an den Agenten könnten sein:

- „Prüfe Kapitel 4 auf Widersprüche zur Storyline in `AGENTS.md`.”
- „Liste alle Stellen auf, an denen die Hauptfigur mehr zu wissen scheint, als sie zu diesem Zeitpunkt wissen dürfte.”
- „Suche nach Zeitformwechseln und erkläre kurz, warum sie auffallen.”
- „Schlage Alternativen für diese Szene vor, ohne die Perspektive zu wechseln.”

So entsteht ein Dialog, der einem Lektoratsgespräch ähnelt: Der Agent kritisiert nicht endgültig, sondern liefert Beobachtungen und mögliche Wege.

## Der Mensch bleibt die Instanz

Gerade bei literarischen Texten ist Kontrolle entscheidend. Eine KI kann sehr überzeugend formulieren, aber sie kennt nicht automatisch die innere Notwendigkeit eines Textes. Manchmal ist ein Bruch gewollt. Manchmal soll ein Satz sperrig bleiben. Manchmal ist eine Wiederholung kein Fehler, sondern Rhythmus.

Darum sollte der Agent nicht als Autorität auftreten, sondern als Werkzeug mit klarer Aufgabe. Die besten Ergebnisse entstehen, wenn Autorinnen und Autoren präzise festlegen, auf welcher Ebene die KI helfen soll:

1. **Beobachten:** Stil, Perspektive, Zeitform oder Logik prüfen.
2. **Erklären:** Auffälligkeiten begründen und einordnen.
3. **Vorschlagen:** mehrere Alternativen anbieten.
4. **Umsetzen:** nur nach ausdrücklicher Freigabe ändern.

Diese Reihenfolge schützt den eigenen Text. Sie verhindert, dass eine KI aus einem eigenwilligen Manuskript einen glatten Durchschnittstext macht.

## Schreiben mit Gedächtnis und Regeln

In Verbindung mit Versionskontrolle wird dieser Ansatz noch stärker. Wenn ein Projekt in einem Repository liegt, bleiben Änderungen nachvollziehbar – du siehst, welche Vorschläge übernommen wurden und welche Fassung vorher existierte. Was Commits, Branches und Repository im Detail bedeuten, haben wir in [Git und GitHub einfach erklärt](/blog/git-and-github-for-writers) aufgeschrieben; den praktischen Workflow in bun.ink zeigt [GitHub richtig nutzen](/blog/using-github-with-bun-ink).

Eine `AGENTS.md` liefert dabei die Regeln. Das Repository bewahrt die Geschichte. Der Agent hilft beim Prüfen und Überarbeiten. Zusammen entsteht eine Arbeitsweise, in der KI nicht heimlich übernimmt, sondern sichtbar mitarbeitet.

Das ist vielleicht der wichtigste Gedanke: KI-gestützte Texterstellung muss nicht bedeuten, dass ein Text weniger persönlich wird. Richtig eingesetzt kann sie sogar helfen, die eigene Absicht klarer zu schützen – weil Stil, Perspektive und Handlung nicht nur im Kopf der Autorin oder des Autors liegen, sondern als überprüfbare Regeln im Projekt stehen.

Die Zukunft des Schreibens liegt deshalb nicht im Knopfdruck, der ein fertiges Buch erzeugt. Sie liegt in Werkzeugen, die aufmerksam mitlesen, kluge Fragen stellen und Alternativen anbieten – während der Mensch entscheidet, welche Stimme der Text am Ende haben soll.
