# Emails Navigation

Prompt:

```
Um das E-Mail-System zu verstehen, sieh dir das Paket `frappe/email` an.
Wichtige Dateien und Ordner sind:
- `__init__.py` mit Hilfsfunktionen wie `sendmail_to_system_managers` und RPCs.
- `email_body.py` für die Erstellung der MIME-Nachrichten.
- `doctype/` enthält DocTypes wie `email_queue` oder `email_account`, die Versand
  und Empfang steuern.
- `assets/` bietet Bilder und weitere Ressourcen für E-Mail-Templates.
- `email.md` erläutert die Architektur des gesamten Moduls.
Bei Bedarf findest du in `queue.py`, `receive.py` und `smtp.py` weitere
Funktionen für das Abrufen und Versenden von Nachrichten. Lade jeweils nur die
relevanten Funktionsdefinitionen, um den Kontext kompakt zu halten.
```
