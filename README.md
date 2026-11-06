# Grundriss-Planer

Ein Werkzeug zum Zeichnen von Grundrissen, das ohne Installation im Browser läuft. Du zeichnest Wände, legst echte Längen fest und platzierst Objekte maßstabsgetreu. Außerdem kannst du Wege einzeichnen, Räume beschriften und Abstände messen.

Das ganze Programm steckt in **einer einzigen HTML-Datei**. Es braucht keinen Server, keinen Build-Schritt und keine Abhängigkeiten.

## Schnellstart

1. `grundriss-planer.html` aus diesem Repository herunterladen.
2. Im Browser öffnen (Chrome, Edge oder Firefox).
3. Beim Start ist ein Beispielplan geladen. Mit **Neu** beginnst du einen leeren Grundriss.

Ohne Internetverbindung funktioniert alles. Es fehlt nur die Webschrift, an ihrer Stelle wird eine Systemschrift verwendet.

## Funktionen

### Wände und Maßstab

- Wände zeichnest du als Linienzug. Ecken und T-Stöße werden automatisch verbunden.
- **Exakte Längen:** Tippe während des Zeichnens eine Zahl ein und drücke Enter, z. B. `350`, `3,5m` oder `3500mm`.
- **Maßstab über eine Referenz:** Die erste Wandlänge, die du festlegst, bestimmt den Maßstab. Die ganze Zeichnung wird danach auf diesen Maßstab gebracht.
- **Wandlänge ändern:** Mit Doppelklick auf eine Wand gibst du ihre Länge ein. Du wählst dabei, welcher Punkt fest bleibt (Anfang, Mitte oder Ende). Anschließende Wände werden mitgezogen, damit der Raum rechtwinklig bleibt.
- **Wandmaß umschaltbar:** Längen werden innen, außen oder auf der Achse angezeigt und eingegeben. Ecken und T-Anschlüsse werden dabei berücksichtigt.
- Festgelegte Längen erscheinen fett. Nur gezeichnete Längen sind mit „≈“ markiert.

### Objekte

- Beim Einfügen gibst du Name, Breite, Tiefe, Drehung, Form (Rechteck oder rund) und Farbe an.
- Vorlagen gibt es z. B. für Europalette, Gitterbox, Schaltschrank und Werkbank.
- Mit Doppelklick änderst du die Größe.
- Am ausgewählten Objekt zeigt das Tool die **Abstände zur nächsten Wand oder zum nächsten Objekt**. Ein Klick auf einen Abstand setzt ihn exakt.

### Wege

- Wege zeichnest du als Linienzug mit echter Breite.
- Es gibt vier Wegarten:

  | Art | Farbe | Standardbreite | Richtungspfeile |
  |---|---|---|---|
  | Verkehrsweg | gelb | 120 cm | aus |
  | Fluchtweg | grün | 120 cm | an |
  | Staplerweg | orange | 250 cm | aus |
  | Laufweg | blau | 80 cm | an |

- Breite, Bezeichnung und Pfeile lassen sich anpassen. Die Pfeilrichtung kannst du umkehren.
- Länge und ungefähre Fläche werden angezeigt.

> Die Standardbreiten sind nur Startwerte. Welche Mindestbreiten tatsächlich gelten, prüfst du anhand der einschlägigen Regeln, z. B. ASR A1.8 und ASR A2.3.

### Texte

- Freie Beschriftung, z. B. für Raumnamen. Mehrzeilige Texte sind möglich.
- Die Schriftgröße ist eine Höhe im Plan (z. B. 35 cm). Sie skaliert beim Zoomen mit und wird im richtigen Maßstab gedruckt.

### Messen

- Du misst zwischen zwei Punkten. Die Punkte rasten an Ecken, Objektkanten und Wegpunkten ein.
- Messungen bleiben im Plan stehen und lassen sich nachträglich ziehen.

### Speichern, Teilen und Drucken

| Funktion | Ergebnis |
|---|---|
| **Speichern** | Lädt den Plan als `.json`-Datei herunter |
| **Öffnen** | Lädt eine solche `.json`-Datei |
| **Als HTML teilen** | Lädt eine eigenständige HTML-Datei mit eingebettetem Plan herunter |
| **Drucken / PDF** | Druck in A4 oder A3 mit festem Maßstab (1:20 bis 1:500) oder eingepasst, optional mit Objekt- und Wegeliste |
| PNG-Export | Speichert den Plan als Bild (im Druckdialog) |

Zusätzlich speichert der Browser den aktuellen Stand automatisch.

**Hinweise zum Drucken:**

- Für ein PDF wählst du im Druckfenster des Browsers „Als PDF speichern“.
- Für einen maßstabsgetreuen Ausdruck stellst du die Skalierung auf 100 % bzw. „Tatsächliche Größe“.
- Passt der Plan beim gewählten Maßstab nicht aufs Blatt, sagt das Tool dir, wie viel Platz fehlt.

**Hinweis zum Teilen:** Änderungen in einer geöffneten Datei bleiben im Browser des jeweiligen Nutzers. Die Datei selbst ändert sich nicht. Einen neuen Stand gibst du weiter, indem du erneut **Als HTML teilen** klickst.

## Bedienung

### Werkzeuge

| Taste | Werkzeug |
|---|---|
| `V` | Auswählen und verschieben |
| `W` | Wand zeichnen |
| `O` | Objekt einfügen |
| `G` | Weg zeichnen |
| `T` | Text einfügen |
| `M` | Messen |

