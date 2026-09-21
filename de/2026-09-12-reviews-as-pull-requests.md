---
title: Das Lektorat kommt zum Text – Überarbeitungen als Pull Request
date: 2026-09-12
description: Wie jemand anders deinen Text überarbeitet, ohne ihn anzufassen – und wie du am Ende Stelle für Stelle entscheidest, was davon in dein Manuskript kommt.
---

Es gibt diesen Ordner. `kapitel-3.docx`, `kapitel-3-lektorat.docx`,
`kapitel-3-lektorat-final.docx`, `kapitel-3-lektorat-final-KORR.docx`. Irgendwo darin steht die
Fassung, die gilt. Welche das ist, weiss nach der dritten Runde niemand mehr sicher, und die
Anmerkung, die am Rand von Seite 14 stand, ist beim Übertragen verloren gegangen.

bun.ink macht daraus etwas anderes: eine **Überarbeitung**. Jemand liest deinen Text, markiert
Stellen, schlägt neue Formulierungen vor – und dein Text bleibt dabei unangetastet, bis du
Stelle für Stelle entschieden hast, was du davon übernimmst. Am Ende gibt es keine zweite Datei.
Es gibt deinen Text, und darin steht, was du wolltest.

## Der Unterschied: niemand schreibt in dein Manuskript

Das ist der Punkt, an dem diese Funktion anders ist als eine geteilte Datei. Wenn dein Lektorat
eine Überarbeitung beginnt, bekommt es dafür eine eigene Kopie deines Textes – in Git heisst das
ein Branch, eine Abzweigung, wie in [GitHub richtig nutzen](/blog/using-github-with-bun-ink)
beschrieben. Alles, was dort geschieht, geschieht dort: Umformulierungen, Streichungen,
Anmerkungen.

Deine Fassung merkt davon nichts. Du kannst weiterschreiben, während jemand anders liest. Erst
wenn die Überarbeitung fertig ist und abgeschickt wird, klopft sie bei dir an – und auch dann
ändert sich in deinem Text noch immer nichts, solange du nicht selbst etwas übernimmst.

Das ist die eigentliche Umkehr. In einem geteilten Dokument ist die fremde Änderung erst einmal
da und du musst sie rückgängig machen, wenn du sie nicht willst. Hier ist sie ein Vorschlag, der
darauf wartet, dass du ihn annimmst.

Eine Voraussetzung dafür, gleich vorweg: Der Text, der überarbeitet werden soll, liegt selbst
schon auf einer Abzweigung – etwa `kapitel-3` – und nicht auf dem Hauptstand deines Projekts. Die
Überarbeitung braucht ein Ziel, das sich später zusammenführen lässt, und der Hauptstand ist
dafür bewusst tabu. Eine Abzweigung anzulegen ist ein Klick, mehr nicht.

## Wie eine Überarbeitung entsteht

Aus Sicht der Person, die überarbeitet, ist der Anfang unspektakulär: Sie öffnet dein Projekt,
wechselt auf deinen Text und startet die Überarbeitung. bun.ink erklärt in einem Satz, was gleich
passiert – die Überarbeitung bekommt ihre eigene Abzweigung neben deiner, dort wird gearbeitet,
und ihr Vorschlag wird dir später angetragen.

Danach wird gearbeitet, und zwar ganz normal im Editor. Sätze umstellen, kürzen, streichen – so,
wie jeder andere Text auch. Für die überarbeitende Person fühlt es sich an, als würde sie deinen
Text bearbeiten. Tatsächlich bearbeitet sie ihre Kopie.

Aus dieser Kopie werden dann **Vorschläge**. bun.ink zeigt deinen Text und die überarbeitete
Fassung nebeneinander, mit allen Unterschieden hervorgehoben – als lesbaren Text, nicht als
Code. Die überarbeitende Person geht die geänderten Stellen durch und macht aus jeder, die sie dir
vorlegen will, einen Vorschlag: Das ist die Stelle, so soll sie neu lauten, und – wenn sie will –
darum. Die Begründung ist das, was du später liest, bevor du entscheidest.

Es geht auch ohne neuen Wortlaut. Manchmal will eine Anmerkung gar nichts ändern, sondern nur
etwas sagen: «Das kommt zu früh», «Der Name stimmt hier nicht». Solche Anmerkungen hängen an
ihrer Stelle im Text und gehen genauso wenig verloren wie ein Vorschlag. Und für alles, was sich
an keiner Stelle festmachen lässt – zum Aufbau, zum Ton –, gibt es Notizen zum ganzen Text.

