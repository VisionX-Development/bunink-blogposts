---
title: Wie bun.ink deine Texte schützt – Verschlüsselung einfach erklärt
date: 2026-07-28
description: Was mit deinen Texten passiert, bevor sie gespeichert werden – die serverseitige Verschlüsselung für alle Dokumente, der High-Privacy-Ordner und das High-Privacy-Projekt für dein Tagebuch, und wofür du dabei selbst verantwortlich bist.
---

Ein Text ist etwas Persönliches. Ein halbfertiges Kapitel, eine Recherche mit Quellen, die niemand kennen soll, ein Tagebucheintrag von einem schlechten Tag – das sind keine beliebigen Daten. Deshalb ist die Frage „Wer kann das eigentlich lesen?" bei einer Schreib-App keine technische Randnotiz, sondern eine Vertrauensfrage.

Dieser Artikel beantwortet sie so genau wie möglich – ohne Fachvokabular, aber auch ohne Versprechen, die wir nicht halten können.

## Zwei Schichten – eine für alle, eine für dein Tagebuch

bun.ink schützt Inhalte auf zwei Ebenen, und es ist wichtig, sie auseinanderzuhalten:

- **Schicht 1 – serverseitige Verschlüsselung.** Gilt für alle Dokumente, ohne dass du etwas tun oder einstellen musst. Deine Texte liegen in der Datenbank nicht als lesbarer Klartext.
- **Schicht 2 – der High-Privacy-Ordner oder ein High-Privacy-Projekt.** Ein besonderer Ordner- oder Projekttyp, den du selbst anlegst. Seine Inhalte werden **in deinem Browser** verschlüsselt. Niemand ausser dir kann sie lesen – auch wir nicht.

Schicht 1 ist Komfort ohne Kompromiss. Schicht 2 ist maximaler Schutz gegen einen Preis, den du kennen solltest. Beides erklären wir hier der Reihe nach.

## Kurz vorweg – was Verschlüsselung überhaupt macht

Stell dir einen Text vor, der durch eine Maschine läuft und als unlesbarer Zeichensalat wieder herauskommt. Die Maschine braucht dafür einen **Schlüssel** – eine lange, zufällige Zahl. Mit demselben Schlüssel läuft der Zeichensalat wieder zurück in den ursprünglichen Text. Ohne den Schlüssel ist er praktisch nicht rekonstruierbar; kein Rätsel, das man mit Geduld lösen kann, sondern eine Rechenaufgabe, die selbst mit riesigen Rechenzentren nicht in Menschenlebensdauern aufgeht.

bun.ink verwendet dafür **AES-256-GCM**, das Standardverfahren, mit dem auch Banken, Behörden und HTTPS-Verbindungen arbeiten. Zwei Eigenschaften davon sind für dich praktisch relevant:

- **Jede Speicherung nutzt einen frischen Zufallswert.** Zweimal derselbe Text ergibt zweimal völlig unterschiedlichen Zeichensalat. Aus den gespeicherten Daten lässt sich also nicht erkennen, dass zwei Dokumente denselben Inhalt haben.
- **Jeder verschlüsselte Text trägt ein Siegel.** Verändert jemand die gespeicherten Daten auch nur um ein Zeichen, lässt sich der Text nicht mehr entschlüsseln – die Manipulation fällt sofort auf, statt still einen verfälschten Text auszuliefern.

Ausserdem gilt: **Für jede Art von Daten ein eigener Schlüssel.** Dokumentinhalte, GitHub-Zugangstoken und Backups haben jeweils ihren eigenen. Wer den einen hätte, käme mit den anderen Daten nichts anfangen. Die Schlüssel liegen nie im Programmcode und nie in deinem Repository, sondern ausschliesslich in der Konfiguration des Servers und in einem Passwortmanager.

## Schicht 1 – deine Texte liegen nicht im Klartext in der Datenbank

Wenn du speicherst, geht dein Text verschlüsselt in die Datenbank. Der Server verschlüsselt ihn direkt vor dem Schreiben und entschlüsselt ihn nach dem Lesen wieder – dazwischen ist er in der Datenbank nur Zeichensalat. Dasselbe gilt für gespeicherte Versionen (die Schnappschüsse deiner Textgeschichte) und für deine Textschnipsel.

Davon merkst du **nichts**. Volltextsuche, Versionsvergleiche, Konfliktbehandlung, GitHub-Sync: alles funktioniert unverändert und ohne spürbare Verzögerung – Verschlüsselung dieser Art arbeitet im Bereich von Millisekunden, nicht Sekunden.

