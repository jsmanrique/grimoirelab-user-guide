---
layout: default
title: Install
nav_order: 2
has_children: true
has_toc: false
---

# Install GrimoireLab

GrimoireLab offers three options for installation:

* [Docker Compose](./docker-compose)
  - Use `docker-compose` if you want separate containers for the database.
* [Docker](./docker)
  - Use `docker` if you want to work with one self-contained container that includes everything.
* [PIP](./pip)
  - Use `pip` if you want to use GrimoireLab components individually.

Regardless of which way you install GrimoireLab, you will need to configure it as described below.

## Define analysis scope

### Tell GrimoireLab what projects to collect data from

GrimoireLab needs to know what projects to collect data from. 
The default [projects.json](https://github.com/chaoss/grimoirelab/blob/master/default-grimoirelab-settings/projects.json) file is configured to collect metrics about the GrimoireLab git repository. 

To start collecting data about the projects that matter to you, you need to define projects and data endpoints in the project.json file.
The [GrimoireLab tutorial section on the projects file](https://chaoss.github.io/grimoirelab-tutorial/sirmordred/projects.html) explains how the file needs to be built.

### Provide API keys and other configurations

In addition to defining projects and their data endpoints, specific data endpoints need to be activated in GrimoireLab.
The default [setup.cfg](https://github.com/chaoss/grimoirelab/blob/master/default-grimoirelab-settings/setup.cfg) has only `git` enabled.

Enabling additional data endpoints, such as GitHub issues and pull requests, involves (1) uncommenting relevant sections in the setup.cfg and (2) providing API keys.


## Deploy and run GrimoireLab

TBD