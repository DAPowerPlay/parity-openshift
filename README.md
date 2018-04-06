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

### OpenShift template - The GUI Way


![alt text][r1]

`Click 'Add to project', then 'Import YAML/JSON'`


![alt text][r2]

`Either c/p the Parity Openshift template or click Browse and upload the file.`


![alt text][r3]

`Add the template to your project and process the template`


![alt text][r4]

`Configure your Parity node, click Create`


![alt text][r5]

`If everything goes ok, you'll see a green checkmark`


![alt text][r6]

`Scale your Parity node.`


[r1]: assets/images/readme-1.png "Click some buttons"
[r2]: assets/images/readme-2.png "Then some more"
[r3]: assets/images/readme-3.png "Why not both?"
[r4]: assets/images/readme-4.png "Just click Create"
[r5]: assets/images/readme-5.png "Yay!"
[r6]: assets/images/readme-6.png "Yay! x2"
