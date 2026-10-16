# Nazar Friseur: Designkonzept

Unverbindlicher Entwurf für eine neue Website von **Nazar Friseur** (vier Barbershops: Moosach, Stiglmaierplatz, Sendling, Oberhaching).
Keine offizielle Website des Betriebs. Alle Seiten sind für Suchmaschinen gesperrt (`noindex`), Buchen und Anrufen führen zu den echten Kanälen (Treatwell, Salonkee, Telefon).

Vorschau: https://kebronkg-cmyk.github.io/omer-layout-1/

## Aufbau
- `index.html`: Startseite mit 3D-Strähnen, Salon-Ring, Übersicht mit Stadtplan, Leistungen, Team, Einblicke
- `<salon>/index.html`: je Salon eine Seite mit Glasschrift, Öffnungszeiten, Route, Stadtplan, Schema.org `BarberShop`
- `hinweis/`: Hinweis zum Konzept, Quellen, Link zum Impressum des Betriebs

## Bauen
```
python3 tools/thema.py              # Markenfarbe (Neon-Türkis aus dem Leuchtschild) auf das Grunddesign
python3 tools/bilder.py <originale> # Fotos zuschneiden, WebP in mehreren Breiten
python3 tools/karten.py             # Stadtpläne aus OpenStreetMap
python3 tools/build.py              # Seiten aus tools/daten.json
```
Die 3D-Szenen (`tools/glas3d.src.js`, `tools/straehnen.src.js`) werden mit esbuild und three.js r170 nach `assets/js/` gebündelt.

## Offen, vom Betrieb bestätigen lassen
- Adresse Sendling (Waldfriedhofstr. 30, aus Instagram) und Postleitzahl Stiglmaierplatz (80333 oder 80335)
- Preise (nicht öffentlich), weitere Teamnamen und Zuordnung der Fotos zu den Salons
