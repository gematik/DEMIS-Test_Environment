### DEMIS Docker TEST Umgebung ###

Die vollständige Anleitung finden Sie auf der DEMIS Wissensdatenbank: 
https://wiki.gematik.de/display/DSKB/DEMIS+Docker+TEST+Umgebung


Kurzanleitung: 
- Docker installieren 
- Starten der Umgebung mit: 
    docker-compose --file .\demis.yml up --detach 
- DEMIS-Adapter Download von https://cloud.gematik.de/index.php/s/rbkGyg4XQyTyWzD
- DEMIS-Importer Download von https://cloud.gematik.de/index.php/s/rbkGyg4XQyTyWzD
- Meldung mit DEMIS-Adapter senden
- Meldung mit DEMIS-Importer abholen
- Beenden der Umgebung mit: 
    docker-compose --file .\demis.yml down -v