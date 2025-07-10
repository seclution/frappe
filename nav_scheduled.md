# Scheduled Tasks Navigation

Prompt:

```
Geplante Aufgaben laufen über `frappe/utils/scheduler.py`. Dort findest du
Funktionen wie `enqueue_events` oder `is_scheduler_inactive`.
Die konkreten Events sind im Dictionary `scheduler_events` in
`frappe/hooks.py` hinterlegt und werden bei Bedarf als
`Scheduled Job Type` unter `frappe/core/doctype/scheduled_job_type` erzeugt.
Protokolle findest du im `Scheduled Job Log` unter
`frappe/core/doctype/scheduled_job_log`.
Server Scripts vom Typ „Scheduler Event" erstellen Jobs über
`frappe/core/doctype/server_script/server_script.py`.
Der CLI-Einstiegspunkt liegt in `frappe/commands/scheduler.py`.
Weitere Statusinformationen liefert der `System Health Report` unter
`frappe/desk/doctype/system_health_report`.
Um einen bestimmten Job zu untersuchen, suche nach seinem Methodennamen in
diesen Dateien und lade nur die relevanten Funktionsdefinitionen.
```
