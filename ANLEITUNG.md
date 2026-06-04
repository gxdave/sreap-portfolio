# SREAP Website – Anleitung

## Zugang teilen

Das aktuelle Passwort ist: **SREAP2026**

Um das Passwort zu ändern: `index.html` öffnen, Zeile suchen:
```
const ACCESS_CODE = 'SREAP2026';
```
Wert ersetzen, Datei speichern.

---

## Neues Asset hinzufügen

1. Datei `assets.json` öffnen (mit Texteditor oder Claude)
2. Neuen Eintrag **ganz oben** in die eckige Klammer `[` einfügen:

```json
{
  "id": "XYZ-001",
  "dateAdded": "2026-06-10",
  "title": "Zürich – Wohnhaus Seeblick",
  "location": "Zürich, Switzerland",
  "category": "Residential",
  "salePrice": 9500000,
  "currency": "CHF",
  "yield": 3.8,
  "netRentalIncome": 361000,
  "details": [
    "12 Wohnungen",
    "Vollrenoviert 2023",
    "Direkter Seezugang"
  ],
  "tags": ["Zürich", "Residential", "Seeblick"]
},
```

3. Datei speichern → Asset erscheint automatisch **ganz oben** auf der Webseite

### Pflichtfelder:
- `id` – eindeutige ID (z.B. "ZRH-001")
- `dateAdded` – Datum im Format YYYY-MM-DD
- `title` – Bezeichnung
- `location` – Ort
- `category` – Eines von: Mixed-Use, Residential, Development, Portfolio, Commercial

### Optionale Felder:
- `salePrice` – Kaufpreis in CHF (Zahl ohne Anführungszeichen)
- `investmentVolume` – Investitionsvolumen (falls kein salePrice)
- `yield` – Rendite als Zahl (z.B. 4.8 für 4.8%)
- `grossYield` – Bruttorendite
- `yieldPotential` – Potenzielle Rendite
- `netRentalIncome` – Jahresnettomiete
- `annualRentalIncome` – Jahresmiete
- `details` – Liste mit Details (Array von Strings)
- `tags` – Tags für Filter/Suche

---

## Kategorien
- `Mixed-Use` – Gemischte Nutzung
- `Residential` – Wohnliegenschaften
- `Development` – Entwicklungsprojekte
- `Portfolio` – Portfolios
- `Commercial` – Reine Gewerbeobjekte

---

## Neue Assets hervorheben
Assets die in den letzten 7 Tagen hinzugefügt wurden (`dateAdded`) erhalten automatisch:
- Goldenen Rahmen
- "NEU" Badge
- Erscheinen ganz oben auf der Seite

