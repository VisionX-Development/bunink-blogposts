---
title: Deine Arbeit belegen – was das KI-Wasserzeichen nicht verrät
date: 2026-09-20
description: Seit diesem Sommer tragen KI-erzeugte Texte ein unsichtbares Wasserzeichen – auch dann, wenn nur die Rechtschreibhilfe darübergelaufen ist. Warum daraus falsche Vorwürfe entstehen – und warum deine Commit-Historie kein Beweis ist, aber ein Beleg, den nur du erklären kannst.
---

Vor einer Weile haben wir hier beschrieben, wie sich eine KI als
[kontrollierter Schreibpartner](/blog/ai-controlled-writing-partner) einsetzen lässt: mit klaren
Regeln und einem Agenten, der prüft und vorschlägt, während der Mensch entscheidet.

Hier geht es um eine Frage, die sich unabhängig davon stellt: Wie belegst du, dass ein Text deine
Arbeit ist?

Wie jemand mit KI umgeht, ist eine persönliche Entscheidung, die dieser Artikel niemandem abnimmt.
Manche lassen sich Szenen vorschlagen, manche wollen keine Zeile davon, und die meisten liegen
dazwischen: Sie schreiben jeden Satz selbst und lassen die Rechtschreibung prüfen.

Für die Frage nach dem Nachweis spielt diese Haltung erstaunlich wenig Rolle. Die Antwort liegt in
keinem Fall im fertigen Text, sondern in seiner Entstehung – und genau die hält die Versionierung
fest, die bun.ink ohnehin mitbringt.

## Das neue Problem: den Negativbeweis führen

Wer einen Text abliefert, muss zunehmend etwas belegen können, das vor kurzem niemand belegen
musste: dass er ihn selbst geschrieben hat. Verlage lassen sich das versichern, Redaktionen nehmen
entsprechende Klauseln in Verträge auf. Die Werkzeuge, mit denen dabei geprüft wird, taugen wenig:
KI-Detektoren raten anhand von Oberflächenmerkmalen und liegen regelmässig falsch – auch bei
Menschen, die einfach nur sauber schreiben.

Das Kernproblem: Wer einen Text verfasst hat, sieht man ihm nicht an. Ein fertiger Text ist ein
Ergebnis, und Ergebnisse sehen sich ähnlich, egal wie sie entstanden sind. Der Unterschied liegt in
der Entstehung – und die ist normalerweise verschwunden, sobald die Datei gespeichert ist.
Maschinell erzeugter Text trägt inzwischen zwar eine Markierung; sie beantwortet aber ausgerechnet
diese Frage nicht – gleich mehr dazu.

## Die dritte Gruppe: eigener Text, fremde Werkzeuge

Über eine der drei Haltungen vom Anfang wird am wenigsten gesprochen, obwohl sie vermutlich die
häufigste ist: Menschen, die jeden Satz selbst schreiben, aber eine Rechtschreib- oder
Grammatikprüfung, ein digitales Lektorat benutzen.

Dass solche Werkzeuge unter der Haube längst Sprachmodelle einsetzen, sieht man ihnen nicht an. Wer
eine Grammatikkorrektur annimmt, hat nicht das Gefühl, mit einer KI zu schreiben – und hat recht
damit. Trotzdem ist an einer Stelle eine Maschine über den Text gelaufen. Genau daraus ist seit
diesem Sommer ein Problem geworden.

## Das Wasserzeichen ist keine Zukunftsmusik

Seit Sommer 2026 versehen die grossen Anbieter ihre Modelle mit einem unsichtbaren Wasserzeichen im
erzeugten Text. Bei Anthropic trägt es jedes Modell ab dem 2. August 2026, ältere sollen bis zum 2. Dezember 2026 nachgezogen haben. Abschalten lässt es sich nicht. Dahinter stehen die
Transparenzpflichten des europäischen KI-Rechts, andere Anbieter gehen denselben Weg.

