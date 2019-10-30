---
layout: default
title: About
nav_order: 1
permalink: /
---

# About GrimoireLab

GrimoireLab is a 100% free, open source toolset from [CHAOSS](https://chaoss.community) to do software
development analytics, that includes:

* Automatic and incremental **data gathering** from the tools (*data source*) related with software development (source code management, issue tracking systems, forums, etc.).
* Automatic gathered **data processing** like merging duplicated identities, adding additional information about contributors affiliation, calculation delays, geographical data, etc.
* **Data consumption**, including **data visualization**, allowing filtering by time range, project, repository, contributor, etc.

# Quick Start

Using `docker-compose`

Requirements: 
* Software:[git](https://git-scm.com/), [docker client](https://docs.docker.com/install/), and [docker compose](https://docs.docker.com/compose/install/). As an example of working configuration:
```console
root@test-68b8628f:~# git --version
git version 2.17.1
root@test-68b8628f:~# docker --version
Docker version 19.03.1, build 74b1e89
root@test-68b8628f:~# docker-compose --version
docker-compose version 1.22.0, build f46880fe
```
* Hardware: 2 CPUs, 8GB memory RAM and [enough virtual memory for Elasticsearch](https://www.elastic.co/guide/en/elasticsearch/reference/current/vm-max-map-count.html) 

Steps:
1. Clone GrimoireLab project
```console
foo@bar:~$ git clone https://github.com/chaoss/grimoirelab
```
2. Go to `docker-compose` folder and run the following command:
```console
foo@bar:~$ cd grimoirelab/docker-compose
foo@bar:~/grimoirelab/docker-compose$ docker-compose up -d
```

Your dashboard will be ready after a while in `https://localhost:5601`
