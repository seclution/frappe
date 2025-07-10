# Workflows Navigation

Prompt:

```
Workflows steuern mehrstufige Freigabeprozesse fuer Dokumente.
Der zugehoerige Code liegt unter `frappe/workflow/doctype`:
- `workflow` als zentrales Workflow-DocType
- `workflow_action` und `workflow_action_master` fuer moegliche Aktionen
- `workflow_action_permitted_role` legt Rollenrechte fest
- `workflow_document_state` und `workflow_state` beschreiben Zustaende
- `workflow_transition` definiert die moeglichen Uebergaenge
Die Oberflaeche zum Erstellen findest du in
`frappe/workflow/page/workflow_builder`.
Lade nur die benoetigten Dateien wie `.py`, `.json` oder Tests,
um den Kontext schlank zu halten.
```
