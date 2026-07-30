---
title: Der Entwicklungsrechner wird eingerichtet
band: Band I – Unternehmen und Kommunikation
chapter: 003
level: C1+
setting: Erster Arbeitstag – Vormittag
participants:
  - Lukas Weber (Embedded-AI Engineer)
  - Tobias Klein (Embedded Software Engineer)
field:
  - Embedded AI
  - Linux
  - Git
  - Embedded Systems
  - Softwareentwicklung
---

# Der Entwicklungsrechner wird eingerichtet

## Situation

Nach der Vorstellungsrunde gehen Lukas und Tobias in einen kleineren Entwicklungsraum. Dort stehen mehrere leistungsstarke Linux-Workstations sowie verschiedene Embedded-Boards, Messgeräte und Prototypen.

Während Tobias den neuen Rechner vorbereitet, unterhalten sich beide über die Arbeitsweise des Teams, die Entwicklungsumgebung und die ersten Schritte im Projekt.

---

# Dialog

**Tobias**

So, das hier wird in den nächsten Monaten dein Arbeitsplatz sein.

Der Rechner ist bereits vorbereitet, wir müssen nur noch dein Benutzerkonto einrichten und die letzten Zugänge freischalten.

---

**Lukas**

Sieht nach einer ziemlich leistungsfähigen Maschine aus.

---

**Tobias**

Ja, die brauchen wir auch.

Einige Kollegen trainieren neuronale Netze lokal, andere kompilieren FPGA-Bitstreams oder führen umfangreiche Simulationen durch.

Da kommt selbst aktuelle Hardware gelegentlich ins Schwitzen.

---

**Lukas**

Ich kenne das.

Man wartet zwanzig Minuten auf einen Build und stellt anschließend fest, dass irgendwo nur ein Semikolon fehlt.

---

**Tobias**

*(lacht)*

Willkommen im Alltag eines Softwareentwicklers.

Manchmal verbringt man länger mit der Fehlersuche als mit dem eigentlichen Programmieren.

---

**Lukas**

Das beruhigt mich fast.

Ich hatte schon befürchtet, das läge nur an mir.

---

**Tobias**

Ganz bestimmt nicht.

Wenn dir irgendwann jemand erzählt, bei ihm funktioniere jedes Programm auf Anhieb, dann solltest du misstrauisch werden.

---

**Lukas**

Das merke ich mir.

---

*Tobias meldet sich am Administrationsportal an.*

---

**Tobias**

Zunächst richten wir dein Firmenkonto ein.

Darüber authentifizierst du dich später praktisch überall.

E-Mail, GitLab, Wiki, Jira, VPN, Build-Server ...

Im Idealfall musst du dir nur ein einziges Passwort merken.

---

**Lukas**

GitLab also?

Kein GitHub?

---

**Tobias**

Für Open-Source-Projekte verwenden wir durchaus GitHub.

Unsere interne Entwicklung läuft allerdings vollständig über GitLab.

Das erleichtert uns die Rechteverwaltung und die Integration in unsere CI-Pipeline.

---

**Lukas**

Verstehe.

Habt ihr viele Open-Source-Projekte?

---

**Tobias**

Ein paar.

Wir versuchen grundsätzlich, alles zu veröffentlichen, was keine vertraulichen Kundeninformationen enthält.

Davon profitiert letztlich jeder.

Außerdem verbessert sich dadurch häufig auch die Qualität unseres Codes.

---

**Lukas**

Interessant.

Viele Unternehmen verfolgen eher die umgekehrte Strategie und behandeln selbst allgemeine Bibliotheken wie Staatsgeheimnisse.

---

**Tobias**

Ja ...

Das erleben wir leider auch.

Dabei vergessen viele, dass Open Source nicht bedeutet, sämtliche Geschäftsgeheimnisse preiszugeben.

Man muss lediglich sauber zwischen allgemeiner Technologie und kundenspezifischen Entwicklungen unterscheiden.

