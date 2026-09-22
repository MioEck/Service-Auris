# Service Auris

Kleine Wartungs-App für den Toyota Auris. Läuft im Browser über GitHub Pages und speichert alle Einträge als `data.json` in diesem Repository.

## Einrichten

1. **GitHub Pages aktivieren:** Repository → *Settings* → *Pages* → *Source: Deploy from a branch* → Branch `main`, Ordner `/ (root)` → *Save*.
   Danach ist die App erreichbar unter `https://mioeck.github.io/Service-Auris/`.
2. **Token erstellen (einmalig pro Gerät):** GitHub → *Settings* → *Developer settings* → *Personal access tokens* → *Fine-grained tokens* → *Generate new token*
   - Repository access: *Only select repositories* → `Service-Auris`
   - Permissions → *Contents*: **Read and write**
3. In der App unter **Einstellungen → Speichern auf GitHub** den Token eintragen und auf *Verbinden & laden* tippen.

Ab dann wird jede Änderung automatisch als Commit in `data.json` gespeichert.

## Funktionen

- Service eintragen: Datum, Kilometerstand, erledigte Arbeiten (Öl, Ölfilter, Luftfilter innen/außen, Kühlwasser, …), Werkstatt, Kosten, Notiz
- Automatische Berechnung, wann jede Arbeit wieder fällig ist (km **oder** Monate – was zuerst eintritt; Standard 15.000 km / 12 Monate, in den Einstellungen änderbar)
- Übersicht mit nächstem Service und Status (OK / Bald fällig / Fällig)
- Historie mit Bearbeiten/Löschen
- Kennzeichen und Modell im Kopf
- Export/Import als JSON-Datei

**Hinweis:** Das Repository ist öffentlich – damit ist auch `data.json` (Kennzeichen, Kilometerstände) öffentlich lesbar.
