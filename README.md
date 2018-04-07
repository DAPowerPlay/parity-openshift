[![License: MIT](https://img.shields.io/badge/License-MIT-green.svg)](https://opensource.org/licenses/MIT) 
[![Pulls](https://shields.beevelop.com/docker/pulls/dapowerplay/parity.svg)](https://hub.docker.com/r/dapowerplay/parity/)
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

*"Creation is always an act of collaboration."*

:link::link::link:


Happy Coding! :fire:          :fire_engine:


