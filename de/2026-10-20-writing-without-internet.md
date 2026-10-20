---
title: Schreiben ohne Internet – mit Text, der nicht verloren geht
date: 2026-10-20
description: Wie bun.ink im Zug, im Ferienhaus oder im Flugzeug weiterläuft, was offline geht, was nicht, und was mit deinem Text passiert, wenn die Verbindung zurückkommt.
---

Die besten Schreibstunden liegen oft dort, wo das Netz aufhört: im Zug, im Ferienhaus, im Flugzeug. Eine Schreib-App im Browser ist da meistens am Ende – die Seite lädt nicht, und was du vor dem Funkloch getippt hast, hängt irgendwo zwischen Tab und Server.

[bun.ink](https://bun.ink) ist ein Schreibeditor für Markdown, auf Wunsch mit deinem eigenen GitHub-Repository dahinter. Seit dieser Woche läuft es auch ohne Verbindung weiter, ein paar Tage lang, im Browser-Tab, als installierte App am Computer und auf dem iPhone. Die Regel dahinter: **Was du schreibst, bleibt auf deinem Gerät, bis der Server es sicher hat – und nichts wird stillschweigend überschrieben.**

## Vorbereiten, einmal

Offline gibt es nur, was vorher auf dem Gerät liegt. Dafür gibt es zwei Wege:

- **Von Hand:** Rechtsklick auf ein Projekt in der Seitenleiste (am Handy lange drücken) und **Offline verfügbar** wählen. Eine kleine Wolke am Projektnamen zeigt, dass es bereitliegt.
- **Automatisch:** Unter **Einstellungen → Konto → Offline auf diesem Gerät** schaltest du **Geöffnete Projekte automatisch offline verfügbar machen** ein. Dann wird jedes Projekt, das du auf diesem Gerät öffnest, von selbst mitgenommen.

Die Automatik ist bewusst ein Schalter pro Gerät und nicht einfach immer an. Die Kopie liegt lesbar im Speicher des Browsers. Auf deinem Laptop ist das genau richtig, auf dem Rechner in der Bibliothek nicht.

Danach musst du nichts mehr tun. Solange du online bist, hält bun.ink die Kopie aktuell: beim Öffnen, nach jedem Speichern und wenn du im Projekt einen Ordner anlegst oder etwas umbenennst.

Auf iPhone und iPad gibt es eine Besonderheit: iOS kann Daten eines Browser-Tabs nach einigen Tagen ohne Nutzung löschen. Lege bun.ink deshalb über **Teilen → Zum Home-Bildschirm** als App an und mache das Projekt **dort** offline verfügbar. Die App hat ihren eigenen, geschützten Speicher.

## Wenn das Netz wegfällt

Du merkst es kaum. Fällt die Verbindung beim Schreiben weg, schreibst du einfach weiter. Öffnest du bun.ink ohne Netz, lädt es den Editor aus der Kopie auf dem Gerät, mit dem Hinweis **Offline – du arbeitest mit der Kopie auf diesem Gerät.**

Offline kannst du:

- vorhandene Dokumente bearbeiten, schliessen und wieder öffnen,
- neue Dokumente anlegen, umbenennen, verschieben, exportieren und wieder löschen,
- High-Privacy-Bereiche mit deiner Passphrase entsperren und darin schreiben,
- im Projekt suchen und Snippets verwenden.

Was offline geändert ist, erkennst du auf einen Blick: Der Punkt am Tab bleibt rot, und im Explorer steht hinter dem Dokument eine kleine Wolke. Sie bedeutet: **bisher nur auf diesem Gerät gespeichert.** Sichern musst du nichts – bun.ink legt jeden Stand laufend auf dem Gerät ab, auch wenn du das Fenster schliesst.

Alles, was den Server braucht, wartet: GitHub, der Versionsverlauf, die Ansicht der Änderungen, Projekte und Ordner anlegen, vorhandene Dokumente umbenennen oder löschen. Ein Klick darauf sagt **Offline nicht verfügbar**, und du bleibst im Editor. Dasselbe gilt für Links auf Seiten wie die Einstellungen oder den Blog. Sie führen offline nicht mehr ins Leere.

## Wieder online

Kommt die Verbindung zurück, lädt bun.ink deine Änderungen hoch. Hattest du die App ohne Netz geöffnet, zeigt der Hinweis **Du bist wieder online**, und **Online weiterarbeiten** holt den normalen Editor. Der Wechsel passiert bewusst auf Klick, damit er dich nicht mitten im Satz unterbricht. Danach verschwinden Wolken und rote Punkte, und bun.ink meldet, wie viele Offline-Änderungen hochgeladen wurden.

Spannend wird es, wenn du dasselbe Dokument in der Zwischenzeit auf einem zweiten Gerät geändert hast. Dann überschreibt bun.ink nichts. Es zeigt den Dialog **Dokument wurde an anderer Stelle gespeichert**:

- **Lokale Version sichern** legt deine Offline-Fassung als Version in den Verlauf. Das Dokument trägt danach den neueren Stand vom anderen Gerät, und deine Fassung kannst du jederzeit wiederherstellen.
- **Trotzdem überschreiben** nimmt deine Offline-Fassung als neuen Stand.

Bei High-Privacy-Dokumenten verlässt der Text das Gerät ohnehin nur verschlüsselt. Deshalb kann bun.ink ihn auch hochladen, wenn der Bereich gesperrt ist. Nur zum Vergleichen im Konfliktfall musst du entsperren, denn vergleichen lässt sich nur Klartext. Bis dahin bleibt dein Text auf dem Gerät.

## Vierzehn Tage

Ein Gerät darf vierzehn Tage nach dem letzten Kontakt mit dem Server offline schreiben. Die Frist erneuert sich bei jedem Online-Kontakt von selbst, in den letzten vier Tagen erinnert dich der Hinweis daran. Läuft sie ab, kannst du weiter lesen und exportieren, nur nicht mehr bearbeiten, bis das Gerät einmal online war. Was du geschrieben hast, bleibt dabei auf dem Gerät. Die Frist ist vom Server signiert, sie lässt sich weder im Speicher verlängern noch durch eine zurückgestellte Uhr.

## Was du wissen solltest

- **Browserdaten löschen löscht auch die Kopie.** Solange **Änderungen warten aufs Hochladen** zu sehen ist, lösche keine Website-Daten. Danach liegt alles auf dem Server.
- **Abmelden räumt auf.** Die Kopien und alles, was noch wartet, werden vom Gerät gelöscht – vorher warnt dich bun.ink, wenn noch etwas offen ist. Der automatische Logout nach Inaktivität ruht offline, damit du dich nicht aussperrst.
- **Anmelden braucht eine Verbindung.** Wer abgemeldet ist, sieht offline nur einen Hinweis. Sobald das Netz zurück ist, geht es von selbst zur Anmeldung.

Was genau auf dem Gerät liegt, beschreibt die [Datenschutzerklärung](/privacy) im Abschnitt «Offline-Kopien auf Ihrem Gerät».

## Mehr dazu

Schritt für Schritt, mit allen Sonderfällen, steht es im [Handbuch im Kapitel «Ohne Internet schreiben»](https://github.com/VisionX-Development/writing-with-bunink/blob/main/de/12-ohne-internet-schreiben.md). Wie bun.ink High-Privacy-Bereiche verschlüsselt und deine Texte sonst schützt, beschreibt der Artikel [Wie bun.ink deine Texte schützt](/blog/how-bun-ink-protects-your-texts). Wie du bun.ink am Handy nutzt, steht in [bun.ink auf dem Mobilgerät nutzen](/blog/using-bun-ink-on-mobile).
