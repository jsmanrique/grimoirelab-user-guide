---
layout: default
title: Docker Compose Install
nav_order: 2
parent: Install
---


# Instal GrimoireLab using Docker Compose

Use this method for installing GrimoireLab if you want to:

* have separate containers for databases
* insight to the different components required to run GrimoireLab


## Prerequisites

Make sure you have the following applications and services available:

- [Git](https://git-scm.com/book/en/v2/Getting-Started-Installing-Git)
- [Docker](https://docs.docker.com/v17.09/engine/installation/)
- [Docker Compose](https://docs.docker.com/compose/install/)
- [Docker Machine](https://docs.docker.com/machine/install-machine/)

You do this by running the following commands:

```bash
$ git --version
$ docker --version
$ docker-compose --version
$ docker-machine --version
```

Resources requirements depend on the number of projects and their size:
- Plan for a minimum of 100GB of storage, 2 CPUs, and 8 GB of RAM for a analyzing a small project.


## Get Docker Compose Instructions

The Docker Compose instructions `docker-compose.yml` are located in the GrimoireLab repository. Clone it to a local folder of your choice.

```bash
$ git clone https://github.com/chaoss/grimoirelab
$ cd grimoirelab/docker-compose
```


## Start GrimoireLab

Before starting GrimoireLab the first time, make sure to [set `vm.max_map_count` to at least `262144`](https://www.elastic.co/guide/en/elasticsearch/reference/current/docker.html#_set_vm_max_map_count_to_at_least_262144) for elasticsearch.

By default, GrimoireLab is ready to be started. 

```bash
$ docker-compose up -d
```
Once your containers are all started successfully, go to http://localhost:5601 

Manage contributors profile information with HatStall at http://localhost:8000 
To get access:
* User: admin
* Pass: admin

## Configure GrimoireLab

Configuration is done through two files:

* projects.json
* setup.cfg

Docker-Compose is by default configured to look for these files in the 'default-grimoirelab-settings' folder. 

```bash
$ cd ../default-grimoirelab-settings
```

The configuration is the same for all ways of installing GrimoireLab and thus explained in [the general installation page](./..).

## Error Handling

If you experience an error, run `docker-compose` up without the `-d` flag. That will output all messages and give insight to problems. 


### Unable to connect to Elasticsearch on first start?

By default, Elasticsearch will not work. This is a known problem: you need to [set `vm.max_map_count' to at least `262144'](https://www.elastic.co/guide/en/elasticsearch/reference/current/docker.html#_set_vm_max_map_count_to_at_least_262144). See the [elasticsearch documentation](https://www.elastic.co/guide/en/elasticsearch/reference/current/docker.html#_set_vm_max_map_count_to_at_least_262144) for how to do it on Linux, Mac, or Windows.


### Port already in use?

If an error reads something like “Error starting proxy: listen tcp 0.0.0.0:3306: bind: address already in use”, then you already have a program listening on a port, in this case port 3306 which would be the case if you are running an AMP with MySQL. 
To resolve this issue, stop the service that is already using a port GrimoireLab needs.
