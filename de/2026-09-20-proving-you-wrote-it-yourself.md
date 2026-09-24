```
title: Deine Arbeit belegen – was das KI-Wasserzeichen nicht verrät
date: 2026-09-20
description: Seit diesem Sommer tragen KI-erzeugte Texte ein unsichtbares Wasserzeichen – auch dann, wenn nur die Rechtschreibhilfe darübergelaufen ist. Warum daraus falsche Vorwürfe entstehen – und warum deine Commit-Historie kein Beweis ist, aber ein Beleg, den nur du erklären kannst.
```

Vor einer Weile haben wir hier beschrieben, wie sich eine KI als  
[kontrollierter Schreibpartner](/blog/ai-controlled-writing-partner) einsetzen lässt: mit klaren  
Regeln und einem Agenten, der prüft und vorschlägt, während der Mensch entscheidet.

Hier geht es um eine Frage, die sich unabhängig davon stellt: Wie belegst du, dass ein Text deine  
Arbeit ist?

### Wie jemand mit KI umgeht, ist eine persönliche Entscheidung, die dieser Artikel niemandem abnimmt.

Grob und vollkommen wertfrei, kann man die Mehrzahl der Autoren in drei Gruppen einteilen. Die erste Gruppe von Autoren verwendet überhaupt keine KI. Die zweite Gruppe von Autoren verwendet KI um ganze Szenen, d.h. vollständige Textpassagen bis hin zu ganzen Kapiteln und sogar Bücher zu erstellen. Die dritte Gruppe liegt irgendwo dazwischen, sie schreiben zwar jeden Satz selber, verwenden KI-Tools aber z.B. für eine Rechtschreibprüfung oder Stilanalyse usw.

Für die Frage nach dem Beleg eigener Arbeit spielt keine der Wege wirklich eine Rolle. Die Antwort liegt nicht im fertigen Text selber, sondern eher in seiner Entstehung – und genau das ist der Punkt an dem Versionierung eines Textes von Vorteil sein kann.

### Das neue Problem: den Negativbeweis führen

Wer einen Text abliefert, muss zunehmend belegen können, was vor kurzem niemand belegen  
musste: dass er ihn selbst und nicht eine KI geschrieben hat. Verlage lassen sich das versichern, Redaktionen nehmen  
entsprechende Klauseln in Verträge auf. Die Werkzeuge, mit denen dabei geprüft wird, taugen wenig:  
KI-Detektoren raten anhand von Oberflächenmerkmalen und liegen regelmässig falsch – auch bei  
Menschen, die einfach nur sauber schreiben.

Das Kernproblem: Ob eine KI oder ein Mensch einen Text verfasst hat, sieht man ihm zunehmend nicht mehr an. Ein fertiger Text ist ein  
Ergebnis, und Ergebnisse sehen sich ähnlich, egal wie sie entstanden sind. Der Unterschied liegt in  
dem Weg wie der Text entsteht – doch die Dokumentation dazu ist normalerweise verschwunden, sobald die Datei gespeichert ist.  
Maschinell erzeugter Text trägt inzwischen zwar eine Markierung; sie beantwortet aber ausgerechnet  
diese Frage nicht – gleich mehr dazu.

### Die dritte Gruppe: eigener Text, fremde Werkzeuge

Über eine der drei Haltungen vom Anfang wird am wenigsten gesprochen, obwohl sie vermutlich die  
häufigste ist: Menschen, die jeden Satz selbst schreiben, aber eine Rechtschreib- oder  
Grammatikprüfung oder gar ein Stilanalyse- Tool benutzen.

Dass solche Werkzeuge unter der Haube längst Sprachmodelle einsetzen, sieht man ihnen nicht sofort an. Wer  
eine Grammatikkorrektur annimmt, hat nicht das Gefühl, mit einer KI zu schreiben. Trotzdem ist an einer Stelle eine Maschine über den Text gelaufen. Genau daraus ist seit diesem Sommer ein Problem geworden.

### Das Wasserzeichen ist keine Zukunftsmusik

Auf Grund einer verschärften EU- Vorschrift versehen die grossen KI- Anbieter seit Sommer 2026 ihre Modelle mit einem unsichtbaren Wasserzeichen im erzeugten Text. Bei Anthropic z.B. tragen es einzelne Modelle bereits ab August 2026, bis Anfang Dezember 2026 sollen es alle Modelle haben. Abschalten lässt es sich nicht. Da hinter diesen Änderungen die Transparenzpflichten des europäischen KI-Rechts stehen, werden andere Anbieter ähnliche Wege gehen müssen.

Entscheidend ist, wo diese Markierung auftaucht: **Jedes Werkzeug, das im Hintergrund ein solches**  
**Modell benutzt, hinterlässt sie** – auch die Rechtschreibhilfe. Und sie ist zäh: Sie steckt nicht in  
einer Datei-Eigenschaft, sondern in der Wortwahl selbst. Sie übersteht Kopieren, Einfügen,  
Umformatieren – und verschwindet erst, wenn die Stelle vollständig neu geschrieben wird.

