# Escape-Spiel „Der Sinussatz“ – Klasse 10

## Designentscheidungen (Zusammenfassung)

| Frage | Entscheidung |
|---|---|
| Fach / Thema | Mathematik, Sinussatz |
| Lernziele | Anwenden, Entscheiden, Beurteilen |
| Denkoperationen | Strukturieren, begründet auswählen |
| Interaktionsform | Escape-Spiel |
| Differenzierung | Steigende Schwierigkeit von Raum zu Raum |
| Rückmeldung | Hinweisgebend (Denkanstöße statt Lösungen) |
| Umfang | 8 Räume (ca. eine Doppelstunde) |
| Klassenstufe | 10 |

Annahme: Der Kosinussatz ist bereits bekannt, weil die Lernenden zwischen Sinus- und Kosinussatz entscheiden sollen. Falls nicht, Raum 3 und Raum 5 im Prompt entsprechend anpassen (siehe Hinweis am Ende).

---

## Optimierter Coding-Prompt

> Den folgenden Block vollständig in Claude (oder ein anderes KI-Werkzeug) kopieren.

```
Erstelle eine eigenständige, interaktive HTML-Anwendung (eine einzige Datei mit HTML, CSS und JavaScript, ohne externe Abhängigkeiten außer optional einer CDN-Schriftart) für ein digitales Escape-Spiel zum Thema „Der Sinussatz“ für Schülerinnen und Schüler der Klasse 10 eines Gymnasiums. Alle Texte auf Deutsch, Schülerinnen und Schüler werden mit „du“ angesprochen.

RAHMENHANDLUNG
Die Lernenden sind in einem alten Vermessungsamt eingeschlossen. Jeder der 8 Räume ist mit einem Zahlenschloss gesichert. Wer einen Raum löst, erhält einen Buchstaben. Die 8 Buchstaben ergeben am Ende das Lösungswort DREIECKE, mit dem sich die Ausgangstür öffnet.

DIDAKTISCHER KERN (in jedem Raum, wo sinnvoll, in genau dieser Reihenfolge)
1. Strukturieren: Die Lernenden ordnen zuerst die gegebenen Größen. Sie klicken in einer SVG-Skizze an, welche Seite welchem Winkel gegenüberliegt, oder wählen aus, welches Paar „Seite + gegenüberliegender Winkel“ vollständig bekannt ist.
2. Begründet auswählen: Danach wählen sie das Verfahren (Sinussatz / Kosinussatz / Trigonometrie im rechtwinkligen Dreieck) UND eine Begründung aus 3–4 vorgegebenen Begründungen (Multiple Choice). Erst wenn beides stimmt, wird das Rechenfeld freigeschaltet.
3. Anwenden: Ergebnis eingeben (Dezimalkomma UND Dezimalpunkt akzeptieren, Toleranz ±0,1 bei Längen bzw. ±0,2° bei Winkeln).
4. Beurteilen: In ausgewählten Räumen eine kurze Plausibilitätsfrage (z. B. „Liegt der größte Winkel der größten Seite gegenüber?“, Winkelsumme).

RÜCKMELDUNG (hinweisgebend)
- Bei falscher Eingabe NIE die Lösung zeigen, sondern einen gestuften Denkanstoß: 1. Fehlversuch → allgemeiner Hinweis, 2. Fehlversuch → konkreterer Hinweis, ab 3. Fehlversuch → Hinweis auf den nächsten Rechenschritt (aber weiterhin ohne Endergebnis).
- Hinweise beziehen sich auf typische Fehler: falsches Paar zugeordnet, Taschenrechner im Bogenmaß (RAD statt DEG), Sinussatz bei SWS/SSS angewendet, zweite Lösung im mehrdeutigen Fall übersehen.
- Bei richtiger Eingabe: kurze Bestätigung, Buchstabe erscheint mit kleiner Animation, Button „Weiter zum nächsten Raum“.

DIE 8 RÄUME (steigende Schwierigkeit; verwende genau diese Werte, Ergebnisse sind nachgerechnet)

Raum 1 – Die Paare erkennen (Buchstabe D)
Gegeben: α = 40°, β = 60°, a = 8 cm. Gesucht: b.
Strukturieren: Welches Paar ist vollständig? (a–α). Verfahren: Sinussatz, Begründung: „Ein vollständiges Paar und eine weitere Größe sind bekannt.“
Lösung: b ≈ 10,78 cm.

Raum 2 – Erst den dritten Winkel (Buchstabe R)
Gegeben: α = 35°, γ = 95°, c = 12 cm. Gesucht: a.
Strukturieren: vollständiges Paar c–γ. Verfahren: Sinussatz.
Lösung: a ≈ 6,91 cm.
Zusatz-Beurteilung: „Ist a kleiner als c? Warum muss das so sein?“ (Auswahlfrage).

Raum 3 – Die Verfahrenswahl (Buchstabe E), keine Rechnung
Zuordnungsaufgabe per Drag-and-drop: Ordne vier Dreieckskonstellationen dem passenden Verfahren zu:
WSW → Sinussatz; SWS → Kosinussatz; SSS → Kosinussatz; rechtwinkliges Dreieck mit Hypotenuse und Winkel → sin/cos/tan.
Hinweis bei Fehlern: „Prüfe, ob irgendwo ein vollständiges Paar aus Seite und gegenüberliegendem Winkel bekannt ist.“
Code: Raum öffnet sich, wenn alle vier Zuordnungen stimmen.

Raum 4 – Einen Winkel berechnen (Buchstabe I)
Gegeben: a = 7 cm, b = 5 cm, α = 70°. Gesucht: β.
Lösung: β ≈ 42,2°.
Zusatz-Beurteilung: „Warum gibt es hier nur eine Lösung für β?“ (Weil b < a, muss β < α sein; der stumpfe Winkel 137,8° scheidet aus.)

Raum 5 – Die Falle (Buchstabe E)
Gegeben: b = 6 cm, c = 9 cm, α = 50°. Gesucht: a.
Strukturieren: Es gibt KEIN vollständiges Paar. Wer „Sinussatz“ wählt, erhält den Hinweis: „Welcher Winkel liegt b gegenüber? Ist er bekannt?“ Richtiges Verfahren: Kosinussatz (SWS).
Lösung: a ≈ 6,90 cm.

Raum 6 – Peilung auf See (Buchstabe C), Sachaufgabe
Zwei Leuchttürme L₁ und L₂ stehen 12 km voneinander entfernt. Ein Schiff S wird von L₁ unter dem Winkel 48° und von L₂ unter dem Winkel 75° (jeweils gemessen zur Verbindungslinie L₁L₂) angepeilt. Wie weit ist das Schiff von L₁ entfernt?
Strukturieren: Skizze mit beschriftbaren Ecken; Winkel bei S = 57° muss zuerst bestimmt werden.
Lösung: L₁S ≈ 13,82 km.

Raum 7 – Die Flussbreite (Buchstabe K), zweistufige Sachaufgabe
Auf einer Uferseite liegen die Punkte A und B 50 m auseinander. Ein Baum C steht am gegenüberliegenden Ufer. Gemessen: Winkel bei A = 62°, Winkel bei B = 71°. Wie breit ist der Fluss (senkrechter Abstand von C zur Strecke AB)?
Schritt 1: AC mit dem Sinussatz (Lösung ≈ 64,64 m). Schritt 2: Breite = AC · sin 62° (Lösung ≈ 57,08 m; Toleranz ±0,1 m).
Beide Schritte einzeln abfragen.

Raum 8 – Der mehrdeutige Fall (Buchstabe E), Endgegner
Gegeben: a = 6 cm, b = 8 cm, α = 40°. Gesucht: β.
Zuerst Auswahlfrage: „Wie viele Dreiecke gibt es mit diesen Angaben?“ (0 / 1 / 2) → richtig: 2.
Dann beide Lösungen eingeben: β₁ ≈ 59,0° und β₂ ≈ 121,0° (Reihenfolge egal).
Hinweise: „Der Sinus hat zwischen 0° und 180° oft zwei passende Winkel.“ / „Prüfe mit der Winkelsumme, ob auch der stumpfe Winkel ein Dreieck ergibt.“
Hintergrundwerte: γ₁ ≈ 81,0°, γ₂ ≈ 19,0°.

GESTALTUNG
- Jeder Raum hat eine schlichte, maßstabsgetreu wirkende SVG-Skizze des Dreiecks; gegebene Größen farbig, gesuchte Größe mit „?“.
- Fortschrittsleiste oben mit 8 Schloss-Symbolen, die sich nacheinander öffnen, darunter die bisher gesammelten Buchstaben.
- Ruhiges, gut lesbares Design, große Schrift, hoher Kontrast, funktioniert auf Tablet und Smartphone (responsive), alle Bedienelemente auch per Tastatur erreichbar.
- Formelkarte zum Aufklappen (Sinussatz, Kosinussatz, Winkelsumme), aber ohne Lösungen.
- Kein Zeitlimit; optional eine Stoppuhr, die nur angezeigt wird.

ABSCHLUSS
- Nach Raum 8 Eingabe des Lösungsworts DREIECKE, dann Erfolgsbildschirm.
- Kurze Selbsteinschätzung mit drei Aussagen (z. B. „Ich erkenne sicher, wann der Sinussatz passt.“) auf einer 4-stufigen Skala.
- Übersicht: Anzahl benötigter Hinweise pro Raum, damit Lernende und Lehrkraft sehen, wo es gehakt hat.

TECHNISCHES
- Spielstand in localStorage speichern (in try/catch), damit ein versehentliches Neuladen nicht alles löscht; Button „Neu starten“.
- Keine Daten an Server senden.
- Code übersichtlich kommentieren, die Raumdaten in einem gut editierbaren JavaScript-Array am Anfang ablegen, damit die Lehrkraft Werte und Hinweise leicht ändern kann.
```

