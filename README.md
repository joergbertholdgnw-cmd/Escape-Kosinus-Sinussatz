# Das Vermessungsamt – Escape-Spiele zum Sinus- und Kosinussatz

Digitale Escape-Spiele für Mathematik, Klasse 10 (Gymnasium). Jedes Spiel ist eine einzelne HTML-Datei, die ohne Installation im Browser läuft, auf Tablet, Smartphone oder PC.

| Datei | Inhalt | Lösungswort |
|---|---|---|
| `teil1/index.html` | Teil 1: Sinussatz, 8 Räume | DREIECKE |
| `teil2/index.html` | Teil 2: Sinus- und Kosinussatz im Vergleich, 8 Akten in 3 Stufen | GEOMETER |
| `index.html` | Startseite mit Links zu beiden Teilen | |
| `vorlagen/` | Planung, Lösungen und Coding-Prompts zu beiden Teilen | |

## Ablauf in jedem Raum

1. **Ordnen:** gegebene Größen zuordnen (Was liegt sich gegenüber? Ist ein vollständiges Paar bekannt?)
2. **Entscheiden:** Verfahren und Begründung wählen
3. **Rechnen:** Ergebnis eingeben (Komma oder Punkt; Toleranz ±0,1 bei Längen, ±0,2° bei Winkeln)
4. **Prüfen:** Plausibilität beurteilen

Bei falschen Antworten gibt es gestufte Hinweise, nie die Lösung.

## Hinweise für Lehrkräfte

- **Lehrkraft-Modus (Teil 2):** `teil2/index.html?lehrkraft=1` öffnet eine Auswahl, mit der man direkt zu jeder Akte springen kann. Lösungen werden dabei nicht angezeigt.
- **Spielstand:** Er wird nur lokal im Browser gespeichert (localStorage). Es werden keine Daten an einen Server gesendet.
- **Auswertung:** Am Ende zeigt Teil 2 die Fehlversuche und Tipps pro Akte und eine Selbsteinschätzung. Beides lässt sich als Text kopieren.
- **Werte ändern:** Alle Aufgaben, Lösungen, Hinweise und typischen Fehlwerte stehen im `ROOMS`-Array am Anfang des Scripts.

## Auf der Website mathe-koenner

Teil 2 wird von der Website mathe-koenner direkt aus diesem Repository übernommen (Ordner `teil2`). Änderungen hier kommen spätestens nach dem nächtlichen Lauf dort an.

## Online bereitstellen (GitHub Pages)

Unter *Settings → Pages* als Quelle „Deploy from a branch“, Branch `main`, Ordner `/ (root)` wählen. Danach ist die Startseite unter `https://joergbertholdgnw-cmd.github.io/escape-kosinus-sinussatz/` erreichbar.
