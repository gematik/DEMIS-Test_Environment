<img align="right" width="200" height="37" src="image/Gematik_Logo_Flag.png"/> <br/>

# Release notes DEMIS-Test-Environment

### Release 2.2.0 (2023-08-07)
- Added latest RKI Profiles for rki.demis.r4.core-1.23.1-rc1

### Release 2.1.0 (2023-06-28)
- Added latest RKI Profiles 1.23.0.alpha3
- Removed DV1 Profiles
- Added QR Code in the PDF Receipt
- Update of Services
- Updated Postman Collection for the Docker Test Environment
- Updated License

### Release 2.0.2 (2023-04-25)
- Quality enhancements
- Deprecation of DV1 Profiles
- InEK got updated
 
### Release 2.0.1 (2023-03-10)
- demis-configuration
  - update
- Hospital-Location-Service
  - quality enhancement
- Report-Processing-Service
  - quality enhancement
- Validation-Service
  - quality enhancement
- PDFgen-Service
  - quality enhancement

### Release 2.0.0 (2023-02-13)

### fixed/update
- hospital-location-service
  - bugfix
  - InEK got updated
- report-processing-service
  - bugfix

### security
- change notification-clearing-api
  - quality enhancement
- change pdfgen-service
  - quality enhancement
- change postgresql
  - quality enhancement
- change report-processing-service
  - quality enhancement

## Release 1.5.2 (2022-09-21)

### fixed
- country code for germany was removed from pdf receipt
- database update with InEK data


## Release 1.5.1 (2022-09-15)

### fixed
- truncated zip code with leading "0"


## Release 1.5.0 (2022-09-13)

Activation of the FHIR interface for reporting the daily hospitalization incidence (bed occupancy)

### added

- added validation-service
  - This service deals with validation of notification or report messages sent to DEMIS system. Validation is done based on DEMIS FHIR profiles. Currently only bed occupancy profiles are supported.
- added hospital-location-service
  - This service provides information for hospital location data. For any valid IK-Number it provides a list of adresses of allowed/registered/known hospital-locations based on InEK-data.
- added report-processing-service
  - This service serves as a central processing point for report notifications to the DEMIS system. As a central interface, other services such as the validation service are addressed, the results are bundled and transferred to the NCAPI.
- added pdfgen-service
  - Service generating pdf documents from a thymeleaf template for a notification receipt for bed occupancy reports.


### fixed

- change pdf-generation Service
  - fixed the additional information on the exposure location is missing in the pdf receipt
  - quality enhancement
- change notification-entry-service
  - fixed V1 messages generate " generic internal server error"
  - quality enhancement
- change notification-clearing-api
  - quality enhancement

### security

- change pdf-generation-service
  - quality enhancement
- change notification-entry-service
  - quality enhancement
- change notification-clearing-api
  - quality enhancement

# Release 1.4.0
- add KIS interface (hospitalization)
- add Profile Package rki.demis.r4.core 1.22.0

# Release 1.3.1
update demis.yml to latest image versions

# Release 1.3.0
- adds processing of DEMIS Profile Package 1.21.0 (https://simplifier.net/packages/rki.demis.r4.core/1.21.0)
- enables backward compatibility for existing SARS-CoV-2 profile (https://simplifier.net/Covid-19Labormeldung)

# Release 1.2.0
- add processing of profiles 1.16.0 (https://simplifier.net/packages/demis.fhir.profiles/1.16.0)

Note: DEMIS Profile Package 1.16.0 is not backward compatible with the existing SARS-CoV-2 profile (https://simplifier.net/Covid-19Labormeldung). A fully backward compatible environment will be available soon. Therefore, this environment should only be used for testing with the new base profiles.

# Release 1.1.0
- add configurable Server Url and Port
- add processing of SARS-CoV-2, Influenca, Rotavirus (https://simplifier.net/demis)
- add Postgres DB with test notifications

# Release 1.0.1
DEMIS Docker TEST Environment 1.0.1 (DEMIS 1.8.2)

- update demis.yml

# Release 1.0.0
DEMIS Docker TEST Environment 1.0.0 (DEMIS 1.8.2)
- add demis.yml for DEMIS Test Environment
- add link to preconfigured DEMIS-Adapter
- add link to preconfigured DEMIS-Importer