---

*Tobias öffnet ein Terminal.*

---

**Tobias**

Arbeitest du normalerweise unter Linux?

---

**Lukas**

Fast ausschließlich.

Ich benutze Ubuntu seit vielen Jahren.

Nur einige FPGA-Werkzeuge zwingen mich gelegentlich noch zu Windows.

---

**Tobias**

Dann wirst du dich hier schnell zurechtfinden.

Fast alle unsere Entwicklungsrechner laufen unter Linux.

Unsere Build-Server sowieso.

---

**Lukas**

Hat das historische Gründe oder ist das eine bewusste Entscheidung?

---

**Tobias**

Beides.

Vor vielen Jahren war Linux einfach die unkomplizierteste Plattform für Embedded-Entwicklung.

Heute sprechen zusätzlich viele praktische Gründe dafür.

Unsere Toolchains lassen sich leichter automatisieren, Skripte laufen zuverlässig und die Entwicklungsumgebungen verhalten sich auf allen Rechnern nahezu identisch.

---

**Lukas**

Das reduziert vermutlich auch die Zahl der schwer reproduzierbaren Fehler.

---

**Tobias**

Genau.

Nichts ist frustrierender als der Satz:

*"Bei mir funktioniert es."*

---

**Lukas**

*(lacht)*

Den habe ich tatsächlich schon erstaunlich oft gehört.

---

**Tobias**

Deshalb versuchen wir, möglichst reproduzierbare Entwicklungsumgebungen bereitzustellen.

Ein neuer Kollege soll im Idealfall innerhalb weniger Stunden produktiv werden können.

---

**Lukas**

Das klingt nach einer Menge Vorarbeit.

---

**Tobias**

Ist es auch.

Aber dieser Aufwand zahlt sich langfristig aus.

Wenn jeder seinen Rechner anders konfiguriert, verliert das gesamte Team unnötig Zeit.

---

*Tobias tippt einige Befehle in das Terminal.*

---

**Tobias**

So.

Jetzt klonen wir zunächst unsere wichtigsten Repositories.

Keine Sorge, du musst heute noch nicht verstehen, wie alle Projekte zusammenhängen.

Am Anfang wirkt unsere Architektur auf fast jeden etwas überwältigend.

---

**Lukas**

Das überrascht mich nicht.

Je größer ein Projekt wird, desto schwieriger wird es, den Überblick zu behalten.

---

**Tobias**

Absolut.

Deshalb versuchen wir, neue Kolleginnen und Kollegen nicht mit Informationen zu überladen.

Niemand erwartet, dass du nach zwei Tagen sämtliche Komponenten kennst.

---

**Lukas**

Das finde ich ehrlich gesagt sehr angenehm.

Ich habe auch schon erlebt, dass neue Mitarbeiter am ersten Tag Dokumentationen mit mehreren tausend Seiten bekommen haben.

---

**Tobias**

*(lacht)*

Ja ...

Nach dem Motto:

*"Hier sind unsere Unterlagen. Viel Erfolg."*

---

**Lukas**

Genau.

Und zwei Wochen später fragt man sich, warum der Neue immer noch kaum Fragen stellt.

---

**Tobias**

Dabei ist das meistens ein schlechtes Zeichen.

Wenn jemand gar nichts fragt, bedeutet das oft nicht, dass er alles verstanden hat.

Sondern eher das Gegenteil.

---

**Lukas**

Da stimme ich dir vollkommen zu.

Ich finde es ohnehin sinnvoller, früh nachzufragen, als später falsche Annahmen zu treffen.

---

**Tobias**

Das sehen wir genauso.

Wir diskutieren hier lieber zehn Minuten länger, bevor wir zwei Wochen in die falsche Richtung entwickeln.

---

*Tobias öffnet GitLab und zeigt Lukas die Projektübersicht.*

---

**Tobias**

Lass dich von der Anzahl der Projekte nicht abschrecken.

