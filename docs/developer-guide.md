# Development guide

## Scope

Vinlab benefits from the works of many excellent opensource
projects. If you have any improvements related to the upstream
projects, please contribute these changes to the upstreams' offical
repositories.

This development guide only apply to works made by **Vinlab Team** and
is specific to the logic of Vinlab.

## Contribution guideline

If you have any idea that might improve **Vinlab**, feel free to make
a _feature request_ in the repo **vinlab-frontend**.

If you have any feature implementation, bug fixing, or any code that
improve a part of **Vinlab** , please making **pull request** to the
associate repos. It is more that welcome if those pieces of code are
documented and tested.

## Overview

**Vinlab** is composed by multiple microservices. The deployment of
those services can vary according to the use case. **Vinlab Team**
provides some recipes to quickly deploy **Vinlab** in a repository
named **recipes**.

### UI

**vinlab-frontend**: The code for UI, mainly derived from OHIF.

### Backend

- **vinlab-api**: A REST API service writen in Go,handles all the
  logic under the vinlab excepts the DICOM uploading.
- **vinlab-uploader**: A REST API service handles the DICOM
  uploading. This service is writen in Python to utitlize the
  excellent PyDicom, a Dicom manipulation library.
- **id-generator**: A service that generates **id** for vinlab
  objects.

### Databases:

- **Orthanc** : Used as the DICOM storage.
- **Elasticsearch**: Used as the primary storage service storing all
  objects defined by **Vinlab**.
- **Redis**: Providing the locking mechanism.
- **rqlite**: Small database service shipped with **id-generator**.

### User management

- **Keycloak**: Keycloak is used as a Identity Access Management service,
  providing the authentication and access control. Keycloak must be
  initialized with predefinded user roles and rules.
