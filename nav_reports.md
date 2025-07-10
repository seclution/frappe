# Reports Navigation

Prompt:

```
Berichte des Frameworks liegen unter `frappe/core/report`. Dort findest du folgende Unterordner:
- `database_storage_usage_by_tables`
- `document_share_report`
- `permitted_documents_for_user`
- `prepared_report_analytics`
- `transaction_log_report`

Jeder Ordner enthält die Dateien `<name>.py`, `.js` und `.json` mit der Logik und den Felddefinitionen des jeweiligen Reports. Die zentrale `__init__.py` im Ordner `report` liefert keine weitere Funktionalität.

Öffne für Analysen oder Anpassungen nur die relevanten Dateien aus diesen Verzeichnissen, um den Kontext klein zu halten.
```