Bis hierhin ist noch nichts unterwegs. Jeder Vorschlag lässt sich noch umformulieren oder
zurücknehmen; wird er zurückgenommen, verschwindet auch die Änderung im Text wieder, damit nicht
still etwas übrig bleibt, wozu es keinen Vorschlag mehr gibt. Und hat sich der Text unter einem
Vorschlag inzwischen geändert, sagt bun.ink das deutlich, bevor etwas abgeschickt wird.

Die angefangene Überarbeitung bleibt auf dem Gerät der überarbeitenden Person, auch wenn sie das
Fenster schliesst oder morgen weitermacht. Erst ein Abmelden räumt sie weg – bun.ink warnt davor
–, und was als Text schon gespeichert wurde, ist ohnehin sicher. Abgeschickt wird alles auf
einmal, als **Pull Request**. Das ist nichts weiter als die Form, in der GitHub eine solche
Anfrage transportiert: «Hier ist ein Vorschlag für deinen Text, schau ihn dir an.»

Kommt später noch etwas dazu, entsteht dafür kein zweiter Vorgang. Zu jedem Text gibt es genau
eine Überarbeitung, und weitere Runden hängen sich an dieselbe – ein Gespräch, nicht ein Stapel
Gespräche.

## Was bei dir ankommt

Bei dir erscheint ein Hinweis: Für deinen Text liegt eine Überarbeitung vor. Von da an hast du
zwei Wege, und du kannst sie mischen.

Der erste Weg führt durch dein Dokument. Neben deinem Text erscheinen die Vorschläge, die es dazu
gibt: die markierte Stelle, der vorgeschlagene Wortlaut, die Begründung, und wer das geschrieben
hat. Du springst zur Fundstelle, liest sie im Zusammenhang, und übernimmst den Vorschlag – oder
lässt es.

Übernommenes steht sofort in deinem Dokument. Nicht «wird beantragt», nicht «wird beim nächsten
Schritt eingearbeitet» – es steht da, und du kannst weiter daran schreiben. Auf Anmerkungen, die
nur etwas sagen wollten, kannst du direkt antworten; die Antwort erscheint beim Lektorat an genau
der Stelle, um die es ging.

### Wenn eine Stelle nicht mehr passt

Du hast weitergeschrieben, während gelesen wurde. Der Vorschlag bezieht sich auf einen Satz, den
es so nicht mehr gibt – oder der inzwischen zweimal vorkommt. bun.ink rät dann nicht, sondern
sagt es: Diese Stelle braucht deine Entscheidung.

Du siehst beide Fassungen nebeneinander – was gerade in deinem Text steht und was vorgeschlagen
wurde – und genau die Zeilen, um die es geht. Du setzt den Vorschlag ein, schreibst deine eigene
Fassung oder lässt alles, wie es ist. Nichts wird im Hintergrund verschoben.

Das ist bewusst die unbequemere Variante. Ein automatisch gesetzter Vorschlag, der um ein paar
Zeilen danebenliegt, fällt erst Wochen später auf – wenn überhaupt.

## Der ganze Vorschlag auf einmal

Der zweite Weg ist die Gesamtansicht: alle geänderten Dateien gegenübergestellt, links dein Text,
rechts die Fassung der Überarbeitung. Wo eine Änderung nur die Formatierung betrifft – ein Satz
war kursiv und soll fett werden –, sagt bun.ink das dazu, statt dich zweimal denselben Satz
vergleichen zu lassen.

Hier wird nicht nach Zeilen entschieden, sondern nach **Stellen** – zusammenhängende Passagen,
in denen sich etwas geändert hat. Das ist bei Prosa die richtige Einheit: Ein umformulierter Satz
hängt an seinen Nachbarn, und eine einzelne Zeile daraus zu übernehmen ergibt einen Text, den
niemand geschrieben hat. Ein Vorschlag, der über zwei Absätze geht, ist deshalb eine Stelle und
eine Entscheidung, nicht zwei.

Zu jeder Stelle hast du drei Antworten:

- **Behalten** – die Änderung kommt mit, wenn du die Überarbeitung am Ende übernimmst.
- **Verwerfen** – die Stelle bleibt, wie sie bei dir war. Wenn du willst, mit einem Grund.
- **Eigene Fassung** – weder das eine noch das andere, sondern dein dritter Wortlaut. Er geht als
  Gegenvorschlag zurück ans Lektorat.

