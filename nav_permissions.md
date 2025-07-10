# Permissions Navigation

Prompt:

```
Um Berechtigungen zu verstehen, lies zuerst `frappe/permissions.py`. Dort
befinden sich Kernfunktionen wie `has_permission`, `get_doc_permissions` und
`get_role_permissions`. Viele DocTypes haben eigene Hooks wie
`get_permission_query_conditions` oder `has_permission`; Beispiele findest du in
`frappe/core/doctype/file/file.py` oder
`frappe/core/doctype/prepared_report/prepared_report.py`.

Rollen- und Rechte-Definitionen liegen unter `frappe/core/doctype` in den
Ordnern:

- `docperm` und `custom_docperm` für Standard- und benutzerdefinierte
  DocType-Rechte
- `user_permission` für dokumentbezogene Einschränkungen
- `role`, `has_role` und `role_profile` für Rollenverwaltung
- `role_permission_for_page_and_report` für Seiten- und Berichtrechte

Öffne bei Bedarf die jeweiligen JSON- oder Python-Dateien und lade nur die
relevanten Abschnitte, um den Überblick kompakt zu halten.
```
