# Development guide

## Scope

VinDr Lab benefits from the works of many excellent opensource
projects. If you have any improvements related to the upstream
projects, please contribute these changes to the upstreams' offical
repositories.

This development guide only apply to works made by **VinDr Lab Team** and
is specific to the logic of VinDr Lab.

## Contribution guideline

If you have any idea that might improve **VinDr Lab**, feel free to make
a _feature request_ in the repo **vinlab-frontend**.

If you have any feature implementation, bug fixing, or any code that
improve a part of **VinDr Lab** , please making **pull request** to the
associate repos. It is more that welcome if those pieces of code are
documented and tested.

## Overview

**VinDr Lab** is composed by multiple microservices. The deployment of
those services can vary according to the use case. **VinDr Lab Team**
provides some recipes to quickly deploy **VinDr Lab** in a repository
named **recipes**.

### UI

**vinlab-frontend**: The code for UI, mainly derived from OHIF.

### Backend

- **vinlab-api**: A REST API service writen in Go, handles all the
  logic under the vinlab excepts the DICOM uploading.
- **vinlab-uploader**: A REST API service handles the DICOM
  uploading. This service is writen in Python to utitlize the
  excellent PyDicom, a Dicom manipulation library.
- **id-generator**: A service that generates **id** for vinlab
  objects.

### Databases

- [**Orthanc**](https://www.orthanc-server.com/) : Used as the DICOM storage.
- [**Elasticsearch**](https://www.elastic.co/): Used as the primary storage service storing all
  objects defined by **VinDr Lab**.
- [**Redis**](https://redis.io/): Providing the locking mechanism.
- [**rqlite**](https://github.com/rqlite/rqlite): Small database service shipped with **id-generator**.

### User management

- [**Keycloak**](https://www.keycloak.org/): Keycloak is used as a Identity Access Management service,
  providing the authentication and access control. Keycloak must be
  initialized with predefinded user roles and rules.

&nbsp;