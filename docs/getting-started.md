# Getting started

Welcome to the VinDr Lab project. This section helps you deploy VinDr Lab, please visit our original manual at [deployment repository](https://github.com/vinbigdata-medical/vindr-lab-deployment) !

## Start it up

There are two ways to deploy our project are:

**Option 1: Kubernetes**

**Option 2: Docker**

and the instruction is going to be described below. But we think using Kubernetes will be more interting.

## Kubernetes

### Prerequisites

Install the <a href="https://k3s.io/">k3s</a> at first. But please remind that we will use `ingress-nginx` for routing purposes, it conflicts with default component of k3s is traefik, so you just need to disable that. Please follow this <a href="https://github.com/k3s-io/k3s/issues/1160" target="_top">issue</a> to fix.

### Run

- First, you must initialize the namespace for these deployments by running: `kubectl create namespace vinlab`

- Then, go in to the kubernetes folder, and create the config map: `sh ./create_config_map.sh`

- As you can see, we use ingress-nginx to load-balance and route endpoints.
  First, create a specific namespace for it by: `kubectl create namespace vingress` then install the `ingress-nginx`:

```
helm repo add ingress-nginx https://kubernetes.github.io/ingress-nginx
helm repo update

helm install ingress-nginx ingress-nginx/ingress-nginx -n ingress
```

- Next step, just run `kubectl apply -f .`

## Docker

### Prerequisites

To deploy using Docker, yes, install docker first

### Run

We've already made it as simple as we can. Just go to the docker directory then run: `sh ./run.sh` and double check by `docker ps`

## Relevants

### Keycloak

We use Keycloak as an user management system (users, roles, permissions...), please follow [this link](https://github.com/vinbigdata-medical/vindr-lab-deployment/blob/master/KEYCLOAK.md) to complete the installation.

### MinIO

MinIO is being used to store some other things from the API. There is a small setup to do. After launching the whole system, please visit [MinIO url](http://localhost:8080/minio), then login with the keys we provided, feel free to change it to whatever you want but remember that.

## Endpoints

| Name     | Endpoint                              |
| -------- | ------------------------------------- |
| Main     | `http://localhost:8080`               |
| Backend  | `http://localhost:8080/api`           |
| Orthanc  | `http://localhost:8080/dicomweb`      |
| Keycloak | `http://localhost:8080/auth`          |
| ES       | `http://localhost:8080/elasticsearch` |
| MinIO    | `http://localhost:8080/minio`         |

---

Have fun!

&nbsp;