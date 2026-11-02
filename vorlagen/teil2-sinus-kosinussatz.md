# Escape-Spiel „Das Vermessungsamt – Teil 2“: Sinus- und Kosinussatz – Klasse 10

## 1. Rahmen

| Frage | Entscheidung |
|---|---|
| Fach / Thema | Mathematik, Sinussatz und Kosinussatz im Vergleich |
| Vorwissen | Teil 1 (Sinussatz) gespielt, Kosinussatz eingeführt |
| Lernziele | Anwenden, Verfahren begründet wählen, Ergebnisse beurteilen |
| Interaktionsform | Digitales Escape-Spiel (eine HTML-Datei, Tablet/Smartphone) |
| Umfang | 8 Räume, ca. eine Doppelstunde |
| Differenzierung | Drei Stufen mit steigendem Schwierigkeitsgrad |
| Rückmeldung | Gestufte Denkanstöße, nie die fertige Lösung |
| Lösungswort | **GEOMETER** (= alter Name für Landvermesser) |

**Rahmenhandlung.** Nach der Flucht aus dem alten Vermessungsamt (Teil 1) erhält die Klasse einen Auftrag: Im Archiv des Amtes liegen acht unerledigte Vermessungsakten. Jede Akte ist mit einem Zahlenschloss gesichert. Wer eine Akte richtig bearbeitet, erhält einen Buchstaben. Die acht Buchstaben ergeben die Berufsbezeichnung, die als Passwort für den Ausgang dient.

**Ablauf in jedem Raum** (wie in Teil 1):
1. *Strukturieren*: gegebene Größen in der Skizze zuordnen (Welche Seite liegt welchem Winkel gegenüber? Ist ein vollständiges Paar bekannt?).
2. *Begründet auswählen*: Verfahren **und** Begründung wählen. Erst wenn beides stimmt, öffnet sich das Rechenfeld.
3. *Anwenden*: Ergebnis eingeben (Komma und Punkt erlaubt, Toleranz ±0,1 bei Längen, ±0,2° bei Winkeln).
4. *Beurteilen*: kurze Plausibilitätsfrage.

**Stufen**

| Stufe | Räume | Anforderung |
|---|---|---|
| I – Anwenden | 1–3 | Je ein Satz, direkt anwendbar, realer Kontext |
| II – Entscheiden | 4–6 | Verfahrenswahl, zwei Rechenschritte, versteckte Fallen |
| III – Kombinieren und Modellieren | 7–8 | Beide Sätze in einer Aufgabe, mehrdeutiger Fall mit Entscheidung im Kontext |

---

## 2. Die acht Räume

Alle Werte sind per Skript nachgerechnet (Python, Gradmaß).

### Stufe I – Anwenden

#### Raum 1 – Der neue Zaun (Buchstabe G) · Kosinussatz, Seite
Ein dreieckiges Grundstück hat an der Ecke A zwei Grenzen von 45 m und 62 m Länge, die einen Winkel von 74° einschließen. Wie lang muss der Zaun an der dritten Grenze werden?

- Strukturieren: Der Winkel 74° liegt **zwischen** den beiden bekannten Seiten (SWS); kein vollständiges Paar.
- Verfahren: Kosinussatz. Begründung: „Zwei Seiten und der eingeschlossene Winkel sind bekannt.“
- **Lösung: a ≈ 65,81 m**
- Beurteilen: „Bei einem rechten Winkel wäre der Zaun √(45² + 62²) ≈ 76,6 m lang. Muss er bei 74° kürzer oder länger sein?“ → kürzer, weil der Winkel kleiner als 90° ist.
- Hinweise: (1) „Liegt der bekannte Winkel zwischen den bekannten Seiten oder gegenüber?“ (2) „a² = b² + c² − 2bc·cos α“ (3) „Rechnest du im Gradmaß (DEG)? Zieh am Ende die Wurzel.“

#### Raum 2 – Der Dachstuhl (Buchstabe E) · Kosinussatz, Winkel
Ein Zimmermann baut ein asymmetrisches Dach. Die beiden Dachsparren sind 5,2 m und 6,8 m lang, die Spannweite unten beträgt 9,5 m. Welcher Winkel entsteht am First?