Entscheidend ist, wo diese Markierung auftaucht: **Jedes Werkzeug, das im Hintergrund ein solches
Modell benutzt, hinterlässt sie** – auch die Rechtschreibhilfe. Und sie ist zäh: Sie steckt nicht in
einer Datei-Eigenschaft, sondern in der Wortwahl selbst. Sie übersteht Kopieren, Einfügen,
Umformatieren – und verschwindet erst, wenn die Stelle vollständig neu geschrieben wird.

## Was ein Wasserzeichen aussagt – und was nicht

Für die dritte Gruppe wird es jetzt unangenehm, aus einem Grund, der nichts mit schlechter Technik
zu tun hat: Die Markierung ist grob. Sie belegt, dass ein Modell beteiligt war – nicht, dass es den
Text geschrieben hat. Anthropic sagt das selbst deutlich: Sie unterscheidet nicht zwischen
geschrieben, überarbeitet, übersetzt und zusammengefasst. Wer den eigenen Text Korrektur lesen
lässt, bekommt dieselbe Markierung wie jemand, der ein ganzes Kapitel erzeugen liess.

Dazu kommt das eigentliche Ärgernis: **Du kannst es selbst nicht nachprüfen.** Die Erkennung steht
bisher nur berechtigten Stellen offen – Behörden, Medien, Forschung. Ein öffentliches Werkzeug, mit
dem du einen Vorwurf entkräften könntest, gibt es nicht.

Daraus folgt der Satz, um den sich dieser Artikel dreht: Wenn dir jemand vorhält, dein Text sei «von
der KI», widerlegst du das nicht, indem du auf den fertigen Text zeigst. Dein Beleg ist nicht das
Ergebnis. Dein Beleg ist der Weg dorthin.

