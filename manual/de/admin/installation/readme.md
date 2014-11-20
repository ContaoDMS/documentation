# Installation

Die Erweiterung [DokManSystem] kann in der Contao Erweiterungsverwaltung im Backend installiert werden.

→ System → Erweiterungsverwaltung → Erweiterung installieren → Eingabe: DokManSystem

Für die manuelle Installation, können die benötigten Dateien hier heruntergeladen werden:

http://www.contao.org/de/extension-list/view/DokManSystem.html 

Anschließend steht dem Administrator das Modul "DMS" mit den Werkzeugen: 

Kategorien, Zugriffsrechte, Dokumente (und Dateityp-Sets) zur Verfügung.


## Serverkonfiguration

Unter Umständen muss man eine eigene `php.ini` ins Web-ROOT der Installation legen um z.B. Arbeitsspeicher Limits oder Ausführungszeiten zu definieren. Sind diese zur gering kann es vorkommen, dass größere Dateien nicht hochgeladen werden können.

Ein Beispiel für den Inhalt einer solchen `php.ini` Datei sieht wie folgt aus:

```
# increase memory limits and execution time
upload_max_filesize = 5M
memory_limit = 512M
max_execution_time = 50000
post_max_size = 40M
```