Wogegen dich das schützt:

- **Ein Datenbank-Leak.** Wer sich Zugriff auf die Datenbank verschafft, hat Zeichensalat, keine Texte.
- **Ein gestohlenes oder verlorenes Backup.** Backups enthalten dieselben verschlüsselten Daten – und sind zusätzlich selbst verschlüsselt.
- **Zugriff über die Datenbank-Konsole.** Auch wer sich dort umsieht – heute oder als künftiges Teammitglied – sieht deine Inhalte nicht.

Und jetzt der ehrliche Teil, denn dieser Punkt entscheidet, ob du Schicht 2 brauchst:

- **Schicht 1 ist kein „niemand kann es lesen".** Der Server braucht den Schlüssel, um dir deinen Text im Editor zu zeigen. Wer Zugriff auf die Server-Konfiguration hat – also wir als Betreiber – hat damit technisch auch Zugriff auf den Schlüssel. Wir tun das nicht, aber die Verschlüsselung allein verhindert es nicht. Genau diese Lücke schliesst Schicht 2.
- **GitHub bleibt absichtlich lesbar.** „Git für Writers" lebt davon, dass in deinem Repository echte, lesbare Markdown-Dateien liegen – dort kannst du sie auf jedem Gerät öffnen, und dort können [AI-Agenten](/blog/ai-controlled-writing-partner) mit ihnen arbeiten. Verschlüsselter Zeichensalat im Repo wäre nutzlos. Die Verschlüsselung schützt also unsere Datenbank, nicht dein GitHub-Konto; für dein Repository gelten die Zugriffsrechte, die du auf GitHub selbst setzt (ein privates Repository bleibt privat).
- **Namen und Zahlen bleiben sichtbar.** Dokument-, Projekt- und Ordnernamen, Zeitstempel, Versionszahlen und die ungefähre Textlänge werden nicht verschlüsselt – sie sind nötig, damit Listen, Sortierung und Baumansicht funktionieren. Nenne einen Ordner also nicht nach dem Geheimnis, das darin steht.

## Schicht 2 – der High-Privacy-Ordner oder ein High-Privacy-Projekt

Für ein Tagebuch, für vertrauliche Quellen, für Texte, die niemand sehen soll, gibt es zwei Varianten von **High-Privacy**. Der Unterschied zu Schicht 1 klingt klein, ist aber grundlegend: Hier wird nicht auf dem Server verschlüsselt, sondern **in deinem Browser** – bevor irgendetwas unser Rechenzentrum erreicht. Beim Server und in der Datenbank kommt nur noch Zeichensalat an, für den dort kein Schlüssel existiert.

Du wählst beim Anlegen, wie gross der geschützte Bereich sein soll:

- **High-Privacy-Ordner.** Schützt genau diesen einen Ordner (und seine Unterordner) innerhalb eines ansonsten normalen Projekts. Der Rest des Projekts bleibt normal nutzbar – inklusive GitHub-Sync, der die verschlüsselten Dokumente einfach auslässt.
- **High-Privacy-Projekt.** Schützt das gesamte Projekt automatisch, auch Dokumente, die direkt im Projekt liegen und in keinem Ordner stecken. Dafür lässt sich ein solches Projekt gar nicht erst mit GitHub verknüpfen – es gäbe ja nichts Synchronisierbares darin.

Kryptografisch ist beides identisch: derselbe Algorithmus, derselbe Ablauf, dieselben Regeln. Ein Projekt und seine Ordner können aber nicht gemischt werden – in einem High-Privacy-Projekt lässt sich kein zusätzlicher High-Privacy-Ordner anlegen, das wäre ein Schlüssel im Schlüssel. Alles, was im Folgenden für den „High-Privacy-Ordner" beschrieben ist, gilt daher unverändert auch für das High-Privacy-Projekt.

Das ist echte Ende-zu-Ende-Verschlüsselung. Wir können diese Inhalte nicht lesen, nicht durchsuchen, nicht wiederherstellen und niemandem herausgeben – auch nicht aus Backups, denn dort steht dasselbe Unlesbare.

So funktioniert es, in einfachen Worten:

1. Beim Anlegen erzeugt dein Browser einen zufälligen **Ordner-Schlüssel**. Mit ihm werden alle Dokumente in diesem Ordner ver- und entschlüsselt.
2. Du wählst eine **Passphrase**. Aus ihr rechnet der Browser einen zweiten Schlüssel, der den Ordner-Schlüssel wie in einen Safe einschliesst. Nur dieser verschlossene Safe wird gespeichert – die Passphrase selbst verlässt deinen Browser nie und wird nirgends gespeichert.
3. Diese Umrechnung ist absichtlich **rechenintensiv** (Argon2id, ein Verfahren speziell gegen Passwort-Rateangriffe). Ein Angreifer, der Millionen Passphrasen durchprobieren möchte, muss für jeden Versuch spürbar Rechenzeit und Speicher aufwenden. Für dich dauert es beim Entsperren weniger als eine Sekunde.
4. Nach dem Anlegen zeigt bun.ink dir **einmalig** einen **Wiederherstellungsschlüssel**. Das ist der Ordner-Schlüssel selbst, in Textform. Er öffnet den Ordner auch dann, wenn du die Passphrase vergessen hast.
5. Beim Öffnen eines Dokuments fragt bun.ink nach der Passphrase (oder dem Wiederherstellungsschlüssel). Danach arbeitest du normal weiter: Editor, lokale Suche, Wortzählung. Beim Speichern verschlüsselt dein Browser wieder.
6. Der entsperrte Schlüssel lebt **nur im Arbeitsspeicher** dieser Browser-Sitzung – nie in einem Cookie, nie in einem lokalen Speicher. Ein Neuladen oder Logout sperrt den Ordner automatisch wieder.

Eine falsche Passphrase wird übrigens zuverlässig erkannt, ohne dass irgendwo ein Passwort hinterlegt sein muss: Der Safe lässt sich damit einfach nicht öffnen, und das Siegel der verschlüsselten Daten schlägt Alarm.

## Deine Verantwortung – und sie ist echt

Ende-zu-Ende-Verschlüsselung bedeutet: Der Schutz liegt bei dir, weil der Schlüssel bei dir liegt. Daraus folgt der wichtigste Satz dieses Artikels:

> **Wenn du Passphrase _und_ Wiederherstellungsschlüssel verlierst, sind die Inhalte dieses Ordners oder Projekts endgültig verloren.**

Endgültig heisst wirklich endgültig. Es gibt kein „Passwort zurücksetzen", keinen Support-Weg, keinen Notschlüssel und keine Wiederherstellung aus dem Backup. Wir haben nichts, womit wir helfen könnten – und genau das ist ja der Sinn der Sache. Ein Hintertürchen für uns wäre auch ein Hintertürchen für alle anderen. Bei einem High-Privacy-Projekt wiegt das potenziell schwerer als bei einem einzelnen Ordner, weil dort auf einen Schlag der gesamte Projektinhalt betroffen ist.

Deshalb, bevor du den ersten Satz in so einen Ordner oder ein solches Projekt schreibst:

- **Passphrase in den Passwortmanager**, sofort und nicht „später". Sie ist nicht dein bun.ink-Passwort, sondern eine zusätzliche, eigene Passphrase.
- **Wiederherstellungsschlüssel sichern**, solange er angezeigt wird – Passwortmanager, verschlüsselte Notiz, oder ausgedruckt an einem Ort, an dem du auch Ausweispapiere aufbewahrst. Er wird nur ein einziges Mal gezeigt.
- **Zwei Orte statt einem.** Passphrase und Wiederherstellungsschlüssel sind dein Backup füreinander. Bewahre sie so auf, dass nicht ein einziges verlorenes Gerät beide mitnimmt.
- **Einmal üben.** Lade die Seite neu und entsperre den Ordner erneut – am besten einmal mit der Passphrase und einmal mit dem Wiederherstellungsschlüssel. So weisst du, dass beides wirklich funktioniert, solange der Ordner noch leer ist.

Die Passphrase kannst du später jederzeit ändern (Kontextmenü des Ordners). Der Ordner-Schlüssel bleibt dabei derselbe, es muss nichts neu verschlüsselt werden – und dein Wiederherstellungsschlüssel bleibt gültig, denn er hängt am Ordner-Schlüssel, nicht an der Passphrase.

## Was High-Privacy kostet

Weil der Server diese Inhalte nicht lesen kann, kann er auch nichts damit tun. Das ist kein fehlendes Feature, sondern die logische Konsequenz – aber du solltest sie vor dem Anlegen kennen. Die folgenden Punkte gelten für Ordner und Projekt gleichermassen:

- **Kein GitHub.** Dokumente aus High-Privacy-Ordnern werden nie zu GitHub synchronisiert; sie tauchen in keinem Push, keinem Pull und keinem Commit auf, der Rest des Projekts bleibt aber verknüpfbar. Ein High-Privacy-**Projekt** lässt sich erst gar nicht mit GitHub verknüpfen – dort gibt es ja nichts Unverschlüsseltes, das synchronisiert werden könnte. Versionierung über Git, Branches und die Arbeit mit AI-Agenten stehen für diese Texte also nicht zur Verfügung.
- **Suche nur lokal und nur entsperrt.** Die projektweite Suche kann verschlüsselte Dokumente nicht durchsuchen. Ist der Ordner entsperrt, sucht bun.ink lokal in deinem Browser mit; ist er gesperrt, werden diese Dokumente übersprungen.
- **Keine Versionsvorschau und kein Vergleich.** Versionen werden gespeichert – verschlüsselt und sicher –, aber Vorschau und Zeile-für-Zeile-Vergleich sind für diese Dokumente derzeit deaktiviert.
- **Nach jedem Neuladen wieder gesperrt.** Es gibt für diese Dokumente absichtlich keinen lokalen Zwischenspeicher und keine Wiederherstellung offener Tabs, damit kein Klartext auf dem Gerät zurückbleibt. Du gibst die Passphrase also einmal pro Sitzung ein.
- **Bei einem Speicherkonflikt gewinnt Neuladen.** Hast du denselben Text parallel in zwei Fenstern geändert, kann der Server die Fassungen nicht vergleichen. Statt eines Zusammenführens heisst es dann: neu laden, entsperren, weiterarbeiten.
- **Die Entscheidung ist endgültig.** Ein Ordner oder Projekt ist von Anfang an High-Privacy oder normal. Nachträglich lässt sich die Verschlüsselung nicht ein- oder ausschalten, und Dokumente lassen sich nicht zwischen verschlüsseltem und normalem Bereich verschieben – der Schlüssel würde am Ziel nicht mehr passen. Willst du wechseln, kopierst du den Text von Hand in einen neu angelegten Ordner oder ein neu angelegtes Projekt. Unterordner sind erlaubt und erben den Schutz; ein High-Privacy-Ordner innerhalb eines High-Privacy-Projekts ist dagegen nicht möglich – ein Projekt ist entweder ganz geschützt oder gar nicht.
- **Namen und Grössen bleiben sichtbar.** Wie in Schicht 1 sind Ordner- und Dokumentnamen, Zeitstempel, Anzahl Versionen und Wortzahlen nicht verschlüsselt. Nur der Inhalt ist es.
- **Dein Gerät bleibt deine Aufgabe.** Verschlüsselung im Browser hilft nicht gegen einen Rechner mit Schadsoftware oder ein unbeaufsichtigtes, entsperrtes Notebook. Beim Schreiben ist der Text zwangsläufig lesbar – auf deinem Bildschirm.

## Was wir empfehlen

Für die meisten Projekte – Buchmanuskript, Artikel, Dokumentation – ist der normale Ordner der richtige Ort. Deine Inhalte sind dort verschlüsselt gespeichert, und du behältst alles, was bun.ink stark macht: [Versionierung über GitHub](/blog/using-github-with-bun-ink), Vergleiche, Branches, [AI-Unterstützung](/blog/ai-controlled-writing-partner).

High-Privacy nimm bewusst und gezielt für das, was wirklich niemanden sonst betrifft: Tagebuch, Therapienotizen, geschützte Quellen, sehr persönliche Entwürfe. Für gelegentlich private Inhalte neben einem sonst normalen Projekt reicht meist ein einzelner **Ordner** „Tagebuch". Schreibst du dagegen konsequent alles in einem eigenen, durchgehend privaten Zusammenhang – etwa ein persönliches Tagebuch-Projekt mit vielen Dokumenten, oder Notizen aus einer Therapie – ist ein eigenes **High-Privacy-Projekt** oft die aufgeräumtere Wahl, weil dann auch Dokumente direkt im Projekt automatisch mitgeschützt sind. In beiden Fällen gilt: nicht alles verschlüsseln, sondern das Richtige.

Und ganz unabhängig davon, in welchem Ordner du schreibst: Deine Texte liegen in Europa, sie werden verschlüsselt gespeichert, sie sind täglich gesichert – und sie bleiben deine. Als Markdown, in einem offenen Format, jederzeit exportierbar. Genau [darum haben wir bun.ink gebaut](/blog/why-bun-ink-exists).