- Strukturieren: Drei Seiten bekannt (SSS); der Winkel am First liegt der Spannweite gegenüber.
- Verfahren: Kosinussatz (nach dem Winkel umgestellt).
- **Lösung: γ ≈ 103,9°**
- Beurteilen: „Warum ist der Winkel am First stumpf?“ → weil 9,5² > 5,2² + 6,8² (90,25 > 73,28), also cos γ < 0.
- Hinweise: (1) „Welche Seite liegt dem Firstwinkel gegenüber?“ (2) „cos γ = (a² + b² − c²) / (2ab)“ (3) „Ein negativer Kosinuswert ist kein Fehler.“

#### Raum 3 – Die Insel im Bergsee (Buchstabe O) · Sinussatz, Seite
Zwei Messpunkte A und B am Ufer eines Bergsees liegen 850 m auseinander. Von A aus erscheint eine Insel C unter 52°, von B aus unter 67° zur Strecke AB. Wie weit ist die Insel von A entfernt?

- Strukturieren: Zuerst γ = 61° bestimmen; vollständiges Paar AB–γ. Gesucht AC liegt β gegenüber.
- Verfahren: Sinussatz (WSW).
- **Lösung: AC ≈ 894,59 m**
- Beurteilen: „Ist AC länger als AB? Prüfe mit den gegenüberliegenden Winkeln.“ (67° > 61° → ja)
- Hinweise: (1) „Welcher Winkel fehlt noch?“ (2) „Welcher Winkel liegt AC gegenüber?“ (3) „AC / sin 67° = 850 / sin 61°“

### Stufe II – Entscheiden

#### Raum 4 – Die Aktensortierung (Buchstabe M) · Verfahrenswahl, keine Rechnung
Ordne fünf Situationen per Drag-and-drop dem passenden Verfahren zu:

| Situation | Verfahren |
|---|---|
| Eine 6 m lange Leiter lehnt unter 70° an einer senkrechten Wand. Wie hoch reicht sie? | Rechtwinkliges Dreieck (sin/cos/tan) |
| Zwei Wanderwege gehen von einer Kreuzung ab (3,2 km und 4,5 km lang) und bilden 58°. Wie weit liegen die Enden auseinander? | Kosinussatz (SWS) |
| Ein dreieckiges Segel hat die Seiten 4 m, 5 m und 6 m. Wie groß ist der Winkel am Mast? | Kosinussatz (SSS) |
| Zwei Förster peilen ein Feuer vom Ende einer 2 km langen Strecke mit 48° und 71° an. | Sinussatz (WSW) |
| Ein Stützbalken: zwei Seiten bekannt und der Winkel gegenüber der kürzeren. | Sinussatz, Vorsicht: evtl. zwei Lösungen (SsW) |

- Raum öffnet sich bei fünf richtigen Zuordnungen.
- Hinweise: (1) „Gibt es einen rechten Winkel?“ (2) „Ist ein Paar aus Seite und gegenüberliegendem Winkel vollständig?“ (3) „Liegt der bekannte Winkel zwischen den Seiten oder gegenüber?“

#### Raum 5 – Der Schusswinkel (Buchstabe E) · Kosinussatz, dann Sinussatz
Beim Fußball steht der Ball 16 m vom linken Pfosten entfernt. Die Verbindung Ball–linker Pfosten bildet mit der Torlinie einen Winkel von 72°. Das Tor ist 7,32 m breit. In welchem Winkel „sieht“ der Ball das Tor (Schusswinkel)?

- Schritt 1: Abstand Ball–rechter Pfosten mit dem Kosinussatz (SWS). **Lösung: ≈ 15,40 m**
- Schritt 2: Schusswinkel mit dem Sinussatz (liegt der Torbreite gegenüber). **Lösung: ≈ 26,9°**
- Strukturieren: Wer sofort den Sinussatz wählt, bekommt: „Ist ein vollständiges Paar bekannt?“
- Beurteilen: „Darf man den Sinussatz hier ohne Sorge um eine zweite Lösung nutzen?“ → Ja, weil die Torbreite die kürzeste Seite ist, der Schusswinkel also spitz sein muss.
- Hinweise: (1) „Zeichne das Dreieck Ball–linker Pfosten–rechter Pfosten.“ (2) „Der 72°-Winkel liegt zwischen 16 m und 7,32 m.“ (3) „sin(Schusswinkel) = 7,32 · sin 72° / 15,40“