Viele davon sind Bibliotheken oder interne Werkzeuge.

Für deinen Einstieg werden wir uns zunächst nur mit drei Repositories beschäftigen.

---

**Lukas**

Das klingt überschaubar.

Wie organisiert ihr eure Entwicklung?

Ein großes Monorepository oder mehrere voneinander getrennte Projekte?

---

**Tobias**

Mehrere Repositories.

Früher hatten wir tatsächlich über ein Monorepo nachgedacht.

Inzwischen hat sich jedoch gezeigt, dass unsere Teams mit einer modularen Struktur deutlich besser arbeiten können.

Außerdem lassen sich einzelne Komponenten unabhängig voneinander versionieren.

---

**Lukas**

Das erleichtert wahrscheinlich auch die Wiederverwendung in anderen Projekten.

---

**Tobias**

Ganz genau.

Wir versuchen grundsätzlich, Funktionalität möglichst generisch zu entwickeln.

Wenn wir ein Problem bereits einmal sauber gelöst haben, möchten wir dieselbe Lösung nicht beim nächsten Projekt erneut implementieren müssen.

---

*Tobias lehnt sich kurz zurück und schaut auf den Bildschirm.*

---

**Tobias**

Gut.

Die ersten Downloads laufen.

Das dauert jetzt ein paar Minuten.

Perfekter Zeitpunkt für eine wichtige Regel bei uns.

---

**Lukas**

Jetzt bin ich gespannt.

---

**Tobias**

Bei uns committet niemand direkt auf den *main*-Branch.

Auch ich nicht.

Und Dr. Fischer übrigens ebenfalls nicht.

---

**Lukas**

Das finde ich ehrlich gesagt beruhigend.

---

**Tobias**

Warum?

---

**Lukas**

Weil es zeigt, dass Regeln für alle gelten.

Ich habe schon erlebt, dass Teamleiter Sonderrechte hatten und Änderungen direkt in den Hauptzweig geschrieben haben.

Das führte früher oder später fast immer zu Problemen.

---

**Tobias**

Genau deshalb machen wir das nicht.

Jede Änderung beginnt mit einem eigenen Feature-Branch.

Anschließend wird ein Merge Request erstellt.

Mindestens eine weitere Person schaut sich den Code an.

Erst danach wird zusammengeführt.

---

**Lukas**

Und wenn es sich nur um eine Kleinigkeit handelt?

Ein Tippfehler beispielsweise?

---

**Tobias**

Gerade dann.

Ein Merge Request dauert meistens nur wenige Minuten.

Aber diese wenigen Minuten verhindern manchmal stundenlange Fehlersuche.

---

**Lukas**

Wie ausführlich fallen eure Code-Reviews normalerweise aus?

---

**Tobias**

Das hängt vom Projekt ab.

Bei sicherheitskritischen Komponenten prüfen wir praktisch jede einzelne Änderung.

Bei internen Werkzeugen genügt oft ein etwas pragmatischerer Blick.

Uns geht es nicht darum, Fehler zu suchen.

Ein gutes Code-Review ist eine gemeinsame Diskussion darüber, wie man den Code verständlicher, robuster und langfristig wartbarer machen kann.

---

**Lukas**

Das gefällt mir.

Viele Entwickler empfinden Code-Reviews leider immer noch als persönliche Kritik.

---

**Tobias**

Ja.

Dabei sollte niemand seinen Quellcode mit seiner Persönlichkeit verwechseln.

Wir diskutieren den Code.

Nicht den Menschen.

---

**Lukas**

Das ist wahrscheinlich leichter gesagt als getan.

---

**Tobias**

Natürlich.

Jeder steckt viel Arbeit in seine Lösungen.

Aber irgendwann erkennt man, dass fast jede Idee noch verbessert werden kann.

Ich selbst lerne in Code-Reviews wahrscheinlich mehr als beim eigentlichen Programmieren.

---

**Lukas**

Interessanter Gedanke.

---

**Tobias**