### Beim Zeichnen von Wänden und Wegen

| Eingabe | Wirkung |
|---|---|
| Klick | Punkt setzen |
| Zahl + `Enter` | Exakte Länge der nächsten Strecke |
| `Shift` gedrückt | Nur rechtwinklig zeichnen |
| `Rücktaste` | Letzten Wegpunkt entfernen |
| `Enter`, `Esc` oder Doppelklick | Zeichnen beenden |

### Allgemein

| Eingabe | Wirkung |
|---|---|
| Doppelklick | Wand, Objekt, Weg oder Text bearbeiten |
| `R` | Ausgewähltes Objekt oder ausgewählten Text um 90° drehen |
| `L` | Wandmaß wechseln (innen, außen, Achse) |
| Pfeiltasten | Auswahl um 1 cm verschieben (mit `Shift` um 10 cm) |
| `Entf` | Auswahl löschen |
| `F` | Ganzen Plan einpassen |
| Mausrad, `+` / `−` | Zoomen |
| Leere Fläche ziehen oder rechte Maustaste | Ansicht verschieben |
| `Alt` beim Ziehen | Ohne Raster frei verschieben |
| `Strg+Z` / `Strg+Y` | Rückgängig / Wiederholen |
| `Strg+S` | Als JSON speichern |
| `Strg+P` | Drucken / PDF |

## Dateiformat

Ein gespeicherter Plan ist eine JSON-Datei. **Alle Maße sind in Zentimetern.** Die y-Achse zeigt nach unten.

```json
{
  "name": "Halle 9-14",
  "calibrated": true,
  "thick": 24,
  "lenMode": "axis",
  "verts":  [{ "id": "v0", "x": 0, "y": 0 }],
  "walls":  [{ "id": "w0", "a": "v0", "b": "v1", "fixed": true }],
  "objs":   [{ "id": "o1", "name": "Europalette", "x": 500, "y": 300,
               "w": 120, "d": 80, "rot": 0, "shape": "rect", "color": "#2f6fdb" }],
  "paths":  [{ "id": "p1", "name": "Fluchtweg", "kind": "escape", "width": 120,
               "arrows": true, "pts": [{ "x": 100, "y": 430 }, { "x": 640, "y": 430 }] }],
  "texts":  [{ "id": "t1", "text": "Lager", "x": 1000, "y": 330,
               "size": 40, "bold": true, "rot": 0, "color": "" }],
  "dims":   [{ "id": "m1", "x1": 800, "y1": 462, "x2": 800, "y2": 788 }]
}
```

| Feld | Bedeutung |
|---|---|
| `calibrated` | `true`, sobald eine Länge den Maßstab festgelegt hat |
| `thick` | Wandstärke in cm |
| `lenMode` | Angezeigtes Wandmaß: `inner`, `outer` oder `axis` |
| `verts` | Eckpunkte. Wände verweisen über `a` und `b` auf sie. |
| `walls` | Wände. `fixed` markiert eine festgelegte Länge. |
| `objs` | Objekte. `x`/`y` ist der Mittelpunkt, `w`/`d` sind Breite und Tiefe, `rot` die Drehung in Grad. `shape` ist `rect` oder `circle`. |
| `paths` | Wege. `kind` ist `traffic`, `escape`, `forklift` oder `walk`. |
| `texts` | Texte. `size` ist die Schrifthöhe in cm. |
| `dims` | Gespeicherte Messungen |

Damit lassen sich Pläne auch per Skript erzeugen, z. B. aus vorhandenen Zeichnungen oder Tabellen.

## Technik

- Reines HTML, CSS und JavaScript in einer Datei, ohne Frameworks.
- Die Zeichnung entsteht auf einem HTML-Canvas.
- Der Arbeitsstand liegt im `localStorage` des Browsers. Jede geteilte HTML-Datei bekommt dort einen eigenen Speicherplatz.
- Bei einer geteilten Datei steckt der Plan in einem `<script id="plan-data" type="application/json">`-Block.
- Helles und dunkles Design folgen der Systemeinstellung. Ausdrucke sind immer hell.

### Auf GitHub Pages veröffentlichen

Lege die Datei als `index.html` ins Repository und aktiviere GitHub Pages. Das Tool läuft dann direkt unter der Pages-Adresse.

Beachte dabei: Der automatisch gespeicherte Stand liegt pro Browser und pro Adresse. Er ist also nicht zwischen Nutzern geteilt. Zum Austausch nutzt ihr **Speichern** oder **Als HTML teilen**.

## Grenzen

- Es gibt eine Wandstärke für den ganzen Plan.
- Türen und Fenster sind keine eigenen Elemente. Als Ersatz kannst du Objekte oder Texte verwenden.
- Wandlängen, die du beim Zeichnen eintippst, gelten immer als Achsmaß. Danach kannst du die Wand per Doppelklick auf ein Innen- oder Außenmaß bringen.
- Gleichzeitiges Bearbeiten durch mehrere Personen ist nicht möglich.

## Lizenz

Veröffentlicht unter der [MIT-Lizenz](LICENSE). Du darfst das Tool frei verwenden, verändern und weitergeben, auch kommerziell. Der Copyright-Hinweis muss dabei erhalten bleiben. Das Tool wird ohne Gewähr bereitgestellt.