#### Raum 6 – Kurswechsel auf See (Buchstabe T) · Kosinussatz, dann Sinussatz, mit Falle
Ein Segelboot fährt vom Hafen H aus 14 km geradeaus bis zur Boje B. Dort ändert es seinen Kurs um 35° nach Steuerbord und fährt 9 km weiter bis zum Punkt P. Wie weit ist es jetzt vom Hafen entfernt, und um wie viel Grad weicht die Richtung zu P vom ursprünglichen Kurs ab (Winkel bei H)?

- Falle: Der Innenwinkel bei B ist **145°**, nicht 35°. Wer 35° einsetzt, erhält ≈ 8,4 km und den Hinweis: „Das Boot ist fast 23 km gefahren. Kann es nur 8,4 km vom Hafen entfernt sein?“
- Schritt 1: **HP ≈ 21,99 km** (Kosinussatz)
- Schritt 2: **Winkel bei H ≈ 13,6°** (Sinussatz; eindeutig, da der Winkel 9 km gegenüberliegt und 145° bereits der stumpfe Winkel ist)
- Hinweise: (1) „Skizziere den Kurswechsel. Welcher Winkel liegt im Dreieck?“ (2) „Innenwinkel = 180° − Kursänderung“ (3) „Für Schritt 2: Welche Seite liegt dem Winkel bei H gegenüber?“

### Stufe III – Kombinieren und Modellieren

#### Raum 7 – Das Viereck-Grundstück (Buchstabe E) · beide Sätze kombiniert
Ein Grundstück hat die Form eines Vierecks ABCD. Gemessen wurden: AB = 60 m, BC = 45 m, ∠B = 110°, CD = 50 m, ∠D = 95°. Die Diagonale AC teilt das Grundstück in zwei Dreiecke. Wie lang ist die Grenze AD?

- Schritt 1: Diagonale AC im Dreieck ABC mit dem Kosinussatz. **Lösung: AC ≈ 86,44 m**
- Schritt 2: Im Dreieck ACD ist AC–∠D ein vollständiges Paar. ∠CAD mit dem Sinussatz: ≈ 35,2° (eindeutig, da ∠D stumpf). Dann ∠ACD ≈ 49,8°.
- Schritt 3: **AD ≈ 66,29 m** (Sinussatz)
- Abfrage: AC und AD einzeln.
- Beurteilen: „Warum musste in Dreieck ABC der Kosinussatz und in Dreieck ACD der Sinussatz verwendet werden?“ (Auswahl)
- Hinweise: (1) „Teile das Viereck entlang AC.“ (2) „In welchem Teildreieck reichen die Angaben schon aus?“ (3) „Für AD brauchst du den Winkel bei C im Dreieck ACD.“

#### Raum 8 – Die verlorene Drohne (Buchstabe R) · mehrdeutiger Fall im Kontext
Eine Vermessungsdrohne hat den Funkkontakt verloren. Station A meldet: Abstand zur Drohne 120 m. Die Stationen A und B sind 150 m voneinander entfernt. Station B peilt die Drohne unter 40° zur Strecke BA an. Wie weit ist die Drohne von Station B entfernt?

- Strukturieren: Gegeben sind zwei Seiten und ein Winkel, der nicht eingeschlossen ist (SsW, 40° liegt der kürzeren Seite 120 m gegenüber).
- Auswahlfrage: „Wie viele Positionen sind möglich?“ (0 / 1 / 2) → **2**
- Lösungen: ∠C₁ ≈ 53,5° → **BC₁ ≈ 186,35 m**; ∠C₂ ≈ 126,5° → **BC₂ ≈ 43,47 m**
- Modellieren: Zusatzinformation „Station B meldet: Die Drohne ist mehr als 100 m entfernt.“ → Welche Position ist richtig? → **BC ≈ 186,35 m**
- Beurteilen: „Warum liefert der Sinussatz hier zwei Winkel?“ (sin x = sin(180° − x); beide passen in die Winkelsumme)
- Hinweise: (1) „Liegt der bekannte Winkel der längeren oder der kürzeren Seite gegenüber?“ (2) „Prüfe auch 180° − ∠C.“ (3) „Berechne für jeden Fall den Winkel bei A und dann BC.“

---

## 3. Abschluss

- Eingabe des Lösungsworts **GEOMETER**, Erfolgsbildschirm.
- Selbsteinschätzung (4-stufige Skala): „Ich erkenne, ob Sinus- oder Kosinussatz passt.“ / „Ich finde den richtigen Innenwinkel in einer Sachsituation.“ / „Ich erkenne, wann es zwei Lösungen geben kann.“
- Übersicht der benötigten Hinweise pro Raum (Diagnose für Lehrkraft).

## 4. Didaktische Begründung

- **Stufe I** sichert jeden Satz einzeln in einem realen Kontext ab und baut Selbstvertrauen auf.
- **Stufe II** verlagert den Schwerpunkt vom Rechnen aufs Entscheiden. Raum 6 enthält mit dem Kurswinkel einen typischen Modellierungsfehler aus der Praxis; die Plausibilitätsfrage macht ihn selbst entdeckbar.
- **Stufe III** verlangt, eine Figur zu zerlegen und beide Sätze nacheinander einzusetzen (Raum 7) sowie einen mathematisch mehrdeutigen Befund mit Kontextwissen zu entscheiden (Raum 8). Hier liegt der Kern des Modellierens: Die Mathematik liefert Möglichkeiten, die Sachsituation wählt aus.
- Die Struktur „Strukturieren → Begründen → Rechnen → Beurteilen“ bleibt aus Teil 1 erhalten, damit die Lernenden die Arbeitsweise wiedererkennen.

---

## 5. Optimierter Coding-Prompt

> Den folgenden Block vollständig in Claude (oder ein anderes KI-Werkzeug) kopieren. Er enthält alle Werte, das Dokument oben wird nicht zusätzlich benötigt.

