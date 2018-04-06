![repotag][tag] ![license][license] ![dockerpulls][dockerpulls]
# parity-openshift

This repository contains **non-root** Docker [Parity](https://www.parity.io/) image based on [CentOS](https://www.centos.org/) alongside with [OpenShift](https://www.openshift.com/) template based on that image.

## How to use this Docker image

### Install

Install the image:

```
docker pull dapowerplay/parity
```

Alternatively, pull a specific version:

```
docker pull dapowerplay/parity:1.9.5-centos
```

### Usage

Start Parity container in working directory:

```
docker run -d dapowerplay/parity:1.9.5-centos --base-path=.
``````

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

### OpenShift template - The GUI Way

If you don't have your OpenShift instance, register an account on RedHats [OpenShift Online](https://manage.openshift.com/).

Once your Openshift project is ready, check out [GUI guidelines](/assets/GUIWAY.md) to run Parity and get access to Ethereum network on OpenShift. 


[tag]: 	https://img.shields.io/github/tag/dapowerplay/openshift-parity.svg
[license]: https://img.shields.io/github/license/dapowerplay/openshift-parity.svg
[dockerpulls]: https://img.shields.io/docker/pulls/dapowerplay/parity.svg