Außerdem verteilt sich Wissen dadurch automatisch im Team.

Wenn immer nur dieselbe Person ein bestimmtes Modul kennt, entsteht irgendwann ein Engpass.

---

**Lukas**

Der berühmte *Single Point of Failure*.

---

**Tobias**

Ganz genau.

Nur eben nicht bei der Hardware, sondern beim Wissen.

---

*Währenddessen erscheinen die ersten Repositorys im Dateisystem.*

---

**Tobias**

Perfekt.

Dann sehen wir uns kurz die Projektstruktur an.

Keine Sorge, wir gehen heute nicht jedes Verzeichnis einzeln durch.

Das wäre selbst für mich zu viel.

---

**Lukas**

Dafür bin ich dir ausgesprochen dankbar.

---

**Tobias**

Hier liegen unsere Bibliotheken.

Dort befinden sich die eigentlichen Anwendungen.

Und dieses Repository enthält ausschließlich gemeinsame Werkzeuge, Build-Skripte und Hilfsprogramme.

---

**Lukas**

Das wirkt überraschend aufgeräumt.

---

**Tobias**

Diesen Eindruck versuchen wir zumindest aufrechtzuerhalten.

Die Realität sieht manchmal etwas chaotischer aus.

Softwareprojekte haben leider die unangenehme Eigenschaft, mit der Zeit immer weiter zu wachsen.

---

**Lukas**

Wie verhindert ihr, dass die Architektur irgendwann unübersichtlich wird?

---

**Tobias**

Gar nicht vollständig.

Aber wir versuchen gegenzusteuern.

In regelmäßigen Abständen nehmen wir uns bewusst Zeit, um bestehende Komponenten zu überarbeiten.

Nicht weil der Kunde das verlangt.

Sondern weil wir selbst auch in zwei Jahren noch verstehen möchten, was wir heute entwickelt haben.

---

**Lukas**

Das klingt nach einer gesunden Einstellung.

Refactoring wird im Projektalltag leider häufig verschoben.

---

**Tobias**

Leider.

Refactoring verkauft sich beim Kunden nicht besonders gut.

Ein stabiles Produkt dagegen schon.

Und meistens hängt beides enger zusammen, als man zunächst denkt.

---

*Tobias öffnet nun das Terminal.*

---

**Tobias**

Dann wagen wir jetzt den ersten Build.

Mal sehen, ob der berühmte Vorführeffekt heute zuschlägt.

---

**Lukas**

Du meinst ...

Alles funktioniert genau so lange, bis jemand zusieht?

---

**Tobias**

Exakt.

Entwickler sind manchmal erstaunlich abergläubisch.

---

*Der Build startet.*

Mehrere tausend Zeilen laufen über den Bildschirm.

---

**Lukas**

Beeindruckend.

Wie lange dauert ein vollständiger Build normalerweise?

---

**Tobias**

Auf diesem Rechner vielleicht sechs oder sieben Minuten.

Unser CI-Server benötigt etwas länger, dafür testet er deutlich mehr Konfigurationen.

---

**Lukas**

Lässt ihr automatisch testen?

---

**Tobias**

Natürlich.

Jeder Merge Request startet automatisch verschiedene Pipelines.

Unit-Tests.

Statische Codeanalyse.

Formatprüfung.

Compiler-Warnungen.

Abhängig vom Projekt kommen manchmal noch Hardware-in-the-Loop-Tests hinzu.

---

**Lukas**

Dann dürfte eigentlich kaum noch etwas Ungeprüftes im Repository landen.

---

**Tobias**

Zumindest ist das unser Anspruch.

Absolute Fehlerfreiheit gibt es nicht.

Aber man kann die Wahrscheinlichkeit deutlich reduzieren.

---

*Plötzlich erscheint eine gelbe Warnung.*

---

**Lukas**

Oh ...

Da ist gerade eine Warnung aufgetaucht.

---

**Tobias**

Keine Panik.

Die kenne ich bereits.

