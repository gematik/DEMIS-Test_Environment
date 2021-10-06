# DEMIS Docker TEST Umgebung

Die vollständige Anleitung finden Sie auf der DEMIS Wissensdatenbank:

[Informationen zur Docker Testumgebung](https://wiki.gematik.de/display/DSKB/Informationen+zur+Docker+Testumgebung)

______________________________________________________________________________________
## Release 1.1.0 

### Updated Images
- Configuration 1.1.0
- Notification API 1.9.0
- Notification Clearing API 1.9.0
- Postgres 1.8.2-configured-test

### Features
 - Verarbeitung der [neuen Profile]([https://simplifier.net/demis](https://simplifier.net/demis)): SARS-CoV-2, Influenza, Rotavirus
- Konfiguration der Server Adresse möglich, ausführliche Informationen sind hier zu finden
Image: `gematik1/demis/notification-clearing-api:1.9.0`
-- zusätzlicher `environment` Parameter: `HAPI_OIDC_ISSUER=https://localhost:7443/auth/realms/OEGD`
-- zusätzlicher `environment` Parameter: `HAPI_SERVER_ADDRESS=https://localhost:7443/notification-clearing-api/fhir/`
Image: `gematik1/demis/notification-api:1.9.0`
-- zusätzlicher `environment` Parameter: `HAPI_OIDC_ISSUER=https://localhost:7443/auth/realms/LAB`
**Bitte ersetzen Sie in allen drei Parametern `localhost:7443` mit Ihrer Server URL und Port. Fehler in der Konfiguration führen dazu, dass einzelne Komponenten nicht erreichbar sind!**

- Vorbespielte Postgres Datenbank mit [Beispielmeldungen](https://wiki.gematik.de/display/DSKB/Neue+Profilversionen)
Für jedes der 10 Test-Gesundheitsämter sind Beispielmeldungen enthalten, die die oben genannten unterstützten Profile darstellen.
-- image: `gematik1/demis/postgres:1.8.2-configured-test`
-- zusätzlicher `environment` Parameter: `PGDATA=demis_database`

- [DEMIS-Adapter 2.0.0](https://cloud.gematik.de/index.php/s/rbkGyg4XQyTyWzD) zur Unterstützung der neuen Profilversionen mit Beispiel LDT- und JSON-Dateien



______________________________________________________________________________________

## Kurzanleitung

- Docker installieren (s. [Installation DEMIS Testumgebung in Docker für Windows10](https://wiki.gematik.de/pages/viewpage.action?pageId=422118286))

- Starten der Umgebung mit: `docker-compose --file .\demis.yml up --detach`

- [DEMIS-Adapter Download](https://cloud.gematik.de/index.php/s/rbkGyg4XQyTyWzD)

- [DEMIS-Importer Download](https://cloud.gematik.de/index.php/s/rbkGyg4XQyTyWzD)

- Meldung mit DEMIS-Adapter senden

- Meldung mit DEMIS-Importer abholen

- Beenden der Umgebung mit: `docker-compose --file .\demis.yml down -v`