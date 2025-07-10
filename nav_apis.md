# APIs Navigation

Prompt:

```
Um Endpunkte oder RPC-Methoden zu verstehen, sieh dir zuerst
`frappe/api/__init__.py` an. Dort werden die Routen `/api/method` und
`/api/resource` sowie die Versionen `v1` und `v2` registriert.

REST-Funktionen liegen in `frappe/api/v1.py` und `frappe/api/v2.py`. Für
Dateioperationen findest du APIs unter `frappe/core/api/file.py`. Die
generischen CRUD-Methoden für `/api/resource` sind in `frappe/client.py`
implementiert, während Aufrufe über `/api/method` in `frappe/handler.py`
landen.

Suche zusätzlich in den Modulen nach Funktionen mit dem Dekorator
`@frappe.whitelist`, um weitere freigegebene RPC-Methoden zu finden. Öffne nur
die relevanten Funktionsdefinitionen, um den Kontext kompakt zu halten. Beispiele
für API-Aufrufe findest du in `frappe/tests/test_api.py` und
`frappe/tests/test_api_v2.py`.
```