```
Erstelle eine eigenständige, interaktive HTML-Anwendung (eine einzige Datei mit HTML, CSS und JavaScript, ohne externe Abhängigkeiten außer optional einer CDN-Schriftart) für ein digitales Escape-Spiel „Das Vermessungsamt – Teil 2: Sinus- und Kosinussatz“ für Schülerinnen und Schüler der Klasse 10 eines Gymnasiums. Alle Texte auf Deutsch, die Lernenden werden mit „du“ angesprochen.

RAHMENHANDLUNG
Nach der Flucht aus dem alten Vermessungsamt (Teil 1) bekommen die Lernenden einen Auftrag: Im Archiv liegen acht unerledigte Vermessungsakten, jede mit einem Zahlenschloss gesichert. Wer eine Akte löst, erhält einen Buchstaben. Die 8 Buchstaben ergeben das Lösungswort GEOMETER (alter Name für Landvermesser), mit dem sich der Ausgang öffnet. Startbildschirm mit kurzer Geschichte (3–4 Sätze) und Button „Archiv betreten“.

STUFEN (in der Fortschrittsleiste farblich kennzeichnen)
Stufe I „Anwenden“: Räume 1–3. Stufe II „Entscheiden“: Räume 4–6. Stufe III „Kombinieren und Modellieren“: Räume 7–8. Beim Übergang in eine neue Stufe kurze Zwischenkarte („Stufe II: Jetzt musst du selbst entscheiden, welcher Satz passt.“).

DIDAKTISCHER KERN (in jedem Rechenraum genau in dieser Reihenfolge)
1. Strukturieren: Die Lernenden markieren in der SVG-Skizze, welche Seite welchem Winkel gegenüberliegt, oder beantworten per Auswahl, ob ein vollständiges Paar „Seite + gegenüberliegender Winkel“ bekannt ist bzw. welcher Fall vorliegt (SSS, SWS, WSW, SsW).
2. Begründet auswählen: Verfahren (Sinussatz / Kosinussatz / Trigonometrie im rechtwinkligen Dreieck) UND eine Begründung aus 3–4 Vorgaben wählen. Erst wenn beides stimmt, wird das Rechenfeld freigeschaltet. Bei mehrschrittigen Räumen erfolgt die Verfahrenswahl vor jedem Schritt erneut.
3. Anwenden: Ergebnis eingeben. Dezimalkomma UND Dezimalpunkt akzeptieren, Einheiten im Eingabefeld ignorieren. Toleranz ±0,1 bei Längen, ±0,2° bei Winkeln. Bei Folgeschritten mit dem exakten Zwischenwert weiterrechnen, aber gerundete Eingaben (Zwischenergebnis auf 2 Nachkommastellen) ebenfalls innerhalb der Toleranz akzeptieren.
4. Beurteilen: kurze Plausibilitätsfrage als Auswahl (Single Choice), wie unten je Raum angegeben.

RÜCKMELDUNG (hinweisgebend)
- Bei falscher Eingabe NIE die Lösung zeigen. Gestufte Hinweise: 1. Fehlversuch → Hinweis 1, 2. Fehlversuch → Hinweis 2, ab dem 3. Fehlversuch → Hinweis 3 (bleibt sichtbar). Zusätzlich ein Button „Ich brauche einen Tipp“, der den nächsten Hinweis freiwillig öffnet und als genutzter Hinweis zählt.
- Erkenne typische Fehlwerte und gib dazu einen gezielten Hinweis (siehe „Fehlwerte“ je Raum). Allgemein: Ergebnis passt zu Bogenmaß statt Gradmaß → „Steht dein Taschenrechner auf DEG?“
- Bei richtiger Eingabe: kurze Bestätigung, Buchstabe erscheint mit kleiner Animation, Button „Nächste Akte“.

DIE 8 RÄUME (verwende genau diese Werte, alle Ergebnisse sind nachgerechnet)

Raum 1 – Der neue Zaun (Buchstabe G), Stufe I
Text: Ein dreieckiges Grundstück hat an der Ecke A zwei Grenzen von 45 m und 62 m Länge, die einen Winkel von 74° einschließen. Wie lang muss der Zaun an der dritten Grenze werden?
Strukturieren: „Wo liegt der bekannte Winkel?“ → zwischen den bekannten Seiten (SWS); „Ist ein vollständiges Paar bekannt?“ → nein.
Verfahren: Kosinussatz. Begründung (richtig): „Zwei Seiten und der eingeschlossene Winkel sind bekannt.“ Distraktoren: „Ein Winkel und die gegenüberliegende Seite sind bekannt.“ / „Das Dreieck ist rechtwinklig.“
Lösung: 65,81 m.
Beurteilen: „Bei einem rechten Winkel wäre der Zaun √(45² + 62²) ≈ 76,6 m lang. Muss er bei 74° kürzer oder länger sein?“ → kürzer, weil 74° < 90°.
Hinweise: (1) „Liegt der bekannte Winkel zwischen den bekannten Seiten oder gegenüber?“ (2) „a² = b² + c² − 2bc · cos α“ (3) „Rechne im Gradmaß (DEG) und zieh am Ende die Wurzel.“
Fehlwerte: 4331 (Wurzel vergessen) → „Hast du am Ende die Wurzel gezogen?“

Raum 2 – Der Dachstuhl (Buchstabe E), Stufe I
Text: Ein Zimmermann baut ein asymmetrisches Dach. Die beiden Dachsparren sind 5,2 m und 6,8 m lang, die Spannweite unten beträgt 9,5 m. Welcher Winkel entsteht am First?
Strukturieren: Drei Seiten bekannt (SSS); in der Skizze die Seite anklicken, die dem Firstwinkel gegenüberliegt (Spannweite).
Verfahren: Kosinussatz (nach dem Winkel umgestellt). Begründung: „Alle drei Seiten sind bekannt, kein Winkel.“
Lösung: 103,9°.
Beurteilen: „Warum ist der Winkel am First stumpf?“ → „Weil 9,5² größer ist als 5,2² + 6,8², also cos γ < 0.“
Hinweise: (1) „Welche Seite liegt dem Firstwinkel gegenüber?“ (2) „cos γ = (a² + b² − c²) / (2ab)“ (3) „Ein negativer Kosinuswert ist kein Fehler, er bedeutet einen stumpfen Winkel.“
Fehlwerte: 76,1 (Vorzeichenfehler, 180° − 103,9°) → „Prüfe das Vorzeichen im Zähler.“

Raum 3 – Die Insel im Bergsee (Buchstabe O), Stufe I
Text: Zwei Messpunkte A und B am Ufer eines Bergsees liegen 850 m auseinander. Von A aus erscheint eine Insel C unter 52°, von B aus unter 67° zur Strecke AB. Wie weit ist die Insel von A entfernt?
Strukturieren: Zuerst den Winkel bei C eingeben (61°). Dann: vollständiges Paar AB–γ; gesuchte Seite AC liegt β gegenüber.
Verfahren: Sinussatz. Begründung: „Eine Seite und alle Winkel sind bekannt, also gibt es ein vollständiges Paar.“
Lösung: 894,59 m.
Beurteilen: „Ist AC länger als AB?“ → ja, weil der gegenüberliegende Winkel 67° größer ist als 61°.
Hinweise: (1) „Welcher Winkel fehlt noch? Denk an die Winkelsumme.“ (2) „Welcher Winkel liegt AC gegenüber?“ (3) „AC / sin 67° = 850 / sin 61°“
Fehlwerte: 765,8 (falscher Winkel 52° statt 67° im Zähler) → „Liegt 52° wirklich AC gegenüber?“

Raum 4 – Die Aktensortierung (Buchstabe M), Stufe II, keine Rechnung
Zuordnung per Drag-and-drop (zusätzlich per Antippen bzw. Tastatur bedienbar: Karte wählen, dann Zielfeld wählen). Fünf Zielfelder: „Rechtwinkliges Dreieck (sin/cos/tan)“, „Kosinussatz (SWS)“, „Kosinussatz (SSS)“, „Sinussatz (WSW)“, „Sinussatz – Vorsicht, evtl. zwei Lösungen (SsW)“.
Karten:
- Eine 6 m lange Leiter lehnt unter 70° an einer senkrechten Wand. Wie hoch reicht sie? → Rechtwinkliges Dreieck
- Zwei Wanderwege gehen von einer Kreuzung ab (3,2 km und 4,5 km) und bilden 58°. Wie weit liegen die Enden auseinander? → Kosinussatz (SWS)
- Ein dreieckiges Segel hat die Seiten 4 m, 5 m und 6 m. Wie groß ist der Winkel am Mast? → Kosinussatz (SSS)
- Zwei Förster peilen ein Feuer von den Enden einer 2 km langen Strecke unter 48° und 71° an. → Sinussatz (WSW)
- Ein Stützbalken: zwei Seiten sind bekannt und der Winkel gegenüber der kürzeren Seite. → Sinussatz, evtl. zwei Lösungen (SsW)
Button „Prüfen“: falsch zugeordnete Karten werden markiert (ohne die richtige Lösung zu zeigen). Raum öffnet sich bei 5 richtigen Zuordnungen.
Hinweise: (1) „Gibt es einen rechten Winkel?“ (2) „Ist ein Paar aus Seite und gegenüberliegendem Winkel vollständig?“ (3) „Liegt der bekannte Winkel zwischen den Seiten oder einer Seite gegenüber?“

Raum 5 – Der Schusswinkel (Buchstabe E), Stufe II, zwei Schritte
Text: Beim Fußball liegt der Ball 16 m vom linken Pfosten entfernt. Die Verbindung Ball–linker Pfosten bildet mit der Torlinie einen Winkel von 72°. Das Tor ist 7,32 m breit. Unter welchem Winkel „sieht“ der Ball das Tor (Schusswinkel)?
SVG: Tor von oben mit beiden Pfosten, Ball, Dreieck Ball–linker Pfosten–rechter Pfosten.
Schritt 1: Abstand Ball–rechter Pfosten. Verfahren: Kosinussatz (SWS: 72° liegt zwischen 16 m und 7,32 m). Wer Sinussatz wählt, bekommt: „Ist ein vollständiges Paar bekannt?“ Lösung: 15,40 m.
Schritt 2: Schusswinkel. Verfahren: Sinussatz (jetzt ist das Paar 15,40 m – 72° vollständig). Lösung: 26,9°.
Beurteilen: „Musst du hier mit einer zweiten Lösung für den Schusswinkel rechnen?“ → nein, weil die Torbreite die kürzeste Seite ist und der Schusswinkel daher spitz sein muss.
Hinweise: (1) „Der 72°-Winkel liegt zwischen 16 m und 7,32 m.“ (2) „Für Schritt 2: Welche Seite liegt dem Schusswinkel gegenüber?“ (3) „sin(Schusswinkel) = 7,32 · sin 72° / 15,40“

Raum 6 – Kurswechsel auf See (Buchstabe T), Stufe II, zwei Schritte mit Falle
Text: Ein Segelboot fährt vom Hafen H aus 14 km geradeaus bis zur Boje B. Dort ändert es seinen Kurs um 35° nach Steuerbord und fährt 9 km weiter bis zum Punkt P. Wie weit ist es jetzt vom Hafen entfernt? Um wie viel Grad weicht die Richtung zu P vom ursprünglichen Kurs ab (Winkel bei H)?
SVG: Kursverlauf mit gestrichelter Verlängerung der ersten Strecke, Kursänderung 35° an der Verlängerung eingezeichnet, Innenwinkel bei B mit „?“.
Strukturieren: Zuerst den Innenwinkel bei B eingeben → 145°. Bei Eingabe 35°: „Der 35°-Winkel liegt außen, zwischen der Verlängerung und dem neuen Kurs. Welcher Winkel liegt im Dreieck?“
Schritt 1: HP mit dem Kosinussatz. Lösung: 21,99 km.
Fehlwerte Schritt 1: 8,40 → „Das Boot ist fast 23 km gefahren und hat nur leicht den Kurs geändert. Kann es nur 8,4 km vom Hafen entfernt sein?“
Schritt 2: Winkel bei H mit dem Sinussatz. Lösung: 13,6°.
Beurteilen: „Warum ist der Winkel bei H eindeutig?“ → weil das Dreieck mit 145° schon seinen stumpfen Winkel hat.
Hinweise: (1) „Skizziere den Kurswechsel. Welcher Winkel liegt im Dreieck?“ (2) „Innenwinkel = 180° − Kursänderung“ (3) „Für Schritt 2: Welche Seite liegt dem Winkel bei H gegenüber?“

Raum 7 – Das Viereck-Grundstück (Buchstabe E), Stufe III, beide Sätze kombiniert
Text: Ein Grundstück hat die Form eines Vierecks ABCD. Gemessen wurden: AB = 60 m, BC = 45 m, ∠B = 110°, CD = 50 m, ∠D = 95°. Wie lang ist die Grenze AD?
SVG: Viereck mit gestrichelter Diagonale AC; die beiden Teildreiecke beim Bearbeiten farblich hervorheben.
Strukturieren: „In welchem Teildreieck reichen die Angaben schon für eine Rechnung?“ → ABC (SWS).
Schritt 1: AC mit dem Kosinussatz. Lösung: 86,44 m.
Schritt 2: ∠CAD im Dreieck ACD mit dem Sinussatz (vollständiges Paar AC–∠D). Lösung: 35,2°.
Schritt 3: AD mit dem Sinussatz über ∠ACD = 49,8°. Lösung: 66,29 m.
Beurteilen: „Warum Kosinussatz in ABC, aber Sinussatz in ACD?“ → „In ABC liegt der Winkel zwischen den Seiten, in ACD ist mit AC und ∠D ein vollständiges Paar bekannt.“
Hinweise: (1) „Teile das Viereck entlang der Diagonalen AC.“ (2) „Im Dreieck ACD: Welcher Winkel liegt AC gegenüber?“ (3) „Für AD brauchst du den Winkel bei C im Dreieck ACD: 180° − 95° − ∠CAD.“

Raum 8 – Die verlorene Drohne (Buchstabe R), Stufe III, Endgegner
Text: Eine Vermessungsdrohne hat den Funkkontakt verloren. Station A meldet: Abstand zur Drohne 120 m. Die Stationen A und B sind 150 m voneinander entfernt. Station B peilt die Drohne unter 40° zur Strecke BA an. Wie weit ist die Drohne von Station B entfernt?
Strukturieren: Fall bestimmen → SsW (der 40°-Winkel liegt der kürzeren Seite 120 m gegenüber).
Auswahlfrage: „Wie viele mögliche Positionen der Drohne gibt es?“ (0 / 1 / 2) → 2.
Dann beide Abstände eingeben (Reihenfolge egal): 186,35 m und 43,47 m. Hintergrundwerte: ∠C₁ = 53,5°, ∠A₁ = 86,5°; ∠C₂ = 126,5°, ∠A₂ = 13,5°.
SVG: Nach richtiger Eingabe zeigt die Skizze animiert beide möglichen Drohnenpositionen auf dem Peilstrahl von B (Kreisbogen um A mit Radius 120 m schneidet den Strahl zweimal).
Modellieren: Zusatzmeldung „Station B: Die Drohne ist mehr als 100 m entfernt.“ → „Wo ist die Drohne?“ Auswahl 186,35 m / 43,47 m / nicht entscheidbar → 186,35 m.
Beurteilen: „Warum liefert der Sinussatz hier zwei Winkel?“ → „Weil sin x = sin(180° − x) und beide Winkel mit 40° zusammen unter 180° bleiben.“
Hinweise: (1) „Liegt der bekannte Winkel der längeren oder der kürzeren Seite gegenüber?“ (2) „Prüfe auch 180° − ∠C.“ (3) „Berechne für jeden Fall den Winkel bei A und dann BC mit dem Sinussatz.“

GESTALTUNG
- Jeder Raum als „Akte“ (Karteikarten-Optik) mit schlichter, maßstabsgetreu wirkender SVG-Skizze; gegebene Größen farbig, gesuchte Größe mit „?“, bereits berechnete Zwischenwerte erscheinen nachträglich in der Skizze.
- Fortschrittsleiste oben mit 8 Schloss-Symbolen in drei Stufenfarben, darunter die gesammelten Buchstaben.
- Ruhiges, gut lesbares Design, große Schrift, hoher Kontrast, responsiv für Tablet und Smartphone, alle Bedienelemente per Tastatur erreichbar, Fokus sichtbar.
- Formelkarte zum Aufklappen: Sinussatz, Kosinussatz (für Seite und nach Winkel umgestellt), Winkelsumme, Entscheidungshilfe „SSS/SWS → Kosinussatz, WSW/SsW → Sinussatz“, aber ohne Lösungen.
- Kein Zeitlimit; optional eine Stoppuhr, die nur angezeigt wird.

ABSCHLUSS
- Nach Raum 8 Eingabe des Lösungsworts GEOMETER (Groß-/Kleinschreibung egal), dann Erfolgsbildschirm.
- Selbsteinschätzung auf einer 4-stufigen Skala: „Ich erkenne, ob der Sinus- oder der Kosinussatz passt.“ / „Ich finde in einer Sachsituation den richtigen Innenwinkel.“ / „Ich erkenne, wann es zwei Lösungen geben kann.“
- Übersicht: Anzahl der Fehlversuche und genutzten Hinweise pro Raum, gegliedert nach Stufen, damit Lernende und Lehrkraft sehen, wo es gehakt hat. Button „Ergebnis als Text kopieren“.

TECHNISCHES
- Spielstand in localStorage speichern (jeder Zugriff in try/catch), Button „Neu starten“ mit Rückfrage.
- Keine Daten an einen Server senden.
- Code übersichtlich kommentieren. Raumdaten (Texte, Werte, Toleranzen, Begründungen, Hinweise, Fehlwerte) in einem gut editierbaren JavaScript-Array am Anfang der Datei ablegen, damit die Lehrkraft Werte leicht ändern kann.
- Lehrkraft-Modus über den URL-Parameter ?lehrkraft=1: zeigt einen Sprung zu jedem Raum (zum Testen), aber keine Lösungen.
```
