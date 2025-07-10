# Database / Query Builder Navigation

Prompt:

```
Um Datenbank-Operationen oder den Query Builder zu verstehen, sieh dir die Module unter `frappe/database` an.

- `database.py` implementiert die zentrale `Database`-Klasse mit CRUD-APIs.
- `query.py` stellt den Query Builder `Engine` bereit und verarbeitet Filter sowie Felder.
- `schema.py` definiert Klassen und Utilities zur Schema-Verwaltung.
- `db_manager.py` bietet Hilfsfunktionen zur Einrichtung und Wartung von Datenbanken.
- `mariadb/` und `postgres/` enthalten die jeweiligen Dialekt-Implementierungen.
- `operator_map.py` übersetzt Filteroperatoren.
- `__init__.py` stellt Einstiegspunkte wie `get_db()` bereit.

Lade nur die benötigten Dateien oder Funktionsausschnitte, um den Kontext kompakt zu halten.
```