Sie stammt von einer externen Bibliothek.

Genau deshalb unterscheiden wir übrigens zwischen Warnungen, die wir beeinflussen können, und solchen, die außerhalb unseres Verantwortungsbereichs liegen.

---

**Lukas**

Das ergibt Sinn.

Sonst würde man irgendwann alle Warnungen einfach ignorieren.

---

**Tobias**

Und genau das wäre gefährlich.

Warnungen verlieren ihren Wert, wenn ständig dieselben irrelevanten Meldungen auftauchen.

---

*Der Build endet erfolgreich.*

---

**Tobias**

Geschafft.

Herzlichen Glückwunsch.

Dein erster Build bei NovaTech war erfolgreich.

---

**Lukas**

Das ging erstaunlich reibungslos.

Ich hatte innerlich schon mit deutlich mehr Schwierigkeiten gerechnet.

---

**Tobias**

Keine Sorge.

Die kommen früh genug.

*(beide lachen)*

---

**Lukas**

Darf ich dir eine Frage stellen?

---

**Tobias**

Natürlich.

---

**Lukas**

Was gefällt dir persönlich am meisten an deiner Arbeit?

Nicht an der Firma.

Sondern am Beruf selbst.

---

*Tobias überlegt einen Moment.*

---

**Tobias**

Wahrscheinlich die Tatsache, dass man ständig dazulernt.

Kaum hat man das Gefühl, ein Thema wirklich verstanden zu haben, taucht schon das nächste auf.

Neue Prozessoren.

Neue Programmiersprachen.

Neue Werkzeuge.

Neue Algorithmen.

Man bleibt eigentlich sein ganzes Berufsleben lang Student.

---

**Lukas**

Genau das hat mich an der Elektrotechnik schon immer fasziniert.

Es gibt nie den Punkt, an dem man sagen könnte:

*"Jetzt weiß ich alles."*

---

**Tobias**

Und ehrlich gesagt wäre das auch ziemlich langweilig.

---

*In diesem Moment erscheint Dr. Fischer an der Tür.*

---

**Dr. Fischer**

Na?

Hat der Rechner den ersten Tag überlebt?

---

**Tobias**

Gerade eben.

Und Lukas hat seinen ersten erfolgreichen Build hinter sich.

---

**Dr. Fischer**

Sehr schön.

Dann machen wir jetzt Mittagspause.

Am Nachmittag schauen wir uns das eigentliche Projekt an.

Und keine Sorge ...

Ab morgen wird es langsam ernst.

---

**Lukas**

Ich freue mich darauf.

---

# Fachwortschatz

| Ausdruck | Bedeutung |
|-----------|-----------|
| etwas nachvollziehen | einen Gedankengang oder Ablauf verstehen |
| etwas freigeben | offiziell genehmigen oder zur Nutzung bereitstellen |
| sich abstimmen | gemeinsam Entscheidungen koordinieren |
| der Engpass | limitierender Faktor innerhalb eines Prozesses |
| langfristig wartbar | so entwickelt, dass spätere Änderungen leicht möglich sind |
| gegensteuern | bewusst Maßnahmen ergreifen, um eine negative Entwicklung zu verhindern |
| der Vorführeffekt | etwas funktioniert genau dann nicht mehr, wenn andere zuschauen |
| reibungslos | ohne Schwierigkeiten oder Unterbrechungen |
| der Verantwortungsbereich | Bereich, für den jemand zuständig ist |
| der Anspruch | der eigene Qualitätsmaßstab oder das angestrebte Niveau |
| sich Zeit für etwas nehmen | bewusst Zeit investieren |
| etwas beeinflussen können | auf etwas aktiv einwirken können |
| etwas verschieben | auf einen späteren Zeitpunkt verlegen |
| sich bewähren | sich in der Praxis als gut oder zuverlässig erweisen |

---

# Redemittel

