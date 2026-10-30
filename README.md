# Ausflugsgarten Kreuzlingen & Konstanz

Ein Digital Garden mit Ausflugsideen für Besucher in Kreuzlingen und Konstanz, gebaut mit [Quartz 5](https://quartz.jzhao.xyz/).

Live: https://stpaulifan.github.io

## Inhalte bearbeiten

Alle Inhalte liegen als Markdown in `content/`:

- `content/aktivitaeten/` – eine Notiz pro Aktivität
- `content/wanderungen/` – eine Notiz pro Wanderung
- `content/tags/` – Einleitungstexte der Kategorien
- `content/bilder/` – Bilder (WebP, max. 1200 px), eingebunden mit `![Alt](/bilder/name.webp)`
- `content/templates/` – Vorlagen für neue Notizen (werden nicht veröffentlicht)

Die Kategorien sind Tags im Frontmatter. Eine Notiz erscheint automatisch in jeder Kategorie, deren Tag sie trägt:

| Tag              | Kategorie         |
| ---------------- | ----------------- |
| `schlechtwetter` | 🌧️ Schlechtwetter |
| `gutwetter`      | ☀️ Gutwetter      |
| `kinder`         | 🧒 Mit Kindern    |
| `wanderung`      | 🥾 Wanderungen    |

Der Ordner `content/` lässt sich auch direkt als Obsidian-Vault öffnen.

## Lokal ansehen

```sh
npm ci
npx quartz build --serve   # http://localhost:8080
```

## Veröffentlichen

Jeder Push auf `main` baut die Seite per GitHub Actions (`.github/workflows/deploy.yml`) und veröffentlicht sie auf GitHub Pages.
Einmalig nötig: Repo-Einstellungen → Pages → Source: **GitHub Actions**.

Einstellungen (Titel, Farben, Plugins) stehen in `quartz.config.yaml`.
