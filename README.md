# parity-openshift

This repository contains Docker [Parity](https://www.parity.io/) image based on [CentOS](https://www.centos.org/) alongside [OpenShift](https://www.openshift.com/) template based on that image.

## How to use this Docker image

### Install

Install the container:

```
docker pull dapowerplay/parity
```

Alternatively, pull a specific version:

```
docker pull dapowerplay/parity:1.9.5-centos
```

### Usage


## How to use this OpenShift template

### Install

Upload template to OpenShift cluster:

```
oc create -f parity-openshift-ephemeral.json
```

### Usage

Generate API object from template:

```
oc process parity-openshift | oc create -f -
```
