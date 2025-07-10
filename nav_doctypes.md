# Doctypes Navigation

Dieses Dokument bietet einen schnellen Überblick, wo DocType-Definitionen und zugehöriger Code im Repository liegen.

## Verzeichnisse
DocTypes befinden sich in Unterordnern namens `doctype` in verschiedenen Modulen. Häufig genutzte Pfade sind u. a.:

- `frappe/core/doctype`
- `frappe/desk/doctype`
- `frappe/website/doctype`
- `frappe/email/doctype`
- `frappe/custom/doctype`
- `frappe/contacts/doctype`
- `frappe/automation/doctype`
- `frappe/social/doctype`
- `frappe/geo/doctype`
- `frappe/printing/doctype`
- `frappe/integrations/doctype`
- `frappe/workflow/doctype`
- `frappe/core/form_tour/doctype`
- `frappe/public/js/frappe/doctype` (Client‑seitige Hilfen)

Die Basisklassen findest du unter `frappe/model/document.py` und `frappe/model/base_document.py`.

## Aufbau eines DocType-Verzeichnisses
Ein DocType umfasst typischerweise folgende Dateien:

- `<DocType>.json` – Felddefinitionen und Einstellungen
- `<DocType>.py` – serverseitige Logik
- optional `<DocType>.js` – clientseitige Logik
- optionale weitere Ressourcen wie `<DocType>.md`, Test- oder Patch-Verzeichnisse

Prompt:
```
Analysiere oder erstelle einen DocType. Suche im Repository nach `frappe/**/doctype/<DocType>` und öffne die genannten Dateien. Fasse anschließend die relevanten Abschnitte prägnant zusammen.
```
