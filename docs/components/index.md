---
layout: default
title: Components
nav_order: 3
has_children: false
has_toc: false
---

# GrimoireLab Components

GrimoireLab is composed of different tools, which are summarized in the following figure below and listed below:

![](../../assets/grimoirelab-all-details.png)

* Data retrieval related components:
  * [Perceval](https://github.com/chaoss/grimoirelab-perceval): retrieval of data from data sources
    * [Perceval (bundle for OPNFV)](https://github.com/chaoss/grimoirelab-perceval-opnfv)
    * [Perceval (bundle for Mozilla)](https://github.com/chaoss/grimoirelab-perceval-mozilla)
    * [Perceval (bundle for Puppet)](https://github.com/chaoss/grimoirelab-perceval-puppet)
    * [Perceval (bundle for FINOS)](https://github.com/Bitergia/grimoirelab-perceval-finos)
  * [Graal](https://github.com/chaoss/grimoirelab-graal): source code analysis with external tools
  * [KingArthur](https://github.com/chaoss/grimoirelab-kingarthur): batch processing for massive retrieval
* Data enrichment related components:
  * [GrimoireElk](https://github.com/chaoss/grimoirelab-elk): storage and enrichment of data
  * [Cereslib](https://github.com/chaoss/grimoirelab-cereslib): generic data processor
  * [SortingHat](https://github.com/chaoss/grimoirelab-sortinghat): projects contributors identity management
* Data consumption related components:
  * [Kibiter](https://github.com/chaoss/grimoirelab-kibiter): dashboard, downstream version of Kibana
  * [Sigils](https://github.com/chaoss/grimoirelab-sigils): visualizations and dashboards
  * [Kidash](https://github.com/chaoss/grimoirelab-kidash): visualizations and dashboards manager
  * [Manuscripts](https://github.com/chaoss/grimoirelab-manuscripts): reporting
* Platform management, orchestration, and common utilities:
  * [Mordred](https://github.com/chaoss/grimoirelab-mordred): orchestration
  * [GrimoireLab Toolkit](https://github.com/chaoss/grimoirelab-toolkit): common utilities
  * [Bestiary](https://github.com/chaoss/grimoirelab-bestiary): web-based user interface to manage repositories and projects for Mordred
  * [Hatstall](https://github.com/chaoss/grimoirelab-hatstall): web-based user interface to manage SortingHat identities