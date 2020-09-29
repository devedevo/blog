---
layout: post
title: Set up Portainer for remote control on QNAP NAS
description: How to set up Portainer on various platforms.
date: 2020-09-29
author: Hardy Scheel
tags: [Docker, Portainer, QNAP]
published: true
---

### Table of content
* [Deploy Portainer within Docker for Linux or Windows](#Deploy-Portainer-within-Docker-for-Linux-or-Windows)
    * [Using docker compose](#Using-docker-compose)
    * [Further information](#further-information)
* [Deploy Portainer on a QNAP NAS](#Deploy-Portainer-on-a-QNAP-NAS)
    * [Best practices](#Best-practices)
    * [Further information](#further-information)
* [Remote control Portainer on a QNAP NAS](#Remote-control-Portainer-on-a-QNAP-NAS)
    * [Modify your QNAP NAS to accept Portainer connections](#Modify-your-QNAP-NAS-to-accept-Portainer-connections)
    * [Further information](#further-information)

---

## Deploy Portainer within Docker for Linux or Windows

Portainer consists of two elements: the Portainer server and the Portainer agent. Both elements run as lightweight Docker containers on a Docker engine.

Deploy Portainer on Linux or Windows Docker host with Linux backend e.g Windows WSL 2 or Linux containers.

Create a container called `portainer_data`:
```shell
$ docker volume create portainer_data
```

```shell
$ docker run -d -p 8000:8000 -p 9000:9000 --name=portainer --restart=always -v /var/run/docker.sock:/var/run/docker.sock -v portainer_data:/data portainer/portainer-ce
```

Note:
* Access the Portainer gui on port 9000 within a web browser.
* Portainer agent is not needed on Docker standalone hosts.
* Port 8000 is used exclusively by the EDGE agent for the reverse tunnel function. If you don't use this port you can left it out.

### Using docker compose

It is a way more comfortable to use a single file with all configuration in it. The shell command above will look like this in a docker compose yaml file. Store it in a file called `docker-compose.yml`:
```yaml
version: '3'

services:
    portainer:
        container_name: portainer
        image: portainer/portainer
        restart: always
        ports:
            - "8000:8000"
            - "9000:9000"
        volumes:
         - /var/run/docker.sock:/var/run/docker.sock
         - portainer_data:/data portainer/portainer-ce

volumes:
    portainer_data:
```

**Deploy it** (within the same folder as the *.yml file is):
```shell
$ docker-compose up -d
```
This runs docker compose in detached mode, pulls the needed Docker images, and starts the containers

**Shut down**
```shell
$ docker-compose down
```
This removes the containers and default network, but preserves the data.

**Shut down and clean up**
```shel
$ docker-compose down --volumes
```
This removes the containers, network and also the persistent data which is stored in a volume.

### Further information
* https://www.portainer.io/installation/

---

## Deploy Portainer on a QNAP NAS

Use a Docker Compose file as `qnap-portainer.yml` with the following configuration:
```yaml
version: '3'
services:
     portainer:
         container_name: portainer
         image: portainer/portainer
         restart: always
         ports:
         - "9000:9000"
         volumes:
         - /var/run/docker.sock:/var/run/docker.sock
         - /share/Docker/portainer:/data
```

Now **deploy** Portainer with the help of this Docker Compose configuration file on your QNAP NAS. Copy it to a location of your choice e.g. ~/. Log onto the QNAP NAS with ssh an navigate to the folder where the yaml configuration file is. And deploy the container:

```shell
$ docker-compose -f qnap-portainer.yml up -d
```

**Shut down**
```shell
$ docker-compose -f qnap-portainer.yml down
```
This removes the containers and default network, but preserves the data.

**Shut down and clean up**
```shel
$ docker-compose -f qnap-portainer.yml --volumes
```
This removes the containers, network and also the persistent data which is stored in a volume.

### Best practices

* Store persistent data in a location other than `Container` (QNAP Container Station default folder). E.g. in a new shared folder `Docker`. The path would `/share/Docker`.
* Use Docker Compose to build containers using a yaml config file.

### Further information

* [Best practices for Docker on QNAP NAS](https://mwunderling.com/blog/qnapcontainertips.html)
* [Install Portainer on QNAP NAS](https://mwunderling.com/blog/portainerconfig.html)

---

## Remote control Portainer on a QNAP NAS

### Modify your QNAP NAS to accept Portainer connections

If you want to connect to your QNAP NAS Portainer instance from another computer, then follow these instructions:

1. Open Container Station and go to: `Preferences -> Docker Certificate`.
2. Click the Download button to save a zipped certificate to your PC.
3. Unzip the certificate file on your computer.
4. Upload the zipped certificate file to `/share/Container/` on your QNAP  NAS.
5. Login to your NAS via SSH (`$ ssh admin@<your-qnap-nas>`) with admin privileges.
6. Create a hidden directory by executing `mkdir -pv ~/.docker`
7. Unzip and copy the cert file contents to the hidden directory:
`$ unzip /share/Container/cert.zip -d ~/.docker`
8. Now use this command: `$ export DOCKER_HOST=tcp://192.168.xxx.xxx:2376 DOCKER_TLS_VERIFY=1` Update this line with your NAS’s IP address.

### Connect o the QNAP NAS Portainer instance

On another Portainer instance on a different computer add QNAP Container Station/Portainer as an endpoint to Portainer:

1. Add an endpoint: Choose `Docker - Directly connect to the Docker API`.
2. The endpoint URL is the same as above including the port number: `192.168.xxx.xxx:2376`
3. Turn on `TLS` and choose: `TLS with server and client verification`.
4. Use the unzipped certificate files from your QNAP NAS:
    * TLS CA certificate == ca.pem
    * TLS certificate == cert.pem
    * TLS key == key.pem
5. You now can remote control your QNAP NAS.

### Further information

* [Configure Portainer remote access](https://mwunderling.com/blog/portainerconfig.html)