---

## Didaktische Begründung

**Strukturieren vor Rechnen.** Der häufigste Fehler beim Sinussatz ist nicht das Rechnen, sondern das falsche Zuordnen von Seite und Winkel. Deshalb verlangt jeder Raum zuerst, das vollständige Paar aus Seite und gegenüberliegendem Winkel zu identifizieren. Das macht den Strukturierungsschritt sichtbar und für die Lehrkraft überprüfbar.

**Begründete Verfahrenswahl.** Die Lernenden müssen das Verfahren nicht nur wählen, sondern auch begründen. Raum 3 (reine Zuordnung) und Raum 5 (die „Falle“ mit SWS) trainieren gezielt die Grenze des Sinussatzes. So entsteht flexibles Wissen statt einer starren Rechenroutine.

**Steigende Schwierigkeit.** Die Räume folgen einer Progression: direkte Anwendung (1, 2), Verfahrenswahl (3), Winkelberechnung (4), Abgrenzung zum Kosinussatz (5), Sachaufgaben im Vermessungskontext (6, 7) und der anspruchsvolle mehrdeutige Fall (8). Dadurch erleben alle früh Erfolge, während leistungsstärkere Lernende am Ende gefordert werden.

**Hinweisgebende Rückmeldung.** Gestufte Denkanstöße halten die kognitive Aktivität bei den Lernenden, statt sie durch fertige Lösungen abzunehmen. Die Hinweise zielen auf typische Fehlvorstellungen (falsches Paar, Bogenmaß, übersehene zweite Lösung) und wirken damit wie eine individuelle Lernbegleitung.

**Beurteilen durch Plausibilität.** Kurze Kontrollfragen (z. B. „größter Winkel gegenüber der größten Seite“) verankern das dritte Lernziel, ohne den Spielfluss zu bremsen.

**Motivation durch das Escape-Format.** Das Lösungswort, die sich öffnenden Schlösser und die Vermessungsgeschichte geben dem Üben ein Ziel. Die Hinweisstatistik am Ende liefert zugleich eine Diagnose für die Lehrkraft.

---

## Hinweis zur Anpassung

Falls der Kosinussatz in der Klasse noch nicht behandelt wurde: In Raum 3 die Kategorie „Kosinussatz“ durch „Mit dem Sinussatz allein nicht lösbar“ ersetzen und Raum 5 nur bis zur begründeten Entscheidung spielen lassen (ohne Rechnung).