Den Stand zum Wasserzeichen erklärt Anthropic in seiner
[Hilfe zur Kennzeichnung KI-erzeugter Inhalte](https://support.claude.com/en/articles/16266773-how-claude-marks-ai-generated-content).

## Was in einer Versionierung ausser dem Text noch steht

Genau hier tut die Versionierung etwas, das sie eigentlich für ganz andere Zwecke tut. Wenn du in
bun.ink arbeitest, speicherst du keine Datei, die sich selbst überschreibt, sondern legst
Speicherpunkte an – Commits, die festhalten, wie der Text aussah, wann das war und was du notiert
hast. Was Commits, Branches und Repository bedeuten, erklärt
[Git und GitHub einfach erklärt](/blog/git-and-github-for-writers).

Dadurch entsteht neben deinem Text ein zweiter, den niemand bewusst schreibt: seine
Entstehungsgeschichte. Wann der erste Absatz da war, welcher Satz drei Wochen lang unverändert
stand, wo du eine Szene verworfen und später anders wieder aufgenommen hast. Diese zweite Ebene ist dein Beleg – sie entsteht nebenbei, während du ganz normal arbeitest. Die Zeitleiste: wann welcher Satz entstanden ist

Im Writer kannst du diese Historie auch lesen. Im Changes-Tab gibt es den **Commit-Browser**: eine
Liste aller Speicherpunkte, jeder mit Zeitstempel und Nachricht. Du wählst zwei Stände – etwa den
ersten Commit und den von heute – und siehst dazwischen jede Änderung hervorgehoben. Ausführlich
beschrieben in [Der Commit-Browser](/blog/browsing-your-commit-history).

Wenn dich also jemand fragt, ob Kapitel 7 wirklich von dir ist, musst du nicht beteuern. Du kannst
die vierzig Speicherpunkte zeigen, aus denen es geworden ist.

## Warum Mikroschritte überzeugender sind als ein fertiges Kapitel

Der eigentliche Beweis liegt nicht in einem einzelnen Commit, sondern in der **Form** der Historie.
Menschliches Schreiben ist krumm: Ein Absatz wächst über eine Woche in sieben Schritten, ein anderer
entsteht in zwanzig Minuten und wird am nächsten Tag halbiert. Es gibt Tage mit vierhundert Wörtern
und Tage mit vierzig, Sätze, die dreimal umgestellt werden, Streichungen, Pausen, Rückkehr.

Genau das steht in einer gewachsenen Commit-Historie – und genau das fehlt, wenn ein Kapitel in
einem einzigen Schritt auftaucht: vollständig, ohne eine einzige Überarbeitung danach. Ein Text, der
so entsteht, ist entweder anderswo entstanden oder erzeugt worden. Beides sieht anders aus als
Arbeit.

Je kleiner du speicherst, desto dichter wird dieser Nachweis. Das ist kein Zusatzaufwand für eine
Prüfinstanz – es ist ohnehin die Arbeitsweise, die dir beim Zurückgehen hilft.

## Vorher und nachher: was die Historie über das Werkzeug verrät

Für die dritte Gruppe wird das sehr konkret. Deine Historie enthält den Absatz, **bevor** das
Werkzeug ihn angefasst hat: Der Commit vom Dienstagabend zeigt deine Fassung, der vom Mittwochmorgen
zeigt, was die Korrektur daraus gemacht hat. Dazwischen liegt ein Vergleich, den jeder lesen kann –
ein Komma, zwei umgestellte Wörter.

Damit verschiebt sich die Frage von «Ist da Maschine drin?» zu «Was genau hat sie getan?». Du
beweist nicht, dass nie ein Werkzeug im Spiel war – das kannst du seit diesem Sommer ohnehin nicht
mehr. Du beweist Urheberschaft: dass der Text von dir stammt und das Werkzeug ihn an den Rändern
berührt hat, nicht in der Substanz.

Praktisch heisst das: **ein Commit vor dem Werkzeug, ein Commit danach.** Zehn Sekunden Aufwand –
und die Grenze zwischen deiner Arbeit und der Korrektur ist dauerhaft dokumentiert. Weil sich die
Markierung nicht herauswaschen lässt und du sie selbst nicht prüfen kannst, ist deine Historie der
einzige Nachweis, der dir gehört.

## Die Statistik macht es sichtbar

Was in der Historie steckt, lässt sich auch ansehen statt lesen. Die
[Schreibstatistik](/blog/writing-statistics-that-motivate) im Writer zeigt deine Arbeit als Zahlen
und Bilder: Wörter pro Tag und Woche, aktive Schreibzeit, eine Heatmap über zwölf Monate. Für
Projekte mit Repository kommt die Commit-Aktivität dazu.

Ein Jahr Schreibarbeit sieht darin aus wie ein Jahr Schreibarbeit: ungleichmässig, mit Löchern und
dichten Phasen vor Abgabeterminen – nicht wie drei Nachmittage, an denen ein Buch erschienen ist.
Die Statistik zählt dabei dich, nicht deinen Text: Erfasst werden Wortmengen und Zeiten, keine
Inhalte.

## GitHub als unbeteiligter Zeuge

Bis hierhin liegt alles bei dir – und alles, was bei dir liegt, kannst du im Zweifel auch selbst
inszeniert haben. Der letzte Schritt macht daraus etwas Belastbares: Ist dein Projekt mit GitHub
verknüpft, landen deine Commits bei einem Dritten, der nichts mit deinem Text zu tun hat. Wie das
geht, steht in [GitHub richtig nutzen](/blog/using-github-with-bun-ink).

Ein Zeitstempel, den du selbst setzt, ist eine Behauptung. Einer auf einem fremden Server ist ein
Beleg. Du gibst Zugriff so grob oder fein, wie du willst – eine Person einladen, das Repository
öffnen, oder die Commit-Liste exportieren. Aus «Ich habe das selbst geschrieben» wird «Hier sind die
312 Schritte, mit Datum».

## Und die Sicherheit deiner Texte?

Eine Frage vom Anfang ist offengeblieben: *Landet mein Manuskript irgendwo in einem Training?* Bei
bun.ink ist die Antwort kurz. Die App schickt deine Texte nicht an ein Sprachmodell, und in der
Datenbank liegen sie nicht als lesbarer Klartext, sondern verschlüsselt. Wie das im Detail
funktioniert, steht in [Wie bun.ink deine Texte schützt](/blog/how-bun-ink-protects-your-texts).

Dein Text geht also nirgends hin – weder in ein Training noch als Klartext in eine Datenbank. Was
daraus für den Nachweis folgt, hat allerdings eine Kehrseite.

## Ein ehrlicher Vorbehalt

Sie lautet: Beides zugleich geht nicht. Ein High-Privacy-Projekt, das deinen Schlüssel nie verlässt,
hat bewusst keine GitHub-Historie – maximal privat und öffentlich nachweisbar schliessen einander
aus. bun.ink lässt dich das pro Projekt entscheiden.

Und ein zweiter Vorbehalt: Forensischer Beweis ist eine Historie nicht, sie liesse sich mit genügend
Aufwand inszenieren. Was die Versionierung leistet, ist bescheidener und trotzdem nützlich: Sie
verschiebt die Frage von «sieht der Text menschlich aus?» zu «gibt es eine über Wochen gewachsene,
stimmige Arbeitsspur?». Das ist die bessere Frage, und sie lässt sich beantworten.

## Was du dafür tun solltest

Wenn dir dieser Nachweis wichtig ist, lohnen sich ein paar Gewohnheiten:

- **Früh anfangen.** Die Historie beginnt mit dem ersten Commit, nicht erst beim fertigen Manuskript.
- **Klein speichern.** Lieber fünf Commits an einem Nachmittag als einen am Monatsende.
- **Ehrliche Nachrichten schreiben.** «Dialog gekürzt, Rückblende raus» sagt mehr als «Update».
- **Umwege stehen lassen.** Verworfene Fassungen sind kein Makel, sie sind der Beleg.
- **Werkzeuge einrahmen.** Vor und nach jedem Durchlauf durch eine Korrekturhilfe einmal speichern.
- **Den Agenten getrennt halten.** Grössere KI-Arbeit gehört auf einen eigenen Branch und unter das
eigene Konto des Agenten – die Unterscheidung ist der halbe Nachweis.
- **Überarbeitungen auch im Alleingang.** Was du verworfen hast, bleibt so mitsamt Begründung
dokumentiert – wie das geht, steht in [Das Lektorat kommt zum Text](/blog/reviews-as-pull-requests).

## Zum Schluss: ein offenes Buch, in beide Richtungen

Eine faire Warnung zum Schluss: Was hier als Nachweis beschrieben wird, funktioniert in beide
Richtungen. Eine Versionierung, die zeigt, dass ein Kapitel in vierzig Schritten gewachsen ist,
zeigt genauso, dass ein anderes in einem Schritt fertig dastand. Wer mit KI arbeitet, hinterlässt
eine erkennbare Spur in der Historie – und seit diesem Sommer zusätzlich eine im Text selbst.

Für die meisten ist das kein Problem: Wer sein Werkzeug offenlegt, hat nichts zu verbergen, und ein
gut geführtes Repository zeigt sogar, was vorgeschlagen und was übernommen wurde – genau der
Gedanke im Artikel über den [kontrollierten Schreibpartner](/blog/ai-controlled-writing-partner).

Denn das ist der Preis und der Wert derselben Sache: Mit bun.ink ist der Entstehungsprozess eines
Textes ein sprichwörtlich offenes Buch. Wer jede Zeile selbst schreibt, findet darin den Nachweis,
auf den er künftig angewiesen sein wird. Wer sich nur korrigieren lässt, findet den Unterschied
zwischen «da war eine Maschine im Spiel» und «hier steht, was sie getan hat». Und wer mit KI
arbeitet, findet die Wahrheit über seine Arbeitsweise. Nur unsichtbar ist der Prozess nicht mehr.
