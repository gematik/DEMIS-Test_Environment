# DEMIS Docker TEST Umgebung

Die vollständige Anleitung finden Sie auf der DEMIS Wissensdatenbank:

[Informationen zur DEMIS Docker Testumgebung](https://wiki.gematik.de/display/DSKB/Informationen+zur+DEMIS+Docker+Testumgebung)

______________________________________________________________________________________

## Kurzanleitung

- Docker installieren (s. [Installation DEMIS Testumgebung in Docker für Windows10](https://wiki.gematik.de/pages/viewpage.action?pageId=422118286))

- Starten der Umgebung mit: `docker-compose --file .\demis.yml up --detach`

- [DEMIS-Adapter Download](https://nexus.prod.ccs.gematik.solutions/repository/DEMIS/adapter/DEMIS-Adapter-2.0.1.zip)

- [DEMIS-Importer Download](https://nexus.prod.ccs.gematik.solutions/repository/DEMIS/importer/DEMIS-Importer.zip)

- Meldung mit DEMIS-Adapter senden

- Meldung mit DEMIS-Importer abholen

- Beenden der Umgebung mit: `docker-compose --file .\demis.yml down -v`

______________________________________________________________________________________

## FHIR-Schnittstelle

- Postman Collection: FHIR-Schnittstelle/DDTU_postman_collection.json

- [Dokumentation zur Postman Collection](https://wiki.gematik.de/display/DSKB/Informationen+zur+DEMIS+Docker+Testumgebung#InformationenzurDEMISDockerTestumgebung-FHIRSchnittstelle-Postman-Collection)