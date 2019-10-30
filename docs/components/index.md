---
layout: default
title: Architecture and Data Flow
nav_order: 3
has_children: false
has_toc: false
---

# GrimoireLab Components

GrimoireLab toolkit is organized in the following repositories:

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
  * [SortingHat](https://github.com/chaoss/grimoirelab-sortinghat): projects contributors identity management
* Data consumption related components:
  * [Kibiter](https://github.com/chaoss/grimoirelab-kibiter): dashboard, downstream version of Kibana
  * [Sigils](https://github.com/chaoss/grimoirelab-sigils): visualizations and dashboards
  * [Manuscripts](https://github.com/chaoss/grimoirelab-manuscripts): reporting
* Platform management, orchestration, and common utilities:
  * [Mordred](https://github.com/chaoss/grimoirelab-mordred): orchestration
  * [GrimoireLab Toolkit](https://github.com/chaoss/grimoirelab-toolkit): common utilities
  * [Bestiary](https://github.com/chaoss/grimoirelab-bestiary): web-based user interface to manage repositories and projects for Mordred
  * [Hatstall](https://github.com/chaoss/grimoirelab-hatstall): web-based user interface to manage SortingHat identities

# GrimoireLab Architecture

Data flow through GrimoireLab components