- Das finde ich ehrlich gesagt beruhigend.
- Das ergibt Sinn.
- Darüber lohnt es sich nachzudenken.
- Unser Anspruch ist ...
- Wir versuchen gegenzusteuern.
- Das sehe ich genauso.
- Genau darauf legen wir großen Wert.
- Das zahlt sich langfristig aus.
- Das wirkt auf den ersten Blick ...
- Man sollte dabei nicht vergessen, dass ...

---

# Andere Formulierungen

### Statt

> Das ergibt Sinn.

kann man auch sagen

- Das leuchtet mir ein.
- Das erscheint mir nachvollziehbar.
- Das ist durchaus plausibel.
- Das überzeugt mich.
- Das kann ich gut nachvollziehen.
- Das ist ein schlüssiger Ansatz.

---

### Statt

> Das gefällt mir.

kann man auch sagen

- Das spricht mich an.
- Das finde ich überzeugend.
- Mit dieser Vorgehensweise kann ich mich gut identifizieren.
- Diese Herangehensweise sagt mir zu.
- Das halte ich für sinnvoll.

---

### Statt

> Keine Sorge.

kann man auch sagen

- Mach dir darüber keinen Kopf.
- Das bekommen wir hin.
- Das wird schon.
- Das kriegen wir gemeinsam hin.
- Darüber musst du dir wirklich keine Gedanken machen.
- Das ist halb so schlimm.

---

### Statt

> Das zahlt sich langfristig aus.

kann man auch sagen

- Langfristig lohnt sich dieser Aufwand.
- Auf Dauer spart uns das viel Arbeit.
- Davon profitieren wir später erheblich.
- Mittelfristig macht sich das bezahlt.
- Der zusätzliche Aufwand rechnet sich langfristig.

---

### Statt

> Genau darauf legen wir großen Wert.

kann man auch sagen

- Das hat bei uns hohe Priorität.
- Darauf achten wir besonders.
- Das ist ein zentraler Bestandteil unserer Arbeitsweise.
- Das ist uns ausgesprochen wichtig.
- Das gehört zu unserer Unternehmenskultur.

---

# Grammatik im Kontext

## Nominalstil und Verbalstil

Im Berufsalltag werden häufig Nominalisierungen verwendet:

> **Die Freigabe erfolgt nach erfolgreicher Prüfung.**

Im Gespräch klingt die verbale Variante jedoch oft natürlicher:

> **Wir geben den Code frei, sobald wir ihn geprüft haben.**

Professionelle Sprecher wechseln je nach Situation bewusst zwischen beiden Stilen.

---

# Kulturelle Hinweise

In vielen deutschen Entwicklungsabteilungen gelten **Code Reviews** nicht als Kontrolle, sondern als Instrument des gemeinsamen Lernens. Kritik wird idealerweise sachlich formuliert und bezieht sich auf den Code, nicht auf die Person.

Außerdem wird langfristige Wartbarkeit oft genauso hoch bewertet wie kurzfristige Funktionalität. Zeit für Refactoring oder technische Verbesserungen einzuplanen, gilt in vielen erfahrenen Teams als Investition in die Zukunft und nicht als Zeitverlust.

---

# Zusammenfassung

Lukas richtet gemeinsam mit Tobias seine Entwicklungsumgebung ein und erhält einen ersten Einblick in die technischen Arbeitsabläufe bei NovaTech Systems. Neben Git-Workflows, Build-Prozessen und Code Reviews wird deutlich, welche Werte das Team prägen: Zusammenarbeit, Wissensaustausch, Qualität und nachhaltige Softwareentwicklung.

---

## Ausblick

**Kapitel 004 – Die erste Kaffeepause**

Beim gemeinsamen Kaffee lernt Lukas seine Kolleginnen und Kollegen auf einer persönlicheren Ebene kennen. Zwischen lockeren Gesprächen über Hobbys, frühere Projekte und kuriose Fehlersuchen erfährt er mehr über die Unternehmenskultur und die Menschen hinter den technischen Rollen.
