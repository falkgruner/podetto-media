# podetto-media

Öffentliche Ablage für fertige Grafiken von Podetto, vor allem für Social Media (Buffer, Instagram).
Ausgeliefert über Cloudflare Pages unter **https://media.podetto.de** (kein Build-Schritt).

Hier liegen nur fertige, veröffentlichte Grafiken. Keine Entwürfe, keine Fotos von Personen, keine personenbezogenen Daten.

## Ordner

| Ordner | Inhalt |
|---|---|
| `social/hoertipps/` | Hörtipp-Grafiken |
| `social/eltern-alltag/` | Beiträge zum Familienalltag |
| `social/changelog/YYYY/` | Grafiken zu Neuigkeiten, nach Jahr |

## Dateinamen

- nur Kleinbuchstaben, Ziffern und Bindestriche, keine Leerzeichen, keine Umlaute (ä → ae, ö → oe, ü → ue, ß → ss)
- fortlaufende Nummer mit zwei Stellen: `hoertipp-01.png`, `hoertipp-02.png`
- Changelog mit Datum: `social/changelog/2026/2026-11-17-elternbereich.png`
- Formate: `.png`, `.jpg`, `.webp` (Video: `.mp4`)

## Wichtig: Dateien nicht überschreiben

Bilder werden ein Jahr lang im Browser und bei Cloudflare zwischengespeichert (`immutable`).
Eine geänderte Grafik bekommt deshalb einen neuen Namen, zum Beispiel `hoertipp-01-v2.png`.

## Adresse einer Datei

`social/hoertipps/hoertipp-01.png` → `https://media.podetto.de/social/hoertipps/hoertipp-01.png`

## Technik

- `_headers`: Content-Type je Bildformat, langes Caching, `noindex`
- `index.html` und `404.html`: leer, `noindex` (kein Verzeichnis-Listing; fehlende Dateien liefern 404)
- `robots.txt`: Suchmaschinen ausgeschlossen
