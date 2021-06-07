DEMIS
This project includes the Docker Compose files for DEMIS. 

Currently supported environments: 
- demis.yml --> TEST
- demis-dev.yml --> DEV
- demis-local.yml --> local nginx and keycloak

Docker.exe has to be installed! 

For startup:
docker-compose --file .\demis.yml up

For shutdown:
docker-compose --file .\demis.yml down -v
