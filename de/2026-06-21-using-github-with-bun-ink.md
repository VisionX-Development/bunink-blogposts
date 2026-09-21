---
title: GitHub richtig nutzen – der Versionierungs-Workflow in bun.ink
date: 2026-06-21
description: Vom kostenlosen GitHub-Konto über das erste Repository bis zum kompletten Branch-, Commit- und Sync-Workflow in bun.ink – Schritt für Schritt und ohne Fachchinesisch erklärt.
---

Im Artikel [Git und GitHub einfach erklärt – Versionskontrolle für Autoren](/blog/git-and-github-for-writers) ging es um die grosse Frage: Was sind Git und GitHub eigentlich, und warum sind diese Werkzeuge gerade für Schreibende nützlich? Dieser Beitrag setzt genau dort an und wird konkret. Es geht jetzt nicht mehr um das Was, sondern um das Wie: den praktischen Workflow, mit dem du deine Dokumente über GitHub versionierst – direkt aus bun.ink heraus.

Falls dir Begriffe wie Repository, Branch oder Commit noch nichts sagen, lies am besten zuerst den vorherigen Artikel. Hier gehen wir davon aus, dass du eine grobe Vorstellung davon hast, und zeigen dir den Weg von Schritt für Schritt.

## Ein kostenloses GitHub-Konto genügt

Für diese Art der Versionskontrolle brauchst du einen GitHub-Zugang – und der ist kostenlos. Du musst keine Zahlungsdaten hinterlegen, keine Kreditkarte angeben und kein kostenpflichtiges Abo abschliessen. Ein normales, kostenloses Konto reicht für den hier beschriebenen Workflow vollständig aus.

So legst du in wenigen Minuten los:

