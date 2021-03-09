# Developer guide

## Components

**Vinlab** is composed by multiple microservices.

### UI

**vinlab-frontend**: The code for UI, mainly derived from OHIF.

### Backend

- **vinlab-backend**: A REST API service writen in Go,handles all the
  logic under the vinlab excepts the DICOM uploading.
- **vinlab-uploader**: A REST API service handles the DICOM
  uploading. This service is writen in Python to utitlize the
  excellent PyDicom, a Dicom manipulation library.

### Databases:

- **Orthanc** : Used as the DICOM storage.
- **Elasticsearch**: Used as the primary storage service storing all
  objects defined by **Vinlab**.
- **Redis**: Providing the locking mechanism.

### User management

- **Keycloak**: Keycloak is used as a Identity Access Management service,
  providing the authentication and access control. Keycloak must be
  initialized with predefinded user roles and rules.

## Contribution guideline

### Scope

The Vinlab benefits from the works of many excellent opensource
projects. If you have any improvements related to the upstream
projects, please contribute these changes to the upstreams' offical
repositories.

This development guide only apply to works made by Vinlab team and is
specific to the business logic of Vinlab.
