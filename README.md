# M644 CNC – Lernkarten

Interaktive Lernkarten (Flashcards) zur Vorbereitung auf die Klausur im **Modul M644 CNC**
(HTW Dresden, Fak. Maschinenbau – PT, Prof. Jäckel, SS 2026).

Jede Karte lässt sich mit **✓ Sicher** oder **✗ Nicht gewusst** bewerten. Der Fortschritt wird
im Browser gespeichert (`localStorage`), sodass du gezielt die noch nicht sitzenden Karten
wiederholen kannst.

## Inhalt

Die Fragen orientieren sich an den offiziellen **Prüfungsschwerpunkten** und decken **A-Wissen**
(typischer Prüfungsstoff) und **B-Wissen** (kommt seltener dran) ab. Themen:

| Thema | Quelle (Skript) |
|---|---|
| NC-Programmierung | 1_M644_Skript_NC-Programmierung |
| CNC-Steuerungen | 2_M644_Skript_CNC-Steuerungen |
| CAM-Systeme | 3_M644_Skript_CAM-Systeme |
| Funktionen CNC-Maschine | 4_M644_Skript_Funktionen CNC-Maschine |

Aktuell **79 Karten** in drei Formaten: offene Prüfungsfragen, Multiple-Choice und kurze Karteikarten.

## Benutzung

### Online (GitHub Pages)
👉 **https://trampa336.github.io/m644-cnc-lernkarten/**

### Lokal
Einfach `index.html` im Browser öffnen – oder, damit die Kartendaten (`fetch`) geladen werden,
einen kleinen lokalen Server starten:

```bash
python3 -m http.server 8000
# dann http://localhost:8000 öffnen
```

### Bedienung
- **Antwort zeigen** / `Leertaste` – Antwort aufdecken
- `→` – **Sicher** · `←` – **Nicht gewusst**
- `n` / `p` – nächste / vorherige Karte
- Filter nach **Thema**, **Priorität (A/B)** und **Typ**
- **„Nur nicht gewusst wiederholen“** – drillt nur die offenen/schwachen Karten
- **Mischen** und **Fortschritt zurücksetzen**

## Eigene Karten hinzufügen

Karten liegen als JSON unter [`data/`](data/) – eine Datei pro Thema. Aufbau einer Karte:

```json
{
  "id": "nc-030",
  "topic": "NC-Programmierung",
  "subtopic": "Bezugspunkte",
  "priority": "A",
  "type": "open",
  "question": "Frage …",
  "answer": "Antwort …",
  "options": ["…"],
  "answerIndex": 0,
  "image": "img/dateiname.png"
}
```

- `type`: `open` (offene Frage), `mc` (Multiple Choice, dann `options` + `answerIndex` nötig)
  oder `flashcard` (kurze Karteikarte).
- `priority`: `A` oder `B`.
- `image` ist optional und wird auf der Antwortseite angezeigt.

## Hinweise

- Die Schwerpunkte gelten laut Dozent **einmalig für die aktuelle Prüfung** (SS 2026).
- Die Skript-PDFs selbst sind **nicht** Teil dieses Repos (Urheberrecht). Die Diagramme unter
  `img/` sind Auszüge zur Lernunterstützung.
- Inhaltliche Fehler? Gerne per Issue/PR korrigieren.

*Kein offizielles Material der HTW Dresden – privates Lernprojekt.*