1. Öffne [github.com](https://github.com) und klicke auf **Sign up**.
2. Gib eine E-Mail-Adresse, ein Passwort und einen Benutzernamen ein.
3. Bestätige deine E-Mail-Adresse über den Link, den GitHub dir zuschickt.
4. Fertig – du hast ein kostenloses GitHub-Konto.

Mehr ist für den Anfang nicht nötig. Erst danach kommt das erste Repository.

## Das erste Repository anlegen

Ein **Repository** ist der Ort, an dem GitHub deine Dateien und deren Versionsgeschichte speichert. Du kannst es dir wie einen Projektordner mit eingebautem Gedächtnis vorstellen: Es merkt sich jede gespeicherte Fassung.

Wichtig für das Verständnis: Ein Repository hat in bun.ink denselben Rang wie ein **Projekt**. Alle Schriftstücke eines Schreib-Projektes gehören in genau ein Repository. Du kannst beliebig viele Repositories anlegen – zum Beispiel eines pro Buch, pro Artikelserie oder pro Kunde –, aber die Dokumente eines zusammengehörenden Projektes bleiben sinnvollerweise zusammen in einem Repository.

So erstellst du dein erstes Repository auf GitHub:

1. Klicke oben rechts auf das **+** und dann auf **New repository**.
2. Vergib einen **Namen** für das Repository.
3. Wähle die Sichtbarkeit (dazu gleich mehr).
4. Klicke auf **Create repository**.

Beim Namen gibt es ein paar Regeln zu beachten: Erlaubt sind Buchstaben, Ziffern, Bindestriche, Unterstriche und Punkte. Leerzeichen sind nicht erlaubt – statt `Mein Roman` schreibst du also etwa `mein-roman`. Der Name muss innerhalb deines Kontos eindeutig sein.

## Privat oder öffentlich? Wähle privat

Beim Anlegen entscheidest du, ob das Repository **privat** oder **öffentlich** ist. Dieser Unterschied ist wichtig:

- **Öffentlich** bedeutet: Jede Person im Internet kann den Inhalt sehen.
- **Privat** bedeutet: Nur du (und ausdrücklich eingeladene Personen) seht den Inhalt.

bun.ink stellt beide Arten dar und kann mit beiden arbeiten. Aber mach dir den Unterschied bewusst: Ein öffentliches Repository ist für alle einsehbar, ein privates nur für dich. Für deine eigenen Texte ist die klare Empfehlung deshalb: **privat**. So bleibt dein Werk geschützt, bis du dich aktiv entscheidest, etwas zu teilen.

## Wie sich GitHub selbst anfühlt – und warum bun.ink es einfacher macht

Über das **GitHub-Dashboard** im Browser kannst du grundsätzlich alle Dateien einsehen und sogar bearbeiten, die mit GitHub synchronisiert sind. Auf den ersten Blick wirkt das aber umständlich, weil GitHub aus der Programmierwelt kommt und einige technische Eigenheiten mitbringt.

Ein gutes Beispiel sind Ordner. Auf GitHub kannst du nicht einfach „einen neuen Ordner anlegen". Ordner sind dort sogenannte **Pfade**, die erst durch eine Datei entstehen. Möchtest du also einen Ordner erzeugen, gehst du so vor:

1. Klicke auf **Add file** und dann auf **Create new file**.
2. Gib im Namensfeld einen Pfad ein, zum Beispiel `docs/meinedatei.md`.
3. Mit dem `/` im Namen legt GitHub automatisch den Ordner `docs` an und legt die Datei hinein.

Einen **leeren** Ordner kannst du auf GitHub nicht erstellen – ein Ordner existiert nur, solange mindestens eine Datei darin liegt.

Auch das Verzweigen von Projekten ist auf GitHub möglich: Es gibt einen Hauptast (meist `main` oder `master` genannt) und du kannst beliebig viele Seitenäste – **Branches** – erstellen, die du jeweils benennen musst.

Die Bearbeitung über bun.ink ist bewusst intuitiver und einfacher gehalten. Wir wissen dabei, dass nicht jede einzelne Möglichkeit von Git in bun.ink abgebildet ist – das ist Absicht. So kannst du zum Beispiel beim Bearbeiten eines Branches in bun.ink keine neuen Ordner oder Dokumente erstellen. Neue Ordner müssen zuerst im Hauptast (`main`) angelegt werden; danach lassen sie sich auch auf den Seitenästen bearbeiten. Was zunächst wie eine Einschränkung wirkt, erleichtert den Workflow erheblich, weil die Projektstruktur über alle Branches hinweg stabil und übersichtlich bleibt.

## Der Einstieg in bun.ink: Projekt und Repository verknüpfen

Damit bun.ink mit GitHub zusammenarbeiten kann, braucht es eine Verbindung zwischen einem **Projekt** in bun.ink und einem **Repository** auf GitHub. Den Anfang machst du im Editor in der Seitenleiste unter **Dateien**:

- Wähle ein bestehendes Projekt aus **oder** lege ein neues Projekt an.
- Alternativ kannst du ein bestehendes GitHub-Repository direkt als neues Projekt öffnen.

Die Verknüpfung selbst stösst du über den Button **Repository verknüpfen** an. bun.ink fragt dich dann, ob du das Repository **als neues Projekt öffnen** oder **mit dem aktuell geöffneten Projekt verknüpfen** möchtest. Anschliessend listet bun.ink alle deine Repositories auf – öffentliche wie private – und du wählst das passende aus.

### Einmalig: Zugriff über die OAuth-App erlauben

Damit der Austausch zwischen bun.ink und GitHub funktioniert, ist eine einmalige Freigabe nötig. Hinter bun.ink steht die Entwicklerfirma **VisionX Development**, und über deren GitHub-Konto läuft eine sogenannte **OAuth-App**. Diese App benötigt deine Erlaubnis, auf dein GitHub-Konto zuzugreifen, damit bun.ink in deinem Namen mit deinen Repositories kommunizieren kann – also Dateien lesen und schreiben kann.

Beim ersten Verbinden wirst du deshalb zu GitHub geleitet und bestätigst dort den Zugriff. Das ist ein normaler, transparenter Vorgang: Du siehst, welche Berechtigungen erteilt werden, und du kannst diese Freigabe jederzeit wieder zurücknehmen – in den GitHub-Einstellungen oder direkt im Kontobereich von bun.ink, wo du den GitHub-Account auch wieder trennen kannst.

## Der Workflow in bun.ink im Überblick

Sobald ein Projekt mit einem Repository verknüpft ist, kannst du komfortabel aus bun.ink heraus versionieren. Hier die wichtigsten Bausteine – bewusst einfach gehalten.

### Speichern und committen

Wenn du Änderungen sicherst, fragt bun.ink, wohin sie sollen. Beim Pushen nach GitHub gibst du eine **Commit-Nachricht** ein. Ein Commit ist nichts anderes als ein bewusst gesetzter Speicherpunkt mit einer kurzen Beschreibung dessen, was du geändert hast. Damit du nicht jedes Mal überlegen musst, schlägt bun.ink standardmässig das **aktuelle Datum und die aktuelle Uhrzeit** als Nachricht vor (im Format `21.06.2026 14:30`). Du kannst diesen Vorschlag einfach übernehmen oder durch eine aussagekräftige Beschreibung ersetzen, etwa „Kapitel 2 überarbeitet".

### Pushen

**Pushen** heisst, deine committeten Änderungen von bun.ink zu GitHub hochzuladen. Erst nach dem Push sind sie in deinem Repository angekommen und Teil der Versionsgeschichte. Beim Speichern hast du dafür mehrere Möglichkeiten: auf dem aktuellen Branch pushen, einen neuen Branch erstellen und dorthin pushen, oder vorerst nur lokal speichern, ohne zu pushen.

### Branches erstellen und bearbeiten

Ein **Branch** ist ein Seitenast deines Projektes, auf dem du etwas ausprobieren kannst, ohne den Hauptast zu verändern. In bun.ink erstellst du einen Branch mit wenigen Klicks und vergibst ihm einen Namen. Bist du auf einem Branch unterwegs, zeigt dir bun.ink das deutlich mit einem **Branch-Modus**-Hinweis an.

Wichtig dabei: Änderungen auf einem Branch landen **nicht** in der bun.ink-Datenbank, denn dort wird nur der Hauptast gespeichert. Branch-Stände gehören nach GitHub. Beim Speichern auf einem Branch wählst du daher, ob nach GitHub committet und gepusht werden soll – oder ob du den aktuellen Stand zusätzlich als bun.ink-Version sichern möchtest. Und wie oben erwähnt: Neue Ordner und Dokumente legst du nur auf dem Hauptast an, nicht auf einem Branch.

### Mergen

**Mergen** bedeutet, die Änderungen eines Branches zurück in den Hauptast zu übernehmen. Wenn dein Seitenast fertig ist und du mit dem Ergebnis zufrieden bist, führst du ihn über **In main mergen** mit dem Hauptast zusammen. bun.ink achtet darauf, dass der Branch vorher sauber nach GitHub gespeichert ist; andernfalls wirst du gebeten, das zuerst zu erledigen.

### Änderungen sehen und synchronisieren

Im Bereich **Änderungen** zeigt dir bun.ink, was es zu tun gibt: deine eigenen, noch nicht gepushten Änderungen einerseits und eingehende Änderungen von GitHub andererseits. Über die Diff-Ansicht kannst du jederzeit den Unterschied zum GitHub-Stand betrachten.

Die **Synchronisierungslogik** ist dabei einfach gedacht: Hat GitHub neue Änderungen, bittet dich bun.ink, zuerst zu synchronisieren, bevor du erneut pushst. Eingehende Änderungen werden automatisch übernommen, soweit sie sich nicht mit deinen eigenen überschneiden. Wo dieselbe Datei lokal und auf GitHub geändert wurde, entsteht ein **Konflikt** – und den löst du pro Datei ganz bewusst auf: die GitHub-Version übernehmen, deine eigene Version behalten oder beide als getrennte Dateien aufheben. So gehen keine Änderungen unbemerkt verloren.

## Der Fokus bleibt beim Schreiben

GitHub bringt im Hintergrund eine mächtige Versionskontrolle mit – mit allen technischen Möglichkeiten, aber auch mit einigen Hürden. bun.ink nimmt dir genau diese Hürden ab: Du arbeitest in einer aufgeräumten Schreibumgebung, und das Versionieren, Verzweigen, Zusammenführen und Synchronisieren passiert über klare, einfache Schritte.

So bekommst du die Sicherheit einer professionellen Versionskontrolle, ohne ihre Komplexität – und der Fokus bleibt dort, wo er hingehört: beim Schreiben.
