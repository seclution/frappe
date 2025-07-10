# Frappe Repository Navigation

Dieses Dokument fasst die Navigation aus `nav.md` sowie aus allen `nav_<topic>.md` Dateien zusammen. Es dient als zentrale Einstiegshilfe für KI-gestützte Entwicklung.

## nav.md
# Repository Navigation

This repository contains the core code of the **Frappe Framework**. Use the navigation files listed below to gather context for specific topics when developing a Frappe application.

- [Doctypes](nav_doctypes.md)
- [APIs](nav_apis.md)
- [Emails](nav_emails.md)
- [Websites](nav_websites.md)
- [Permissions](nav_permissions.md)
- [Fixtures](nav_fixtures.md)
- [Hooks](nav_hooks.md)
- [Integrations](nav_integrations.md)
- [Patches](nav_patches.md)
- [Translations](nav_translations.md)
- [Reports](nav_reports.md)
- [Printing](nav_printing.md)
- [Themes](nav_themes.md)
- [Webforms](nav_webforms.md)
- [Database](nav_database.md)
- [Scheduled Tasks](nav_scheduled.md)
- [Search](nav_search.md)
- [CLI Commands](nav_commands.md)
- [Workflows](nav_workflows.md)

Each `nav_<topic>.md` file contains prompt templates and directory hints so you can load only the necessary code in context.


## nav_apis.md
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


## nav_commands.md
# CLI Commands Navigation

Prompt:

```
Die verschiedenen Kommandozeilenbefehle des Frappe Frameworks befinden sich im Verzeichnis `frappe/commands`.
Relevante Dateien sind unter anderem:
- `__init__.py` (Command-Gruppen und gemeinsame Optionen)
- `gettext.py` (Übersetzungswerkzeuge)
- `redis_utils.py` (Redis-Hilfen)
- `scheduler.py` (Scheduler-Steuerung)
- `site.py` (Site- und Installationsbefehle)
- `translate.py` (Datenübersetzung)
- `utils.py` (allgemeine Helferfunktionen)

Öffne nur die nötigen Funktionsdefinitionen oder Click-Kommandos, um den Kontext schlank zu halten.
```


## nav_database.md
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


## nav_doctypes.md
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


## nav_emails.md
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


## nav_fixtures.md
# Fixtures Navigation

Prompt:

```
Beispiel- und Testdaten findest du in
`frappe/custom/fixtures`, `frappe/core/doctype/data_import/fixtures`
und `cypress/fixtures` (inklusive Anhänge für E2E-Tests).
Python-Hilfen zum Import/Export liegen in `frappe/utils/fixtures.py`.
Tests dazu sind unter `frappe/tests/test_fixture_import.py` und
`frappe/tests/test_exporter_fixtures.py` zu finden. Der Setup Wizard
nutzt `frappe/desk/page/setup_wizard/install_fixtures.py`.
Eigene Fixtures speicherst du im App-Verzeichnis `fixtures`.
Lade nur die benötigten Dateien, um den Kontext klein zu halten.
```


## nav_hooks.md
# Hooks Navigation

Prompt:

```
Zentrale Hook-Einstellungen des Frameworks liegen in `frappe/hooks.py` im
Wurzelverzeichnis. Dort findest du Keys wie `doc_events`, `scheduler_events`,
`permission_query_conditions`, `has_permission`, `jinja` oder
`override_whitelisted_methods`. Eigene Apps besitzen im jeweiligen
App-Ordner ebenfalls eine `hooks.py`. Öffne bei Bedarf nur die relevanten
Abschnitte aus diesen Dateien. Eine Übersicht aller möglichen Hook-Keys steht
in `hooks.md`.
```


## nav_integrations.md
# Integrations Navigation

Prompt:

```
Die wichtigsten Integrationsmodule liegen unter `frappe/integrations`.
Schlüsseldateien sind:
- `__init__.py`
- `doctype/` mit verschiedenen Integration-DocTypes
- `frappe_providers/` mit Hilfsfunktionen für FrappeCloud
- `google_oauth.py` für OAuth-Anbindung an Google
- `oauth2.py` als generischer OAuth2-Server

Sieh dir bei Fragen zu Integrationen nur die benötigten Module in diesem
Verzeichnis an, um den Kontext klein zu halten.
```


## nav_patches.md
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


## nav_permissions.md
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


## nav_printing.md
# Printing Navigation

Prompt:

```
Quellcode zu Druckfunktionen und Print-Formaten liegt im Verzeichnis `frappe/printing`.

- `__init__.py` initialisiert das Modul
- `doctype/` enthält DocTypes wie `print_format`, `print_settings` oder `letter_head`
- `form_tour/` liefert geführte Touren zu Druck-Doctypes
- `page/` umfasst Seiten wie `print` und `print_format_builder`
- `print_style/` bietet CSS-Themes für Drucklayouts

Suche bei Aufgaben rund um Print-Formate in diesen Ordnern nach den relevanten Dateien und öffne nur die benötigten Ausschnitte.
```


## nav_reports.md
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


## nav_scheduled.md
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


## nav_search.md
# Search Navigation

Prompt:

```
Suche-Funktionen liegen im Modul `frappe/search`.
Verschaffe dir zuerst einen Überblick in `frappe/search/__init__.py`, dort ist `web_search` als Whitelist-Methode verfügbar.

Die Basisklasse `FullTextSearch` befindet sich in `frappe/search/full_text_search.py`.
Website-spezifische Suche wird mit `WebsiteSearch` in `frappe/search/website_search.py` umgesetzt.
Beispiele und Tests findest du in `frappe/search/test_full_text_search.py`.

Öffne nur die relevanten Klassendefinitionen und Methoden, um den Kontext übersichtlich zu halten.
```


## nav_themes.md
# Themes Navigation

Prompt:

```
Um das Erscheinungsbild anzupassen, sieh dir zuerst die DocType `website_theme` unter `frappe/website/doctype/website_theme` und zugehörige Templates in `frappe/website/website_theme` an. SCSS-Dateien für Website und Desk liegen unter `frappe/public/scss/website` bzw. `frappe/public/scss/desk`. Der Wechsel zwischen hellen und dunklen Themes erfolgt über `frappe/public/js/frappe/ui/theme_switcher.js`.

Eigene Bootstrap-Themes kannst du mit `generate_bootstrap_theme.js` erstellen. Weitere Beispiele findest du in `frappe/templates/includes/website_theme`. Lade nur die benötigten Dateien, um den Kontext schlank zu halten.
```


## nav_translations.md
# Translations Navigation

Prompt:

```
Die Übersetzungsdateien befinden sich im Verzeichnis `frappe/translations`.
Jede CSV-Datei enthält Paare aus englischem Originaltext und der jeweiligen
Übersetzung. Beispiele für Sprachdateien sind:
- `af.csv`
- `am.csv`
- `bg.csv`
- `bn.csv`
- `ca.csv`

Zum Laden und Zusammenführen von Übersetzungen nutzt das Framework Funktionen
in `frappe/translate.py`, etwa `get_all_translations` oder
`get_app_translations`. Öffne nur die relevanten Dateien oder
Funktionsabschnitte, um den Kontext knapp zu halten.
```


## nav_webforms.md
# Webforms Navigation

Prompt:

```
Webforms und ihre Definitionen befinden sich an mehreren Stellen im Repository:

- Die DocType-Grundlage liegt in `frappe/website/doctype/web_form` mit Templates im Unterordner `templates`. Begleitende Doctypes wie `web_form_field` und `web_form_list_column` findest du ebenfalls hier.
- Vorgefertigte Webforms liegen unter `frappe/website/web_form` sowie `frappe/core/web_form`. Jeder Ordner enthält `<name>.json`, `<name>.py` und optional `<name>.js`.
- Clientseitige Scripts und Styles findest du unter `frappe/public/js/frappe/web_form` bzw. `frappe/public/scss`.
- Tests und Beispielseiten liegen in `frappe/tests/test_webform.py` und `frappe/www/_test/_test_webform.py`.

Suche bei Aufgaben zum Thema Webform in diesen Verzeichnissen nach der passenden Datei und lade nur den relevanten Ausschnitt, um den Kontext fokussiert zu halten.
```


## nav_websites.md
# Websites Navigation

Prompt:

```
Um Website-Funktionen zu bearbeiten, öffne die Seiten unter `frappe/www` (HTML und Python).
Weitere Module findest du in `frappe/website`:
- `doctype/` für Web-bezogene DocTypes wie `web_page`, `blog_post` oder `website_theme`.
- `page_renderers/` und `router.py` regeln Rendering und Routing.
- `web_template/` enthält wiederverwendbare Website-Templates.
- `website_theme/` sowie `public/scss/website` definieren das Styling.

Statische Assets liegen in `frappe/public`, Templates in `frappe/templates` und Unterordnern.
Lade nur die jeweils benötigten Dateien, um den Kontext schlank zu halten.
```


## nav_workflows.md
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