### Was ein Wasserzeichen aussagt – und was nicht

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
Ergebnis. **Dein Beleg ist NUR der Weg dorthin.**

Den Stand zum Wasserzeichen erklärt Anthropic in seiner  
[Hilfe zur Kennzeichnung KI-erzeugter Inhalte](https://support.claude.com/en/articles/16266773-how-claude-marks-ai-generated-content).

### Was in einer Versionierung ausser dem Text noch steht

Genau hier tut die Versionierung etwas, das sie eigentlich für ganz andere Zwecke tut. Wenn du in  
bun.ink arbeitest, speicherst du keine Datei, die sich selbst überschreibt, sondern legst  
Speicherpunkte an – Commits, die festhalten, wie der Text aussah, wann das war und was du notiert  
hast. Was Commits, Branches und Repository bedeuten, erklärt der Blogartikel:  
[Git und GitHub einfach erklärt](/blog/git-and-github-for-writers).

Dadurch entsteht neben deinem Text eine Geschichte, die niemand bewusst aufschreibt: seine  
Entstehungsgeschichte. Wann der erste Absatz da war, welcher Satz drei Wochen lang unverändert  
stand, wo du eine Szene verworfen und später anders wieder aufgenommen hast. Diese zweite Ebene ist dein Beleg – sie entsteht nebenbei, während du ganz normal arbeitest. Es entsteht eine Zeitleiste die bezeugt wann welcher Satz entstanden ist.

Im Writer kannst du diese Historie auch lesen. Im Changes-Tab gibt es den **Commit-Browser**: eine  
Liste aller Speicherpunkte, jeder mit Zeitstempel und Nachricht für jede Branch. Du wählst zwei Stände – etwa den  
ersten Commit und den von heute – und siehst dazwischen jede Änderung hervorgehoben. Ausführlich  
beschrieben in [Der Commit-Browser](/blog/browsing-your-commit-history).

Wenn dich also jemand fragt, ob Kapitel 7 wirklich von dir ist, kannst du die vierzig Speicherpunkte zeigen, aus denen es entstanden ist – und zu jedem erzählen, was du warum gemacht hast.

### Warum Mikroschritte überzeugender sind als ein fertiges Kapitel

Das eigentliche Indiz liegt nicht in einem einzelnen Commit, sondern in der **Form** der Historie.  
Menschliches Schreiben ist krumm: Ein Absatz wächst über eine Woche in sieben Schritten, ein anderer  
entsteht in zwanzig Minuten und wird am nächsten Tag halbiert. Es gibt Tage mit vierhundert Wörtern  
und Tage mit vierzig, Sätze, die dreimal umgestellt werden, Streichungen, Pausen, Rückkehr.

Genau das steht in einer gewachsenen Commit-Historie – und genau das fehlt, wenn ein Kapitel in einem einzigen Schritt auftaucht: vollständig, ohne eine einzige Überarbeitung danach. Das beweist noch nichts; vielleicht hast du das Kapitel anderswo geschrieben und nur eingefügt. Aber es gibt dir dann auch nichts in die Hand, wenn jemand fragt.

Je kleiner du speicherst, desto dichter wird diese Spur. Und es ist kein zusätzlicher Zusatzaufwand – es ist ohnehin die vorgesehene Arbeitsweise mit Versionskontrolle in bun.ink. Aus «Ich habe das selbst geschrieben» wird dadurch sehr leicht: «Hier sind die 312 Schritte, mit Datum und Kommentar – frag mich zu jedem, was ich da gemacht habe».

### Der naheliegende Einwand: Kann eine KI das nicht auch?

Doch, kann sie. Ein Agent kann einen fertigen Text in vierzig Schritte zerlegen, Umwege und Streichungen einbauen, glaubwürdige Commit-Nachrichten schreiben und das Ganze über Wochen verteilt speichern. Er kann sich sogar selbst kommentieren – unter einem zweiten Account, der aussieht wie eine Lektor oder Überarbeiter. Eine Historie ist deshalb kein Echtheitszertifikat, und wer das Gegenteil verspricht, verspricht etwas, das es nicht gibt: Kein Artefakt beweist lückenlos, dass es ein Mensch war der das geschrieben hat.

Was die Historie trotzdem leistet, ist etwas anderes. Sie verändert die Sachlage von «Klingt nach KI», eine Vermutung die nichts kostet zu «Du hast deine Arbeitsspur über Monate gefälscht», ein manifester Täuschungsvorwurf der teuer werden könnte da er selber belegt werden muss.

Vor allem aber ist deine Historie etwas, das du erzählen kannst. Warum die Rückblende rausflog, was vorher an dieser Stelle stand, warum Kapitel 3 zwei Wochen ruhte: Wer das erlebt hat, kann darüber sprechen, zu jedem beliebigen Commit, ohne Vorbereitung. Eine mit KI erzeugte Spur ist ein Drehbuch, das man erst auswendig lernen müsste.

Am meisten zählt, was ausserhalb deiner Historie bestätigt wird – von Menschen, nicht von Accounts. Ein Reviewer-Profil ist in einer Minute angelegt; eine Lektorin mit Namen, Ruf und Verlag, die sich an den Zwischenstand vom April erinnert, nicht. Am stärksten ist, wer zu der Seite gehört, die später zweifelt: Hat die Lektorin des Verlags Kapitel 3 selbst kommentiert, kann der Verlag seine eigenen Leute fragen.

### Vorher und nachher: was die Historie über das Werkzeug verrät

Für die dritte Gruppe wird das sehr konkret. Deine Historie enthält den Absatz, **bevor** das  
Werkzeug ihn angefasst hat: Der Commit vom Dienstagabend zeigt deine Fassung, der vom Mittwochmorgen  
zeigt, was die Korrektur daraus gemacht hat. Dazwischen liegt ein Vergleich, den jeder lesen kann –  
ein Komma, zwei umgestellte Wörter.

Damit verschiebt sich die Frage von «Ist da Maschine drin?» zu «Was genau hat sie getan?». Du  
beweist nicht, dass nie ein Werkzeug im Spiel war – das kannst du seit diesem Sommer ohnehin nicht  
mehr. Du belegst Urheberschaft: dass der Text von dir stammt und das Werkzeug ihn an den Rändern  
berührt hat, nicht in der Substanz.

Praktisch heisst das: **ein Commit vor dem Werkzeug, ein Commit danach.** Zehn Sekunden Aufwand –  
und die Grenze zwischen deiner Arbeit und der Korrektur ist dauerhaft dokumentiert. Weil sich die  
Markierung nicht herauswaschen lässt und du sie selbst nicht prüfen kannst, ist deine Historie der einzige Beleg, den du selbst in der Hand hast.

### Und die Sicherheit deiner Texte?

Eine Frage vom Anfang ist offengeblieben: *Landet mein Manuskript irgendwo in einem Daten-Training?* Bei  
bun.ink ist die Antwort kurz. Die App schickt deine Texte nicht an ein Sprachmodell, und in der  
Datenbank liegen sie nicht als lesbarer Klartext, sondern verschlüsselt. Wie das im Detail  
funktioniert, steht in [Wie bun.ink deine Texte schützt](/blog/how-bun-ink-protects-your-texts).

Dein Text geht also nirgends hin – weder in ein Training noch als Klartext in eine Datenbank. Mit einem High-Privacy-Projekt kannst du deine Texte sogar noch weiter Schützen, wie das funktioniert ist auch in dem oben genannten Blog- Artikel erklärt. Allerdings musst du dir darüber im klaren sein, dass es für High-Privacy-Projekte keine GitHub- Verknüpfung gibt und damit auch die Vorteile der git Versionskontrolle die in diesem Artikel besprochen wurden, wegfallen. 

### Nochmal in Kürze: 

Was du also für den Beleg deiner eigenständigen Arbeit mit der Hilfe von Versionskontrolle tun solltest:

- **Früh anfangen.** Die Historie beginnt mit dem ersten Commit, nicht erst beim fertigen Manuskript.
- **Klein speichern.** Lieber fünf Commits an einem Nachmittag als einen am Monatsende.
- **Ehrliche Nachrichten schreiben.** «Dialog gekürzt, Rückblende raus» sagt mehr als «Update».
- **Umwege stehen lassen.** Verworfene Fassungen sind kein Makel, sie sind der Beleg.
- **Werkzeuge einrahmen.** Vor und nach jedem Durchlauf durch eine Korrekturhilfe einmal speichern.
- **Den Agenten getrennt halten.** Grössere KI-Arbeit gehört auf einen eigenen Branch und unter das  
eigene Konto des Agenten – so bleibt auch für dich selbst sichtbar, was von dir stammt und was vom Agenten.
- **Überarbeitungen auch im Alleingang.** Was du verworfen hast, bleibt so mitsamt Begründung  
dokumentiert – wie das geht, steht in [Das Lektorat kommt zum Text](/blog/reviews-as-pull-requests).
- **Andere Menschen einbeziehen.** Nicht irgendein Account, sondern Menschen, die man fragen kann: eine Lektorin, ein Redakteur, jemand vom Verlag. Ein Review, in dem eine erreichbare Person einen Zwischenstand kommentiert hat, wiegt mehr als hundert Commits – am meisten, wenn diese Person zu der Seite gehört, die später Fragen stellt.
