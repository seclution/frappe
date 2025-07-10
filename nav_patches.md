# Patches Navigation

Prompt:

```
Versionsaktualisierungen werden über Dateien in `frappe/patches` und der
Liste `frappe/patches.txt` gesteuert. Patches liegen in den
Versionsordnern wie `frappe/patches/v16_0` und enthalten jeweils eine
`execute()`-Funktion. Die Ausführung übernimmt
`frappe/modules/patch_handler.py`, welcher ausgeführte Skripte im DocType
`Patch Log` unter `frappe/core/doctype/patch_log` vermerkt. Migrationsabläufe
nutzen `frappe/migrate.py`; einzelne Patches lassen sich über den CLI-Befehl
`run-patch` in `frappe/commands/site.py` starten. Prüfhilfen befinden sich in
`frappe/tests/test_patches.py`.
```
