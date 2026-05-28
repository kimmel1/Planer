# Zahntechnik Fertigungsplaner

Web-App zur Planung von Fertigungsabschnitten in der Zahntechnik. Berechnet realistische Zeitpläne unter Berücksichtigung von Arbeitszeiten, Wochenenden und Feiertagen in Rheinland-Pfalz.

## Funktionen

### Produktionsplaner
- **Produktauswahl** für gängige Zahntechnik-Arbeiten:
  - Kronen/Brücken (glasiert/bemalt und verblendet)
  - Totalprothese (klassisch / mit Modellguss)
  - Inlay/Teilkrone
  - Aufbissschienen
  - Interims/ClearSplint
  - Teleskopierende Prothese
- **Zeitplanung** mit Startdatum und automatischer Berechnung aller Arbeitsschritte
- **Liefertermin** basierend auf dem letzten Fertigungsschritt
- **Produktspezifische Optionen** (z. B. Implantat, Verblendung, Modellguss, Teleskop-Varianten)
- **Bearbeitungsmodus** zum Anpassen der Arbeitsschritte pro Produkt

### Stammdaten (Katalog)
- Verwaltung von bis zu 200 Fertigungsabschnitten
- Kategorien: Manuell, Digital, Maschinell
- Zeitvorgaben in Tagen, Stunden und Minuten
- Suche, Sortierung und Bearbeitung des Katalogs

### Zeitlogik
- Arbeitszeiten: **Mo–Do 08:00–17:00**, **Fr 08:00–14:00**
- Keine Arbeit an Wochenenden
- Feiertage in **Rheinland-Pfalz** (Neujahr, Karfreitag, Ostermontag, Tag der Arbeit, Christi Himmelfahrt, Pfingstmontag, Fronleichnam, Tag der Deutschen Einheit, Allerheiligen, Weihnachten)

## Tech-Stack

- [React 19](https://react.dev/) + [TypeScript](https://www.typescriptlang.org/)
- [Vite 6](https://vite.dev/)
- [Tailwind CSS 4](https://tailwindcss.com/)
- [Motion](https://motion.dev/) (Animationen)
- [Lucide React](https://lucide.dev/) (Icons)

## Voraussetzungen

- [Node.js](https://nodejs.org/) 20 oder höher
- npm

## Installation & Start

```bash
# Repository klonen
git clone https://github.com/kimmel1/Planer.git
cd Planer

# Abhängigkeiten installieren
npm install

# Entwicklungsserver starten (http://localhost:3000)
npm run dev
```

## Skripte

| Befehl | Beschreibung |
|--------|--------------|
| `npm run dev` | Entwicklungsserver starten |
| `npm run build` | Produktions-Build erstellen |
| `npm run preview` | Build lokal testen |
| `npm run lint` | TypeScript-Prüfung |
| `npm run clean` | `dist/`-Ordner löschen |

## Projektstruktur

```
├── src/
│   ├── App.tsx       # Hauptanwendung (Planer + Katalog)
│   ├── main.tsx      # React-Einstiegspunkt
│   └── index.css     # Tailwind CSS
├── index.html
├── vite.config.ts
├── tsconfig.json
└── package.json
```

## Deployment

Nach `npm run build` liegt die fertige App im Ordner `dist/`. Dieser kann auf jedem Static-Host deployed werden, z. B.:

- [GitHub Pages](https://pages.github.com/)
- [Netlify](https://www.netlify.com/)
- [Vercel](https://vercel.com/)

Für GitHub Pages mit Vite ggf. `base: '/REPO-NAME/'` in `vite.config.ts` setzen.

## Lizenz

Apache License 2.0 – siehe [LICENSE](LICENSE).