Und wie im Dokument kannst du auch hier eine Stelle sofort in deinen Text übernehmen. Das gilt
sogar für Streichungen, die sich sonst schlecht «vorschlagen» lassen: eine Entscheidung, und der
Absatz ist bei dir weg.

### Verworfenes geht zurück

Hier passiert etwas, das es auf Papier nicht gibt. Was du verwirfst oder mit einer eigenen
Fassung beantwortest, wird auf die Kopie der Überarbeitung zurückgeschrieben – mit deinem Grund
dazu, wenn du einen genannt hast. Dein Lektorat sieht also, welche Stellen du nicht wolltest und
was du stattdessen vorschlägst.

Der Grund für diesen Umweg ist einfach: Die Alternative wäre, dass du die unerwünschten Stellen
still weglässt. Dann stünde am Ende ein Text, den beide Seiten für abgesprochen halten, obwohl
niemand über die Hälfte der Änderungen gesprochen hat. So bleibt die Abstimmung vollständig und
in beide Richtungen nachlesbar.

## Am Ende: übernehmen oder schliessen

Zwei Arten, eine Überarbeitung abzuschliessen.

**Alles auf einmal übernehmen.** In Git heisst das Mergen: Die Kopie der Überarbeitung wird in
deinen Text zusammengeführt, und die Kopie verschwindet. bun.ink lässt das erst zu, wenn über jede
einzelne Stelle entschieden ist, und zählt dir bis dahin vor, wie viele noch offen sind. Vorher
würde ein unbeantworteter Vorschlag ungesehen mitwandern, und das ist die gefährlichste Art von
Fehler: Es geht nichts schief, es fällt nur nie jemandem auf.

Ein Fall verdient einen eigenen Satz: Hast du vorher schon einzelne Vorschläge in deinen Text
übernommen und gespeichert, sieht GitHub an dieser Stelle zwei Änderungen – deine und die der
Überarbeitung – und kann nicht wissen, dass es dieselbe ist. bun.ink weiss es und löst das für
dich auf: Was du entschieden hast, gilt, der Rest kommt aus der Überarbeitung, und die
Zusammenführung geht durch. Kein neuer Vorgang, kein Umweg über GitHub.

**Einzeln übernommen und dann schliessen.** Wenn du alles, was du wolltest, schon Stelle für
Stelle in deinen Text geholt hast, braucht es keine Zusammenführung mehr. Du schliesst die
Überarbeitung, und dein Lektorat bekommt automatisch eine Rückmeldung: welche Datei, wie viele der
vorgeschlagenen Änderungen übernommen wurden. Kein Vorgang, der ohne ein Wort verschwindet.

## Was du dafür brauchst

Ehrlich gesagt ist das der unromantischste Abschnitt, aber ohne ihn funktioniert nichts:

- **Beide Seiten brauchen ein eigenes GitHub-Konto** und ein eigenes bun.ink-Konto. Es gibt kein
  geteiltes Passwort und keinen Gastzugang.
- **Der Zugang läuft über GitHub**, nicht über bun.ink: Du lädst dein Lektorat als
  Mitarbeiter:in in dein Repository ein, so wie du auch jemandem Zugriff auf einen geteilten
  Ordner gibst. Wer dort keinen Zugang hat, sieht dein Projekt in bun.ink gar nicht erst.
- **Ein aktives Abo oder eine laufende Testphase** auf beiden Seiten.
- **Zusammenführen darf nur, wer Schreibrechte im Repository hat.** Lesen und vorschlagen geht
  auch ohne.

Und eine Einschränkung, die du kennen solltest: Solange du auf einer Abzweigung arbeitest, liegt
dein Text nicht in bun.ink, sondern nur in deinem Browser – bis du ihn nach GitHub speicherst.
Das gilt beim Überarbeiten genauso wie sonst. Speichere dort früher und öfter, als du es gewohnt
bist.

## Warum das die Mühe wert ist

Ein Lektorat ist ein Gespräch über einen Text, und Gespräche gehen kaputt, wenn man sie über
Dateianhänge führt. Jemand schreibt eine Anmerkung, jemand anders überträgt sie von Hand, dabei
geht die Hälfte verloren und der Rest steht plötzlich an der falschen Stelle.

Hier bleibt jede Anmerkung an ihrer Stelle, jeder Vorschlag ist eine Entscheidung und keine
Tatsache, und am Ende kann man nachlesen, wer was vorgeschlagen und wer was übernommen hat. Nicht
weil jemand misstrauisch wäre – sondern weil ein Text, dessen Entstehung man nachlesen kann, ein
Text ist, über den man sich in einem halben Jahr noch einig werden kann.
