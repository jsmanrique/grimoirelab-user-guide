---
layout: default
title: Docker Install
nav_order: 2
parent: Install
---

# Install GrimoireLab using `docker run`

Use `docker run` if you want to work with one self-contained container that includes everything.


## Prerequisites

* **Software**: 
- [Git](https://git-scm.com/book/en/v2/Getting-Started-Installing-Git)
- [Docker](https://docs.docker.com/v17.09/engine/installation/)

You do this by running the following commands:

```console
$ git --version
$ docker --version
```

* **Hardware**: Resources requirements depend on the number of projects and their size:
  - Plan for a minimum of 100GB of storage, 2 CPUs, and 8 GB of RAM for a analyzing a small project.

## Start GrimoireLab

1. Clone the github.com/chaoss/grimoirelab project repository
```console
$ git clone https://github.com/chaoss/grimoirelab
```

2. Go to the project folder 
```console
$ cd grimoirelab
```

3. Run the following command
```console
$ docker run -p 127.0.0.1:5601:5601 \
-v $(pwd)/default-grimoirelab-settings/projects.json:/projects.json \
-v $(pwd)/default-grimoirelab-settings/setup.cfg:/setup.cfg \
-t grimoirelab/full
```

More details in the [docker folder](https://github.com/chaoss/grimoirelab/blob/master/docker/).

Your dashboard will be ready after a while in `http://localhost:5601`

## Configure GrimoireLab

Configuration is done through two files:

* projects.json
* setup.cfg

Above `docker run` commands looks for these files in the 'default-grimoirelab-settings' folder. 

```console
$ cd ../default-grimoirelab-settings
```

The configuration is the same for all ways of installing GrimoireLab and thus explained in [the general installation page](./..).