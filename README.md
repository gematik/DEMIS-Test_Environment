<img align="right" width="250" height="47" src="image/Gematik_Logo_Flag.png"/> <br/> 
<div align="center" style="border: 1px solid #dee2e6; padding: 20px; background-color: #3d98ef;">
    <h1 style="color: #ff001b;">Project Status</h1>
    <p style="color: #000000;">This project is no longer being developed.</p>
    <p style="color: #000000;">A new project will be available in the future!</p>
</div>

<details>
  <summary>Table of Contents</summary>
  <ol>
    <li>
      <a href="#about-the-project">About The Project</a>
       <ul>
        <li><a href="#documentation">Documentation</a></li>
        <li><a href="#release-notes">Release Notes</a></li>
      </ul>
	</li>
    <li><a href="#getting-started">Getting Started</a></li>
    <li><a href="#fhir-interfaces">FHIR-Interfaces</a></li>
    <li><a href="#contributing">Contributing</a></li>
    <li><a href="#license">License</a></li>
    <li><a href="#contact">Contact</a></li>
  </ol>
</details>
<details>
  <summary>Table of Contents</summary>
  <ol>
    <li>
      <a href="#about-the-project">About The Project</a>
       <ul>
        <li><a href="#documentation">Documentation</a></li>
        <li><a href="#release-notes">Release Notes</a></li>
      </ul>
	</li>
    <li><a href="#getting-started">Getting Started</a></li>
    <li><a href="#fhir-interfaces">FHIR-Interfaces</a></li>
    <li><a href="#contributing">Contributing</a></li>
    <li><a href="#license">License</a></li>
    <li><a href="#contact">Contact</a></li>
  </ol>
</details>

# DEMIS Docker TEST Environment

## About The Project

This is a Docker-based Test environment for the Deutschen Elektronischen Melde- und Informationssystem für den Infektionsschutz (DEMIS).

### Documentation

The complete Documentation can be found in the DEMIS Knownledge Base (in German):

[Informationen zur DEMIS Docker Testumgebung](https://wiki.gematik.de/display/DSKB/Informationen+zur+DEMIS+Docker+Testumgebung)

### Release Notes

See [ReleaseNotes.md](./ReleaseNotes.md) for all information regarding the (newest) releases.
______________________________________________________________________________________

## Getting Started

- Install Docker (s. [Installation DEMIS Testumgebung in Docker für Windows10](https://wiki.gematik.de/pages/viewpage.action?pageId=422118286))

- Start the environment: `docker compose --project-name demis --file demis.yml up --detach`

- Download the [DEMIS-Adapter](https://nexus.prod.ccs.gematik.solutions/repository/DEMIS/adapter/DEMIS-Adapter-2.0.1.zip)

- Download the [DEMIS-Importer](https://nexus.prod.ccs.gematik.solutions/repository/DEMIS/importer/DEMIS-Importer.zip)

- Send Messages with the DEMIS-Adapter

- Receive Messages with DEMIS-Importer

- Stop the environment: `docker compose --project-name demis --file demis.yml down -v`

______________________________________________________________________________________

## FHIR-Interfaces

- Postman Collection: FHIR-Schnittstelle/DDTU_postman_collection.json

- [Documentation for the Postman Collection (German)](https://wiki.gematik.de/display/DSKB/Informationen+zur+DEMIS+Docker+Testumgebung#InformationenzurDEMISDockerTestumgebung-FHIRSchnittstelle-Postman-Collection)

## Contributing

If you want to contribute, please check our [CONTRIBUTING.md](./CONTRIBUTING.md).

## License

EUROPEAN UNION PUBLIC LICENCE v. 1.2

EUPL © the European Union 2007, 2016

See [LICENSE](./LICENSE).

## Contact

E-Mail to [DEMIS Entwicklung](mailto:demis-entwicklung@gematik.de?subject=[GitHub]%20DDTU)
