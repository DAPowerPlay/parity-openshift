[![License: MIT](https://img.shields.io/badge/License-MIT-green.svg)](https://opensource.org/licenses/MIT) 
[![Pulls](https://shields.beevelop.com/docker/pulls/dapowerplay/parity.svg)](https://hub.docker.com/r/dapowerplay/parity/)
# parity-openshift

This repository contains **non-root** Docker [Parity](https://www.parity.io/) image based on [CentOS](https://www.centos.org/) alongside with [OpenShift](https://www.openshift.com/) template based on that image.

![alt text][r1]

## How to use this OpenShift templates - The GUI Way

Run a Parity Ethereum node on OpenShift for free in just a few clicks:

1) If you don't have your OpenShift instance, register an account on RedHats [OpenShift Online](https://manage.openshift.com/), or install [Minishift](https://github.com/minishift/minishift)

2) Pick a template
 
 - [Parity (Ephemeral)](/templates/parity-openshift-ephemeral.json)
 Ideal for just trying things out, spawns one Parity ethereum node. [Guidelines here,](/assets/GUIWAY.md)


 - [OpenShift Blockhain Consortium starter](/templates/parity-consortium-starter-openshift.json)
 For a more serious deployment; runs 1 Validator (authority) ethereum node running AuRa consensus algorithm, 3 load balanced, fatDB enabled, Secondary ethereum nodes, 1 Block explorer. [Guidelines here.](/assets/STARTER_TEMPLATE.md)


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


*"Creation is always an act of collaboration."*

:link::link::link:


Happy Coding! :fire:          :fire_engine:


[r1]: assets/images/starter-drawio.png ""


