# Dataset Profile – Baromètre du live parisien

## Task 5 – Find a dataset

- **Gesucht auf:** data.gouv.fr (nationales französisches Open-Data-Portal)
- **Suchbegriff:** concert / live music
- **Treffer:** Baromètre du live parisien – concerts par arrondissement et par genre (été 2026)
- **Link:** [data.gouv.fr](https://www.data.gouv.fr/datasets/barometre-du-live-parisien-concerts-par-arrondissement-et-par-genre-ete-2026)
- **Herausgeber:** concerts.paris (rédaction), veröffentlicht über data.gouv.fr
- **Lizenz:** Creative Commons Attribution (CC BY 4.0) — auf data.gouv.fr als
  "Creative Commons Attribution" geführt, mit Verweis auf opendefinition.org
- **Formate:** CSV (1,4 Ko), XLSX (11,1 Ko), JSON (5,4 Ko)
- **Direkter CSV-Download:** [data.gouv.fr](https://www.data.gouv.fr/api/1/datasets/r/c9fda731-bd35-4d63-9906-14968a6f0067)

## Task 6 – Profile the dataset

### 1. Facts

| Feld | Wert |
|------|------|
| Titel | Baromètre du live parisien – concerts par arrondissement et par genre (été 2026) |
| Herausgeber | concerts.paris, veröffentlicht auf data.gouv.fr |
| Link | [data.gouv.fr](https://www.data.gouv.fr/datasets/barometre-du-live-parisien-concerts-par-arrondissement-et-par-genre-ete-2026) |
| Formate | CSV, XLSX, JSON |
| Größe | CSV 1,4 Ko · XLSX 11,1 Ko · JSON 5,4 Ko |
| Abdeckung | Paris intra-muros, 20 Arrondissements · Instantané vom 9. Juli 2026 |
| Letztes Update | 8. August 2026 (Datensatz-Metadaten: 2. November 2026) |
| Lizenz | CC BY 4.0 |

### 2. Stars

Bewertung nach dem 5-Sterne-Open-Data-Schema:

- ★ **Offen lizenziert** — CC BY 4.0, ausdrücklich als Open Definition
  konforme Lizenz verlinkt.
- ★ **Maschinenlesbar** — CSV und JSON, nicht nur PDF.
- ★ **Offenes Format** — CSV ohne proprietäre Bindung.
- ★ **URI zur Identifikation** — jede Zeile über den Arrondissement-Namen
  ansprechbar, der Datensatz selbst über eine stabile data.gouv.fr-URL.
- ✗ **Verknüpfte Daten (Linked Data)** — es fehlen URIs zu externen
  Referenzsystemen (z. B. Wikidata für Arrondissements oder Genre-Vokabulare).

**Fehlt für den fünften Stern:** RDF-Export bzw. verlinkte Konzepte.

### 3. Open the data

- **Werkzeug:** LibreOffice Calc
- **`concerts_total`:** min = 7 · max = 410 · mean = 128,9 (2 578 / 20)
- **`part_offre`:** min ≈ 0,3 % · max ≈ 15,9 % · mean = 5 %
- **Leere Zellen:** keine — die Summe der Genre-Spalten gleicht laut
  Datensatzbeschreibung exakt `concerts_total` auf jeder Zeile.
- **Auffälligkeiten:** Dezimaltrennzeichen ist in der CSV-Version der
  Punkt, in der französischen Excel-Version das Komma. Kodierung UTF-8,
  Umlaute/Akzente (z. B. "électro") korrekt. Einheiten: Anzahl Konzerte
  bzw. Prozent. 2 578 Konzerte über 20 Zeilen.

### 4. Data dictionary

| Spalte | Bedeutung | Typ | Einheit | Beispielwert |
|--------|-----------|-----|---------|--------------|
| `arrondissement` | Pariser Stadtbezirk | Text | – | 18e |
| `concerts_total` | Anzahl kommender Konzerte | Ganzzahl | Anzahl | 410 |
| `part_offre` | Anteil an der Pariser Angebotsmenge | Dezimal | Prozent | 15,9 |
| `rang` | Platzierung nach Konzertanzahl | Ganzzahl | Rang | 1 |
| `genre_dominant` | häufigstes Genre im Bezirk | Text | – | pop-rock indé |
| `pop_rock_indie` … `rock_metal` | je Genre: Anzahl Konzerte (8 Spalten) | Ganzzahl | Anzahl | 112 |
| `autres_genres` | seltene Genres und nicht klassierte Konzerte | Ganzzahl | Anzahl | 24 |

Dokumentation: Die Beschreibung auf data.gouv.fr erklärt jede Spalte und
stellt klar, dass die Genre-Spalten exakt `concerts_total` ergeben. Ein
formales Datenwörterbuch als eigene Datei gibt es nicht.

### 5. Licence

**Ist der Datensatz offen im Sinne der Open Definition? Ja.**

CC BY 4.0 erlaubt Nutzung, Weitergabe und Bearbeitung — auch kommerziell —
unter der einzigen Bedingung der Namensnennung. Der Datensatz ist auf
data.gouv.fr ausdrücklich als CC BY gelistet und verlinkt auf
opendefinition.org/licenses/cc-by.

**Was musst du tun, wenn du den Datensatz weiterverwendest:** Die
Quellenangabe anbringen, in dieser Form:

> Source : Baromètre du live parisien, concerts.paris, édition Été 2026.

**Attributionszeile (TASL):**

concerts.paris, "Baromètre du live parisien – concerts par arrondissement
et par genre (été 2026)", data.gouv.fr, CC BY 4.0,
[data.gouv.fr](https://www.data.gouv.fr/datasets/barometre-du-live-parisien-concerts-par-arrondissement-et-par-genre-ete-2026)

### 6. People

**Enthält der Datensatz personenbezogene Daten? Nein.**

Der Datensatz ist vollständig aggregiert: eine Zeile pro Arrondissement,
keine Venue-Namen, keine Veranstalter, keine Einzelpersonen, keine
Adressen. Es gibt also nichts zu anonymisieren.

**Auffälligkeiten:** Ein indirektes Re-Identifikationsrisiko besteht bei
kleinen Werten — ein Arrondissement mit sehr wenigen Konzerten und einem
dominanten Genre lässt sich theoretisch auf eine einzelne Location
eingrenzen. Für die Auswertung im Kurs ist das unerheblich, weil wir nur
die aggregierten Zahlen verwenden. Es werden keine Venue- oder
Personendaten ergänzt oder veröffentlicht.
