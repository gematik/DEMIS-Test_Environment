# DEMIS Docker TEST Umgebung

Die vollständige Anleitung finden Sie auf der DEMIS Wissensdatenbank:

[Informationen zur DEMIS Docker Testumgebung](https://wiki.gematik.de/display/DSKB/Informationen+zur+DEMIS+Docker+Testumgebung)

______________________________________________________________________________________

## Kurzanleitung

- Docker installieren (s. [Installation DEMIS Testumgebung in Docker für Windows10](https://wiki.gematik.de/pages/viewpage.action?pageId=422118286))

- Starten der Umgebung mit: `docker-compose --file .\demis.yml up --detach`

- [DEMIS-Adapter Download](https://cloud.gematik.de/index.php/s/rbkGyg4XQyTyWzD)

- [DEMIS-Importer Download](https://cloud.gematik.de/index.php/s/rbkGyg4XQyTyWzD)

- Meldung mit DEMIS-Adapter senden

- Meldung mit DEMIS-Importer abholen

- Beenden der Umgebung mit: `docker-compose --file .\demis.yml down -v`